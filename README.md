## Inhaltsverzeichnis

* 01 - [Kapitel 701.1 Modern Software Development](#701.1)
* 02 - [Kapitel 701.3 Source Code Management](#701.3)
* 03 - [Kapitel 701.4 Continuous Integration and Continuous Deliver](#701.4)
* 04 - [Kapitel 702.1 Container Usage](#702.1)
* 05 - [Kapitel 702.2 Container Deployment and Orchestration](#702.2)
* 06 - [Kapitel 703.1 Virtual Machine Deployment](#703.1)
* 07 - [Kapitel 704.1 Ansible](#704.1)

## Fahrplan
***


| Datum | behandelte Unterrichtsinhalte: | Gewichtung |
| -------- | ------ | -------- |
| 15.05.19 | 701.1 Modern Software Development | 6 + 4|
| 22.05.19 | 701.3 Source Code Management | 4 |
| 29.05.19 | 701.4 Continuous Integration and Continuous Deliver | 5 | 
| 05.06.19 | 702.1 Container Usage | 7 |
| 12.06.19 | 702.2 Container Deployment and Orchestration | (7) |
| 19.06.19 | 702.2 Container Deployment and Orchestration , 703.1 Virtual Machine Deployment, 704.1 Ansible | 5 |
| 26.06.19 | LB1 Theoretische Prüfung und Abschluss LB2 | - |
| 03.07.19 | Sommersporttage | - |
|          | Total Punkte | 27 (34) ! |

Die Kapitel wurden in der Gruppe mit Aris Kabashi erarbeitet. 

## Dokumention des Lern- und Entwicklungsprozesses
***

### Kapitel: 701.1 Modern Software Development <a name="701.1">
> [⇧ **Nach oben**](#inhaltsverzeichnis)

**Weight**: 6 + 4 Bonuspunkte für eigenen Mikroprozesse erstellen

**Beschreibung** Aufweisung, wie man eine Containerumgebung einrichtet. Die Begriffe Security, Performenz, Erreichbarkeit, Loadbalancing etc. werden nach diesem Topic bekannt sein.

**Tagesziele**, 
* Verstehen, wie eine Containerumgebung funktioniert
* Begrifflichkeiten verstehen (Security, Performenz, Erreichbarkeit, Loadbalancing etc.)
* Mikroprozesse erstellen

**Vorgehen**, In den Unterlagen war ein Video vorhanden, dass ausführlich erklärt hat, wie ein Mikroprozess funktioniert. Dazu haben wir in diesem Kapitel kurz beschrieben, was genau ein Mikroprozess ist und haben sogar einen eigenen geschrieben.

**Arbeitsergebnisse**

**Was ist ein Mirkoprozess?**

Ein Mikroprozess ist ein einzelner Prozess eines grossen Konstruktes. Der Sinn von Mikroprozesse ist, dass man nicht alles in einer grossen Applikation abspeichert, sondern man spaltet jeden einzelnen Ablauf ab, damit man eine höhere Erreichbarkeit erzielen.

**Mikroprozess JavaScript**
Voraussetzung: Node JS installiert

    var http = require("http");
    http.createServer(function (request, response) {
        // Send the HTTP header 
        // HTTP Status: 200 : OK
        // Content Type: text/plain
        response.writeHead(200, {'Content-Type': 'text/plain'});
        
        // Send the response body as "Hello World"
        response.end('Hello World\n');
    }).listen(8081);
    
    // Console will print the message
    console.log('Server running at http://127.0.0.1:8081/');

 Danach läuft hello world über den Localhost auf Port 8081


### Kapitel: 701.3 Source Code Management <a name="701.3">
> [⇧ **Nach oben**](#inhaltsverzeichnis)

**Weight**: 5
**Beschreibung** Kandidaten sollten in der Lage sein, Git zur Verwaltung und Freigabe von Quellcode zu verwenden. Dazu gehören das Erstellen und Beitragen zu einem Repository sowie die Verwendung von Tags, Zweigen und Remote-Repositories. Darüber hinaus sollte der Kandidat in der Lage sein, Dateien zusammenzuführen und Konflikte zu lösen.

**Tagesziele**, 
* Git als Repository verstehen
* Dateistruktur von Git verstehen
* Verwaltung von branches, tags und forks verstehen

**Vorgehen**, Ich versuche selber ein GIT Repo zu erstellen, welchen ich selber verwalten werde. Danach schaue ein informatives Video an, welches mir die Grundlagen von GIT näher beibringt.

**Beispiele und Arbeitsergebnisse**
Hier zeige ich auf, wie git mit VisualStudioCode verwalte. Mit Markdown kann ich gewisse Steuerelemente verwalten. z.B eine Tabelle wird hier mit dem Pipe Symbol getrennt.

![VisualStudioCodeMarkdown](/images/VisualStudioCodeGIT.png)


**Branch** 

Ein Branch ist eine isolierte Entwicklungszone. Hier testet man einzelne Skripts oder Programme bevor sie in die Produktion kommen.
Man kann Beispielsweise eine Entwicklungszone mit git branch "Name" einrichten und von dort aus ausserhalb der Produktiven Zone arbeiten. Da man getrennt ist, wird die "master" Umgebung nicht beinträchtig. 


**Tags** 

Tags sind Referenzen für eine bestimmte Version einer GIT Datei


**Forks** 

Wenn man ein bestimmmtes GIT Repository forked, dann zieht man eine eigene Version auf das eigene GIT


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


### 702.1 Container Usage  <a name="702.1">
> [⇧ **Nach oben**](#inhaltsverzeichnis)

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

### 702.2 Container Deployment and Orchestration <a name="702.2">
**Weight**: 5

**Beschreibung**,  Die Kandidaten sollten in der Lage sein, Kubernetes einzurichten und Docker Compose einzusetzen

**Tagesziele**,  
* Kubernetes Umgebung einrichten
* Weave einrichten
* Docker Compose verstehen

**Vorgehen**, 
Lernumgebung starten und Kubernetes Umgebung anschauen. Weave installieren.

**Beispiele und Arbeitsergebnisse**
git clone https://github.com/mc-b/lernkube
cd lernkube
git clone https://github.com/mc-b/iot.kafka
cp templates/MISEGR.yaml config.yaml
vagrant plugin install vagrant-disksize
vagrant up
source kubeenv
kubectlapply -f misegr/ewolff/ms-kubernetes/

### 703.1 Virtual Machine Deployment <a name="703.1">
> [⇧ **Nach oben**](#inhaltsverzeichnis)

**Weight**: 4

**Beschreibung**,  Die Kandidaten wissen wie man ein eigenes Vagrantfile erstellt. Zudem können sie damit eine eigene automatisierte Umgebung aufbauen

**Tagesziele**,  
* Vagrant
* Vagrantfile
* Vagrant VM einrichten
* Vagrant verstehen

**Vorgehen**, 
Vagrantfile schreiben und eigene VMs erstellen. 

**Beispiele und Arbeitsergebnisse**

Vagrant ist ein Tool zum Erstellen und Verwalten von Umgebungen virtueller Maschinen in einem einzigen Workflow.

Vagrant bietet einfach zu konfigurierende Arbeitsumgebungen, die auf einem einzigen Workflow gesteuert werden, um die Produktivität und Flexibilität eines wiederholendes Vorgehen zu automatisieren.

Auf folgender Seite kann Vagrant installiert werden: https://www.vagrantup.com/downloads.html

Man kann von der Seite https://app.vagrantup.com/boxes/search?utf8=%E2%9C%93&sort=downloads&provider=&q= verschiedene VM Boxen herunterladen, um einzelne Vagrantmaschinen zu installieren und einzurichten.
1. Nun kann man im Terminal folgenden Befehl eingeben, um die Debian Box zu installieren
    ```
        vagrant box add debian/jessie64

        Result:
        ==> box: Loading metadata for box 'debian/jessie64'
        box: URL: https://vagrantcloud.com/debian/jessie64
        This box can work with multiple providers! The providers that it
        can work with are listed below. Please review the list and choose
        the provider you will be working with.

        1) libvirt
        2) virtualbox

        Enter your choice: 2
    ```
2. Danach erstellt man ein eigenes Vagrantfile um die VM einzurichten
    ```
        vagrant init debian/jessie64
    ```
3. Zum Schluss kann man auch eigene Konfigurationen mitgeben
    ```
        vi Vagrantfile

        Vagrant.configure("2") do |config|
            config.vm.box = "debian/jessie64"
        end
    ```

**Commands** 

| Commands | Bedeutung |
| ----- | ----- |
| vagrant box add | fügt vagrant boxen hinzu |
| vagrant box list | listet alle verfügbaren vagrant boxen auf |
| vagrant init | erstellt ein eigenes Vagrantfile |
| vagrant up | erstellt mit dem Vagrantfile die VM | 
| vagrant ssh | man greift mit diesem Befehl auf die Vagrant VM zu (mittels SSH) |
| vagrant halt | stoppt die Vagrant VM |
| vagrant destroy | stoppt und zerstört die Vagrant VM |

**Vagrantfile**

```
        Vagrant.configure("2") do |config|
            # Jenkins and Apache Virtual Machine
            config.vm.define "web01" do |web01|
                web01.vm.box = "ubuntu/xenial64"
                
                # Portforwarding, Jenkins 8082, http 80, sql 3306
                web01.vm.network "forwarded_port", guest:80, host:8080, auto_correct: true
                web01.vm.network "forwarded_port", guest:8081, host:8081, auto_correct: true
                web01.vm.network "forwarded_port", guest:8082, host:8082, auto_correct: true
                web01.vm.network "forwarded_port", guest:3306, host:3306, auto_correct: true  
                
                # Enabling a forwarded Portrange for Jenkins
                for i in 32760..32780
                        web01.vm.network :forwarded_port, guest: i, host: i
                end	
            
                # Network web01	
                web01.vm.network "private_network", ip: "192.168.0.3"		
            
                # Docker Provisioner (Install image)
                web01.vm.provision "docker" do |d|
                    d.pull_images "ubuntu:14.04"
                end	

                # Hostname
                web01.vm.hostname = "ch-web01"

                # Vagrant Name
                web01.vm.provider "virtualbox" do |v|
                    v.name = "ch-web01"
                end

                #Shell Script Part Updating APT Repository and create Synch Folder
                web01.vm.provision :shell, inline: <<-SHELL
                    sudo apt-get update
                    sudo apt-get -y install apache2
                    mkdir /etc/shared
                    sh /vagrant/scripts/ufw.sh
                    sh /vagrant/scripts/docker_web01.sh
                SHELL
                web01.vm.synced_folder "./shared_web01", "/etc/shared"
                
                # Firewall Configurations
                web01.vm.provision "shell", path: "scripts/ufw.sh"

                # Docker Configurations
                web01.vm.provision "shell", path: "scripts/docker_web01.sh"
            end

            # MySQL Virtual Machine
            config.vm.define "db01" do |db01|
                db01.vm.box = "ubuntu/xenial64"
                
                # Portforwarding, Jenkins 8082, http 80, sql 3306
                db01.vm.network "forwarded_port", guest:80, host:8080, auto_correct: true
                db01.vm.network "forwarded_port", guest:8081, host:8081, auto_correct: true
                db01.vm.network "forwarded_port", guest:8082, host:8082, auto_correct: true
                db01.vm.network "forwarded_port", guest:3306, host:3306, auto_correct: true  
                
                db01.vm.provision :shell, inline: <<-SHELL
                    sudo apt-get update
                    sudo apt-get -y install apache2
                    sudo apt-get -y install docker
			        sudo apt-get -y install docker.io
                    sh /vagrant/scripts/ufw.sh
                    sh /vagrant/scripts/docker_db01.sh 
                SHELL
                db01.vm.synced_folder "./shared_db01", "/etc/shared"
                
                # Network db01
                db01.vm.network "private_network", ip: "192.168.0.4"
                
                # Docker Provisioner (Install image)
                db01.vm.provision "docker" do |d|
                    d.pull_images "ubuntu:14.04"
                end

                # Docker Configurations
                        db01.vm.provision "shell", path: "scripts/docker_db01.sh"

                # Hostname
                db01.vm.hostname = "ch-db01"

                # Virtualbox Name
                db01.vm.provider "virtualbox" do |v|
                    v.name = "ch-db01"
                end	
            end
        end
```

### 704.1 Ansible <a name="704.1">
> [⇧ **Nach oben**](#inhaltsverzeichnis)

**Weight**: 8

**Beschreibung**,  Der Kandidat wissen nach diesem Thema, was Ansible ist und wie man es einsetzt.

**Tagesziele**,  
* Ansible-playbook verstehen
* Ansible.cfg verstehen
* Ansible Galaxy verstehen
* Ansible-doc verstehen
* Ansible einsetzen

**Vorgehen**, 
Lernumgebung starten und Kubernetes Umgebung anschauen. Weave installieren.

**Beispiele und Arbeitsergebnisse**

**Ansible.cfg**

Das ist das Konfigurationsfile von Ansible. Die standardmässig vorhandenen Konfigurationen sollten in der Regel reichen. Das File findet man unter /etc/ansible.
Im File können auch Umgebungsvariablen erstellt werden, welche die grundsätzlichen Variablen überschreibt. 

**Ansible-playbook**

In Ansible-playbook können Regeln definiert werden oder auch was auf dem Remote System erledigt werden sollte. Das Ansible-playbook-File liegt im besten Fall in einem Directory, wo alle Playbooks gesichert sind. Das Playbook wird im Format .yml gespeichert und kann folgendermassen aussehen: 

  - name: Run Powershell Scripts
    hosts: windows
    tasks:
  - name: run a powershell script
    win_command: powershell.exe -ExecutionPolicy ByPass -File C:/Users/Administrator/Documents/simple_ps.ps1

In diesem Fall wird eine Remote-Verbindung zum Hosts «windows» gemacht und dort wird das PowerShell-Script ausgeführt, welches sich im Pfad «C:/Users/Administrator/Documents/simple_ps.ps1» befindet. 

Zum Ansible mit einem Playbook auszuführen, kann man beispielsweise folgenden Befehl verwenden. 

    ansible-playbook $PlaybookPath -i $HostPath
    
**Ansible-vault**

Ansible-Vault ist ein Tool, dass es ermöglicht Files zu verschlüsseln. So stehen beispielweise Benutzername und Passwörter nicht im Klartext. 

![Ansible1](/images/Ansible_1.png)

In diesem Beispiel wären der Benutzername und das Passwort vom Remote-Server klar ersichtlich.


![Ansible2](/images/Ansible_2.png)

Um ein File mit Ansible-Vault zu entschlüsseln kann man beispielsweise folgenden Befehl verwenden: 
*ansible-playbook $PlaybookPath -i $HostPath --ask-vault-pass*

**Ansible-galaxy**

Ansible Galaxy ist eine Communityseite, wo sich einzelne User auf der ganzen Welt ihre eigene Projekte präsentieren. Diese herunterladen und selber testen.

https://galaxy.ansible.com/


**Ansible-doc**

Zeigt Informationen zu Modulen an, die in Ansible-Bibliotheken installiert sind. Es zeigt eine kurze Auflistung von Plugins und deren Kurzbeschreibungen, liefert einen Ausdruck ihrer DOCUMENTATION-Strings und kann einen kurzen "Ausschnitt" erstellen, der in ein Playbook eingefügt werden kann.

**Hosts**

In ansible gibt es im Verzeichnis /etc/ansible eine File namens hosts. Dort kann man viele IP-Adressen zu einer bestimmten Gruppe auflisten, damit beim Ausführen eines Befehls, die ganze Gruppe den Befehl ausführt. Man könnte dort auch die Benutzername und das Passwort des Remote-Servers angeben, wäre aber nicht so praktisch, weil es dafür eine bessere Lösung gibt. 

![Ansible3](/images/Ansible_3.png)

**Group_vars**

Dieser Ordner muss man noch erstellen und normalerweise werde dort auch die Anmeldeinformationen der hosts in .yaml Files gespeichert. Allerdings ist es aber auch möglich einen anderen Namen für diesen Ordner zu definieren, das müsste aber dann wiederrum im ansible.cfg konfiguriert werden. Group_vars ist der Standardname.

**Ansible für nicht-Linux-Systeme**

Ansible kann man auch für Windows benutzen. Dafür wird das Protokoll winrm verwendet. Der ganze Aufbau ist auch sehr ähnlich, wie bei Linux-Systemen. Auf dem Windows-Server müssen nur wenige PowerShell Scripts und PowerShell-Befehle ausgeführt werden, damit die Ports 5985 für http und 5986 für HTTPS. WinRM ist ein SOAP(Simple Object Access Protocol) Netzwerkprotokoll. Die ganze Anleitung für die Konfiguration unter Windows findet man hier: https://docs.ansible.com/ansible/latest/user_guide/windows_winrm.html

**Arbeitsergebnisse**
![Ansible Dokumente](ansible)