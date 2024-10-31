# Домашнее задание к занятию "`Защита хоста`" - `Ли Олег`


### Инструкция по выполнению домашнего задания

   1. Сделайте `fork` данного репозитория к себе в Github и переименуйте его по названию или номеру занятия, например, https://github.com/имя-вашего-репозитория/git-hw или  https://github.com/имя-вашего-репозитория/7-1-ansible-hw).
   2. Выполните клонирование данного репозитория к себе на ПК с помощью команды `git clone`.
   3. Выполните домашнее задание и заполните у себя локально этот файл README.md:
      - впишите вверху название занятия и вашу фамилию и имя
      - в каждом задании добавьте решение в требуемом виде (текст/код/скриншоты/ссылка)
      - для корректного добавления скриншотов воспользуйтесь [инструкцией "Как вставить скриншот в шаблон с решением](https://github.com/netology-code/sys-pattern-homework/blob/main/screen-instruction.md)
      - при оформлении используйте возможности языка разметки md (коротко об этом можно посмотреть в [инструкции  по MarkDown](https://github.com/netology-code/sys-pattern-homework/blob/main/md-instruction.md))
   4. После завершения работы над домашним заданием сделайте коммит (`git commit -m "comment"`) и отправьте его на Github (`git push origin`);
   5. Для проверки домашнего задания преподавателем в личном кабинете прикрепите и отправьте ссылку на решение в виде md-файла в вашем Github.
   6. Любые вопросы по выполнению заданий спрашивайте в чате учебной группы и/или в разделе “Вопросы по заданию” в личном кабинете.
   
Желаем успехов в выполнении домашнего задания!
   
### Дополнительные материалы, которые могут быть полезны для выполнения задания

1. [Руководство по оформлению Markdown файлов](https://gist.github.com/Jekins/2bf2d0638163f1294637#Code)

---

### Задание 1

```

"attributes": {
            "bcrypt_hash": "$2a$10$10dkHz5bmmPG8wes/IeL6uan8ejGkTnhJkb0ZU4mc.5Pm8HSg7j3y",
            "id": "none",
            "keepers": null,
            "length": 16,
            "lower": true,
            "min_lower": 1,
            "min_numeric": 1,
            "min_special": 0,
            "min_upper": 1,
            "number": true,
            "numeric": true,
            "override_special": null,
            "result": "b5l31iDlED6wbRrB",
            "special": false,
            "upper": true
          },
```
4. Отсутствует тип ресурса на 24 строке, не верное имя, должно начинваться с цифры, в ресурсе docker_container не верно заданно имя
![image](https://github.com/user-attachments/assets/d4dd8fc2-2953-4d4e-b355-6a4f13472f97)





```
resource "docker_image" "nginx" {
  name         = "nginx:latest"
  keep_locally = true
}

resource "docker_container" "nginx1" {
  image = docker_image.nginx.image_id
  name  = random_password.random_string.result

  ports {
    internal = 80
    external = 9090
  }
}
```
Данный ключ пропускает план, а это может привести к ошибкам, потому что код не проверенный
![image](https://github.com/user-attachments/assets/5d75a291-0ef0-47ae-be41-c131fa68fb96)

```
{
  "version": 4,
  "terraform_version": "1.8.4",
  "serial": 11,
  "lineage": "65c1f51e-beba-db8d-7d4e-83c10689ebbb",
  "outputs": {},
  "resources": [],
  "check_results": null
}
```






