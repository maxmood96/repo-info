<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `adminer`

-	[`adminer:4`](#adminer4)
-	[`adminer:4-fastcgi`](#adminer4-fastcgi)
-	[`adminer:4-standalone`](#adminer4-standalone)
-	[`adminer:4.8.1`](#adminer481)
-	[`adminer:4.8.1-fastcgi`](#adminer481-fastcgi)
-	[`adminer:4.8.1-standalone`](#adminer481-standalone)
-	[`adminer:fastcgi`](#adminerfastcgi)
-	[`adminer:latest`](#adminerlatest)
-	[`adminer:standalone`](#adminerstandalone)

## `adminer:4`

```console
$ docker pull adminer@sha256:4203fd6bcd82fe25dceaf8acb4826129cf7a6e93b22a5ab2fc0ec5a7cdaca3f4
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

### `adminer:4` - linux; amd64

```console
$ docker pull adminer@sha256:b5570962c3a9981b6572e61dd33f5cbd394a1a9d27ee6342b4241338af330449
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95921691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e1b3241b20061365693574e1c1241f64a48b15a7f439b8df760456d83009c7`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:15 GMT
ADD file:459d1e92eb8c24ff4758f974d289ca8a2abe04cf50b6fe2bd760aa4589478289 in / 
# Thu, 23 Mar 2023 01:30:15 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 05:55:49 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 05:56:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 05:56:13 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 05:56:14 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 05:56:14 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 05:56:14 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 05:56:14 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 05:56:14 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 05:56:14 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 05:56:25 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 05:56:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 05:56:26 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 05:56:26 GMT
USER adminer
# Thu, 23 Mar 2023 05:56:26 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 05:56:26 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:3e440a7045683e27f8e2fa04000e0e078d8dfac0c971358ae0f8c65c13321c8e`  
		Last Modified: Thu, 23 Mar 2023 01:34:00 GMT  
		Size: 55.0 MB (55045608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6386bc062c6cf91f6c1451db68015d43a1afd7d67a8f0710050e557777a30a`  
		Last Modified: Thu, 23 Mar 2023 05:57:00 GMT  
		Size: 39.5 MB (39486568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dbc633dab938fa31a0afdfe3ac449318f04eb42e13b59c2602178aed2af127e`  
		Last Modified: Thu, 23 Mar 2023 05:56:53 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39317196bba2d873b239492ba23f8f1d62f89b661fb1760b65f29b1404322c60`  
		Last Modified: Thu, 23 Mar 2023 05:56:53 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ea8e1da1f9854a8c3bf43a78f5b403bdfad3f2c2861edfbfd902566950a7a2`  
		Last Modified: Thu, 23 Mar 2023 05:56:53 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ce0ac056362cd982a31febaaf97daa568c31c2e95f1f4265e82cc6fbeaffd4`  
		Last Modified: Thu, 23 Mar 2023 05:56:53 GMT  
		Size: 1.4 MB (1385271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3ee3b23021de0471ff83e0b10babf764acf8f57dbb17c2eef966f084eb314a`  
		Last Modified: Thu, 23 Mar 2023 05:56:53 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; arm variant v5

```console
$ docker pull adminer@sha256:4344599d09a3a9134c3a42f59ad31606dd3e8952bb9ae5d72d64dc5297cdc6bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91184910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512e73052fee795753bdd64cababc1bcc5ccdc4ce7ae0391a67a4013d1b98432`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 00:48:37 GMT
ADD file:8419f4bee11379b8aa511da1fe7cdcd6b2cb8c252bc90f76dec672a5b802ea27 in / 
# Thu, 23 Mar 2023 00:48:37 GMT
CMD ["bash"]
# Sat, 25 Mar 2023 02:48:49 GMT
STOPSIGNAL SIGINT
# Sat, 25 Mar 2023 02:49:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Sat, 25 Mar 2023 02:49:17 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Sat, 25 Mar 2023 02:49:17 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 25 Mar 2023 02:49:17 GMT
WORKDIR /var/www/html
# Sat, 25 Mar 2023 02:49:18 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 25 Mar 2023 02:49:18 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 25 Mar 2023 02:49:18 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 25 Mar 2023 02:49:18 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Sat, 25 Mar 2023 02:49:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 25 Mar 2023 02:49:30 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 25 Mar 2023 02:49:30 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 25 Mar 2023 02:49:30 GMT
USER adminer
# Sat, 25 Mar 2023 02:49:30 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 25 Mar 2023 02:49:30 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:9a8ea6c28ff9e1b5a437e1e5b168873207139672ec8d755939cad00b23349e22`  
		Last Modified: Thu, 23 Mar 2023 02:21:35 GMT  
		Size: 52.5 MB (52549555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeab9bc611f5a84450bb374d38da4707075933d49bf1f7653fd834777749923e`  
		Last Modified: Sat, 25 Mar 2023 02:50:47 GMT  
		Size: 37.2 MB (37246063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e679cbf63988e1866986ea77804721769a09f59bdef7a89368f93a3abd2409`  
		Last Modified: Sat, 25 Mar 2023 02:50:39 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7959eefb479c10f4ab8829bcc4ee81ce479a5bff4f3d776e2d684522e56d36c`  
		Last Modified: Sat, 25 Mar 2023 02:50:39 GMT  
		Size: 1.9 KB (1865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b261a380e55719d974d3c7d0d3816f93ba071f56ab2669b4e941c91a49aa11c9`  
		Last Modified: Sat, 25 Mar 2023 02:50:39 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f7d098a043908e9b0872735983e550db864960c2b9998a675db2c956a02a60`  
		Last Modified: Sat, 25 Mar 2023 02:50:39 GMT  
		Size: 1.4 MB (1385072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a8d1397cd986a98157defb67fbca51bfe84b0d994ad3b7e2199a9d4adb3bf5`  
		Last Modified: Sat, 25 Mar 2023 02:50:39 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; arm variant v7

```console
$ docker pull adminer@sha256:208e28dc00b696fd2786ae0fac00bbac135df7d327a78f1a3b07b430e8be29fa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87782361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924e553786350523e3dabd52a79ebaa532e1ee1f1cd4f55c123b6f2debfd887b`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 01:13:21 GMT
ADD file:fa1cbfdd44274e571cabd5ca7fafa08b17c6f497ecfca6368a9eec4d2527a364 in / 
# Thu, 23 Mar 2023 01:13:22 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 13:53:52 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 13:54:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 13:54:17 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 13:54:17 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 13:54:18 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 13:54:18 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 13:54:18 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 13:54:18 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 13:54:18 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 13:54:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 13:54:30 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 13:54:30 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 13:54:30 GMT
USER adminer
# Thu, 23 Mar 2023 13:54:30 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 13:54:30 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:d50e868f9a626a3c456c0c52c3b013e87619bbac7798ac0c2acf2a2407303125`  
		Last Modified: Thu, 23 Mar 2023 01:33:00 GMT  
		Size: 50.2 MB (50211788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750746172b8a677cb809244c17155d7b05d643b2d816de3d8090ff3593de19ea`  
		Last Modified: Thu, 23 Mar 2023 13:55:03 GMT  
		Size: 36.2 MB (36181275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79543298adbabe76f964cc3578ae398897a0bc10ee8ebf4a0a3338a8ee26b6e8`  
		Last Modified: Thu, 23 Mar 2023 13:54:55 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7b7c098bbce560d98941c87164725c63999c701f19f2500e91578c8d994c8f`  
		Last Modified: Thu, 23 Mar 2023 13:54:56 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90441e257dd07454f7d03e5aa41e80d43c14256ff5040356a29d4639b23d75fc`  
		Last Modified: Thu, 23 Mar 2023 13:54:55 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65767342491a731ec4afa7560fd1b162f1ea5c932fc69e8326baad4bec228e7e`  
		Last Modified: Thu, 23 Mar 2023 13:54:56 GMT  
		Size: 1.4 MB (1385066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a8450e329b8116e25e9fa7cb6b678d57084c5946b3167f2cb126880295263a`  
		Last Modified: Thu, 23 Mar 2023 13:54:55 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:7fe9245eaab6579d2f02b2c43ece653c6f014f78be767a77580df6401023b8b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94334964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da1ba2cdb7c1dcd745eda1a855a3c5d0cc50e77182d900a1a13fab7ecb94f0f1`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:02 GMT
ADD file:70d18f9eea4e4fbdb941e66490ccb7233e182fe7ded1185de91c7d55580dd13e in / 
# Thu, 23 Mar 2023 00:45:02 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:50:38 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 06:50:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 06:50:57 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 06:50:57 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 06:50:58 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 06:50:58 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 06:50:58 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 06:50:58 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 06:50:58 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 06:51:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 06:51:08 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 06:51:08 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 06:51:08 GMT
USER adminer
# Thu, 23 Mar 2023 06:51:08 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 06:51:08 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:8022b074731d9ecee7f4fba79b993920973811dda168bbc08636f18523b90122`  
		Last Modified: Thu, 23 Mar 2023 00:47:46 GMT  
		Size: 53.7 MB (53703099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98305094c7fd13042b057082ec8d7bcc2b6f08cf0bba01a567b6bc108039bdf1`  
		Last Modified: Thu, 23 Mar 2023 06:51:37 GMT  
		Size: 39.2 MB (39242570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbbb9ddd2e012fdf94f2222f96fe1f8514ec4285c8acff371dd027ca67043c8`  
		Last Modified: Thu, 23 Mar 2023 06:51:30 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b3fa21b5eaa269a0e522ee6faa17c1942a9eb531a85d65093c785db3bf4ca32`  
		Last Modified: Thu, 23 Mar 2023 06:51:30 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbcc9aba89fb8cb163ab7c6f00eaee21df2f499f9cfbb89de3b18e5f24ba0087`  
		Last Modified: Thu, 23 Mar 2023 06:51:30 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf77c8ff22b40bbe616794e9d54103a4a9648107d69c9057deb1a83342d3d58`  
		Last Modified: Thu, 23 Mar 2023 06:51:31 GMT  
		Size: 1.4 MB (1385053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bd969a23b87a5402679ff8373fd3e9ce7af9a3e999bad556fe0cc25dda1cc6`  
		Last Modified: Thu, 23 Mar 2023 06:51:30 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; 386

```console
$ docker pull adminer@sha256:ca2ee65836fd06aba737873c17718cd1ae4e52f6ba9a2869000be6794922ec0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96975396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47306ce39706e8ed333600b8d4399cb09c02ffe4e169f76bd59fa5b6569ae778`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 00:39:08 GMT
ADD file:f331251c4c21fceff56d13f76442a6334dc355c29ec7450768c1c86a3db1adab in / 
# Thu, 23 Mar 2023 00:39:09 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 21:17:12 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 21:17:40 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 21:17:41 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 21:17:41 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 21:17:41 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 21:17:42 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 21:17:42 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 21:17:42 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 21:17:42 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 21:17:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 21:17:54 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 21:17:54 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 21:17:54 GMT
USER adminer
# Thu, 23 Mar 2023 21:17:55 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 21:17:55 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:c1bb878cff31d37952c5c73ed15c167f599bb7f97b3eeaa1a17352b2473b3394`  
		Last Modified: Thu, 23 Mar 2023 00:42:44 GMT  
		Size: 56.0 MB (56027911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67239d163b3f7b443f91919b613775ed043520e6b06b413a9628905d01e98992`  
		Last Modified: Thu, 23 Mar 2023 21:18:34 GMT  
		Size: 39.6 MB (39558048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88061812377dcf7351518633da4694430dfe02ac13bdbc48516d26c18586a0d5`  
		Last Modified: Thu, 23 Mar 2023 21:18:24 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c664bb8231af50f8a98b457a9e7c291444345b0066ed54ddbcc0b2129859965`  
		Last Modified: Thu, 23 Mar 2023 21:18:24 GMT  
		Size: 1.9 KB (1869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a209358917bcf344993c93aad3b156d6a09b6ab64d43df3941ca51e6c414b9`  
		Last Modified: Thu, 23 Mar 2023 21:18:24 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061ad9c8d5ae0dc7e0d69094e0f6d09b29dea00ec113641833b5a37f404de058`  
		Last Modified: Thu, 23 Mar 2023 21:18:24 GMT  
		Size: 1.4 MB (1385210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2761eeb066c4b63e66ada920b87fc430284439f4c76fac14a274ef528430d3f`  
		Last Modified: Thu, 23 Mar 2023 21:18:24 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; mips64le

```console
$ docker pull adminer@sha256:14de06501f131ba9f62a814f592d766d6f050b30eab65a15bb1e753a436aab3d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92605785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddae0bdce53fcfedd28644c8fc0df52f38f44000615def4d84b2c88db2aff3ab`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 05:17:18 GMT
ADD file:2337efa705c8772705fa8519e513f4299e72c9eb63e3a68069778ca95a1511e6 in / 
# Thu, 23 Mar 2023 05:17:24 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 20:06:00 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 20:07:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 20:08:02 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 20:08:09 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 20:08:13 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 20:08:16 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 20:08:19 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 20:08:22 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 20:08:26 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 20:09:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 20:09:20 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 20:09:24 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 20:09:27 GMT
USER adminer
# Thu, 23 Mar 2023 20:09:31 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 20:09:34 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:f3951ee58695b4d906b37f2d9a07e6158f66a7328d0c70445d9607cd8367ede0`  
		Last Modified: Thu, 23 Mar 2023 05:25:08 GMT  
		Size: 53.3 MB (53264720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1180d0aa65a6936ad9b336fd7ddf64160d0a95203d7f3d82027fe8912c936d73`  
		Last Modified: Thu, 23 Mar 2023 20:11:59 GMT  
		Size: 38.0 MB (37950695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a23105a66b5d86b4852f9dcf6753d154e1d5b3b76c178cf8baced410a4deb2`  
		Last Modified: Thu, 23 Mar 2023 20:11:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba90b5b3033a3d6ba607430a17c7e37f0fae8f0664ac81a4e571e9ad9fca9e2`  
		Last Modified: Thu, 23 Mar 2023 20:11:33 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b1980d6708cacd2f28ca074bd917c1143a47040b425da5985915850214f197f`  
		Last Modified: Thu, 23 Mar 2023 20:11:33 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfbeda1e7451034cf22503ff221351a0d3f5e1f63a6f11dc71a81450a7aaadd`  
		Last Modified: Thu, 23 Mar 2023 20:11:34 GMT  
		Size: 1.4 MB (1386264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b87439fd13726c64bed775edf40ceb3cbc1b5dbf3f62fb9b127024394aaece4`  
		Last Modified: Thu, 23 Mar 2023 20:11:33 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; ppc64le

```console
$ docker pull adminer@sha256:ddf406bedb6ea27fd15da89331e085e564dcde0c98ba31f3914b14b4483aa56e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101249875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8b45276387b274e6256e8c13851f3460fdd98b29ca47a09f04a8fad8d02090`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 01:19:25 GMT
ADD file:3eb86af6fda22c3e84548a6d0039be04819ce464b2700e8d8c140be49530ff7c in / 
# Thu, 23 Mar 2023 01:19:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 12:41:38 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 12:42:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 12:42:59 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 12:43:01 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 12:43:01 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 12:43:01 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 12:43:02 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 12:43:02 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 12:43:03 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 12:43:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 12:43:33 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 12:43:33 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 12:43:34 GMT
USER adminer
# Thu, 23 Mar 2023 12:43:35 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 12:43:35 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:566bc84f2641b393ac5a2f4a2ca405c09943aa3ec679f38ea1588f6ee930219e`  
		Last Modified: Thu, 23 Mar 2023 01:23:52 GMT  
		Size: 58.9 MB (58921026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2fbb285bf85ccfbb4c5282ba9f10d09cecbc5a0bab31ef237b51b3201089c2`  
		Last Modified: Thu, 23 Mar 2023 12:45:00 GMT  
		Size: 40.9 MB (40939153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5c4d551007797e513e8983796e921a39828107b5d1309cb2783b12bc6aaac4`  
		Last Modified: Thu, 23 Mar 2023 12:44:46 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19dcdc4ed08a4d33d3c19d3c7a7fcb606bed16f514bbdf68d09ed75d0ef5a039`  
		Last Modified: Thu, 23 Mar 2023 12:44:47 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0187a4a30cb1c249de5010601f0912c92400f91482facb00198f8ba8e3691e`  
		Last Modified: Thu, 23 Mar 2023 12:44:46 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3867a61f6a3237b86e8a6bb431978b79ef5a1320ee3ebe58670b7a68f930c0f`  
		Last Modified: Thu, 23 Mar 2023 12:44:47 GMT  
		Size: 1.4 MB (1385455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553fdd9019949edcff0333970ef2dc5fa9af5479a21e08ecaf14a608524f497f`  
		Last Modified: Thu, 23 Mar 2023 12:44:46 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; s390x

```console
$ docker pull adminer@sha256:3a1427b2251efb24343fedded181036a73a9a9edd77c0241f1907db59654d4f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93684414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d7a2d888bb0da291a197f178923752e3a408b6b8002d6ae4d4c8595173ec84`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 00:43:50 GMT
ADD file:1111f9325245c8edccf2d9480c39cf2368f783ad86c2700d452be4e8cbebef8a in / 
# Thu, 23 Mar 2023 00:43:54 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:12:38 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 07:12:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 07:12:59 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 07:12:59 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 07:12:59 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 07:12:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 07:12:59 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 07:12:59 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 07:12:59 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 07:13:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 07:13:07 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 07:13:07 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 07:13:08 GMT
USER adminer
# Thu, 23 Mar 2023 07:13:08 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 07:13:08 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:00dac46cbc44f444bd1dffe5b00a1b239054295b96f7984793273e9d12e75591`  
		Last Modified: Thu, 23 Mar 2023 00:47:04 GMT  
		Size: 53.3 MB (53277499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef40e14df43903a504c3865251eb934e8f644d89890514fc292b06981fca7826`  
		Last Modified: Thu, 23 Mar 2023 07:13:44 GMT  
		Size: 39.0 MB (39017484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f79bdf3c2e58c635953d9f0329b1010a5ff99b977d98975e467b7ab57a155e`  
		Last Modified: Thu, 23 Mar 2023 07:13:37 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ebc836b2a414afb40c1d84fa4fe4af21828a8f07dcbbbfe020a9a2270b0c467`  
		Last Modified: Thu, 23 Mar 2023 07:13:37 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:395b8975dd5a57c4e6e30bccd71a2d34125566cbb50b6000d142e49fb27dc1ea`  
		Last Modified: Thu, 23 Mar 2023 07:13:37 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7cb7770c3999b7b71cb8bd67b1686854b1cf6a8fbd340c7da905fddae466c1`  
		Last Modified: Thu, 23 Mar 2023 07:13:37 GMT  
		Size: 1.4 MB (1385197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47125e4be7b760f757795627cf23bffd8efbadc93fd3f20e13ac58ddac7b2639`  
		Last Modified: Thu, 23 Mar 2023 07:13:37 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4-fastcgi`

```console
$ docker pull adminer@sha256:5deda468db781fc1cf37cd89932cca5e14d827305089725caae037d065f9eae9
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
$ docker pull adminer@sha256:35e5285bea82c78b08355dc314739f980e2437cbf1c9e51291b5168fd5cd6f75
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95924422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23fae11ad3f1ae58e8aa6d5af50bb131d52fd3b3fadbb2c8e22e67ceca7a76d7`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:15 GMT
ADD file:459d1e92eb8c24ff4758f974d289ca8a2abe04cf50b6fe2bd760aa4589478289 in / 
# Thu, 23 Mar 2023 01:30:15 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 05:55:49 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 05:56:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 05:56:13 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 05:56:30 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 23 Mar 2023 05:56:30 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 05:56:30 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 05:56:30 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 05:56:30 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 05:56:31 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 05:56:31 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 05:56:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 05:56:41 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 05:56:41 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 05:56:41 GMT
USER adminer
# Thu, 23 Mar 2023 05:56:42 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:3e440a7045683e27f8e2fa04000e0e078d8dfac0c971358ae0f8c65c13321c8e`  
		Last Modified: Thu, 23 Mar 2023 01:34:00 GMT  
		Size: 55.0 MB (55045608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6386bc062c6cf91f6c1451db68015d43a1afd7d67a8f0710050e557777a30a`  
		Last Modified: Thu, 23 Mar 2023 05:57:00 GMT  
		Size: 39.5 MB (39486568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dbc633dab938fa31a0afdfe3ac449318f04eb42e13b59c2602178aed2af127e`  
		Last Modified: Thu, 23 Mar 2023 05:56:53 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e43c5bb8d604942de8a801fbd515cde458e8296cda94b628a1a311281fe880`  
		Last Modified: Thu, 23 Mar 2023 05:57:17 GMT  
		Size: 2.7 KB (2712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991cbf4d6fdd0b401219e6f0c1474c3c379889e229e8305e5c7afc86459d6599`  
		Last Modified: Thu, 23 Mar 2023 05:57:16 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420cfe44d3089c8454b9568ad65803581ce9a8565536455cf2602d4b96ff6e35`  
		Last Modified: Thu, 23 Mar 2023 05:57:16 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad56f1c45901a03ae785f94f8dfc35d5689f400e95502fdf74ee2243dd5fd22`  
		Last Modified: Thu, 23 Mar 2023 05:57:17 GMT  
		Size: 1.4 MB (1385298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36974e24611dd62fec010effb08e11fdd389b0898bff3ee057b6bf9266aa3d8e`  
		Last Modified: Thu, 23 Mar 2023 05:57:16 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm variant v5

```console
$ docker pull adminer@sha256:83ad65624afb37bbccd0d59d7d82fc2814210821ac3b1f544cb057038e30a610
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91187641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd884953fb56ddec123031e25c1aef7a0add8ec9d119447de370a5aadc0e2166`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 23 Mar 2023 00:48:37 GMT
ADD file:8419f4bee11379b8aa511da1fe7cdcd6b2cb8c252bc90f76dec672a5b802ea27 in / 
# Thu, 23 Mar 2023 00:48:37 GMT
CMD ["bash"]
# Sat, 25 Mar 2023 02:48:49 GMT
STOPSIGNAL SIGINT
# Sat, 25 Mar 2023 02:49:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Sat, 25 Mar 2023 02:49:17 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Sat, 25 Mar 2023 02:49:47 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Sat, 25 Mar 2023 02:49:48 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 25 Mar 2023 02:49:48 GMT
WORKDIR /var/www/html
# Sat, 25 Mar 2023 02:49:48 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 25 Mar 2023 02:49:48 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 25 Mar 2023 02:49:48 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 25 Mar 2023 02:49:48 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Sat, 25 Mar 2023 02:50:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 25 Mar 2023 02:50:01 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 25 Mar 2023 02:50:01 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 25 Mar 2023 02:50:01 GMT
USER adminer
# Sat, 25 Mar 2023 02:50:01 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:9a8ea6c28ff9e1b5a437e1e5b168873207139672ec8d755939cad00b23349e22`  
		Last Modified: Thu, 23 Mar 2023 02:21:35 GMT  
		Size: 52.5 MB (52549555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeab9bc611f5a84450bb374d38da4707075933d49bf1f7653fd834777749923e`  
		Last Modified: Sat, 25 Mar 2023 02:50:47 GMT  
		Size: 37.2 MB (37246063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e679cbf63988e1866986ea77804721769a09f59bdef7a89368f93a3abd2409`  
		Last Modified: Sat, 25 Mar 2023 02:50:39 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a070ee59349bc1327cf753932c17cc9396004abaf993e6a56c9a2ef071b9d97`  
		Last Modified: Sat, 25 Mar 2023 02:51:03 GMT  
		Size: 2.7 KB (2709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39741322e4fc4e150bbe02d05ecb189f61fb32138b1a0a34a412390730e6b0a`  
		Last Modified: Sat, 25 Mar 2023 02:51:03 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b7e40e37ad3d10c54c47aac9a2000613f3fc90a30fe6b3166040b3b1d3416d`  
		Last Modified: Sat, 25 Mar 2023 02:51:03 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c99b025114fb17d7175738951a97689c171bbd82cd5177796b12d6d0424699`  
		Last Modified: Sat, 25 Mar 2023 02:51:03 GMT  
		Size: 1.4 MB (1385089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e4611882f0550bdfd18af6aa74746b7a16226506f8cc4951a3b6c05a61e999`  
		Last Modified: Sat, 25 Mar 2023 02:51:02 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:bc666796aa3d0cee0b13bc0afeb827eddb224ac94c2825e90be0b7935f4e8122
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87785110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8477e704cb362785d6fffb06bca6d401c7163028a20adb041de59c8927810ecc`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 23 Mar 2023 01:13:21 GMT
ADD file:fa1cbfdd44274e571cabd5ca7fafa08b17c6f497ecfca6368a9eec4d2527a364 in / 
# Thu, 23 Mar 2023 01:13:22 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 13:53:52 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 13:54:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 13:54:17 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 13:54:32 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 23 Mar 2023 13:54:33 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 13:54:33 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 13:54:33 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 13:54:33 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 13:54:33 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 13:54:33 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 13:54:44 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 13:54:44 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 13:54:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 13:54:44 GMT
USER adminer
# Thu, 23 Mar 2023 13:54:44 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:d50e868f9a626a3c456c0c52c3b013e87619bbac7798ac0c2acf2a2407303125`  
		Last Modified: Thu, 23 Mar 2023 01:33:00 GMT  
		Size: 50.2 MB (50211788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750746172b8a677cb809244c17155d7b05d643b2d816de3d8090ff3593de19ea`  
		Last Modified: Thu, 23 Mar 2023 13:55:03 GMT  
		Size: 36.2 MB (36181275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79543298adbabe76f964cc3578ae398897a0bc10ee8ebf4a0a3338a8ee26b6e8`  
		Last Modified: Thu, 23 Mar 2023 13:54:55 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31633dada050baeaf275a6f4e00621a9f3e3224c8045210053670913ba6d6585`  
		Last Modified: Thu, 23 Mar 2023 13:55:19 GMT  
		Size: 2.7 KB (2709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c21aec687480c0c87c1badd06ad8d1bc38a37d87223bc20a78ba010fd626cac`  
		Last Modified: Thu, 23 Mar 2023 13:55:19 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac9619b29c31046e1d85965461b5a590b86fb5f2f78c27167ec6cfca6f21651e`  
		Last Modified: Thu, 23 Mar 2023 13:55:19 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd30156b59e64f168057bb8a5fae751059636af01bb28f176af27932691211a`  
		Last Modified: Thu, 23 Mar 2023 13:55:20 GMT  
		Size: 1.4 MB (1385116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60631e91dd1890dcbae61adf6317c4a7be616954ef21fec67df71f340de0d351`  
		Last Modified: Thu, 23 Mar 2023 13:55:19 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:7596c184b40a20292868a7080a783453ddf723197fbd6e8c671d314d8b488e24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94337713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39cf91641fd4f5e8d3515aaa989cebc88d71589b000cc0c7a53339912cb8b5c`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:02 GMT
ADD file:70d18f9eea4e4fbdb941e66490ccb7233e182fe7ded1185de91c7d55580dd13e in / 
# Thu, 23 Mar 2023 00:45:02 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:50:38 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 06:50:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 06:50:57 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 06:51:11 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 23 Mar 2023 06:51:12 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 06:51:12 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 06:51:12 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 06:51:12 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 06:51:12 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 06:51:12 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 06:51:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 06:51:22 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 06:51:22 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 06:51:22 GMT
USER adminer
# Thu, 23 Mar 2023 06:51:22 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:8022b074731d9ecee7f4fba79b993920973811dda168bbc08636f18523b90122`  
		Last Modified: Thu, 23 Mar 2023 00:47:46 GMT  
		Size: 53.7 MB (53703099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98305094c7fd13042b057082ec8d7bcc2b6f08cf0bba01a567b6bc108039bdf1`  
		Last Modified: Thu, 23 Mar 2023 06:51:37 GMT  
		Size: 39.2 MB (39242570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbbb9ddd2e012fdf94f2222f96fe1f8514ec4285c8acff371dd027ca67043c8`  
		Last Modified: Thu, 23 Mar 2023 06:51:30 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed10fa53994213c7460cfbbec9c399e9d8cca8c2aec04202fedff5a70cf2889`  
		Last Modified: Thu, 23 Mar 2023 06:51:52 GMT  
		Size: 2.7 KB (2708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d7483fec2e916d9b95f32278191c4d548eaabe455a3f3ebc0fd94a93216b8f`  
		Last Modified: Thu, 23 Mar 2023 06:51:52 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8280d00d8418fda79bfb9d617fcbe8d8e10e3c43d208cbb6e3559b653a49557d`  
		Last Modified: Thu, 23 Mar 2023 06:51:52 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33939ddffa9123237cf16bfec2e9a607bd843a5bee2d288d4310a31c3194cd1e`  
		Last Modified: Thu, 23 Mar 2023 06:51:53 GMT  
		Size: 1.4 MB (1385099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7183c9f17e4410b0677871e77f993826accf0981aefec7b2a4e3c238c5d657b`  
		Last Modified: Thu, 23 Mar 2023 06:51:52 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:4fec14cf5a78e727b8c74c974ab7d5e4cecd7f2474147a58a4218ddebc02dd87
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96978049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b0466b7b74fdb561f8edf82d5292c2ae17b67cdff6e3c10539493ba7fd11f3`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 23 Mar 2023 00:39:08 GMT
ADD file:f331251c4c21fceff56d13f76442a6334dc355c29ec7450768c1c86a3db1adab in / 
# Thu, 23 Mar 2023 00:39:09 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 21:17:12 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 21:17:40 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 21:17:41 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 21:18:01 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 23 Mar 2023 21:18:01 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 21:18:01 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 21:18:02 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 21:18:02 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 21:18:02 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 21:18:02 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 21:18:14 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 21:18:14 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 21:18:14 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 21:18:14 GMT
USER adminer
# Thu, 23 Mar 2023 21:18:14 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:c1bb878cff31d37952c5c73ed15c167f599bb7f97b3eeaa1a17352b2473b3394`  
		Last Modified: Thu, 23 Mar 2023 00:42:44 GMT  
		Size: 56.0 MB (56027911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67239d163b3f7b443f91919b613775ed043520e6b06b413a9628905d01e98992`  
		Last Modified: Thu, 23 Mar 2023 21:18:34 GMT  
		Size: 39.6 MB (39558048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88061812377dcf7351518633da4694430dfe02ac13bdbc48516d26c18586a0d5`  
		Last Modified: Thu, 23 Mar 2023 21:18:24 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e265f46cc6fadbfde249ce57b0f1b54264aab3a0c6a1453f7f2699545e0b3204`  
		Last Modified: Thu, 23 Mar 2023 21:18:50 GMT  
		Size: 2.7 KB (2710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca518b34b603a08f7c5881dd84c944bb8236eb9f03a74636f1d2496138c0f756`  
		Last Modified: Thu, 23 Mar 2023 21:18:50 GMT  
		Size: 1.9 KB (1869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c12e6b62649c51d5b810142e53b66da078b62baadc21eecf203444c93de1263`  
		Last Modified: Thu, 23 Mar 2023 21:18:50 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f8a77bc64220b5352e77dfca8700a11755ee9d00cb280da618809bcaefc541`  
		Last Modified: Thu, 23 Mar 2023 21:18:50 GMT  
		Size: 1.4 MB (1385152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9c79da4d828244f71b3b0c18abe0d34506e6202fb0c07c7b38bcb553ff9361`  
		Last Modified: Thu, 23 Mar 2023 21:18:50 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; mips64le

```console
$ docker pull adminer@sha256:6071b807c18fd9c3a868729b6c008a72c4f33193d038d3266c552a13c81c2ebe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92608465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8730ff222f47754b556a9a28db99999e3b00e5f51261ff97b8c794f168b61cdf`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 23 Mar 2023 05:17:18 GMT
ADD file:2337efa705c8772705fa8519e513f4299e72c9eb63e3a68069778ca95a1511e6 in / 
# Thu, 23 Mar 2023 05:17:24 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 20:06:00 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 20:07:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 20:08:02 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 20:09:46 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 23 Mar 2023 20:09:52 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 20:09:56 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 20:09:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 20:10:02 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 20:10:06 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 20:10:09 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 20:11:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 20:11:04 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 20:11:08 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 20:11:11 GMT
USER adminer
# Thu, 23 Mar 2023 20:11:14 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:f3951ee58695b4d906b37f2d9a07e6158f66a7328d0c70445d9607cd8367ede0`  
		Last Modified: Thu, 23 Mar 2023 05:25:08 GMT  
		Size: 53.3 MB (53264720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1180d0aa65a6936ad9b336fd7ddf64160d0a95203d7f3d82027fe8912c936d73`  
		Last Modified: Thu, 23 Mar 2023 20:11:59 GMT  
		Size: 38.0 MB (37950695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a23105a66b5d86b4852f9dcf6753d154e1d5b3b76c178cf8baced410a4deb2`  
		Last Modified: Thu, 23 Mar 2023 20:11:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f6b792b9dbc62affd1f59a5c64bae91e7a40650b891a2227ee50499b244671`  
		Last Modified: Thu, 23 Mar 2023 20:12:18 GMT  
		Size: 2.7 KB (2713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bd7b3264510c2ff115b5bde0691e4507a8037e8afac4227a80c9b20927cd71`  
		Last Modified: Thu, 23 Mar 2023 20:12:18 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede1a6707d65116cd7175d9a72eb51517e94fd922e91749a84b539c88f0c1cbc`  
		Last Modified: Thu, 23 Mar 2023 20:12:18 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532cd52f2b4a83b3f92484a39a21601e8bcf404137a7665b958c9589d2a56c97`  
		Last Modified: Thu, 23 Mar 2023 20:12:19 GMT  
		Size: 1.4 MB (1386242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:799eb60dea8fba148d5d409a75beb6c1f6decb8507259a122daedabe15408244`  
		Last Modified: Thu, 23 Mar 2023 20:12:18 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:e8c3e0fd2be16699af072a6eb61d32ad6743ed74ba014f197f781e6626136e8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101252603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3cc4b2c295df05bffd40f80bc7f0829e1bee38b774903a1c79561b01d3c25a8`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 23 Mar 2023 01:19:25 GMT
ADD file:3eb86af6fda22c3e84548a6d0039be04819ce464b2700e8d8c140be49530ff7c in / 
# Thu, 23 Mar 2023 01:19:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 12:41:38 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 12:42:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 12:42:59 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 12:43:48 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 23 Mar 2023 12:43:50 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 12:43:51 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 12:43:51 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 12:43:52 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 12:43:53 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 12:43:54 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 12:44:25 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 12:44:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 12:44:27 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 12:44:27 GMT
USER adminer
# Thu, 23 Mar 2023 12:44:28 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:566bc84f2641b393ac5a2f4a2ca405c09943aa3ec679f38ea1588f6ee930219e`  
		Last Modified: Thu, 23 Mar 2023 01:23:52 GMT  
		Size: 58.9 MB (58921026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2fbb285bf85ccfbb4c5282ba9f10d09cecbc5a0bab31ef237b51b3201089c2`  
		Last Modified: Thu, 23 Mar 2023 12:45:00 GMT  
		Size: 40.9 MB (40939153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5c4d551007797e513e8983796e921a39828107b5d1309cb2783b12bc6aaac4`  
		Last Modified: Thu, 23 Mar 2023 12:44:46 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a981786b6703fc32d30f8d08bcc4e47bc3359d29ec0b8ad35e1815c6e43f95`  
		Last Modified: Thu, 23 Mar 2023 12:45:18 GMT  
		Size: 2.7 KB (2711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b538b21119d1b99f45b99c3482fbc3815a12ff274279e57de7f322366ac5a064`  
		Last Modified: Thu, 23 Mar 2023 12:45:18 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f469564ebedfa716940bf361e3f4e958f5760932c5afc56a10524d0f633f1e90`  
		Last Modified: Thu, 23 Mar 2023 12:45:18 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e96f627d9a4deaae5faff7c9935f1dbc2bbe05dccc2d627c79cb48f600de895`  
		Last Modified: Thu, 23 Mar 2023 12:45:19 GMT  
		Size: 1.4 MB (1385464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf7d927e154813af62ae740af92fe128baf1c4372c852b3600355800ebc4636`  
		Last Modified: Thu, 23 Mar 2023 12:45:18 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; s390x

```console
$ docker pull adminer@sha256:44709f3540da7398591b1e5e2e96af71000ca46ab83e50d64901e0b4d7cea28b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93687112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c143ca3a2b00fef62f75a55e8ec15ee516c01070c860f9ec12c57d5c7f1196`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 23 Mar 2023 00:43:50 GMT
ADD file:1111f9325245c8edccf2d9480c39cf2368f783ad86c2700d452be4e8cbebef8a in / 
# Thu, 23 Mar 2023 00:43:54 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:12:38 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 07:12:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 07:12:59 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 07:13:14 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 23 Mar 2023 07:13:14 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 07:13:14 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 07:13:15 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 07:13:15 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 07:13:15 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 07:13:15 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 07:13:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 07:13:23 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 07:13:23 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 07:13:23 GMT
USER adminer
# Thu, 23 Mar 2023 07:13:23 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:00dac46cbc44f444bd1dffe5b00a1b239054295b96f7984793273e9d12e75591`  
		Last Modified: Thu, 23 Mar 2023 00:47:04 GMT  
		Size: 53.3 MB (53277499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef40e14df43903a504c3865251eb934e8f644d89890514fc292b06981fca7826`  
		Last Modified: Thu, 23 Mar 2023 07:13:44 GMT  
		Size: 39.0 MB (39017484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f79bdf3c2e58c635953d9f0329b1010a5ff99b977d98975e467b7ab57a155e`  
		Last Modified: Thu, 23 Mar 2023 07:13:37 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a99c25318d8aa437b51f90c7016573b6f47e86afa9443badc88e8d1e03a23fd`  
		Last Modified: Thu, 23 Mar 2023 07:13:53 GMT  
		Size: 2.7 KB (2712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446aa9007ef953ba5564a78772fc6cdebc498a99f3886fd21e2d62598591aa84`  
		Last Modified: Thu, 23 Mar 2023 07:13:53 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548528b8aa2488b1c52162c3f227b73f2af8c56b1df973565066e37ee4295939`  
		Last Modified: Thu, 23 Mar 2023 07:13:53 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b53cd708608bcb6d8d6e0638c077f3c2544501bce3b0103d029da761aa9dd3`  
		Last Modified: Thu, 23 Mar 2023 07:13:54 GMT  
		Size: 1.4 MB (1385185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83e4966551f089235a491b28f9fb699ef37fe5dc8c27f816f6fa9ca6b1cbdaa`  
		Last Modified: Thu, 23 Mar 2023 07:13:53 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4-standalone`

```console
$ docker pull adminer@sha256:4203fd6bcd82fe25dceaf8acb4826129cf7a6e93b22a5ab2fc0ec5a7cdaca3f4
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
$ docker pull adminer@sha256:b5570962c3a9981b6572e61dd33f5cbd394a1a9d27ee6342b4241338af330449
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95921691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e1b3241b20061365693574e1c1241f64a48b15a7f439b8df760456d83009c7`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:15 GMT
ADD file:459d1e92eb8c24ff4758f974d289ca8a2abe04cf50b6fe2bd760aa4589478289 in / 
# Thu, 23 Mar 2023 01:30:15 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 05:55:49 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 05:56:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 05:56:13 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 05:56:14 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 05:56:14 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 05:56:14 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 05:56:14 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 05:56:14 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 05:56:14 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 05:56:25 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 05:56:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 05:56:26 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 05:56:26 GMT
USER adminer
# Thu, 23 Mar 2023 05:56:26 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 05:56:26 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:3e440a7045683e27f8e2fa04000e0e078d8dfac0c971358ae0f8c65c13321c8e`  
		Last Modified: Thu, 23 Mar 2023 01:34:00 GMT  
		Size: 55.0 MB (55045608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6386bc062c6cf91f6c1451db68015d43a1afd7d67a8f0710050e557777a30a`  
		Last Modified: Thu, 23 Mar 2023 05:57:00 GMT  
		Size: 39.5 MB (39486568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dbc633dab938fa31a0afdfe3ac449318f04eb42e13b59c2602178aed2af127e`  
		Last Modified: Thu, 23 Mar 2023 05:56:53 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39317196bba2d873b239492ba23f8f1d62f89b661fb1760b65f29b1404322c60`  
		Last Modified: Thu, 23 Mar 2023 05:56:53 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ea8e1da1f9854a8c3bf43a78f5b403bdfad3f2c2861edfbfd902566950a7a2`  
		Last Modified: Thu, 23 Mar 2023 05:56:53 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ce0ac056362cd982a31febaaf97daa568c31c2e95f1f4265e82cc6fbeaffd4`  
		Last Modified: Thu, 23 Mar 2023 05:56:53 GMT  
		Size: 1.4 MB (1385271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3ee3b23021de0471ff83e0b10babf764acf8f57dbb17c2eef966f084eb314a`  
		Last Modified: Thu, 23 Mar 2023 05:56:53 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; arm variant v5

```console
$ docker pull adminer@sha256:4344599d09a3a9134c3a42f59ad31606dd3e8952bb9ae5d72d64dc5297cdc6bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91184910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512e73052fee795753bdd64cababc1bcc5ccdc4ce7ae0391a67a4013d1b98432`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 00:48:37 GMT
ADD file:8419f4bee11379b8aa511da1fe7cdcd6b2cb8c252bc90f76dec672a5b802ea27 in / 
# Thu, 23 Mar 2023 00:48:37 GMT
CMD ["bash"]
# Sat, 25 Mar 2023 02:48:49 GMT
STOPSIGNAL SIGINT
# Sat, 25 Mar 2023 02:49:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Sat, 25 Mar 2023 02:49:17 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Sat, 25 Mar 2023 02:49:17 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 25 Mar 2023 02:49:17 GMT
WORKDIR /var/www/html
# Sat, 25 Mar 2023 02:49:18 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 25 Mar 2023 02:49:18 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 25 Mar 2023 02:49:18 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 25 Mar 2023 02:49:18 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Sat, 25 Mar 2023 02:49:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 25 Mar 2023 02:49:30 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 25 Mar 2023 02:49:30 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 25 Mar 2023 02:49:30 GMT
USER adminer
# Sat, 25 Mar 2023 02:49:30 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 25 Mar 2023 02:49:30 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:9a8ea6c28ff9e1b5a437e1e5b168873207139672ec8d755939cad00b23349e22`  
		Last Modified: Thu, 23 Mar 2023 02:21:35 GMT  
		Size: 52.5 MB (52549555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeab9bc611f5a84450bb374d38da4707075933d49bf1f7653fd834777749923e`  
		Last Modified: Sat, 25 Mar 2023 02:50:47 GMT  
		Size: 37.2 MB (37246063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e679cbf63988e1866986ea77804721769a09f59bdef7a89368f93a3abd2409`  
		Last Modified: Sat, 25 Mar 2023 02:50:39 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7959eefb479c10f4ab8829bcc4ee81ce479a5bff4f3d776e2d684522e56d36c`  
		Last Modified: Sat, 25 Mar 2023 02:50:39 GMT  
		Size: 1.9 KB (1865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b261a380e55719d974d3c7d0d3816f93ba071f56ab2669b4e941c91a49aa11c9`  
		Last Modified: Sat, 25 Mar 2023 02:50:39 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f7d098a043908e9b0872735983e550db864960c2b9998a675db2c956a02a60`  
		Last Modified: Sat, 25 Mar 2023 02:50:39 GMT  
		Size: 1.4 MB (1385072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a8d1397cd986a98157defb67fbca51bfe84b0d994ad3b7e2199a9d4adb3bf5`  
		Last Modified: Sat, 25 Mar 2023 02:50:39 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:208e28dc00b696fd2786ae0fac00bbac135df7d327a78f1a3b07b430e8be29fa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87782361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924e553786350523e3dabd52a79ebaa532e1ee1f1cd4f55c123b6f2debfd887b`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 01:13:21 GMT
ADD file:fa1cbfdd44274e571cabd5ca7fafa08b17c6f497ecfca6368a9eec4d2527a364 in / 
# Thu, 23 Mar 2023 01:13:22 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 13:53:52 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 13:54:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 13:54:17 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 13:54:17 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 13:54:18 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 13:54:18 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 13:54:18 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 13:54:18 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 13:54:18 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 13:54:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 13:54:30 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 13:54:30 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 13:54:30 GMT
USER adminer
# Thu, 23 Mar 2023 13:54:30 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 13:54:30 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:d50e868f9a626a3c456c0c52c3b013e87619bbac7798ac0c2acf2a2407303125`  
		Last Modified: Thu, 23 Mar 2023 01:33:00 GMT  
		Size: 50.2 MB (50211788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750746172b8a677cb809244c17155d7b05d643b2d816de3d8090ff3593de19ea`  
		Last Modified: Thu, 23 Mar 2023 13:55:03 GMT  
		Size: 36.2 MB (36181275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79543298adbabe76f964cc3578ae398897a0bc10ee8ebf4a0a3338a8ee26b6e8`  
		Last Modified: Thu, 23 Mar 2023 13:54:55 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7b7c098bbce560d98941c87164725c63999c701f19f2500e91578c8d994c8f`  
		Last Modified: Thu, 23 Mar 2023 13:54:56 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90441e257dd07454f7d03e5aa41e80d43c14256ff5040356a29d4639b23d75fc`  
		Last Modified: Thu, 23 Mar 2023 13:54:55 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65767342491a731ec4afa7560fd1b162f1ea5c932fc69e8326baad4bec228e7e`  
		Last Modified: Thu, 23 Mar 2023 13:54:56 GMT  
		Size: 1.4 MB (1385066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a8450e329b8116e25e9fa7cb6b678d57084c5946b3167f2cb126880295263a`  
		Last Modified: Thu, 23 Mar 2023 13:54:55 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:7fe9245eaab6579d2f02b2c43ece653c6f014f78be767a77580df6401023b8b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94334964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da1ba2cdb7c1dcd745eda1a855a3c5d0cc50e77182d900a1a13fab7ecb94f0f1`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:02 GMT
ADD file:70d18f9eea4e4fbdb941e66490ccb7233e182fe7ded1185de91c7d55580dd13e in / 
# Thu, 23 Mar 2023 00:45:02 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:50:38 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 06:50:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 06:50:57 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 06:50:57 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 06:50:58 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 06:50:58 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 06:50:58 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 06:50:58 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 06:50:58 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 06:51:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 06:51:08 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 06:51:08 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 06:51:08 GMT
USER adminer
# Thu, 23 Mar 2023 06:51:08 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 06:51:08 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:8022b074731d9ecee7f4fba79b993920973811dda168bbc08636f18523b90122`  
		Last Modified: Thu, 23 Mar 2023 00:47:46 GMT  
		Size: 53.7 MB (53703099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98305094c7fd13042b057082ec8d7bcc2b6f08cf0bba01a567b6bc108039bdf1`  
		Last Modified: Thu, 23 Mar 2023 06:51:37 GMT  
		Size: 39.2 MB (39242570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbbb9ddd2e012fdf94f2222f96fe1f8514ec4285c8acff371dd027ca67043c8`  
		Last Modified: Thu, 23 Mar 2023 06:51:30 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b3fa21b5eaa269a0e522ee6faa17c1942a9eb531a85d65093c785db3bf4ca32`  
		Last Modified: Thu, 23 Mar 2023 06:51:30 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbcc9aba89fb8cb163ab7c6f00eaee21df2f499f9cfbb89de3b18e5f24ba0087`  
		Last Modified: Thu, 23 Mar 2023 06:51:30 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf77c8ff22b40bbe616794e9d54103a4a9648107d69c9057deb1a83342d3d58`  
		Last Modified: Thu, 23 Mar 2023 06:51:31 GMT  
		Size: 1.4 MB (1385053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bd969a23b87a5402679ff8373fd3e9ce7af9a3e999bad556fe0cc25dda1cc6`  
		Last Modified: Thu, 23 Mar 2023 06:51:30 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; 386

```console
$ docker pull adminer@sha256:ca2ee65836fd06aba737873c17718cd1ae4e52f6ba9a2869000be6794922ec0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96975396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47306ce39706e8ed333600b8d4399cb09c02ffe4e169f76bd59fa5b6569ae778`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 00:39:08 GMT
ADD file:f331251c4c21fceff56d13f76442a6334dc355c29ec7450768c1c86a3db1adab in / 
# Thu, 23 Mar 2023 00:39:09 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 21:17:12 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 21:17:40 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 21:17:41 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 21:17:41 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 21:17:41 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 21:17:42 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 21:17:42 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 21:17:42 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 21:17:42 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 21:17:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 21:17:54 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 21:17:54 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 21:17:54 GMT
USER adminer
# Thu, 23 Mar 2023 21:17:55 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 21:17:55 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:c1bb878cff31d37952c5c73ed15c167f599bb7f97b3eeaa1a17352b2473b3394`  
		Last Modified: Thu, 23 Mar 2023 00:42:44 GMT  
		Size: 56.0 MB (56027911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67239d163b3f7b443f91919b613775ed043520e6b06b413a9628905d01e98992`  
		Last Modified: Thu, 23 Mar 2023 21:18:34 GMT  
		Size: 39.6 MB (39558048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88061812377dcf7351518633da4694430dfe02ac13bdbc48516d26c18586a0d5`  
		Last Modified: Thu, 23 Mar 2023 21:18:24 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c664bb8231af50f8a98b457a9e7c291444345b0066ed54ddbcc0b2129859965`  
		Last Modified: Thu, 23 Mar 2023 21:18:24 GMT  
		Size: 1.9 KB (1869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a209358917bcf344993c93aad3b156d6a09b6ab64d43df3941ca51e6c414b9`  
		Last Modified: Thu, 23 Mar 2023 21:18:24 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061ad9c8d5ae0dc7e0d69094e0f6d09b29dea00ec113641833b5a37f404de058`  
		Last Modified: Thu, 23 Mar 2023 21:18:24 GMT  
		Size: 1.4 MB (1385210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2761eeb066c4b63e66ada920b87fc430284439f4c76fac14a274ef528430d3f`  
		Last Modified: Thu, 23 Mar 2023 21:18:24 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; mips64le

```console
$ docker pull adminer@sha256:14de06501f131ba9f62a814f592d766d6f050b30eab65a15bb1e753a436aab3d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92605785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddae0bdce53fcfedd28644c8fc0df52f38f44000615def4d84b2c88db2aff3ab`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 05:17:18 GMT
ADD file:2337efa705c8772705fa8519e513f4299e72c9eb63e3a68069778ca95a1511e6 in / 
# Thu, 23 Mar 2023 05:17:24 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 20:06:00 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 20:07:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 20:08:02 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 20:08:09 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 20:08:13 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 20:08:16 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 20:08:19 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 20:08:22 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 20:08:26 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 20:09:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 20:09:20 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 20:09:24 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 20:09:27 GMT
USER adminer
# Thu, 23 Mar 2023 20:09:31 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 20:09:34 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:f3951ee58695b4d906b37f2d9a07e6158f66a7328d0c70445d9607cd8367ede0`  
		Last Modified: Thu, 23 Mar 2023 05:25:08 GMT  
		Size: 53.3 MB (53264720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1180d0aa65a6936ad9b336fd7ddf64160d0a95203d7f3d82027fe8912c936d73`  
		Last Modified: Thu, 23 Mar 2023 20:11:59 GMT  
		Size: 38.0 MB (37950695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a23105a66b5d86b4852f9dcf6753d154e1d5b3b76c178cf8baced410a4deb2`  
		Last Modified: Thu, 23 Mar 2023 20:11:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba90b5b3033a3d6ba607430a17c7e37f0fae8f0664ac81a4e571e9ad9fca9e2`  
		Last Modified: Thu, 23 Mar 2023 20:11:33 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b1980d6708cacd2f28ca074bd917c1143a47040b425da5985915850214f197f`  
		Last Modified: Thu, 23 Mar 2023 20:11:33 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfbeda1e7451034cf22503ff221351a0d3f5e1f63a6f11dc71a81450a7aaadd`  
		Last Modified: Thu, 23 Mar 2023 20:11:34 GMT  
		Size: 1.4 MB (1386264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b87439fd13726c64bed775edf40ceb3cbc1b5dbf3f62fb9b127024394aaece4`  
		Last Modified: Thu, 23 Mar 2023 20:11:33 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:ddf406bedb6ea27fd15da89331e085e564dcde0c98ba31f3914b14b4483aa56e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101249875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8b45276387b274e6256e8c13851f3460fdd98b29ca47a09f04a8fad8d02090`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 01:19:25 GMT
ADD file:3eb86af6fda22c3e84548a6d0039be04819ce464b2700e8d8c140be49530ff7c in / 
# Thu, 23 Mar 2023 01:19:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 12:41:38 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 12:42:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 12:42:59 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 12:43:01 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 12:43:01 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 12:43:01 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 12:43:02 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 12:43:02 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 12:43:03 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 12:43:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 12:43:33 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 12:43:33 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 12:43:34 GMT
USER adminer
# Thu, 23 Mar 2023 12:43:35 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 12:43:35 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:566bc84f2641b393ac5a2f4a2ca405c09943aa3ec679f38ea1588f6ee930219e`  
		Last Modified: Thu, 23 Mar 2023 01:23:52 GMT  
		Size: 58.9 MB (58921026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2fbb285bf85ccfbb4c5282ba9f10d09cecbc5a0bab31ef237b51b3201089c2`  
		Last Modified: Thu, 23 Mar 2023 12:45:00 GMT  
		Size: 40.9 MB (40939153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5c4d551007797e513e8983796e921a39828107b5d1309cb2783b12bc6aaac4`  
		Last Modified: Thu, 23 Mar 2023 12:44:46 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19dcdc4ed08a4d33d3c19d3c7a7fcb606bed16f514bbdf68d09ed75d0ef5a039`  
		Last Modified: Thu, 23 Mar 2023 12:44:47 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0187a4a30cb1c249de5010601f0912c92400f91482facb00198f8ba8e3691e`  
		Last Modified: Thu, 23 Mar 2023 12:44:46 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3867a61f6a3237b86e8a6bb431978b79ef5a1320ee3ebe58670b7a68f930c0f`  
		Last Modified: Thu, 23 Mar 2023 12:44:47 GMT  
		Size: 1.4 MB (1385455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553fdd9019949edcff0333970ef2dc5fa9af5479a21e08ecaf14a608524f497f`  
		Last Modified: Thu, 23 Mar 2023 12:44:46 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; s390x

```console
$ docker pull adminer@sha256:3a1427b2251efb24343fedded181036a73a9a9edd77c0241f1907db59654d4f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93684414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d7a2d888bb0da291a197f178923752e3a408b6b8002d6ae4d4c8595173ec84`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 00:43:50 GMT
ADD file:1111f9325245c8edccf2d9480c39cf2368f783ad86c2700d452be4e8cbebef8a in / 
# Thu, 23 Mar 2023 00:43:54 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:12:38 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 07:12:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 07:12:59 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 07:12:59 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 07:12:59 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 07:12:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 07:12:59 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 07:12:59 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 07:12:59 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 07:13:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 07:13:07 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 07:13:07 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 07:13:08 GMT
USER adminer
# Thu, 23 Mar 2023 07:13:08 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 07:13:08 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:00dac46cbc44f444bd1dffe5b00a1b239054295b96f7984793273e9d12e75591`  
		Last Modified: Thu, 23 Mar 2023 00:47:04 GMT  
		Size: 53.3 MB (53277499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef40e14df43903a504c3865251eb934e8f644d89890514fc292b06981fca7826`  
		Last Modified: Thu, 23 Mar 2023 07:13:44 GMT  
		Size: 39.0 MB (39017484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f79bdf3c2e58c635953d9f0329b1010a5ff99b977d98975e467b7ab57a155e`  
		Last Modified: Thu, 23 Mar 2023 07:13:37 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ebc836b2a414afb40c1d84fa4fe4af21828a8f07dcbbbfe020a9a2270b0c467`  
		Last Modified: Thu, 23 Mar 2023 07:13:37 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:395b8975dd5a57c4e6e30bccd71a2d34125566cbb50b6000d142e49fb27dc1ea`  
		Last Modified: Thu, 23 Mar 2023 07:13:37 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7cb7770c3999b7b71cb8bd67b1686854b1cf6a8fbd340c7da905fddae466c1`  
		Last Modified: Thu, 23 Mar 2023 07:13:37 GMT  
		Size: 1.4 MB (1385197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47125e4be7b760f757795627cf23bffd8efbadc93fd3f20e13ac58ddac7b2639`  
		Last Modified: Thu, 23 Mar 2023 07:13:37 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4.8.1`

```console
$ docker pull adminer@sha256:4203fd6bcd82fe25dceaf8acb4826129cf7a6e93b22a5ab2fc0ec5a7cdaca3f4
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

### `adminer:4.8.1` - linux; amd64

```console
$ docker pull adminer@sha256:b5570962c3a9981b6572e61dd33f5cbd394a1a9d27ee6342b4241338af330449
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95921691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e1b3241b20061365693574e1c1241f64a48b15a7f439b8df760456d83009c7`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:15 GMT
ADD file:459d1e92eb8c24ff4758f974d289ca8a2abe04cf50b6fe2bd760aa4589478289 in / 
# Thu, 23 Mar 2023 01:30:15 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 05:55:49 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 05:56:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 05:56:13 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 05:56:14 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 05:56:14 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 05:56:14 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 05:56:14 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 05:56:14 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 05:56:14 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 05:56:25 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 05:56:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 05:56:26 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 05:56:26 GMT
USER adminer
# Thu, 23 Mar 2023 05:56:26 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 05:56:26 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:3e440a7045683e27f8e2fa04000e0e078d8dfac0c971358ae0f8c65c13321c8e`  
		Last Modified: Thu, 23 Mar 2023 01:34:00 GMT  
		Size: 55.0 MB (55045608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6386bc062c6cf91f6c1451db68015d43a1afd7d67a8f0710050e557777a30a`  
		Last Modified: Thu, 23 Mar 2023 05:57:00 GMT  
		Size: 39.5 MB (39486568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dbc633dab938fa31a0afdfe3ac449318f04eb42e13b59c2602178aed2af127e`  
		Last Modified: Thu, 23 Mar 2023 05:56:53 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39317196bba2d873b239492ba23f8f1d62f89b661fb1760b65f29b1404322c60`  
		Last Modified: Thu, 23 Mar 2023 05:56:53 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ea8e1da1f9854a8c3bf43a78f5b403bdfad3f2c2861edfbfd902566950a7a2`  
		Last Modified: Thu, 23 Mar 2023 05:56:53 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ce0ac056362cd982a31febaaf97daa568c31c2e95f1f4265e82cc6fbeaffd4`  
		Last Modified: Thu, 23 Mar 2023 05:56:53 GMT  
		Size: 1.4 MB (1385271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3ee3b23021de0471ff83e0b10babf764acf8f57dbb17c2eef966f084eb314a`  
		Last Modified: Thu, 23 Mar 2023 05:56:53 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1` - linux; arm variant v5

```console
$ docker pull adminer@sha256:4344599d09a3a9134c3a42f59ad31606dd3e8952bb9ae5d72d64dc5297cdc6bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91184910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512e73052fee795753bdd64cababc1bcc5ccdc4ce7ae0391a67a4013d1b98432`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 00:48:37 GMT
ADD file:8419f4bee11379b8aa511da1fe7cdcd6b2cb8c252bc90f76dec672a5b802ea27 in / 
# Thu, 23 Mar 2023 00:48:37 GMT
CMD ["bash"]
# Sat, 25 Mar 2023 02:48:49 GMT
STOPSIGNAL SIGINT
# Sat, 25 Mar 2023 02:49:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Sat, 25 Mar 2023 02:49:17 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Sat, 25 Mar 2023 02:49:17 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 25 Mar 2023 02:49:17 GMT
WORKDIR /var/www/html
# Sat, 25 Mar 2023 02:49:18 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 25 Mar 2023 02:49:18 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 25 Mar 2023 02:49:18 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 25 Mar 2023 02:49:18 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Sat, 25 Mar 2023 02:49:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 25 Mar 2023 02:49:30 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 25 Mar 2023 02:49:30 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 25 Mar 2023 02:49:30 GMT
USER adminer
# Sat, 25 Mar 2023 02:49:30 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 25 Mar 2023 02:49:30 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:9a8ea6c28ff9e1b5a437e1e5b168873207139672ec8d755939cad00b23349e22`  
		Last Modified: Thu, 23 Mar 2023 02:21:35 GMT  
		Size: 52.5 MB (52549555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeab9bc611f5a84450bb374d38da4707075933d49bf1f7653fd834777749923e`  
		Last Modified: Sat, 25 Mar 2023 02:50:47 GMT  
		Size: 37.2 MB (37246063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e679cbf63988e1866986ea77804721769a09f59bdef7a89368f93a3abd2409`  
		Last Modified: Sat, 25 Mar 2023 02:50:39 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7959eefb479c10f4ab8829bcc4ee81ce479a5bff4f3d776e2d684522e56d36c`  
		Last Modified: Sat, 25 Mar 2023 02:50:39 GMT  
		Size: 1.9 KB (1865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b261a380e55719d974d3c7d0d3816f93ba071f56ab2669b4e941c91a49aa11c9`  
		Last Modified: Sat, 25 Mar 2023 02:50:39 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f7d098a043908e9b0872735983e550db864960c2b9998a675db2c956a02a60`  
		Last Modified: Sat, 25 Mar 2023 02:50:39 GMT  
		Size: 1.4 MB (1385072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a8d1397cd986a98157defb67fbca51bfe84b0d994ad3b7e2199a9d4adb3bf5`  
		Last Modified: Sat, 25 Mar 2023 02:50:39 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1` - linux; arm variant v7

```console
$ docker pull adminer@sha256:208e28dc00b696fd2786ae0fac00bbac135df7d327a78f1a3b07b430e8be29fa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87782361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924e553786350523e3dabd52a79ebaa532e1ee1f1cd4f55c123b6f2debfd887b`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 01:13:21 GMT
ADD file:fa1cbfdd44274e571cabd5ca7fafa08b17c6f497ecfca6368a9eec4d2527a364 in / 
# Thu, 23 Mar 2023 01:13:22 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 13:53:52 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 13:54:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 13:54:17 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 13:54:17 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 13:54:18 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 13:54:18 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 13:54:18 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 13:54:18 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 13:54:18 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 13:54:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 13:54:30 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 13:54:30 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 13:54:30 GMT
USER adminer
# Thu, 23 Mar 2023 13:54:30 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 13:54:30 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:d50e868f9a626a3c456c0c52c3b013e87619bbac7798ac0c2acf2a2407303125`  
		Last Modified: Thu, 23 Mar 2023 01:33:00 GMT  
		Size: 50.2 MB (50211788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750746172b8a677cb809244c17155d7b05d643b2d816de3d8090ff3593de19ea`  
		Last Modified: Thu, 23 Mar 2023 13:55:03 GMT  
		Size: 36.2 MB (36181275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79543298adbabe76f964cc3578ae398897a0bc10ee8ebf4a0a3338a8ee26b6e8`  
		Last Modified: Thu, 23 Mar 2023 13:54:55 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7b7c098bbce560d98941c87164725c63999c701f19f2500e91578c8d994c8f`  
		Last Modified: Thu, 23 Mar 2023 13:54:56 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90441e257dd07454f7d03e5aa41e80d43c14256ff5040356a29d4639b23d75fc`  
		Last Modified: Thu, 23 Mar 2023 13:54:55 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65767342491a731ec4afa7560fd1b162f1ea5c932fc69e8326baad4bec228e7e`  
		Last Modified: Thu, 23 Mar 2023 13:54:56 GMT  
		Size: 1.4 MB (1385066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a8450e329b8116e25e9fa7cb6b678d57084c5946b3167f2cb126880295263a`  
		Last Modified: Thu, 23 Mar 2023 13:54:55 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:7fe9245eaab6579d2f02b2c43ece653c6f014f78be767a77580df6401023b8b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94334964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da1ba2cdb7c1dcd745eda1a855a3c5d0cc50e77182d900a1a13fab7ecb94f0f1`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:02 GMT
ADD file:70d18f9eea4e4fbdb941e66490ccb7233e182fe7ded1185de91c7d55580dd13e in / 
# Thu, 23 Mar 2023 00:45:02 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:50:38 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 06:50:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 06:50:57 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 06:50:57 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 06:50:58 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 06:50:58 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 06:50:58 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 06:50:58 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 06:50:58 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 06:51:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 06:51:08 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 06:51:08 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 06:51:08 GMT
USER adminer
# Thu, 23 Mar 2023 06:51:08 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 06:51:08 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:8022b074731d9ecee7f4fba79b993920973811dda168bbc08636f18523b90122`  
		Last Modified: Thu, 23 Mar 2023 00:47:46 GMT  
		Size: 53.7 MB (53703099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98305094c7fd13042b057082ec8d7bcc2b6f08cf0bba01a567b6bc108039bdf1`  
		Last Modified: Thu, 23 Mar 2023 06:51:37 GMT  
		Size: 39.2 MB (39242570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbbb9ddd2e012fdf94f2222f96fe1f8514ec4285c8acff371dd027ca67043c8`  
		Last Modified: Thu, 23 Mar 2023 06:51:30 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b3fa21b5eaa269a0e522ee6faa17c1942a9eb531a85d65093c785db3bf4ca32`  
		Last Modified: Thu, 23 Mar 2023 06:51:30 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbcc9aba89fb8cb163ab7c6f00eaee21df2f499f9cfbb89de3b18e5f24ba0087`  
		Last Modified: Thu, 23 Mar 2023 06:51:30 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf77c8ff22b40bbe616794e9d54103a4a9648107d69c9057deb1a83342d3d58`  
		Last Modified: Thu, 23 Mar 2023 06:51:31 GMT  
		Size: 1.4 MB (1385053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bd969a23b87a5402679ff8373fd3e9ce7af9a3e999bad556fe0cc25dda1cc6`  
		Last Modified: Thu, 23 Mar 2023 06:51:30 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1` - linux; 386

```console
$ docker pull adminer@sha256:ca2ee65836fd06aba737873c17718cd1ae4e52f6ba9a2869000be6794922ec0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96975396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47306ce39706e8ed333600b8d4399cb09c02ffe4e169f76bd59fa5b6569ae778`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 00:39:08 GMT
ADD file:f331251c4c21fceff56d13f76442a6334dc355c29ec7450768c1c86a3db1adab in / 
# Thu, 23 Mar 2023 00:39:09 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 21:17:12 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 21:17:40 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 21:17:41 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 21:17:41 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 21:17:41 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 21:17:42 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 21:17:42 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 21:17:42 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 21:17:42 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 21:17:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 21:17:54 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 21:17:54 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 21:17:54 GMT
USER adminer
# Thu, 23 Mar 2023 21:17:55 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 21:17:55 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:c1bb878cff31d37952c5c73ed15c167f599bb7f97b3eeaa1a17352b2473b3394`  
		Last Modified: Thu, 23 Mar 2023 00:42:44 GMT  
		Size: 56.0 MB (56027911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67239d163b3f7b443f91919b613775ed043520e6b06b413a9628905d01e98992`  
		Last Modified: Thu, 23 Mar 2023 21:18:34 GMT  
		Size: 39.6 MB (39558048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88061812377dcf7351518633da4694430dfe02ac13bdbc48516d26c18586a0d5`  
		Last Modified: Thu, 23 Mar 2023 21:18:24 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c664bb8231af50f8a98b457a9e7c291444345b0066ed54ddbcc0b2129859965`  
		Last Modified: Thu, 23 Mar 2023 21:18:24 GMT  
		Size: 1.9 KB (1869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a209358917bcf344993c93aad3b156d6a09b6ab64d43df3941ca51e6c414b9`  
		Last Modified: Thu, 23 Mar 2023 21:18:24 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061ad9c8d5ae0dc7e0d69094e0f6d09b29dea00ec113641833b5a37f404de058`  
		Last Modified: Thu, 23 Mar 2023 21:18:24 GMT  
		Size: 1.4 MB (1385210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2761eeb066c4b63e66ada920b87fc430284439f4c76fac14a274ef528430d3f`  
		Last Modified: Thu, 23 Mar 2023 21:18:24 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1` - linux; mips64le

```console
$ docker pull adminer@sha256:14de06501f131ba9f62a814f592d766d6f050b30eab65a15bb1e753a436aab3d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92605785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddae0bdce53fcfedd28644c8fc0df52f38f44000615def4d84b2c88db2aff3ab`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 05:17:18 GMT
ADD file:2337efa705c8772705fa8519e513f4299e72c9eb63e3a68069778ca95a1511e6 in / 
# Thu, 23 Mar 2023 05:17:24 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 20:06:00 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 20:07:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 20:08:02 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 20:08:09 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 20:08:13 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 20:08:16 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 20:08:19 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 20:08:22 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 20:08:26 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 20:09:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 20:09:20 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 20:09:24 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 20:09:27 GMT
USER adminer
# Thu, 23 Mar 2023 20:09:31 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 20:09:34 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:f3951ee58695b4d906b37f2d9a07e6158f66a7328d0c70445d9607cd8367ede0`  
		Last Modified: Thu, 23 Mar 2023 05:25:08 GMT  
		Size: 53.3 MB (53264720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1180d0aa65a6936ad9b336fd7ddf64160d0a95203d7f3d82027fe8912c936d73`  
		Last Modified: Thu, 23 Mar 2023 20:11:59 GMT  
		Size: 38.0 MB (37950695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a23105a66b5d86b4852f9dcf6753d154e1d5b3b76c178cf8baced410a4deb2`  
		Last Modified: Thu, 23 Mar 2023 20:11:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba90b5b3033a3d6ba607430a17c7e37f0fae8f0664ac81a4e571e9ad9fca9e2`  
		Last Modified: Thu, 23 Mar 2023 20:11:33 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b1980d6708cacd2f28ca074bd917c1143a47040b425da5985915850214f197f`  
		Last Modified: Thu, 23 Mar 2023 20:11:33 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfbeda1e7451034cf22503ff221351a0d3f5e1f63a6f11dc71a81450a7aaadd`  
		Last Modified: Thu, 23 Mar 2023 20:11:34 GMT  
		Size: 1.4 MB (1386264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b87439fd13726c64bed775edf40ceb3cbc1b5dbf3f62fb9b127024394aaece4`  
		Last Modified: Thu, 23 Mar 2023 20:11:33 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1` - linux; ppc64le

```console
$ docker pull adminer@sha256:ddf406bedb6ea27fd15da89331e085e564dcde0c98ba31f3914b14b4483aa56e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101249875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8b45276387b274e6256e8c13851f3460fdd98b29ca47a09f04a8fad8d02090`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 01:19:25 GMT
ADD file:3eb86af6fda22c3e84548a6d0039be04819ce464b2700e8d8c140be49530ff7c in / 
# Thu, 23 Mar 2023 01:19:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 12:41:38 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 12:42:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 12:42:59 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 12:43:01 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 12:43:01 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 12:43:01 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 12:43:02 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 12:43:02 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 12:43:03 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 12:43:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 12:43:33 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 12:43:33 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 12:43:34 GMT
USER adminer
# Thu, 23 Mar 2023 12:43:35 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 12:43:35 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:566bc84f2641b393ac5a2f4a2ca405c09943aa3ec679f38ea1588f6ee930219e`  
		Last Modified: Thu, 23 Mar 2023 01:23:52 GMT  
		Size: 58.9 MB (58921026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2fbb285bf85ccfbb4c5282ba9f10d09cecbc5a0bab31ef237b51b3201089c2`  
		Last Modified: Thu, 23 Mar 2023 12:45:00 GMT  
		Size: 40.9 MB (40939153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5c4d551007797e513e8983796e921a39828107b5d1309cb2783b12bc6aaac4`  
		Last Modified: Thu, 23 Mar 2023 12:44:46 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19dcdc4ed08a4d33d3c19d3c7a7fcb606bed16f514bbdf68d09ed75d0ef5a039`  
		Last Modified: Thu, 23 Mar 2023 12:44:47 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0187a4a30cb1c249de5010601f0912c92400f91482facb00198f8ba8e3691e`  
		Last Modified: Thu, 23 Mar 2023 12:44:46 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3867a61f6a3237b86e8a6bb431978b79ef5a1320ee3ebe58670b7a68f930c0f`  
		Last Modified: Thu, 23 Mar 2023 12:44:47 GMT  
		Size: 1.4 MB (1385455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553fdd9019949edcff0333970ef2dc5fa9af5479a21e08ecaf14a608524f497f`  
		Last Modified: Thu, 23 Mar 2023 12:44:46 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1` - linux; s390x

```console
$ docker pull adminer@sha256:3a1427b2251efb24343fedded181036a73a9a9edd77c0241f1907db59654d4f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93684414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d7a2d888bb0da291a197f178923752e3a408b6b8002d6ae4d4c8595173ec84`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 00:43:50 GMT
ADD file:1111f9325245c8edccf2d9480c39cf2368f783ad86c2700d452be4e8cbebef8a in / 
# Thu, 23 Mar 2023 00:43:54 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:12:38 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 07:12:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 07:12:59 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 07:12:59 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 07:12:59 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 07:12:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 07:12:59 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 07:12:59 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 07:12:59 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 07:13:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 07:13:07 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 07:13:07 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 07:13:08 GMT
USER adminer
# Thu, 23 Mar 2023 07:13:08 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 07:13:08 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:00dac46cbc44f444bd1dffe5b00a1b239054295b96f7984793273e9d12e75591`  
		Last Modified: Thu, 23 Mar 2023 00:47:04 GMT  
		Size: 53.3 MB (53277499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef40e14df43903a504c3865251eb934e8f644d89890514fc292b06981fca7826`  
		Last Modified: Thu, 23 Mar 2023 07:13:44 GMT  
		Size: 39.0 MB (39017484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f79bdf3c2e58c635953d9f0329b1010a5ff99b977d98975e467b7ab57a155e`  
		Last Modified: Thu, 23 Mar 2023 07:13:37 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ebc836b2a414afb40c1d84fa4fe4af21828a8f07dcbbbfe020a9a2270b0c467`  
		Last Modified: Thu, 23 Mar 2023 07:13:37 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:395b8975dd5a57c4e6e30bccd71a2d34125566cbb50b6000d142e49fb27dc1ea`  
		Last Modified: Thu, 23 Mar 2023 07:13:37 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7cb7770c3999b7b71cb8bd67b1686854b1cf6a8fbd340c7da905fddae466c1`  
		Last Modified: Thu, 23 Mar 2023 07:13:37 GMT  
		Size: 1.4 MB (1385197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47125e4be7b760f757795627cf23bffd8efbadc93fd3f20e13ac58ddac7b2639`  
		Last Modified: Thu, 23 Mar 2023 07:13:37 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4.8.1-fastcgi`

```console
$ docker pull adminer@sha256:5deda468db781fc1cf37cd89932cca5e14d827305089725caae037d065f9eae9
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

### `adminer:4.8.1-fastcgi` - linux; amd64

```console
$ docker pull adminer@sha256:35e5285bea82c78b08355dc314739f980e2437cbf1c9e51291b5168fd5cd6f75
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95924422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23fae11ad3f1ae58e8aa6d5af50bb131d52fd3b3fadbb2c8e22e67ceca7a76d7`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:15 GMT
ADD file:459d1e92eb8c24ff4758f974d289ca8a2abe04cf50b6fe2bd760aa4589478289 in / 
# Thu, 23 Mar 2023 01:30:15 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 05:55:49 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 05:56:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 05:56:13 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 05:56:30 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 23 Mar 2023 05:56:30 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 05:56:30 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 05:56:30 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 05:56:30 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 05:56:31 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 05:56:31 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 05:56:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 05:56:41 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 05:56:41 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 05:56:41 GMT
USER adminer
# Thu, 23 Mar 2023 05:56:42 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:3e440a7045683e27f8e2fa04000e0e078d8dfac0c971358ae0f8c65c13321c8e`  
		Last Modified: Thu, 23 Mar 2023 01:34:00 GMT  
		Size: 55.0 MB (55045608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6386bc062c6cf91f6c1451db68015d43a1afd7d67a8f0710050e557777a30a`  
		Last Modified: Thu, 23 Mar 2023 05:57:00 GMT  
		Size: 39.5 MB (39486568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dbc633dab938fa31a0afdfe3ac449318f04eb42e13b59c2602178aed2af127e`  
		Last Modified: Thu, 23 Mar 2023 05:56:53 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e43c5bb8d604942de8a801fbd515cde458e8296cda94b628a1a311281fe880`  
		Last Modified: Thu, 23 Mar 2023 05:57:17 GMT  
		Size: 2.7 KB (2712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991cbf4d6fdd0b401219e6f0c1474c3c379889e229e8305e5c7afc86459d6599`  
		Last Modified: Thu, 23 Mar 2023 05:57:16 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420cfe44d3089c8454b9568ad65803581ce9a8565536455cf2602d4b96ff6e35`  
		Last Modified: Thu, 23 Mar 2023 05:57:16 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad56f1c45901a03ae785f94f8dfc35d5689f400e95502fdf74ee2243dd5fd22`  
		Last Modified: Thu, 23 Mar 2023 05:57:17 GMT  
		Size: 1.4 MB (1385298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36974e24611dd62fec010effb08e11fdd389b0898bff3ee057b6bf9266aa3d8e`  
		Last Modified: Thu, 23 Mar 2023 05:57:16 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-fastcgi` - linux; arm variant v5

```console
$ docker pull adminer@sha256:83ad65624afb37bbccd0d59d7d82fc2814210821ac3b1f544cb057038e30a610
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91187641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd884953fb56ddec123031e25c1aef7a0add8ec9d119447de370a5aadc0e2166`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 23 Mar 2023 00:48:37 GMT
ADD file:8419f4bee11379b8aa511da1fe7cdcd6b2cb8c252bc90f76dec672a5b802ea27 in / 
# Thu, 23 Mar 2023 00:48:37 GMT
CMD ["bash"]
# Sat, 25 Mar 2023 02:48:49 GMT
STOPSIGNAL SIGINT
# Sat, 25 Mar 2023 02:49:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Sat, 25 Mar 2023 02:49:17 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Sat, 25 Mar 2023 02:49:47 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Sat, 25 Mar 2023 02:49:48 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 25 Mar 2023 02:49:48 GMT
WORKDIR /var/www/html
# Sat, 25 Mar 2023 02:49:48 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 25 Mar 2023 02:49:48 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 25 Mar 2023 02:49:48 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 25 Mar 2023 02:49:48 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Sat, 25 Mar 2023 02:50:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 25 Mar 2023 02:50:01 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 25 Mar 2023 02:50:01 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 25 Mar 2023 02:50:01 GMT
USER adminer
# Sat, 25 Mar 2023 02:50:01 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:9a8ea6c28ff9e1b5a437e1e5b168873207139672ec8d755939cad00b23349e22`  
		Last Modified: Thu, 23 Mar 2023 02:21:35 GMT  
		Size: 52.5 MB (52549555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeab9bc611f5a84450bb374d38da4707075933d49bf1f7653fd834777749923e`  
		Last Modified: Sat, 25 Mar 2023 02:50:47 GMT  
		Size: 37.2 MB (37246063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e679cbf63988e1866986ea77804721769a09f59bdef7a89368f93a3abd2409`  
		Last Modified: Sat, 25 Mar 2023 02:50:39 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a070ee59349bc1327cf753932c17cc9396004abaf993e6a56c9a2ef071b9d97`  
		Last Modified: Sat, 25 Mar 2023 02:51:03 GMT  
		Size: 2.7 KB (2709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39741322e4fc4e150bbe02d05ecb189f61fb32138b1a0a34a412390730e6b0a`  
		Last Modified: Sat, 25 Mar 2023 02:51:03 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b7e40e37ad3d10c54c47aac9a2000613f3fc90a30fe6b3166040b3b1d3416d`  
		Last Modified: Sat, 25 Mar 2023 02:51:03 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c99b025114fb17d7175738951a97689c171bbd82cd5177796b12d6d0424699`  
		Last Modified: Sat, 25 Mar 2023 02:51:03 GMT  
		Size: 1.4 MB (1385089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e4611882f0550bdfd18af6aa74746b7a16226506f8cc4951a3b6c05a61e999`  
		Last Modified: Sat, 25 Mar 2023 02:51:02 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:bc666796aa3d0cee0b13bc0afeb827eddb224ac94c2825e90be0b7935f4e8122
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87785110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8477e704cb362785d6fffb06bca6d401c7163028a20adb041de59c8927810ecc`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 23 Mar 2023 01:13:21 GMT
ADD file:fa1cbfdd44274e571cabd5ca7fafa08b17c6f497ecfca6368a9eec4d2527a364 in / 
# Thu, 23 Mar 2023 01:13:22 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 13:53:52 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 13:54:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 13:54:17 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 13:54:32 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 23 Mar 2023 13:54:33 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 13:54:33 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 13:54:33 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 13:54:33 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 13:54:33 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 13:54:33 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 13:54:44 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 13:54:44 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 13:54:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 13:54:44 GMT
USER adminer
# Thu, 23 Mar 2023 13:54:44 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:d50e868f9a626a3c456c0c52c3b013e87619bbac7798ac0c2acf2a2407303125`  
		Last Modified: Thu, 23 Mar 2023 01:33:00 GMT  
		Size: 50.2 MB (50211788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750746172b8a677cb809244c17155d7b05d643b2d816de3d8090ff3593de19ea`  
		Last Modified: Thu, 23 Mar 2023 13:55:03 GMT  
		Size: 36.2 MB (36181275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79543298adbabe76f964cc3578ae398897a0bc10ee8ebf4a0a3338a8ee26b6e8`  
		Last Modified: Thu, 23 Mar 2023 13:54:55 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31633dada050baeaf275a6f4e00621a9f3e3224c8045210053670913ba6d6585`  
		Last Modified: Thu, 23 Mar 2023 13:55:19 GMT  
		Size: 2.7 KB (2709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c21aec687480c0c87c1badd06ad8d1bc38a37d87223bc20a78ba010fd626cac`  
		Last Modified: Thu, 23 Mar 2023 13:55:19 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac9619b29c31046e1d85965461b5a590b86fb5f2f78c27167ec6cfca6f21651e`  
		Last Modified: Thu, 23 Mar 2023 13:55:19 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd30156b59e64f168057bb8a5fae751059636af01bb28f176af27932691211a`  
		Last Modified: Thu, 23 Mar 2023 13:55:20 GMT  
		Size: 1.4 MB (1385116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60631e91dd1890dcbae61adf6317c4a7be616954ef21fec67df71f340de0d351`  
		Last Modified: Thu, 23 Mar 2023 13:55:19 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:7596c184b40a20292868a7080a783453ddf723197fbd6e8c671d314d8b488e24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94337713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39cf91641fd4f5e8d3515aaa989cebc88d71589b000cc0c7a53339912cb8b5c`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:02 GMT
ADD file:70d18f9eea4e4fbdb941e66490ccb7233e182fe7ded1185de91c7d55580dd13e in / 
# Thu, 23 Mar 2023 00:45:02 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:50:38 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 06:50:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 06:50:57 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 06:51:11 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 23 Mar 2023 06:51:12 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 06:51:12 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 06:51:12 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 06:51:12 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 06:51:12 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 06:51:12 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 06:51:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 06:51:22 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 06:51:22 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 06:51:22 GMT
USER adminer
# Thu, 23 Mar 2023 06:51:22 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:8022b074731d9ecee7f4fba79b993920973811dda168bbc08636f18523b90122`  
		Last Modified: Thu, 23 Mar 2023 00:47:46 GMT  
		Size: 53.7 MB (53703099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98305094c7fd13042b057082ec8d7bcc2b6f08cf0bba01a567b6bc108039bdf1`  
		Last Modified: Thu, 23 Mar 2023 06:51:37 GMT  
		Size: 39.2 MB (39242570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbbb9ddd2e012fdf94f2222f96fe1f8514ec4285c8acff371dd027ca67043c8`  
		Last Modified: Thu, 23 Mar 2023 06:51:30 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed10fa53994213c7460cfbbec9c399e9d8cca8c2aec04202fedff5a70cf2889`  
		Last Modified: Thu, 23 Mar 2023 06:51:52 GMT  
		Size: 2.7 KB (2708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d7483fec2e916d9b95f32278191c4d548eaabe455a3f3ebc0fd94a93216b8f`  
		Last Modified: Thu, 23 Mar 2023 06:51:52 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8280d00d8418fda79bfb9d617fcbe8d8e10e3c43d208cbb6e3559b653a49557d`  
		Last Modified: Thu, 23 Mar 2023 06:51:52 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33939ddffa9123237cf16bfec2e9a607bd843a5bee2d288d4310a31c3194cd1e`  
		Last Modified: Thu, 23 Mar 2023 06:51:53 GMT  
		Size: 1.4 MB (1385099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7183c9f17e4410b0677871e77f993826accf0981aefec7b2a4e3c238c5d657b`  
		Last Modified: Thu, 23 Mar 2023 06:51:52 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:4fec14cf5a78e727b8c74c974ab7d5e4cecd7f2474147a58a4218ddebc02dd87
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96978049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b0466b7b74fdb561f8edf82d5292c2ae17b67cdff6e3c10539493ba7fd11f3`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 23 Mar 2023 00:39:08 GMT
ADD file:f331251c4c21fceff56d13f76442a6334dc355c29ec7450768c1c86a3db1adab in / 
# Thu, 23 Mar 2023 00:39:09 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 21:17:12 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 21:17:40 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 21:17:41 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 21:18:01 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 23 Mar 2023 21:18:01 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 21:18:01 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 21:18:02 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 21:18:02 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 21:18:02 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 21:18:02 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 21:18:14 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 21:18:14 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 21:18:14 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 21:18:14 GMT
USER adminer
# Thu, 23 Mar 2023 21:18:14 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:c1bb878cff31d37952c5c73ed15c167f599bb7f97b3eeaa1a17352b2473b3394`  
		Last Modified: Thu, 23 Mar 2023 00:42:44 GMT  
		Size: 56.0 MB (56027911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67239d163b3f7b443f91919b613775ed043520e6b06b413a9628905d01e98992`  
		Last Modified: Thu, 23 Mar 2023 21:18:34 GMT  
		Size: 39.6 MB (39558048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88061812377dcf7351518633da4694430dfe02ac13bdbc48516d26c18586a0d5`  
		Last Modified: Thu, 23 Mar 2023 21:18:24 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e265f46cc6fadbfde249ce57b0f1b54264aab3a0c6a1453f7f2699545e0b3204`  
		Last Modified: Thu, 23 Mar 2023 21:18:50 GMT  
		Size: 2.7 KB (2710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca518b34b603a08f7c5881dd84c944bb8236eb9f03a74636f1d2496138c0f756`  
		Last Modified: Thu, 23 Mar 2023 21:18:50 GMT  
		Size: 1.9 KB (1869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c12e6b62649c51d5b810142e53b66da078b62baadc21eecf203444c93de1263`  
		Last Modified: Thu, 23 Mar 2023 21:18:50 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f8a77bc64220b5352e77dfca8700a11755ee9d00cb280da618809bcaefc541`  
		Last Modified: Thu, 23 Mar 2023 21:18:50 GMT  
		Size: 1.4 MB (1385152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9c79da4d828244f71b3b0c18abe0d34506e6202fb0c07c7b38bcb553ff9361`  
		Last Modified: Thu, 23 Mar 2023 21:18:50 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-fastcgi` - linux; mips64le

```console
$ docker pull adminer@sha256:6071b807c18fd9c3a868729b6c008a72c4f33193d038d3266c552a13c81c2ebe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92608465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8730ff222f47754b556a9a28db99999e3b00e5f51261ff97b8c794f168b61cdf`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 23 Mar 2023 05:17:18 GMT
ADD file:2337efa705c8772705fa8519e513f4299e72c9eb63e3a68069778ca95a1511e6 in / 
# Thu, 23 Mar 2023 05:17:24 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 20:06:00 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 20:07:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 20:08:02 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 20:09:46 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 23 Mar 2023 20:09:52 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 20:09:56 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 20:09:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 20:10:02 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 20:10:06 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 20:10:09 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 20:11:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 20:11:04 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 20:11:08 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 20:11:11 GMT
USER adminer
# Thu, 23 Mar 2023 20:11:14 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:f3951ee58695b4d906b37f2d9a07e6158f66a7328d0c70445d9607cd8367ede0`  
		Last Modified: Thu, 23 Mar 2023 05:25:08 GMT  
		Size: 53.3 MB (53264720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1180d0aa65a6936ad9b336fd7ddf64160d0a95203d7f3d82027fe8912c936d73`  
		Last Modified: Thu, 23 Mar 2023 20:11:59 GMT  
		Size: 38.0 MB (37950695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a23105a66b5d86b4852f9dcf6753d154e1d5b3b76c178cf8baced410a4deb2`  
		Last Modified: Thu, 23 Mar 2023 20:11:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f6b792b9dbc62affd1f59a5c64bae91e7a40650b891a2227ee50499b244671`  
		Last Modified: Thu, 23 Mar 2023 20:12:18 GMT  
		Size: 2.7 KB (2713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bd7b3264510c2ff115b5bde0691e4507a8037e8afac4227a80c9b20927cd71`  
		Last Modified: Thu, 23 Mar 2023 20:12:18 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede1a6707d65116cd7175d9a72eb51517e94fd922e91749a84b539c88f0c1cbc`  
		Last Modified: Thu, 23 Mar 2023 20:12:18 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532cd52f2b4a83b3f92484a39a21601e8bcf404137a7665b958c9589d2a56c97`  
		Last Modified: Thu, 23 Mar 2023 20:12:19 GMT  
		Size: 1.4 MB (1386242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:799eb60dea8fba148d5d409a75beb6c1f6decb8507259a122daedabe15408244`  
		Last Modified: Thu, 23 Mar 2023 20:12:18 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:e8c3e0fd2be16699af072a6eb61d32ad6743ed74ba014f197f781e6626136e8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101252603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3cc4b2c295df05bffd40f80bc7f0829e1bee38b774903a1c79561b01d3c25a8`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 23 Mar 2023 01:19:25 GMT
ADD file:3eb86af6fda22c3e84548a6d0039be04819ce464b2700e8d8c140be49530ff7c in / 
# Thu, 23 Mar 2023 01:19:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 12:41:38 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 12:42:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 12:42:59 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 12:43:48 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 23 Mar 2023 12:43:50 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 12:43:51 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 12:43:51 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 12:43:52 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 12:43:53 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 12:43:54 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 12:44:25 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 12:44:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 12:44:27 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 12:44:27 GMT
USER adminer
# Thu, 23 Mar 2023 12:44:28 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:566bc84f2641b393ac5a2f4a2ca405c09943aa3ec679f38ea1588f6ee930219e`  
		Last Modified: Thu, 23 Mar 2023 01:23:52 GMT  
		Size: 58.9 MB (58921026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2fbb285bf85ccfbb4c5282ba9f10d09cecbc5a0bab31ef237b51b3201089c2`  
		Last Modified: Thu, 23 Mar 2023 12:45:00 GMT  
		Size: 40.9 MB (40939153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5c4d551007797e513e8983796e921a39828107b5d1309cb2783b12bc6aaac4`  
		Last Modified: Thu, 23 Mar 2023 12:44:46 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a981786b6703fc32d30f8d08bcc4e47bc3359d29ec0b8ad35e1815c6e43f95`  
		Last Modified: Thu, 23 Mar 2023 12:45:18 GMT  
		Size: 2.7 KB (2711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b538b21119d1b99f45b99c3482fbc3815a12ff274279e57de7f322366ac5a064`  
		Last Modified: Thu, 23 Mar 2023 12:45:18 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f469564ebedfa716940bf361e3f4e958f5760932c5afc56a10524d0f633f1e90`  
		Last Modified: Thu, 23 Mar 2023 12:45:18 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e96f627d9a4deaae5faff7c9935f1dbc2bbe05dccc2d627c79cb48f600de895`  
		Last Modified: Thu, 23 Mar 2023 12:45:19 GMT  
		Size: 1.4 MB (1385464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf7d927e154813af62ae740af92fe128baf1c4372c852b3600355800ebc4636`  
		Last Modified: Thu, 23 Mar 2023 12:45:18 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-fastcgi` - linux; s390x

```console
$ docker pull adminer@sha256:44709f3540da7398591b1e5e2e96af71000ca46ab83e50d64901e0b4d7cea28b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93687112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c143ca3a2b00fef62f75a55e8ec15ee516c01070c860f9ec12c57d5c7f1196`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 23 Mar 2023 00:43:50 GMT
ADD file:1111f9325245c8edccf2d9480c39cf2368f783ad86c2700d452be4e8cbebef8a in / 
# Thu, 23 Mar 2023 00:43:54 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:12:38 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 07:12:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 07:12:59 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 07:13:14 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 23 Mar 2023 07:13:14 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 07:13:14 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 07:13:15 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 07:13:15 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 07:13:15 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 07:13:15 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 07:13:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 07:13:23 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 07:13:23 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 07:13:23 GMT
USER adminer
# Thu, 23 Mar 2023 07:13:23 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:00dac46cbc44f444bd1dffe5b00a1b239054295b96f7984793273e9d12e75591`  
		Last Modified: Thu, 23 Mar 2023 00:47:04 GMT  
		Size: 53.3 MB (53277499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef40e14df43903a504c3865251eb934e8f644d89890514fc292b06981fca7826`  
		Last Modified: Thu, 23 Mar 2023 07:13:44 GMT  
		Size: 39.0 MB (39017484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f79bdf3c2e58c635953d9f0329b1010a5ff99b977d98975e467b7ab57a155e`  
		Last Modified: Thu, 23 Mar 2023 07:13:37 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a99c25318d8aa437b51f90c7016573b6f47e86afa9443badc88e8d1e03a23fd`  
		Last Modified: Thu, 23 Mar 2023 07:13:53 GMT  
		Size: 2.7 KB (2712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446aa9007ef953ba5564a78772fc6cdebc498a99f3886fd21e2d62598591aa84`  
		Last Modified: Thu, 23 Mar 2023 07:13:53 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548528b8aa2488b1c52162c3f227b73f2af8c56b1df973565066e37ee4295939`  
		Last Modified: Thu, 23 Mar 2023 07:13:53 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b53cd708608bcb6d8d6e0638c077f3c2544501bce3b0103d029da761aa9dd3`  
		Last Modified: Thu, 23 Mar 2023 07:13:54 GMT  
		Size: 1.4 MB (1385185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83e4966551f089235a491b28f9fb699ef37fe5dc8c27f816f6fa9ca6b1cbdaa`  
		Last Modified: Thu, 23 Mar 2023 07:13:53 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4.8.1-standalone`

```console
$ docker pull adminer@sha256:4203fd6bcd82fe25dceaf8acb4826129cf7a6e93b22a5ab2fc0ec5a7cdaca3f4
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

### `adminer:4.8.1-standalone` - linux; amd64

```console
$ docker pull adminer@sha256:b5570962c3a9981b6572e61dd33f5cbd394a1a9d27ee6342b4241338af330449
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95921691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e1b3241b20061365693574e1c1241f64a48b15a7f439b8df760456d83009c7`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:15 GMT
ADD file:459d1e92eb8c24ff4758f974d289ca8a2abe04cf50b6fe2bd760aa4589478289 in / 
# Thu, 23 Mar 2023 01:30:15 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 05:55:49 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 05:56:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 05:56:13 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 05:56:14 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 05:56:14 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 05:56:14 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 05:56:14 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 05:56:14 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 05:56:14 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 05:56:25 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 05:56:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 05:56:26 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 05:56:26 GMT
USER adminer
# Thu, 23 Mar 2023 05:56:26 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 05:56:26 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:3e440a7045683e27f8e2fa04000e0e078d8dfac0c971358ae0f8c65c13321c8e`  
		Last Modified: Thu, 23 Mar 2023 01:34:00 GMT  
		Size: 55.0 MB (55045608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6386bc062c6cf91f6c1451db68015d43a1afd7d67a8f0710050e557777a30a`  
		Last Modified: Thu, 23 Mar 2023 05:57:00 GMT  
		Size: 39.5 MB (39486568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dbc633dab938fa31a0afdfe3ac449318f04eb42e13b59c2602178aed2af127e`  
		Last Modified: Thu, 23 Mar 2023 05:56:53 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39317196bba2d873b239492ba23f8f1d62f89b661fb1760b65f29b1404322c60`  
		Last Modified: Thu, 23 Mar 2023 05:56:53 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ea8e1da1f9854a8c3bf43a78f5b403bdfad3f2c2861edfbfd902566950a7a2`  
		Last Modified: Thu, 23 Mar 2023 05:56:53 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ce0ac056362cd982a31febaaf97daa568c31c2e95f1f4265e82cc6fbeaffd4`  
		Last Modified: Thu, 23 Mar 2023 05:56:53 GMT  
		Size: 1.4 MB (1385271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3ee3b23021de0471ff83e0b10babf764acf8f57dbb17c2eef966f084eb314a`  
		Last Modified: Thu, 23 Mar 2023 05:56:53 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-standalone` - linux; arm variant v5

```console
$ docker pull adminer@sha256:4344599d09a3a9134c3a42f59ad31606dd3e8952bb9ae5d72d64dc5297cdc6bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91184910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512e73052fee795753bdd64cababc1bcc5ccdc4ce7ae0391a67a4013d1b98432`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 00:48:37 GMT
ADD file:8419f4bee11379b8aa511da1fe7cdcd6b2cb8c252bc90f76dec672a5b802ea27 in / 
# Thu, 23 Mar 2023 00:48:37 GMT
CMD ["bash"]
# Sat, 25 Mar 2023 02:48:49 GMT
STOPSIGNAL SIGINT
# Sat, 25 Mar 2023 02:49:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Sat, 25 Mar 2023 02:49:17 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Sat, 25 Mar 2023 02:49:17 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 25 Mar 2023 02:49:17 GMT
WORKDIR /var/www/html
# Sat, 25 Mar 2023 02:49:18 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 25 Mar 2023 02:49:18 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 25 Mar 2023 02:49:18 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 25 Mar 2023 02:49:18 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Sat, 25 Mar 2023 02:49:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 25 Mar 2023 02:49:30 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 25 Mar 2023 02:49:30 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 25 Mar 2023 02:49:30 GMT
USER adminer
# Sat, 25 Mar 2023 02:49:30 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 25 Mar 2023 02:49:30 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:9a8ea6c28ff9e1b5a437e1e5b168873207139672ec8d755939cad00b23349e22`  
		Last Modified: Thu, 23 Mar 2023 02:21:35 GMT  
		Size: 52.5 MB (52549555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeab9bc611f5a84450bb374d38da4707075933d49bf1f7653fd834777749923e`  
		Last Modified: Sat, 25 Mar 2023 02:50:47 GMT  
		Size: 37.2 MB (37246063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e679cbf63988e1866986ea77804721769a09f59bdef7a89368f93a3abd2409`  
		Last Modified: Sat, 25 Mar 2023 02:50:39 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7959eefb479c10f4ab8829bcc4ee81ce479a5bff4f3d776e2d684522e56d36c`  
		Last Modified: Sat, 25 Mar 2023 02:50:39 GMT  
		Size: 1.9 KB (1865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b261a380e55719d974d3c7d0d3816f93ba071f56ab2669b4e941c91a49aa11c9`  
		Last Modified: Sat, 25 Mar 2023 02:50:39 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f7d098a043908e9b0872735983e550db864960c2b9998a675db2c956a02a60`  
		Last Modified: Sat, 25 Mar 2023 02:50:39 GMT  
		Size: 1.4 MB (1385072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a8d1397cd986a98157defb67fbca51bfe84b0d994ad3b7e2199a9d4adb3bf5`  
		Last Modified: Sat, 25 Mar 2023 02:50:39 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:208e28dc00b696fd2786ae0fac00bbac135df7d327a78f1a3b07b430e8be29fa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87782361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924e553786350523e3dabd52a79ebaa532e1ee1f1cd4f55c123b6f2debfd887b`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 01:13:21 GMT
ADD file:fa1cbfdd44274e571cabd5ca7fafa08b17c6f497ecfca6368a9eec4d2527a364 in / 
# Thu, 23 Mar 2023 01:13:22 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 13:53:52 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 13:54:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 13:54:17 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 13:54:17 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 13:54:18 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 13:54:18 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 13:54:18 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 13:54:18 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 13:54:18 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 13:54:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 13:54:30 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 13:54:30 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 13:54:30 GMT
USER adminer
# Thu, 23 Mar 2023 13:54:30 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 13:54:30 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:d50e868f9a626a3c456c0c52c3b013e87619bbac7798ac0c2acf2a2407303125`  
		Last Modified: Thu, 23 Mar 2023 01:33:00 GMT  
		Size: 50.2 MB (50211788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750746172b8a677cb809244c17155d7b05d643b2d816de3d8090ff3593de19ea`  
		Last Modified: Thu, 23 Mar 2023 13:55:03 GMT  
		Size: 36.2 MB (36181275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79543298adbabe76f964cc3578ae398897a0bc10ee8ebf4a0a3338a8ee26b6e8`  
		Last Modified: Thu, 23 Mar 2023 13:54:55 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7b7c098bbce560d98941c87164725c63999c701f19f2500e91578c8d994c8f`  
		Last Modified: Thu, 23 Mar 2023 13:54:56 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90441e257dd07454f7d03e5aa41e80d43c14256ff5040356a29d4639b23d75fc`  
		Last Modified: Thu, 23 Mar 2023 13:54:55 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65767342491a731ec4afa7560fd1b162f1ea5c932fc69e8326baad4bec228e7e`  
		Last Modified: Thu, 23 Mar 2023 13:54:56 GMT  
		Size: 1.4 MB (1385066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a8450e329b8116e25e9fa7cb6b678d57084c5946b3167f2cb126880295263a`  
		Last Modified: Thu, 23 Mar 2023 13:54:55 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-standalone` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:7fe9245eaab6579d2f02b2c43ece653c6f014f78be767a77580df6401023b8b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94334964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da1ba2cdb7c1dcd745eda1a855a3c5d0cc50e77182d900a1a13fab7ecb94f0f1`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:02 GMT
ADD file:70d18f9eea4e4fbdb941e66490ccb7233e182fe7ded1185de91c7d55580dd13e in / 
# Thu, 23 Mar 2023 00:45:02 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:50:38 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 06:50:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 06:50:57 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 06:50:57 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 06:50:58 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 06:50:58 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 06:50:58 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 06:50:58 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 06:50:58 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 06:51:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 06:51:08 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 06:51:08 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 06:51:08 GMT
USER adminer
# Thu, 23 Mar 2023 06:51:08 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 06:51:08 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:8022b074731d9ecee7f4fba79b993920973811dda168bbc08636f18523b90122`  
		Last Modified: Thu, 23 Mar 2023 00:47:46 GMT  
		Size: 53.7 MB (53703099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98305094c7fd13042b057082ec8d7bcc2b6f08cf0bba01a567b6bc108039bdf1`  
		Last Modified: Thu, 23 Mar 2023 06:51:37 GMT  
		Size: 39.2 MB (39242570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbbb9ddd2e012fdf94f2222f96fe1f8514ec4285c8acff371dd027ca67043c8`  
		Last Modified: Thu, 23 Mar 2023 06:51:30 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b3fa21b5eaa269a0e522ee6faa17c1942a9eb531a85d65093c785db3bf4ca32`  
		Last Modified: Thu, 23 Mar 2023 06:51:30 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbcc9aba89fb8cb163ab7c6f00eaee21df2f499f9cfbb89de3b18e5f24ba0087`  
		Last Modified: Thu, 23 Mar 2023 06:51:30 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf77c8ff22b40bbe616794e9d54103a4a9648107d69c9057deb1a83342d3d58`  
		Last Modified: Thu, 23 Mar 2023 06:51:31 GMT  
		Size: 1.4 MB (1385053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bd969a23b87a5402679ff8373fd3e9ce7af9a3e999bad556fe0cc25dda1cc6`  
		Last Modified: Thu, 23 Mar 2023 06:51:30 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-standalone` - linux; 386

```console
$ docker pull adminer@sha256:ca2ee65836fd06aba737873c17718cd1ae4e52f6ba9a2869000be6794922ec0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96975396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47306ce39706e8ed333600b8d4399cb09c02ffe4e169f76bd59fa5b6569ae778`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 00:39:08 GMT
ADD file:f331251c4c21fceff56d13f76442a6334dc355c29ec7450768c1c86a3db1adab in / 
# Thu, 23 Mar 2023 00:39:09 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 21:17:12 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 21:17:40 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 21:17:41 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 21:17:41 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 21:17:41 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 21:17:42 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 21:17:42 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 21:17:42 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 21:17:42 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 21:17:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 21:17:54 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 21:17:54 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 21:17:54 GMT
USER adminer
# Thu, 23 Mar 2023 21:17:55 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 21:17:55 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:c1bb878cff31d37952c5c73ed15c167f599bb7f97b3eeaa1a17352b2473b3394`  
		Last Modified: Thu, 23 Mar 2023 00:42:44 GMT  
		Size: 56.0 MB (56027911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67239d163b3f7b443f91919b613775ed043520e6b06b413a9628905d01e98992`  
		Last Modified: Thu, 23 Mar 2023 21:18:34 GMT  
		Size: 39.6 MB (39558048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88061812377dcf7351518633da4694430dfe02ac13bdbc48516d26c18586a0d5`  
		Last Modified: Thu, 23 Mar 2023 21:18:24 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c664bb8231af50f8a98b457a9e7c291444345b0066ed54ddbcc0b2129859965`  
		Last Modified: Thu, 23 Mar 2023 21:18:24 GMT  
		Size: 1.9 KB (1869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a209358917bcf344993c93aad3b156d6a09b6ab64d43df3941ca51e6c414b9`  
		Last Modified: Thu, 23 Mar 2023 21:18:24 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061ad9c8d5ae0dc7e0d69094e0f6d09b29dea00ec113641833b5a37f404de058`  
		Last Modified: Thu, 23 Mar 2023 21:18:24 GMT  
		Size: 1.4 MB (1385210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2761eeb066c4b63e66ada920b87fc430284439f4c76fac14a274ef528430d3f`  
		Last Modified: Thu, 23 Mar 2023 21:18:24 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-standalone` - linux; mips64le

```console
$ docker pull adminer@sha256:14de06501f131ba9f62a814f592d766d6f050b30eab65a15bb1e753a436aab3d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92605785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddae0bdce53fcfedd28644c8fc0df52f38f44000615def4d84b2c88db2aff3ab`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 05:17:18 GMT
ADD file:2337efa705c8772705fa8519e513f4299e72c9eb63e3a68069778ca95a1511e6 in / 
# Thu, 23 Mar 2023 05:17:24 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 20:06:00 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 20:07:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 20:08:02 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 20:08:09 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 20:08:13 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 20:08:16 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 20:08:19 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 20:08:22 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 20:08:26 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 20:09:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 20:09:20 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 20:09:24 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 20:09:27 GMT
USER adminer
# Thu, 23 Mar 2023 20:09:31 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 20:09:34 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:f3951ee58695b4d906b37f2d9a07e6158f66a7328d0c70445d9607cd8367ede0`  
		Last Modified: Thu, 23 Mar 2023 05:25:08 GMT  
		Size: 53.3 MB (53264720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1180d0aa65a6936ad9b336fd7ddf64160d0a95203d7f3d82027fe8912c936d73`  
		Last Modified: Thu, 23 Mar 2023 20:11:59 GMT  
		Size: 38.0 MB (37950695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a23105a66b5d86b4852f9dcf6753d154e1d5b3b76c178cf8baced410a4deb2`  
		Last Modified: Thu, 23 Mar 2023 20:11:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba90b5b3033a3d6ba607430a17c7e37f0fae8f0664ac81a4e571e9ad9fca9e2`  
		Last Modified: Thu, 23 Mar 2023 20:11:33 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b1980d6708cacd2f28ca074bd917c1143a47040b425da5985915850214f197f`  
		Last Modified: Thu, 23 Mar 2023 20:11:33 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfbeda1e7451034cf22503ff221351a0d3f5e1f63a6f11dc71a81450a7aaadd`  
		Last Modified: Thu, 23 Mar 2023 20:11:34 GMT  
		Size: 1.4 MB (1386264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b87439fd13726c64bed775edf40ceb3cbc1b5dbf3f62fb9b127024394aaece4`  
		Last Modified: Thu, 23 Mar 2023 20:11:33 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:ddf406bedb6ea27fd15da89331e085e564dcde0c98ba31f3914b14b4483aa56e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101249875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8b45276387b274e6256e8c13851f3460fdd98b29ca47a09f04a8fad8d02090`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 01:19:25 GMT
ADD file:3eb86af6fda22c3e84548a6d0039be04819ce464b2700e8d8c140be49530ff7c in / 
# Thu, 23 Mar 2023 01:19:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 12:41:38 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 12:42:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 12:42:59 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 12:43:01 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 12:43:01 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 12:43:01 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 12:43:02 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 12:43:02 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 12:43:03 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 12:43:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 12:43:33 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 12:43:33 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 12:43:34 GMT
USER adminer
# Thu, 23 Mar 2023 12:43:35 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 12:43:35 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:566bc84f2641b393ac5a2f4a2ca405c09943aa3ec679f38ea1588f6ee930219e`  
		Last Modified: Thu, 23 Mar 2023 01:23:52 GMT  
		Size: 58.9 MB (58921026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2fbb285bf85ccfbb4c5282ba9f10d09cecbc5a0bab31ef237b51b3201089c2`  
		Last Modified: Thu, 23 Mar 2023 12:45:00 GMT  
		Size: 40.9 MB (40939153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5c4d551007797e513e8983796e921a39828107b5d1309cb2783b12bc6aaac4`  
		Last Modified: Thu, 23 Mar 2023 12:44:46 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19dcdc4ed08a4d33d3c19d3c7a7fcb606bed16f514bbdf68d09ed75d0ef5a039`  
		Last Modified: Thu, 23 Mar 2023 12:44:47 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0187a4a30cb1c249de5010601f0912c92400f91482facb00198f8ba8e3691e`  
		Last Modified: Thu, 23 Mar 2023 12:44:46 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3867a61f6a3237b86e8a6bb431978b79ef5a1320ee3ebe58670b7a68f930c0f`  
		Last Modified: Thu, 23 Mar 2023 12:44:47 GMT  
		Size: 1.4 MB (1385455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553fdd9019949edcff0333970ef2dc5fa9af5479a21e08ecaf14a608524f497f`  
		Last Modified: Thu, 23 Mar 2023 12:44:46 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-standalone` - linux; s390x

```console
$ docker pull adminer@sha256:3a1427b2251efb24343fedded181036a73a9a9edd77c0241f1907db59654d4f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93684414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d7a2d888bb0da291a197f178923752e3a408b6b8002d6ae4d4c8595173ec84`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 00:43:50 GMT
ADD file:1111f9325245c8edccf2d9480c39cf2368f783ad86c2700d452be4e8cbebef8a in / 
# Thu, 23 Mar 2023 00:43:54 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:12:38 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 07:12:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 07:12:59 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 07:12:59 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 07:12:59 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 07:12:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 07:12:59 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 07:12:59 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 07:12:59 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 07:13:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 07:13:07 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 07:13:07 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 07:13:08 GMT
USER adminer
# Thu, 23 Mar 2023 07:13:08 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 07:13:08 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:00dac46cbc44f444bd1dffe5b00a1b239054295b96f7984793273e9d12e75591`  
		Last Modified: Thu, 23 Mar 2023 00:47:04 GMT  
		Size: 53.3 MB (53277499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef40e14df43903a504c3865251eb934e8f644d89890514fc292b06981fca7826`  
		Last Modified: Thu, 23 Mar 2023 07:13:44 GMT  
		Size: 39.0 MB (39017484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f79bdf3c2e58c635953d9f0329b1010a5ff99b977d98975e467b7ab57a155e`  
		Last Modified: Thu, 23 Mar 2023 07:13:37 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ebc836b2a414afb40c1d84fa4fe4af21828a8f07dcbbbfe020a9a2270b0c467`  
		Last Modified: Thu, 23 Mar 2023 07:13:37 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:395b8975dd5a57c4e6e30bccd71a2d34125566cbb50b6000d142e49fb27dc1ea`  
		Last Modified: Thu, 23 Mar 2023 07:13:37 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7cb7770c3999b7b71cb8bd67b1686854b1cf6a8fbd340c7da905fddae466c1`  
		Last Modified: Thu, 23 Mar 2023 07:13:37 GMT  
		Size: 1.4 MB (1385197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47125e4be7b760f757795627cf23bffd8efbadc93fd3f20e13ac58ddac7b2639`  
		Last Modified: Thu, 23 Mar 2023 07:13:37 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:fastcgi`

```console
$ docker pull adminer@sha256:5deda468db781fc1cf37cd89932cca5e14d827305089725caae037d065f9eae9
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
$ docker pull adminer@sha256:35e5285bea82c78b08355dc314739f980e2437cbf1c9e51291b5168fd5cd6f75
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95924422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23fae11ad3f1ae58e8aa6d5af50bb131d52fd3b3fadbb2c8e22e67ceca7a76d7`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:15 GMT
ADD file:459d1e92eb8c24ff4758f974d289ca8a2abe04cf50b6fe2bd760aa4589478289 in / 
# Thu, 23 Mar 2023 01:30:15 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 05:55:49 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 05:56:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 05:56:13 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 05:56:30 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 23 Mar 2023 05:56:30 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 05:56:30 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 05:56:30 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 05:56:30 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 05:56:31 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 05:56:31 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 05:56:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 05:56:41 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 05:56:41 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 05:56:41 GMT
USER adminer
# Thu, 23 Mar 2023 05:56:42 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:3e440a7045683e27f8e2fa04000e0e078d8dfac0c971358ae0f8c65c13321c8e`  
		Last Modified: Thu, 23 Mar 2023 01:34:00 GMT  
		Size: 55.0 MB (55045608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6386bc062c6cf91f6c1451db68015d43a1afd7d67a8f0710050e557777a30a`  
		Last Modified: Thu, 23 Mar 2023 05:57:00 GMT  
		Size: 39.5 MB (39486568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dbc633dab938fa31a0afdfe3ac449318f04eb42e13b59c2602178aed2af127e`  
		Last Modified: Thu, 23 Mar 2023 05:56:53 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15e43c5bb8d604942de8a801fbd515cde458e8296cda94b628a1a311281fe880`  
		Last Modified: Thu, 23 Mar 2023 05:57:17 GMT  
		Size: 2.7 KB (2712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991cbf4d6fdd0b401219e6f0c1474c3c379889e229e8305e5c7afc86459d6599`  
		Last Modified: Thu, 23 Mar 2023 05:57:16 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:420cfe44d3089c8454b9568ad65803581ce9a8565536455cf2602d4b96ff6e35`  
		Last Modified: Thu, 23 Mar 2023 05:57:16 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aad56f1c45901a03ae785f94f8dfc35d5689f400e95502fdf74ee2243dd5fd22`  
		Last Modified: Thu, 23 Mar 2023 05:57:17 GMT  
		Size: 1.4 MB (1385298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36974e24611dd62fec010effb08e11fdd389b0898bff3ee057b6bf9266aa3d8e`  
		Last Modified: Thu, 23 Mar 2023 05:57:16 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; arm variant v5

```console
$ docker pull adminer@sha256:83ad65624afb37bbccd0d59d7d82fc2814210821ac3b1f544cb057038e30a610
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91187641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd884953fb56ddec123031e25c1aef7a0add8ec9d119447de370a5aadc0e2166`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 23 Mar 2023 00:48:37 GMT
ADD file:8419f4bee11379b8aa511da1fe7cdcd6b2cb8c252bc90f76dec672a5b802ea27 in / 
# Thu, 23 Mar 2023 00:48:37 GMT
CMD ["bash"]
# Sat, 25 Mar 2023 02:48:49 GMT
STOPSIGNAL SIGINT
# Sat, 25 Mar 2023 02:49:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Sat, 25 Mar 2023 02:49:17 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Sat, 25 Mar 2023 02:49:47 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Sat, 25 Mar 2023 02:49:48 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 25 Mar 2023 02:49:48 GMT
WORKDIR /var/www/html
# Sat, 25 Mar 2023 02:49:48 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 25 Mar 2023 02:49:48 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 25 Mar 2023 02:49:48 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 25 Mar 2023 02:49:48 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Sat, 25 Mar 2023 02:50:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 25 Mar 2023 02:50:01 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 25 Mar 2023 02:50:01 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 25 Mar 2023 02:50:01 GMT
USER adminer
# Sat, 25 Mar 2023 02:50:01 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:9a8ea6c28ff9e1b5a437e1e5b168873207139672ec8d755939cad00b23349e22`  
		Last Modified: Thu, 23 Mar 2023 02:21:35 GMT  
		Size: 52.5 MB (52549555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeab9bc611f5a84450bb374d38da4707075933d49bf1f7653fd834777749923e`  
		Last Modified: Sat, 25 Mar 2023 02:50:47 GMT  
		Size: 37.2 MB (37246063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e679cbf63988e1866986ea77804721769a09f59bdef7a89368f93a3abd2409`  
		Last Modified: Sat, 25 Mar 2023 02:50:39 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a070ee59349bc1327cf753932c17cc9396004abaf993e6a56c9a2ef071b9d97`  
		Last Modified: Sat, 25 Mar 2023 02:51:03 GMT  
		Size: 2.7 KB (2709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e39741322e4fc4e150bbe02d05ecb189f61fb32138b1a0a34a412390730e6b0a`  
		Last Modified: Sat, 25 Mar 2023 02:51:03 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b7e40e37ad3d10c54c47aac9a2000613f3fc90a30fe6b3166040b3b1d3416d`  
		Last Modified: Sat, 25 Mar 2023 02:51:03 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c99b025114fb17d7175738951a97689c171bbd82cd5177796b12d6d0424699`  
		Last Modified: Sat, 25 Mar 2023 02:51:03 GMT  
		Size: 1.4 MB (1385089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e4611882f0550bdfd18af6aa74746b7a16226506f8cc4951a3b6c05a61e999`  
		Last Modified: Sat, 25 Mar 2023 02:51:02 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:bc666796aa3d0cee0b13bc0afeb827eddb224ac94c2825e90be0b7935f4e8122
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87785110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8477e704cb362785d6fffb06bca6d401c7163028a20adb041de59c8927810ecc`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 23 Mar 2023 01:13:21 GMT
ADD file:fa1cbfdd44274e571cabd5ca7fafa08b17c6f497ecfca6368a9eec4d2527a364 in / 
# Thu, 23 Mar 2023 01:13:22 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 13:53:52 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 13:54:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 13:54:17 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 13:54:32 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 23 Mar 2023 13:54:33 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 13:54:33 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 13:54:33 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 13:54:33 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 13:54:33 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 13:54:33 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 13:54:44 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 13:54:44 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 13:54:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 13:54:44 GMT
USER adminer
# Thu, 23 Mar 2023 13:54:44 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:d50e868f9a626a3c456c0c52c3b013e87619bbac7798ac0c2acf2a2407303125`  
		Last Modified: Thu, 23 Mar 2023 01:33:00 GMT  
		Size: 50.2 MB (50211788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750746172b8a677cb809244c17155d7b05d643b2d816de3d8090ff3593de19ea`  
		Last Modified: Thu, 23 Mar 2023 13:55:03 GMT  
		Size: 36.2 MB (36181275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79543298adbabe76f964cc3578ae398897a0bc10ee8ebf4a0a3338a8ee26b6e8`  
		Last Modified: Thu, 23 Mar 2023 13:54:55 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31633dada050baeaf275a6f4e00621a9f3e3224c8045210053670913ba6d6585`  
		Last Modified: Thu, 23 Mar 2023 13:55:19 GMT  
		Size: 2.7 KB (2709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c21aec687480c0c87c1badd06ad8d1bc38a37d87223bc20a78ba010fd626cac`  
		Last Modified: Thu, 23 Mar 2023 13:55:19 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac9619b29c31046e1d85965461b5a590b86fb5f2f78c27167ec6cfca6f21651e`  
		Last Modified: Thu, 23 Mar 2023 13:55:19 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd30156b59e64f168057bb8a5fae751059636af01bb28f176af27932691211a`  
		Last Modified: Thu, 23 Mar 2023 13:55:20 GMT  
		Size: 1.4 MB (1385116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60631e91dd1890dcbae61adf6317c4a7be616954ef21fec67df71f340de0d351`  
		Last Modified: Thu, 23 Mar 2023 13:55:19 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:7596c184b40a20292868a7080a783453ddf723197fbd6e8c671d314d8b488e24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94337713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e39cf91641fd4f5e8d3515aaa989cebc88d71589b000cc0c7a53339912cb8b5c`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:02 GMT
ADD file:70d18f9eea4e4fbdb941e66490ccb7233e182fe7ded1185de91c7d55580dd13e in / 
# Thu, 23 Mar 2023 00:45:02 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:50:38 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 06:50:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 06:50:57 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 06:51:11 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 23 Mar 2023 06:51:12 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 06:51:12 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 06:51:12 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 06:51:12 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 06:51:12 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 06:51:12 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 06:51:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 06:51:22 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 06:51:22 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 06:51:22 GMT
USER adminer
# Thu, 23 Mar 2023 06:51:22 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:8022b074731d9ecee7f4fba79b993920973811dda168bbc08636f18523b90122`  
		Last Modified: Thu, 23 Mar 2023 00:47:46 GMT  
		Size: 53.7 MB (53703099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98305094c7fd13042b057082ec8d7bcc2b6f08cf0bba01a567b6bc108039bdf1`  
		Last Modified: Thu, 23 Mar 2023 06:51:37 GMT  
		Size: 39.2 MB (39242570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbbb9ddd2e012fdf94f2222f96fe1f8514ec4285c8acff371dd027ca67043c8`  
		Last Modified: Thu, 23 Mar 2023 06:51:30 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed10fa53994213c7460cfbbec9c399e9d8cca8c2aec04202fedff5a70cf2889`  
		Last Modified: Thu, 23 Mar 2023 06:51:52 GMT  
		Size: 2.7 KB (2708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d7483fec2e916d9b95f32278191c4d548eaabe455a3f3ebc0fd94a93216b8f`  
		Last Modified: Thu, 23 Mar 2023 06:51:52 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8280d00d8418fda79bfb9d617fcbe8d8e10e3c43d208cbb6e3559b653a49557d`  
		Last Modified: Thu, 23 Mar 2023 06:51:52 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33939ddffa9123237cf16bfec2e9a607bd843a5bee2d288d4310a31c3194cd1e`  
		Last Modified: Thu, 23 Mar 2023 06:51:53 GMT  
		Size: 1.4 MB (1385099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7183c9f17e4410b0677871e77f993826accf0981aefec7b2a4e3c238c5d657b`  
		Last Modified: Thu, 23 Mar 2023 06:51:52 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:4fec14cf5a78e727b8c74c974ab7d5e4cecd7f2474147a58a4218ddebc02dd87
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96978049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b0466b7b74fdb561f8edf82d5292c2ae17b67cdff6e3c10539493ba7fd11f3`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 23 Mar 2023 00:39:08 GMT
ADD file:f331251c4c21fceff56d13f76442a6334dc355c29ec7450768c1c86a3db1adab in / 
# Thu, 23 Mar 2023 00:39:09 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 21:17:12 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 21:17:40 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 21:17:41 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 21:18:01 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 23 Mar 2023 21:18:01 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 21:18:01 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 21:18:02 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 21:18:02 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 21:18:02 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 21:18:02 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 21:18:14 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 21:18:14 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 21:18:14 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 21:18:14 GMT
USER adminer
# Thu, 23 Mar 2023 21:18:14 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:c1bb878cff31d37952c5c73ed15c167f599bb7f97b3eeaa1a17352b2473b3394`  
		Last Modified: Thu, 23 Mar 2023 00:42:44 GMT  
		Size: 56.0 MB (56027911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67239d163b3f7b443f91919b613775ed043520e6b06b413a9628905d01e98992`  
		Last Modified: Thu, 23 Mar 2023 21:18:34 GMT  
		Size: 39.6 MB (39558048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88061812377dcf7351518633da4694430dfe02ac13bdbc48516d26c18586a0d5`  
		Last Modified: Thu, 23 Mar 2023 21:18:24 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e265f46cc6fadbfde249ce57b0f1b54264aab3a0c6a1453f7f2699545e0b3204`  
		Last Modified: Thu, 23 Mar 2023 21:18:50 GMT  
		Size: 2.7 KB (2710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca518b34b603a08f7c5881dd84c944bb8236eb9f03a74636f1d2496138c0f756`  
		Last Modified: Thu, 23 Mar 2023 21:18:50 GMT  
		Size: 1.9 KB (1869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c12e6b62649c51d5b810142e53b66da078b62baadc21eecf203444c93de1263`  
		Last Modified: Thu, 23 Mar 2023 21:18:50 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f8a77bc64220b5352e77dfca8700a11755ee9d00cb280da618809bcaefc541`  
		Last Modified: Thu, 23 Mar 2023 21:18:50 GMT  
		Size: 1.4 MB (1385152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9c79da4d828244f71b3b0c18abe0d34506e6202fb0c07c7b38bcb553ff9361`  
		Last Modified: Thu, 23 Mar 2023 21:18:50 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; mips64le

```console
$ docker pull adminer@sha256:6071b807c18fd9c3a868729b6c008a72c4f33193d038d3266c552a13c81c2ebe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92608465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8730ff222f47754b556a9a28db99999e3b00e5f51261ff97b8c794f168b61cdf`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 23 Mar 2023 05:17:18 GMT
ADD file:2337efa705c8772705fa8519e513f4299e72c9eb63e3a68069778ca95a1511e6 in / 
# Thu, 23 Mar 2023 05:17:24 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 20:06:00 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 20:07:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 20:08:02 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 20:09:46 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 23 Mar 2023 20:09:52 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 20:09:56 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 20:09:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 20:10:02 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 20:10:06 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 20:10:09 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 20:11:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 20:11:04 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 20:11:08 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 20:11:11 GMT
USER adminer
# Thu, 23 Mar 2023 20:11:14 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:f3951ee58695b4d906b37f2d9a07e6158f66a7328d0c70445d9607cd8367ede0`  
		Last Modified: Thu, 23 Mar 2023 05:25:08 GMT  
		Size: 53.3 MB (53264720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1180d0aa65a6936ad9b336fd7ddf64160d0a95203d7f3d82027fe8912c936d73`  
		Last Modified: Thu, 23 Mar 2023 20:11:59 GMT  
		Size: 38.0 MB (37950695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a23105a66b5d86b4852f9dcf6753d154e1d5b3b76c178cf8baced410a4deb2`  
		Last Modified: Thu, 23 Mar 2023 20:11:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f6b792b9dbc62affd1f59a5c64bae91e7a40650b891a2227ee50499b244671`  
		Last Modified: Thu, 23 Mar 2023 20:12:18 GMT  
		Size: 2.7 KB (2713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bd7b3264510c2ff115b5bde0691e4507a8037e8afac4227a80c9b20927cd71`  
		Last Modified: Thu, 23 Mar 2023 20:12:18 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede1a6707d65116cd7175d9a72eb51517e94fd922e91749a84b539c88f0c1cbc`  
		Last Modified: Thu, 23 Mar 2023 20:12:18 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532cd52f2b4a83b3f92484a39a21601e8bcf404137a7665b958c9589d2a56c97`  
		Last Modified: Thu, 23 Mar 2023 20:12:19 GMT  
		Size: 1.4 MB (1386242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:799eb60dea8fba148d5d409a75beb6c1f6decb8507259a122daedabe15408244`  
		Last Modified: Thu, 23 Mar 2023 20:12:18 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:e8c3e0fd2be16699af072a6eb61d32ad6743ed74ba014f197f781e6626136e8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101252603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3cc4b2c295df05bffd40f80bc7f0829e1bee38b774903a1c79561b01d3c25a8`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 23 Mar 2023 01:19:25 GMT
ADD file:3eb86af6fda22c3e84548a6d0039be04819ce464b2700e8d8c140be49530ff7c in / 
# Thu, 23 Mar 2023 01:19:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 12:41:38 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 12:42:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 12:42:59 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 12:43:48 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 23 Mar 2023 12:43:50 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 12:43:51 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 12:43:51 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 12:43:52 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 12:43:53 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 12:43:54 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 12:44:25 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 12:44:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 12:44:27 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 12:44:27 GMT
USER adminer
# Thu, 23 Mar 2023 12:44:28 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:566bc84f2641b393ac5a2f4a2ca405c09943aa3ec679f38ea1588f6ee930219e`  
		Last Modified: Thu, 23 Mar 2023 01:23:52 GMT  
		Size: 58.9 MB (58921026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2fbb285bf85ccfbb4c5282ba9f10d09cecbc5a0bab31ef237b51b3201089c2`  
		Last Modified: Thu, 23 Mar 2023 12:45:00 GMT  
		Size: 40.9 MB (40939153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5c4d551007797e513e8983796e921a39828107b5d1309cb2783b12bc6aaac4`  
		Last Modified: Thu, 23 Mar 2023 12:44:46 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a981786b6703fc32d30f8d08bcc4e47bc3359d29ec0b8ad35e1815c6e43f95`  
		Last Modified: Thu, 23 Mar 2023 12:45:18 GMT  
		Size: 2.7 KB (2711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b538b21119d1b99f45b99c3482fbc3815a12ff274279e57de7f322366ac5a064`  
		Last Modified: Thu, 23 Mar 2023 12:45:18 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f469564ebedfa716940bf361e3f4e958f5760932c5afc56a10524d0f633f1e90`  
		Last Modified: Thu, 23 Mar 2023 12:45:18 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e96f627d9a4deaae5faff7c9935f1dbc2bbe05dccc2d627c79cb48f600de895`  
		Last Modified: Thu, 23 Mar 2023 12:45:19 GMT  
		Size: 1.4 MB (1385464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf7d927e154813af62ae740af92fe128baf1c4372c852b3600355800ebc4636`  
		Last Modified: Thu, 23 Mar 2023 12:45:18 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; s390x

```console
$ docker pull adminer@sha256:44709f3540da7398591b1e5e2e96af71000ca46ab83e50d64901e0b4d7cea28b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93687112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c143ca3a2b00fef62f75a55e8ec15ee516c01070c860f9ec12c57d5c7f1196`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 23 Mar 2023 00:43:50 GMT
ADD file:1111f9325245c8edccf2d9480c39cf2368f783ad86c2700d452be4e8cbebef8a in / 
# Thu, 23 Mar 2023 00:43:54 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:12:38 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 07:12:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 07:12:59 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 07:13:14 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 23 Mar 2023 07:13:14 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 07:13:14 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 07:13:15 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 07:13:15 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 07:13:15 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 07:13:15 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 07:13:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 07:13:23 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 07:13:23 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 07:13:23 GMT
USER adminer
# Thu, 23 Mar 2023 07:13:23 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:00dac46cbc44f444bd1dffe5b00a1b239054295b96f7984793273e9d12e75591`  
		Last Modified: Thu, 23 Mar 2023 00:47:04 GMT  
		Size: 53.3 MB (53277499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef40e14df43903a504c3865251eb934e8f644d89890514fc292b06981fca7826`  
		Last Modified: Thu, 23 Mar 2023 07:13:44 GMT  
		Size: 39.0 MB (39017484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f79bdf3c2e58c635953d9f0329b1010a5ff99b977d98975e467b7ab57a155e`  
		Last Modified: Thu, 23 Mar 2023 07:13:37 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a99c25318d8aa437b51f90c7016573b6f47e86afa9443badc88e8d1e03a23fd`  
		Last Modified: Thu, 23 Mar 2023 07:13:53 GMT  
		Size: 2.7 KB (2712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446aa9007ef953ba5564a78772fc6cdebc498a99f3886fd21e2d62598591aa84`  
		Last Modified: Thu, 23 Mar 2023 07:13:53 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548528b8aa2488b1c52162c3f227b73f2af8c56b1df973565066e37ee4295939`  
		Last Modified: Thu, 23 Mar 2023 07:13:53 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b53cd708608bcb6d8d6e0638c077f3c2544501bce3b0103d029da761aa9dd3`  
		Last Modified: Thu, 23 Mar 2023 07:13:54 GMT  
		Size: 1.4 MB (1385185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83e4966551f089235a491b28f9fb699ef37fe5dc8c27f816f6fa9ca6b1cbdaa`  
		Last Modified: Thu, 23 Mar 2023 07:13:53 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:latest`

```console
$ docker pull adminer@sha256:4203fd6bcd82fe25dceaf8acb4826129cf7a6e93b22a5ab2fc0ec5a7cdaca3f4
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

### `adminer:latest` - linux; amd64

```console
$ docker pull adminer@sha256:b5570962c3a9981b6572e61dd33f5cbd394a1a9d27ee6342b4241338af330449
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95921691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e1b3241b20061365693574e1c1241f64a48b15a7f439b8df760456d83009c7`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:15 GMT
ADD file:459d1e92eb8c24ff4758f974d289ca8a2abe04cf50b6fe2bd760aa4589478289 in / 
# Thu, 23 Mar 2023 01:30:15 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 05:55:49 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 05:56:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 05:56:13 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 05:56:14 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 05:56:14 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 05:56:14 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 05:56:14 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 05:56:14 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 05:56:14 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 05:56:25 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 05:56:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 05:56:26 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 05:56:26 GMT
USER adminer
# Thu, 23 Mar 2023 05:56:26 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 05:56:26 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:3e440a7045683e27f8e2fa04000e0e078d8dfac0c971358ae0f8c65c13321c8e`  
		Last Modified: Thu, 23 Mar 2023 01:34:00 GMT  
		Size: 55.0 MB (55045608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6386bc062c6cf91f6c1451db68015d43a1afd7d67a8f0710050e557777a30a`  
		Last Modified: Thu, 23 Mar 2023 05:57:00 GMT  
		Size: 39.5 MB (39486568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dbc633dab938fa31a0afdfe3ac449318f04eb42e13b59c2602178aed2af127e`  
		Last Modified: Thu, 23 Mar 2023 05:56:53 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39317196bba2d873b239492ba23f8f1d62f89b661fb1760b65f29b1404322c60`  
		Last Modified: Thu, 23 Mar 2023 05:56:53 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ea8e1da1f9854a8c3bf43a78f5b403bdfad3f2c2861edfbfd902566950a7a2`  
		Last Modified: Thu, 23 Mar 2023 05:56:53 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ce0ac056362cd982a31febaaf97daa568c31c2e95f1f4265e82cc6fbeaffd4`  
		Last Modified: Thu, 23 Mar 2023 05:56:53 GMT  
		Size: 1.4 MB (1385271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3ee3b23021de0471ff83e0b10babf764acf8f57dbb17c2eef966f084eb314a`  
		Last Modified: Thu, 23 Mar 2023 05:56:53 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; arm variant v5

```console
$ docker pull adminer@sha256:4344599d09a3a9134c3a42f59ad31606dd3e8952bb9ae5d72d64dc5297cdc6bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91184910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512e73052fee795753bdd64cababc1bcc5ccdc4ce7ae0391a67a4013d1b98432`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 00:48:37 GMT
ADD file:8419f4bee11379b8aa511da1fe7cdcd6b2cb8c252bc90f76dec672a5b802ea27 in / 
# Thu, 23 Mar 2023 00:48:37 GMT
CMD ["bash"]
# Sat, 25 Mar 2023 02:48:49 GMT
STOPSIGNAL SIGINT
# Sat, 25 Mar 2023 02:49:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Sat, 25 Mar 2023 02:49:17 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Sat, 25 Mar 2023 02:49:17 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 25 Mar 2023 02:49:17 GMT
WORKDIR /var/www/html
# Sat, 25 Mar 2023 02:49:18 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 25 Mar 2023 02:49:18 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 25 Mar 2023 02:49:18 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 25 Mar 2023 02:49:18 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Sat, 25 Mar 2023 02:49:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 25 Mar 2023 02:49:30 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 25 Mar 2023 02:49:30 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 25 Mar 2023 02:49:30 GMT
USER adminer
# Sat, 25 Mar 2023 02:49:30 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 25 Mar 2023 02:49:30 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:9a8ea6c28ff9e1b5a437e1e5b168873207139672ec8d755939cad00b23349e22`  
		Last Modified: Thu, 23 Mar 2023 02:21:35 GMT  
		Size: 52.5 MB (52549555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeab9bc611f5a84450bb374d38da4707075933d49bf1f7653fd834777749923e`  
		Last Modified: Sat, 25 Mar 2023 02:50:47 GMT  
		Size: 37.2 MB (37246063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e679cbf63988e1866986ea77804721769a09f59bdef7a89368f93a3abd2409`  
		Last Modified: Sat, 25 Mar 2023 02:50:39 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7959eefb479c10f4ab8829bcc4ee81ce479a5bff4f3d776e2d684522e56d36c`  
		Last Modified: Sat, 25 Mar 2023 02:50:39 GMT  
		Size: 1.9 KB (1865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b261a380e55719d974d3c7d0d3816f93ba071f56ab2669b4e941c91a49aa11c9`  
		Last Modified: Sat, 25 Mar 2023 02:50:39 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f7d098a043908e9b0872735983e550db864960c2b9998a675db2c956a02a60`  
		Last Modified: Sat, 25 Mar 2023 02:50:39 GMT  
		Size: 1.4 MB (1385072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a8d1397cd986a98157defb67fbca51bfe84b0d994ad3b7e2199a9d4adb3bf5`  
		Last Modified: Sat, 25 Mar 2023 02:50:39 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; arm variant v7

```console
$ docker pull adminer@sha256:208e28dc00b696fd2786ae0fac00bbac135df7d327a78f1a3b07b430e8be29fa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87782361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924e553786350523e3dabd52a79ebaa532e1ee1f1cd4f55c123b6f2debfd887b`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 01:13:21 GMT
ADD file:fa1cbfdd44274e571cabd5ca7fafa08b17c6f497ecfca6368a9eec4d2527a364 in / 
# Thu, 23 Mar 2023 01:13:22 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 13:53:52 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 13:54:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 13:54:17 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 13:54:17 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 13:54:18 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 13:54:18 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 13:54:18 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 13:54:18 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 13:54:18 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 13:54:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 13:54:30 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 13:54:30 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 13:54:30 GMT
USER adminer
# Thu, 23 Mar 2023 13:54:30 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 13:54:30 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:d50e868f9a626a3c456c0c52c3b013e87619bbac7798ac0c2acf2a2407303125`  
		Last Modified: Thu, 23 Mar 2023 01:33:00 GMT  
		Size: 50.2 MB (50211788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750746172b8a677cb809244c17155d7b05d643b2d816de3d8090ff3593de19ea`  
		Last Modified: Thu, 23 Mar 2023 13:55:03 GMT  
		Size: 36.2 MB (36181275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79543298adbabe76f964cc3578ae398897a0bc10ee8ebf4a0a3338a8ee26b6e8`  
		Last Modified: Thu, 23 Mar 2023 13:54:55 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7b7c098bbce560d98941c87164725c63999c701f19f2500e91578c8d994c8f`  
		Last Modified: Thu, 23 Mar 2023 13:54:56 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90441e257dd07454f7d03e5aa41e80d43c14256ff5040356a29d4639b23d75fc`  
		Last Modified: Thu, 23 Mar 2023 13:54:55 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65767342491a731ec4afa7560fd1b162f1ea5c932fc69e8326baad4bec228e7e`  
		Last Modified: Thu, 23 Mar 2023 13:54:56 GMT  
		Size: 1.4 MB (1385066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a8450e329b8116e25e9fa7cb6b678d57084c5946b3167f2cb126880295263a`  
		Last Modified: Thu, 23 Mar 2023 13:54:55 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:7fe9245eaab6579d2f02b2c43ece653c6f014f78be767a77580df6401023b8b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94334964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da1ba2cdb7c1dcd745eda1a855a3c5d0cc50e77182d900a1a13fab7ecb94f0f1`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:02 GMT
ADD file:70d18f9eea4e4fbdb941e66490ccb7233e182fe7ded1185de91c7d55580dd13e in / 
# Thu, 23 Mar 2023 00:45:02 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:50:38 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 06:50:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 06:50:57 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 06:50:57 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 06:50:58 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 06:50:58 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 06:50:58 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 06:50:58 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 06:50:58 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 06:51:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 06:51:08 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 06:51:08 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 06:51:08 GMT
USER adminer
# Thu, 23 Mar 2023 06:51:08 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 06:51:08 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:8022b074731d9ecee7f4fba79b993920973811dda168bbc08636f18523b90122`  
		Last Modified: Thu, 23 Mar 2023 00:47:46 GMT  
		Size: 53.7 MB (53703099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98305094c7fd13042b057082ec8d7bcc2b6f08cf0bba01a567b6bc108039bdf1`  
		Last Modified: Thu, 23 Mar 2023 06:51:37 GMT  
		Size: 39.2 MB (39242570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbbb9ddd2e012fdf94f2222f96fe1f8514ec4285c8acff371dd027ca67043c8`  
		Last Modified: Thu, 23 Mar 2023 06:51:30 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b3fa21b5eaa269a0e522ee6faa17c1942a9eb531a85d65093c785db3bf4ca32`  
		Last Modified: Thu, 23 Mar 2023 06:51:30 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbcc9aba89fb8cb163ab7c6f00eaee21df2f499f9cfbb89de3b18e5f24ba0087`  
		Last Modified: Thu, 23 Mar 2023 06:51:30 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf77c8ff22b40bbe616794e9d54103a4a9648107d69c9057deb1a83342d3d58`  
		Last Modified: Thu, 23 Mar 2023 06:51:31 GMT  
		Size: 1.4 MB (1385053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bd969a23b87a5402679ff8373fd3e9ce7af9a3e999bad556fe0cc25dda1cc6`  
		Last Modified: Thu, 23 Mar 2023 06:51:30 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; 386

```console
$ docker pull adminer@sha256:ca2ee65836fd06aba737873c17718cd1ae4e52f6ba9a2869000be6794922ec0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96975396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47306ce39706e8ed333600b8d4399cb09c02ffe4e169f76bd59fa5b6569ae778`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 00:39:08 GMT
ADD file:f331251c4c21fceff56d13f76442a6334dc355c29ec7450768c1c86a3db1adab in / 
# Thu, 23 Mar 2023 00:39:09 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 21:17:12 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 21:17:40 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 21:17:41 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 21:17:41 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 21:17:41 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 21:17:42 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 21:17:42 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 21:17:42 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 21:17:42 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 21:17:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 21:17:54 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 21:17:54 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 21:17:54 GMT
USER adminer
# Thu, 23 Mar 2023 21:17:55 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 21:17:55 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:c1bb878cff31d37952c5c73ed15c167f599bb7f97b3eeaa1a17352b2473b3394`  
		Last Modified: Thu, 23 Mar 2023 00:42:44 GMT  
		Size: 56.0 MB (56027911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67239d163b3f7b443f91919b613775ed043520e6b06b413a9628905d01e98992`  
		Last Modified: Thu, 23 Mar 2023 21:18:34 GMT  
		Size: 39.6 MB (39558048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88061812377dcf7351518633da4694430dfe02ac13bdbc48516d26c18586a0d5`  
		Last Modified: Thu, 23 Mar 2023 21:18:24 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c664bb8231af50f8a98b457a9e7c291444345b0066ed54ddbcc0b2129859965`  
		Last Modified: Thu, 23 Mar 2023 21:18:24 GMT  
		Size: 1.9 KB (1869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a209358917bcf344993c93aad3b156d6a09b6ab64d43df3941ca51e6c414b9`  
		Last Modified: Thu, 23 Mar 2023 21:18:24 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061ad9c8d5ae0dc7e0d69094e0f6d09b29dea00ec113641833b5a37f404de058`  
		Last Modified: Thu, 23 Mar 2023 21:18:24 GMT  
		Size: 1.4 MB (1385210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2761eeb066c4b63e66ada920b87fc430284439f4c76fac14a274ef528430d3f`  
		Last Modified: Thu, 23 Mar 2023 21:18:24 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; mips64le

```console
$ docker pull adminer@sha256:14de06501f131ba9f62a814f592d766d6f050b30eab65a15bb1e753a436aab3d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92605785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddae0bdce53fcfedd28644c8fc0df52f38f44000615def4d84b2c88db2aff3ab`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 05:17:18 GMT
ADD file:2337efa705c8772705fa8519e513f4299e72c9eb63e3a68069778ca95a1511e6 in / 
# Thu, 23 Mar 2023 05:17:24 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 20:06:00 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 20:07:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 20:08:02 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 20:08:09 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 20:08:13 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 20:08:16 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 20:08:19 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 20:08:22 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 20:08:26 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 20:09:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 20:09:20 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 20:09:24 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 20:09:27 GMT
USER adminer
# Thu, 23 Mar 2023 20:09:31 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 20:09:34 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:f3951ee58695b4d906b37f2d9a07e6158f66a7328d0c70445d9607cd8367ede0`  
		Last Modified: Thu, 23 Mar 2023 05:25:08 GMT  
		Size: 53.3 MB (53264720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1180d0aa65a6936ad9b336fd7ddf64160d0a95203d7f3d82027fe8912c936d73`  
		Last Modified: Thu, 23 Mar 2023 20:11:59 GMT  
		Size: 38.0 MB (37950695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a23105a66b5d86b4852f9dcf6753d154e1d5b3b76c178cf8baced410a4deb2`  
		Last Modified: Thu, 23 Mar 2023 20:11:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba90b5b3033a3d6ba607430a17c7e37f0fae8f0664ac81a4e571e9ad9fca9e2`  
		Last Modified: Thu, 23 Mar 2023 20:11:33 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b1980d6708cacd2f28ca074bd917c1143a47040b425da5985915850214f197f`  
		Last Modified: Thu, 23 Mar 2023 20:11:33 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfbeda1e7451034cf22503ff221351a0d3f5e1f63a6f11dc71a81450a7aaadd`  
		Last Modified: Thu, 23 Mar 2023 20:11:34 GMT  
		Size: 1.4 MB (1386264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b87439fd13726c64bed775edf40ceb3cbc1b5dbf3f62fb9b127024394aaece4`  
		Last Modified: Thu, 23 Mar 2023 20:11:33 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; ppc64le

```console
$ docker pull adminer@sha256:ddf406bedb6ea27fd15da89331e085e564dcde0c98ba31f3914b14b4483aa56e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101249875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8b45276387b274e6256e8c13851f3460fdd98b29ca47a09f04a8fad8d02090`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 01:19:25 GMT
ADD file:3eb86af6fda22c3e84548a6d0039be04819ce464b2700e8d8c140be49530ff7c in / 
# Thu, 23 Mar 2023 01:19:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 12:41:38 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 12:42:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 12:42:59 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 12:43:01 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 12:43:01 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 12:43:01 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 12:43:02 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 12:43:02 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 12:43:03 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 12:43:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 12:43:33 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 12:43:33 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 12:43:34 GMT
USER adminer
# Thu, 23 Mar 2023 12:43:35 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 12:43:35 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:566bc84f2641b393ac5a2f4a2ca405c09943aa3ec679f38ea1588f6ee930219e`  
		Last Modified: Thu, 23 Mar 2023 01:23:52 GMT  
		Size: 58.9 MB (58921026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2fbb285bf85ccfbb4c5282ba9f10d09cecbc5a0bab31ef237b51b3201089c2`  
		Last Modified: Thu, 23 Mar 2023 12:45:00 GMT  
		Size: 40.9 MB (40939153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5c4d551007797e513e8983796e921a39828107b5d1309cb2783b12bc6aaac4`  
		Last Modified: Thu, 23 Mar 2023 12:44:46 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19dcdc4ed08a4d33d3c19d3c7a7fcb606bed16f514bbdf68d09ed75d0ef5a039`  
		Last Modified: Thu, 23 Mar 2023 12:44:47 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0187a4a30cb1c249de5010601f0912c92400f91482facb00198f8ba8e3691e`  
		Last Modified: Thu, 23 Mar 2023 12:44:46 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3867a61f6a3237b86e8a6bb431978b79ef5a1320ee3ebe58670b7a68f930c0f`  
		Last Modified: Thu, 23 Mar 2023 12:44:47 GMT  
		Size: 1.4 MB (1385455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553fdd9019949edcff0333970ef2dc5fa9af5479a21e08ecaf14a608524f497f`  
		Last Modified: Thu, 23 Mar 2023 12:44:46 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; s390x

```console
$ docker pull adminer@sha256:3a1427b2251efb24343fedded181036a73a9a9edd77c0241f1907db59654d4f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93684414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d7a2d888bb0da291a197f178923752e3a408b6b8002d6ae4d4c8595173ec84`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 00:43:50 GMT
ADD file:1111f9325245c8edccf2d9480c39cf2368f783ad86c2700d452be4e8cbebef8a in / 
# Thu, 23 Mar 2023 00:43:54 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:12:38 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 07:12:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 07:12:59 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 07:12:59 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 07:12:59 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 07:12:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 07:12:59 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 07:12:59 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 07:12:59 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 07:13:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 07:13:07 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 07:13:07 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 07:13:08 GMT
USER adminer
# Thu, 23 Mar 2023 07:13:08 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 07:13:08 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:00dac46cbc44f444bd1dffe5b00a1b239054295b96f7984793273e9d12e75591`  
		Last Modified: Thu, 23 Mar 2023 00:47:04 GMT  
		Size: 53.3 MB (53277499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef40e14df43903a504c3865251eb934e8f644d89890514fc292b06981fca7826`  
		Last Modified: Thu, 23 Mar 2023 07:13:44 GMT  
		Size: 39.0 MB (39017484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f79bdf3c2e58c635953d9f0329b1010a5ff99b977d98975e467b7ab57a155e`  
		Last Modified: Thu, 23 Mar 2023 07:13:37 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ebc836b2a414afb40c1d84fa4fe4af21828a8f07dcbbbfe020a9a2270b0c467`  
		Last Modified: Thu, 23 Mar 2023 07:13:37 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:395b8975dd5a57c4e6e30bccd71a2d34125566cbb50b6000d142e49fb27dc1ea`  
		Last Modified: Thu, 23 Mar 2023 07:13:37 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7cb7770c3999b7b71cb8bd67b1686854b1cf6a8fbd340c7da905fddae466c1`  
		Last Modified: Thu, 23 Mar 2023 07:13:37 GMT  
		Size: 1.4 MB (1385197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47125e4be7b760f757795627cf23bffd8efbadc93fd3f20e13ac58ddac7b2639`  
		Last Modified: Thu, 23 Mar 2023 07:13:37 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:standalone`

```console
$ docker pull adminer@sha256:4203fd6bcd82fe25dceaf8acb4826129cf7a6e93b22a5ab2fc0ec5a7cdaca3f4
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

### `adminer:standalone` - linux; amd64

```console
$ docker pull adminer@sha256:b5570962c3a9981b6572e61dd33f5cbd394a1a9d27ee6342b4241338af330449
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95921691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e1b3241b20061365693574e1c1241f64a48b15a7f439b8df760456d83009c7`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:15 GMT
ADD file:459d1e92eb8c24ff4758f974d289ca8a2abe04cf50b6fe2bd760aa4589478289 in / 
# Thu, 23 Mar 2023 01:30:15 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 05:55:49 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 05:56:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 05:56:13 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 05:56:14 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 05:56:14 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 05:56:14 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 05:56:14 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 05:56:14 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 05:56:14 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 05:56:25 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 05:56:26 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 05:56:26 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 05:56:26 GMT
USER adminer
# Thu, 23 Mar 2023 05:56:26 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 05:56:26 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:3e440a7045683e27f8e2fa04000e0e078d8dfac0c971358ae0f8c65c13321c8e`  
		Last Modified: Thu, 23 Mar 2023 01:34:00 GMT  
		Size: 55.0 MB (55045608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6386bc062c6cf91f6c1451db68015d43a1afd7d67a8f0710050e557777a30a`  
		Last Modified: Thu, 23 Mar 2023 05:57:00 GMT  
		Size: 39.5 MB (39486568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dbc633dab938fa31a0afdfe3ac449318f04eb42e13b59c2602178aed2af127e`  
		Last Modified: Thu, 23 Mar 2023 05:56:53 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39317196bba2d873b239492ba23f8f1d62f89b661fb1760b65f29b1404322c60`  
		Last Modified: Thu, 23 Mar 2023 05:56:53 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ea8e1da1f9854a8c3bf43a78f5b403bdfad3f2c2861edfbfd902566950a7a2`  
		Last Modified: Thu, 23 Mar 2023 05:56:53 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ce0ac056362cd982a31febaaf97daa568c31c2e95f1f4265e82cc6fbeaffd4`  
		Last Modified: Thu, 23 Mar 2023 05:56:53 GMT  
		Size: 1.4 MB (1385271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3ee3b23021de0471ff83e0b10babf764acf8f57dbb17c2eef966f084eb314a`  
		Last Modified: Thu, 23 Mar 2023 05:56:53 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; arm variant v5

```console
$ docker pull adminer@sha256:4344599d09a3a9134c3a42f59ad31606dd3e8952bb9ae5d72d64dc5297cdc6bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91184910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:512e73052fee795753bdd64cababc1bcc5ccdc4ce7ae0391a67a4013d1b98432`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 00:48:37 GMT
ADD file:8419f4bee11379b8aa511da1fe7cdcd6b2cb8c252bc90f76dec672a5b802ea27 in / 
# Thu, 23 Mar 2023 00:48:37 GMT
CMD ["bash"]
# Sat, 25 Mar 2023 02:48:49 GMT
STOPSIGNAL SIGINT
# Sat, 25 Mar 2023 02:49:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Sat, 25 Mar 2023 02:49:17 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Sat, 25 Mar 2023 02:49:17 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 25 Mar 2023 02:49:17 GMT
WORKDIR /var/www/html
# Sat, 25 Mar 2023 02:49:18 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 25 Mar 2023 02:49:18 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 25 Mar 2023 02:49:18 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 25 Mar 2023 02:49:18 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Sat, 25 Mar 2023 02:49:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 25 Mar 2023 02:49:30 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 25 Mar 2023 02:49:30 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 25 Mar 2023 02:49:30 GMT
USER adminer
# Sat, 25 Mar 2023 02:49:30 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 25 Mar 2023 02:49:30 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:9a8ea6c28ff9e1b5a437e1e5b168873207139672ec8d755939cad00b23349e22`  
		Last Modified: Thu, 23 Mar 2023 02:21:35 GMT  
		Size: 52.5 MB (52549555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeab9bc611f5a84450bb374d38da4707075933d49bf1f7653fd834777749923e`  
		Last Modified: Sat, 25 Mar 2023 02:50:47 GMT  
		Size: 37.2 MB (37246063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e679cbf63988e1866986ea77804721769a09f59bdef7a89368f93a3abd2409`  
		Last Modified: Sat, 25 Mar 2023 02:50:39 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7959eefb479c10f4ab8829bcc4ee81ce479a5bff4f3d776e2d684522e56d36c`  
		Last Modified: Sat, 25 Mar 2023 02:50:39 GMT  
		Size: 1.9 KB (1865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b261a380e55719d974d3c7d0d3816f93ba071f56ab2669b4e941c91a49aa11c9`  
		Last Modified: Sat, 25 Mar 2023 02:50:39 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f7d098a043908e9b0872735983e550db864960c2b9998a675db2c956a02a60`  
		Last Modified: Sat, 25 Mar 2023 02:50:39 GMT  
		Size: 1.4 MB (1385072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a8d1397cd986a98157defb67fbca51bfe84b0d994ad3b7e2199a9d4adb3bf5`  
		Last Modified: Sat, 25 Mar 2023 02:50:39 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:208e28dc00b696fd2786ae0fac00bbac135df7d327a78f1a3b07b430e8be29fa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87782361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924e553786350523e3dabd52a79ebaa532e1ee1f1cd4f55c123b6f2debfd887b`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 01:13:21 GMT
ADD file:fa1cbfdd44274e571cabd5ca7fafa08b17c6f497ecfca6368a9eec4d2527a364 in / 
# Thu, 23 Mar 2023 01:13:22 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 13:53:52 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 13:54:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 13:54:17 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 13:54:17 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 13:54:18 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 13:54:18 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 13:54:18 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 13:54:18 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 13:54:18 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 13:54:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 13:54:30 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 13:54:30 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 13:54:30 GMT
USER adminer
# Thu, 23 Mar 2023 13:54:30 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 13:54:30 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:d50e868f9a626a3c456c0c52c3b013e87619bbac7798ac0c2acf2a2407303125`  
		Last Modified: Thu, 23 Mar 2023 01:33:00 GMT  
		Size: 50.2 MB (50211788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750746172b8a677cb809244c17155d7b05d643b2d816de3d8090ff3593de19ea`  
		Last Modified: Thu, 23 Mar 2023 13:55:03 GMT  
		Size: 36.2 MB (36181275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79543298adbabe76f964cc3578ae398897a0bc10ee8ebf4a0a3338a8ee26b6e8`  
		Last Modified: Thu, 23 Mar 2023 13:54:55 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7b7c098bbce560d98941c87164725c63999c701f19f2500e91578c8d994c8f`  
		Last Modified: Thu, 23 Mar 2023 13:54:56 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90441e257dd07454f7d03e5aa41e80d43c14256ff5040356a29d4639b23d75fc`  
		Last Modified: Thu, 23 Mar 2023 13:54:55 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65767342491a731ec4afa7560fd1b162f1ea5c932fc69e8326baad4bec228e7e`  
		Last Modified: Thu, 23 Mar 2023 13:54:56 GMT  
		Size: 1.4 MB (1385066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a8450e329b8116e25e9fa7cb6b678d57084c5946b3167f2cb126880295263a`  
		Last Modified: Thu, 23 Mar 2023 13:54:55 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:7fe9245eaab6579d2f02b2c43ece653c6f014f78be767a77580df6401023b8b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94334964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da1ba2cdb7c1dcd745eda1a855a3c5d0cc50e77182d900a1a13fab7ecb94f0f1`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:02 GMT
ADD file:70d18f9eea4e4fbdb941e66490ccb7233e182fe7ded1185de91c7d55580dd13e in / 
# Thu, 23 Mar 2023 00:45:02 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:50:38 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 06:50:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 06:50:57 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 06:50:57 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 06:50:58 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 06:50:58 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 06:50:58 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 06:50:58 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 06:50:58 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 06:51:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 06:51:08 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 06:51:08 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 06:51:08 GMT
USER adminer
# Thu, 23 Mar 2023 06:51:08 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 06:51:08 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:8022b074731d9ecee7f4fba79b993920973811dda168bbc08636f18523b90122`  
		Last Modified: Thu, 23 Mar 2023 00:47:46 GMT  
		Size: 53.7 MB (53703099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98305094c7fd13042b057082ec8d7bcc2b6f08cf0bba01a567b6bc108039bdf1`  
		Last Modified: Thu, 23 Mar 2023 06:51:37 GMT  
		Size: 39.2 MB (39242570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbbb9ddd2e012fdf94f2222f96fe1f8514ec4285c8acff371dd027ca67043c8`  
		Last Modified: Thu, 23 Mar 2023 06:51:30 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b3fa21b5eaa269a0e522ee6faa17c1942a9eb531a85d65093c785db3bf4ca32`  
		Last Modified: Thu, 23 Mar 2023 06:51:30 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbcc9aba89fb8cb163ab7c6f00eaee21df2f499f9cfbb89de3b18e5f24ba0087`  
		Last Modified: Thu, 23 Mar 2023 06:51:30 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf77c8ff22b40bbe616794e9d54103a4a9648107d69c9057deb1a83342d3d58`  
		Last Modified: Thu, 23 Mar 2023 06:51:31 GMT  
		Size: 1.4 MB (1385053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bd969a23b87a5402679ff8373fd3e9ce7af9a3e999bad556fe0cc25dda1cc6`  
		Last Modified: Thu, 23 Mar 2023 06:51:30 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; 386

```console
$ docker pull adminer@sha256:ca2ee65836fd06aba737873c17718cd1ae4e52f6ba9a2869000be6794922ec0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96975396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47306ce39706e8ed333600b8d4399cb09c02ffe4e169f76bd59fa5b6569ae778`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 00:39:08 GMT
ADD file:f331251c4c21fceff56d13f76442a6334dc355c29ec7450768c1c86a3db1adab in / 
# Thu, 23 Mar 2023 00:39:09 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 21:17:12 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 21:17:40 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 21:17:41 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 21:17:41 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 21:17:41 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 21:17:42 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 21:17:42 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 21:17:42 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 21:17:42 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 21:17:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 21:17:54 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 21:17:54 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 21:17:54 GMT
USER adminer
# Thu, 23 Mar 2023 21:17:55 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 21:17:55 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:c1bb878cff31d37952c5c73ed15c167f599bb7f97b3eeaa1a17352b2473b3394`  
		Last Modified: Thu, 23 Mar 2023 00:42:44 GMT  
		Size: 56.0 MB (56027911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67239d163b3f7b443f91919b613775ed043520e6b06b413a9628905d01e98992`  
		Last Modified: Thu, 23 Mar 2023 21:18:34 GMT  
		Size: 39.6 MB (39558048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88061812377dcf7351518633da4694430dfe02ac13bdbc48516d26c18586a0d5`  
		Last Modified: Thu, 23 Mar 2023 21:18:24 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c664bb8231af50f8a98b457a9e7c291444345b0066ed54ddbcc0b2129859965`  
		Last Modified: Thu, 23 Mar 2023 21:18:24 GMT  
		Size: 1.9 KB (1869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a209358917bcf344993c93aad3b156d6a09b6ab64d43df3941ca51e6c414b9`  
		Last Modified: Thu, 23 Mar 2023 21:18:24 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061ad9c8d5ae0dc7e0d69094e0f6d09b29dea00ec113641833b5a37f404de058`  
		Last Modified: Thu, 23 Mar 2023 21:18:24 GMT  
		Size: 1.4 MB (1385210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2761eeb066c4b63e66ada920b87fc430284439f4c76fac14a274ef528430d3f`  
		Last Modified: Thu, 23 Mar 2023 21:18:24 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; mips64le

```console
$ docker pull adminer@sha256:14de06501f131ba9f62a814f592d766d6f050b30eab65a15bb1e753a436aab3d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92605785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddae0bdce53fcfedd28644c8fc0df52f38f44000615def4d84b2c88db2aff3ab`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 05:17:18 GMT
ADD file:2337efa705c8772705fa8519e513f4299e72c9eb63e3a68069778ca95a1511e6 in / 
# Thu, 23 Mar 2023 05:17:24 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 20:06:00 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 20:07:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 20:08:02 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 20:08:09 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 20:08:13 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 20:08:16 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 20:08:19 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 20:08:22 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 20:08:26 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 20:09:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 20:09:20 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 20:09:24 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 20:09:27 GMT
USER adminer
# Thu, 23 Mar 2023 20:09:31 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 20:09:34 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:f3951ee58695b4d906b37f2d9a07e6158f66a7328d0c70445d9607cd8367ede0`  
		Last Modified: Thu, 23 Mar 2023 05:25:08 GMT  
		Size: 53.3 MB (53264720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1180d0aa65a6936ad9b336fd7ddf64160d0a95203d7f3d82027fe8912c936d73`  
		Last Modified: Thu, 23 Mar 2023 20:11:59 GMT  
		Size: 38.0 MB (37950695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a23105a66b5d86b4852f9dcf6753d154e1d5b3b76c178cf8baced410a4deb2`  
		Last Modified: Thu, 23 Mar 2023 20:11:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba90b5b3033a3d6ba607430a17c7e37f0fae8f0664ac81a4e571e9ad9fca9e2`  
		Last Modified: Thu, 23 Mar 2023 20:11:33 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b1980d6708cacd2f28ca074bd917c1143a47040b425da5985915850214f197f`  
		Last Modified: Thu, 23 Mar 2023 20:11:33 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfbeda1e7451034cf22503ff221351a0d3f5e1f63a6f11dc71a81450a7aaadd`  
		Last Modified: Thu, 23 Mar 2023 20:11:34 GMT  
		Size: 1.4 MB (1386264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b87439fd13726c64bed775edf40ceb3cbc1b5dbf3f62fb9b127024394aaece4`  
		Last Modified: Thu, 23 Mar 2023 20:11:33 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:ddf406bedb6ea27fd15da89331e085e564dcde0c98ba31f3914b14b4483aa56e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101249875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8b45276387b274e6256e8c13851f3460fdd98b29ca47a09f04a8fad8d02090`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 01:19:25 GMT
ADD file:3eb86af6fda22c3e84548a6d0039be04819ce464b2700e8d8c140be49530ff7c in / 
# Thu, 23 Mar 2023 01:19:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 12:41:38 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 12:42:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 12:42:59 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 12:43:01 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 12:43:01 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 12:43:01 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 12:43:02 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 12:43:02 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 12:43:03 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 12:43:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 12:43:33 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 12:43:33 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 12:43:34 GMT
USER adminer
# Thu, 23 Mar 2023 12:43:35 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 12:43:35 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:566bc84f2641b393ac5a2f4a2ca405c09943aa3ec679f38ea1588f6ee930219e`  
		Last Modified: Thu, 23 Mar 2023 01:23:52 GMT  
		Size: 58.9 MB (58921026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2fbb285bf85ccfbb4c5282ba9f10d09cecbc5a0bab31ef237b51b3201089c2`  
		Last Modified: Thu, 23 Mar 2023 12:45:00 GMT  
		Size: 40.9 MB (40939153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5c4d551007797e513e8983796e921a39828107b5d1309cb2783b12bc6aaac4`  
		Last Modified: Thu, 23 Mar 2023 12:44:46 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19dcdc4ed08a4d33d3c19d3c7a7fcb606bed16f514bbdf68d09ed75d0ef5a039`  
		Last Modified: Thu, 23 Mar 2023 12:44:47 GMT  
		Size: 1.9 KB (1876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0187a4a30cb1c249de5010601f0912c92400f91482facb00198f8ba8e3691e`  
		Last Modified: Thu, 23 Mar 2023 12:44:46 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3867a61f6a3237b86e8a6bb431978b79ef5a1320ee3ebe58670b7a68f930c0f`  
		Last Modified: Thu, 23 Mar 2023 12:44:47 GMT  
		Size: 1.4 MB (1385455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553fdd9019949edcff0333970ef2dc5fa9af5479a21e08ecaf14a608524f497f`  
		Last Modified: Thu, 23 Mar 2023 12:44:46 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; s390x

```console
$ docker pull adminer@sha256:3a1427b2251efb24343fedded181036a73a9a9edd77c0241f1907db59654d4f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93684414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2d7a2d888bb0da291a197f178923752e3a408b6b8002d6ae4d4c8595173ec84`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 23 Mar 2023 00:43:50 GMT
ADD file:1111f9325245c8edccf2d9480c39cf2368f783ad86c2700d452be4e8cbebef8a in / 
# Thu, 23 Mar 2023 00:43:54 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:12:38 GMT
STOPSIGNAL SIGINT
# Thu, 23 Mar 2023 07:12:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 07:12:59 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 23 Mar 2023 07:12:59 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 23 Mar 2023 07:12:59 GMT
WORKDIR /var/www/html
# Thu, 23 Mar 2023 07:12:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 23 Mar 2023 07:12:59 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 23 Mar 2023 07:12:59 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 23 Mar 2023 07:12:59 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 23 Mar 2023 07:13:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 07:13:07 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 23 Mar 2023 07:13:07 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 23 Mar 2023 07:13:08 GMT
USER adminer
# Thu, 23 Mar 2023 07:13:08 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 23 Mar 2023 07:13:08 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:00dac46cbc44f444bd1dffe5b00a1b239054295b96f7984793273e9d12e75591`  
		Last Modified: Thu, 23 Mar 2023 00:47:04 GMT  
		Size: 53.3 MB (53277499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef40e14df43903a504c3865251eb934e8f644d89890514fc292b06981fca7826`  
		Last Modified: Thu, 23 Mar 2023 07:13:44 GMT  
		Size: 39.0 MB (39017484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f79bdf3c2e58c635953d9f0329b1010a5ff99b977d98975e467b7ab57a155e`  
		Last Modified: Thu, 23 Mar 2023 07:13:37 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ebc836b2a414afb40c1d84fa4fe4af21828a8f07dcbbbfe020a9a2270b0c467`  
		Last Modified: Thu, 23 Mar 2023 07:13:37 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:395b8975dd5a57c4e6e30bccd71a2d34125566cbb50b6000d142e49fb27dc1ea`  
		Last Modified: Thu, 23 Mar 2023 07:13:37 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7cb7770c3999b7b71cb8bd67b1686854b1cf6a8fbd340c7da905fddae466c1`  
		Last Modified: Thu, 23 Mar 2023 07:13:37 GMT  
		Size: 1.4 MB (1385197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47125e4be7b760f757795627cf23bffd8efbadc93fd3f20e13ac58ddac7b2639`  
		Last Modified: Thu, 23 Mar 2023 07:13:37 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
