# Обновление LineageOS на Samsung Galaxy Tab S5e

Имеем:

- Установленный LineageOS 20
- Установленный Magisk
- Скомпилированный [форк](https://github.com/luk1337/Heimdall/) Heimdall (у оригинала проблемы с этим прибором) 

## Шаги

1. [Качаем новую версию LineageOS и recovery.img](https://download.lineageos.org/devices/gts4lvwifi/builds)
2. Стартуем в recovery (volume up + power) и загоняем новую версию LineageOS    

    `adb -d sideload  ~/Downloads/lineage-20.0-20231206-nightly-gts4lvwifi-signed.zip`

3. Прибор перезапускается, Magisk слетел.
3. Переносим на прибор recovery.img и патчим с помощю Magisk
4. Патченый recovery.img переносим на ПК
5. Перезапускаем прибор в fastboot (volume up + volume down + power)
6. Загоняем патченый recovery.img

    `./heimdall flash --RECOVERY ~/Downloads/magisk_patched-26400_vvbXP.img `

7. Перезапускаем прибор в Magisk (volume up + power --> splash screen --> отпускаем кнопки)
8. Запускаем Magisk 