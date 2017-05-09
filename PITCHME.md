
## Analyse comparative d'outils de déploiment et de configuration 
Stage de fin d'étude réalisé au CETIC
Présenté par Valentin GOEMANNE

Sous la direction de Sébastien DUPONT et de Michel HANOTIAUX

Mai 2017

---
## Sommaire
 - <span class ="fragment">Le CETIC ? C'est quoi ?</span>  
 - <span class ="fragment">Etat de l'art</span>
 - <span class ="fragment"> Analyse comparative d'outils de déploiment et de configuration </span> 

---

## Le CETIC ? C'est quoi ?
<strong class="fragment">C</strong>entre d'<strong class="fragment">E</strong>xcellence <strong class="fragment">T</strong>echnologie de l'<strong class="fragment">I</strong>nformation et de la <strong class="fragment">C</strong>ommunication 

+++
### Présentation
- <span class="fragment">ASBL</span>
- <span class="fragment">45 personnes</span>
- <span class="fragment">15 ans</span>
- <span class="fragment">Zonning de Gosselie</span>

+++
### Les equipes
- <span class="fragment">Software and System Engineering</span>
- <span class="fragment">Software Services Technologies</span>
- <span class="fragment">Embedded & Communicating Systems</span>

+++
### Leur jobs 
Aider et promouvoir l'IT dans les entreprises walonnes

<span class="fragment">Comment ? </span> 

<span class="fragment">En les aidant dans leur projet en créant des inovations</span>

+++
### Leurs projets 

- <span style="color:grey">Santé</span>
    - <span class="fragment">SEAMPAT</span>

- <span style="color:grey">Transport</span>
    - <span class="fragment">MOBITS</span>


---
## Etat de l'art
- <span class="fragment">Autonomie</span>
- <span class="fragment">Curiosité</span>

+++
### Le versionning 

- <span class="fragment">Git </span>
- <span class="fragment">GitLab</span>

+++
### Le Cloud

- <span class="fragment">IAAS: Infractruture As A Service</span>
- <span class="fragment">SAAS: Software As A Service</span>
- <span class="fragment">PAAS: Plateforme As A Service</span>

+++

### La Virtualisation 

Hyperviseur
- <span class="fragment" style="color:grey">Type Natif</span>
- <span class="fragment" style="color:grey">Type Hosted</span>

    

+++

### La Virtualisation 

![Logo](Hyperviseurwiki.png)

+++

### La virtualisation 

#### Vagrant 


```ruby
Vagrant.configure(2) do |config|
   #Pour toute les machine qui fonctionne avec virtualbox
   config.vm.provider "virtualbox" do |vb|
    vb.memory = "512" 
  end

  #Configuration de la VM "VM1"
  config.vm.define "VM1" do |machine|
    machine.vm.box = "centos6.7"   #Nom de la box utilisée
    machine.vm.hostname = "TestVM1"     #Hostname de la VM
    machine.vm.network :private_network, ip: "192.168.10.191"   #Création d'un réseau privé avec l'ip mentionné 
  end

  #Configuration de la VM "VM2"
  config.vm.define "VM2" do |machine|
    machine.vm.box = "centos6.7"    #Nom de la box utilisée
    machine.vm.hostname = "TestVM2"      #Hostname de la VM
    machine.vm.network :private_network, ip: "192.168.10.192"   ##Création d'un réseau privé avec l'ip mentionné
  end
end
```
+++

### Les Conteneurs 

![Logo](logo_docker.png)
![Logo](CaptureDocker1.png)

