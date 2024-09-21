<!--StartFragment-->

**LLM Model Translation Notebook**

This notebook implements an AI model for translation, designed to handle tasks involving prediction, evaluation, and translation of text from English to Twi (A language spoken in Ghana). The model used in this machine translation project is "facebook/nllb-200-distilled-1.3B", which is part of the NLLB (No Language Left Behind) project by Facebook. The model is fine-tuned using LoRA (Low-Rank Adaptation) configuration for the sequence-to-sequence translation task. Here's a breakdown of the key points:



<!--EndFragment-->
<!--StartFragment-->

- **Model**: `facebook/nllb-200-distilled-1.3B` (NLLB-200)

- **Tokenizer**: `NllbTokenizerFast` with source language as `eng_Latn` and target language as `twi_Latn`

- **PEFT (Parameter-Efficient Fine-Tuning)**: LoRA configuration used to adapt the model with low-rank matrix approximations to efficiently fine-tune the model.

- **Task**: Sequence-to-sequence translation task using `AutoModelForSeq2SeqLM`.




<!--EndFragment-->
<!--StartFragment-->

- <!--StartFragment-->


  ## **Prediction Function**

  A function is created to generate predictions for the input dataset. It takes a test\_data Huggingface Dataset object, along with a trained model and tokenizer, and processes the data in batches.


  ## **Saving Predictions**

  Once predictions are generated, they are saved back into the original DataFrame, creating a new column, Predicted Translation, that holds the model's translation output.


  ## **Output and Export**

  Finally, the updated DataFrame with the original text and the corresponding translations is exported to a CSV file for submission.

  


  <!--EndFragment-->

<!--EndFragment-->
