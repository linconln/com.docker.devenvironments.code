kubectl apply -f .

# cria o deploy e executa o consumer
# para gerar os dados, seria melhor um sistema web, mas perdi muito tempo com outros detalhes e mantive a lógica anterior
# executa o pod para alimentar o consumer e gerar os dados

kubectl exec consumer-584d69954-rn58c -- python producer.py

# os endereços dos relatórios são listados na tela, porém, com o endereço do host interno do POD
# para ver os resultados, expor o serviço com o minikube e abrir o minio

minikube service minio-svc --url