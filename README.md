# Oracle-Docker

Pre-requisite:

- Install Docker Desktop and docker compose

1.  Visit https://container-registry.oracle.com/ and create your new account
![image](https://github.com/AlxVarp/Oracle-Docker/assets/21965009/327dbf6d-f6a8-4743-b33d-5cd7d24f0c29)

2. Select Enterprise.

![image](https://github.com/AlxVarp/Oracle-Docker/assets/21965009/8ee5b307-b521-4988-9836-cea8fa46067a)

3. Click “Sign In”
![image](https://github.com/AlxVarp/Oracle-Docker/assets/21965009/e92278e6-b606-4305-9d3d-f1d3d4fc63b1)

4.  Authenticate by entering your registered email ID and password.

  ![image](https://github.com/AlxVarp/Oracle-Docker/assets/21965009/d630e11a-2f3f-4d7d-9720-f29f1b3a2003)

6.  en  la  consola  ingresar el comando docker login  container-registry.oracle.com


![image](https://github.com/AlxVarp/Oracle-Docker/assets/21965009/55ff5858-c12a-4afa-92c6-ec9b130ae309)

7. Git clone  git@github.com:AlxVarp/Oracle-Docker.git

8. ![image](https://github.com/AlxVarp/Oracle-Docker/assets/21965009/81733d5e-3ba7-4e18-ac17-34568f4c2160)

![image](https://github.com/AlxVarp/Oracle-Docker/assets/21965009/2133aa15-b84d-4642-a359-5019b0a7fa79)

![image](https://github.com/AlxVarp/Oracle-Docker/assets/21965009/c75dcb83-05c7-4df1-aa8d-989413cd5903)



    docker-compose logs -f
	
![image](https://github.com/AlxVarp/Oracle-Docker/assets/21965009/2ea997b1-195c-4a72-8891-41cded778193)



    docker-compose  ps
![image](https://github.com/AlxVarp/Oracle-Docker/assets/21965009/c00cbfb0-673c-48ce-aab5-f4356d4195de)

![image](https://github.com/AlxVarp/Oracle-Docker/assets/21965009/f0e9b61e-3c89-465a-ad17-95fc43495ba4)



    environment:
          - ORACLE_SID=ORCLCDB
          - ORACLE_PDB=ORCLPDB1
          - ORACLE_PWD=Oracle_123
![image](https://github.com/AlxVarp/Oracle-Docker/assets/21965009/d624d1c3-a687-41bd-ae85-b1aa164d9d09)



    begin
        execute immediate 'drop user egibide cascade';
    exception
        when others then
            dbms_output.put_line('El usuario no existe.');
    end;
![image](https://github.com/AlxVarp/Oracle-Docker/assets/21965009/e0cbf1f3-9e66-4e97-a7cc-e002c662e103)



    CREATE TABLESPACE LIBRERIA_NEW DATAFILE '/opt/oracle/oradata/LIBRERIA_NEW' SIZE 100 M AUTOEXTEND ON NEXT 100 M MAXSIZE 1 G;
    
    CREATE USER DESARROLLO
    IDENTIFIED BY DESARROLLO
    DEFAULT TABLESPACE LIBRERIA_NEW;
	
