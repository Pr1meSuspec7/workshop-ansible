# Workshop Ansible

In questo workshop vedremo in azione Ansible e alcuni casi d'uso.<br>
Vedremo come automatizzare la configurazione degli apparati network su tecnologia legacy e tecnologia SDN.

Per poter utilizzare il materiale di questo corso avrete bisogno di:
*  una VM linux Ubuntu based (Ubuntu, Mint, Pop_OS, etc..)
*  Python 3.x + modulo virtualenv + modulo paramiko
*  configurazione di un virtual environment python
*  Ansible + moduli necessari
*  una VM Cisco csr1000v **(facoltativo)**

**NOTA:** Questo laboratorio NON FUNZIONA su windows WSL

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
`$ sudo apt-get install python3 python3-pip`

*  installare il modulo virtualenv<br>
`$ sudo pip3 install virtualenv `

*  creare e attivare virtual env<br>
`$ virtualenv -p python3 py3_ansible_venv`<br>
`$ source py3_ansible_venv/bin/activate`<br>
Sul prompt dovrebbe apparire il nome del virtualenv:<br>
`(py3_ansible_venv) $ `

*  installare Ansible<br>
`$ pip3 install ansible`

* verificare installazione di Ansible<br>
`$ ansible --version`<br>
`ansible 2.10.6`<br>
`...`<br>

* installare modulo paramiko<br>
`$ pip3 install paramiko`

* installare i moduli Ansible necessari<br>
`$ ansible-galaxy collection install cisco.nxos`<br>
`$ ansible-galaxy collection install cisco.aci`<br>
`$ ansible-galaxy collection install ansible.netcommon`

### Installazione VM Cisco csr1000v (facoltativo)
* [Cliccando qui potete scaricare l'immagine Cisco csr1000v](https://software.cisco.com/download/home/284364978/type/282046477/release/Amsterdam-17.3.3)
* [Cliccando qui trovate il video con le istruzioni per l'installazione](https://www.youtube.com/watch?v=hnD_IKRiAmE)

**NOTA:** senza la VM csr1000v potrete testare gli script di Ansible usando la sandbox di Cisco Devnet.