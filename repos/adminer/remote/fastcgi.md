## `adminer:fastcgi`

```console
$ docker pull adminer@sha256:0c4d608bed13ff6f35601a436851efca63c1f6afb329e31eca42856795c6be60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `adminer:fastcgi` - linux; amd64

```console
$ docker pull adminer@sha256:8dacfdd34d8f2ee88811c2155758af23008579f788e467533ef0952c6f0acadc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95983351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d3dd2de505d7752d3c1eaf46298e94753d3447a5423aacb66c4856862e20a8`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 13 Jun 2024 01:21:05 GMT
ADD file:d2a2ac890c4f902560feaadaac9f36a9b844131c97453ecb90241cf525185196 in / 
# Thu, 13 Jun 2024 01:21:06 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:37:42 GMT
STOPSIGNAL SIGINT
# Thu, 13 Jun 2024 03:38:04 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 03:38:05 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 13 Jun 2024 03:38:24 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 13 Jun 2024 03:38:25 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 13 Jun 2024 03:38:25 GMT
WORKDIR /var/www/html
# Thu, 13 Jun 2024 03:38:25 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 13 Jun 2024 03:38:25 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 13 Jun 2024 03:38:25 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 13 Jun 2024 03:38:25 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 13 Jun 2024 03:38:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 13 Jun 2024 03:38:36 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 13 Jun 2024 03:38:37 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 13 Jun 2024 03:38:37 GMT
USER adminer
# Thu, 13 Jun 2024 03:38:37 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:29f873e2e3f8f1b35ae4bee023807e71b6e16e714dbd1cbd19b3124c62e7634c`  
		Last Modified: Thu, 13 Jun 2024 01:25:49 GMT  
		Size: 55.1 MB (55099190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e07974af910654bca759ee27f65bb302be21b6a79fa67c5daf0a5e6c7e4de3`  
		Last Modified: Thu, 13 Jun 2024 03:38:56 GMT  
		Size: 39.5 MB (39491055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4bf202c95f39951ed1d92c95afaf550dcba3af9ae246eaf2d12ae86b190449`  
		Last Modified: Thu, 13 Jun 2024 03:38:49 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fe90b7fe507ed5eb8b42d1eb17e519cf69402f928e226bcda012f794123f74`  
		Last Modified: Thu, 13 Jun 2024 03:39:11 GMT  
		Size: 2.7 KB (2706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc2ebaf552da5fe6c2590e341ba5409682bee883c57e58c466dac63d44ab1b8`  
		Last Modified: Thu, 13 Jun 2024 03:39:11 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3a0e95ac47f3afc3fbe4d7dc0ac3bd8cebd23870a0e97cf3d507b2d76529d8`  
		Last Modified: Thu, 13 Jun 2024 03:39:11 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4737d1757b4cfd9b4b4410a0e561cd41baa3a1137cf9429f60341c0dd4fd3d2f`  
		Last Modified: Thu, 13 Jun 2024 03:39:11 GMT  
		Size: 1.4 MB (1386197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b1ba1961087c956a626db4f4f15e13371030de99245cdcb54e3b96bd00bfd5`  
		Last Modified: Thu, 13 Jun 2024 03:39:11 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; arm variant v5

```console
$ docker pull adminer@sha256:08c5b65a1be7c7aa54a2968fd1cbeb86e2d55bfbacfc9a9586c6181b475e952c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91225088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46b875fcea77f64e68b2c0a75a9ca64f9c4330b33cfbb48daa8cac1bfeeb9a01`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 02 Jul 2024 00:48:35 GMT
ADD file:cb32078a57dd8b6e640717e8afff9bcae9ea1cf42a7bd24509f83795da6d69ed in / 
# Tue, 02 Jul 2024 00:48:36 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:53:30 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 03:54:03 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:54:05 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 02 Jul 2024 03:54:28 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 02 Jul 2024 03:54:29 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 03:54:29 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 03:54:30 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 03:54:30 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 03:54:30 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 03:54:30 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 03:54:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 03:54:42 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:54:42 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 03:54:42 GMT
USER adminer
# Tue, 02 Jul 2024 03:54:42 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:cbbd165d7f0cb06245f1b11503844a1b512035157df3061a56ffc65bcd1fb0fa`  
		Last Modified: Tue, 02 Jul 2024 00:51:50 GMT  
		Size: 52.6 MB (52585748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f7309ec90f621fa946352bef134afda446f74cb6b7d9d7267e5330449e36c8`  
		Last Modified: Tue, 02 Jul 2024 03:55:00 GMT  
		Size: 37.2 MB (37247382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44798298ec5e66cb4c8fb9ed12052832d036fcd4175db67f70e1aa039485dd79`  
		Last Modified: Tue, 02 Jul 2024 03:54:51 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b002ee3154ea598fd6fa999f27d843bb1260cff8116f6cc5554d091026e8bcd`  
		Last Modified: Tue, 02 Jul 2024 03:55:16 GMT  
		Size: 2.7 KB (2710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48beb330b9a8cda7814bbe4e5281be2d34ec03ff5952849069898825d8598286`  
		Last Modified: Tue, 02 Jul 2024 03:55:15 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4772562fb04746e825af5723e66383ce63dcc0fee85d1260cff7fd3c2e7c16`  
		Last Modified: Tue, 02 Jul 2024 03:55:16 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf9151092b5d5a5880823f20e908eb4d95e781ed2fdd0163acf36431645d33c`  
		Last Modified: Tue, 02 Jul 2024 03:55:16 GMT  
		Size: 1.4 MB (1385055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82e06b0e9743e64637ffe594013f2f8950ad5f0181cd12c52cc90ee465c00d3`  
		Last Modified: Tue, 02 Jul 2024 03:55:15 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:d7a9613f54b6800baf5bff5ddcb78570f6db49624259395a8ad6b0050ecb20e5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87821273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a2ddcac894862583bc57384d0d86ff4f4b0f6a6cf7e3bc06703072915061612`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 02 Jul 2024 01:00:11 GMT
ADD file:6e828fd5dbd54f949f96129ea922c27ff88709484119faef51401e338e900e6e in / 
# Tue, 02 Jul 2024 01:00:12 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:22:33 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 01:22:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:22:58 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 02 Jul 2024 01:23:13 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 02 Jul 2024 01:23:14 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 01:23:14 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 01:23:14 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 01:23:14 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 01:23:15 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 01:23:15 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 01:23:25 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 01:23:25 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:23:25 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 01:23:26 GMT
USER adminer
# Tue, 02 Jul 2024 01:23:26 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:a0610bbe9cb80952dba5ef5efb55f03668fd4f8ab63ade3ba30e22a4c03c42da`  
		Last Modified: Tue, 02 Jul 2024 01:03:38 GMT  
		Size: 50.2 MB (50238998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3e702585d2844b32f333ffa43613971f1013588b36c6af0beb94933ab329df`  
		Last Modified: Tue, 02 Jul 2024 01:23:46 GMT  
		Size: 36.2 MB (36190267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc161248142474da0285bc49623a26644f13d41d531c678d99f6bcdf27b70ab2`  
		Last Modified: Tue, 02 Jul 2024 01:23:38 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278e0879cbde71294809045b9f266e5c21efd08e0de37a1524fe849c5aec091c`  
		Last Modified: Tue, 02 Jul 2024 01:24:01 GMT  
		Size: 2.7 KB (2707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f295d684f8c49423746d3e3453eb9b6558b2420fadcd2af073560ef3ba3164d`  
		Last Modified: Tue, 02 Jul 2024 01:24:01 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78de186446d878b08a2248378c5a7995e08af1f3ea0d9065bbaa93e3064f1492`  
		Last Modified: Tue, 02 Jul 2024 01:24:01 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:291046b85c65fb3c2d96ff23de17cb1c7081d6b3f79c1de2f385ac1f5187badf`  
		Last Modified: Tue, 02 Jul 2024 01:24:01 GMT  
		Size: 1.4 MB (1385106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798f52a962b7b31eaf46167c88b2046248291c575487d9f62d0b772246eb029b`  
		Last Modified: Tue, 02 Jul 2024 01:24:01 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:9fb8238a5c521871ff35554f5ae5d0bc01b3a02f6533c066354b1c7c3aa35975
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94360998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faef7483bf1a2f17c558024437e653b95e330af2e8d65c5eedad8936e1f74bfe`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:43 GMT
ADD file:4e98397394fc6db8fa55fb21c15dab09007b6ba883cb193f3a53f94480fee872 in / 
# Tue, 02 Jul 2024 00:39:44 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:49:11 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 03:49:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:49:30 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 02 Jul 2024 03:49:45 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 02 Jul 2024 03:49:45 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 03:49:45 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 03:49:45 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 03:49:45 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 03:49:45 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 03:49:46 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 03:49:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 03:49:55 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:49:55 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 03:49:55 GMT
USER adminer
# Tue, 02 Jul 2024 03:49:55 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:a4cd3ad66f7873241881d2ddd4efa6521034245e95e2b0b4a059817345151048`  
		Last Modified: Tue, 02 Jul 2024 00:42:43 GMT  
		Size: 53.7 MB (53721653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d598a96e1f6c21d200bed4ce637590b40e15537e182f139ad9e7dfbc0eb771`  
		Last Modified: Tue, 02 Jul 2024 03:50:10 GMT  
		Size: 39.2 MB (39247390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3f80d153c4cb4557ae4f75ad9ef8e2ccf062c76da8936df8457390e52b9aa6`  
		Last Modified: Tue, 02 Jul 2024 03:50:04 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb4338986eb0e74c2a78eb3fb1c88b08efa0da12646ae08717abf7b89dfca94`  
		Last Modified: Tue, 02 Jul 2024 03:50:25 GMT  
		Size: 2.7 KB (2706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12aeb9b0cfed224e44d5cd010b441e1421250b30d59505b259226be454dbcea`  
		Last Modified: Tue, 02 Jul 2024 03:50:25 GMT  
		Size: 1.8 KB (1846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103d2b1fd9f9d5ec62ae330e21b9dd3420e7cc4dacda67c6228f87f2d163b409`  
		Last Modified: Tue, 02 Jul 2024 03:50:25 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87eed7923ccd186885c991e63d8f620ec55d458fcffe40ad06c067e8fd37fe9`  
		Last Modified: Tue, 02 Jul 2024 03:50:25 GMT  
		Size: 1.4 MB (1385053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aed3eee28acfa327acb6c32934aa1fa14ad89654b1eacf3cda9008af112fd57`  
		Last Modified: Tue, 02 Jul 2024 03:50:25 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:fa1d9f1ea22ae5c61170f9fca064e7a8cc4fabf1019b36a3832f60df96b74c43
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (97016037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7cad11f7e3e9a78b9d09353a2a7622180fb8ec1b0c3cfe492b84b158920fa35`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:05 GMT
ADD file:e6fa59569d6234c463e39f7c2465f2984240a5e8cd613c1ffdc14ab3abb4a7ad in / 
# Tue, 02 Jul 2024 00:39:06 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:40:12 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 01:40:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:40:37 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 02 Jul 2024 01:41:01 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 02 Jul 2024 01:41:01 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 01:41:01 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 01:41:02 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 01:41:02 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 01:41:02 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 01:41:02 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 01:41:14 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 01:41:14 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:41:14 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 01:41:14 GMT
USER adminer
# Tue, 02 Jul 2024 01:41:14 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:72a2b38d7f88bb9b0be6097180e8f8261c31815017cb512a158422c2bfba6973`  
		Last Modified: Tue, 02 Jul 2024 00:43:02 GMT  
		Size: 56.1 MB (56064975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1cb0658743f3bf0542329357279433eb0f426af95c0d7e94dce6fb75ee5bf9`  
		Last Modified: Tue, 02 Jul 2024 01:41:34 GMT  
		Size: 39.6 MB (39559157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6a4f14b6f1d3fff499cb07c9d87429145bd9132193f2cacbe04e36cd333e65`  
		Last Modified: Tue, 02 Jul 2024 01:41:24 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9102ca46ad37706c2be0b65c1be59d6007926e9d4e03ebdb282b137ea8830054`  
		Last Modified: Tue, 02 Jul 2024 01:41:50 GMT  
		Size: 2.7 KB (2706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14ce46ed6df23d0620ded4345cd9f8e93171ed138a0677bf391a25a8a54d5b1`  
		Last Modified: Tue, 02 Jul 2024 01:41:50 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a0c53dafacd37de3b69783b77f9770b20b43a4f99bc948d477e150d7a8b48a`  
		Last Modified: Tue, 02 Jul 2024 01:41:50 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa73ce21828f04d5751def3ef27e43f9a28a47017d4722c1779458182367585`  
		Last Modified: Tue, 02 Jul 2024 01:41:51 GMT  
		Size: 1.4 MB (1385008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ea734ba44cd83d16f8eeaf1377c387cc0d4ce1a249ce59477930beefb21fab`  
		Last Modified: Tue, 02 Jul 2024 01:41:50 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; mips64le

```console
$ docker pull adminer@sha256:4447d41c532506f31b176016e55e9828ec5b38983f1024ef6d2c69df6c3bd68b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92652819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25380b4bd6f270cbc89408a5d5ffa417d87da456e9deeedbc5c71b48683017bf`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 02 Jul 2024 01:18:58 GMT
ADD file:c27c9e3b89ea2f05df44728fc1fc46f994aa335600846cab7240fdd415afec7a in / 
# Tue, 02 Jul 2024 01:19:04 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 02:42:44 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 02:44:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 02:44:43 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 02 Jul 2024 02:46:32 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 02 Jul 2024 02:46:39 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 02:46:43 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 02:46:46 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 02:46:50 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 02:46:54 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 02:46:57 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 02:47:47 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 02:47:50 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 02:47:54 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 02:47:58 GMT
USER adminer
# Tue, 02 Jul 2024 02:48:01 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:47b1b1e48b458e7bb52034561a02c3a9df945540ee55d2b8112f6501aaad6d66`  
		Last Modified: Tue, 02 Jul 2024 01:30:13 GMT  
		Size: 53.3 MB (53306204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90a42cb8f86637789485d8f3342a992c44b570dfb8b57fdff85b71953ba6011`  
		Last Modified: Tue, 02 Jul 2024 02:48:45 GMT  
		Size: 38.0 MB (37953612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a9026c134b9f52702d6723ec03385ca9d23e41902b989e29e01be697d047e7e`  
		Last Modified: Tue, 02 Jul 2024 02:48:18 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27a9ac3be746df72fd5ce2862d251918ac18034b8446dc78c54d1f513123cc8`  
		Last Modified: Tue, 02 Jul 2024 02:49:04 GMT  
		Size: 2.7 KB (2717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288935c60a3913c0f4a9e2afbd507b542b3acd7e694aff3d21b2c625253a022b`  
		Last Modified: Tue, 02 Jul 2024 02:49:04 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b9cab53977f50243418e093156f2da54d6873c602ebc74d12370bffb232fca`  
		Last Modified: Tue, 02 Jul 2024 02:49:04 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20200af67ae61cf64bdec599fe75711da487cc15e6c3191b4503b4c6efa70b5d`  
		Last Modified: Tue, 02 Jul 2024 02:49:05 GMT  
		Size: 1.4 MB (1386189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0abd175a01e1719444884e910bad30c0071ecfe4cba369ae8c37792fe8ca466`  
		Last Modified: Tue, 02 Jul 2024 02:49:04 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:8c36f5365333111df7fecbeff71b2feb1c75377f1ea2d81d63d0c1c8ab37339a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101287189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666b4ff57f2616ee35b12f1422755e8dffedeb55c23cc89d98991eff8c295df2`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 02 Jul 2024 01:17:47 GMT
ADD file:288859e020cf9178f55732ac2eaa62400e2c2d66b3ca500ac7df69c8025abba9 in / 
# Tue, 02 Jul 2024 01:17:50 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:41:50 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 01:42:26 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:42:29 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 02 Jul 2024 01:43:02 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 02 Jul 2024 01:43:03 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 01:43:03 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 01:43:04 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 01:43:04 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 01:43:04 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 01:43:05 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 01:43:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 01:43:22 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:43:23 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 01:43:23 GMT
USER adminer
# Tue, 02 Jul 2024 01:43:23 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:202e493da11eac96a36d754afa396feec67f46e0492e70c0cc4d61dfb06d6a75`  
		Last Modified: Tue, 02 Jul 2024 01:22:20 GMT  
		Size: 59.0 MB (58950397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7eac8c8c144e55267a50109e782157ccd5cd6ddec77fcdcbc539adbba14e68`  
		Last Modified: Tue, 02 Jul 2024 01:43:46 GMT  
		Size: 40.9 MB (40944698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ca81bd5ac1b95ad159c22cbaaa5d6261ef14464275873a0f0f7a3ff99f8196`  
		Last Modified: Tue, 02 Jul 2024 01:43:37 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0b7cb50172b19398a4adade2d74ad7bcce9240a064caca833d7eb3feb43531`  
		Last Modified: Tue, 02 Jul 2024 01:44:01 GMT  
		Size: 2.7 KB (2710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f335caa4cad8e2e7fdbecfa110480577032340be8e50cb15491eb7a2b7a50989`  
		Last Modified: Tue, 02 Jul 2024 01:44:01 GMT  
		Size: 1.9 KB (1855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3a5a23cc915a801b4423819e6ddb10f6d5c4cd92f8019a62496f88e224a27f`  
		Last Modified: Tue, 02 Jul 2024 01:44:02 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fe0d02446353d9ead6d6a9ace37ee925439eae7af5c23ea02665eb9d4f68ac`  
		Last Modified: Tue, 02 Jul 2024 01:44:02 GMT  
		Size: 1.4 MB (1385166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27eb9dfa96764a0fba42d2baa6b891a577a34153fd1cda29ef60fde217a580f9`  
		Last Modified: Tue, 02 Jul 2024 01:44:01 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; s390x

```console
$ docker pull adminer@sha256:e7f8d32569a5db1ff3c0ccf426f649132c1d578ed7c2602ddeb67781ed94432a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93737943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a95c2c12bdb252df9d0621dffca03eaccd6cf8f844b0112e109016a96066bb1b`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 02 Jul 2024 00:43:57 GMT
ADD file:5752d26037cbb262eeafd1819ecd77ecf8a8cd0019683c05fb92c50c6a458861 in / 
# Tue, 02 Jul 2024 00:44:00 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:09:46 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 01:10:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:10:15 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 02 Jul 2024 01:10:39 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 02 Jul 2024 01:10:39 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 01:10:39 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 01:10:39 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 01:10:39 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 01:10:39 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 01:10:39 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 01:10:47 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 01:10:47 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:10:47 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 01:10:47 GMT
USER adminer
# Tue, 02 Jul 2024 01:10:47 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:aa9549a3d8effd17bc1f93fd40d83261d2505d37791c5aa837c9f7c0fff5c9e3`  
		Last Modified: Tue, 02 Jul 2024 00:48:47 GMT  
		Size: 53.3 MB (53319825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedf208e7ad95eff4e4a53475d4f372a5db2c23c030fb667e956a0c8680cd80d`  
		Last Modified: Tue, 02 Jul 2024 01:11:07 GMT  
		Size: 39.0 MB (39026087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19727321c5dc021f6445e25e21dced8c0dcba8235da541f23ee00f2bc54eaea5`  
		Last Modified: Tue, 02 Jul 2024 01:11:00 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9076ecdc74fae7d7ef0c5d114c4db792912ab1ae1a12762c60a2f9a54171bfc3`  
		Last Modified: Tue, 02 Jul 2024 01:11:17 GMT  
		Size: 2.7 KB (2709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b7e7f7d0ce935920fb39131256800949b224adad4cc0901b92ee8580d7c3a2`  
		Last Modified: Tue, 02 Jul 2024 01:11:17 GMT  
		Size: 1.8 KB (1849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567bf21a89c547de6dc47991e16b14e580892319f21623900bbed80f96c32aa4`  
		Last Modified: Tue, 02 Jul 2024 01:11:17 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55d536c07334228af9a1a649481984dade1492e5fb91515c44aef6a5f3b81d9e`  
		Last Modified: Tue, 02 Jul 2024 01:11:18 GMT  
		Size: 1.4 MB (1385114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a180d0fa448c885cd3aab9720eaf86a3d562d51b38cd00e5010ccd49df7a271f`  
		Last Modified: Tue, 02 Jul 2024 01:11:17 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
