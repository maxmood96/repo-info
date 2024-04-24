## `adminer:fastcgi`

```console
$ docker pull adminer@sha256:f83937ce4e078bbfca599757b0d0901c8fbd7440d4e1b83bc9eb12ef023ff245
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
$ docker pull adminer@sha256:253f0e2df72c7f2aa864744ff5e138feaa1546a0969b738b20b76555c91aba49
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95983050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2f19b054ecdafda61fc923e7e464c9ee593dbf9578d712b073644404fd35b5`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:55:47 GMT
STOPSIGNAL SIGINT
# Wed, 24 Apr 2024 07:56:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 07:56:08 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 24 Apr 2024 07:56:29 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 24 Apr 2024 07:56:29 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 24 Apr 2024 07:56:29 GMT
WORKDIR /var/www/html
# Wed, 24 Apr 2024 07:56:29 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 24 Apr 2024 07:56:29 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 24 Apr 2024 07:56:30 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 24 Apr 2024 07:56:30 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 24 Apr 2024 07:56:40 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 07:56:40 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 24 Apr 2024 07:56:40 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 24 Apr 2024 07:56:41 GMT
USER adminer
# Wed, 24 Apr 2024 07:56:41 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5096f84f4308bc954f0361dfa1b3e03e6b8031b58c17ec09b11df165ea3ebaa0`  
		Last Modified: Wed, 24 Apr 2024 07:57:01 GMT  
		Size: 39.5 MB (39490925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0db97453a39997547f4044074fdb80860d005a0aa7fc63c3fa6733afa85df8e`  
		Last Modified: Wed, 24 Apr 2024 07:56:53 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5dc0139d6b46bc5066e2771144862b5948aeca4385145d4cfc6a1b83b52029e`  
		Last Modified: Wed, 24 Apr 2024 07:57:17 GMT  
		Size: 2.7 KB (2709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e164ab4bb7e5edb155515cc1ddca133c823a0dd5145e7bc59e9c25f6fa177db`  
		Last Modified: Wed, 24 Apr 2024 07:57:17 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8091b5ef47d5b40df0a890a8649777982d9f82ed11949ffac71155f0073dbaf3`  
		Last Modified: Wed, 24 Apr 2024 07:57:17 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bab32144b8352b1d012d077f05cf9840b8e1b003817ad90679b6c55926b1444`  
		Last Modified: Wed, 24 Apr 2024 07:57:18 GMT  
		Size: 1.4 MB (1386313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c0ae20bd69ccb765bf51395533ea827b235361d3e3e62364d262707dac21df`  
		Last Modified: Wed, 24 Apr 2024 07:57:17 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; arm variant v5

```console
$ docker pull adminer@sha256:698f789e22a2a6b48a26edc869596a52aa273ce28bafbe5fd2a9a81a3b8d5c7d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91245470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4872a73c5da2302fc5f68c7ead990ed8d12732be27a20abcbbab2f31329384`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 24 Apr 2024 03:53:19 GMT
ADD file:a9204ad0624794bf1867ecaadf429b37a75cf0470efcb6420d52afd6a0d7384a in / 
# Wed, 24 Apr 2024 03:53:20 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:33:29 GMT
STOPSIGNAL SIGINT
# Wed, 24 Apr 2024 04:33:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:33:58 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 24 Apr 2024 04:34:18 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 24 Apr 2024 04:34:18 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 24 Apr 2024 04:34:19 GMT
WORKDIR /var/www/html
# Wed, 24 Apr 2024 04:34:19 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 24 Apr 2024 04:34:19 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 24 Apr 2024 04:34:19 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 24 Apr 2024 04:34:19 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 24 Apr 2024 04:34:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 04:34:32 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 24 Apr 2024 04:34:32 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 24 Apr 2024 04:34:32 GMT
USER adminer
# Wed, 24 Apr 2024 04:34:32 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:96ca8272ff5aa89d1aff093d37bbcb1b79155357b7c25c1163da1eeded65ad16`  
		Last Modified: Wed, 24 Apr 2024 03:56:49 GMT  
		Size: 52.6 MB (52602918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9c2f1ca3404d823faf0fb61a552906dcbf4b3bcafae1507821484aafc96b74`  
		Last Modified: Wed, 24 Apr 2024 04:34:50 GMT  
		Size: 37.2 MB (37249468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4186f270398d6d2318b44d1ad7bcb9fd75573b7ea49870201d60cd7584e9594d`  
		Last Modified: Wed, 24 Apr 2024 04:34:41 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1090535c78e1a6707aac95cc19f671d875f0883efde54e75d94fa32bac57817`  
		Last Modified: Wed, 24 Apr 2024 04:35:06 GMT  
		Size: 2.7 KB (2708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:058daecd4fc076ab0f28f6704a7d9d9dcb99bf7f7311d96e4635373f0a3d3c69`  
		Last Modified: Wed, 24 Apr 2024 04:35:07 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888bdd7f93c1e83f27637d9403cc0752eb16a81d83cb2130d95509c949014075`  
		Last Modified: Wed, 24 Apr 2024 04:35:06 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:433899a33c359e104ed57a9ed99906f751a8075d290c1080afd4d3d30017abee`  
		Last Modified: Wed, 24 Apr 2024 04:35:07 GMT  
		Size: 1.4 MB (1386139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b573a377509b048bccdb104f68c8d18b2e580933f564e9f9752730c2e582f72a`  
		Last Modified: Wed, 24 Apr 2024 04:35:07 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:0f73f7486b8ad79b78675bc767dcbacf482c15e6eaa64255193b999a0ec09fef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87840003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4c328b17743d7d71a4fc0f56b46224efc7ac88872e087395c6775905603ec96`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:15 GMT
ADD file:59046a1e0987059e779fff5a0f35e03203c109d778a75058e9474705d3fcfdff in / 
# Wed, 24 Apr 2024 04:07:15 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 07:00:55 GMT
STOPSIGNAL SIGINT
# Wed, 24 Apr 2024 07:01:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 07:01:24 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 24 Apr 2024 07:01:53 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 24 Apr 2024 07:01:54 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 24 Apr 2024 07:01:54 GMT
WORKDIR /var/www/html
# Wed, 24 Apr 2024 07:01:54 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 24 Apr 2024 07:01:54 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 24 Apr 2024 07:01:54 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 24 Apr 2024 07:01:55 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 24 Apr 2024 07:02:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 07:02:07 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 24 Apr 2024 07:02:07 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 24 Apr 2024 07:02:07 GMT
USER adminer
# Wed, 24 Apr 2024 07:02:07 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:853e2341066ebc3a07d3c44ebac8c3ce40daf429fb9cc3f49f2d35115e9cc93f`  
		Last Modified: Wed, 24 Apr 2024 04:11:34 GMT  
		Size: 50.3 MB (50255574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba9aea151c123300ec4c6ebfa8d960f68ecba70226807aba751761aada89370`  
		Last Modified: Wed, 24 Apr 2024 07:02:28 GMT  
		Size: 36.2 MB (36191313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c64e04373df38d5b56e2a72a0292a80c1d271b5e1639188b4f832479de6638e`  
		Last Modified: Wed, 24 Apr 2024 07:02:19 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7224829184412f47583d46329b64dc144a51c6b0ccfad5e5884bfd27fb7ba5e3`  
		Last Modified: Wed, 24 Apr 2024 07:02:44 GMT  
		Size: 2.7 KB (2708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7785c8eccd949f5dd6d11e06dc1c1238b8d1ac9ae3f6f03c1a8be6ee22a6c5e`  
		Last Modified: Wed, 24 Apr 2024 07:02:44 GMT  
		Size: 1.9 KB (1873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd95b4fa45165adb6433e46abb5925c2ddc8320cc1c920a7d4d2f0cfb80081b`  
		Last Modified: Wed, 24 Apr 2024 07:02:44 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e0bec56da1d754d7efda005511a554028ef1d1ccb277793af1843065c25da73`  
		Last Modified: Wed, 24 Apr 2024 07:02:44 GMT  
		Size: 1.4 MB (1386172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a5d038b542292e6a84f74b054f63fe540a6f4d6c95306732191d91693e4588`  
		Last Modified: Wed, 24 Apr 2024 07:02:44 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:655c8050585ba25102b9e5072261f1a1fca555f5ce83dbc4302c909aca892232
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94382216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1da926a695bc86fd1a86d50b2ff97238545f400eb2e06428c2af9417e8e298`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:46 GMT
ADD file:3ebbb50438ec23ebe0c880a5421d505922771b7bd4202b5c8f839702dd726036 in / 
# Wed, 24 Apr 2024 04:10:46 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:51:29 GMT
STOPSIGNAL SIGINT
# Wed, 24 Apr 2024 04:51:48 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:51:49 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 24 Apr 2024 04:52:03 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 24 Apr 2024 04:52:03 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 24 Apr 2024 04:52:03 GMT
WORKDIR /var/www/html
# Wed, 24 Apr 2024 04:52:03 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 24 Apr 2024 04:52:03 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 24 Apr 2024 04:52:04 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 24 Apr 2024 04:52:04 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 24 Apr 2024 04:52:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 04:52:13 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 24 Apr 2024 04:52:13 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 24 Apr 2024 04:52:13 GMT
USER adminer
# Wed, 24 Apr 2024 04:52:13 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:64d502aff46d2ed56e6228994304818b354d02b13d6122492c5d3e0886c92897`  
		Last Modified: Wed, 24 Apr 2024 04:14:26 GMT  
		Size: 53.7 MB (53739959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20cad2dcdecbe0dc4f7ca89b641bb6af757ab184972b6faa4deea50db6985046`  
		Last Modified: Wed, 24 Apr 2024 04:52:30 GMT  
		Size: 39.2 MB (39249115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1017a92e52bb823e05bdc12ae4878481bc7ba88cb21946e5294728242e59ce`  
		Last Modified: Wed, 24 Apr 2024 04:52:23 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2db244fa298bcfaea3cb8cb8c57ac6657a549b5f881c8269f0b601ab7dfecaf`  
		Last Modified: Wed, 24 Apr 2024 04:52:45 GMT  
		Size: 2.7 KB (2709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41fe42387f85f24a52bc76fe518a3f8643e0f917edc6fccaeeb4317846693f51`  
		Last Modified: Wed, 24 Apr 2024 04:52:45 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4370fae2824c861dacb6de720838fe3e34c495aa67f23fc5434341050b7b3a67`  
		Last Modified: Wed, 24 Apr 2024 04:52:45 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf465604b4a20831de40f82fbdcf58871f6a9c68868d4ab6754caa609bd6188`  
		Last Modified: Wed, 24 Apr 2024 04:52:45 GMT  
		Size: 1.4 MB (1386190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed4a622e4387dc227f5199dc8fec0094b5cfac3b1056ccd4c90517e399db419`  
		Last Modified: Wed, 24 Apr 2024 04:52:45 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:219d759b2bf8eb597d62e56113fe3af26fbc544791116bf97098a514e32ff5db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (97030491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf768a6445d667aa9a3fdc7a45e6d590a5dce57ad75e5151b8032ba546848a23`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 24 Apr 2024 03:39:08 GMT
ADD file:f45ff600062e56788dec8eb7a1a4eb58c56391243efecfc62b3f911f35ce7517 in / 
# Wed, 24 Apr 2024 03:39:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:51:11 GMT
STOPSIGNAL SIGINT
# Wed, 24 Apr 2024 04:51:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:51:44 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 24 Apr 2024 04:52:10 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 24 Apr 2024 04:52:10 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 24 Apr 2024 04:52:11 GMT
WORKDIR /var/www/html
# Wed, 24 Apr 2024 04:52:11 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 24 Apr 2024 04:52:11 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 24 Apr 2024 04:52:11 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 24 Apr 2024 04:52:11 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 24 Apr 2024 04:52:26 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 04:52:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 24 Apr 2024 04:52:26 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 24 Apr 2024 04:52:26 GMT
USER adminer
# Wed, 24 Apr 2024 04:52:26 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:531ff4ee4f75fb0b1990fd185259fbec17670ebea9c3011de30a27e2de08c387`  
		Last Modified: Wed, 24 Apr 2024 03:43:58 GMT  
		Size: 56.1 MB (56076550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3713475eda203220b4592ce7cc17e6f2aba351d5c2cb6b6e8561832ba118fd3b`  
		Last Modified: Wed, 24 Apr 2024 04:52:49 GMT  
		Size: 39.6 MB (39560832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc2be56ea12f89081c28d0c1defdfa75b3e59b6e03327049481f660c7b34c30`  
		Last Modified: Wed, 24 Apr 2024 04:52:38 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f9f99c1fe51e40f1951e1422179370739ea827c626105a42e253bbb9d95d4f`  
		Last Modified: Wed, 24 Apr 2024 04:53:06 GMT  
		Size: 2.7 KB (2713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a92e702f5d4a5b984253456899f05c9ab95f8c96e8580daa937ade037adfcd2`  
		Last Modified: Wed, 24 Apr 2024 04:53:06 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90301fe51eb9b2ef53e4b1f364ab08be495170eaba4d6c2264b1574573d8bd8b`  
		Last Modified: Wed, 24 Apr 2024 04:53:06 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b976ab8e491d1317d59065657b957511de8833dd1b30eddc736b0d1237a188`  
		Last Modified: Wed, 24 Apr 2024 04:53:06 GMT  
		Size: 1.4 MB (1386160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbcbd7b0f7f6b9dfb0148ca4eea97db3a55285371aa4698ca7450e36af4b0183`  
		Last Modified: Wed, 24 Apr 2024 04:53:06 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; mips64le

```console
$ docker pull adminer@sha256:87c9dd79192a65b2eb9a6e22c78a27db76699a1a3b9b943ef06c34bc596d49dd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92672154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef95db063489d6c4141d6c7302b6ab25b8a0cff057a55113fa470c3118dd0c11`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 24 Apr 2024 03:14:51 GMT
ADD file:d071b57187646d0653c08b1eb289840e8f9b901923339a0c04c87c0cddd93a41 in / 
# Wed, 24 Apr 2024 03:14:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 10:43:49 GMT
STOPSIGNAL SIGINT
# Wed, 24 Apr 2024 10:45:40 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 10:45:46 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 24 Apr 2024 10:47:37 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 24 Apr 2024 10:47:43 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 24 Apr 2024 10:47:47 GMT
WORKDIR /var/www/html
# Wed, 24 Apr 2024 10:47:50 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 24 Apr 2024 10:47:53 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 24 Apr 2024 10:47:56 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 24 Apr 2024 10:48:00 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 24 Apr 2024 10:48:50 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 10:48:53 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 24 Apr 2024 10:48:56 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 24 Apr 2024 10:48:59 GMT
USER adminer
# Wed, 24 Apr 2024 10:49:03 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:1d0c8a1684008e75383df0eb74516bfb1122de8ea4827b46099c12fd8e762fd1`  
		Last Modified: Wed, 24 Apr 2024 03:26:04 GMT  
		Size: 53.3 MB (53322762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:279765339683ddab38d8a848da07ff0ab06dc236bd83f3ed8c0a50caaa988348`  
		Last Modified: Wed, 24 Apr 2024 10:49:50 GMT  
		Size: 38.0 MB (37955469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0264741265ee3dd74b58446e908c99a3e7f6a83dd796a6569a61269de234be00`  
		Last Modified: Wed, 24 Apr 2024 10:49:24 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c092fcb633c74d70c8a1350fdc63dbf3a123c631f6920cba24c229a96ab492a`  
		Last Modified: Wed, 24 Apr 2024 10:50:08 GMT  
		Size: 2.7 KB (2713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a20ba1b0ffad90940a29736f4746889cd71b07d685142a86fcf58912fdbaa2`  
		Last Modified: Wed, 24 Apr 2024 10:50:08 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088524a2925a944807584966325ca9f4219e38cb09eb9c437139363ebbe9ba9f`  
		Last Modified: Wed, 24 Apr 2024 10:50:09 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b265d11eaac6002abf5c4079db316107a2818ab9c640c2c2a444dde6a0dd03fe`  
		Last Modified: Wed, 24 Apr 2024 10:50:09 GMT  
		Size: 1.4 MB (1387112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe88e468aa13e1afc53c0db6b7834c181495e98db9d6eda804fc58a0a68374b1`  
		Last Modified: Wed, 24 Apr 2024 10:50:08 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:ccfcd9e9bbd5570e14f029e39b97f455082d4edff0481da70ac7e89c96b2f018
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101308296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d738f471ab473f3298b4957f7f17e01528c7d2960838adcecb039a941030bdc3`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:25 GMT
ADD file:f5283c61db1fea68c9d742ae60d7572775bfb46d2e8a92659edbd0c98e083a93 in / 
# Wed, 24 Apr 2024 03:21:30 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 05:37:12 GMT
STOPSIGNAL SIGINT
# Wed, 24 Apr 2024 05:38:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 05:38:10 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 24 Apr 2024 05:38:52 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 24 Apr 2024 05:38:55 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 24 Apr 2024 05:38:55 GMT
WORKDIR /var/www/html
# Wed, 24 Apr 2024 05:38:56 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 24 Apr 2024 05:38:56 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 24 Apr 2024 05:38:57 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 24 Apr 2024 05:38:57 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 24 Apr 2024 05:39:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 05:39:17 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 24 Apr 2024 05:39:18 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 24 Apr 2024 05:39:18 GMT
USER adminer
# Wed, 24 Apr 2024 05:39:18 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:aac3759e46343ae5d9b035355707bd07abf04ff80e3d29e689ea89cc78633190`  
		Last Modified: Wed, 24 Apr 2024 03:27:06 GMT  
		Size: 59.0 MB (58968197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57d70fa503320b06bf9baec13f40612a46b936e08316af464f545d0bd898eb9`  
		Last Modified: Wed, 24 Apr 2024 05:39:44 GMT  
		Size: 40.9 MB (40946838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff94d39249854f08c8a7bfec1326398e6d73a712740eda11d2212a1d7e87501`  
		Last Modified: Wed, 24 Apr 2024 05:39:35 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80b70f072261a749d318f7229e45328b58a8ca7d0a64453ca3eb56ab80cc352`  
		Last Modified: Wed, 24 Apr 2024 05:40:02 GMT  
		Size: 2.7 KB (2711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1edf40c11d7ccd8854593fae8d8ea5a7c9c4c059a1c8b0c920b37a98ee3b14b3`  
		Last Modified: Wed, 24 Apr 2024 05:40:03 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db06926b7323e1bdede1ab01770f87647828492ba9caad07da94e48830e270e3`  
		Last Modified: Wed, 24 Apr 2024 05:40:03 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ad3edc542f9c06d0ba70f2828b8d4ae425114238b32ca5c9a7abaaccea0829`  
		Last Modified: Wed, 24 Apr 2024 05:40:03 GMT  
		Size: 1.4 MB (1386300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2283858cd964f10d3b1aa58951c8c35f3ace6ace1fff3b59930a932ad740fc1`  
		Last Modified: Wed, 24 Apr 2024 05:40:03 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; s390x

```console
$ docker pull adminer@sha256:53b76f101a7260b2a9046cca04f5cbfaae97417a4f6e2d892a580b6eba42db9b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.8 MB (93758414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0777dc8b6920e4d68810e2bc17b1e6ef048647575728563311986ea108d80262`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:33 GMT
ADD file:e0a1fc1de1477cea6fe41bdd15378013c680928cad3988dd16926cc1562c775e in / 
# Wed, 24 Apr 2024 03:43:38 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:08:14 GMT
STOPSIGNAL SIGINT
# Wed, 24 Apr 2024 04:08:39 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:08:42 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 24 Apr 2024 04:09:07 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 24 Apr 2024 04:09:08 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 24 Apr 2024 04:09:08 GMT
WORKDIR /var/www/html
# Wed, 24 Apr 2024 04:09:08 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 24 Apr 2024 04:09:08 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 24 Apr 2024 04:09:08 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 24 Apr 2024 04:09:08 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 24 Apr 2024 04:09:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 04:09:18 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 24 Apr 2024 04:09:18 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 24 Apr 2024 04:09:18 GMT
USER adminer
# Wed, 24 Apr 2024 04:09:18 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:b57a10abb081ff40e5bb34246c3875a71b8d258f767c4f8384d7054b1bc42725`  
		Last Modified: Wed, 24 Apr 2024 03:49:31 GMT  
		Size: 53.3 MB (53337419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f000da620f18f4a31edb16d3869bd09f18ee883656f6a7b4067f1d3cdb6dc58`  
		Last Modified: Wed, 24 Apr 2024 04:09:46 GMT  
		Size: 39.0 MB (39027838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c567243ba0a6c61cf24125bdd5fef1f1282a50aefcec2250c74a458a3f66d39f`  
		Last Modified: Wed, 24 Apr 2024 04:09:39 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f524d98f9e4f1d111a66102fd300283b0b485a66caa3279ee5dacb27c46b50b7`  
		Last Modified: Wed, 24 Apr 2024 04:09:58 GMT  
		Size: 2.7 KB (2709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd2ae17bf3436611f5b19dba7cef8266c0833d9ac3f15ba83370cf2cde3a37d`  
		Last Modified: Wed, 24 Apr 2024 04:09:58 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90500ec28ae8e1e6d94723ff18bf64e13c02212dafda08f34e6ddd229112f108`  
		Last Modified: Wed, 24 Apr 2024 04:09:58 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd5769551615f91e2ab618eb8144b0dc1ba4c3b35f4ccc7501751354a049138`  
		Last Modified: Wed, 24 Apr 2024 04:09:58 GMT  
		Size: 1.4 MB (1386203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d9b32af69904ae5fa3b0cadc44a62f38cb3871e38286c13b4e6af61dd46300`  
		Last Modified: Wed, 24 Apr 2024 04:09:58 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
