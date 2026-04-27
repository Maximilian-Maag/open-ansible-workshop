# open-ansible-workshop
A challenge based workshop to learn ansible. English version below.

Ein Challenge basierter workshop, um den Umgang mit Ansible zu lernen.
Dieser Workshop sollte in einer Gruppe von ca. 4 - 6 Personen abgehalten werden. Größere Gruppen sind zwar möglich machen die Betreuung einzelner Teilnehmer schwieriger. Es wird empfohlen mehrere Kleingruppen zu bilden, um Einzelpersonen das erreichen der Lernziele des Workshops zu erleichtern.

## Konzept
Die Teilnehmer bekommen eine von zwei Rollen zugewiesen. Entweder Rabbit oder Huntsman. Nach einem gemeinsamen Kickoff dauert der Workshop 14 Tage. Nach der Hälfte der Zeit werden die Rollen getauscht. Die Teilnehmer werden in Paare aus einem Rabbit und einem Huntsman eingeteilt und versuchen schneller als der jeweils Andere Ihre zugewiesenen Challenges abzuschließen.

Die Challenges der Rabbits zielen darauf ab mehr Infrastrutktur zu deployen als die Huntsman managen können.

Siegesbedingung für den Rabbit: Es müssen am Ende des Zeitlimits mehr Server deployed werden als im Inventory des Huntsman gemanged werden.

Siegesbedingung für den Huntsman: Sämtliche Infrastruktur des Rabbit muss in einem Ansible Inventory am Ende des Zeitlimits gemanged sein.

Zusätzlich zu den Siegesbedingungen müssen alle Huntsman bzw. Rabbit Challenges abgeschlossen sein.

### Huntsman
Huntsman soll sich damit beschäftigen bestehende Infrastruktur in einem Ansible Repositor zu organisieren. Management hosts sollen errichtet und verwaltet werden. Das Reale Problem des IT Wildwuchs soll verstanden und durch Ansible behoben werden. Es ist ein gut organisiertes Inventar zu führen und gezielt playbooks auf bestehende Hostgruppen anzuwenden. Ein Namenskonzept soll entwickelt und angewandt werden. Huntsman nehmen eine ordnende Rolle ein. Sie fangen den Wildwuchs der Rabbits ein.

### Rabbit
Rabbits sind dafür verantwortlich möglichst viele Workloads zu deployend, damit diese mit Ansible verwaltet werden können. Die Aufgabe der Rabbits ist es IT Infrastruktur schneller zu deployen, als diese von Huntsman organisiert und gemanged werden können. Rabbits konzentrieren sich während der Übung darauf repitive Aufgaben auf einzelnen Hosts zu automatisieren.

## Setup



