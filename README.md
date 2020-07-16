# Real_estate_website
A real estate website(using django) having nice interface, use of little lightbox for images, different search options for properties, single property page, register and login and logout options, Dashboard to manage your account, making enquiry about a property, sending email to concerned realtor after an inquiry, a customized Administration area for handling data in database. 

The main project is in 'btre', in this you will find settings.py and main urlpatterns(or routes).

There are five apps in this project{pages, accounts, contacts, realtors, listings}
pages app: It handles Home page and about page dynamically by bringing data from listings and realtors app models(databases).
accounts app: It handles Register, login, logout and information on dashboard (model not created manually for users as they are already available in django).
contacts app: It takes information from inquiry form(like name,phone user_id,property_id..etc) and save it in database(using model Contact)
              for further use in displaying inquiry information on user's dashboard. Also it sends an emsil to the concerned Realtor.
realtors app: It creates a model for Realtors (realtors can be added, removed and edited only through admin area).
listings app: It creates a model for property (property can be added, removed and edited only through admin area) which is displayed on home page(by index method), featured listing page(by listing method)
              It also handles the search options,it filters isting according to searched info and displays them.
              
              
Templates : All templates are stored in templates folder.
           base.html(contains topbar, navbar and footer) extends to all templates.
           to make base.html short ,code for navbar,topbar and footer are in templates/partials.
           _alert.html in templates/partials is used to display django messages for errors and success.
           Other templates can be understood by their names.
