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

# 2.3 Driver

1. Écrivez un driver pour piloter les LED. Utilisez une structure.
2. Écrivez une fonction shell permettant d’allumer ou d’éteindre n’importe
quelle LED.

# 3 Le CODEC Audio SGTL5000
# 3.1 Configuration préalables

1. Quelles pins sont utilisées pour l’I2C ? 
Réponse :
Les pins utilisés pour l'I2C sont :
-SCL (Serial Clock Line) : ligne d'horloge
-SDA (Serial Data Line) : ligne de données

À quel I2C cela correspond dans le STM32 ?
Réponse :
I2C_SLC ==> PB10
I2C_SDA ==> PB11

2. Activons l’I2C correspondant, laissez la configuration par défaut.

3. Activez l’I2C correspondant, laissez la configuration par défaut.

4. Configurez le SAI2 :
— SAI A : Master with Master Clock Out,
— Cochez I2S/PCM protocol,
— SAI B : Synchronous Slave,
— Cochez I2S/PCM protocol.

# 3.2 Configuration du CODEC par l’I2C

1. À l’aide d’un oscilloscope, vérifiez la présence d’une horloge sur le signal
MCLK.

2. À l’aide de la fonction HAL_I2C_Mem_Read(), récupérez la valeur du registre
CHIP_ID (addresse 0x0000). L’adresse I2C du CODEC est 0x14.














































