# YelpZip Dataset for spam review detection and sentiment analysis

This repository contains the **YelpZip dataset**, introduced in the paper:

**"Collective Opinion Spam Detection: Bridging Review Networks and Metadata"**  
by *Shebuti Rayana* and *Leman Akoglu* (KDD 2015)

This is the dataset that is used on our research paper **Enhancing Fake Review Detection in E-Commerce Platforms Using RoBERTa-GRU: A Hybrid Deep Learning Approach**

The dataset is labeled for **spam review detection** but may also be used for **sentiment analysis**.

--

## Dataset Structure
Review Content
- `reviewContent.txt` | Contains raw review text | 
- `metadata.txt` | Includes review metadata | `user_id`, `prod_id`, `rating`, `label`, `date` |
- `reviewGraph.txt` | Used for graph based models | `user_id`, `prod_id`, `rating` |

ID Mapping
- `userIdMapping.txt` | Maps original `user_id`s to unique numerical IDs |
- `productIdMapping.txt` | Maps original `prod_id`s to unique numerical IDs |

--

## How to Use

To extract feature or train models you would typically merge `reviewContent.txt` and `metadata.txt`.
To use on graph based models you may need `reviewGraph.txt`, along with the ID Mapping files

## Metadata
Format for data contained in `metadata.txt` follows this structure:
- `user_id`: reviewer identifier  
- `prod_id`: product/business identifier  
- `rating`: 1–5 stars  
- `label`: 1 (real) or -1 (spam)  
- `date`: review date

## Citation
### BibTeX
```
@inproceedings{DBLP:conf/sigkdd/Akoglu15,
  author = {Shebuti Rayana and Leman Akoglu},
  title = {Collective Opinion Spam Detection: Bridging Review Networks and metadata},
  booktitle = {Proceeding of the 21st ACM SIGKDD international conference
  on Knowledge discovery and data mining, {KDD�15}},
  year = {2015},
}
```
