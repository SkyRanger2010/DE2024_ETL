# Используем официальный образ Apache NiFi в качестве базового
FROM apache/nifi:latest

# Указываем рабочую директорию
WORKDIR /opt/nifi/nifi-current

# Копируем пользовательские конфигурации (если есть) в папку конфигурации NiFi
# Убедитесь, что файлы конфигурации находятся в той же директории, что и Dockerfile
COPY ./conf/ ./conf/

# Настраиваем переменные среды для логина и пароля (можно переопределить во время запуска контейнера)
ENV SINGLE_USER_CREDENTIALS_USERNAME=admin
ENV SINGLE_USER_CREDENTIALS_PASSWORD=admin_password

# Указываем команду по умолчанию для запуска NiFi
CMD ["bin/nifi.sh", "run"]
