# ODM Operator
<h1 align="center">
  <br>
  <a href="https://github.com/SaifRehman/mongo-rest-operator"><img src="https://thumbor.forbes.com/thumbor/960x0/https%3A%2F%2Fblogs-images.forbes.com%2Fjanakirammsv%2Ffiles%2F2018%2F05%2Frh-os.jpg" alt="openshift" width="IBM"></a>
  <br>
      ODM operator for Openshift
  <br>
  <br>
</h1>

<h4 align="center">Powered by Openshift and OperatorSDK</h4>

<p align="center">
  <a>
    <img src="https://img.shields.io/travis/keppel/lotion/master.svg"
         alt="Travis Build">
  </a>
</p>
<br>
ODM installation via Operator

## Install Operator on Openshift

1. clone the repo
```
$ git clone https://github.com/SaifRehman/odm-operator.git
```
2. install ***serviceaccount***, ***rolebinding***, ***role***, ***crd***, and ***operator***
```
$ oc apply -f deploy/service_account.yaml
$ oc apply -f deploy/role.yaml
$ oc apply -f deploy/role_binding.yaml
$ oc apply -f deploy/operator.yaml
$ oc apply -f deploy/crds/mongorest_v1alpha1_mongorest_crd.yaml
$ oc apply -f sc.yaml
```
## Deploy ODM in minutes 
``` YAML
apiVersion: ibm.odm.com/v1alpha1
kind: Odm
metadata:
  name: odm
spec:
  license: accept
```
4. Apply these YAML configuration