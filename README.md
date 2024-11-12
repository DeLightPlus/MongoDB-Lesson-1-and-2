# MongoDB-Lesson-1-and-2

## MongoDB Shell Commands for Codetribe Project
The outlines of specific MongoDB shell commands used to set up and manipulate the Codetribe database, 
which includes collections for Facilitators, Trainees, and Projects. 
It also provides installation instructions for MongoDB and how to start the MongoDB shell (Mongosh).

### **1. Installation Instructions**
To use MongoDB and the MongoDB shell (Mongosh), follow these steps based on your operating system.
   
   - #### **Install MongoDB on Windows**
      For Windows, MongoDB provides an installer that you can download and run.
     
      1. Download the MongoDB Community Edition and MongoDB shell installers.
      2. Run the installers and follow the instructions. During installation, choose the option to install MongoDB as a service.
      3. Once installed, open a command prompt (or PowerShell) and to verify installation type:  
          ```sh
          mongod
          mongosh
      If everything is working properly, this command will open a MongoDB shell prompt.
      ![1 mongosh](https://github.com/user-attachments/assets/ea0b3991-bbc1-491a-bac5-41da1fe8dead)

### **2. Create the *Codetribe* Database**
Now that MongoDB is installed and running, we can proceed with creating the Codetribe database and its collections.

  - #### **Create the *Codetribe* Database**
    To create the Codetribe database, open the MongoDB shell (mongosh) and run:
      ```sh
      use Codetribe
    
  ![2 use_Codetribe](https://github.com/user-attachments/assets/40211e56-a95b-4215-b4c6-e0f44121d7d5)
  
  This command switches to the Codetribe database and creates it if it doesn't already exist.
    

### **3. Create Collections and Insert Data**
In MongoDB, collections are created automatically when you insert data. 
Here’s how to create the required collections and insert sample data.
  - ### **Create *Facilitators* Collection and Insert Document**
    ```bash
    db.Facilitators.insertOne({ Name: "Refilwe", Location: "Limpopo, Polokwane", Course: "Node.Js"  })
  
  ![3 insertFacilitators](https://github.com/user-attachments/assets/c6861ae1-acc2-4bf9-886e-0586dfc238d0)
  
  This command inserts a document into the *Facilitators* collection with the specified fields (*Name*, *Location*, and *Course*).

   - ### **Create *Trainees* Collection and Insert Document**
      ```bash
      db.Trainees.insertOne({ Name: "Kabelo", Location: "Limpopo, Polokwane", Facilitator: "Refilwe" })

  ![4 insertTrainees](https://github.com/user-attachments/assets/ac45d463-e748-4b21-bcba-63eb907b26b8)
  
  This command inserts a document into the *Trainees* collection with the specified fields (*Name*, *Location*, and *Facilitator*).

  - ### **Create *Projects* Collection and Insert Document**
      ```bash
      db.Projects.insertOne({ Name: "NodeJs-Create-Basic-Server", Course: "Node.Js", Lesson: "2" })

  ![5 insertProjects](https://github.com/user-attachments/assets/570b0a64-c04b-44a9-8ae0-ea9894692f1d)
  
  This command inserts a document into the *Projects* collection with the specified fields (*Name*, *Course*, and *Lesson*).
  
### **4. Conclusion**
  In this README, you learned how to:
  1. Install MongoDB on macOS, Windows, and Linux.
  2. Start the MongoDB shell (Mongosh).
  3. Create a Codetribe database and its collections (Facilitators, Trainees, Projects).
  4. Insert sample data into each collection.

         
