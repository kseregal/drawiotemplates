# drawiotemplates

Клиентские библиотеки инструментов для drawio.
Библиотека - набор фигур для использования в диаграмме. Очень много наборов поставляется
из коробки. Но нашему клиенту нужны свои наборы.

Для этого требуется чтобы клиент предоставил набор в виде vss файла. 
Нужно преобразовать этот файлв в xml. Для этого в облачной версии https://app.diagrams.net/ создаем
новую пустую диаграмму. Далее Файл - Импортировать из - Это устройство. 
Выбираем vss файл и появляется нобор слева на боковой панели с именем файла.
Затем нажимаем карандаш на этом наборе (рядом с названием в шапке набора).
В открывшемся диалоге выбираем **Экспортировать** - **Это устройство**.
Сохраняем полученный xml файл.
Затем кладем в репозиторий, комитим, пушим на github.
Идем в интерфейс github. Открываем нужный xml как raw файл и копируем ссылку.
Пример ссылки
```shell
https://raw.githubusercontent.com/kseregal/drawiotemplates/main/tpl_vo.vss.xml
```
Далее это адрес можно использовать в ссылке открытия drawio. Только в кодированном для 
адресной строки виде.

Можно прогнать через инструмент.

https://jgraph.github.io/drawio-tools/tools/convert.html

Можно сделать непосредственно в приложении.

Пример uri для встройки draw.io в интерфейс.

http://localhost:8080/?splash=0&lang=en&embed=1&ui=atlas&spin=1&proto=json&saveAndExit=1&noSaveBtn=0&libraries=1&clibs=Uhttps%3A%2F%2Fraw.githubusercontent.com%2Fkseregal%2Fdrawiotemplates%2Fmain%2Fshablov_vo.xml

Документация по этому рецепту

https://github.com/jgraph/drawio-libs

На всякий случай дублирую важное здесь.

# Create and share custom libraries:
1. Use the scratchpad or create a new library by clicking File, New Library
2. Once the library appears in the sidebar, you can drag and drop cells and images from the diagram or your harddrive
3. Supported image formats are PNG, JPG, SVG and GIF (including animated GIFs). If you are adding SVG files, you can make the colors of the SVG configurable using this method: https://desk.draw.io/support/solutions/articles/16000079239
4. When all elements have been added, click the pen icon, add titles to the entries and click Export
5. This will download the library file to your computer
6. To share it, the file must be uploaded to the web and made available via a public URL. One way to do this is to upload it to a public GitHub repository.
7. If you are using GitHub, use the RAW URL of the library which is of the form https://raw.githubusercontent.com/ORG/REPO/REF/PATH/FILENAME.xml, eg. https://raw.githubusercontent.com/jgraph/drawio-libs/master/libs/templates.xml
8. Once you have the URL of the library, you can share it by encoding the URL and adding it the clibs parameter. To encode the URL, paste it into the text box at https://jgraph.github.io/drawio-tools/tools/convert.html and click URL Encode. For our example, this will yield https%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Ftemplates.xml
9. Then add this to https://app.diagrams.net/?splash=0&clibs=U, eg. https://app.diagrams.net/?splash=0&clibs=Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Ftemplates.xml (where splash=0 bypasses the splash screen). Multiple libraries can be specified by separating them with semicolons. Each value must be prefixed with a U if it's a URL, eg. https://app.diagrams.net/?splash=0&clibs=Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fun-ocha-icons-bluebox.xml;Uhttps%3A%2F%2Fjgraph.github.io%2Fdrawio-libs%2Flibs%2Fun-ocha-icons.xml
10. You can then share this link and clicking on it will open and install your custom libraries in draw.io

Также полезная статья https://desk.draw.io/support/solutions/articles/16000067790