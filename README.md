## Requirements
Run the command-

		pip install -r requirements.txt

To install all the dependencies.


### Add New Faces

Run the command-

	   	python save_face.py
		
to add a new face which will be stored in a new folder- new_faces
Enter the id as 1 
After that it will ask the initial value, enter it as 1(if you are entering for the first time), otherwise as 301.
Webcam will take your 300 photos, or you can also add own photos in the new_faces folder. 

### Running the csv file

Run the command-

		python store_facial_features.py 

What this file does is it iteratively searches for every face in the faces folder, then computes the embeddings of each of them.
These embeddings are stored in a csv file called dataset.csv.

### Getting training and testing data from the csv file

Run the csv_to_pickle.py file
	
		python csv_to_pickle.py

4 new files will be created train_features, train_labels, test_features and test_labels.

### Train the model

Run the train_model_tf.py file to train using Tensorflow. Remember to delete the tmp/ folder first if other faces are added or else you will face errors with shape of the output data.

		python train_model_tf.py
Run the train_model_keras.py file to train using Keras

		python train_model_keras.py

Take Atleast 4 different faces for best result.

### Recognition

Make sure to run the train_model_keras.py file first.
		
		python recognize.py


