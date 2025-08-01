 # Aws-Rag-Chatbot

# COST
  The whole project should cost less than 1$ , make sure to delete resources at the end or you will get cooked (like me) :)

  I have attached the documents I used for knowledge base and testing the bot

# Services Used
  Amazon Lex, Bedrock, S3, OpenSearchService

# Steps

  <img width="966" height="625" alt="image" src="https://github.com/user-attachments/assets/0ebaa163-7fb0-40e8-b7df-75fc728e7bc3" />
  
  # Request Access to the Amazon Bedrock Models(Titan Embeddings) and Claude
  
  1. Search for Amazon Bedrock
     

  <img width="1057" height="870" alt="image" src="https://github.com/user-attachments/assets/34a4d862-1c76-4a6d-8347-76984842a24c" />
  

  2. Click on Model access and Request access for Titan Text Embeddings G1 Text
  
   <img width="1918" height="964" alt="image" src="https://github.com/user-attachments/assets/3b5ef5c3-0781-4d1a-8e34-5193b40ee1c7" />

   <img width="1897" height="904" alt="image" src="https://github.com/user-attachments/assets/fd0b3f1a-6b5d-45e4-902a-c3578185ba90" />

   Scroll Down and click next

   <img width="1912" height="581" alt="image" src="https://github.com/user-attachments/assets/8b6bffaa-0468-444a-98b7-9d2cbfa2d01c" />

   <img width="1659" height="275" alt="image" src="https://github.com/user-attachments/assets/40945f71-e3cc-4c24-b19b-4b46587e64c2" />
   

 3. For Claude

   <img width="1632" height="667" alt="image" src="https://github.com/user-attachments/assets/a4ca378a-403a-4f8b-80da-a1a25cae41ba" />

   <img width="1662" height="649" alt="image" src="https://github.com/user-attachments/assets/7d4bef9b-b050-4c61-ba12-f98c14169d96" />

   <img width="1175" height="140" alt="image" src="https://github.com/user-attachments/assets/8ad4fb4d-4b18-4ecd-8176-f93c0dc58f31" />

   <img width="1180" height="672" alt="image" src="https://github.com/user-attachments/assets/88051d2c-6513-453e-b37e-f8b898163070" />


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


  <img width="1581" height="283" alt="image" src="https://github.com/user-attachments/assets/d19a5a1e-7d32-42e6-af70-e91460298bfd" />


  <img width="594" height="340" alt="image" src="https://github.com/user-attachments/assets/12977f3c-b5d6-4f43-bb86-a9b34b361435" />


  Select the model
  

  <img width="873" height="790" alt="image" src="https://github.com/user-attachments/assets/a86d2b06-76a9-4ad6-997b-c19b056b75a3" />


  Go back to Amazon bedrock and copy the knowledge base id and paste it here and save the intent


  <img width="1919" height="808" alt="image" src="https://github.com/user-attachments/assets/cb5a1159-712a-4e3d-a5e0-70750d62b017" />


  <img width="779" height="293" alt="image" src="https://github.com/user-attachments/assets/ccdc94a6-b1cf-4669-a539-f2394fb6b9ba" />


  Save this Intent and build the Intents again


  <img width="1599" height="451" alt="image" src="https://github.com/user-attachments/assets/d3652a42-d2e5-4c11-829c-21f26a6f03f4" />


 # Test the genAI QnAIntent in Amazon Lex chatbot


  <img width="278" height="618" alt="image" src="https://github.com/user-attachments/assets/ebe1f010-82fc-42ea-b5da-5302b91268cd" />
  

  <img width="285" height="614" alt="image" src="https://github.com/user-attachments/assets/349cdcb1-4d45-44e1-ba2b-60036224c2c7" />


  <img width="287" height="616" alt="image" src="https://github.com/user-attachments/assets/6c3b79c7-edd1-4758-a26a-444492749ab4" />
  

# !Important! Delete your resources 

 Why? -> I forgot to delete the open search service resource and it costed me 8$ for 15 hours :(  Employement = 0 Bills++

 1. Delete the Knowledge base from Amazon Bedrock

 <img width="1895" height="597" alt="image" src="https://github.com/user-attachments/assets/8237396b-65ba-48bd-a850-10b67349d176" />
 
 <img width="1635" height="735" alt="image" src="https://github.com/user-attachments/assets/6fe0f085-1883-4ce8-af1f-ef2322d8a036" />


2. Delete collection from OpenSearchService 

 <img width="840" height="286" alt="image" src="https://github.com/user-attachments/assets/9893f568-9806-41bc-a41b-a7fcc1c40a51" />

 <img width="1900" height="727" alt="image" src="https://github.com/user-attachments/assets/7a648e90-7cfb-47f9-a778-efeb38a12a8a" />

 <img width="1802" height="595" alt="image" src="https://github.com/user-attachments/assets/a377161f-2f50-4639-aeb9-29751a2e3593" />


3. Delete S3 bucket

  <img width="1818" height="451" alt="image" src="https://github.com/user-attachments/assets/5e9ac80e-6cd4-4ae7-b79e-385085c77073" />

  <img width="1581" height="427" alt="image" src="https://github.com/user-attachments/assets/07f0f229-b554-4f8d-b9cc-ae08fed78808" />

  <img width="1191" height="319" alt="image" src="https://github.com/user-attachments/assets/7c122b50-9b9e-41b8-b273-99e28757d4e9" />

  <img width="1571" height="398" alt="image" src="https://github.com/user-attachments/assets/000edabd-d149-40f7-acec-bdb7e90171fc" />


4. Delete Lex chatbot

   <img width="1874" height="468" alt="image" src="https://github.com/user-attachments/assets/dd511689-be7f-4c0e-9b0e-9a13875c1d9f" />

   <img width="549" height="255" alt="image" src="https://github.com/user-attachments/assets/6cac41c9-27b9-4427-a7c2-432106cbbb83" />









 

 


  






 
 


  


     










  



  


 




   







 



  



  






