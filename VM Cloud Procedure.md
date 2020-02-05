---


---

<h1 id="exporter-une-vm-d’un-esxi-vers-openstack"><strong>Exporter une VM d’un ESXi vers OpenStack</strong></h1>
<p><strong>Prérequis :</strong></p>
<p>Un système Open Stack fonctionnel<br>
OVFTool installé</p>
<h2 id="ère-étape-"><strong>1ère étape :</strong></h2>
<p>Se rendre dans le dossier d’OVFTool :</p>
<p>C:\Program Files\VMware\VMware OVF Tool</p>
<p>Ouvrir un terminal puis exécuter la commande suivante :</p>
<blockquote>
<p><strong>ovftool.exe --noSSLVerify --allowExtraConfig vi://user:password@147.135.255.164/vm  destination/nom.vmdk</strong></p>
</blockquote>
<p>Remplacer <em>user</em> et password par les logins de votre ESXi, vm par le nom de la vm que vous voulez exporter de l’ESXi et remplacer destination par le lieu ou vous souhaitez enregistrer votre vm par exemple : c:\vm\ et nom par le nom que vous souhaitez lui donner</p>
<h2 id="explications-de-la-commande-">Explications de la commande :</h2>
<ul>
<li>
<p>ovftool.exe : Exécute OVFTOOL</p>
</li>
<li>
<p>–noSSLVerify : Ne vérifie pas si les certificats sont outdated ou pas</p>
</li>
<li>
<p>–allowExtraConfig : Prend en compte toute les configurations / paramètres de la VM</p>
</li>
<li>
<p>vi:// : permet de définir sur quelle machine nous allons nous connecter</p>
</li>
<li>
<p>@IP : indique sur quelle IP nous allons nous connecter</p>
</li>
</ul>
<p>Ici j’utilise le format VMDK, mais nous pouvons aussi très bien utiliser le format ISO, OVA, ou autres, pour plus d’informations rendez-vous sur le site officiel de VMware sur <a href="https://bit.ly/395PWxe">la page d’OVFTool</a></p>
