# argocd
expose clusterIP to NodePort
$kubectl patch svc argocd-server -n argocd -p '{"spec": {"type": "NodePort"}}'
