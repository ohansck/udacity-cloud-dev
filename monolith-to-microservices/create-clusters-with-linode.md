## Creating kubernetes clusters with linode (@Executioner on slack channel ALX-C2-En)
### Save AWS credits by creating clusters with [Linode](https://linode.com/calebcurry)

---

To create your cluster, take the following steps (screenshots in the Images folder):

1: Create a Linode account at [the Linode official website](https://linode.com/calebcurry), and recieve free $100 Linode credits

2: [Login](https://cloud.linode.com) to your account on [cloud.linode.com](https://cloud.linode.com)

3: <ul>
<li>Click on <b>Create</b>, select <b>Kubernetes</b>, than click on <b>Create</b></li>
<li>OR</li>
<li>Click on the left side menu, select <b>Kubernetes</b>, and click on <b>Create cluster</b></li>
</ul>

4: Choose <b>Cluster name</b>

5: Select a <b>Region</b>, preferably any of the first four

6: Select <b>Kubernetes version</b> (1.23)

7: In <b>Add Node Pools</b>, select <b>Shared CPU</b>

8: On <b>Linode 2 GB</b>, leave the default number as <b>3</b>, and click <b>Add</b>

9: Under <b>Cluster Summary</b>, select checkbox <b>Enable HA Control Plane</b>, and click <b>Create Cluster</b>

10: After a few seconds, your cluster dashboard will appear

11: Wait a few minutes for your <b>Kubeconfig</b> file <code>clusterName-kubeconfig.yaml</code> to be generated

12: Download the file to your local machine

13: <ul>
    <li>
    <ul>In <code>C:/Users/userName/.kube/</code> delete or move the already exisiting <code>config</code> file to a different location</ul>
       <ul><b>Rename</b> the downloaded <code>clusterName-kubeconfig.yaml</code> file to <code>config</code> without file extensions</ul>
       <ul>Copy <strong>config</strong> file to <code>C:/Users/userName/.kube/</code></ul>
  </li>
  <li>OR</li>
  <li><ul>

``` bash
cp ~/downloads/clusterName-kubeconfig.yaml ~/.kube/config
```
  </ul></li>
  </ul>
14: Run all kubectl commands as normal. Deploy your containers and services as normal <ul>

```bash
kubectl get pods
kubectl get deploy
kubectl apply -f aws-secret.yaml
kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/latest/download/components.yaml
kubectl replace --force -f udagram-feed-deployment.yaml
```
</ul>

16: Practice without the fear of finishing your AWS credits. Kubectl away!!!

---

[Follow me](https://github.com/ohansck) on github

[Connect](https://linkedin.com/in/ohaneme-kingsley) with me on LinkedIn

Kindly give this repo a star if you found it's content useful
