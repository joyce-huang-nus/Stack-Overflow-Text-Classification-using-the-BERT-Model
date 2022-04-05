# Stackflow-text-classification-using-BERT-model
For final model I used the BERT model. First, I loaded in the BERT pretrained model configuration as tokenizer. From there, we then encoded the train, validation, and test data. The max_length of the text was set to be 128 and I split the data into input_ids, attention_masks and labels. Second, I loaded in the BERT pretrained model and create data loaders which combine dataset and sampler together. RandomSampler is used for training and SequentialSampler for validation. The batch_size is set to be 1 due to the limited memory in my Google Colab. Third, I created a scheduler with an AdamW optimizer and iterations of 1. I tried to run for 2 to 3 epochs, but due to the limited memory on my laptop, only 1 epoch worked successfully after multiple attempts. Finally, I started with my BERT model training process with free Tesla K80 GPU on Google Colab and saved my model in my device, so I can load my pretrained model and evaluate the performance.
