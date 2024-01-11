## `adminer:4-fastcgi`

```console
$ docker pull adminer@sha256:e5db6d8cd1ffc4e134bbdd30d3bcda3f3d86a1471d3f361d9df4a9eec9767a26
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

### `adminer:4-fastcgi` - linux; amd64

```console
$ docker pull adminer@sha256:428b1c03245be20d091c25ceaa53e61519614ed494b11c44ac6c12b9b224c00a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95944761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2f8b7002f6c5e2444661106e648ef25f2c03a911273a3f6def3ad40d397ab83`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:04 GMT
ADD file:35f7caaedc3b6f725dee87eb8d1f2727c04cb21062b5eb7f59801dafced61993 in / 
# Thu, 11 Jan 2024 02:38:05 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:30:08 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jan 2024 04:30:28 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 04:30:29 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 11 Jan 2024 04:30:50 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 11 Jan 2024 04:30:50 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 11 Jan 2024 04:30:50 GMT
WORKDIR /var/www/html
# Thu, 11 Jan 2024 04:30:50 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 11 Jan 2024 04:30:51 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 11 Jan 2024 04:30:51 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 11 Jan 2024 04:30:51 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 11 Jan 2024 04:31:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 04:31:02 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 11 Jan 2024 04:31:02 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 11 Jan 2024 04:31:02 GMT
USER adminer
# Thu, 11 Jan 2024 04:31:02 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:e455cf41eadb2f19f014361006086cdc5b3de16f3d13bd1d586be63e66c7fc63`  
		Last Modified: Thu, 11 Jan 2024 02:42:47 GMT  
		Size: 55.1 MB (55057723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50af658c9ab413883d4e6df2a572288002f42aeb0144a51da34ef08bed4a5529`  
		Last Modified: Thu, 11 Jan 2024 04:31:21 GMT  
		Size: 39.5 MB (39493696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8160da1ef8d0655d1d4ff5d4d477d45a35bdc030938d3b7fc2066e741c94cc40`  
		Last Modified: Thu, 11 Jan 2024 04:31:13 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6000afd3a98cb4650edf578e28c2dbf25506cc3eb63a49bcfb407eba92028cae`  
		Last Modified: Thu, 11 Jan 2024 04:31:38 GMT  
		Size: 2.7 KB (2709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed4fc433f5710b9e30704d54fdbe2d20e80ecc2341cabb556b3f582a4817549`  
		Last Modified: Thu, 11 Jan 2024 04:31:38 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca7d816923ed25e42755849f48218ccaececf80f997c54481cd738c7bc0e009`  
		Last Modified: Thu, 11 Jan 2024 04:31:38 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2617ae903532bbe630607477cfc859337a3b9fb572c2c1600d52ca7ef44e6e3d`  
		Last Modified: Thu, 11 Jan 2024 04:31:38 GMT  
		Size: 1.4 MB (1386394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92cf8d5f81dc9aef3e6c1bb6bdfe67637acb85685d6417bc74d01f52275df7e4`  
		Last Modified: Thu, 11 Jan 2024 04:31:38 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm variant v5

```console
$ docker pull adminer@sha256:68a3aa1692f6a0a88892dffa89329c325fe5bf46183d148f8a533cafdbe53fc3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91208860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b242336ed6ca45a8505807bc3dd09f9bb52d13dbf6be4e0ee2573a491f3e144`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 11 Jan 2024 01:49:11 GMT
ADD file:a5224163b267c4b112f96005ef36619be78d0b949e20d9008f94efc7116f9605 in / 
# Thu, 11 Jan 2024 01:49:12 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:46:10 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jan 2024 06:47:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:47:39 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 11 Jan 2024 06:48:21 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 11 Jan 2024 06:48:23 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 11 Jan 2024 06:48:23 GMT
WORKDIR /var/www/html
# Thu, 11 Jan 2024 06:48:24 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 11 Jan 2024 06:48:24 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 11 Jan 2024 06:48:24 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 11 Jan 2024 06:48:25 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 11 Jan 2024 06:48:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 06:48:54 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 11 Jan 2024 06:48:54 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 11 Jan 2024 06:48:55 GMT
USER adminer
# Thu, 11 Jan 2024 06:48:55 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:8600a8817f4f0136707c29239c933cdd333774f1c11cb22b584b1a8aeb8dfc22`  
		Last Modified: Thu, 11 Jan 2024 01:54:27 GMT  
		Size: 52.6 MB (52562506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989303398ed7d45ff7b18369ecf38c49b25c4af9baba52a84aa352418c84457a`  
		Last Modified: Thu, 11 Jan 2024 06:49:23 GMT  
		Size: 37.3 MB (37252999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb106eefbdc467cdbc6bf17e7caf3453251d7411bb91657867c48e88767c20f`  
		Last Modified: Thu, 11 Jan 2024 06:49:11 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6dd21b9dbff0aaaf39c3faa9223d206fbcdfe5facd1d7508916fba7026a7218`  
		Last Modified: Thu, 11 Jan 2024 06:49:41 GMT  
		Size: 2.7 KB (2715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84cc3e9cb7b14c2db01eaa9f33bf321ff3184fe986f4a69443578b81917623d`  
		Last Modified: Thu, 11 Jan 2024 06:49:41 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1eb5df7a6b406d038ae31f5d745ffb6ea8de1f0cc10bc59554804d62bbf48c8`  
		Last Modified: Thu, 11 Jan 2024 06:49:42 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ef5de32a13dbc1dece3a76eff98c94f0a52ddceeeabf54f1f06f56bcc9d2e0`  
		Last Modified: Thu, 11 Jan 2024 06:49:42 GMT  
		Size: 1.4 MB (1386405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad74f4802fecf96e338a45b502e0e70a231365aa89a12113931b269a975ffa3e`  
		Last Modified: Thu, 11 Jan 2024 06:49:41 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:d856eb5b15c35630750cf97009273130736918b562a01f5db76f299a38aa515a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87800161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0230b73676d6472e3c0e4cc8b735e6223fadcf642df896d701c2019196dc2b46`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:21 GMT
ADD file:06c355196a858f2594c761bea3314e053018c78a4b06eabe168db940f6c18e26 in / 
# Thu, 11 Jan 2024 02:42:21 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:40:02 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jan 2024 03:41:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:41:03 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 11 Jan 2024 03:41:41 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 11 Jan 2024 03:41:42 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 11 Jan 2024 03:41:43 GMT
WORKDIR /var/www/html
# Thu, 11 Jan 2024 03:41:43 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 11 Jan 2024 03:41:43 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 11 Jan 2024 03:41:43 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 11 Jan 2024 03:41:44 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 11 Jan 2024 03:42:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 03:42:09 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 11 Jan 2024 03:42:09 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 11 Jan 2024 03:42:09 GMT
USER adminer
# Thu, 11 Jan 2024 03:42:09 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:6c8fc6a3ed50d9d1c829e556b5efd4ca23cd5d51d5dcdec2a7a70b583673ef89`  
		Last Modified: Thu, 11 Jan 2024 02:49:02 GMT  
		Size: 50.2 MB (50215530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393242fd9ebca2ed8f76825b93d33a2ced3fd664d9bc240f1c0cd0913c502b27`  
		Last Modified: Thu, 11 Jan 2024 03:42:34 GMT  
		Size: 36.2 MB (36191266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e6941710463f6127edf0a350f987d17b54c4ce5147fb9b7e321bbbc5dc2e35`  
		Last Modified: Thu, 11 Jan 2024 03:42:24 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39439bf487c4b5f845d5930c3cc420646f700e985dbbe650a8618ffeca110dbc`  
		Last Modified: Thu, 11 Jan 2024 03:42:52 GMT  
		Size: 2.7 KB (2713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5726201484242065e73c8f83c71d03b77e66c98ec8c45dd72deea6221d7baf72`  
		Last Modified: Thu, 11 Jan 2024 03:42:51 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129f3997c07b2c6bc8651e7b3438869b66434e3923449a7e2f30bf1cfed28c45`  
		Last Modified: Thu, 11 Jan 2024 03:42:52 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33464f9b0b5797a1cfde2b2ce11d8ed7e17ee9d24d17792cf62f2de8a8c4a0f7`  
		Last Modified: Thu, 11 Jan 2024 03:42:52 GMT  
		Size: 1.4 MB (1386414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50990180c915d311a54f496310e0753d76dd14d088fe9b05d47400c760745ef5`  
		Last Modified: Thu, 11 Jan 2024 03:42:52 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:0d7981bef8bf2361b992c03944af49559feb6f1483857730bc591a347ade0ce8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94348790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2479ca7adf9fd616bce7217e56b4d5c0b27cf37dd02da980eb5695c3ef9c154`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:51 GMT
ADD file:8fb65cadfd211811589ee046d0fbd69d1fe11461b0c0c154a7650bf97307b857 in / 
# Thu, 11 Jan 2024 02:40:51 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:03:59 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jan 2024 06:04:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:04:19 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 11 Jan 2024 06:04:33 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 11 Jan 2024 06:04:34 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 11 Jan 2024 06:04:34 GMT
WORKDIR /var/www/html
# Thu, 11 Jan 2024 06:04:34 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 11 Jan 2024 06:04:34 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 11 Jan 2024 06:04:34 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 11 Jan 2024 06:04:34 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 11 Jan 2024 06:04:44 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 06:04:44 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 11 Jan 2024 06:04:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 11 Jan 2024 06:04:44 GMT
USER adminer
# Thu, 11 Jan 2024 06:04:44 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:cf83973c4a096cce9f37c421ad6f19cf1ebf7ae4d8ea98dac4913bd2aef08d1c`  
		Last Modified: Thu, 11 Jan 2024 02:44:25 GMT  
		Size: 53.7 MB (53707847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f269d1e13e8a9cceac6262c568deaabac15aa36ba54b79a081c8b8c71d2df6a6`  
		Last Modified: Thu, 11 Jan 2024 06:05:01 GMT  
		Size: 39.2 MB (39247707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:771fefea0ccd9d09a0bea66cad41f8e2baac7b16d6fc8bc39ca32a0807e9e3ac`  
		Last Modified: Thu, 11 Jan 2024 06:04:54 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb49879cdda1781e46db9c28b40e320b69b3020eccedf42bb1f6b5dc72faa46`  
		Last Modified: Thu, 11 Jan 2024 06:05:17 GMT  
		Size: 2.7 KB (2706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28fc5f60578708cc360e10338b3658ef523f69c8e6ebd9a09a73a3ddf7b80245`  
		Last Modified: Thu, 11 Jan 2024 06:05:17 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f66e04104d703660eb02d32cc3904bb18ae29fa18344272e255bd1f985bb4f`  
		Last Modified: Thu, 11 Jan 2024 06:05:17 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d6c062a648c769aab7f106669dee841a2080d1d92766f8e8ad9ed2a814604b`  
		Last Modified: Thu, 11 Jan 2024 06:05:18 GMT  
		Size: 1.4 MB (1386300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91dc93ad63d16daa0c1616fd4672614bebbc906048f2f40b918430983733a12a`  
		Last Modified: Thu, 11 Jan 2024 06:05:17 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:822d1fd3d6cccc8b10c800a59053516d7fe65879f08388e4dcbcb9d000a38603
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (97001798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da28c6c8ddd5d252654efc285d64462600e0f7ed9016dcd4feb8fe26078a72ce`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:50 GMT
ADD file:5ec37a8451203256eba8b114f21ff297f9b2e0b420ec7f0c50658a448ffc8f7b in / 
# Thu, 11 Jan 2024 02:38:51 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:05:44 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jan 2024 03:06:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:06:18 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 11 Jan 2024 03:06:42 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 11 Jan 2024 03:06:43 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 11 Jan 2024 03:06:43 GMT
WORKDIR /var/www/html
# Thu, 11 Jan 2024 03:06:43 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 11 Jan 2024 03:06:43 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 11 Jan 2024 03:06:43 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 11 Jan 2024 03:06:44 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 11 Jan 2024 03:06:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 03:06:58 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 11 Jan 2024 03:06:58 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 11 Jan 2024 03:06:58 GMT
USER adminer
# Thu, 11 Jan 2024 03:06:58 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:9b04188f89c4a7eaa549c59c16834ec81012244afac6c52196bafd2cd4486602`  
		Last Modified: Thu, 11 Jan 2024 02:43:42 GMT  
		Size: 56.0 MB (56046385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:557ba77a2179e833f238a36ff27c3977536c4e63ab00529f4e1a0cb24c302f6d`  
		Last Modified: Thu, 11 Jan 2024 03:07:21 GMT  
		Size: 39.6 MB (39562156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b430d827cfd080a15f4193e049c9ad09e7466e43e39f8aceb2cf0c24b34e2f6`  
		Last Modified: Thu, 11 Jan 2024 03:07:10 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad22c3e37ac2ac679ddb7524d636470595f4addb50a3a6cf1d6748997ba33e24`  
		Last Modified: Thu, 11 Jan 2024 03:07:39 GMT  
		Size: 2.7 KB (2708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69cb852bf1bf40d6c675011c0dd9794e3397c512678d4368d3e02ff0b631c73`  
		Last Modified: Thu, 11 Jan 2024 03:07:39 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c25244273439f085a234d49ce3ae41f17def49d603abcedd1ce2fce2418ffae3`  
		Last Modified: Thu, 11 Jan 2024 03:07:39 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35caa8d081928bc490d4393dd5bf7756163d704e6471084f8d826cdd5454f653`  
		Last Modified: Thu, 11 Jan 2024 03:07:40 GMT  
		Size: 1.4 MB (1386324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7d2bc93aec35dbc49fcfc41bbd09f6e73f78302a524f9db5ed862758afd912`  
		Last Modified: Thu, 11 Jan 2024 03:07:39 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; mips64le

```console
$ docker pull adminer@sha256:fbea597e10ec834d856f9fab16036fc72d02683ddd41ccb7a727bb9fcdcf0bc1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92636895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b606ebfbb73b849e86eb6c28bb434647dc14dfd2ead832a23b3f8e40cce483`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 11 Jan 2024 02:12:20 GMT
ADD file:624f588d8cd5ac8189fd789968263b87196e86dd1d90debb6c5261b515ce80a4 in / 
# Thu, 11 Jan 2024 02:12:26 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:38:49 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jan 2024 03:40:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:40:50 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 11 Jan 2024 03:42:36 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 11 Jan 2024 03:42:43 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 11 Jan 2024 03:42:46 GMT
WORKDIR /var/www/html
# Thu, 11 Jan 2024 03:42:50 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 11 Jan 2024 03:42:53 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 11 Jan 2024 03:42:56 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 11 Jan 2024 03:43:00 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 11 Jan 2024 03:43:52 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 03:43:56 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 11 Jan 2024 03:43:59 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 11 Jan 2024 03:44:02 GMT
USER adminer
# Thu, 11 Jan 2024 03:44:06 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:80f37a7fb2daee9d24c2a15489b4104fd20747297db13799a90f5f67e3a79154`  
		Last Modified: Thu, 11 Jan 2024 02:23:35 GMT  
		Size: 53.3 MB (53288875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a45f60bd06d99fdc86e166c6ec488d71b6ec3ff0f31531ea23330ad67b5c66e`  
		Last Modified: Thu, 11 Jan 2024 03:44:50 GMT  
		Size: 38.0 MB (37954063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874d6b2ddf770f9b8fe5901b87f5f358fb0c3d1d99c06bd073658ca884ba4ec5`  
		Last Modified: Thu, 11 Jan 2024 03:44:23 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c639cc8f8989c039ca520477309a78629c7a30dd27d5d752119adbf19d90155`  
		Last Modified: Thu, 11 Jan 2024 03:45:11 GMT  
		Size: 2.7 KB (2713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0359ebd1a69e48f0f2a37e319376e8a1075bb1e7a7b7c867ecad4574083af25b`  
		Last Modified: Thu, 11 Jan 2024 03:45:11 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0c1cdcdcb872a58a47874d775455e8c2fff3c8758368c060689e098c586a6c`  
		Last Modified: Thu, 11 Jan 2024 03:45:11 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0e125fb6c2ab0e456cb0c276f3a41570145d4de918d679feb48df217b9db0d`  
		Last Modified: Thu, 11 Jan 2024 03:45:12 GMT  
		Size: 1.4 MB (1387148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f73fcaccba401ec2261bc5eb58d8eaefc2188bc6a4d3215fd74c2ce9264f39`  
		Last Modified: Thu, 11 Jan 2024 03:45:11 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:7103727e5003a136890eb32159f265de5dda9148ed2ba76fd724db1698a737fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101268132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea55041d97ec9d84436ab7029aa47364b4793d5c05bad1df145c49fa1adfd904`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 11 Jan 2024 02:34:41 GMT
ADD file:cb900134161e1d051fb57c4a488efa9478959953f2773baa8a90b13198589a81 in / 
# Thu, 11 Jan 2024 02:34:45 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:26:59 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jan 2024 03:27:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:27:57 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 11 Jan 2024 03:28:40 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 11 Jan 2024 03:28:45 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 11 Jan 2024 03:28:46 GMT
WORKDIR /var/www/html
# Thu, 11 Jan 2024 03:28:47 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 11 Jan 2024 03:28:48 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 11 Jan 2024 03:28:48 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 11 Jan 2024 03:28:49 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 11 Jan 2024 03:29:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 03:29:18 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 11 Jan 2024 03:29:19 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 11 Jan 2024 03:29:21 GMT
USER adminer
# Thu, 11 Jan 2024 03:29:21 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:1b9340c192fedc0211d4cda28f7a01e9ff3be108c42783e576f4a366c373f30b`  
		Last Modified: Thu, 11 Jan 2024 02:39:48 GMT  
		Size: 58.9 MB (58929662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1e18ece4f9364199efeacabb85ac129470bd1fa02cfd4b2ab48ff7254ce79f`  
		Last Modified: Thu, 11 Jan 2024 03:29:44 GMT  
		Size: 40.9 MB (40945077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053655d07d22b020905527282024ef91938650ca6ab5f7897bdb8f2f928887ce`  
		Last Modified: Thu, 11 Jan 2024 03:29:35 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce52f4d275ce5a8f47c31ca862041fb5d5e079abfb49f755e7d7220a8661b200`  
		Last Modified: Thu, 11 Jan 2024 03:30:05 GMT  
		Size: 2.7 KB (2713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e168130eccf362640c8ff5c3c0ec842c94737b3f6dcd9779c9f62ca49ee8a25`  
		Last Modified: Thu, 11 Jan 2024 03:30:05 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d624880a4043b3472f5945b20315c5ef5a3f8ad0b895110e987f99c54d933d0`  
		Last Modified: Thu, 11 Jan 2024 03:30:05 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739d3977f9d33aa962b7a675d0b922380a301ece0b6f4d5cd1faad55820ba74b`  
		Last Modified: Thu, 11 Jan 2024 03:30:05 GMT  
		Size: 1.4 MB (1386443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e3c6adacec3368238e45172d21cb168fa9c63ec0197cdd0ed41cedf835c53b`  
		Last Modified: Thu, 11 Jan 2024 03:30:05 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; s390x

```console
$ docker pull adminer@sha256:9b2edb3d42f0197697d0fb25279d4b51cb9f312deff418f78785a810affc6cea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93711772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a598a4c397b82defb0e17455996f9d1358d862e17774ecb4f5cb238e878a767f`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 11 Jan 2024 01:45:23 GMT
ADD file:9ddcb5238e539e3b1fd8032aecf5e40f0b8b8162e6d045fcd58520db01e93296 in / 
# Thu, 11 Jan 2024 01:45:28 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 05:11:26 GMT
STOPSIGNAL SIGINT
# Thu, 11 Jan 2024 05:11:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 05:11:53 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 11 Jan 2024 05:12:18 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 11 Jan 2024 05:12:19 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 11 Jan 2024 05:12:20 GMT
WORKDIR /var/www/html
# Thu, 11 Jan 2024 05:12:20 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 11 Jan 2024 05:12:20 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 11 Jan 2024 05:12:21 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 11 Jan 2024 05:12:21 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 11 Jan 2024 05:12:31 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 05:12:31 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 11 Jan 2024 05:12:31 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 11 Jan 2024 05:12:32 GMT
USER adminer
# Thu, 11 Jan 2024 05:12:32 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:a1442bb0c8abfd050e8bdb2270126c2f24402a8c57a00f8229c40c2a35253665`  
		Last Modified: Thu, 11 Jan 2024 01:51:04 GMT  
		Size: 53.3 MB (53296125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c8d324b28795303c67c725b39143680fbca822ca5f0345dc958ff36e82b5d9`  
		Last Modified: Thu, 11 Jan 2024 05:12:53 GMT  
		Size: 39.0 MB (39022243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40537cf8343759ee3cffdfd506cc3b7636605e1031c5bbc9e2aef1b261188887`  
		Last Modified: Thu, 11 Jan 2024 05:12:47 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c3f6eb6dc37fb28619d4f5141c59ec1c608278ba352c7bfe2bb8edbcdb60aa`  
		Last Modified: Thu, 11 Jan 2024 05:13:03 GMT  
		Size: 2.7 KB (2707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160c24f82dd7d641055647f4198626af068a257d5b7aae730e535ba3c2901ced`  
		Last Modified: Thu, 11 Jan 2024 05:13:03 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da0c39c41099ecc051a629510b3ade0b0f6849bc1d21070f6b44fe3be34f3d8`  
		Last Modified: Thu, 11 Jan 2024 05:13:03 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdaebbfb2dde205d6cbcedc7ee804f77d09779143aafe0862faa8c13cc71b6ad`  
		Last Modified: Thu, 11 Jan 2024 05:13:03 GMT  
		Size: 1.4 MB (1386460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b7d889345ac0bd0de31d1fdbe0a913f62ad16bc8d9b6cb949b7cce3b8978ed`  
		Last Modified: Thu, 11 Jan 2024 05:13:02 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
