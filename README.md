DESCRIPTION
AirBnB Clone is a complete web application, integrating database storage, a back-end API, and front-end interfacing in a clone of AirBnB.

The project currently only implements the back-end console.


CLASSES:
AirBnB Clone utilizes the following classes

	BaseModel	FileStorage	User	State	City	Amenity	Place	Review
PUBLIC INSTANCE ATTRIBUTES	id
created_at
updated_at		Inherits from BaseModel	Inherits from BaseModel	Inherits from BaseModel	Inherits from BaseModel	Inherits from BaseModel	Inherits from BaseModel
PUBLIC INSTANCE METHODS	save
to_dict	all
new
save
reload	""	""	""	""	""	""
PUBLIC CLASS ATTRIBUTES			email
password
first_name
last_name	name	state_id
name	name	city_id
user_id
name
description
number_rooms
number_bathrooms
max_guest
price_by_night
latitude
longitude
amenity_ids	place_id
user_id
text
PRIVATE CLASS ATTRIBUTES		file_path
objects


STORAGE:

The above classes are handled by the abstracted storage engine defined in the FileStorage class.

Every time the backend is initialized, AirBnB Clone instantiates an instance of FileStorage called storage. The storage object is loaded/re-loaded from any class instances stored in the JSON file file.json. As class instances are created, updated, or deleted, the storage object is used to register corresponding changes in the file.json.


CONSOLE:
	The console is a command line interpreter that permits management of the backend of AirBnB Clone. It can be used to handle and manipulate all classes utilized by the application (achieved by calls on the storage object defined above).

Using the Console
The AirBnB Clone console can be run both interactively and non-interactively. To run the console in non-interactive mode, pipe any command(s) into an execution of the file console.py at the command line.

$ echo "help" | ./console.py
(hbnb) 
Documented commands (type help <topic>):
========================================
EOF  all  count  create  destroy  help  quit  show  update

(hbnb) 
$

Alternatively, to use the AirBnB Clone  console in interactive mode, run the file console.py by itself:

$ ./console.py

While running in interactive mode, the console displays a prompt for input:

$ ./console.py
(hbnb) 

To quit the console, enter the command quit, or input an EOF signal (ctrl-D).

$ ./console.py
(hbnb) quit
$
$ ./console.py
(hbnb) EOF
$

Console Commands
The AirBnB Clone console supports the following commands:

create
	Usage: create <class>
Creates a new instance of a given class. The class' ID is printed and the instance is saved to the file file.json.

$ ./console.py
(hbnb) create BaseModel
119be863-6fe5-437e-a180-b9892e8746b8
(hbnb) quit


