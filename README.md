# Автоматический ИИ-обработчик заявок на клееный брус

Проект автоматизирует обработку входящих писем от клиентов с помощью локальной LLM и n8n.

## Как это работает:
1. n8n получает письмо по IMAP.
2. Текст письма очищается от HTML-тегов.
3. Двухэтапная обработка ИИ (LM Studio / Gemma 4B): "Аналитик" выделяет параметры, "Форматировщик" упаковывает их в строгий JSON.
4. Данные превращаются в HTML-таблицу.
5. Клиенту отправляется ответной письмо с таблицей и уточняющими вопросами.

## Стек
* n8n (Docker)
* LM Studio (локальная модель Gemma 4 E2B)
* JavaScript (обработка данных в n8n)
* IMAP/SMTP

## Файлы
* `workflow.json` — готовый к импорту процесс n8n.
* `docker-compose.yml` — конфигурация для запуска n8n и внешнего Python-раннера.

## Скриншоты
<img width="943" height="266" alt="image" src="https://github.com/user-attachments/assets/589a7902-aa21-4ee4-ac5a-bbeae25f7c2f" />
<img width="900" height="235" alt="image" src="https://github.com/user-attachments/assets/470a5d19-7d62-45ef-ab7b-bfa548b5bf3b" />
