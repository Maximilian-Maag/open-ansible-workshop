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
Für beide Gruppen gilt folgendes Setup:
Es muss ein SSH keypair erstellt werden.
 - Ein Keypair wird auf der lokalen Maschine erstellt.
 - Nur der Public Key wird auf andere Maschinen kopiert, um ssh zugriff zu ermöglichen.

Alle Teilnehmer erhalten einen API Token und ein Testnotebook.
In der Testumgebung, Linode, wird ein Domaincontroller angelegt.
Jede Maschine, die von einem Rabbit deployed wird muss mit einem A und einem AAAA Record auf die deployte Maschine zeigen. Folgendes Namenskonzept ist dabei zu beachten:

```
rabbitname-servernumber.simple-test.org
```

### Rabbit setup
Rabbits müssen in der lage sein Infrastruktur zu deployen.
Für das Deployment sind Terraformskripte zu verwenden.
Das OS Management auf der jeweiligen Maschine erfolgt mittels Ansible.
Als Master Node kann das eigene Notebook verwendet werden.
Für jede beschriebene Challenge ist das Deployment der passenden Infrastruktur mittels Terraform vor zunehmen und die Aufgabe mittels eines Ansibleskripts zu lösen. Auf jeder Deployten VM muss der Huntsmann zugriff erhalten, um diese in sein Inventory aufnehmen zu können.

### Huntsman setup
Huntsmann müssen MINDESTENS einen Master Node als VM deployen. Hierauf wird der Ansible Master Node installiert. Diese Maschine erzeugt ein Keypair. Der Public Key dieses Keypairs muss an den jeweiligen Rabbit übergegen werden. Zusätlich zum Keypair auf dem Master Node muss ein lokales Keypair erzeugt werden, um den Master Node mittels SSH zu verwalten.
