1- the setup process:
	1.1- to run the code please install "sentence-transformers"
	by running the first cell:
	pip install -U sentence-transformers
	
	1.2- I am also using the os, and re libraries 
	os library: to access the working dirctory and using CLI.
	re library: to use the regular expresions.
	if you don't have them please install them also.
	
	1.3- add the files: "text.txt, lis.txt" to the working directry.
	
2-the used technologies:
	2.1-sentence-transformers: is a Python framework for state-of-the-art sentence, text and image embeddings. 
	The initial work is described in our paper Sentence-BERT: Sentence Embeddings using Siamese BERT-Networks.
	this framework is based on Pytorch and transformers, and they offer a large collection of pre-trained models tuned for various tasks.
	
	I used this frame work to create embeddings for various sentences.
	
	2.2- util.pytorch_cos_sim: this function is used to calculate the cosine similarity cos_sim between two sentences.
	
3- rational behind the design decisions:
	since the input is a text: the idea was to split it into sentences, since in english typically each sentence convay one idea.
	this means I need a model to process sentences instead of words, this is why I used the sentence-transformers framework.
	the pseudocode behind my code:
	
	initial_task():
		file_input =open the file of the text input
		sentences= list(read lines of file_input and split them into sentences using the re library).
		
		file_stan_phrase= open the file of the standarized phrases.
		standarized_phrases= list(read lines of file_stan_phrase and put each line as an element).
		
		model= SentenceTransformer('sentence-transformers/all-MiniLM-L6-v2') #initialize an instance of the sentence-transformers library.
		
		#define a dictionary to store embeddings of the standarized_phrases
		#I wanted to calculat the embedings only once to make the code run faster.
		for phrase in standarized_phrases:
			#get embeddings using the defined model.
			standardized_phrases_dict[phrase]= model.encode(phrase, convert_to_tensor=True)
			
		for sentence in sentences:
			sentences_dict[sentence]=model.encode(sentence, convert_to_tensor=True)
			
		#create a dictionary to store the similarities values
		similarities= dict()
		
		for key_stand,values_stand in standardized_phrases_dict.items():
			for key_sent, value_sent in sentences_dict.items():
				#the keys of the dictionary are the standarized_phrase and the input_sentence and the value is the similarity score.
				similarities[str(key_stand)+"__"+str(key_sent)]= util.pytorch_cos_sim(values_stand, value_sent)

		#I decided to keep all similarities because I wnated to show even the sentences that are not similar.
		store the similarities dict in a descending order
		
		print the keys and values when the similarities greater then a threshhold for example "0.4".
		
		

		
