---
marp: true
theme: default
paginate: true
footer: "ETML - Module C190 - AGR"
---
<!-- header: "C-190 - Le licensing des produits VMware" -->
# C-190 - Le licensing des produits VMware

# Plan du cours
- Introduction
- Types de licences VMware
- Modèles de licence
- Différences avec les serveurs physiques
- Problématique des licences d'autres fournisseurs à cause de la virtualisation - Exemple avec Oracle
- Conclusion

---
<!-- header: "C-190 - Le licensing des produits VMware > Introduction" -->
## Introduction
La gestion des licences est un aspect crucial de l'utilisation des produits VMware. Comprendre les différents types de licences et comment les gérer efficacement peut aider à optimiser les coûts et à garantir la conformité.

---

## Types de licences VMware
- **Licence par cœur** : Basée sur le nombre de cœurs physiques dans les hôtes ESXi, avec un minimum de 16 cœurs par processeur.
- **Licence par abonnement** : Basée sur un modèle de paiement récurrent, offrant flexibilité et accès aux mises à jour.

*Remarque : Les licences par processeur, par VM et par utilisateur ont été supprimées au profit d'un modèle simplifié basé sur les cœurs et les abonnements. Les licences perpétuelles ont également été supprimées depuis le rachat par Broadcom*

---

## Modèles de licence
- **Licence par abonnement** : Paiement récurrent pour une utilisation continue, incluant support et mises à jour.
- **Licence perpétuelle** : Ce modèle a été supprimé en faveur des licences par abonnement depuis le 13 décembre 2023. Une décision de Broadcom qui a racheté VMware.
- **Licence d'évaluation** : Licence temporaire pour tester les produits VMware.

---

### Single Host ESXi
C'était une licence gratuite pour un seul hôte ESXi. Elle a été supprimée en 2023 par Broadcom. 

> J'utilisais cette licence dans mon HomeLab. Aujourd'hui je vous conseille de tester Proxmox si vous souhaitez monter un homelab.

---

## Différences avec les serveurs physiques
- **Licences par cœur** : Les licences VMware sont désormais basées sur le nombre de cœurs physiques, contrairement aux licences de serveurs physiques qui sont souvent basées sur le matériel.
- **Flexibilité** : Les licences VMware offrent plus de flexibilité pour ajuster les ressources en fonction des besoins.
- **Gestion centralisée** : Les licences VMware peuvent être gérées de manière centralisée, simplifiant la gestion par rapport aux licences de serveurs physiques.

---

## Problématique des licences d'autres fournisseurs à cause de la virtualisation - Exemple avec Oracle
**Oracle** est connu pour sa politique de licence stricte en matière de virtualisation. Voici quelques points à considérer lors de l'utilisation de produits Oracle avec VMware :

**Partitionnement souple vs. partitionnement rigide :** Oracle distingue entre le partitionnement souple (soft partitioning) et le partitionnement rigide (hard partitioning). Les technologies de partitionnement souple, comme VMware, ne sont pas reconnues par Oracle pour limiter la licence à une partie spécifique du matériel. Par conséquent, même si une machine virtuelle (VM) Oracle est confinée à un hôte particulier, Oracle peut exiger que tous les processeurs de l'ensemble du cluster soient licenciés.

---

## Problématique des licences d'autres fournisseurs à cause de la virtualisation - Exemple avec Oracle (suite)


**Mobilité des VM :** Avec des fonctionnalités comme vMotion de VMware, les VM peuvent migrer dynamiquement entre différents hôtes physiques. Oracle considère que, puisque les VM peuvent potentiellement s'exécuter sur n'importe quel hôte du cluster, tous ces hôtes doivent être couverts par des licences, augmentant ainsi le nombre total de licences requises.

---

## Conclusion
La gestion efficace des licences VMware mais également des licences des autres fournisseurs est essentielle pour garantir la conformité et optimiser les coûts. Comprendre les différents types de licences, les modèles de licence et les implications de la virtualisation sur les licences peut aider à éviter les problèmes et les coûts inutiles. 

Certains cas de précis comme les licences Oracle peuvent être particulièrement complexes et nécessitent une attention particulière pour éviter les pénalités et les coûts supplémentaires.

---

# Questions ?

---

## Sources
- [Broadcom VMware Licensing Changes Explained](https://redresscompliance.com/broadcom-vmware-licensing-and-subscription-changes-explained/)
- [Oracle Partitioning Policy](https://www.oracle.com/assets/partitioning-070609.pdf)
- [Broadcom Acquisition of VMware](https://www.broadcom.com/info/vmware)
- [7 costly oracle licensing pitfalls](https://xynomix.com/7-costly-oracle-licensing-pitfalls/)
- [Licensing Oracle software in VMware vCenter 6.0](https://www.softwareone.com/en/blog/articles/2020/12/01/oracle-licensing-in-vmware-vcenter-6-0)