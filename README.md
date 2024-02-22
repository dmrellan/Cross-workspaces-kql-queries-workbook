# Cross-workspaces-kql-queries-workbook
Cross-workspace KQL queries workbook

AIDA
A
Alguna vez te has encontrado en la necesidad de ejecutar una query KQL contra muchos o todos tus Log Analytics workspaces?

I
Probablemente ya sabrás que esto lo se llaman cross-queries (https://learn.microsoft.com/en-us/azure/azure-monitor/logs/cross-workspace-query) y podrás ejecutarlas directamente teniendo esto en mente a la hora de escribir la query contemplándolo en la sintaxis o, incluso, utilizando el propio portal de Azure modificando el scope de la query. Son soluciones perfectamente válidas y eficaces, pero no siempre las más eficientes ya que la primera obliga a complicar un poco la query añadiendo líneas para atacar a cada workspace y unificar los resultados y la segunda se vuelve poco útil cuando el número de workspaces es muy alto (debido a la necesidad de seleccionar uno a uno los workspaces). Pero hay una tercera opción, utilizar Azure Workbooks, y esta es en la que me quiero enfocar.

D
Hoy vengo aquí a compartir contigo un Azure workbook sencillo pero que te ahorrará mucho tiempo si necesitas hacer esta tarea varias veces. Como puedes ver más abajo se trata de un workbook con tres parámetros típicos (suscripciones, workspaces y time range) y un cuarto en el que tendremos que escribir una KQL query. El resultado en la tabla a continuación será el de ejecutar dicha query contra todos los log analytics seleccionados (cross-workspace query) unificando los resultados. De esta forma sólo necesitarás consultar la tabla o exportarla a excel para tratar los resultados.

A
Como siempre, el código workbook lo encontrarás en este mismo artículo en la carpeta materiales. Disfrútalo!
NOTA: Recuerda que el límite máximo de workspaces para una kql query son 100 en cada ejecución. Por lo que si tienes más de 100 workspaces (https://learn.microsoft.com/en-us/azure/azure-monitor/logs/cross-workspace-query#limitations)deberás hacer varias ejecuciones. 
Cualquier feedback al respecto será bienvenido.
