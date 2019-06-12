## Inhaltsverzeichnis

* 01 - [Kapitel 701.1 Modern Software Development](#701.1)
* 02 - [Kapitel 701.3 Source Code Management](#701.3)
* 03 - [Kapitel 701.4 Continuous Integration and Continuous Deliver](#701.4)
* 04 - [K4](#k4-)
* 05 - [K5](#k5-)

## Fahrplan
***


| Datum | behandelte Unterrichtsinhalte: | Gewichtung |
| -------- | ------ | -------- |
| 15.05.19 | Installation SW, Einrichten Linux VM(s)<br>[701.1 Modern Software Development, 1. Teil](https://github.com/w901-fr19-mi/E701#7011-modern-software-development) | 6 |
| 22.05.19 | [701.1 Modern Software Development, 2. Teil](https://github.com/w901-fr19-mi/E701#7011-modern-software-development) | 4 |
| 29.05.19 | [701.3 Source Code Management](https://github.com/w901-fr19-mi/E701#7013-source-code-management) | 5 | 
| 05.06.19 | 702.1 Container Usage, 1. Teil | 7 |
| 12.06.19 | 702.1 Container Usage, 2. Teil | (7) |
| 19.06.19 | 702.2 Container Deployment and Orchestration | 5 |
| 26.06.19 | LB1 Theoretische Prüfung und Abschluss LB2 | - |
| 03.07.19 | Sommersporttage | - |
|          | Total Punkte | 27 (34) ! |

Kapitel aus E701 wurden in der Gruppe mit .... erarbeitet. Davon sind mindestens 14 Punkte selbständig erarbeitet worden. 

## Dokumention des Lern- und Entwicklungsprozesses
***

### Kapitel: 701.1 Modern Software Development <a name="701.1">

**Weight**: 6 (4)

**Beschreibung** Aufweisung, wie man eine Containerumgebung einrichtet. Die Begriffe Security, Performenz, Erreichbarkeit, Loadbalancing etc. werden nach diesem Topic bekannt sein.

**Tagesziele**, Mit einem eigenem erstellten Container werde ich verstehen, wie die funktionalität einer Containerumgebung funktioniert. Dafür werde ich zusätzlich einen Mikroprozess erstellen, welcher mir aufzeigt, wie einer funktioniert.

**Vorgehen**, In den Unterlagen war ein Video vorhanden, dass ausführlich erklärt hat, wie ein Mikroprozess funktioniert

**Beispiele und Arbeitsergebnisse**

| Linux          | Container      | Beschreibung      |
| -------------- | -------------- | ----------------- |
| Namespaces     | laufender Container | beim Starten des Containers wird in eine andere Linux Namespace gewechselt |
| UnionFS        | Image Layer         | Container Verwenden UnionFileSysteme um .... |
| Unix Prozesse  | run/start/stop      | docker run/start/stop Befehle ähneln dem .... Subsystem |

**Fazit und Aussicht**, z.B. Die Durcharbeitung von ... gab mir ein besseres Verständnis über die Funktionsweise von Containern.

## Links

* [Exam 701: DevOps Tools Engineer](https://www.lpi.org/our-certifications/exam-701-objectives) 
* [E701 Dokumentation](https://github.com/w901-fr19-mi/E701)
* [myE701 Original Repository](https://github.com/w901-fr19-mi/myE701) 

***
### Kapitel: 701.3 Source Code Management <a name="701.3">

**Weight**: 6 (4)
**Beschreibung** Kandidaten sollten in der Lage sein, Git zur Verwaltung und Freigabe von Quellcode zu verwenden. Dazu gehören das Erstellen und Beitragen zu einem Repository sowie die Verwendung von Tags, Zweigen und Remote-Repositories. Darüber hinaus sollte der Kandidat in der Lage sein, Dateien zusammenzuführen und Konflikte zu lösen.

**Tagesziele**, 
* Git als Repository verstehen
* Dateistruktur von Git verstehen
* Verwaltung von branches, tags und forks verstehen

**Vorgehen**, Ich versuche selber ein GIT Repo zu erstellen, welchen ich selber verwalten werde. Danach schaue ein informatives Video an, welches mir die Grundlagen von GIT näher beibringt.

**Beispiele und Arbeitsergebnisse**
Hier zeige ich auf, wie git mit VisualStudioCode verwalte. Mit Markdown kann ich gewisse Steuerelemente verwalten. z.B eine Tabelle wird hier mit dem Pipe Symbol getrennt.

![VisualStudioCodeMarkdown](/images/VisualStudioCodeGIT.png)

*Branch* Ein Branch ist eine isolierte Entwicklungszone. Hier testet man einzelne Skripts oder Programme bevor sie in die Produktion kommen.
Man kann Beispielsweise eine Entwicklungszone mit git branch "Name" einrichten und von dort aus ausserhalb der Produktiven Zone arbeiten. Da man getrennt ist, wird die "master" Umgebung nicht beinträchtig. 

*Tags* Tags sind Referenzen für eine bestimmte Version einer GIT Datei

*Forks* Wenn man ein bestimmmtes GIT Repository forked, dann zieht man eine eigene Version auf das eigene GIT

**Commands**
| Commands | Bedeutung |
| -------------- | -------------- |
| git branch | Mit diesem Befehl listet man alle Branches im eigenem Repo auf. Ebenfalls ist es möglich eigene Branches zu erstellen oder zu dem genannten Branch zu wechseln |
| git checkout | Mit diesem Befehl wechselt man einen Branch |
| git commit | Damit ruft man eine Bestätigung für eine gespeicherte Aktion aus |
| git clone | Mit diesem Befehl klont man lokal ein Repository aus einem Git |

**Fazit und Aussicht**, Durch dieses Kapitel wurden mir die Grundlagen der Gitverwaltung beigebracht. Dabei habe ich viele verschiedene Perspektiven in der Gitumgebung gesehen. Forken, Tags, Branch sind mir neue gelernte Begriffe. Ich kann nun mit GIT zukünftig meine Dokumentationen schreiben und Versionsgezielt arbeiten.

## Links

* [Git scm Basic Branches](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging) 
* [Git Buch](https://git-scm.com/book/de/v2)
* [myE701 Original Repository](https://github.com/w901-fr19-mi/myE701) 


### Kapitel: 701.4 Continuous Integration and Continuous Deliver <a name="701.4">

**Weight**: 5 + 5 Bonuspunkte für Aussetzen eines eigenes Projektes (Microservice) und dessen CI/CD mittels Jenkins.

**Beschreibung** Gegenüberstellung welche Linux Technologien für Container verwendet werden.

**Tagesziele**, z.B. Erstellung einer Tabelle Linux - Container. 

**Vorgehen**, z.B. Studieren Background Linux Namespaces vs. Container, UnionFS vs. Container Layer, Unix Prozesse (Jobs) vs. Docker run/start/stop

**Beispiele und Arbeitsergebnisse**

| Linux          | Container      | Beschreibung      |
| -------------- | -------------- | ----------------- |
| Namespaces     | laufender Container | beim Starten des Containers wird in eine andere Linux Namespace gewechselt |
| UnionFS        | Image Layer         | Container Verwenden UnionFileSysteme um .... |
| Unix Prozesse  | run/start/stop      | docker run/start/stop Befehle ähneln dem .... Subsystem |

**Fazit und Aussicht**, z.B. Die Durcharbeitung von ... gab mir ein besseres Verständnis über die Funktionsweise von Containern.


### 702.1 Container Usage 

**Weight**: 7 + (7 für Schüler die das Modul 300 noch nicht besucht haben)

**Beschreibung**,  Die Kandidaten sollten in der Lage sein, Docker-Container zu erstellen, zu teilen und zu betreiben. 

**Tagesziele**,  
* Dockerfunktionen dokumentieren 
* eigenes Dockerfile erstellen
* Docker Container erstellen

**Vorgehen**, 
Ich erstelle ein eigenes Dockerfile. In diesem Dockerfile wird automatisch ein MySQL Container erstellt.

**Beispiele und Arbeitsergebnisse**
Anhand dieses Dockerfiles habe ich einen MySQL Container erstellt:

    FROM ubuntu:14.04

    # root Password setzen
    RUN echo 'mysql-server mysql-server/root_password password Server.22' | debconf-set-selections 
    RUN echo 'mysql-server mysql-server/root_password_again password Server.22' | debconf-set-selections 

    # Installation
    RUN apt-get update && apt-get install -y mysql-server

    # mysql config
    RUN sed -i -e"s/^bind-address\s*=\s*127.0.0.1/bind-address = 0.0.0.0/" /etc/mysql/my.cnf

    EXPOSE 3306

    VOLUME /var/lib/mysql

    CMD ["mysqld"]

*Docker Befehle*

| Command | Bedeutung |
| ---- | ---- |
| docker build "Source" | Erstellt ein Docker image | 
| docker images | Zeigt alle verfügbare Docker images |
| docker rmi "image" | Löscht ein Docker image |
| docker run "image" | startet ein Docker image |
| docker exec -it "Container" \bin\bash | Exploriert einen Container |

*Was ist Docker?*

Mit Docker kann man vereinfacht Container bereitstellen und installieren.


