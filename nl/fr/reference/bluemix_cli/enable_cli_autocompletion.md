---



copyright:

  years: 2018
lastupdated: "2018-07-13"

---

{:codeblock: .codeblock} 
{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:tip: .tip}

# Activation de l'exécution automatique de shell pour l'interface CLI {{site.data.keyword.Bluemix_notm}} (Linux/MacOS uniquement)

Depuis la version `0.7.0`, les programmes d'installation de l'interface CLI {{site.data.keyword.Bluemix_notm}} n'activent pas automatiquement l'exécution automatique de shell. Pour pouvoir bénéficier de cette fonction, vous devez l'activer manuellement. Les scripts d'exécution automatique sont installés aux emplacements suivants :

* Exécution automatique de `Bash` : `/usr/local/ibmcloud/bx/bash_autocomplete`
* Exécution automatique de `Zsh` : `/usr/local/ibmcloud/bx/zsh_autocomplete`

## Activation de l'exécution automatique pour Linux

* Si vous utilisez `Bash`, ajoutez 

`source /usr/local/ibmcloud/bx/bash_autocomplete` dans un des fichiers suivants. 

  * Pour un shell de connexion : `~/.bash_profile`
  * Pour les autres types de shell : `~/.bash_rc`
  
* Si vous utilisez `Zsh`, ajoutez : 

`source /usr/local/ibmcloud/bx/zsh_autocomplete` dans `~/.zshrc`.

## Activation du support d'exécution automatique pour MacOS

* Si vous utilisez `Bash`, ajoutez : 

`source /usr/local/ibmcloud/bx/bash_autocomplete` dans `~/.bash_profile`.
* Si vous utilisez `Zsh`, ajoutez : 

`source /usr/local/ibmcloud/bx/zsh_autocomplete` dans `~/.zshrc`.
