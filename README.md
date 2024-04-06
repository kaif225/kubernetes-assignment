To Successfully complete this assignment using the following steps
1. Created a deployment.yaml, service.yaml, hpa.yaml files
2.  then applied all the files using the commands
    -- kubectl apply -f deployment.yaml
    -- kubectl apply -f service.yaml
    --  kubectl apply -f hpa.yaml
3. Then run kubectl get svc to see the ip on which the service is running
4. Then run the following command to create a pod to generate load
   -- kubectl run -i --tty load-generator --rm --image=busybox --restart=Never -- /bin/sh -c "while sleep 0.01; do wget -q -O- http://ip:port_no; done
5. after this to monitore the creation the termination of pods i have run
   -- watch kubectl get pods
6. And to see the load distribution run
   -- kubectl get hpa
