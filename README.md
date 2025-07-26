# Aws-Rag-Chatbot

# COST
  The whole project should cost less than 1$ , make sure to delete resources at the end or you will get cooked :)

# Services Involved
  Amazon Lex, Bedrock, S3

# Steps

  !Make sure you are using IAM user
  
  # Request Access to the Amazon Bedrock Models(Titan Embeddings)
  
  1. Search for Amazon Bedrock

  <img width="1057" height="870" alt="image" src="https://github.com/user-attachments/assets/34a4d862-1c76-4a6d-8347-76984842a24c" />

  2. Click on Model access and Request access for Titan Text Embeddings V2 , scroll down and submit
  
   <img width="1590" height="826" alt="image" src="https://github.com/user-attachments/assets/23b441c0-2dd5-469a-b35a-09c58b0b9763" />

   
   <img width="1829" height="565" alt="image" src="https://github.com/user-attachments/assets/719c7eff-7478-432b-a1b6-adb636f38ba4" />


   <img width="1559" height="192" alt="image" src="https://github.com/user-attachments/assets/a8509aa3-f200-4c36-8660-bd8c2c9bf1ef" />



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

   Text embedding: is a technique used in Natural Language Processing (NLP) to convert text (like words, phrases, or sentences) into numerical vectors. These vectors capture the semantic    meaning of the text, allowing machines to understand and process human language more effectively.

   A vector database: is a type of database designed to store, index, and search high-dimensional vectors—like the text embeddings.
   
   
   <img width="1604" height="595" alt="image" src="https://github.com/user-attachments/assets/a4af179d-8bd8-4149-9f02-0a6023685284" />
   

   <img width="745" height="612" alt="image" src="https://github.com/user-attachments/assets/ef5379e8-bf7d-4559-9d7d-bea79b13fefd" />
   

   <img width="1334" height="371" alt="image" src="https://github.com/user-attachments/assets/2bf4ec79-7394-41ed-894e-5b00b19d2345" />
   

   <img width="1443" height="759" alt="image" src="https://github.com/user-attachments/assets/2f07750f-e5de-42f6-a417-c6a22a43bcab" />


   <img width="920" height="324" alt="image" src="https://github.com/user-attachments/assets/aa9d7dfc-f953-41f9-8cc9-5d830e43727a" />


  6. Once the database is ready , go to data sources and select the data source and sync

  
   <img width="1720" height="591" alt="image" src="https://github.com/user-attachments/assets/652445e0-2da9-4153-9900-9c5bb2c477da" />

  
# Create an Amazon Lex Bot


  <img width="853" height="319" alt="image" src="https://github.com/user-attachments/assets/ee4b9590-2daf-4846-9705-535bece63ee2" />


  <img width="849" height="876" alt="image" src="https://github.com/user-attachments/assets/4487ebbe-ef13-4982-b5a9-2ed99f52cb5e" />  
  

  1. Create a Bot

  <img width="1807" height="837" alt="image" src="https://github.com/user-attachments/assets/426e3116-52dc-4c15-aae0-d759c9647260" />

  2. Configure settings

  <img width="1168" height="783" alt="image" src="https://github.com/user-attachments/assets/650b2d93-1d47-46c6-9d55-938b8363f4af" />
  

  <img width="1029" height="493" alt="image" src="https://github.com/user-attachments/assets/e21e2321-6502-4fab-9c55-9a412c7103e5" />


  <img width="915" height="618" alt="image" src="https://github.com/user-attachments/assets/e2e890e0-fb77-4bf0-8c3b-e92ecf78aa34" />


# Building out an intent in Amazon Lex


  <img width="1842" height="854" alt="image" src="https://github.com/user-attachments/assets/13156cc3-b70e-4405-8536-2daf39309a1e" />
  

  1. We can set our own Intent name and utterances like:
     

  <img width="767" height="603" alt="image" src="https://github.com/user-attachments/assets/d0d191b0-36f9-48cb-b3d2-2cf78c6c1cb4" />

  <img width="764" height="373" alt="image" src="https://github.com/user-attachments/assets/b1c7dc7d-e5c1-4871-8d7c-9dfeaab57ab5" />

  <img width="699" height="833" alt="image" src="https://github.com/user-attachments/assets/8d84c04d-b5df-4cb6-baa3-5f4b7c5226e4" />

  2. Save the intent by scrolling down and click "back to intents list" 

  <img width="348" height="347" alt="image" src="https://github.com/user-attachments/assets/0e1f62a8-9a28-4f13-88a1-3084fd8a9739" />

  !Every bot has a FallbackIntent which gets created automatically and it is invoked when the message doesn't matches with custom intents

  3. Click on Build button
     
  <img width="1573" height="392" alt="image" src="https://github.com/user-attachments/assets/f4ee922c-61f4-4c91-a3fb-e98fa6d35e8a" />


  4. Once it is finished building we can test it out


  <img width="1576" height="444" alt="image" src="https://github.com/user-attachments/assets/2f961b15-9163-45b0-aa3e-d87f1f15b9cd" />


  <img width="740" height="556" alt="image" src="https://github.com/user-attachments/assets/f81e74ec-bee9-4a2b-b74a-3f1842a9ebfa" />


  <img width="734" height="567" alt="image" src="https://github.com/user-attachments/assets/c3b07d39-7e5d-4fe2-88fe-13899dafbfee" />


# Add the QnA Intent to get generative AI capabilities in Amazon Lex chatbot


  <img width="380" height="204" alt="image" src="https://github.com/user-attachments/assets/5daab784-798d-4391-b273-c563ddd8a21b" />


  <img width="558" height="395" alt="image" src="https://github.com/user-attachments/assets/287561b4-2a92-4454-bbcc-2303fdbd62b7" />


  <img width="575" height="244" alt="image" src="https://github.com/user-attachments/assets/18acc9cd-0e2d-4b40-85a6-7ec55c7e7491" />


  2. Select the model

  <img width="606" height="334" alt="image" src="https://github.com/user-attachments/assets/61ff4c76-31b1-428c-a00f-9dcaf3441f32" />


  3. Go back to Amazon bedrock and the knowledge base id 

  


     










  



  


 




   







 



  



  






