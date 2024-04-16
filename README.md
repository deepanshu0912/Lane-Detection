# Lane-Detection
Developed a deep learning Image segmentation approach to identify lanes in a driving scenario

README
Folder Structure
1. Unet: Unet implementation
2. ERnet.ipynb : ERNet implementation
3. Processed.ipynb : to preprocess Dataset and create binary mask 4. Preprocessed_color.ipynb: To create Instance masks
5. CustomLoss.ipynb
Steps to Follow:
1. Past the DataSet folder in the main folder.
2. Go into to Processed.ipynb and follow these steps: #Description of Dataset:
           The lane marking is the main component on the
           highway. It instructs the vehicles interactively and
           safely drive on the highway. Lane detection is a
           critical task in autonomous driving, which
           provides localization information to the control of
           the car. We provide video clips for this task, and
           the last frame of each clip contains labelled
           lanes. The video clip can help algorithms to infer
           better lane detection results.
      ## Dataset Size
           3626 video clips, 3626 labelled frames.
           Information of each clip: 20 frames for
           each one.
      ## Directory Structure:
           |
           |
           |
           |----clips/ #
           video clips, 3626 clips
           |------|
           |------|----some_clip/ #
           Sequential images for the clip, 20 frames
           |------|----...
           |
           |----label_data_0313.json #
           Label data for lanes
           |----label_data_0531.json #
           Label data for lanes
           |----label_data_0601.json #
           Label data for lanes
#Description of the ENet Code:
      It contains a Class names LaneDataset in this
      while initliazation in __init__ change
dataset_path="C:/Users/azhar/OneDrive/Desktop/DL lab/data/lane
detection/ TUSimple/train_set" : to path where dataset is located
#Description of the PreProcessed.ipynb:
      clips =
      '/Users/deepanshubissu/Desktop/DL_Project/TuSimple/TUSimple/train_se
      t/clips/'
      new_frames = '/Users/deepanshubissu/Desktop/DL_Project/Colouring
      Lanes/tusimple_preprocessed/
      training/frames'
      change clips to where clips is located in your
      dataset and new_frames is folder where coloured
      frames will be store create it
      df_0601 = pd.read_json('/Users/deepanshubissu/
      Desktop/DL_Project/TuSimple/TUSimple/train_set/
      label_data_0601.json', lines=True)
      df_0313 = pd.read_json('/Users/deepanshubissu/
      Desktop/DL_Project/TuSimple/TUSimple/train_set/
      label_data_0313.json', lines=True)
      df_0531 = pd.read_json('/Users/deepanshubissu/
      Desktop/DL_Project/TuSimple/TUSimple/train_set/
      label_data_0531.json', lines=True)
      df = pd.concat([df_0601, df_0313, df_0531])
      change the path of these json files accordingly
      as mentioned in above description of dataset
To Run the Unet Code:
      Go to Train.ipynb and change the paths according to the mentioned
above and run the inference.
CustomLoss.ipynb:
 It contains the Custom loss implemented class
