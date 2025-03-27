# Projeto: Pacote de Processamento de Imagens
## Autora do Projeto: Karina Kato
### Aula: Coding Lab PRO - Digital Innovation One
#### Tecnologia: Python
#### Data: 27/03/2025
-----------------------------------------
### Descrição
O pacote "image_processing_test" é usado para:

- **Módulo "Processing"**:
  - Correspondência de histograma;
  - Similaridade estrutural;
  - Redimensionar imagem;

- **Módulo "Utils"**:
  - Ler imagem;
  - Salvar imagem;
  - Plotar imagem;
  - Gerar gráfico de resultados;
  - Plotar histograma;
---------------------------------------------
## Passo a passo da configuração para hospedar um pacote em Python no ambiente de testes Test PyPI

1. **Instale as últimas versões de "setuptools" e "wheel"**:

   ```bash
   py -m pip install --user --upgrade setuptools wheel
   ```

2. **Certifique-se de que o diretório no terminal seja o mesmo do arquivo "setup.py"**:

   ```bash
   C:\Users\breno\image-processing-package> py setup.py sdist bdist_wheel
   ```

3. **Após a instalação, verifique se as pastas abaixo foram adicionadas ao projeto**:
   - `build`;
   - `dist`;
   - `image_processing_test.egg-info`.

4. **Suba os arquivos para o Test PyPI usando o Twine**:

   ```bash
   py -m twine upload --repository testpypi dist/*
   ```

5. **Insira o usuário e senha quando solicitado. Após isso, o projeto estará hospedado no Test PyPI.**

### Observação
O objetivo aqui não é utilizar o projeto da Karina para postar em meu perfil do PyPI pessoal, visto que o projeto é dela. Ainda não tenho nenhum projeto próprio que possa ser utilizado como pacote.

Tenha em mente que o Test PyPI é apenas um ambiente de testes. Para que o projeto esteja disponível como um pacote público, é necessário hospedá-lo no site oficial do PyPI.
----------------------------------------------------
## Instalação local, após hospedagem no Test PyPI

1. **Instale as dependências**:

   ```bash
   pip install -r requirements.txt
   ```

2. **Instale o pacote**:

   Use o gerenciador de pacotes para instalar o pacote hospedado no Test PyPI:

   ```bash
   pip install -i https://test.pypi.org/simple/ image-processing-test
   ```

   Ou instale diretamente:

   ```bash
   pip install image-processing-test
   ```
-------------------------------------------------
## Como usar em qualquer projeto

```python
from image_processing_test.processing import combination
combination.find_difference(image1, image2)
```

## Autor (quem hospedou o projeto no Test PyPI)
Breno Belchior Amaral

## Licença
[MIT](https://choosealicense.com/licenses/mit/)
