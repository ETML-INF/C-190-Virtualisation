# 🖥️ E06 - Étude de Coûts

Nom : _______________  
Prénom : _______________   
Date : _______________

---

## 🎯 Objectifs
L’objectif de cet exercice est de comparer le prix d’une solution virtuelle par rapport à une solution comprenant **50 serveurs physiques**.

---

## ⏳ Temps à disposition
**45 minutes**

---

## 📊 Étude de Coûts

Si on considère une solution purement **physique** permettant de faire tourner **50 services** sur **50 serveurs rackables 1U**, chaque serveur coûtant **2'000 CHF** et consommant **700W**. L’infrastructure comprend également **2 racks serveurs de 42U**, à **3'500 CHF** chacun.

Le **prix de l'électricité** est de **0.21 CHF/kWh**.

Votre tâche est de **proposer une solution virtualisée** permettant d’héberger ces **50 services** sur **2 hyperviseurs redondants**.

1. **Recherchez** sur Internet **un ou deux serveurs du marché** capables de remplir ce rôle.
2. **Comparez** les prix, l’encombrement et la consommation électrique des **2 solutions** (physique vs virtualisée) sous forme d’un fichier Excel.
3. **Prenez en compte les coûts des licences** :
   - **vSphere Enterprise Plus** : **4'500 CHF / CPU**
   - **VMware vCenter Server Standard Edition** : **10'500 CHF**


---

## 🖥️ Hypothèses et Indications
- Chaque service requiert en moyenne **1 vCPU et 4GB de RAM**.
- **Calcul des vCPU disponibles :**
  - **Avec hyper-threading** : `1 CPU * 4 cœurs * 2 = 8 vCPU`
  - **Sans hyper-threading** : `1 CPU * 4 cœurs * 1 = 4 vCPU`
- **Électricité** : Calculer la consommation annuelle en **kWh** pour chaque solution.

**🔗 Ressources utiles :**  
[Spiceworks - Cores, Logical Processors & vCPU en VMware](https://community.spiceworks.com/topic/426675-physical-cores-logical-processors-and-vcpu-in-vmware)

---

## 📊 Tableau des coûts **avant virtualisation** (infrastructure physique)

| Description | Quantité | Prix Unitaire | Montant Total | Consommation Électrique |
|-------------|---------|--------------|---------------|-------------------|
| **Serveurs** | 50 | 2'000 CHF | 100'000 CHF | 700W par serveur |
| **Racks** | 2 | 3'500 CHF | 7'000 CHF |   |
| **Total** | - | - | **107'000 CHF** | - |
| **Électricité (consommation annuelle)** | 306'600 kWh | 0.21 CHF/kWh | **64'386 CHF** | - |

---

✍️ **Comparez ensuite avec votre solution virtualisée et calculez l’économie potentielle réalisée !** 🚀

