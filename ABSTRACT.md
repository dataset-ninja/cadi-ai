Authors introduce **CADI-AI: Cashew Disease Identification with AI**, a valuable dataset designed for object detection tasks, wherein a model has been rigorously trained to discern and pinpoint regions afflicted by the distinctive influences of abiotic factors, diseases, and insect infestations in cashew orchards. This dataset comprises 4,736 images containing a total of 22,609 labeled objects categorized into three distinct classes: *insect*, *disease*, and *abiotic*.

<img src="https://i.ibb.co/KwDCWhd/Screenshot-2023-10-26-180757.png" alt="image" width="800">

<span style="font-size: smaller; font-style: italic;">Class labels associated with data.</span>

## Motivation

The creation of this dataset represents a first contribution of drone data to the field of cashew crop research: Providing an open and accessible resource of high-quality, well-labeled drone imagery collected from Ghana Bono-Region, this dataset will offer data scientists, researchers, and social entrepreneurs within Sub-Saharan Africa and beyond, opportunities for innovative machine learning experiments and the development of solutions for infield cashew crop disease diagnosis and spatial analysis.

## About CADI-AI

Each instance in the dataset includes crop image (JPEG), image status (Disease, Abiotic, and Insect), file type (images and bounding box annotations) and location (this variable though is without values).

The dataset contains various instances that were captured in the Bono region, which is renowned for its cashew production. The data was collected in two rounds: The first data collection happened in November 2022, the second in January 2023. The data captured represents cashew data from a year where cashew blooming was particularly late. Given that the data was collected punctually only twice, it might be that not all blooming variations of Cashews have been captured, potentially influencing the variety of the collected data.

Each instance is associated with a class label based on the status of the crop. The labels are insect/pest, disease and abiotic:
- Insect/ pest stress factors represent the damage to crops by insects or pests
- Diseased factors represent attacks on crops by microorganisms.
- Abiotic stress factors represent stress factors caused by non-living factors, e.g. environmental factors like weather or soil conditions or the lack of mineral nutrients to the crop.

The decision to use the labels "abiotic", "disease", and "insect" for authors' object detection task was recommended by an agricultural scientist with expertise in crop health and disease management, Dr. Torkpor Stephen from University of Ghana.

It is important to note that while these labels provide a general categorization of crop damage, they may not fully capture the complexity of the underlying causes. In addition, the labels may not be exhaustive and other types of damage may not be captured by these categories. As with any dataset, users should be aware of the limitations and context of the labels used and exercise caution when interpreting the results of models trained on this data.

Examples of the limitations and complexities involved includes:
- A plant may exhibit symptoms of both insect damage and disease, making it difficult to assign a single label to the damage.
- Damage caused by abiotic factors such as drought or nutrient deficiency may be similar to damage caused by disease or insect infestation, leading to confusion when assigning labels.
- Damage caused by multiple factors may not fit neatly into a single label category, requiring more nuanced and complex labeling.
- Different species of insects or diseases may cause similar damage to crops, making it difficult to distinguish between them using only the three labels.
- Other factors such as environmental stress, mechanical damage, or chemical exposure may also cause damage to crops, but may not be captured by the current labels.

## Collection process

The images for the cashew data collection process were captured using a drone that was flown manually. The drone was flown at different altitudes to ensure that comprehensive information about the cashew crops was gathered. The photos of the cashew crop were taken at different angles with altitudes ranging from 2 to 10 meters. This altitude range provides a good balance between capturing a close-up view of the fruits and their growth stages and a wider perspective that allows for variation.

Preprocessing and labeling of the data were done during the data annotation stage using annotation tools (makesense.ai). Preprocessing of the data involved removing crop images in which human figures or faces were accidentally captured. Also blurry images were deleted.

The data was labeled by data scientists of KaraAgro AI who worked on this project. To ensure the accurate and efficient annotation of data, the team used advanced annotating tools (makesense.ai, roboflow) that offered various annotation formats (xml, yolo). Before the annotation process began, an expert in Agricultural Science reviewed the cashew images and provided comprehensive training on the annotation process, including appropriate labels (abiotic, insect, and diseased) to assign to each image.
