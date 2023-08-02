#Articles Schema
Generated using [DbSchema](https://dbschema.com)




### Articles Schema
![img](./ArticlesSchema.svg)



### Entity INSTANCE.Authors 
The authors entity contains information related to a particular author.

| | | | |
|---|---|---|---|
| * &#128273;  &#11019; | id| BIGINT  | Author id attribute - unique key |
| * | firstName| VARCHAR(100)  |  |
|  | middleInitials| VARCHAR(16)  |  |
| * | lastName| VARCHAR(100)  |  |


##### Indexes 
| | | |
|---|---|---|
| &#128273;  | pk\_Authors | ON id|



### Entity INSTANCE.article_authors 
| | | | |
|---|---|---|---|
| * &#128273;  &#11016; | article\_id| BIGINT  |  |
| * &#128273;  &#11016; | author\_id| BIGINT  | Author id attribute - unique key |


##### Indexes 
| | | |
|---|---|---|
| &#128273;  | pk | ON article\_id, author\_id|

##### Relationships
| | | |
|---|---|---|
|  | fk_article_authors_articles | ( article\_id ) ref [INSTANCE.articles](#articles) (id) |
|  | fk_article_authors_Authors | ( author\_id ) ref [INSTANCE.Authors](#Authors) (id) |




### Entity INSTANCE.article_keywords 
| | | |
|---|---|---|
| * &#128273;  &#11016; | article\_id| BIGINT  |
| * &#128273;  &#11016; | keyword\_id| BIGINT  |


##### Indexes 
| | | |
|---|---|---|
| &#128273;  | pk | ON article\_id, keyword\_id|

##### Relationships
| | | |
|---|---|---|
|  | fk_article_keywords_articles | ( article\_id ) ref [INSTANCE.articles](#articles) (id) |
|  | fk_article_keywords_keywords | ( keyword\_id ) ref [INSTANCE.keywords](#keywords) (id) |




### Entity INSTANCE.article_publishers 
| | | |
|---|---|---|
| * &#128273;  &#11016; | article\_id| BIGINT  |
| * &#128273;  &#11016; | publisher\_id| BIGINT  |


##### Indexes 
| | | |
|---|---|---|
| &#128273;  | pk | ON article\_id, publisher\_id|

##### Relationships
| | | |
|---|---|---|
|  | fk_article_publishers_articles | ( article\_id ) ref [INSTANCE.articles](#articles) (id) |
|  | fk_article_publishers_publishers | ( publisher\_id ) ref [INSTANCE.publishers](#publishers) (id) |




### Entity INSTANCE.articles 
| | | |
|---|---|---|
| * &#128273;  &#11019; | id| BIGINT  |
| * | title| VARCHAR(100)  |
|  | subtitle| VARCHAR(100)  |
| * | location| VARCHAR(256)  |
| * | filename| VARCHAR(100)  |
|  | publicationDate| DATE  |
|  | copyrightDate| DATE  |
|  | source| VARCHAR(256)  |


##### Indexes 
| | | |
|---|---|---|
| &#128273;  | pk\_articles | ON id|



### Entity INSTANCE.keywords 
| | | |
|---|---|---|
| * &#128273;  &#11019; | id| BIGINT  |
| * | keyword| VARCHAR(100)  |


##### Indexes 
| | | |
|---|---|---|
| &#128273;  | pk\_keywords | ON id|



### Entity INSTANCE.publishers 
| | | |
|---|---|---|
| * &#128273;  &#11019; | id| BIGINT  |
| * | publisher| VARCHAR(100)  |


##### Indexes 
| | | |
|---|---|---|
| &#128273;  | pk\_publishers | ON id|




