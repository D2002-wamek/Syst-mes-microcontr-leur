# Systèmes à microcontrôleur

# COMPTE RENDU TP Systèmes à microcontrôleur
# DJEUNGA Daniela & KITSOUKOU Debora
# 3DN_TP2

# 1 Démarrage
1. Créons un projet pour la carte NUCLEO_L476RG. Initialisons les périphériques
avec leur mode par défaut sans activer la BSP.

2. Testons la LED LD2
Voir image Code pour tester LD2

3. Testons l’USART2 connecté à la STLink interne. (Valider par le prof).
   
# 2 Le GPIO Expander et le VU-Metre

# 2.1 Configuration
1. Quelle est la référence du GPIO Expander ? 
Réponse : La référence du GPIO Expander est MCP23S17: 16-Bit I/O Expander with SPI Interface (Voir Page 39 de la DATASHEET_20001952c).
Téléchargeons sa datasheet.

2. Sur le STM32, quel SPI est utilisé ?
Réponse : Dans notre code, aucune instance SPI n'est initialisée.
Cela veut dire que le SPI n'est pas utilisé pour l'instant dans notre programme.

3. Quels sont les paramètres à configurer dans STM32CubeIDE ?
Réponse :
-Pinout & Configuration : nous avons activé le SPI2
-SPI2 Mode and Configuration : Mode (Full-Duplex Master)
-Basic Parameters : mettre le Data Size 8 bits (voir page 12).
Nous avons mis sur 8 bits car nous voulons uniquement utiliser le PORT A. 

5. Configurons-les.
Voir image Configuration SPI.

# 2.2 Tests
1. Faisons clignoter une ou plusieurs LED.
2. Pour toutes les tester, vous pouvez faire un chenillard (par exemple).




