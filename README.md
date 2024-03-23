# STELLAR_BUKKIT_DOC
Documentazione, non corso, di Bukkit | by StellarSquad

![637538649057112996](https://github.com/Tyranzx/STELLAR_BUKKIT_DOC/assets/70720366/4b01f9bc-80ab-46cf-a7f6-4db1813e9cd0)

# BUKKIT
## Cos'é?
### Non solo é un motore per creare un nostro server di minecraft ma é pure un mezzo per creare complementi da aggiungere nel nostro server. Evidentemente "Bukkit" non é piú usato peró si parte sempre da lí e la struttura generale é identica al resto di API.

## Cosa si imparerá a fare?
### Sicuramente non modalitá intere, ma il sufficiente perché da soli possiate farlo con sforzo e concentrazione.
### Un esempio bruto di modalitá che non potremo insegnare sono KitPVP e Bedwars, perché entrambi usano tecnologie non solo **Spigot** e **Java** ma pure altre tecnologie e possibilmente altri linguaggi di programmazione.
### 
### In conclusione, servirá per aprire la mente e togliere alcuni dubbi a alcune persone che stanno imparando.
### Utilizzeremo Eclipse per gli esempi e/o esempi scritti per MD (Gli stessi avuti nella doc precendente di java)
###
## [👋] Il nostro primo "Hello world" in Bukkit
### Per la creazione della classe principale, ovvero la classe la quale il contenuto sará eseguito per primo, dobbiamo estendere "JavaPlugin".
### É importante ricordarsi che si puó solo estendere una volta sola "JavaPlugin", questo perché la classe (JavaPlugin) ha metodi specifici per far diventare una classe quella "principale".
```java
public class Loader extends JavaPlugin {
	
	public void onEnable() {
		Bukkit.broadcastMessage("Hello world!");
	}
	
	public void onDisable() {
		Bukkit.broadcastMessage("Bye world!");
	}
```
![Screenshot 2024-03-23 113937](https://github.com/Tyranzx/STELLAR_BUKKIT_DOC/assets/70720366/ab9977c8-c4a0-4885-a677-8aa4f839b240)
### Ricordiamoci che son solo due metodi da mettere, rispettando le maiuscole, perché il nostro plugin funzioni come noi vogliamo.
### Unicamente "onEnable" é importante per registrare comandi, mandare messaggi, registrare classi o eseguire azioni e/o istruzioni preparate con certe scopi.
### Nel metodo "onDisable" metteremo le cose che ci serviranno eseguire per quando il server, per esempio, si stia chiudendo.
