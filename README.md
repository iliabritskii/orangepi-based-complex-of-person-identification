Программы в данном репозитории предназначены для настройки программно-аппаратного комплекса идентификации персоны на базе микрокомпьютера.

Для создания программно-аппаратного комплекса необходимо наличие микрокомпьютера и видеокамеры.  Рекомендовано использовать Linux в качестве операционной системы для программно-аппаратного комплекса.

Алгоритм работы программно-аппаратного комплекса:

•	Выделение и сохранение в очередь на обработку кадров из видеопотока, на которых присутствует человек.

•	Обработка сохраненных фотографий, вычисление значений для векторов по точкам на лице человека.

•	Проверка на наличие человека в базе данных.

•	Запись времени появления человека в отчет, в случае успешной идентификации, и удаление фотографии. 

•	Перемещение фотографии и дальнейшее ее прикрепление к отчету, в случае, если человек не был опознан.

•	Отправка отчета на электронную почту в выбранное при настройке программно-аппаратного комплекса время.

Некоторые программы при работе запускают друг друга, поэтому необходимо указать пути до файлов в коде программ в соответствие с размещением программ в вашей директории. 

Описание программ:

• add_new_people.ру - занесение нового человека в базу, запускается из GUI_new_people.

• change_crontab.py - изменяет время отправки отчета на почту (запускается из GUI_login_agmin).

• create_dataset.py - создает пустой файл в нужном формате для занесения датасетов (запускается при удаление всех данных из базы).

• dataset – файл с эталонными данными для сравнения.

• faces_recognition.ру - обработка сохраненной фотографии и распознавание человека.

• GUI_login_admin.ру - GUI для регистрации email и времени получения отчетов (создает mail.txt и time.txt).

• GUI_new_people.ру - GUI для добавления новых людей в базу данных.

• GUI_remove_dataset.py - GUI для удаления базы данных.

• images_checker.sh – проверка на наличие фотографий, добавленных в очередь на обработку (необходимо автоматизировать запуск через Cron или другой планировщик задач).

• mail.txt – текстовый файл, в котором хранится почта для отправки отчетов. 

• people_recognition.ру - распознавание появления человека в кадре, делает фото (работает в фоне постоянно, необходимо поставить в автозапуск через Cron или другой планировщик задач).

• remove.ру - удаляет отправленные отчеты и фото неопознанных людей.

• report.xlsx, report.csv – файлы с отчетом.

• send_report.ру - отправка отчетов и фото на почту

• table_creator.ру - создает файлы для отчетов после их удаления (отправки) (создает report.xlsx и report.csv)

• time.txt – текстовый файл, в котором хранится выбранное время отправки отчетов.

• writer.ру - заносит данные о опознанном человеке в отчет

• white.jpg – используется для добавления белого фона для надписи на фотографиях с неопознанными людьми.

• GUI_login_admin.desktop, GUI_new_people.desktop, GUI_remove_dataset.desktop – ярлыки для запуска программ с графическим интерфейсом.
