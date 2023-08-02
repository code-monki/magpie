#Book Schema
Generated using [DbSchema](https://dbschema.com)




### Book Schema
![img](./BookSchema.svg)



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



### Entity INSTANCE.book_authors 
| | | | |
|---|---|---|---|
| * &#128273;  &#11016; | book\_id| BIGINT  |  |
| * &#128273;  &#11016; | author\_id| BIGINT  | Author id attribute - unique key |


##### Indexes 
| | | |
|---|---|---|
| &#128273;  | pk | ON book\_id, author\_id|

##### Relationships
| | | |
|---|---|---|
|  | fk_book_authors_books | ( book\_id ) ref [INSTANCE.books](#books) (id) |
|  | fk_book_authors_Authors | ( author\_id ) ref [INSTANCE.Authors](#Authors) (id) |




### Entity INSTANCE.book_keywords 
| | | |
|---|---|---|
| * &#128273;  &#11016; | book\_id| BIGINT  |
| * &#128273;  &#11016; | keyword\_id| BIGINT  |


##### Indexes 
| | | |
|---|---|---|
| &#128273;  | pk | ON book\_id, keyword\_id|

##### Relationships
| | | |
|---|---|---|
|  | fk_book_keywords_books | ( book\_id ) ref [INSTANCE.books](#books) (id) |
|  | fk_book_keywords_keywords | ( keyword\_id ) ref [INSTANCE.keywords](#keywords) (id) |




### Entity INSTANCE.book_publishers 
| | | |
|---|---|---|
| * &#128273;  &#11016; | book\_id| BIGINT  |
| * &#128273;  &#11016; | publisher\_id| BIGINT  |


##### Indexes 
| | | |
|---|---|---|
| &#128273;  | pk | ON book\_id, publisher\_id|

##### Relationships
| | | |
|---|---|---|
|  | fk_book_publishers_books | ( book\_id ) ref [INSTANCE.books](#books) (id) |
|  | fk_book_publishers_publishers | ( publisher\_id ) ref [INSTANCE.publishers](#publishers) (id) |




### Entity INSTANCE.books 
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
|  | isbn| VARCHAR(32)  |
|  | volume| VARCHAR(32)  |


##### Indexes 
| | | |
|---|---|---|
| &#128273;  | pk\_articles\_0 | ON id|



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




