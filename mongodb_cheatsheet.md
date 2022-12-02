

 	#To get the list of all databases
		show dbs

	#To create new database
		use database_name

	#To know the current database
		db

	#To drop the database
		db.dropDatabase()

	#To create a new collection
		db.createCollection(name)

	#To view the available collections
		show collections

	#To Drop the collection
		db.collection_name.drop()

	#To insert the document
		db.collection_name.insert(document)

	#To get collection document
		db.collection_name.find()

	#To update document
		db.collection_name.update(select_field, update_value)

	#To delete document
		db.collection_name.remove(deletion_field)

	#Finding a Single Record
		db. collectionname.findOne({"field1": "content"})

	#To finding a Single Record:
		db. collectionname.findOne({"field1": "content"})
		
	#To Show All Databases
	  	show dbs
	 
  	#To display documents from collection (first 10)
		db.collection_name.find()

