environment:

- RAILS_ENV=production
- NEWRELIC_AGENT_ENABLED=false

- POSTGRES_USERNAME=danbooru
- POSTGRES_PASSWORD=foobarXYZ123
- POSTGRES_HOSTNAME=postgres
- POSTGRES_DATABASE=danbooru2

- SERVER_NAME=docker.lan

- DANBOORU_MEMCACHED_SERVERS=memcached:11211

- SECRET_TOKEN=${SECRET_TOKEN}
- SESSION_SECRET_KEY=${SESSION_SECRET_KEY}

- DANBOORU_PASSWORD_SALT=${DANBOORU_PASSWORD_SALT}
- DANBOORU_EMAIL_KEY=${DANBOORU_EMAIL_KEY}

- RECAPTCHA_SITE_KEY=${RECAPTCHA_SITE_KEY}
- RECAPTCHA_SECRET_KEY=${RECAPTCHA_SECRET_KEY}


volumes:
- danbooru-data:/var/www/danbooru2/shared/public/data
- config/danbooru_local_config.rb:/var/www/danbooru2/shared/config/danbooru_local_config.rb:ro