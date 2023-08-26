To play with a test dataset choose one of the example files in the "Choose a test 📁 dataset" widget. The app will load the file and automatically map the columns 🏛️.

To upload your own dataset you need to have an activation key *🔑*. Drop me a mail at fabio.annovazzi at gmail.com. 

*Until further notice the app is free to use (as in free🍺) with the "Mparanza"activation token🗝️ 😊😊😊.*

Your file in never saved on 🖴disk and is completely discarded from RAM once you close your session. The app does not log user sessions and does not have a username 👤 login mechanism.  

You can upload an Excel dataset, or a CSV dataset in UTF-8 format. 

It must be a flat tidy file, one row per observation. This is probably the dataset you are already using for your sales analysis. [Here](https://mparanza.com/site/EXAMPLE_DATASET/) you can see examples of dataset structure. Click [here](https://mparanza.com/download_docs/Superstore.xlsx) to download an example dataset.

Your dataset must have at least a metric column with your revenues 💰 (or costs 💸 if you are doing cost analysis) that **you want to call "Amount"**. Set this column as numeric in Excel, with no thousands separators or 💲 currency signs. 

You can also have other metric columns, such as **"Units"** (number of products sold), **"Volume"** (quantity of product sold), **"Discounts"** and **"COGS"**.

Your dataset also must have a Date 📅 column (aka a column in date format, that **you want to call "Date"**) and/or a Period/Scenario column (if you want to compare Plan with Actual for instance) that **you want to call "Period" or "Scenario"**.

Your dataset can have any number of dimensions (such as Customer, Channel, Product, Line, Division,...) that you can name as you like. 

If your dimensions are in separate datasets from your main, "fact", dataset, you can join⛓️ them using the app as long as the keys are unique and named in the same way in both datasets.  

Use the second, "📤 upload and join⛓️dimension tables" uploader to upload the "dim" datasets. You can then download ⬇️ the joined table to avoid doing the join each time you use the app.

Open the ""➕ 🔍 Detected columns" and the "➕ 📁 Dataset info" expanders to check that your dataset has been correctly mapped and loaded in the app.

 
