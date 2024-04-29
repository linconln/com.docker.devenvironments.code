kubectl apply -f .

# cria o deploy e executa o consumer
# para gerar os dados, seria melhor um sistema web, mas perdi muito tempo com outros detalhes e mantive a lógica anterior
# os endereços dos relatórios são listados na tela (logs), porém, com o endereço do host interno do POD
# para ver os resultados, expor o serviço com o minikube e abrir o minio

minikube service minio-svc --url