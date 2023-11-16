# Home Assistant Add-on: Zigbee2MQTT-1

<div align="center">
    <div style="display: flex;">
        <a href="https://github.com/zigbee2mqtt/hassio-zigbee2mqtt/actions?query=workflow%3ACI">
            <img src="https://github.com/zigbee2mqtt/hassio-zigbee2mqtt/workflows/CI/badge.svg">
        </a>
        <a href="https://github.com/zigbee2mqtt/hassio-zigbee2mqtt/releases">
            <img src="https://img.shields.io/github/release/zigbee2mqtt/hassio-zigbee2mqtt.svg">
        </a>
        <a href="https://github.com/zigbee2mqtt/hassio-zigbee2mqtt/stargazers">
            <img src="https://img.shields.io/github/stars/zigbee2mqtt/hassio-zigbee2mqtt.svg">
        </a>
        <a href="https://discord.gg/dadfWYE">
            <img src="https://img.shields.io/discord/556563650429583360.svg">
        </a>
        <a href="http://zigbee2mqtt.discourse.group/">
            <img src="https://img.shields.io/discourse/https/zigbee2mqtt.discourse.group/status.svg">
        </a>
    </div>
    <p>
<a href="https://esp32.gpio.club:880/">藏机官网（ipv6）</a> <a href="http://esp32.518126.xyz:880/">藏机官网（ipv4）</a> 点击跳转。</p>
</div>

MQTT:
```shell
mqtt:
  base_topic: zigbee2mqtt1
  #base_topic多加一个1 区分多开主题
  server: mqtt://localhost:1883
  #mqtt在Home Assistantaz 安装，localhost是Home Assistantaz的ip,端口1883
  user: mqtt
  password: mqtt
  client_id: zigbee2mqtt1
  #client_id多加一个1 区分多开mqtt客户端id
```

serial:
```shell
serial:
  adapter: ezsp
  port: tcp://[Gateway_IP]:[Port]
  #多模和企业版端口8888 多模自动版端口6638
  #多模自动版域名: port: tcp://tube-zb-gw-efr32-xxxxxx.local:6638
```

channel:
```shell
advanced:
  channel: 15
  #信道要分开 防止干扰 选15 20 25
  #z2m网页UI设置步骤z2m设置→高级→ZigBee channel
```
