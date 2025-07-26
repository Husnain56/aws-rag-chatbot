# Aws-Rag-Chatbot

# COST
  The whole project should cost less than 1$ , make sure to delete resources at the end or you will get cooked :)

# Services Involved
  Amazon Lex, Bedrock, S3

# Steps

  !Make sure you are using IAM user
  
  # Request Access to the Amazon Bedrock Models(Titan Embeddings and Llama 3.1)
  
  1. Search for Amazon Bedrock

  <img width="1057" height="870" alt="image" src="https://github.com/user-attachments/assets/34a4d862-1c76-4a6d-8347-76984842a24c" />

  2. Click on Model access and Request for Titan Text Embeddings V2 and Llama 3.1 8B Instruct
  
  <img width="1843" height="855" alt="image" src="https://github.com/user-attachments/assets/1ed0d045-47d1-4b01-9893-3d1914c9c8a6" />]

  !You will have to click on "Available on request" first to get access to the models
  
  <img width="454" height="135" alt="image" src="https://github.com/user-attachments/assets/80a4dbda-d550-4256-bf92-54b460cb2630" />

# Documents that we'll use for RAG with Bedrock
  
  Any sort of documents with some text can be used for this project
  I have uploaded the documents in the repository which I am gonna use to test the model, You can use them too

# Create an S3 Bucket for document storage

  1. Search for S3
  
  <img width="959" height="352" alt="image" src="https://github.com/user-attachments/assets/8e8ee887-f4fa-4852-baed-38fea7fc70e0" />

  <img width="1844" height="846" alt="image" src="https://github.com/user-attachments/assets/18ec8f28-a82d-44f3-baf0-d92ce9689ae0" />

  2. Enter the Bucket name and leave the rest of the options as it is, scroll down and click create bucket

  <img width="1857" height="852" alt="image" src="https://github.com/user-attachments/assets/a215ac57-67b2-4dfe-be2d-730784722a3e" />

  3. Go your bucket , click add files, scroll down and click upload

  <img width="1015" height="215" alt="image" src="https://github.com/user-attachments/assets/ee6a6228-62f1-459c-a807-3a8b8bf3ec9b" />
  
  <img width="1495" height="426" alt="image" src="https://github.com/user-attachments/assets/d224d54f-785c-438e-a43f-d919c534aa65" />

  <img width="1677" height="533" alt="image" src="https://github.com/user-attachments/assets/1abc3b9e-a294-4673-9454-264dcdc2729c" />

  <img width="1623" height="662" alt="image" src="https://github.com/user-attachments/assets/6a745147-e1d4-4982-b59f-f9c5119db160" />

 # Create a knowledge base in Amazon Bedrock

   <img width="806" height="366" alt="image" src="https://github.com/user-attachments/assets/5e5702cd-6b84-419e-aa79-7b44f3fcff70" />

   1. Go Back to Amazon Bedrock , select Knowledge bases , click create and select Knowledge bases for vector store

   <img width="1866" height="862" alt="image" src="https://github.com/user-attachments/assets/65a4a701-6b90-4725-ae21-6a9e3515b8ee" />

   2. Enter name or keep it default, make sure S3 is selected as the data source and click next

   <img width="1586" height="813" alt="image" src="https://github.com/user-attachments/assets/390953ea-5f1c-4689-8c4b-fa000216b963" />

   3. Click on Browse S3

   <img width="1334" height="756" alt="image" src="https://github.com/user-attachments/assets/95eeb5c3-9b02-491a-90ea-110282c2dd23" />

   4. Select the bucket , scroll down and click next

   <img width="1753" height="279" alt="image" src="https://github.com/user-attachments/assets/3922be88-4cd9-4e08-bcc7-87a6eca64325" />
 
   5. Click on Select embedding model , choose Titan Text Embeddings V2 and choose the Amazon OpenSearch Serverless as your vector databse

   Text embedding: is a technique used in Natural Language Processing (NLP) to convert text (like words, phrases, or sentences) into numerical vectors. These vectors capture the semantic meaning of the text, allowing machines to          understand and process human language more effectively.

   A vector database: is a type of database designed to store, index, and search high-dimensional vectors—like the text embeddings.
   
   <img width="1604" height="595" alt="image" src="https://github.com/user-attachments/assets/a4af179d-8bd8-4149-9f02-0a6023685284" />

   <img width="745" height="612" alt="image" src="https://github.com/user-attachments/assets/ef5379e8-bf7d-4559-9d7d-bea79b13fefd" />

   <img width="1334" height="371" alt="image" src="https://github.com/user-attachments/assets/2bf4ec79-7394-41ed-894e-5b00b19d2345" />

   <img width="1443" height="759" alt="image" src="https://github.com/user-attachments/assets/2f07750f-e5de-42f6-a417-c6a22a43bcab" />







 



  



  






