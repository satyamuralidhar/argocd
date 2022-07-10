# argocd
expose clusterIP to NodePort
$kubectl patch svc argocd-server -n argocd -p '{"spec": {"type": "NodePort"}}'

configure generic webhook trigger in jenkins
http://192.168.1.10:8080/generic-webhook-trigger/invoke?token=argocd
contenet type: application/json


