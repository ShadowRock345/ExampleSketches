# Beispiel-Skripte für MQTT Verbindungen

## Voraussetzungen

1. Funktionsfähige Arduino-IDE
2. MQTT-Broker
3. Installierte MQTTManager Bibliothek. [Anleitung](https://github.com/ShadowRock345/MQTTManager/)

##

<ins>Die Beispiele sind auch verfügbar unter</ins>:  Arduino-IDE -> File/Datei -> Examples/Beispiele -> MQTTManager

##

## Beispiel-Skript mit NeoPixel-Streifen

Dieses Beispiel zeigt die Verwendung der MQTTManager-Bibliothek in Verbindung mit einem NeoPixel-Streifen für Beleuchtungseffekte. Online abrufen: [hier](https://create.arduino.cc/editor/jonasworthofbeeinghere/dc94994d-9c2e-44bc-b27d-ab76443003c1/preview)

```cpp
Example_Sketch_with_strip.zip

Example_Sketch_with_strip.ino
```

## Beispiel-Skript ohne NeoPixel-Streifen

Dieses Beispiel demonstriert die Verwendung der MQTTManager-Bibliothek ohne zusätzliche Funktionalität für den NeoPixel-Streifen. Online abrufen: [hier](https://create.arduino.cc/editor/jonasworthofbeeinghere/268b3efa-8f0b-42e2-9052-97f0c09e9f17/preview)

```cpp
Example_Sketch_without_strip.zip

Example_Sketch_without_strip.ino
```

## Beispiel-Skript mit benutzerdefiniertem Callback

Dieses Beispiel zeigt die Verwendung eines benutzerdefinierten Callbacks für die Verarbeitung eingehender MQTT-Nachrichten. Online abrufen: [hier](https://create.arduino.cc/editor/jonasworthofbeeinghere/24f62ede-c5ff-4e62-a0d0-8d07cbcac979/preview)

```cpp
Example_Sketch_with_custom_callback.zip

Example_Sketch_with_custom_callback.ino
```

Die Custom Callback-Method muss dabei immer wie folgt aussehen (der Name ist dabei nicht weiter wichtig):
```cpp
void customCallback(char* topic, byte* payload, unsigned int length) {
  //custom callback 
}

....

//und so registriert werden:

void setup() {
  ....
  mqttManager.setCallback(customCallback);
  ....
}
```

## Code-Erklärung

  * **Bibliotheken**: Die erforderlichen Bibliotheken werden eingebunden. 
    
  * **Variableninitialisierung**: Die erforderlichen Variablen für das Wi-Fi-Netzwerk (ssid, password), den MQTT-Broker (mqtt_broker, mqtt_username, mqtt_password, mqtt_port), das Thema (topic), den Gerätenamen (name) und den Debug-Modus (debug, wenn der debug Modus aktiviert ist, prüft die Bibliothek zusätzlich die Version der Bibliothek) werden initialisiert.

  * **MQTTManager-Objekt**: Ein Objekt der Klasse MQTTManager wird erstellt und mit den initialisierten Variablen konfiguriert.

  * **Setup**: Die setup()-Funktion initialisiert die serielle Kommunikation und verbindet das MQTT-Manager-Objekt mit dem Broker. .

  * **Loop**: Die loop()-Funktion wird kontinuierlich ausgeführt. Sie ruft die loop()-Methode des MQTT-Manager-Objekts auf, um eingehende Nachrichten zu verarbeiten und um die Verbindung zum Broker aufrecht zu erhalten, und die loop()-Funktion sendet eine Testnachricht an das Thema "test".

  * Je nach Sketch, wird noch die Neopixel Bibliothek benutzt oder ein Custom Callback definiert, der dabei hilft, wie Nachrichten, die eingehen, zu verarbeiten. (Da die Bibliothek eingehende Nachrichten einfach nur printet)

## Lizenz

Diese Beispiele sind unter der MIT-Lizenz lizenziert. 


 * MQTTManager - Bibliothek zur Verwaltung von MQTT-Verbindungen
 * Erstellt von [P_Seminar], [17.04.2024]
 * Copyright (c) [2024] [P_Seminar]
 * Freigegeben unter der MIT-Lizenz. All rights reserved.

## Hilfe und Unterstützung

Bei Fragen oder Problemen können Sie ein Issue im entsprechenden GitHub-Repository erstellen.
