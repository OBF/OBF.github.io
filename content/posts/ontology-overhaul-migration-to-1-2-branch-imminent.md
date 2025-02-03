---
author: hilmar
category:
  - bioperl
date: "2003-03-10T20:27:40+00:00"
guid: http://news.open-bio.org/news/?p=77
summary: |-
  This is the last call for people to test drive and/or criticize the Bio::Ontology & Bio::OntologyIO re-design and implementation.

  The interfaces and modules to look at comprise of Bio::Ontology::OntologyI, Bio::Ontology::TermI, and Bio::OntologyIO. If you care about implementations (as Aaron says most people do rather than bothering with interfaces), check out Bio::Ontology::Ontology, Bio::Ontology::Term, and Bio::OntologyIO.
title: 'Ontology overhaul: migration to 1.2 branch imminent'
url: /2003/03/10/ontology-overhaul-migration-to-12-branch-imminent/

---
This is the last call for people to test drive and/or criticize the Bio::Ontology & Bio::OntologyIO re-design and implementation.

The interfaces and modules to look at comprise of Bio::Ontology::OntologyI, Bio::Ontology::TermI, and Bio::OntologyIO. If you care about implementations (as Aaron says most people do rather than bothering with interfaces), check out Bio::Ontology::Ontology, Bio::Ontology::Term, and Bio::OntologyIO.

This is the last call for people to test drive and/or criticize the Bio::Ontology & Bio::OntologyIO re-design and implementation.

The interfaces and modules to look at comprise of Bio::Ontology::OntologyI, Bio::Ontology::TermI, and Bio::OntologyIO. If you care about implementations (as Aaron says most people do rather than bothering with interfaces), check out Bio::Ontology::Ontology, Bio::Ontology::Term, and Bio::OntologyIO. If you are curious about OntologyEngineI implementations (which basically are the ones powering queries on terms and all their relationships), check out Bio::Ontology::OntologyEngineI for the interface definition and Bio::Ontology::SimpleGOEngine and Bio::Ontology::SimpleOntologyEngine for the currently existing implementations.

Make yourself heard if you think something needs to be amended or changed or whatever; after the release of 1.2.1 you will meet reluctance to change the branch API.

Unless there are objections or ensuing debates what should be changed before release, I'll start migrating to the branch tomorrow, aiming for a release by the end of the week (Friday).
