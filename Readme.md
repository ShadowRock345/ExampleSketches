# Beispiel-Skripte
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

Die Custom Callback-Method muss immer wie folgt aussehen (der Name ist dabei nicht weiter wichtig):
```cpp
void customCallback(char* topic, byte* payload, unsigned int length) {
  //custom callback 
}

....

//und so registriert werden:

void setup() {
  mqttManager.setCallback(customCallback);
}
```

## Lizenz

Diese Bibliothek ist unter der MIT-Lizenz lizenziert. 


 * MQTTManager - Bibliothek zur Verwaltung von MQTT-Verbindungen
 * Erstellt von [P_Seminar], [17.04.2024]
 * Copyright (c) [2024] [P_Seminar]
 * Freigegeben unter der MIT-Lizenz. All rights reserved.

## Hilfe und Unterstützung

Bei Fragen oder Problemen können Sie ein Issue im entsprechenden GitHub-Repository erstellen.
