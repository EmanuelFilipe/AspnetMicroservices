# comando para criar a imagem do mongoDB via Docker
docker run -d -p 27017:27017 --name shopping-mongo mongo

	> se exibir uma mensagem de que ja existe o container rode o comando docker ps -a, 
	> anote o 'CONTAINER ID'
	> execute: docker start CONTAINER_ID

# confira se a imagem esta na lista de imagens
docker ps

# logs
docker logs -f shopping-mongo

# conectando ao interactive terminal
 docker exec -it shopping-mongo mongosh

show dbs
use CatalogDb  --> for create db on mongo
db.createCollection('Products')  --> for create people collection
db.Products.insertMany([{ 'Name':'Asus Laptop','Category':'Computers', 'Summary':'Summary', 'Description':'Description', 'ImageFile':'ImageFile', 'Price':54.93 }, { 'Name':'HP Laptop','Category':'Computers', 'Summary':'Summary', 'Description':'Description', 'ImageFile':'ImageFile', 'Price':88.93 } ])
db.Products.find({}).pretty()

# nugget 
MongoDB.Driver