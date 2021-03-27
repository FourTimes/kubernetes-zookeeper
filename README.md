kubernetes zookeeper docker and yaml file

     kubectl exec -ti pod/zk-2 bash
     $ echo stat | nc localhost 2181 | grep Mode

     kubectl exec zk-0 zkCli.sh create /hello world

     kubectl exec zk-1 zkCli.sh get /hello

     kubectl get pods -w -l app=zk

     kubectl exec zk-2 zkCli.sh get /hello

     kubectl get sts zk -o yaml

     kubectl exec zk-0 cat /usr/etc/zookeeper/log4j.properties

     kubectl logs zk-0 --tail 20

     kubectl exec zk-0 -- ps -elf

     kubectl exec -ti zk-0 -- ls -ld /var/lib/zookeeper/data

     for i in 0 1 2; do kubectl get pod zk-$i --template {{.spec.nodeName}}; echo ""; done

     