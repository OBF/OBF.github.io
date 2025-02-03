---
author: stajich
category:
  - code
date: "2005-11-20T18:25:04+00:00"
guid: http://bioperl.open-bio.org/?p=15
summary: |-
  I've updated the code for [Bio::Tree::Node](http://doc.bioperl.org/bioperl-live/Bio/Tree/Node.html) so that each\_Descendent can return the nodes in alphabetical order. This is achieved by pasing in the string 'alpha' (for alphabetical) or 'revalpha' (for reverse alphabetical). For internal nodes, they are sorted in order of the min or max (alphabetically) node in the sub-clade.

  In addition, you can request the order of writing nodes by [Bio::TreeIO::newick](http://doc.bioperl.org/bioperl-live/Bio/TreeIO/newick.html) by passing in the -order\_by flag which can be 'alpha', 'revalpha', 'height', or 'creation'.

  So you can use it like
title: sort order for Bio::Tree::Node each_Descendent
url: /2005/11/20/sort-order-for-each_descendent/

---
I've updated the code for [Bio::Tree::Node](http://doc.bioperl.org/bioperl-live/Bio/Tree/Node.html) so that each\_Descendent can return the nodes in alphabetical order. This is achieved by pasing in the string 'alpha' (for alphabetical) or 'revalpha' (for reverse alphabetical). For internal nodes, they are sorted in order of the min or max (alphabetically) node in the sub-clade.

In addition, you can request the order of writing nodes by [Bio::TreeIO::newick](http://doc.bioperl.org/bioperl-live/Bio/TreeIO/newick.html) by passing in the -order\_by flag which can be 'alpha', 'revalpha', 'height', or 'creation'.

So you can use it like

```

my $treeio = Bio::TreeIO->new(-format => 'newick',
                              -file => 'file.tre');
my $tree = $treeio->next_tree;
for my $internal ( grep { ! $internal->is_Leaf } $tree->get_nodes ) {
 # this will get the nodes in alphabetical order
  my @subclade = $internal->each_Descendent('alpha');
}
my $out = Bio::TreeIO->new(-format =>'newick',
                           -order_by => 'alpha',
                           -file => 'sorted.tre');
$out->write_tree($tree);

```

This code is in [CVS](/wiki/index.php/CVS) now.

Also, I fixed the code reference option so that arbitrary functions can be passed in. Here is an example which prints out the nodes from a nexus formated tree file.

```

use Bio::TreeIO;
use strict;
my $treeio = Bio::TreeIO->new(-format => 'nexus',
			      -file   => shift);

my $tree = $treeio->next_tree;

print join(",",map { $_->id }
             $tree->get_root_node->each_Descendent(&my_sort_routine)), "n";

sub my_sort_routine {
 my ($aa,$bb) = @_;
 if( $aa->is_Leaf && $bb->is_Leaf ) {
   return $aa->id cmp $bb->id;
 } elsif( $aa->is_Leaf ) {
  my ($left) = sort { $a->id cmp $b->id }
              grep {$_->is_Leaf } $bb->get_all_Descendents;
  return $aa->id cmp $left->id;
 } elsif( $bb->is_Leaf ) {
  my ($left) = sort { $a->id cmp $b->id }
             grep {$_->is_Leaf } $aa->get_all_Descendents;
  return $left->id cmp $bb->id;
 } else {
   my ($left) = sort { $a->id cmp $b->id }
               grep {$_->is_Leaf } $aa->get_all_Descendents;
   my ($right) = sort { $a->id cmp $b->id }
              grep {$_->is_Leaf } $aa->get_all_Descendents;
   return $left->id cmp $right->id;
 }
}

```
