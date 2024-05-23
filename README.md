# Workshop Ansible

In questo workshop vedremo in azione Ansible e alcuni casi d'uso.<br>
Vedremo come automatizzare la configurazione degli apparati network su tecnologia legacy e tecnologia SDN.

Per poter utilizzare il materiale di questo corso avrete bisogno di:
*  VM linux Ubuntu based oppure WSL v2
*  Python 3.x + modulo virtualenv + modulo paramiko
*  Configurazione di un virtual environment python
*  Ansible + moduli necessari
*  Network devices o simulatori come pnetlab/eve-ng **(facoltativo)**

**NOTA:** senza pnetlab/eve-ng potrete testare gli script usando le sandbox di [Cisco Devnet](https://developer.cisco.com/site/sandbox/).

## Istruzioni
Una volta installata la VM linux lanciate il terminale e utilizzate i seguenti comandi per configurare il vostro ambiente python:

* scaricate nella vostra HOME il repository in formato .tar
* scompattate il file .tar nella vostra HOME, poi entrate nella cartella "workshop-ansible"<br>
`$ tar -xvf workshop-ansible-master.tar`<br>
`$ cd workshop-ansible`<br>
`$ pwd`<br>
L'output dovrebbe essere il seguente:<br>
`/home/<vostro-utente>/workshop-ansible`

*  installare python3.x<br>
`$ sudo apt-get install python3.11 python3-pip python3.11-venv`

*  creare e attivare virtual env<br>
`$ python3 -m venv venv-workshop-ansible`<br>
`$ source venv-workshop-ansible/bin/activate`<br>
Sul prompt dovrebbe apparire il nome del virtualenv:<br>
`(venv-workshop-ansible) $ `

*  installare Ansible<br>
`$ pip install ansible ansible-pylibssh ansible-lint`

* verificare installazione di Ansible<br>
`$ ansible --version`<br>
`ansible [core 2.16.7]`<br>
`...`<br>

* installare i moduli Ansible necessari<br>
`$ ansible-galaxy collection install cisco.nxos`<br>
`$ ansible-galaxy collection install cisco.aci`<br>
`$ ansible-galaxy collection install cisco.ios`<br>
`$ ansible-galaxy collection install ansible.netcommon`

### Installazione VM Cisco csr1000v (facoltativo)
* [Cliccando qui potete scaricare l'immagine Cisco csr1000v](https://software.cisco.com/download/home/284364978/type/282046477/release/Amsterdam-17.3.3)
* [Cliccando qui trovate il video con le istruzioni per l'installazione](https://www.youtube.com/watch?v=hnD_IKRiAmE)


