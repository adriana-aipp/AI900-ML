# -------------- Laboratório DIO Azure Machine Learning ------------------#

Finalidade: Gerar modelo de ML automatizado no Azure AI 

# Passos executados para geração do modelo e implantação das extremidades:

1)	Acessado o ambiente ML Azure 
2)	login efetuado na plataforma
3)	Selecionado o Workspace criado (AI-900 em minha conta Azure)
4)	Selecionado o botão <Iniciar o studio>
5)	Selecionada a opção <ML Automatizado> no menu lateral esquerdo
6)	Criado novo trabalho/tarefa de ML automatizado
7)	Informado dados de configuração básica (nome do trabalho, experimento e descrição) , acionado botão <avançar>
8)	Informado tipo de tarefa =  Regressão e acionada a opção criar na seção “Selecionar Dados”, na sequencia  foram preenchidos  os campos para criar o ativo de dados ( nome, descrição e tipo ) e acionado o botão <avançar>, na sequencia
9)	Selecionada o origem da fonte de dados, opção “De arquivos da Web” ,  acionado o botão <avançar>
10)	 Informado fonte = URL /Web publica onde está o arquivo  e acionado o botão <avançar>
11)	Configurados os parâmetros de arquivo de dados, tais como formato de arquivo, UTF, cabeçalho,  delimitador e acionado o botão <avançar>, na sequencia
12)	Na seção “Esquema” nenhuma alteração foi efetuada, apenas acionado o botão <avançar>
13)	Na seção “Examinar” ” nenhuma alteração foi efetuada, apenas acionado o botão <avançar><criar>
14)	Após o processamento foi selecionado o conjunto de dados “AlugueldeBicicletas” e acionado o botão <avançar>
15)	Por fim configurada a tarefa informando o tipo de tarefas e coluna destino =”rentals (Integer)” , informadas configurações adicionais sendo desmarcada as opções de métricas e selecionados os modelos permitidos tais como “RandomForest” e “LigthGBM”,  acionado o botão <salvar>
16)	Preenchido os parâmetros da Seção “Limites” com os seguintes valores respectivamente (3;3;3;0,85;15;15) e marcada a opção “Habilitar encerramento antecipado”
Preenchido os parâmetros da Seção “Validar e Testar” com os seguintes valores Tipo de Validação = “Divisão de Validação e Treinamento,  opção de validação de percentual de dados mantido = 10 , acionado o botão <avançar>
17)	Preservados os parâmetros da seção “Computação”, acionado o botão <avançar>
18)	Preservados os parâmetros da seção “Examinar” e por fim acionado o botão <Enviar trabalho de treinamento>
19)	Após aguardar a finalização da tarefa/JOB de autoML (descritos como “AlugueldeBicicletas:1”)  foi realizada a análise e validação começando por registrar o modelo no Azure na Lista de Modelos da seguinte forma:
a.	Acionada a opção <Modelo> no menu lateral esquerdo
b.	Registrado modelo com o nome  Bike-Teste-ML-Dio (tipo MFLOW)
c.	Selecionado o modelo Bike-Teste-ML-Dio
d.	Selecionada a tab “Detalhes” e clicado no link mslearn-bike-automl_2
e.	Selecionada a tab “Metrica” para validar valores e gráficos gerados pela aplicação exibindo a diferença entre valores previstos e os valores reais num histograma residual .
20)	Iniciada a Implantação do modelo da seguinte forma: 
a.	Selecionado modelo
b.	Acionada a opção < implantar >
c.	Preenchidos os parâmetros a seguir: 
i.	Ponto de extremidade = Novo
ii.	Máquina virtual – (sem alteração, valor padrão mantido) 
iii.	Contagem de instâncias – (sem alteração, valor padrão mantido)
iv.	Ponto de extremidade = Novo
v.	Nome do ponto de extremidade:  ai-900-ml-ydlaz 
vi.	Nome da implantação = bike-teste-ml-dio-1 
vii.	Acionado botão < Implantar> 
d.	Após o processamento foi gerado o seguinte arquivo ai-900-ml-jxumk (ponto de extremidade)
e.	Modelo disponibilizado para as opções teste, consumo e monitoramento.
