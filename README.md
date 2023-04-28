# CS_548-Assignment4
Repository for HY-548 Assignment 4. AM: csd4054
## csd4054

---

### Task 1
  * a)
		
		kubectl apply -f fruit-crd.yaml
			
  * b)
	
		kubectl apply -f fruit-basket.yaml

  * c)
	
		kubectl get fruit apple -o yaml

  * d)

        kubectl get fruits

    ![1](task1/screenshots/1.JPG)
			

### Task 2
  * a)

		docker build -t toutou98/greeting-controller:latest .

        docker push toutou98/greeting-controller:latest
	
        Άρχικά παίρνει το image python:slim-buster και κάνει τα updates, κατεβάζει το kubectl και
        το κάνει εγκατάσταση. Έπειτα αντιγράφει στο /app τα 3 αρχεία που χρειάζονται και κάνει
        εγκατάσταση τα requirements. Τέλος τρέχει τον controller.

	![1](task2/screenshots/1.JPG)

  * b)

		Άρχικά κάνω apply το crd και το deployment:
        
        kubectl apply -f greeting-crd.yaml

        kubectl apply -f greeting-controler.yaml

        Μέσα στο deployment έχουμε ένα CLusterRole και βάζω το * στα rules για να
        είμαι σίγουρος ότι το role Θα έχει access όπου χρειάζεται. Έπειτα έχω ένα
        ClusterRoleBinding όπου κάνει reference το greeting-cluster-role και το κάνει
        bind με το service account. Τέλος είναι το deployment με το image που ανέβασα πριν.

        Για να επαληθεύσω ότι λειτουγεί σωστά μπορώ να δω με το:
        kubectl describe deployments και βλέπω ότι υπάρχουν τα σωστά δεδομένα στα deployments.

        Επίσης μπορώ να δω και τα logs του container που τρέχει το controller.py

	![2](task2/screenshots/2.JPG)
	![3](task2/screenshots/3.JPG)kubectl 


### Task 3
  * a)

		*text*
		
	![1](task3/screenshots/1.JPG)

		*text*

	![2](task3/screenshots/2.JPG)

		*text*

	![3](task3/screenshots/3.JPG)

		*text*