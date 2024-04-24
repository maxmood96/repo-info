## `adminer:4-standalone`

```console
$ docker pull adminer@sha256:4d06c61fbc5f21e83e3aebf15912736e4730a814b03adc1063dd1fc9cd22e58d
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

### `adminer:4-standalone` - linux; amd64

```console
$ docker pull adminer@sha256:eb8020baa66fe590a67eaa37941d57217cc3fe93db1089037c558ec1be1aff3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95980367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e16da0864c3225e8df7016b289f8b27cb3676f738b7dc303cc5e4fb5aa2457b`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Wed, 24 Apr 2024 07:56:09 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 24 Apr 2024 07:56:09 GMT
WORKDIR /var/www/html
# Wed, 24 Apr 2024 07:56:09 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 24 Apr 2024 07:56:09 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 24 Apr 2024 07:56:09 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 24 Apr 2024 07:56:09 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 24 Apr 2024 07:56:20 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 07:56:20 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 24 Apr 2024 07:56:21 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 24 Apr 2024 07:56:21 GMT
USER adminer
# Wed, 24 Apr 2024 07:56:21 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 24 Apr 2024 07:56:21 GMT
EXPOSE 8080
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
	-	`sha256:b3c4bd29e32f9b05cf30cf13c82d332bb2e5b30c708140248940fad31b685535`  
		Last Modified: Wed, 24 Apr 2024 07:56:53 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6fbcee71d95a54005cf7a4e246dbc9b2f0f58aa2ba365c338170bb6f3a0e02`  
		Last Modified: Wed, 24 Apr 2024 07:56:53 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b2bdfb64e389551b443437628b466d5898aeeb945f41e96d6c2111e187a46c`  
		Last Modified: Wed, 24 Apr 2024 07:56:54 GMT  
		Size: 1.4 MB (1386325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0baf3fbae6a5537e38e31a506b17d0ce4fc9c2c0eb82ed99294ce465fc589864`  
		Last Modified: Wed, 24 Apr 2024 07:56:53 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; arm variant v5

```console
$ docker pull adminer@sha256:a08d43fdaf6fa938d0f9652bc6df715fdb8d188708a2ca857fc03d1a3142d23e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91242769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa296da4d66f5fe91b7c28e79598ba96b5e01341cf47fa4f5c78fefb4bc6a8f3`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Wed, 24 Apr 2024 04:33:58 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 24 Apr 2024 04:33:58 GMT
WORKDIR /var/www/html
# Wed, 24 Apr 2024 04:33:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 24 Apr 2024 04:33:59 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 24 Apr 2024 04:33:59 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 24 Apr 2024 04:33:59 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 24 Apr 2024 04:34:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 04:34:11 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 24 Apr 2024 04:34:12 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 24 Apr 2024 04:34:12 GMT
USER adminer
# Wed, 24 Apr 2024 04:34:12 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 24 Apr 2024 04:34:12 GMT
EXPOSE 8080
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
	-	`sha256:8f38ed6df596206df1d694355eda8c3c494a4cce3d5907bde92a51227bbd7f59`  
		Last Modified: Wed, 24 Apr 2024 04:34:41 GMT  
		Size: 1.9 KB (1869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba78c4713daaee1e46fe3576d72db656922889c2b8c473be73223a437dd0be3`  
		Last Modified: Wed, 24 Apr 2024 04:34:42 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6775f269619dc801e1f687dea9a5b3b65ca26e7402453157b3621eef264cb36`  
		Last Modified: Wed, 24 Apr 2024 04:34:42 GMT  
		Size: 1.4 MB (1386149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58eb440fedba98ba7fb5a3aa4742869bf769f136499e6e6e506c3648c320fdbe`  
		Last Modified: Wed, 24 Apr 2024 04:34:41 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:9f0a859c02a6aa50b36f5c5df386a17b5c39ba5569a19ce6b4c164276c69979a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87837315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c029ed7ab133c61681516644dc7db6b9f66ebc45ee3636ac684868c195ee74`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Wed, 24 Apr 2024 07:01:24 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 24 Apr 2024 07:01:24 GMT
WORKDIR /var/www/html
# Wed, 24 Apr 2024 07:01:25 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 24 Apr 2024 07:01:25 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 24 Apr 2024 07:01:25 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 24 Apr 2024 07:01:25 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 24 Apr 2024 07:01:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 07:01:43 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 24 Apr 2024 07:01:43 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 24 Apr 2024 07:01:43 GMT
USER adminer
# Wed, 24 Apr 2024 07:01:43 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 24 Apr 2024 07:01:44 GMT
EXPOSE 8080
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
	-	`sha256:3fff4f0eb4fca3b18d79c6cd0c0f079c515e815e0b4fab54caa19d71700dc3c8`  
		Last Modified: Wed, 24 Apr 2024 07:02:19 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc134556923b33eaaf6534a2eb75ce30d64cf45d3ff6b9e6c3f6cb2145e01ea1`  
		Last Modified: Wed, 24 Apr 2024 07:02:19 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b1b009ecf86f2c60f137ff7e3f10f96208cdc697a284eca13549fcbe520bc67`  
		Last Modified: Wed, 24 Apr 2024 07:02:19 GMT  
		Size: 1.4 MB (1386192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56afc1583c47756cc6117542309863c3856b4e859f9514a085dde46a47d651a5`  
		Last Modified: Wed, 24 Apr 2024 07:02:19 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:65c492b7edea4ccb9f47db94f4b07a8a7b57d19add4e695fcc3bca101e9802c5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94379496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec24f5f6b6ae418030aa2352574939bb750ec1738a4b1a4ab4548659bf8d11c2`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Wed, 24 Apr 2024 04:51:49 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 24 Apr 2024 04:51:49 GMT
WORKDIR /var/www/html
# Wed, 24 Apr 2024 04:51:49 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 24 Apr 2024 04:51:49 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 24 Apr 2024 04:51:49 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 24 Apr 2024 04:51:50 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 24 Apr 2024 04:51:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 04:51:59 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 24 Apr 2024 04:51:59 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 24 Apr 2024 04:51:59 GMT
USER adminer
# Wed, 24 Apr 2024 04:51:59 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 24 Apr 2024 04:51:59 GMT
EXPOSE 8080
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
	-	`sha256:7e56dc4de3330372164a385cd7e549403dfb36cf5c951ea36a87fb7e3bc3b150`  
		Last Modified: Wed, 24 Apr 2024 04:52:23 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5d227a484cedc57b41010d1a4110e0ec0a9618232b30d6b1f48a422ef673c3`  
		Last Modified: Wed, 24 Apr 2024 04:52:23 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bacac63d93d57b5bddb254dd3d7da0dbb2f424ca9bd8be1c3f4a1fec84ac974`  
		Last Modified: Wed, 24 Apr 2024 04:52:24 GMT  
		Size: 1.4 MB (1386178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f6fe11dad426ef565a655533bfde9104b8fa53bd0d7764be57f18c1e5198e55`  
		Last Modified: Wed, 24 Apr 2024 04:52:23 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; 386

```console
$ docker pull adminer@sha256:7937040184340e4e34ff52ea95b29fe602a8e2f520197dc21cb53439d7144d48
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (97027736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3538137003a5917eee08fa6af449535409aee83b371ffdb810d507daf2341147`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Wed, 24 Apr 2024 04:51:44 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 24 Apr 2024 04:51:44 GMT
WORKDIR /var/www/html
# Wed, 24 Apr 2024 04:51:45 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 24 Apr 2024 04:51:45 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 24 Apr 2024 04:51:45 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 24 Apr 2024 04:51:45 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 24 Apr 2024 04:51:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 04:51:59 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 24 Apr 2024 04:51:59 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 24 Apr 2024 04:51:59 GMT
USER adminer
# Wed, 24 Apr 2024 04:51:59 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 24 Apr 2024 04:51:59 GMT
EXPOSE 8080
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
	-	`sha256:93aa146675bb7932c5ef29a1edd009afe720b20e43e555f7ff87ec1143045780`  
		Last Modified: Wed, 24 Apr 2024 04:52:38 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06634a62cae404d22dcd953a02569763e520ed8f37cb17472827ae9c733bba83`  
		Last Modified: Wed, 24 Apr 2024 04:52:37 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:490dda3582e884bf1bbe900625947764daa5e6c743f4c5c7199436daa63fc597`  
		Last Modified: Wed, 24 Apr 2024 04:52:38 GMT  
		Size: 1.4 MB (1386115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46ac19e3184a3f2eeb05d69db95b63d50fb22bb8607da76a109ffc34276036d`  
		Last Modified: Wed, 24 Apr 2024 04:52:37 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; mips64le

```console
$ docker pull adminer@sha256:de263a394a6dbcdc2f65e0232b230314693e0fcc24356d8ce43631bcc51d2a94
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92669440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:514c8c8e2d2113a3a8af960a7cbf0f81de2d3a036479cb7b277855f1029407ef`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Wed, 24 Apr 2024 10:45:53 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 24 Apr 2024 10:45:56 GMT
WORKDIR /var/www/html
# Wed, 24 Apr 2024 10:45:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 24 Apr 2024 10:46:03 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 24 Apr 2024 10:46:06 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 24 Apr 2024 10:46:09 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 24 Apr 2024 10:47:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 10:47:03 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 24 Apr 2024 10:47:06 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 24 Apr 2024 10:47:09 GMT
USER adminer
# Wed, 24 Apr 2024 10:47:13 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 24 Apr 2024 10:47:16 GMT
EXPOSE 8080
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
	-	`sha256:90843704d81a4158b5753eb611b04d65bd0da2f6dcd27681ddd9683fac9f1f8b`  
		Last Modified: Wed, 24 Apr 2024 10:49:24 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bdb59770b069a31e703580bfa996edd4f09a0287acdfc15ec93799431781f5`  
		Last Modified: Wed, 24 Apr 2024 10:49:24 GMT  
		Size: 1.5 KB (1483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729565a2e7b366bde6db907f4738a598d19c977353ee5446df738cc84664cf71`  
		Last Modified: Wed, 24 Apr 2024 10:49:24 GMT  
		Size: 1.4 MB (1387104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d43f743ffe13ca4ed269893e7fe38cdfd979ef65f4edea4222135a5fe98ad08`  
		Last Modified: Wed, 24 Apr 2024 10:49:24 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:98c1678ca56a7a108e5dd18ab15fb74a03950447242f7d1cf8dbbd277f78399e
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101305626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f7222806d91955d715cfdca56fd214037e54a1d66871c54dcf9db3aee51a8fe`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Wed, 24 Apr 2024 05:38:12 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 24 Apr 2024 05:38:12 GMT
WORKDIR /var/www/html
# Wed, 24 Apr 2024 05:38:12 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 24 Apr 2024 05:38:13 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 24 Apr 2024 05:38:13 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 24 Apr 2024 05:38:14 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 24 Apr 2024 05:38:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 05:38:42 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 24 Apr 2024 05:38:43 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 24 Apr 2024 05:38:43 GMT
USER adminer
# Wed, 24 Apr 2024 05:38:43 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 24 Apr 2024 05:38:44 GMT
EXPOSE 8080
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
	-	`sha256:cb483e7b94c67c76a17aee97e3ead97f8434db3e05989e33f8a28dae02daa480`  
		Last Modified: Wed, 24 Apr 2024 05:39:35 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f406bfa73e28ad00180e4488fa238c7955f181998e4dcb157a91c78f0d38f05`  
		Last Modified: Wed, 24 Apr 2024 05:39:35 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888d38e64e1cc60562a01ad1c418c39ecae87cdd151faf98b669a612be6be994`  
		Last Modified: Wed, 24 Apr 2024 05:39:36 GMT  
		Size: 1.4 MB (1386341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baff760ea9f21a15c767a27a0cdc4782e96ae19d2e007be71c164e0e66a4a2fc`  
		Last Modified: Wed, 24 Apr 2024 05:39:35 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; s390x

```console
$ docker pull adminer@sha256:6bfa712fd79a88d24cbf5105ef09c55f806198a096484561bfcf82bb3492e19b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.8 MB (93755756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd165c5c486ad0e2c49d5638a737b8e83806e63df88f5ad4b82cfd5b3b6a352b`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Wed, 24 Apr 2024 04:08:43 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 24 Apr 2024 04:08:43 GMT
WORKDIR /var/www/html
# Wed, 24 Apr 2024 04:08:43 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 24 Apr 2024 04:08:43 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 24 Apr 2024 04:08:43 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 24 Apr 2024 04:08:44 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 24 Apr 2024 04:08:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 24 Apr 2024 04:08:57 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 24 Apr 2024 04:08:57 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 24 Apr 2024 04:08:57 GMT
USER adminer
# Wed, 24 Apr 2024 04:08:57 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 24 Apr 2024 04:08:57 GMT
EXPOSE 8080
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
	-	`sha256:1ef444734c61876ce6e1db265eec6730b5dca1d5562748840aef0fb3bbbd73d2`  
		Last Modified: Wed, 24 Apr 2024 04:09:39 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2671fdba1961aa190de0a6b706111a770e93665d419815ac63ba74c501324d1`  
		Last Modified: Wed, 24 Apr 2024 04:09:38 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9480b43f624068235064ecceed0267e7a5f273046882c75a085192c4c6b52015`  
		Last Modified: Wed, 24 Apr 2024 04:09:39 GMT  
		Size: 1.4 MB (1386246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45cd984bd37fda0dbdf0e2fd76e910d19cfcfba9c3ed7b630c26196c69f3892`  
		Last Modified: Wed, 24 Apr 2024 04:09:38 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
