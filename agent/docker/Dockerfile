FROM jetbrains/teamcity-agent

RUN apt-get update -y && apt-get install -y software-properties-common language-pack-en-base && \
    LC_ALL=en_US.UTF-8 add-apt-repository -y ppa:ondrej/php && \
    apt-get update -y && apt-get install -y \
    vim \
    mc \
    acl \
    npm \
    python-pycurl \
    php7.1 \
    php7.1-cli \
    php7.1-gd \
    php7.1-curl \
    php7.1-intl \
    php7.1-bcmath \
    php7.1-json \
    php7.1-mbstring \
    php7.1-mysql \
    php7.1-opcache \
    php7.1-readline \
    php7.1-soap \
    php7.1-sqlite3 \
    php7.1-xml \
    php7.1-xmlrpc \
    php7.1-zip \
    python-selinux && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

COPY php_config.ini /etc/php/7.1/mods-available/
RUN ln -s /etc/php/7.1/mods-available/php_config.ini /etc/php/7.1/apache2/conf.d/80-php_config.ini && \
    ln -s /etc/php/7.1/mods-available/php_config.ini /etc/php/7.1/cli/conf.d/80-php_config.ini
