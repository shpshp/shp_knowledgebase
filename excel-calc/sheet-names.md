Some examples of using sheet names in formulas
==============================================

```excel
=ДВССЫЛ("'2018'!A1")

=ЗНАЧ(ПРАВ(ЯЧЕЙКА("filename");ДЛСТР(ЯЧЕЙКА("filename"))-НАЙТИ("$";ЯЧЕЙКА("filename"))))

=ЯЧЕЙКА("filename")

=ТЕКСТ(ЗНАЧ(ПРАВ(ЯЧЕЙКА("filename");ДЛСТР(ЯЧЕЙКА("filename"))-НАЙТИ("$";ЯЧЕЙКА("filename"))))-1;"0")

=ДВССЫЛ("'"&ТЕКСТ(ЗНАЧ(ПРАВ(ЯЧЕЙКА("filename");ДЛСТР(ЯЧЕЙКА("filename"))-НАЙТИ("$";ЯЧЕЙКА("filename"))))-1;"0")&"'!A1")
```

[Read more on the installation.](https://tecadmin.net/install-docker-on-ubuntu/)
