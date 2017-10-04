h3. Delete a bunch of leftover cruft
kubectl get configmap | grep pytest | awk '{ print$1 }' | while read line ; do echo "$line" |  kubectl delete configmap "$line" ; done
