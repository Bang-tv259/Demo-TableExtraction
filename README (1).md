# Demo Table Extraction

A deep learning model based on object detection for extracting tables from PDFs and images.

First proposed in ["PubTables-1M: Towards comprehensive table extraction from unstructured documents"](https://openaccess.thecvf.com/content/CVPR2022/html/Smock_PubTables-1M_Towards_Comprehensive_Table_Extraction_From_Unstructured_Documents_CVPR_2022_paper.htm

![table_extraction_v2](https://user-images.githubusercontent.com/10793386/139559159-cd23c972-8731-48ed-91df-f3f27e9f4d79.jpg)

This repository also contains the official code for these papers:
- ["GriTS: Grid table similarity metric for table structure recognition"](https://arxiv.org/abs/2203.12555)
- ["Aligning benchmark datasets for table structure recognition"](https://arxiv.org/abs/2303.00716)

Note: If you are looking to use Table Transformer to extract your own tables, here are some helpful things to know:
- TATR can be trained to work well across many document domains and everything needed to train your own model is included here. But at the moment pre-trained model weights are only available for TATR trained on the PubTables-1M dataset. (See the additional documentation for how to train your own multi-domain model.)
- TATR is an object detection model that recognizes tables from image input. The inference code built on TATR needs text extraction (from OCR or directly from PDF) as a separate input in order to include text in its HTML or CSV output.

Additional information about this project for both users and researchers, including data, training, evaluation, and inference code is provided below.

## Generation Table
Technology: Python, CTGAN
![GenTable](https://user-images.githubusercontent.com/10793386/139559159-cd23c972-8731-48ed-91df-f3f27e9f4d79.jpg)

`08/22/2023`: We have released 3 new pre-trained models for TATR-v1.1 (trained on 1. PubTables-1M, 2. FinTabNet.c, and 3. both datasets combined) according to the details in [our paper](https://arxiv.org/abs/2303.00716).\
`04/19/2023`: Our latest papers ([link](https://arxiv.org/abs/2203.12555) and [link](https://arxiv.org/abs/2303.00716)) have been accepted at [ICDAR 2023](https://icdar2023.org/).\
`03/09/2023`: We have added more image cropping to the official training script (like we do in our most recent paper) and updated the code and environment.yml to use Python 3.10.9, PyTorch 1.13.1, and Torchvision 0.14.1, among others.\
`03/07/2023`: We have released a new simple [inference pipeline](src/inference.py) for TATR. Now you can easily detect and recognize tables from images and convert them to HTML or CSV.\
`03/07/2023`: We have released a [collection of scripts](scripts/) to create training data for TATR and to canonicalize pre-existing datasets, such as FinTabNet and SciTSR.\
`03/01/2023`: New paper "Aligning benchmark datasets for table structure recognition" is now available on [arXiv](https://arxiv.org/abs/2303.00716).\
`11/25/2022`: We have made the full PubTables-1M dataset alternatively available for download from [Hugging Face](https://huggingface.co/datasets/bsmock/pubtables-1m).\
`05/05/2022`: We have released the pre-trained weights for the table structure recognition model trained on PubTables-1M.\
`03/23/2022`: Our paper "GriTS: Grid table similarity metric for table structure recognition" is now available on [arXiv](https://arxiv.org/abs/2203.12555)\
`03/04/2022`: We have released the pre-trained weights for the table detection model trained on PubTables-1M.\
`03/03/2022`: "PubTables-1M: Towards comprehensive table extraction from unstructured documents" has been accepted at [CVPR 2022](https://cvpr2022.thecvf.com/).\
`11/21/2021`: Our updated paper "PubTables-1M: Towards comprehensive table extraction from unstructured documents" is available on [arXiv](https://arxiv.org/pdf/2110.00061.pdf).\
`10/21/2021`: The full PubTables-1M dataset has been officially released on [Microsoft Research Open Data](https://msropendata.com/datasets/505fcbe3-1383-42b1-913a-f651b8b712d3).\
`06/08/2021`: Initial version of the Table Transformer (TATR) project is released.


