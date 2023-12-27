# Object Detector dataset

## Descrição do dataset

O dataset apresenta imagens de objetos manufaturados aditivamente. Sendo composto por por imagens de 3 tipos de objetos manufaturados construídos por impressora 3D. Os objetos são dispostos nas imagens em diferentes posições e distâncias da câmera, cada imagem contém de 1 a 3 objetos. Cada imagem possui 600 pixels de altura e 800 pixels de largura. Os objetos estão localizados no centro da imagem, que possui um fundo da cor cinza. 

Os objetos presentes nas imagens do dataset são peças para a manutenção de elevadores. Além disso elas são utilizadas no projeto Flexible and Autonomous Manufacturing Systems for Custom-Designed Products (FASTEN) (https://inescbrasil.org.br/projetos/projeto-fasten/)  cujo obtivo é desenvolver um sistema de manufatura para produtos personalizados e de baixo custo.

O dataset foi anotado utilizando a ferramenta VGG Image Annotator (VIA) (https://www.robots.ox.ac.uk/~vgg/software/via/) que permite anotar diferentes informações da imagem. As informações anotadas foram: 

- Type (Tipo): A classe que o objeto pertence, part 1, part 2 ou part 3;
- Defect level (Nível de defeito): O nível de defeito do objeto:
    - 0 - Not visible defect (Sem defeitos visíveis): O objeto não apresenta nenhum defeito visível;
    - 1 - Few defects (Poucos defeitos): O objeto apresenta defeitos que podem ser removidos facilmente, exemplo, uma pequena sobressalência que ao manuseá-lo a mesma é removida;
    - 2 - Some defects, but do not interfere with the operation (Alguns defeitos que não interferem na operação do objeto): São defeitos que não interferem na operação do objeto, sendo em sua maioria defeitos estéticos que são facilmente removidos;
    - 3 - Too many defects, object can be discarded (Muitos defeitos, objeto pode ser descartado): O objeto apresenta muitos defeitos que interferem em sua operação, tornando-o inutilizável. O objeto deve então ser descartado para criação de um novo.
- Color (Cor): A cor do objeto, sendo elas: azul claro, azul escuro, branco, roxo ou laranja;
- Defect? (Defeituoso?): Informação se o objeto é defeituoso ou não, isto é, se ele possui algum tipo defeito, opções válidas: sim ou não.
- Defect type (Tipo do defeito): Define o tipo do defeito que o objeto possui, um objeto pode possuir mais de um tipo de defeito. Opções válidas: Warping, Delamination, Stringing, Overhangs, None (nenhum defeito).


## Dependências

- Ferramenta VIA.

# Demais repositórios

- API: https://github.com/LuckasMacedo2/object-detection-api;
- Aplicativo mobile: https://github.com/LuckasMacedo2/object-detection-app

# Arquivos presentes no repositório

- json_dataset.json: Arquivo JSON com as informações anotadas pela ferramenta VIA. Pode ser utilizado para processar os datasets, ou criar novos datasets. Obs.: A localização dos objetos estão no formato de de um poligôno, mas podem ser convertidos para o formato reconhecido por detectores de objetos convertendo um polígono para retângulo;
- Imgs: Pasta contendo todas as imagens para todos os objetos presentes no dataset. Trata-se, portanto do dataset completo. Os demais datasets a seguir são derivados deste:
- Object_isDefective_Dataset: Dataset com os objetos separados em defeituosos e não defeituosos. Estão separados em duas pastas de treino e teste, dentro de cada pasta estão separados conforme a classe - defeituoso (Defect) ou não defeituoso (OK).
- Defect_Level_Dataset: Dataset com os dados referentes ao nível do defeito dos objetos. Contém duas pastas de treino e teste cada uma contendo um dos 4 níveis de defeito que vão do zero até o três.

# Referências:

SILVA, L. M. D.; ALCALÁ, S. G. S.; BARBOSA, T. M. G. D. A. PROPOSTA DE MODELOS DE INTELIGÊNCIA ARTIFICIAL PARA DETECÇÃO DE DEFEITOS EM PEÇAS MANUFATURADAS ADITIVAMENTE. 2022. 

SILVA, L. M. DA; ALCALÁ, S. G. S.; BARBOSA, T. M. G. DE A. Detecção de produtos manufaturados defeituosos utilizando modelos de inteligência artificial. 2022b. 

MACEDO, L.; GOMES, S. UMA REVISÃO SISTEMÁTICA SOBRE A DETECÇÃO DE OBJETOS DEFEITUOSOS PRODUZIDOS POR MANUFATURA ADITIVA. Anais ... Encontro Nacional de Engenharia de Produção, 27 out. 2023. 

SILVA, L. M. D. et al. ALGORITMOS DE APRENDIZAGEM PROFUNDA PARA DETECÇÃO DE OBJETOS DEFEITUOSOS PRODUZIDOS POR MANUFATURA ADITIVA. 2023.

# English

# Object Detector dataset

## Dataset description

The dataset presents images of additively manufactured objects. Consisting of images of 3 types of manufactured objects built by 3D printer. Objects are arranged in the images at different positions and distances from the camera, each image contains 1 to 3 objects. Each image is 600 pixels high and 800 pixels wide. The objects are located in the center of the image, which has a gray background.

The objects present in the images in the dataset are parts for elevator maintenance. Furthermore, they are used in the Flexible and Autonomous Manufacturing Systems for Custom-Designed Products (FASTEN) project (https://inescbrasil.org.br/projetos/projeto-fasten/) whose objective is to develop a manufacturing system for personalized and low cost.

The dataset was annotated using the VGG Image Annotator (VIA) tool (https://www.robots.ox.ac.uk/~vgg/software/via/) which allows you to annotate different image information. The information noted was:

- Type: The class that the object belongs to, part 1, part 2 or part 3;
- Defect level: The defect level of the object:
     - 0 - Not visible defect: The object does not have any visible defects;
     - 1 - Few defects: The object has defects that can be easily removed, for example, a small protrusion that is removed when handled;
     - 2 - Some defects, but do not interfere with the operation: These are defects that do not interfere with the operation of the object, most of which are aesthetic defects that are easily removed;
     - 3 - Too many defects, object can be discarded: The object has many defects that interfere with its operation, making it unusable. The object must then be discarded to create a new one.
- Color: The color of the object, being: light blue, dark blue, white, purple or orange;
- Defect? (Defective?): Information whether the object is defective or not, that is, if it has some type of defect, valid options: yes or no.
- Defect type: Defines the type of defect that the object has, an object can have more than one type of defect. Valid options: Warping, Delamination, Stringing, Overhangs, None (no defects).


## Dependencies

- VIA tool.

# Other repositories

- API: https://github.com/LuckasMacedo2/object-detection-api;
- Mobile app: https://github.com/LuckasMacedo2/object-detection-app

# Files present in the repository

- json_dataset.json: JSON file with the information annotated by the VIA tool. It can be used to process datasets, or create new datasets. Note: The location of the objects are in the format of a polygon, but can be converted to the format recognized by object detectors by converting a polygon to a rectangle;
- Imgs: Folder containing all images for all objects present in the dataset. This is, therefore, the complete dataset. The following other datasets are derived from this one:
- Object_isDefective_Dataset: Dataset with objects separated into defective and non-defective. They are separated into two training and test folders, within each folder they are separated according to the class - defective (Defect) or not defective (OK).
- Defect_Level_Dataset: Dataset with data relating to the defect level of the objects. Contains two training and test folders each containing one of 4 defect levels ranging from zero to three.

# References:

SILVA, L. M. D.; ALCALÁ, S. G. S.; BARBOSA, T. M. G. D. A. PROPOSTA DE MODELOS DE INTELIGÊNCIA ARTIFICIAL PARA DETECÇÃO DE DEFEITOS EM PEÇAS MANUFATURADAS ADITIVAMENTE. 2022. 

SILVA, L. M. DA; ALCALÁ, S. G. S.; BARBOSA, T. M. G. DE A. Detecção de produtos manufaturados defeituosos utilizando modelos de inteligência artificial. 2022b. 

MACEDO, L.; GOMES, S. UMA REVISÃO SISTEMÁTICA SOBRE A DETECÇÃO DE OBJETOS DEFEITUOSOS PRODUZIDOS POR MANUFATURA ADITIVA. Anais ... Encontro Nacional de Engenharia de Produção, 27 out. 2023. 

SILVA, L. M. D. et al. ALGORITMOS DE APRENDIZAGEM PROFUNDA PARA DETECÇÃO DE OBJETOS DEFEITUOSOS PRODUZIDOS POR MANUFATURA ADITIVA. 2023.
