# CNN_Data_mining

!pip install kaggle
# This command installs the Kaggle API client library in your Python environment. 
# The Kaggle API allows you to interact with the Kaggle platform from within your Python scripts, making it easier to download and upload datasets.

from google.colab import drive
drive.mount('/content/drive')
# This connects your google Google Drive to the Colab notebook.

from google.colab import files
uploaded = files.upload()
# Download the API key from your Kaggle account by Account->Create new API Token-> download it to your local drive then upload it to the Colab.

!mkdir ~/.kaggle
# Create a new directory ~/.kaggle to store the kaggle API credentials file and which is used to help the user get access to datasets of Kaggle.

! cp kaggle.json ~/.kaggle/
# Copy the file named kaggle.json to the .kaggle directory in the home directory.

! chmod 644 ~/.kaggle/kaggle.json
# The owner of the file has read and write access, while the group members and other users on the system only have read access.

! kaggle datasets list
# This command lists all the datasets available in Kaggle.

! kaggle datasets download -d samaneheslamifar/facial-emotion-expressions
# Download the dataset for the CNN model.

! unzip facial-emotion-expressions.zip
# Unzip the dataset to model and train your data to achieve classification.
