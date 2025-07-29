 # Aws-Rag-Chatbot

# COST
  The whole project should cost less than 1$ , make sure to delete resources at the end or you will get cooked (like me) :)

# Services Used
  Amazon Lex, Bedrock, S3

# Steps

  <img width="966" height="625" alt="image" src="https://github.com/user-attachments/assets/0ebaa163-7fb0-40e8-b7df-75fc728e7bc3" />
  
  # Request Access to the Amazon Bedrock Models(Titan Embeddings)
  
  1. Search for Amazon Bedrock

  <img width="1057" height="870" alt="image" src="https://github.com/user-attachments/assets/34a4d862-1c76-4a6d-8347-76984842a24c" />

  2. Click on Model access and Request access for Titan Text Embeddings G1 Text
  
   <img width="1918" height="964" alt="image" src="https://github.com/user-attachments/assets/3b5ef5c3-0781-4d1a-8e34-5193b40ee1c7" />

   <img width="1897" height="904" alt="image" src="https://github.com/user-attachments/assets/fd0b3f1a-6b5d-45e4-902a-c3578185ba90" />

   Scroll Down and click next

   <img width="1912" height="581" alt="image" src="https://github.com/user-attachments/assets/8b6bffaa-0468-444a-98b7-9d2cbfa2d01c" />

   <img width="1659" height="275" alt="image" src="https://github.com/user-attachments/assets/40945f71-e3cc-4c24-b19b-4b46587e64c2" />


# Documents that we'll use for RAG with Bedrock
  
  Any sort of documents with some text can be used for this project
  I have uploaded the documents in the repository which I am gonna use to test the model, You can use them too

# Create an S3 Bucket for document storage

  1. Search for S3
  
  <img width="959" height="352" alt="image" src="https://github.com/user-attachments/assets/8e8ee887-f4fa-4852-baed-38fea7fc70e0" />

  <img width="1844" height="846" alt="image" src="https://github.com/user-attachments/assets/18ec8f28-a82d-44f3-baf0-d92ce9689ae0" />

  2. Enter the Bucket name and leave the rest of the options as it is, scroll down and click create bucket

  <img width="1737" height="521" alt="image" src="https://github.com/user-attachments/assets/3fd759ea-88f9-49d8-8bfc-231ac7ed1437" />

  3. Go your bucket , click add files, scroll down and click upload

  <img width="1056" height="219" alt="image" src="https://github.com/user-attachments/assets/5aed7b30-5b00-471f-ac3d-15e9251064e5" />

  <img width="1736" height="413" alt="image" src="https://github.com/user-attachments/assets/484d01ac-53e6-4b90-ac41-9a4283648ae0" />

  <img width="1889" height="998" alt="image" src="https://github.com/user-attachments/assets/5c2f3041-a73b-4c70-a85c-a1755537f6e3" />

  <img width="1634" height="682" alt="image" src="https://github.com/user-attachments/assets/18b15cb1-03eb-4395-a537-c5e21fb915b5" />

# Create a knowledge base in Amazon Bedrock

   <img width="1022" height="449" alt="image" src="https://github.com/user-attachments/assets/355d794a-4252-4aab-83b2-526b170762b7" />

   1. Go Back to Amazon Bedrock , select Knowledge bases , click create and select Knowledge bases for vector store

   <img width="1895" height="874" alt="image" src="https://github.com/user-attachments/assets/56d6b794-870f-4508-a57f-7879f6add72f" />

   2. Enter name or keep it default, make sure S3 is selected as the data source and click next

   <img width="1600" height="759" alt="image" src="https://github.com/user-attachments/assets/d51ae948-8a34-478d-a1c7-210f27346c0a" />

   3. Select your S3 bucket , scroll down and click next

   <img width="1513" height="847" alt="image" src="https://github.com/user-attachments/assets/8208bf49-9154-4330-8832-ba4093f3242e" />
  
   4. Click on Select embedding model , choose Titan Text Embeddings V2 and choose the Amazon OpenSearch Serverless as your vector databse

   Text embedding: is a technique used in Natural Language Processing (NLP) to convert text (like words, phrases, or sentences) into numerical vectors. These vectors capture the semantic    meaning of the text, allowing machines to understand and process human language    more effectively.

   A vector database: is a type of database designed to store, index, and search high-dimensional vectors—like the text embeddings.
   
   
   <img width="1524" height="651" alt="image" src="https://github.com/user-attachments/assets/51a09f48-1c76-4432-8984-ddc9331498cb" />
   

   <img width="1227" height="760" alt="image" src="https://github.com/user-attachments/assets/ef509459-05ab-45b3-92a9-56ee2d64ec77" />


   <img width="1332" height="823" alt="image" src="https://github.com/user-attachments/assets/83602c97-127a-40b2-a2bd-aeaf4beee302" />


   <img width="1075" height="648" alt="image" src="https://github.com/user-attachments/assets/bb629929-504b-49d2-8b03-5ea317fc7c72" />


   6. Once the database is ready , go to data sources and select the data source and sync

  
   <img width="1217" height="637" alt="image" src="https://github.com/user-attachments/assets/3bb7288d-7e51-45d7-830f-89a608a3d1a2" />

  
# Create an Amazon Lex Bot


  <img width="853" height="319" alt="image" src="https://github.com/user-attachments/assets/ee4b9590-2daf-4846-9705-535bece63ee2" />


  <img width="849" height="876" alt="image" src="https://github.com/user-attachments/assets/4487ebbe-ef13-4982-b5a9-2ed99f52cb5e" />  
  

  1. Create a Bot

  <img width="1624" height="344" alt="image" src="https://github.com/user-attachments/assets/b7f61835-025e-4e2d-a6bd-8013021fe1c4" />

  2. Configure settings

  <img width="1055" height="877" alt="image" src="https://github.com/user-attachments/assets/aeded959-4527-4f1a-81a0-86ebbc013f1c" />
  

  <img width="900" height="708" alt="image" src="https://github.com/user-attachments/assets/adf43f1f-87ff-4735-8b88-7236ce48da01" />


  <img width="949" height="654" alt="image" src="https://github.com/user-attachments/assets/ce52d4a0-f5bc-416b-b789-175fd425b90b" />



# Building out an intent in Amazon Lex


  <img width="838" height="93" alt="image" src="https://github.com/user-attachments/assets/b07fe7af-0870-4e5f-a06b-ebec58bad6f3" />


  1. We can set our own Intent name and utterances like:
     
  <img width="881" height="664" alt="image" src="https://github.com/user-attachments/assets/0f6b11af-1f4f-474e-80b3-41439ea6e1bd" />

  <img width="796" height="442" alt="image" src="https://github.com/user-attachments/assets/684d1e5d-a3fb-4263-a3e0-b0f85f746b38" />

  <img width="806" height="883" alt="image" src="https://github.com/user-attachments/assets/27befad3-74c6-4234-a5cf-9f5af15cec0e" />

  2. Save the intent by scrolling down and click "back to intents list" 

  <img width="669" height="326" alt="image" src="https://github.com/user-attachments/assets/7322a752-0963-4b94-9c95-f021e2b67e30" />

  !Every bot has a FallbackIntent which gets created automatically and it is invoked when the message doesn't matches with custom intents

  3. Click on Build button
     
  <img width="1839" height="419" alt="image" src="https://github.com/user-attachments/assets/52e98e3d-5a9d-48dd-930d-4283bbd6d236" />
  

  4. Once it is finished building we can test it out


  <img width="1617" height="438" alt="image" src="https://github.com/user-attachments/assets/17000bd2-55c1-4e8f-82d5-6bd0f1ae7eaf" />


  <img width="753" height="671" alt="image" src="https://github.com/user-attachments/assets/2793aced-cab9-4a1c-84b3-101d7770f7b9" />


  <img width="704" height="495" alt="image" src="https://github.com/user-attachments/assets/81457537-1601-4813-bb6b-7fe699d2a8b7" />


# Add the QnA Intent to get generative AI capabilities in Amazon Lex chatbot


  <img width="380" height="204" alt="image" src="https://github.com/user-attachments/assets/5daab784-798d-4391-b273-c563ddd8a21b" />


  <img width="558" height="395" alt="image" src="https://github.com/user-attachments/assets/287561b4-2a92-4454-bbcc-2303fdbd62b7" />


  <img width="575" height="244" alt="image" src="https://github.com/user-attachments/assets/18acc9cd-0e2d-4b40-85a6-7ec55c7e7491" />


  2. Select the model

  <img width="606" height="334" alt="image" src="https://github.com/user-attachments/assets/61ff4c76-31b1-428c-a00f-9dcaf3441f32" />


  3. Go back to Amazon bedrock and copy the knowledge base id and paste it here and save the intent


  <img width="1688" height="424" alt="image" src="https://github.com/user-attachments/assets/ac0874f4-9b61-4ecf-a7c3-4f58e9422706" />


  <img width="679" height="568" alt="image" src="https://github.com/user-attachments/assets/7df72ca4-0bdb-45ce-9911-44ecd6478d67" />


  4. Now build the Intents again


  <img width="1899" height="950" alt="image" src="https://github.com/user-attachments/assets/630e0557-9723-4e4e-8be4-980114797190" />


  5. Now we can the test bot by asking questions about the documents we uploaded :)

 


  


     










  



  


 




   







 



  



  






