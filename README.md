# reductor-satellite-cloud

Обучает сателлит выгружать реестр запрещённых сайтов от имени нескольких операторов.

**Примечание**: Автоматической генерации и подписи запросов, диагностики на предмет устаревания и невозможности выгрузки на текущий момент не предусмотрено.

Вам нужно:

Установить [Carbon Reductor Satellite](https://github.com/carbonsoft/reductor_satellite_installer)

Создать на нём папку:

```
mkdir /opt/rkn_cloud/
```

В ней создать папки для каждого из юридических лиц, например:

```
mkdir /opt/rkn_cloud/ooo_superprovider_1
mkdir /opt/rkn_cloud/ooo_superprovider_2
mkdir /opt/rkn_cloud/ooo_superprovider_3
```

В них поместить файлы запросов: `request.xml` и `request.xml.sign`

Положить [хук](/rkn_download.sh.hook) на место `/opt/reductor_satellite/userinfo/hooks/rkn_download.sh`
