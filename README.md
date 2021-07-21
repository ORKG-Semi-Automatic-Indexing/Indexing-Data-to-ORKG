# [Indexing Data to ORKG](https://www.orkg.org/orkg/)

## Question
> ___"How do microbiomes behave in obesity?"___

## Goal description
The aim of the project was to extract the metadata of publications on the topic of microbiome obesity from the PubMed metadatabase using the Entrez API. The data was to be stored in a data frame and entered into the ORKG database. 

### What is ORKG?
"The Open Research Knowledge Graph (ORKG) project works on answers and solutions to the next generation of digital libraries so that scholarly publications are semantically
connected to each other and to other research objects. ORKG focuses on the publication content, e.g., research problem, hypothesis or related data, making it easier to compare
publications based on the facts they contain and discuss. It offers multiple views including data tables and graphs. Researchers can directly add their articles and start
describing their content and connect them to others. ORKG aims to describe research papers in a structured manner. With the ORKG, papers are easier to find and compare."

### Workflow
![image](https://user-images.githubusercontent.com/49281346/126359518-65f798d7-2398-45dd-8236-4814f760a8b0.png)

### Procedure
To add new papers into the ORKG a specific question is important but not necessary. In this project the top 10 documents from [PubMed]( https://pubmed.ncbi.nlm.nih.gov/) for the query “microbiome obesity” are added into the graph. After the data of the documents was retrieved, the dataframe needs the right format as shown [here]( https://gitlab.com/TIBHannover/orkg/orkg-pypi/-/wikis/Tutorial:-importing-papers-in-CSV-format-into-the-ORKG). The columns research_field and research_problem needed to be added manually. For the research_field column the right researchfield needs to be found at the [Research fields taxonomy](https://www.orkg.org/orkg/fields) from the ORKG and added manually into the dataframe. <img src=https://user-images.githubusercontent.com/49280839/126453457-d3972429-0956-4299-956c-85c86495abfb.png width=50% height=50%>
 To add the research_problem a summarizing sentence about the question the researcher wants to answer must be added. Also some aditional Keywords can be added so the papers can connect to papers about the same issue. To add these keywords the [Human Disease Ontology](https://bioportal.bioontology.org/ontologies/DOID?p=classes&conceptid=http%3A%2F%2Fpurl.obolibrary.org%2Fobo%2FUBERON_0004119) is needed. With the [annotator](https://bioportal.bioontology.org/annotator) it is simple to find the right terms. The keywords must be formulated as triples as shown here ![triples](https://user-images.githubusercontent.com/49280839/126453487-e6e4fdeb-9f2f-48e9-adf5-216d6affa291.png)

After the manual work is done the dataframe can be saved as csv and is ready to push. Pushing papers into the ORKG is simple, just two lines of code. After the push we can edit the papers everytime we want. ![graph](https://user-images.githubusercontent.com/49280839/126453404-ee4660c1-dec8-45f1-812d-0ee35d39e4a8.png)


### Lessons learned 
- Define research question at the beginning!
- Expert discussions rather at the beginning 
- Define work packages with output
- Better communication with the TIB
- Define what information is needed for the ORKG

### Project continuation
- Apply other research questions
- Extract more paper
- Automatic approach 

## License
Code is under the BSD 2 Clause (NetBSC) license. For further information take a look at the License document in this repository.
