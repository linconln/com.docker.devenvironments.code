kubectl apply -f .

# cria o deploy e executa o consumer
# como o python é interpretado, criei um container e copiei o código dos dois aplicativos criados
# a imagem chama o consumer na criação do container e coloquei a chamada do producer na subida do pod (funcionou no começo, mas depois deu erro)
# para gerar os dados, seria melhor um sistema web, mas perdi muito tempo com outros detalhes e mantive a lógica anterior
# PS. parou de funcionar da forma implementada anteriormente e mudei pra gerar o relatório com uma chamada direta no pod

kubectl exec consumer-???? -- python producer.py

# os endereços dos relatórios são listados na tela (logs), porém, não consegui o acesso direto aos arquivos
# para ver os resultados, expor o serviço com o minikube e abrir o minio

minikube service minio-svc --url

# faltou implementar os resources, secrets e hpa