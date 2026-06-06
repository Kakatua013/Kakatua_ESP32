# Kakatua_ESP32

Firmware do ESP32 para controle da tranca e sensor ultrassônico do bicicletário Kakatua Bikes.

## Como funciona

O ESP32 lê o sensor ultrassônico a cada 100ms. Se detectar um objeto a ≤ 10cm, considera a vaga ocupada e notifica a API. Caso contrário, libera a vaga.

## Bibliotecas necessárias (Arduino IDE)

- `WiFi.h`
- `HTTPClient.h`
- `ArduinoJson.h`

## Configuração

Antes de gravar, edite as constantes no início do arquivo `kakatua_tranca.ino`:

```cpp
const char* ssid     = "NOME_DA_REDE";
const char* password = "SENHA_DA_REDE";
const char* apiKey   = "SUA_API_KEY";
```

Todas as dependências estão listadas em `requirements.txt`.
