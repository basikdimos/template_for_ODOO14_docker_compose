# template_for_ODOO14_docker_compose
Шаблон контейнеров docker для ODOO14

Склонировать репозиторий
Перейти в каталог проекта и запустить docker-compose
	docker-compose up -d
Дождать скачивания и запуска контейнеров
	docker ps

# Config IDE
Настравиваем PyCharm
Открыть каталог как проект в PyCharm Pro
Далее 
	File-Settings-Project:<name>-Python Interpreter
	Config-Add...-"+"
	Docker Compose
		Server-New-все по умолчанию OK
		Service: web
		Python: python3.7 (заходим в контейнер ODOO и проверяем версию python)
		OK
	Path mappings:
		<Project root>/addons→/mnt/extra-addons; <Project root>/config→/etc/odoo
	OK

Далее debug-mode
	Run-Edit Configuration-"+"-Python
		Name: name
		Script path:	/usr/bin/odoo
		Parameters:	--config /etc/odoo/odoo.conf
		Path mappings:	 <Project root>/addons→/mnt/extra-addons; <Project root>/config→/etc/odoo
	OK

всё. Доставляем плагины и начинаем разрабатывать
	
		
