# CNN_cromossome

### Redes neuronais convolutivas utilizadas no PIBIC - Desenvolvimento de um algoritmo para segmentação de cromossomos.

#### Organização das pastas:
* *Modelos Salvos Coloridos* e *Modelos Salvos Segmentados*, contém os arquivos gerados na implementação dos códigos 
desenvolvidos.
    
   Internamente cada uma dessas pastas conterá subpastas que referênciam de forma mais detalhada ao qual código os 
   arquivos pertencem.
   
   * *Resultado_Image* : Imagens contendo as regiões classificadas na fase de teste, sendo **vermelho = não cromossomo** 
   e **verde = cromossomo**.
   * *Teste-ROC* : Curva ROC gerado após a fase de teste.
   * *Treino-Loss_Acurracy* : Gráfico contendo a variação da taxa de acurácia e perca, ocorrida durante a fase de treinamento.
   * *Arquivos com o nome weights* : Arquivos conténdo o peso das redes neurais utilizadas.


#### Nomenclatura dos arquivos:
* *Binaria*: Testes que utilizaram a base resultante da segmentação do algoritmo adaptativo.
* *Colorida*: Teste que utilizaram a base colorida do CRCN.
* *Rede 2*: Arquiteturas implementadas de forma sequencial.
* *Rede 3:* **Tentativa** de implementar as arquiteturas com duas entradas, sendo a primeira o recorte e a segunda o 
vetor de caracteristica do recorte.
* *Rede 4:* Implementação da janela deslizante.


#### Divisão das bases:
* *Base 1*: Dividida incorretamente. **Desconsiderar!**

Nas bases seguintes, selecionou-se 80% das imagens para treinamento, sendo 20% para validação, e utilizou os recortes 
das regiões de cromossomo e não cromossomo dessas imagens. Na fase de teste trabalhou-se com a imagem em sua completude,
inserindo regiões pré-definidas para serem testadas.
* Base 2: Imagens segmentadas ou coloridas, padronizadas ao tamanho de 120x120.
    * [Base binaria](https://bit.ly/2Wy7ZXN)
    * [Base Colorida](https://bit.ly/2FXPery)
* Base 3: Adcionou-se aos recortes das imagens segmentadas bordas com pixels pretos, com o intuito de deixar o tamanho dos recortes 
o mais proximo de 120x120, sem alterar a proporção das imagens em si.
    * [Base binaria](https://bit.ly/2FZolDK)