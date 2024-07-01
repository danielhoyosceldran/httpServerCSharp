No hauria de fer falta, però potser cal habilitat una regla al firewall per acceptar TCP al port 8081
URL:
	http://<pc_IP>:8081

========================================================================================================
Per a cambiar el tipus d'autenticació, modificar la línia 42:

Amb autenticació basic:	_listener.BeginGetContext(new AsyncCallback(ListenerCallback_BasicAuth), _listener);
Sense autenticació:		_listener.BeginGetContext(new AsyncCallback(ListenerCallback_NoAuth), _listener);

========================================================================================================
Si no funciona:

Si no funciona, reincia el servidor. És possible que no s'hagi iniciat bé.
Si segueix sense funcionar pot ser que el port estigui bloquejat, o no accepti peticions.