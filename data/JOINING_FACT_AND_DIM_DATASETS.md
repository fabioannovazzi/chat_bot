To avoid doing the vlookup in excel you can add dimension columns to your dataset. Simply upload one or more "dimension" datasets to 'Mparanza along with your main "fact" dataset.  

Just make sure that the key columns in the two files have the same name and that the key column in the dimension file does not have duplicate entries.  

You can upload more than one "dimension" file. A dimension file can have more than two columns.

Upload your "dimension" files using the "Upload and join dimension tables" upload widget. This widget will appear once you have uploaded your main "fact" csv file.

'Mparanza will automatically left-merge the two "dimension" files to your "fact" file. You can download the joined file to avoid having to join it again in the future.

