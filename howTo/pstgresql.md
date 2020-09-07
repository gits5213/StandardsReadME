# Set up PostgreSQL & pgAdmin 4
<!-- topics>start -->
* [Basic Command for Terminal](#Basic-Command-for-Terminal)
* [Advanced Command](#Advanced-Command)


## Set up PostgreSQL
- [Navigate to the URL](https://www.postgresql.org/)
- Click on the Download Link
- Click on the Operating System which you have 
- Click on the Postgres.app link or [Directly Navigate: ](https://postgresapp.com/)
- Follow the Instruction and Click on the Downloads Link again
- Click on the Download again 
- Extract folder and Move to the Application folder 
- Click on the PostgresSQL
- Configure your $PATH to use the included command line tools (optional):
```
sudo mkdir -p /etc/paths.d &&
echo /Applications/Postgres.app/Contents/Versions/latest/bin | sudo tee /etc/paths.d/postgresapp
```
```
Host	localhost
Port	5432
User	your system user name
Database	same as user
Password	none
Connection URL	postgresql://localhost
```
- To connect with psql, double click a database. To connect directly from the command line, type psql. If you’d rather use a graphical client, see below.

## Set up pgAdmin 4
- [Navigate to URL: ](https://www.postgresql.org/ftp/pgadmin/pgadmin4/v4.25/macos/)
- Click on the ```.dmg``` file
- ```Extract``` it and Move to the ```Application``` Folder
- Set your Master Password 
- Set your username, Password & Host 
