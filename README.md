# Learn and Do: PAAS
#### Guida ai servizi in PaaS e deploy di un'applicazione standard (Wordpress) 
###### CV LAB


## 1) Creare un resource group
Per questioni di segregazione delle risorse cloud, è sempre opportuno suddiverle in appositi contenitori, chiamati "Resource Group".

Per il nostro laboratorio, creeremo uno di questi contenitori con la seguente sintassi:

```bash
CVLAB-RG-<iniziali_nome_cognome>-WORPRESS
```

![Resource Group screen](https://raw.githubusercontent.com/Lukiep/cv-lab-paas/master/images/resource-group.png)


## 2) Creare un database MariaDB PAAS

Per installare il nostro wordpress, avremo bisogno di un database sql funzionante.
Per questo tutorial, utilizzeremo una risorsa PAAS (Platform-as-a-Service)

Per creare il nostro nuovo database, partendo dal vostro Resource Group, cliccate su "New"

Cercate "Maria DB" e createne uno nuovo 

![MariaDB New](https://raw.githubusercontent.com/Lukiep/cv-lab-paas/master/images/create_mariadb.png)

Quando configurate la risorsa, utilizzate la naming convention:
```bash
<iniziali_nome_cognome>-sql-wordpress
```

![MariaDB Option](https://raw.githubusercontent.com/Lukiep/cv-lab-paas/master/images/create_mariadb_option.png)

Cambiate il sizing del database, cliccando su "Configure Server"

![MariaDB Option](https://raw.githubusercontent.com/Lukiep/cv-lab-paas/master/images/create_mariadb_sizing.png)

A questo punto assegnate un tag al vostro database, per poterlo categorizzare meglio

![MariaDB Tag](https://raw.githubusercontent.com/Lukiep/cv-lab-paas/master/images/create_mariadb_tag.png)

Infine cliccate sul pulsante "Create" per far partire il deploy

![MariaDB Create](https://raw.githubusercontent.com/Lukiep/cv-lab-paas/master/images/create_mariadb_create.png)

Partirà quindi il deploy della risorsa

![MariaDB Create](https://raw.githubusercontent.com/Lukiep/cv-lab-paas/master/images/create_mariadb_deploy.png)

## 3) Creare uno schema nel database in paas
A questo punto dovete creare il vostro schema nel database appena creato, dove poi Wordpress instanzierà le sue tabelle. 
Per fare questo collegatevi al database con il vostro tool preferito (es. MySQL Workbench):

![MariaDB Create](https://raw.githubusercontent.com/Lukiep/cv-lab-paas/master/images/mariadb_newdb.png)

![MariaDB Create](https://raw.githubusercontent.com/Lukiep/cv-lab-paas/master/images/mariadb_newdb2.png)

<details>
<summary>Tips</summary>
<pre>
Ricordatevi di autorizzare il vostro IP nella schermata "Connection Security"
</pre>
</details>

