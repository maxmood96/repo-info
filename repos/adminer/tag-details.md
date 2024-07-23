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
$ docker pull adminer@sha256:115edb007e0a41e3743a88599b37bd48b8637bb286ef159af4b26f748fc53492
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
$ docker pull adminer@sha256:c31c78818756bdbed9bdaa64dc19e7f7edd51813a8ef89d538f72ea052dca1f1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95960190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b234f0237cfe467ceb1991adc8e536c60e2307752a844117e3506273c3cc70`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:11 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Tue, 02 Jul 2024 01:25:12 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:48:36 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 04:48:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:48:58 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 02 Jul 2024 04:48:59 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 04:48:59 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 04:48:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 04:48:59 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 04:48:59 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 04:48:59 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 04:49:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 04:49:11 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:49:11 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 04:49:11 GMT
USER adminer
# Tue, 02 Jul 2024 04:49:11 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 02 Jul 2024 04:49:11 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c31c6689a3eaf2e6cb8a6fcc48fb54fc6190f9a34f8be35dff81a5705565a1`  
		Last Modified: Tue, 02 Jul 2024 04:49:50 GMT  
		Size: 39.5 MB (39489478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15098df20048ca7252eef0cee4b2b60f5b4cfe226b37aee2f86c8b8b49ed12da`  
		Last Modified: Tue, 02 Jul 2024 04:49:43 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa436138c493f6b280d90f878c5f42e49161c213e07c63239dba3035d53200f`  
		Last Modified: Tue, 02 Jul 2024 04:49:43 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301530bfa5f53b39e40c2a73ab2943a95bb28f04dbd763bb519c82228cdb6330`  
		Last Modified: Tue, 02 Jul 2024 04:49:43 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b7955944f85a8d66bb95cdfbe4839dc329677da60416ebb8c1d09fef5ec295`  
		Last Modified: Tue, 02 Jul 2024 04:49:43 GMT  
		Size: 1.4 MB (1385152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d923a48aa5d0fcde247f30d40164b9ad0d68d576e0c37c3c69eb83e2dab736e5`  
		Last Modified: Tue, 02 Jul 2024 04:49:43 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; arm variant v5

```console
$ docker pull adminer@sha256:0e52bfd1add93668146a0a1a5544187ee1dc9b4d9b0d7368ec3bd97f77037e9b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91225878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5fc5328a78544dcb2f0a078019b0bea7ab255b502c4eddbcbb0564c616436c`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Mon, 22 Jul 2024 23:57:12 GMT
ADD file:05c877f820dfe73bd5cecf959b857152065c40802cad0d9a46229bc0d5708339 in / 
# Mon, 22 Jul 2024 23:57:13 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 00:24:42 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 00:25:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 00:25:28 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 00:25:29 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 00:25:29 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 00:25:30 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 00:25:30 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 00:25:30 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 00:25:31 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 00:25:47 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 00:25:47 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 00:25:47 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 00:25:47 GMT
USER adminer
# Tue, 23 Jul 2024 00:25:47 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 23 Jul 2024 00:25:47 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:6faa199d3f09eecc4762c527abd2e9a5bc86f34a15c78145707b6b0b0ee526d5`  
		Last Modified: Tue, 23 Jul 2024 00:01:42 GMT  
		Size: 52.6 MB (52588961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea175fc25888492446b9545eb11532a36f0d62f3c448de0e72e72a2d4206256`  
		Last Modified: Tue, 23 Jul 2024 00:26:33 GMT  
		Size: 37.2 MB (37247611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aee3033b2b37548a5949367b960e0d3bb49c486d2b4911b024eadb15301d60f`  
		Last Modified: Tue, 23 Jul 2024 00:26:23 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc5b14232a5b77160d3deb0bbad3fab3c8aac724a97c519210b401938ee10a0`  
		Last Modified: Tue, 23 Jul 2024 00:26:23 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84cad97ff757120302d208a8b77f191afed2dc5624b7f563ca50c8894dac89f6`  
		Last Modified: Tue, 23 Jul 2024 00:26:23 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3600c4e5e44f075d5c68b7655b8084853942806b56b0ecd9baf6783a66197c`  
		Last Modified: Tue, 23 Jul 2024 00:26:23 GMT  
		Size: 1.4 MB (1385103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6851d528b265ea638bd0a586551d946177270672608fa4f8578c8420d0385cb9`  
		Last Modified: Tue, 23 Jul 2024 00:26:23 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; arm variant v7

```console
$ docker pull adminer@sha256:02c012a3b47cb2dc2761b06eed691093d9e166216c92df475cbc9f8eadc9e5c8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87822374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8844c2056e0d57feaca4f1be1253bd8f8f2715f937cd842d1ccbef6c2f7fb2`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:18 GMT
ADD file:45e512d8c89ef619a4db87ca11813c5b48e6332c4c281a9f0d4aaf7301e85990 in / 
# Tue, 23 Jul 2024 03:03:18 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:52:31 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 03:53:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:53:47 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 03:53:49 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 03:53:49 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 03:53:50 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 03:53:50 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 03:53:50 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 03:53:51 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 03:54:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 03:54:18 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 03:54:19 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 03:54:19 GMT
USER adminer
# Tue, 23 Jul 2024 03:54:19 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 23 Jul 2024 03:54:19 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:57c3fa3d04a48c55117bbc60f2775c978886b3bc89b70e48e85c0516ce060947`  
		Last Modified: Tue, 23 Jul 2024 03:07:14 GMT  
		Size: 50.2 MB (50242355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef802d5de026a32dc791f808ef890fca768eb6e270e042642cf443affacfb85`  
		Last Modified: Tue, 23 Jul 2024 03:55:16 GMT  
		Size: 36.2 MB (36190522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa89f6dcd7fec84e6bdff0fa8ed984aebc82e025446b8d87445c270036259aa9`  
		Last Modified: Tue, 23 Jul 2024 03:55:07 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d6bc010107086de83c02e3740522ab10058840d9382aba4debea6502e49e1c`  
		Last Modified: Tue, 23 Jul 2024 03:55:07 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a76f8c1f42f47a8f9dc9bcdd1e024abe9951e9b58f03990d325c34484b042d`  
		Last Modified: Tue, 23 Jul 2024 03:55:07 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4fde1c1ed80b1b4ca7d8802b96bd546050fd8e0b862c6cd2f25f5b27655747`  
		Last Modified: Tue, 23 Jul 2024 03:55:07 GMT  
		Size: 1.4 MB (1385292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d19e9266c2d80bfe86943cee6ac09b905d99cba1d9b5c0b1b1b444eac73acfd`  
		Last Modified: Tue, 23 Jul 2024 03:55:07 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:b03c33368be4bba59f14aaf0cded44fcdc50e355c9bfa19cc3c44d106c4713e0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94358345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299c22d3acc4de54d764bad9b1076848198e8e46a67fc4245d04908c6f28e6dd`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Tue, 02 Jul 2024 03:49:31 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 03:49:31 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 03:49:31 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 03:49:31 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 03:49:31 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 03:49:31 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 03:49:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 03:49:41 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:49:41 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 03:49:41 GMT
USER adminer
# Tue, 02 Jul 2024 03:49:41 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 02 Jul 2024 03:49:42 GMT
EXPOSE 8080
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
	-	`sha256:ca7a060c53754e1f602d8bcd48248ebf6552078b1b5399f1e2bc003e28df66a3`  
		Last Modified: Tue, 02 Jul 2024 03:50:04 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fbd5efe441c2e90738651736224a0fe724fd712995f15c157b715b38b9b9b6`  
		Last Modified: Tue, 02 Jul 2024 03:50:04 GMT  
		Size: 1.5 KB (1483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee7687bec909e9911339ab8fc15c7213b444003fd7dbaa0628eea3d211c7834`  
		Last Modified: Tue, 02 Jul 2024 03:50:05 GMT  
		Size: 1.4 MB (1385094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acee67427be79e892393ce058a4d79428ae50d525217d0cceb4b31ad4c46f482`  
		Last Modified: Tue, 02 Jul 2024 03:50:04 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; 386

```console
$ docker pull adminer@sha256:2d74c7eb07a906d8e576f9e2c9971bdb01ab19aeba06478a94a9c273fa0992b6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (97013341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a850c42c8891f85474d75f6a74938ec55e1bad5d98e957cf59b54e8d6261e7`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Tue, 02 Jul 2024 01:40:38 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 01:40:38 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 01:40:38 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 01:40:38 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 01:40:38 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 01:40:38 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 01:40:50 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 01:40:50 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:40:50 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 01:40:51 GMT
USER adminer
# Tue, 02 Jul 2024 01:40:51 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 02 Jul 2024 01:40:51 GMT
EXPOSE 8080
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
	-	`sha256:8ae625b5731fddecf9b61034a28aedc8d9401e752eb6a7d261521555c3481791`  
		Last Modified: Tue, 02 Jul 2024 01:41:24 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a56bc1ddfe4d69136cc994627bbfeff96048814e1f5025b955be353df22753`  
		Last Modified: Tue, 02 Jul 2024 01:41:24 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6972d1f06dce91eb6060a692e744bf4b0e73bdbcebc740ab73f7249763c59101`  
		Last Modified: Tue, 02 Jul 2024 01:41:24 GMT  
		Size: 1.4 MB (1385010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b50df8e2047966f9043744696cacdc3a5735a5400851144fffc0f0d740dc1e`  
		Last Modified: Tue, 02 Jul 2024 01:41:24 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; mips64le

```console
$ docker pull adminer@sha256:8a01711066df85ed070620061fdd9e1631a1046badc61606c1e6ec8bdc01ec26
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92654371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43da756743e71ac148d7b882a8eb215791392ae2b763de8095c051a6cff1980d`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 23 Jul 2024 00:38:26 GMT
ADD file:3fbf62974aea46ff67427fd8996563bef3939ff51df600b4914acf5abb0b6c51 in / 
# Tue, 23 Jul 2024 00:38:32 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:12:17 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 02:14:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:14:15 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 02:14:23 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 02:14:26 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 02:14:30 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 02:14:34 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 02:14:37 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 02:14:41 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 02:15:33 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 02:15:36 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:15:40 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 02:15:44 GMT
USER adminer
# Tue, 23 Jul 2024 02:15:48 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 23 Jul 2024 02:15:51 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:6fba1199d77f2795fad97ca84f3d7030aab307e1ee7b582027c4e146bacdff14`  
		Last Modified: Tue, 23 Jul 2024 00:49:50 GMT  
		Size: 53.3 MB (53310598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb5ccc2e78cafd7a6bae2b97d6510ada07c2b60961937d42810594c7f3013c2`  
		Last Modified: Tue, 23 Jul 2024 02:18:19 GMT  
		Size: 38.0 MB (37953492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a7bda0b2932d324ef514eff7c5614353c086b9ea7ad4d853f8fd399c51b6d5`  
		Last Modified: Tue, 23 Jul 2024 02:17:52 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20433faf9234936c4ea8be2f288e5c392849bf726237f53f1ba83f71ada2288f`  
		Last Modified: Tue, 23 Jul 2024 02:17:52 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6157345705446634090f1dd03196240215199992409caa373077fa87e33a034a`  
		Last Modified: Tue, 23 Jul 2024 02:17:52 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537f5ec680d68403883c13e21ec08015d0e3df367b0efbd3b21f9461e43c9bd2`  
		Last Modified: Tue, 23 Jul 2024 02:17:53 GMT  
		Size: 1.4 MB (1386185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61a03247e49e3d869b1ec2b1062fd0cb20c2c04614d1964690602a169b6733e`  
		Last Modified: Tue, 23 Jul 2024 02:17:52 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; ppc64le

```console
$ docker pull adminer@sha256:062d939387a558e07d69afde16e368e2fc7adc2e0c43700f46a6c448b8251ce3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101289185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0410f06417580c33e565abde408c17dfeed554975d02709ad62c95208b3ddace`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 23 Jul 2024 01:27:09 GMT
ADD file:538282e20405c23ce510f30f714f80393534997f12fd1cc25a8d7752dc6f1360 in / 
# Tue, 23 Jul 2024 01:27:11 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:25:37 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 02:26:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:26:23 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 02:26:24 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 02:26:25 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 02:26:25 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 02:26:25 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 02:26:25 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 02:26:25 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 02:26:44 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 02:26:44 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:26:45 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 02:26:45 GMT
USER adminer
# Tue, 23 Jul 2024 02:26:45 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 23 Jul 2024 02:26:46 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:fb0b8650d20e29c53f770b72d16b7381f876f2a0053fff3e542a0cc3f0b944b9`  
		Last Modified: Tue, 23 Jul 2024 01:31:32 GMT  
		Size: 59.0 MB (58954687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15738e55b04d20078f3d22ceaa5ebfefad42e7e68c55159ba9f1c6c96104c70a`  
		Last Modified: Tue, 23 Jul 2024 02:27:47 GMT  
		Size: 40.9 MB (40945047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1abb9adf68c77ddb45b48d87fa048994b191b50bb3dcdb65c5a1441b09236be1`  
		Last Modified: Tue, 23 Jul 2024 02:27:38 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69537e8ef3c397be4c3c4bbae3f729010605989d0e55e2e34dec154b6236d385`  
		Last Modified: Tue, 23 Jul 2024 02:27:38 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d85520057f355d14f85487174847109082913ae6990ae521b6c4771322126556`  
		Last Modified: Tue, 23 Jul 2024 02:27:38 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49b987d3a64b41a1a379cbae62ba6a452c233dea35255c15a96f51b7b2f2540`  
		Last Modified: Tue, 23 Jul 2024 02:27:38 GMT  
		Size: 1.4 MB (1385236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094977f5661e09079e9461e6361d77eba3c6d34b09f6673b43866e7684c00646`  
		Last Modified: Tue, 23 Jul 2024 02:27:38 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; s390x

```console
$ docker pull adminer@sha256:c7bff6b618579c93f078953be91ea47360675dbdb7db286ac4c7c7b7a2c31701
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93739700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ee3166c88912b6a2804b5d2bd37d20f188044e94b6ccf08ac6b5df23de3359`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 23 Jul 2024 02:28:03 GMT
ADD file:67d4db619a1cada17f248642d89d5b55ab04b5dd6885587148dedeb665795154 in / 
# Tue, 23 Jul 2024 02:28:06 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:03:04 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 03:03:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:03:30 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 03:03:30 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 03:03:30 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 03:03:31 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 03:03:31 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 03:03:31 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 03:03:31 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 03:03:40 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 03:03:40 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 03:03:40 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 03:03:41 GMT
USER adminer
# Tue, 23 Jul 2024 03:03:41 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 23 Jul 2024 03:03:41 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:0d03391dea2fdd66bd2c594e41ac7575c5879176469a4d1e7301b8498f5e5351`  
		Last Modified: Tue, 23 Jul 2024 02:32:57 GMT  
		Size: 53.3 MB (53324092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f9b72e50d6e2068c7b209cae11aad4b881a45ca10624ddffa7d47ba3dc5258`  
		Last Modified: Tue, 23 Jul 2024 03:04:21 GMT  
		Size: 39.0 MB (39026243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dab3bcf36e0afe3d1e0873b7ab407e216ba4abd68b83db207492bfcb2d0e49c`  
		Last Modified: Tue, 23 Jul 2024 03:04:14 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4cc17406257aa75797eefdc9f711a2a0ef93e0e8a4aa6fab92d8af10d5c9ef6`  
		Last Modified: Tue, 23 Jul 2024 03:04:14 GMT  
		Size: 1.9 KB (1852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe14ae12a8ee2216ee37cf525b13545cadabdbeb782ce5a62b37414bdca70862`  
		Last Modified: Tue, 23 Jul 2024 03:04:14 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef800a2307cd151cb4f22631273389647cac3f39394e0a093c0517adde471b0`  
		Last Modified: Tue, 23 Jul 2024 03:04:14 GMT  
		Size: 1.4 MB (1385146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5161f60448626f1dd88239bdbbf9a186fa2c1a53279e72e50e5f00a2ae987ae`  
		Last Modified: Tue, 23 Jul 2024 03:04:14 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4-fastcgi`

```console
$ docker pull adminer@sha256:cf3d7106f4d11d07a86fb2690a879e522d0561f8136b38a67fdc2bf4eba11c76
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
$ docker pull adminer@sha256:a65f9f3444eecf907fde215fd40219387c99f7d0927ad94fec2fad3d0c91df5c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95962913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b4a63db34258ca6af0f56fcd13e485f38764b0959c6119d1cbda4a1e920532`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:11 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Tue, 02 Jul 2024 01:25:12 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:48:36 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 04:48:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:48:58 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 02 Jul 2024 04:49:18 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 02 Jul 2024 04:49:19 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 04:49:19 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 04:49:19 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 04:49:19 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 04:49:19 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 04:49:19 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 04:49:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 04:49:30 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:49:30 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 04:49:30 GMT
USER adminer
# Tue, 02 Jul 2024 04:49:30 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c31c6689a3eaf2e6cb8a6fcc48fb54fc6190f9a34f8be35dff81a5705565a1`  
		Last Modified: Tue, 02 Jul 2024 04:49:50 GMT  
		Size: 39.5 MB (39489478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15098df20048ca7252eef0cee4b2b60f5b4cfe226b37aee2f86c8b8b49ed12da`  
		Last Modified: Tue, 02 Jul 2024 04:49:43 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7fc47a846479bc3911ccdaed2236fdb846714f9db30dd02d466e224cc5a895`  
		Last Modified: Tue, 02 Jul 2024 04:50:05 GMT  
		Size: 2.7 KB (2711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4d59e9486f131dfc50c56f5ee19dd29849461da1378eab3cb1ffbb7184023f3`  
		Last Modified: Tue, 02 Jul 2024 04:50:05 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f25810dba66fe09876afbcf9e8e39d8456c82613cfc63ac0a7f39738bc27c6`  
		Last Modified: Tue, 02 Jul 2024 04:50:05 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96bea11c7f0698a423d992a197aed5b28d6b8d11d745824720eab682f125c2a`  
		Last Modified: Tue, 02 Jul 2024 04:50:06 GMT  
		Size: 1.4 MB (1385158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8ec6f28e566eaec9db9f59408e63b3d58c7595bca0c831fa9286ebca0f2e29`  
		Last Modified: Tue, 02 Jul 2024 04:50:05 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm variant v5

```console
$ docker pull adminer@sha256:28b821bf07d3288ef8624aba4e348e6c5df13a1c8de63390117bd668767bf873
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91228595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:774685cf6d16dadfa8b111a578dc98947b40415930473f195ea4f3178bbf702f`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Mon, 22 Jul 2024 23:57:12 GMT
ADD file:05c877f820dfe73bd5cecf959b857152065c40802cad0d9a46229bc0d5708339 in / 
# Mon, 22 Jul 2024 23:57:13 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 00:24:42 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 00:25:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 00:25:28 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 00:25:53 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 23 Jul 2024 00:25:54 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 00:25:54 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 00:25:54 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 00:25:54 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 00:25:55 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 00:25:55 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 00:26:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 00:26:10 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 00:26:10 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 00:26:10 GMT
USER adminer
# Tue, 23 Jul 2024 00:26:10 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:6faa199d3f09eecc4762c527abd2e9a5bc86f34a15c78145707b6b0b0ee526d5`  
		Last Modified: Tue, 23 Jul 2024 00:01:42 GMT  
		Size: 52.6 MB (52588961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea175fc25888492446b9545eb11532a36f0d62f3c448de0e72e72a2d4206256`  
		Last Modified: Tue, 23 Jul 2024 00:26:33 GMT  
		Size: 37.2 MB (37247611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aee3033b2b37548a5949367b960e0d3bb49c486d2b4911b024eadb15301d60f`  
		Last Modified: Tue, 23 Jul 2024 00:26:23 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2c14f7e1bfcd1615af505b8319319293cfc170c1feff406f0848d749207bb3`  
		Last Modified: Tue, 23 Jul 2024 00:26:48 GMT  
		Size: 2.7 KB (2715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d26206279c33af8163e48ff66f061c62670069788764b804f76ebdeb5c45be4`  
		Last Modified: Tue, 23 Jul 2024 00:26:48 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36113ffa34469c443f81198f38fef456743291a808133ba71d7b4724e84a1544`  
		Last Modified: Tue, 23 Jul 2024 00:26:48 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2353bf2bc981df8102745bff3ef704ca29e64af6ac487352ed4123647aed2c26`  
		Last Modified: Tue, 23 Jul 2024 00:26:48 GMT  
		Size: 1.4 MB (1385100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7bc91ac0a2b45c59d8992cc845dfdf83f6876423d1f3a4f128fbf503c7f43b`  
		Last Modified: Tue, 23 Jul 2024 00:26:48 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:940499184855825584dffe9b581a4e3d892cda313e8ba1f06f4c0f184d5bc108
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87825032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04142ce31ca904ea987e19dc4b5162e4f1640898ef5b8e4ff2783137dfd80730`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:18 GMT
ADD file:45e512d8c89ef619a4db87ca11813c5b48e6332c4c281a9f0d4aaf7301e85990 in / 
# Tue, 23 Jul 2024 03:03:18 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:52:31 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 03:53:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:53:47 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 03:54:25 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 23 Jul 2024 03:54:27 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 03:54:27 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 03:54:28 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 03:54:28 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 03:54:29 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 03:54:29 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 03:54:50 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 03:54:50 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 03:54:51 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 03:54:51 GMT
USER adminer
# Tue, 23 Jul 2024 03:54:51 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:57c3fa3d04a48c55117bbc60f2775c978886b3bc89b70e48e85c0516ce060947`  
		Last Modified: Tue, 23 Jul 2024 03:07:14 GMT  
		Size: 50.2 MB (50242355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef802d5de026a32dc791f808ef890fca768eb6e270e042642cf443affacfb85`  
		Last Modified: Tue, 23 Jul 2024 03:55:16 GMT  
		Size: 36.2 MB (36190522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa89f6dcd7fec84e6bdff0fa8ed984aebc82e025446b8d87445c270036259aa9`  
		Last Modified: Tue, 23 Jul 2024 03:55:07 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f0ffae6b7a4e7300b5fcc49bdc2bc9b2ad8b6746611c7e99b291ab33fffb3a`  
		Last Modified: Tue, 23 Jul 2024 03:55:32 GMT  
		Size: 2.7 KB (2715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfddd9483e786ea5d31fb2009e0addd025d8cfa3cc664f3a52753091f01dbe0c`  
		Last Modified: Tue, 23 Jul 2024 03:55:32 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff45e2ad6c3b6e678cc25d6976ac0a3a174d46e13268c21d32e308693ec1831`  
		Last Modified: Tue, 23 Jul 2024 03:55:32 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a8c797535832a99c8d88455fe604811f0c45be3d9d29160b653ad03507acdf`  
		Last Modified: Tue, 23 Jul 2024 03:55:33 GMT  
		Size: 1.4 MB (1385237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e909ef8532fe9e3e6c08fb74bd399bce640eb766fc731570b45abdf9c646eb34`  
		Last Modified: Tue, 23 Jul 2024 03:55:33 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm64 variant v8

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

### `adminer:4-fastcgi` - linux; 386

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

### `adminer:4-fastcgi` - linux; mips64le

```console
$ docker pull adminer@sha256:8b5a58dc254439c686e7e263f42168f58ed7a06c2af794b7d4d6a5827f0fd314
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92657102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b23cd2579b0ea5c2e2e6391da4fef0599634b6d8e1c0ae92ba67507153281f`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 23 Jul 2024 00:38:26 GMT
ADD file:3fbf62974aea46ff67427fd8996563bef3939ff51df600b4914acf5abb0b6c51 in / 
# Tue, 23 Jul 2024 00:38:32 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:12:17 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 02:14:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:14:15 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 02:16:05 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 23 Jul 2024 02:16:12 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 02:16:16 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 02:16:20 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 02:16:23 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 02:16:27 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 02:16:31 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 02:17:20 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 02:17:24 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:17:27 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 02:17:31 GMT
USER adminer
# Tue, 23 Jul 2024 02:17:35 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:6fba1199d77f2795fad97ca84f3d7030aab307e1ee7b582027c4e146bacdff14`  
		Last Modified: Tue, 23 Jul 2024 00:49:50 GMT  
		Size: 53.3 MB (53310598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb5ccc2e78cafd7a6bae2b97d6510ada07c2b60961937d42810594c7f3013c2`  
		Last Modified: Tue, 23 Jul 2024 02:18:19 GMT  
		Size: 38.0 MB (37953492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a7bda0b2932d324ef514eff7c5614353c086b9ea7ad4d853f8fd399c51b6d5`  
		Last Modified: Tue, 23 Jul 2024 02:17:52 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee2d26e1899d8a8b268f6ef6d98db730bc341ff6913ace137afde90c8f7ba6c`  
		Last Modified: Tue, 23 Jul 2024 02:18:41 GMT  
		Size: 2.7 KB (2713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76695ee7cfcc7aad4ed6cc2ce0a15b5e71207ab0ccae36294cdeac0cc71ddbf`  
		Last Modified: Tue, 23 Jul 2024 02:18:41 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee98dea0703c2f60a2e4bf777be8e50a609fbe5658ef913b93fddbb604d6e96a`  
		Last Modified: Tue, 23 Jul 2024 02:18:41 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e924f48a941a9836a5762905bb73e501a9c08ec789d9975f88590718f6c0ba`  
		Last Modified: Tue, 23 Jul 2024 02:18:43 GMT  
		Size: 1.4 MB (1386197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77965a700523588d06e3d8ab1c0586c82d83796fbe6949c87d3177d7dd97c701`  
		Last Modified: Tue, 23 Jul 2024 02:18:42 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:dee0c7bb9a7b5aaac331c29123d62662d900d6d1e0d1bf0becc95e9dc35d3599
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101291907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ea903255a4ffa78793f81ea18f5a4560af79838030fbf4c55516f80934f152`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 23 Jul 2024 01:27:09 GMT
ADD file:538282e20405c23ce510f30f714f80393534997f12fd1cc25a8d7752dc6f1360 in / 
# Tue, 23 Jul 2024 01:27:11 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:25:37 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 02:26:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:26:23 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 02:27:02 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 23 Jul 2024 02:27:04 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 02:27:04 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 02:27:04 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 02:27:05 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 02:27:05 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 02:27:05 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 02:27:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 02:27:24 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:27:24 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 02:27:24 GMT
USER adminer
# Tue, 23 Jul 2024 02:27:25 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:fb0b8650d20e29c53f770b72d16b7381f876f2a0053fff3e542a0cc3f0b944b9`  
		Last Modified: Tue, 23 Jul 2024 01:31:32 GMT  
		Size: 59.0 MB (58954687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15738e55b04d20078f3d22ceaa5ebfefad42e7e68c55159ba9f1c6c96104c70a`  
		Last Modified: Tue, 23 Jul 2024 02:27:47 GMT  
		Size: 40.9 MB (40945047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1abb9adf68c77ddb45b48d87fa048994b191b50bb3dcdb65c5a1441b09236be1`  
		Last Modified: Tue, 23 Jul 2024 02:27:38 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8cfaf311da16a0e82541813e3f196fbb549b8d3b4c5d00a0706e9bb113ab61`  
		Last Modified: Tue, 23 Jul 2024 02:28:03 GMT  
		Size: 2.7 KB (2712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97ca69cb806636211daf12ba75a96f6dcd060f44f8de9c8c01f4e7603ad16c4`  
		Last Modified: Tue, 23 Jul 2024 02:28:02 GMT  
		Size: 1.8 KB (1847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0cb83b55519a88ad23c909874d20b54e854376a784207653c4be6f23c73ccc`  
		Last Modified: Tue, 23 Jul 2024 02:28:02 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7531a129bc98acb32209bb040ce99bb7d30fcb76dab8ded8ef5cd08a179854`  
		Last Modified: Tue, 23 Jul 2024 02:28:03 GMT  
		Size: 1.4 MB (1385246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d48a360d8a16035cc5528cd6bc0e45116f172e7c3d935c20ae81eb64111bc3`  
		Last Modified: Tue, 23 Jul 2024 02:28:02 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; s390x

```console
$ docker pull adminer@sha256:5b68c11e23080d7d4f5e745202d62cf73c411b3b6e45519dd1342175e8155e1f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93742391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c221ef6b6f73482a2313e8fe83b8667520970e85e5c41919dbbaa6e72524e1a8`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 23 Jul 2024 02:28:03 GMT
ADD file:67d4db619a1cada17f248642d89d5b55ab04b5dd6885587148dedeb665795154 in / 
# Tue, 23 Jul 2024 02:28:06 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:03:04 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 03:03:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:03:30 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 03:03:51 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 23 Jul 2024 03:03:51 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 03:03:51 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 03:03:51 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 03:03:52 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 03:03:52 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 03:03:52 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 03:04:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 03:04:00 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 03:04:00 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 03:04:00 GMT
USER adminer
# Tue, 23 Jul 2024 03:04:01 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:0d03391dea2fdd66bd2c594e41ac7575c5879176469a4d1e7301b8498f5e5351`  
		Last Modified: Tue, 23 Jul 2024 02:32:57 GMT  
		Size: 53.3 MB (53324092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f9b72e50d6e2068c7b209cae11aad4b881a45ca10624ddffa7d47ba3dc5258`  
		Last Modified: Tue, 23 Jul 2024 03:04:21 GMT  
		Size: 39.0 MB (39026243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dab3bcf36e0afe3d1e0873b7ab407e216ba4abd68b83db207492bfcb2d0e49c`  
		Last Modified: Tue, 23 Jul 2024 03:04:14 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fa842b8d20c971ec35b7b1fd365ebcf06eba7c327f8d3152c8fca17c0e7665`  
		Last Modified: Tue, 23 Jul 2024 03:04:31 GMT  
		Size: 2.7 KB (2709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29efb99675faf1ec4ca57f74dc079ff104548b494b6df8e1ab865f7d1835be99`  
		Last Modified: Tue, 23 Jul 2024 03:04:31 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769d57125a6627215e8720ac3e31b9de7c9d1c2abc3423baecb12e25a1b5729d`  
		Last Modified: Tue, 23 Jul 2024 03:04:31 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f056b55ddb3c62ad27de0b76cafcb5d832cc6d481b3765f7bf3c372bd23890`  
		Last Modified: Tue, 23 Jul 2024 03:04:31 GMT  
		Size: 1.4 MB (1385141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c5a5212a250c3a34617fd215b8dd86b707ceacbd89602ca27b62c14d9ad009`  
		Last Modified: Tue, 23 Jul 2024 03:04:31 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4-standalone`

```console
$ docker pull adminer@sha256:115edb007e0a41e3743a88599b37bd48b8637bb286ef159af4b26f748fc53492
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
$ docker pull adminer@sha256:c31c78818756bdbed9bdaa64dc19e7f7edd51813a8ef89d538f72ea052dca1f1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95960190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b234f0237cfe467ceb1991adc8e536c60e2307752a844117e3506273c3cc70`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:11 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Tue, 02 Jul 2024 01:25:12 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:48:36 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 04:48:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:48:58 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 02 Jul 2024 04:48:59 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 04:48:59 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 04:48:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 04:48:59 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 04:48:59 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 04:48:59 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 04:49:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 04:49:11 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:49:11 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 04:49:11 GMT
USER adminer
# Tue, 02 Jul 2024 04:49:11 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 02 Jul 2024 04:49:11 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c31c6689a3eaf2e6cb8a6fcc48fb54fc6190f9a34f8be35dff81a5705565a1`  
		Last Modified: Tue, 02 Jul 2024 04:49:50 GMT  
		Size: 39.5 MB (39489478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15098df20048ca7252eef0cee4b2b60f5b4cfe226b37aee2f86c8b8b49ed12da`  
		Last Modified: Tue, 02 Jul 2024 04:49:43 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa436138c493f6b280d90f878c5f42e49161c213e07c63239dba3035d53200f`  
		Last Modified: Tue, 02 Jul 2024 04:49:43 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301530bfa5f53b39e40c2a73ab2943a95bb28f04dbd763bb519c82228cdb6330`  
		Last Modified: Tue, 02 Jul 2024 04:49:43 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b7955944f85a8d66bb95cdfbe4839dc329677da60416ebb8c1d09fef5ec295`  
		Last Modified: Tue, 02 Jul 2024 04:49:43 GMT  
		Size: 1.4 MB (1385152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d923a48aa5d0fcde247f30d40164b9ad0d68d576e0c37c3c69eb83e2dab736e5`  
		Last Modified: Tue, 02 Jul 2024 04:49:43 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; arm variant v5

```console
$ docker pull adminer@sha256:0e52bfd1add93668146a0a1a5544187ee1dc9b4d9b0d7368ec3bd97f77037e9b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91225878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5fc5328a78544dcb2f0a078019b0bea7ab255b502c4eddbcbb0564c616436c`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Mon, 22 Jul 2024 23:57:12 GMT
ADD file:05c877f820dfe73bd5cecf959b857152065c40802cad0d9a46229bc0d5708339 in / 
# Mon, 22 Jul 2024 23:57:13 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 00:24:42 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 00:25:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 00:25:28 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 00:25:29 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 00:25:29 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 00:25:30 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 00:25:30 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 00:25:30 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 00:25:31 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 00:25:47 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 00:25:47 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 00:25:47 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 00:25:47 GMT
USER adminer
# Tue, 23 Jul 2024 00:25:47 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 23 Jul 2024 00:25:47 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:6faa199d3f09eecc4762c527abd2e9a5bc86f34a15c78145707b6b0b0ee526d5`  
		Last Modified: Tue, 23 Jul 2024 00:01:42 GMT  
		Size: 52.6 MB (52588961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea175fc25888492446b9545eb11532a36f0d62f3c448de0e72e72a2d4206256`  
		Last Modified: Tue, 23 Jul 2024 00:26:33 GMT  
		Size: 37.2 MB (37247611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aee3033b2b37548a5949367b960e0d3bb49c486d2b4911b024eadb15301d60f`  
		Last Modified: Tue, 23 Jul 2024 00:26:23 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc5b14232a5b77160d3deb0bbad3fab3c8aac724a97c519210b401938ee10a0`  
		Last Modified: Tue, 23 Jul 2024 00:26:23 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84cad97ff757120302d208a8b77f191afed2dc5624b7f563ca50c8894dac89f6`  
		Last Modified: Tue, 23 Jul 2024 00:26:23 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3600c4e5e44f075d5c68b7655b8084853942806b56b0ecd9baf6783a66197c`  
		Last Modified: Tue, 23 Jul 2024 00:26:23 GMT  
		Size: 1.4 MB (1385103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6851d528b265ea638bd0a586551d946177270672608fa4f8578c8420d0385cb9`  
		Last Modified: Tue, 23 Jul 2024 00:26:23 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:02c012a3b47cb2dc2761b06eed691093d9e166216c92df475cbc9f8eadc9e5c8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87822374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8844c2056e0d57feaca4f1be1253bd8f8f2715f937cd842d1ccbef6c2f7fb2`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:18 GMT
ADD file:45e512d8c89ef619a4db87ca11813c5b48e6332c4c281a9f0d4aaf7301e85990 in / 
# Tue, 23 Jul 2024 03:03:18 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:52:31 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 03:53:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:53:47 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 03:53:49 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 03:53:49 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 03:53:50 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 03:53:50 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 03:53:50 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 03:53:51 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 03:54:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 03:54:18 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 03:54:19 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 03:54:19 GMT
USER adminer
# Tue, 23 Jul 2024 03:54:19 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 23 Jul 2024 03:54:19 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:57c3fa3d04a48c55117bbc60f2775c978886b3bc89b70e48e85c0516ce060947`  
		Last Modified: Tue, 23 Jul 2024 03:07:14 GMT  
		Size: 50.2 MB (50242355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef802d5de026a32dc791f808ef890fca768eb6e270e042642cf443affacfb85`  
		Last Modified: Tue, 23 Jul 2024 03:55:16 GMT  
		Size: 36.2 MB (36190522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa89f6dcd7fec84e6bdff0fa8ed984aebc82e025446b8d87445c270036259aa9`  
		Last Modified: Tue, 23 Jul 2024 03:55:07 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d6bc010107086de83c02e3740522ab10058840d9382aba4debea6502e49e1c`  
		Last Modified: Tue, 23 Jul 2024 03:55:07 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a76f8c1f42f47a8f9dc9bcdd1e024abe9951e9b58f03990d325c34484b042d`  
		Last Modified: Tue, 23 Jul 2024 03:55:07 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4fde1c1ed80b1b4ca7d8802b96bd546050fd8e0b862c6cd2f25f5b27655747`  
		Last Modified: Tue, 23 Jul 2024 03:55:07 GMT  
		Size: 1.4 MB (1385292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d19e9266c2d80bfe86943cee6ac09b905d99cba1d9b5c0b1b1b444eac73acfd`  
		Last Modified: Tue, 23 Jul 2024 03:55:07 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:b03c33368be4bba59f14aaf0cded44fcdc50e355c9bfa19cc3c44d106c4713e0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94358345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299c22d3acc4de54d764bad9b1076848198e8e46a67fc4245d04908c6f28e6dd`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Tue, 02 Jul 2024 03:49:31 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 03:49:31 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 03:49:31 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 03:49:31 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 03:49:31 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 03:49:31 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 03:49:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 03:49:41 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:49:41 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 03:49:41 GMT
USER adminer
# Tue, 02 Jul 2024 03:49:41 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 02 Jul 2024 03:49:42 GMT
EXPOSE 8080
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
	-	`sha256:ca7a060c53754e1f602d8bcd48248ebf6552078b1b5399f1e2bc003e28df66a3`  
		Last Modified: Tue, 02 Jul 2024 03:50:04 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fbd5efe441c2e90738651736224a0fe724fd712995f15c157b715b38b9b9b6`  
		Last Modified: Tue, 02 Jul 2024 03:50:04 GMT  
		Size: 1.5 KB (1483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee7687bec909e9911339ab8fc15c7213b444003fd7dbaa0628eea3d211c7834`  
		Last Modified: Tue, 02 Jul 2024 03:50:05 GMT  
		Size: 1.4 MB (1385094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acee67427be79e892393ce058a4d79428ae50d525217d0cceb4b31ad4c46f482`  
		Last Modified: Tue, 02 Jul 2024 03:50:04 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; 386

```console
$ docker pull adminer@sha256:2d74c7eb07a906d8e576f9e2c9971bdb01ab19aeba06478a94a9c273fa0992b6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (97013341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a850c42c8891f85474d75f6a74938ec55e1bad5d98e957cf59b54e8d6261e7`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Tue, 02 Jul 2024 01:40:38 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 01:40:38 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 01:40:38 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 01:40:38 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 01:40:38 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 01:40:38 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 01:40:50 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 01:40:50 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:40:50 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 01:40:51 GMT
USER adminer
# Tue, 02 Jul 2024 01:40:51 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 02 Jul 2024 01:40:51 GMT
EXPOSE 8080
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
	-	`sha256:8ae625b5731fddecf9b61034a28aedc8d9401e752eb6a7d261521555c3481791`  
		Last Modified: Tue, 02 Jul 2024 01:41:24 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a56bc1ddfe4d69136cc994627bbfeff96048814e1f5025b955be353df22753`  
		Last Modified: Tue, 02 Jul 2024 01:41:24 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6972d1f06dce91eb6060a692e744bf4b0e73bdbcebc740ab73f7249763c59101`  
		Last Modified: Tue, 02 Jul 2024 01:41:24 GMT  
		Size: 1.4 MB (1385010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b50df8e2047966f9043744696cacdc3a5735a5400851144fffc0f0d740dc1e`  
		Last Modified: Tue, 02 Jul 2024 01:41:24 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; mips64le

```console
$ docker pull adminer@sha256:8a01711066df85ed070620061fdd9e1631a1046badc61606c1e6ec8bdc01ec26
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92654371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43da756743e71ac148d7b882a8eb215791392ae2b763de8095c051a6cff1980d`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 23 Jul 2024 00:38:26 GMT
ADD file:3fbf62974aea46ff67427fd8996563bef3939ff51df600b4914acf5abb0b6c51 in / 
# Tue, 23 Jul 2024 00:38:32 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:12:17 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 02:14:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:14:15 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 02:14:23 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 02:14:26 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 02:14:30 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 02:14:34 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 02:14:37 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 02:14:41 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 02:15:33 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 02:15:36 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:15:40 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 02:15:44 GMT
USER adminer
# Tue, 23 Jul 2024 02:15:48 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 23 Jul 2024 02:15:51 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:6fba1199d77f2795fad97ca84f3d7030aab307e1ee7b582027c4e146bacdff14`  
		Last Modified: Tue, 23 Jul 2024 00:49:50 GMT  
		Size: 53.3 MB (53310598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb5ccc2e78cafd7a6bae2b97d6510ada07c2b60961937d42810594c7f3013c2`  
		Last Modified: Tue, 23 Jul 2024 02:18:19 GMT  
		Size: 38.0 MB (37953492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a7bda0b2932d324ef514eff7c5614353c086b9ea7ad4d853f8fd399c51b6d5`  
		Last Modified: Tue, 23 Jul 2024 02:17:52 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20433faf9234936c4ea8be2f288e5c392849bf726237f53f1ba83f71ada2288f`  
		Last Modified: Tue, 23 Jul 2024 02:17:52 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6157345705446634090f1dd03196240215199992409caa373077fa87e33a034a`  
		Last Modified: Tue, 23 Jul 2024 02:17:52 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537f5ec680d68403883c13e21ec08015d0e3df367b0efbd3b21f9461e43c9bd2`  
		Last Modified: Tue, 23 Jul 2024 02:17:53 GMT  
		Size: 1.4 MB (1386185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61a03247e49e3d869b1ec2b1062fd0cb20c2c04614d1964690602a169b6733e`  
		Last Modified: Tue, 23 Jul 2024 02:17:52 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:062d939387a558e07d69afde16e368e2fc7adc2e0c43700f46a6c448b8251ce3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101289185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0410f06417580c33e565abde408c17dfeed554975d02709ad62c95208b3ddace`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 23 Jul 2024 01:27:09 GMT
ADD file:538282e20405c23ce510f30f714f80393534997f12fd1cc25a8d7752dc6f1360 in / 
# Tue, 23 Jul 2024 01:27:11 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:25:37 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 02:26:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:26:23 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 02:26:24 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 02:26:25 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 02:26:25 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 02:26:25 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 02:26:25 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 02:26:25 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 02:26:44 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 02:26:44 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:26:45 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 02:26:45 GMT
USER adminer
# Tue, 23 Jul 2024 02:26:45 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 23 Jul 2024 02:26:46 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:fb0b8650d20e29c53f770b72d16b7381f876f2a0053fff3e542a0cc3f0b944b9`  
		Last Modified: Tue, 23 Jul 2024 01:31:32 GMT  
		Size: 59.0 MB (58954687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15738e55b04d20078f3d22ceaa5ebfefad42e7e68c55159ba9f1c6c96104c70a`  
		Last Modified: Tue, 23 Jul 2024 02:27:47 GMT  
		Size: 40.9 MB (40945047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1abb9adf68c77ddb45b48d87fa048994b191b50bb3dcdb65c5a1441b09236be1`  
		Last Modified: Tue, 23 Jul 2024 02:27:38 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69537e8ef3c397be4c3c4bbae3f729010605989d0e55e2e34dec154b6236d385`  
		Last Modified: Tue, 23 Jul 2024 02:27:38 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d85520057f355d14f85487174847109082913ae6990ae521b6c4771322126556`  
		Last Modified: Tue, 23 Jul 2024 02:27:38 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49b987d3a64b41a1a379cbae62ba6a452c233dea35255c15a96f51b7b2f2540`  
		Last Modified: Tue, 23 Jul 2024 02:27:38 GMT  
		Size: 1.4 MB (1385236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094977f5661e09079e9461e6361d77eba3c6d34b09f6673b43866e7684c00646`  
		Last Modified: Tue, 23 Jul 2024 02:27:38 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; s390x

```console
$ docker pull adminer@sha256:c7bff6b618579c93f078953be91ea47360675dbdb7db286ac4c7c7b7a2c31701
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93739700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ee3166c88912b6a2804b5d2bd37d20f188044e94b6ccf08ac6b5df23de3359`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 23 Jul 2024 02:28:03 GMT
ADD file:67d4db619a1cada17f248642d89d5b55ab04b5dd6885587148dedeb665795154 in / 
# Tue, 23 Jul 2024 02:28:06 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:03:04 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 03:03:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:03:30 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 03:03:30 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 03:03:30 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 03:03:31 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 03:03:31 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 03:03:31 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 03:03:31 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 03:03:40 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 03:03:40 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 03:03:40 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 03:03:41 GMT
USER adminer
# Tue, 23 Jul 2024 03:03:41 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 23 Jul 2024 03:03:41 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:0d03391dea2fdd66bd2c594e41ac7575c5879176469a4d1e7301b8498f5e5351`  
		Last Modified: Tue, 23 Jul 2024 02:32:57 GMT  
		Size: 53.3 MB (53324092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f9b72e50d6e2068c7b209cae11aad4b881a45ca10624ddffa7d47ba3dc5258`  
		Last Modified: Tue, 23 Jul 2024 03:04:21 GMT  
		Size: 39.0 MB (39026243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dab3bcf36e0afe3d1e0873b7ab407e216ba4abd68b83db207492bfcb2d0e49c`  
		Last Modified: Tue, 23 Jul 2024 03:04:14 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4cc17406257aa75797eefdc9f711a2a0ef93e0e8a4aa6fab92d8af10d5c9ef6`  
		Last Modified: Tue, 23 Jul 2024 03:04:14 GMT  
		Size: 1.9 KB (1852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe14ae12a8ee2216ee37cf525b13545cadabdbeb782ce5a62b37414bdca70862`  
		Last Modified: Tue, 23 Jul 2024 03:04:14 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef800a2307cd151cb4f22631273389647cac3f39394e0a093c0517adde471b0`  
		Last Modified: Tue, 23 Jul 2024 03:04:14 GMT  
		Size: 1.4 MB (1385146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5161f60448626f1dd88239bdbbf9a186fa2c1a53279e72e50e5f00a2ae987ae`  
		Last Modified: Tue, 23 Jul 2024 03:04:14 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4.8.1`

```console
$ docker pull adminer@sha256:115edb007e0a41e3743a88599b37bd48b8637bb286ef159af4b26f748fc53492
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
$ docker pull adminer@sha256:c31c78818756bdbed9bdaa64dc19e7f7edd51813a8ef89d538f72ea052dca1f1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95960190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b234f0237cfe467ceb1991adc8e536c60e2307752a844117e3506273c3cc70`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:11 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Tue, 02 Jul 2024 01:25:12 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:48:36 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 04:48:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:48:58 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 02 Jul 2024 04:48:59 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 04:48:59 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 04:48:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 04:48:59 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 04:48:59 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 04:48:59 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 04:49:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 04:49:11 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:49:11 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 04:49:11 GMT
USER adminer
# Tue, 02 Jul 2024 04:49:11 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 02 Jul 2024 04:49:11 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c31c6689a3eaf2e6cb8a6fcc48fb54fc6190f9a34f8be35dff81a5705565a1`  
		Last Modified: Tue, 02 Jul 2024 04:49:50 GMT  
		Size: 39.5 MB (39489478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15098df20048ca7252eef0cee4b2b60f5b4cfe226b37aee2f86c8b8b49ed12da`  
		Last Modified: Tue, 02 Jul 2024 04:49:43 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa436138c493f6b280d90f878c5f42e49161c213e07c63239dba3035d53200f`  
		Last Modified: Tue, 02 Jul 2024 04:49:43 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301530bfa5f53b39e40c2a73ab2943a95bb28f04dbd763bb519c82228cdb6330`  
		Last Modified: Tue, 02 Jul 2024 04:49:43 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b7955944f85a8d66bb95cdfbe4839dc329677da60416ebb8c1d09fef5ec295`  
		Last Modified: Tue, 02 Jul 2024 04:49:43 GMT  
		Size: 1.4 MB (1385152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d923a48aa5d0fcde247f30d40164b9ad0d68d576e0c37c3c69eb83e2dab736e5`  
		Last Modified: Tue, 02 Jul 2024 04:49:43 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1` - linux; arm variant v5

```console
$ docker pull adminer@sha256:0e52bfd1add93668146a0a1a5544187ee1dc9b4d9b0d7368ec3bd97f77037e9b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91225878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5fc5328a78544dcb2f0a078019b0bea7ab255b502c4eddbcbb0564c616436c`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Mon, 22 Jul 2024 23:57:12 GMT
ADD file:05c877f820dfe73bd5cecf959b857152065c40802cad0d9a46229bc0d5708339 in / 
# Mon, 22 Jul 2024 23:57:13 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 00:24:42 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 00:25:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 00:25:28 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 00:25:29 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 00:25:29 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 00:25:30 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 00:25:30 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 00:25:30 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 00:25:31 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 00:25:47 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 00:25:47 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 00:25:47 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 00:25:47 GMT
USER adminer
# Tue, 23 Jul 2024 00:25:47 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 23 Jul 2024 00:25:47 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:6faa199d3f09eecc4762c527abd2e9a5bc86f34a15c78145707b6b0b0ee526d5`  
		Last Modified: Tue, 23 Jul 2024 00:01:42 GMT  
		Size: 52.6 MB (52588961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea175fc25888492446b9545eb11532a36f0d62f3c448de0e72e72a2d4206256`  
		Last Modified: Tue, 23 Jul 2024 00:26:33 GMT  
		Size: 37.2 MB (37247611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aee3033b2b37548a5949367b960e0d3bb49c486d2b4911b024eadb15301d60f`  
		Last Modified: Tue, 23 Jul 2024 00:26:23 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc5b14232a5b77160d3deb0bbad3fab3c8aac724a97c519210b401938ee10a0`  
		Last Modified: Tue, 23 Jul 2024 00:26:23 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84cad97ff757120302d208a8b77f191afed2dc5624b7f563ca50c8894dac89f6`  
		Last Modified: Tue, 23 Jul 2024 00:26:23 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3600c4e5e44f075d5c68b7655b8084853942806b56b0ecd9baf6783a66197c`  
		Last Modified: Tue, 23 Jul 2024 00:26:23 GMT  
		Size: 1.4 MB (1385103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6851d528b265ea638bd0a586551d946177270672608fa4f8578c8420d0385cb9`  
		Last Modified: Tue, 23 Jul 2024 00:26:23 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1` - linux; arm variant v7

```console
$ docker pull adminer@sha256:02c012a3b47cb2dc2761b06eed691093d9e166216c92df475cbc9f8eadc9e5c8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87822374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8844c2056e0d57feaca4f1be1253bd8f8f2715f937cd842d1ccbef6c2f7fb2`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:18 GMT
ADD file:45e512d8c89ef619a4db87ca11813c5b48e6332c4c281a9f0d4aaf7301e85990 in / 
# Tue, 23 Jul 2024 03:03:18 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:52:31 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 03:53:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:53:47 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 03:53:49 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 03:53:49 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 03:53:50 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 03:53:50 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 03:53:50 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 03:53:51 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 03:54:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 03:54:18 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 03:54:19 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 03:54:19 GMT
USER adminer
# Tue, 23 Jul 2024 03:54:19 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 23 Jul 2024 03:54:19 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:57c3fa3d04a48c55117bbc60f2775c978886b3bc89b70e48e85c0516ce060947`  
		Last Modified: Tue, 23 Jul 2024 03:07:14 GMT  
		Size: 50.2 MB (50242355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef802d5de026a32dc791f808ef890fca768eb6e270e042642cf443affacfb85`  
		Last Modified: Tue, 23 Jul 2024 03:55:16 GMT  
		Size: 36.2 MB (36190522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa89f6dcd7fec84e6bdff0fa8ed984aebc82e025446b8d87445c270036259aa9`  
		Last Modified: Tue, 23 Jul 2024 03:55:07 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d6bc010107086de83c02e3740522ab10058840d9382aba4debea6502e49e1c`  
		Last Modified: Tue, 23 Jul 2024 03:55:07 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a76f8c1f42f47a8f9dc9bcdd1e024abe9951e9b58f03990d325c34484b042d`  
		Last Modified: Tue, 23 Jul 2024 03:55:07 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4fde1c1ed80b1b4ca7d8802b96bd546050fd8e0b862c6cd2f25f5b27655747`  
		Last Modified: Tue, 23 Jul 2024 03:55:07 GMT  
		Size: 1.4 MB (1385292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d19e9266c2d80bfe86943cee6ac09b905d99cba1d9b5c0b1b1b444eac73acfd`  
		Last Modified: Tue, 23 Jul 2024 03:55:07 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:b03c33368be4bba59f14aaf0cded44fcdc50e355c9bfa19cc3c44d106c4713e0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94358345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299c22d3acc4de54d764bad9b1076848198e8e46a67fc4245d04908c6f28e6dd`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Tue, 02 Jul 2024 03:49:31 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 03:49:31 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 03:49:31 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 03:49:31 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 03:49:31 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 03:49:31 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 03:49:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 03:49:41 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:49:41 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 03:49:41 GMT
USER adminer
# Tue, 02 Jul 2024 03:49:41 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 02 Jul 2024 03:49:42 GMT
EXPOSE 8080
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
	-	`sha256:ca7a060c53754e1f602d8bcd48248ebf6552078b1b5399f1e2bc003e28df66a3`  
		Last Modified: Tue, 02 Jul 2024 03:50:04 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fbd5efe441c2e90738651736224a0fe724fd712995f15c157b715b38b9b9b6`  
		Last Modified: Tue, 02 Jul 2024 03:50:04 GMT  
		Size: 1.5 KB (1483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee7687bec909e9911339ab8fc15c7213b444003fd7dbaa0628eea3d211c7834`  
		Last Modified: Tue, 02 Jul 2024 03:50:05 GMT  
		Size: 1.4 MB (1385094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acee67427be79e892393ce058a4d79428ae50d525217d0cceb4b31ad4c46f482`  
		Last Modified: Tue, 02 Jul 2024 03:50:04 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1` - linux; 386

```console
$ docker pull adminer@sha256:2d74c7eb07a906d8e576f9e2c9971bdb01ab19aeba06478a94a9c273fa0992b6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (97013341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a850c42c8891f85474d75f6a74938ec55e1bad5d98e957cf59b54e8d6261e7`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Tue, 02 Jul 2024 01:40:38 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 01:40:38 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 01:40:38 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 01:40:38 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 01:40:38 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 01:40:38 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 01:40:50 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 01:40:50 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:40:50 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 01:40:51 GMT
USER adminer
# Tue, 02 Jul 2024 01:40:51 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 02 Jul 2024 01:40:51 GMT
EXPOSE 8080
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
	-	`sha256:8ae625b5731fddecf9b61034a28aedc8d9401e752eb6a7d261521555c3481791`  
		Last Modified: Tue, 02 Jul 2024 01:41:24 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a56bc1ddfe4d69136cc994627bbfeff96048814e1f5025b955be353df22753`  
		Last Modified: Tue, 02 Jul 2024 01:41:24 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6972d1f06dce91eb6060a692e744bf4b0e73bdbcebc740ab73f7249763c59101`  
		Last Modified: Tue, 02 Jul 2024 01:41:24 GMT  
		Size: 1.4 MB (1385010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b50df8e2047966f9043744696cacdc3a5735a5400851144fffc0f0d740dc1e`  
		Last Modified: Tue, 02 Jul 2024 01:41:24 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1` - linux; mips64le

```console
$ docker pull adminer@sha256:8a01711066df85ed070620061fdd9e1631a1046badc61606c1e6ec8bdc01ec26
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92654371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43da756743e71ac148d7b882a8eb215791392ae2b763de8095c051a6cff1980d`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 23 Jul 2024 00:38:26 GMT
ADD file:3fbf62974aea46ff67427fd8996563bef3939ff51df600b4914acf5abb0b6c51 in / 
# Tue, 23 Jul 2024 00:38:32 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:12:17 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 02:14:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:14:15 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 02:14:23 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 02:14:26 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 02:14:30 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 02:14:34 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 02:14:37 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 02:14:41 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 02:15:33 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 02:15:36 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:15:40 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 02:15:44 GMT
USER adminer
# Tue, 23 Jul 2024 02:15:48 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 23 Jul 2024 02:15:51 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:6fba1199d77f2795fad97ca84f3d7030aab307e1ee7b582027c4e146bacdff14`  
		Last Modified: Tue, 23 Jul 2024 00:49:50 GMT  
		Size: 53.3 MB (53310598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb5ccc2e78cafd7a6bae2b97d6510ada07c2b60961937d42810594c7f3013c2`  
		Last Modified: Tue, 23 Jul 2024 02:18:19 GMT  
		Size: 38.0 MB (37953492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a7bda0b2932d324ef514eff7c5614353c086b9ea7ad4d853f8fd399c51b6d5`  
		Last Modified: Tue, 23 Jul 2024 02:17:52 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20433faf9234936c4ea8be2f288e5c392849bf726237f53f1ba83f71ada2288f`  
		Last Modified: Tue, 23 Jul 2024 02:17:52 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6157345705446634090f1dd03196240215199992409caa373077fa87e33a034a`  
		Last Modified: Tue, 23 Jul 2024 02:17:52 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537f5ec680d68403883c13e21ec08015d0e3df367b0efbd3b21f9461e43c9bd2`  
		Last Modified: Tue, 23 Jul 2024 02:17:53 GMT  
		Size: 1.4 MB (1386185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61a03247e49e3d869b1ec2b1062fd0cb20c2c04614d1964690602a169b6733e`  
		Last Modified: Tue, 23 Jul 2024 02:17:52 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1` - linux; ppc64le

```console
$ docker pull adminer@sha256:062d939387a558e07d69afde16e368e2fc7adc2e0c43700f46a6c448b8251ce3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101289185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0410f06417580c33e565abde408c17dfeed554975d02709ad62c95208b3ddace`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 23 Jul 2024 01:27:09 GMT
ADD file:538282e20405c23ce510f30f714f80393534997f12fd1cc25a8d7752dc6f1360 in / 
# Tue, 23 Jul 2024 01:27:11 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:25:37 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 02:26:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:26:23 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 02:26:24 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 02:26:25 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 02:26:25 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 02:26:25 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 02:26:25 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 02:26:25 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 02:26:44 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 02:26:44 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:26:45 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 02:26:45 GMT
USER adminer
# Tue, 23 Jul 2024 02:26:45 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 23 Jul 2024 02:26:46 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:fb0b8650d20e29c53f770b72d16b7381f876f2a0053fff3e542a0cc3f0b944b9`  
		Last Modified: Tue, 23 Jul 2024 01:31:32 GMT  
		Size: 59.0 MB (58954687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15738e55b04d20078f3d22ceaa5ebfefad42e7e68c55159ba9f1c6c96104c70a`  
		Last Modified: Tue, 23 Jul 2024 02:27:47 GMT  
		Size: 40.9 MB (40945047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1abb9adf68c77ddb45b48d87fa048994b191b50bb3dcdb65c5a1441b09236be1`  
		Last Modified: Tue, 23 Jul 2024 02:27:38 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69537e8ef3c397be4c3c4bbae3f729010605989d0e55e2e34dec154b6236d385`  
		Last Modified: Tue, 23 Jul 2024 02:27:38 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d85520057f355d14f85487174847109082913ae6990ae521b6c4771322126556`  
		Last Modified: Tue, 23 Jul 2024 02:27:38 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49b987d3a64b41a1a379cbae62ba6a452c233dea35255c15a96f51b7b2f2540`  
		Last Modified: Tue, 23 Jul 2024 02:27:38 GMT  
		Size: 1.4 MB (1385236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094977f5661e09079e9461e6361d77eba3c6d34b09f6673b43866e7684c00646`  
		Last Modified: Tue, 23 Jul 2024 02:27:38 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1` - linux; s390x

```console
$ docker pull adminer@sha256:c7bff6b618579c93f078953be91ea47360675dbdb7db286ac4c7c7b7a2c31701
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93739700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ee3166c88912b6a2804b5d2bd37d20f188044e94b6ccf08ac6b5df23de3359`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 23 Jul 2024 02:28:03 GMT
ADD file:67d4db619a1cada17f248642d89d5b55ab04b5dd6885587148dedeb665795154 in / 
# Tue, 23 Jul 2024 02:28:06 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:03:04 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 03:03:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:03:30 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 03:03:30 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 03:03:30 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 03:03:31 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 03:03:31 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 03:03:31 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 03:03:31 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 03:03:40 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 03:03:40 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 03:03:40 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 03:03:41 GMT
USER adminer
# Tue, 23 Jul 2024 03:03:41 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 23 Jul 2024 03:03:41 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:0d03391dea2fdd66bd2c594e41ac7575c5879176469a4d1e7301b8498f5e5351`  
		Last Modified: Tue, 23 Jul 2024 02:32:57 GMT  
		Size: 53.3 MB (53324092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f9b72e50d6e2068c7b209cae11aad4b881a45ca10624ddffa7d47ba3dc5258`  
		Last Modified: Tue, 23 Jul 2024 03:04:21 GMT  
		Size: 39.0 MB (39026243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dab3bcf36e0afe3d1e0873b7ab407e216ba4abd68b83db207492bfcb2d0e49c`  
		Last Modified: Tue, 23 Jul 2024 03:04:14 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4cc17406257aa75797eefdc9f711a2a0ef93e0e8a4aa6fab92d8af10d5c9ef6`  
		Last Modified: Tue, 23 Jul 2024 03:04:14 GMT  
		Size: 1.9 KB (1852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe14ae12a8ee2216ee37cf525b13545cadabdbeb782ce5a62b37414bdca70862`  
		Last Modified: Tue, 23 Jul 2024 03:04:14 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef800a2307cd151cb4f22631273389647cac3f39394e0a093c0517adde471b0`  
		Last Modified: Tue, 23 Jul 2024 03:04:14 GMT  
		Size: 1.4 MB (1385146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5161f60448626f1dd88239bdbbf9a186fa2c1a53279e72e50e5f00a2ae987ae`  
		Last Modified: Tue, 23 Jul 2024 03:04:14 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4.8.1-fastcgi`

```console
$ docker pull adminer@sha256:cf3d7106f4d11d07a86fb2690a879e522d0561f8136b38a67fdc2bf4eba11c76
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
$ docker pull adminer@sha256:a65f9f3444eecf907fde215fd40219387c99f7d0927ad94fec2fad3d0c91df5c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95962913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b4a63db34258ca6af0f56fcd13e485f38764b0959c6119d1cbda4a1e920532`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:11 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Tue, 02 Jul 2024 01:25:12 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:48:36 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 04:48:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:48:58 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 02 Jul 2024 04:49:18 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 02 Jul 2024 04:49:19 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 04:49:19 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 04:49:19 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 04:49:19 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 04:49:19 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 04:49:19 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 04:49:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 04:49:30 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:49:30 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 04:49:30 GMT
USER adminer
# Tue, 02 Jul 2024 04:49:30 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c31c6689a3eaf2e6cb8a6fcc48fb54fc6190f9a34f8be35dff81a5705565a1`  
		Last Modified: Tue, 02 Jul 2024 04:49:50 GMT  
		Size: 39.5 MB (39489478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15098df20048ca7252eef0cee4b2b60f5b4cfe226b37aee2f86c8b8b49ed12da`  
		Last Modified: Tue, 02 Jul 2024 04:49:43 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7fc47a846479bc3911ccdaed2236fdb846714f9db30dd02d466e224cc5a895`  
		Last Modified: Tue, 02 Jul 2024 04:50:05 GMT  
		Size: 2.7 KB (2711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4d59e9486f131dfc50c56f5ee19dd29849461da1378eab3cb1ffbb7184023f3`  
		Last Modified: Tue, 02 Jul 2024 04:50:05 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f25810dba66fe09876afbcf9e8e39d8456c82613cfc63ac0a7f39738bc27c6`  
		Last Modified: Tue, 02 Jul 2024 04:50:05 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96bea11c7f0698a423d992a197aed5b28d6b8d11d745824720eab682f125c2a`  
		Last Modified: Tue, 02 Jul 2024 04:50:06 GMT  
		Size: 1.4 MB (1385158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8ec6f28e566eaec9db9f59408e63b3d58c7595bca0c831fa9286ebca0f2e29`  
		Last Modified: Tue, 02 Jul 2024 04:50:05 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-fastcgi` - linux; arm variant v5

```console
$ docker pull adminer@sha256:28b821bf07d3288ef8624aba4e348e6c5df13a1c8de63390117bd668767bf873
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91228595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:774685cf6d16dadfa8b111a578dc98947b40415930473f195ea4f3178bbf702f`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Mon, 22 Jul 2024 23:57:12 GMT
ADD file:05c877f820dfe73bd5cecf959b857152065c40802cad0d9a46229bc0d5708339 in / 
# Mon, 22 Jul 2024 23:57:13 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 00:24:42 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 00:25:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 00:25:28 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 00:25:53 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 23 Jul 2024 00:25:54 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 00:25:54 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 00:25:54 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 00:25:54 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 00:25:55 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 00:25:55 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 00:26:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 00:26:10 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 00:26:10 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 00:26:10 GMT
USER adminer
# Tue, 23 Jul 2024 00:26:10 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:6faa199d3f09eecc4762c527abd2e9a5bc86f34a15c78145707b6b0b0ee526d5`  
		Last Modified: Tue, 23 Jul 2024 00:01:42 GMT  
		Size: 52.6 MB (52588961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea175fc25888492446b9545eb11532a36f0d62f3c448de0e72e72a2d4206256`  
		Last Modified: Tue, 23 Jul 2024 00:26:33 GMT  
		Size: 37.2 MB (37247611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aee3033b2b37548a5949367b960e0d3bb49c486d2b4911b024eadb15301d60f`  
		Last Modified: Tue, 23 Jul 2024 00:26:23 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2c14f7e1bfcd1615af505b8319319293cfc170c1feff406f0848d749207bb3`  
		Last Modified: Tue, 23 Jul 2024 00:26:48 GMT  
		Size: 2.7 KB (2715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d26206279c33af8163e48ff66f061c62670069788764b804f76ebdeb5c45be4`  
		Last Modified: Tue, 23 Jul 2024 00:26:48 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36113ffa34469c443f81198f38fef456743291a808133ba71d7b4724e84a1544`  
		Last Modified: Tue, 23 Jul 2024 00:26:48 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2353bf2bc981df8102745bff3ef704ca29e64af6ac487352ed4123647aed2c26`  
		Last Modified: Tue, 23 Jul 2024 00:26:48 GMT  
		Size: 1.4 MB (1385100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7bc91ac0a2b45c59d8992cc845dfdf83f6876423d1f3a4f128fbf503c7f43b`  
		Last Modified: Tue, 23 Jul 2024 00:26:48 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:940499184855825584dffe9b581a4e3d892cda313e8ba1f06f4c0f184d5bc108
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87825032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04142ce31ca904ea987e19dc4b5162e4f1640898ef5b8e4ff2783137dfd80730`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:18 GMT
ADD file:45e512d8c89ef619a4db87ca11813c5b48e6332c4c281a9f0d4aaf7301e85990 in / 
# Tue, 23 Jul 2024 03:03:18 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:52:31 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 03:53:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:53:47 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 03:54:25 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 23 Jul 2024 03:54:27 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 03:54:27 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 03:54:28 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 03:54:28 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 03:54:29 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 03:54:29 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 03:54:50 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 03:54:50 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 03:54:51 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 03:54:51 GMT
USER adminer
# Tue, 23 Jul 2024 03:54:51 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:57c3fa3d04a48c55117bbc60f2775c978886b3bc89b70e48e85c0516ce060947`  
		Last Modified: Tue, 23 Jul 2024 03:07:14 GMT  
		Size: 50.2 MB (50242355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef802d5de026a32dc791f808ef890fca768eb6e270e042642cf443affacfb85`  
		Last Modified: Tue, 23 Jul 2024 03:55:16 GMT  
		Size: 36.2 MB (36190522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa89f6dcd7fec84e6bdff0fa8ed984aebc82e025446b8d87445c270036259aa9`  
		Last Modified: Tue, 23 Jul 2024 03:55:07 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f0ffae6b7a4e7300b5fcc49bdc2bc9b2ad8b6746611c7e99b291ab33fffb3a`  
		Last Modified: Tue, 23 Jul 2024 03:55:32 GMT  
		Size: 2.7 KB (2715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfddd9483e786ea5d31fb2009e0addd025d8cfa3cc664f3a52753091f01dbe0c`  
		Last Modified: Tue, 23 Jul 2024 03:55:32 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff45e2ad6c3b6e678cc25d6976ac0a3a174d46e13268c21d32e308693ec1831`  
		Last Modified: Tue, 23 Jul 2024 03:55:32 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a8c797535832a99c8d88455fe604811f0c45be3d9d29160b653ad03507acdf`  
		Last Modified: Tue, 23 Jul 2024 03:55:33 GMT  
		Size: 1.4 MB (1385237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e909ef8532fe9e3e6c08fb74bd399bce640eb766fc731570b45abdf9c646eb34`  
		Last Modified: Tue, 23 Jul 2024 03:55:33 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-fastcgi` - linux; arm64 variant v8

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

### `adminer:4.8.1-fastcgi` - linux; 386

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

### `adminer:4.8.1-fastcgi` - linux; mips64le

```console
$ docker pull adminer@sha256:8b5a58dc254439c686e7e263f42168f58ed7a06c2af794b7d4d6a5827f0fd314
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92657102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b23cd2579b0ea5c2e2e6391da4fef0599634b6d8e1c0ae92ba67507153281f`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 23 Jul 2024 00:38:26 GMT
ADD file:3fbf62974aea46ff67427fd8996563bef3939ff51df600b4914acf5abb0b6c51 in / 
# Tue, 23 Jul 2024 00:38:32 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:12:17 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 02:14:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:14:15 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 02:16:05 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 23 Jul 2024 02:16:12 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 02:16:16 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 02:16:20 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 02:16:23 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 02:16:27 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 02:16:31 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 02:17:20 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 02:17:24 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:17:27 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 02:17:31 GMT
USER adminer
# Tue, 23 Jul 2024 02:17:35 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:6fba1199d77f2795fad97ca84f3d7030aab307e1ee7b582027c4e146bacdff14`  
		Last Modified: Tue, 23 Jul 2024 00:49:50 GMT  
		Size: 53.3 MB (53310598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb5ccc2e78cafd7a6bae2b97d6510ada07c2b60961937d42810594c7f3013c2`  
		Last Modified: Tue, 23 Jul 2024 02:18:19 GMT  
		Size: 38.0 MB (37953492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a7bda0b2932d324ef514eff7c5614353c086b9ea7ad4d853f8fd399c51b6d5`  
		Last Modified: Tue, 23 Jul 2024 02:17:52 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee2d26e1899d8a8b268f6ef6d98db730bc341ff6913ace137afde90c8f7ba6c`  
		Last Modified: Tue, 23 Jul 2024 02:18:41 GMT  
		Size: 2.7 KB (2713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76695ee7cfcc7aad4ed6cc2ce0a15b5e71207ab0ccae36294cdeac0cc71ddbf`  
		Last Modified: Tue, 23 Jul 2024 02:18:41 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee98dea0703c2f60a2e4bf777be8e50a609fbe5658ef913b93fddbb604d6e96a`  
		Last Modified: Tue, 23 Jul 2024 02:18:41 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e924f48a941a9836a5762905bb73e501a9c08ec789d9975f88590718f6c0ba`  
		Last Modified: Tue, 23 Jul 2024 02:18:43 GMT  
		Size: 1.4 MB (1386197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77965a700523588d06e3d8ab1c0586c82d83796fbe6949c87d3177d7dd97c701`  
		Last Modified: Tue, 23 Jul 2024 02:18:42 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:dee0c7bb9a7b5aaac331c29123d62662d900d6d1e0d1bf0becc95e9dc35d3599
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101291907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ea903255a4ffa78793f81ea18f5a4560af79838030fbf4c55516f80934f152`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 23 Jul 2024 01:27:09 GMT
ADD file:538282e20405c23ce510f30f714f80393534997f12fd1cc25a8d7752dc6f1360 in / 
# Tue, 23 Jul 2024 01:27:11 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:25:37 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 02:26:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:26:23 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 02:27:02 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 23 Jul 2024 02:27:04 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 02:27:04 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 02:27:04 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 02:27:05 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 02:27:05 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 02:27:05 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 02:27:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 02:27:24 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:27:24 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 02:27:24 GMT
USER adminer
# Tue, 23 Jul 2024 02:27:25 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:fb0b8650d20e29c53f770b72d16b7381f876f2a0053fff3e542a0cc3f0b944b9`  
		Last Modified: Tue, 23 Jul 2024 01:31:32 GMT  
		Size: 59.0 MB (58954687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15738e55b04d20078f3d22ceaa5ebfefad42e7e68c55159ba9f1c6c96104c70a`  
		Last Modified: Tue, 23 Jul 2024 02:27:47 GMT  
		Size: 40.9 MB (40945047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1abb9adf68c77ddb45b48d87fa048994b191b50bb3dcdb65c5a1441b09236be1`  
		Last Modified: Tue, 23 Jul 2024 02:27:38 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8cfaf311da16a0e82541813e3f196fbb549b8d3b4c5d00a0706e9bb113ab61`  
		Last Modified: Tue, 23 Jul 2024 02:28:03 GMT  
		Size: 2.7 KB (2712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97ca69cb806636211daf12ba75a96f6dcd060f44f8de9c8c01f4e7603ad16c4`  
		Last Modified: Tue, 23 Jul 2024 02:28:02 GMT  
		Size: 1.8 KB (1847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0cb83b55519a88ad23c909874d20b54e854376a784207653c4be6f23c73ccc`  
		Last Modified: Tue, 23 Jul 2024 02:28:02 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7531a129bc98acb32209bb040ce99bb7d30fcb76dab8ded8ef5cd08a179854`  
		Last Modified: Tue, 23 Jul 2024 02:28:03 GMT  
		Size: 1.4 MB (1385246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d48a360d8a16035cc5528cd6bc0e45116f172e7c3d935c20ae81eb64111bc3`  
		Last Modified: Tue, 23 Jul 2024 02:28:02 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-fastcgi` - linux; s390x

```console
$ docker pull adminer@sha256:5b68c11e23080d7d4f5e745202d62cf73c411b3b6e45519dd1342175e8155e1f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93742391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c221ef6b6f73482a2313e8fe83b8667520970e85e5c41919dbbaa6e72524e1a8`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 23 Jul 2024 02:28:03 GMT
ADD file:67d4db619a1cada17f248642d89d5b55ab04b5dd6885587148dedeb665795154 in / 
# Tue, 23 Jul 2024 02:28:06 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:03:04 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 03:03:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:03:30 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 03:03:51 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 23 Jul 2024 03:03:51 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 03:03:51 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 03:03:51 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 03:03:52 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 03:03:52 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 03:03:52 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 03:04:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 03:04:00 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 03:04:00 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 03:04:00 GMT
USER adminer
# Tue, 23 Jul 2024 03:04:01 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:0d03391dea2fdd66bd2c594e41ac7575c5879176469a4d1e7301b8498f5e5351`  
		Last Modified: Tue, 23 Jul 2024 02:32:57 GMT  
		Size: 53.3 MB (53324092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f9b72e50d6e2068c7b209cae11aad4b881a45ca10624ddffa7d47ba3dc5258`  
		Last Modified: Tue, 23 Jul 2024 03:04:21 GMT  
		Size: 39.0 MB (39026243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dab3bcf36e0afe3d1e0873b7ab407e216ba4abd68b83db207492bfcb2d0e49c`  
		Last Modified: Tue, 23 Jul 2024 03:04:14 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fa842b8d20c971ec35b7b1fd365ebcf06eba7c327f8d3152c8fca17c0e7665`  
		Last Modified: Tue, 23 Jul 2024 03:04:31 GMT  
		Size: 2.7 KB (2709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29efb99675faf1ec4ca57f74dc079ff104548b494b6df8e1ab865f7d1835be99`  
		Last Modified: Tue, 23 Jul 2024 03:04:31 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769d57125a6627215e8720ac3e31b9de7c9d1c2abc3423baecb12e25a1b5729d`  
		Last Modified: Tue, 23 Jul 2024 03:04:31 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f056b55ddb3c62ad27de0b76cafcb5d832cc6d481b3765f7bf3c372bd23890`  
		Last Modified: Tue, 23 Jul 2024 03:04:31 GMT  
		Size: 1.4 MB (1385141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c5a5212a250c3a34617fd215b8dd86b707ceacbd89602ca27b62c14d9ad009`  
		Last Modified: Tue, 23 Jul 2024 03:04:31 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4.8.1-standalone`

```console
$ docker pull adminer@sha256:115edb007e0a41e3743a88599b37bd48b8637bb286ef159af4b26f748fc53492
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
$ docker pull adminer@sha256:c31c78818756bdbed9bdaa64dc19e7f7edd51813a8ef89d538f72ea052dca1f1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95960190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b234f0237cfe467ceb1991adc8e536c60e2307752a844117e3506273c3cc70`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:11 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Tue, 02 Jul 2024 01:25:12 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:48:36 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 04:48:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:48:58 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 02 Jul 2024 04:48:59 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 04:48:59 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 04:48:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 04:48:59 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 04:48:59 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 04:48:59 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 04:49:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 04:49:11 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:49:11 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 04:49:11 GMT
USER adminer
# Tue, 02 Jul 2024 04:49:11 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 02 Jul 2024 04:49:11 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c31c6689a3eaf2e6cb8a6fcc48fb54fc6190f9a34f8be35dff81a5705565a1`  
		Last Modified: Tue, 02 Jul 2024 04:49:50 GMT  
		Size: 39.5 MB (39489478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15098df20048ca7252eef0cee4b2b60f5b4cfe226b37aee2f86c8b8b49ed12da`  
		Last Modified: Tue, 02 Jul 2024 04:49:43 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa436138c493f6b280d90f878c5f42e49161c213e07c63239dba3035d53200f`  
		Last Modified: Tue, 02 Jul 2024 04:49:43 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301530bfa5f53b39e40c2a73ab2943a95bb28f04dbd763bb519c82228cdb6330`  
		Last Modified: Tue, 02 Jul 2024 04:49:43 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b7955944f85a8d66bb95cdfbe4839dc329677da60416ebb8c1d09fef5ec295`  
		Last Modified: Tue, 02 Jul 2024 04:49:43 GMT  
		Size: 1.4 MB (1385152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d923a48aa5d0fcde247f30d40164b9ad0d68d576e0c37c3c69eb83e2dab736e5`  
		Last Modified: Tue, 02 Jul 2024 04:49:43 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-standalone` - linux; arm variant v5

```console
$ docker pull adminer@sha256:0e52bfd1add93668146a0a1a5544187ee1dc9b4d9b0d7368ec3bd97f77037e9b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91225878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5fc5328a78544dcb2f0a078019b0bea7ab255b502c4eddbcbb0564c616436c`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Mon, 22 Jul 2024 23:57:12 GMT
ADD file:05c877f820dfe73bd5cecf959b857152065c40802cad0d9a46229bc0d5708339 in / 
# Mon, 22 Jul 2024 23:57:13 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 00:24:42 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 00:25:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 00:25:28 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 00:25:29 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 00:25:29 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 00:25:30 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 00:25:30 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 00:25:30 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 00:25:31 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 00:25:47 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 00:25:47 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 00:25:47 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 00:25:47 GMT
USER adminer
# Tue, 23 Jul 2024 00:25:47 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 23 Jul 2024 00:25:47 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:6faa199d3f09eecc4762c527abd2e9a5bc86f34a15c78145707b6b0b0ee526d5`  
		Last Modified: Tue, 23 Jul 2024 00:01:42 GMT  
		Size: 52.6 MB (52588961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea175fc25888492446b9545eb11532a36f0d62f3c448de0e72e72a2d4206256`  
		Last Modified: Tue, 23 Jul 2024 00:26:33 GMT  
		Size: 37.2 MB (37247611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aee3033b2b37548a5949367b960e0d3bb49c486d2b4911b024eadb15301d60f`  
		Last Modified: Tue, 23 Jul 2024 00:26:23 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc5b14232a5b77160d3deb0bbad3fab3c8aac724a97c519210b401938ee10a0`  
		Last Modified: Tue, 23 Jul 2024 00:26:23 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84cad97ff757120302d208a8b77f191afed2dc5624b7f563ca50c8894dac89f6`  
		Last Modified: Tue, 23 Jul 2024 00:26:23 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3600c4e5e44f075d5c68b7655b8084853942806b56b0ecd9baf6783a66197c`  
		Last Modified: Tue, 23 Jul 2024 00:26:23 GMT  
		Size: 1.4 MB (1385103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6851d528b265ea638bd0a586551d946177270672608fa4f8578c8420d0385cb9`  
		Last Modified: Tue, 23 Jul 2024 00:26:23 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:02c012a3b47cb2dc2761b06eed691093d9e166216c92df475cbc9f8eadc9e5c8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87822374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8844c2056e0d57feaca4f1be1253bd8f8f2715f937cd842d1ccbef6c2f7fb2`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:18 GMT
ADD file:45e512d8c89ef619a4db87ca11813c5b48e6332c4c281a9f0d4aaf7301e85990 in / 
# Tue, 23 Jul 2024 03:03:18 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:52:31 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 03:53:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:53:47 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 03:53:49 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 03:53:49 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 03:53:50 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 03:53:50 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 03:53:50 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 03:53:51 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 03:54:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 03:54:18 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 03:54:19 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 03:54:19 GMT
USER adminer
# Tue, 23 Jul 2024 03:54:19 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 23 Jul 2024 03:54:19 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:57c3fa3d04a48c55117bbc60f2775c978886b3bc89b70e48e85c0516ce060947`  
		Last Modified: Tue, 23 Jul 2024 03:07:14 GMT  
		Size: 50.2 MB (50242355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef802d5de026a32dc791f808ef890fca768eb6e270e042642cf443affacfb85`  
		Last Modified: Tue, 23 Jul 2024 03:55:16 GMT  
		Size: 36.2 MB (36190522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa89f6dcd7fec84e6bdff0fa8ed984aebc82e025446b8d87445c270036259aa9`  
		Last Modified: Tue, 23 Jul 2024 03:55:07 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d6bc010107086de83c02e3740522ab10058840d9382aba4debea6502e49e1c`  
		Last Modified: Tue, 23 Jul 2024 03:55:07 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a76f8c1f42f47a8f9dc9bcdd1e024abe9951e9b58f03990d325c34484b042d`  
		Last Modified: Tue, 23 Jul 2024 03:55:07 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4fde1c1ed80b1b4ca7d8802b96bd546050fd8e0b862c6cd2f25f5b27655747`  
		Last Modified: Tue, 23 Jul 2024 03:55:07 GMT  
		Size: 1.4 MB (1385292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d19e9266c2d80bfe86943cee6ac09b905d99cba1d9b5c0b1b1b444eac73acfd`  
		Last Modified: Tue, 23 Jul 2024 03:55:07 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-standalone` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:b03c33368be4bba59f14aaf0cded44fcdc50e355c9bfa19cc3c44d106c4713e0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94358345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299c22d3acc4de54d764bad9b1076848198e8e46a67fc4245d04908c6f28e6dd`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Tue, 02 Jul 2024 03:49:31 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 03:49:31 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 03:49:31 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 03:49:31 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 03:49:31 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 03:49:31 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 03:49:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 03:49:41 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:49:41 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 03:49:41 GMT
USER adminer
# Tue, 02 Jul 2024 03:49:41 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 02 Jul 2024 03:49:42 GMT
EXPOSE 8080
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
	-	`sha256:ca7a060c53754e1f602d8bcd48248ebf6552078b1b5399f1e2bc003e28df66a3`  
		Last Modified: Tue, 02 Jul 2024 03:50:04 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fbd5efe441c2e90738651736224a0fe724fd712995f15c157b715b38b9b9b6`  
		Last Modified: Tue, 02 Jul 2024 03:50:04 GMT  
		Size: 1.5 KB (1483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee7687bec909e9911339ab8fc15c7213b444003fd7dbaa0628eea3d211c7834`  
		Last Modified: Tue, 02 Jul 2024 03:50:05 GMT  
		Size: 1.4 MB (1385094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acee67427be79e892393ce058a4d79428ae50d525217d0cceb4b31ad4c46f482`  
		Last Modified: Tue, 02 Jul 2024 03:50:04 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-standalone` - linux; 386

```console
$ docker pull adminer@sha256:2d74c7eb07a906d8e576f9e2c9971bdb01ab19aeba06478a94a9c273fa0992b6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (97013341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a850c42c8891f85474d75f6a74938ec55e1bad5d98e957cf59b54e8d6261e7`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Tue, 02 Jul 2024 01:40:38 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 01:40:38 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 01:40:38 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 01:40:38 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 01:40:38 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 01:40:38 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 01:40:50 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 01:40:50 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:40:50 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 01:40:51 GMT
USER adminer
# Tue, 02 Jul 2024 01:40:51 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 02 Jul 2024 01:40:51 GMT
EXPOSE 8080
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
	-	`sha256:8ae625b5731fddecf9b61034a28aedc8d9401e752eb6a7d261521555c3481791`  
		Last Modified: Tue, 02 Jul 2024 01:41:24 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a56bc1ddfe4d69136cc994627bbfeff96048814e1f5025b955be353df22753`  
		Last Modified: Tue, 02 Jul 2024 01:41:24 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6972d1f06dce91eb6060a692e744bf4b0e73bdbcebc740ab73f7249763c59101`  
		Last Modified: Tue, 02 Jul 2024 01:41:24 GMT  
		Size: 1.4 MB (1385010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b50df8e2047966f9043744696cacdc3a5735a5400851144fffc0f0d740dc1e`  
		Last Modified: Tue, 02 Jul 2024 01:41:24 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-standalone` - linux; mips64le

```console
$ docker pull adminer@sha256:8a01711066df85ed070620061fdd9e1631a1046badc61606c1e6ec8bdc01ec26
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92654371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43da756743e71ac148d7b882a8eb215791392ae2b763de8095c051a6cff1980d`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 23 Jul 2024 00:38:26 GMT
ADD file:3fbf62974aea46ff67427fd8996563bef3939ff51df600b4914acf5abb0b6c51 in / 
# Tue, 23 Jul 2024 00:38:32 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:12:17 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 02:14:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:14:15 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 02:14:23 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 02:14:26 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 02:14:30 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 02:14:34 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 02:14:37 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 02:14:41 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 02:15:33 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 02:15:36 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:15:40 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 02:15:44 GMT
USER adminer
# Tue, 23 Jul 2024 02:15:48 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 23 Jul 2024 02:15:51 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:6fba1199d77f2795fad97ca84f3d7030aab307e1ee7b582027c4e146bacdff14`  
		Last Modified: Tue, 23 Jul 2024 00:49:50 GMT  
		Size: 53.3 MB (53310598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb5ccc2e78cafd7a6bae2b97d6510ada07c2b60961937d42810594c7f3013c2`  
		Last Modified: Tue, 23 Jul 2024 02:18:19 GMT  
		Size: 38.0 MB (37953492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a7bda0b2932d324ef514eff7c5614353c086b9ea7ad4d853f8fd399c51b6d5`  
		Last Modified: Tue, 23 Jul 2024 02:17:52 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20433faf9234936c4ea8be2f288e5c392849bf726237f53f1ba83f71ada2288f`  
		Last Modified: Tue, 23 Jul 2024 02:17:52 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6157345705446634090f1dd03196240215199992409caa373077fa87e33a034a`  
		Last Modified: Tue, 23 Jul 2024 02:17:52 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537f5ec680d68403883c13e21ec08015d0e3df367b0efbd3b21f9461e43c9bd2`  
		Last Modified: Tue, 23 Jul 2024 02:17:53 GMT  
		Size: 1.4 MB (1386185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61a03247e49e3d869b1ec2b1062fd0cb20c2c04614d1964690602a169b6733e`  
		Last Modified: Tue, 23 Jul 2024 02:17:52 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:062d939387a558e07d69afde16e368e2fc7adc2e0c43700f46a6c448b8251ce3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101289185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0410f06417580c33e565abde408c17dfeed554975d02709ad62c95208b3ddace`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 23 Jul 2024 01:27:09 GMT
ADD file:538282e20405c23ce510f30f714f80393534997f12fd1cc25a8d7752dc6f1360 in / 
# Tue, 23 Jul 2024 01:27:11 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:25:37 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 02:26:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:26:23 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 02:26:24 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 02:26:25 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 02:26:25 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 02:26:25 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 02:26:25 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 02:26:25 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 02:26:44 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 02:26:44 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:26:45 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 02:26:45 GMT
USER adminer
# Tue, 23 Jul 2024 02:26:45 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 23 Jul 2024 02:26:46 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:fb0b8650d20e29c53f770b72d16b7381f876f2a0053fff3e542a0cc3f0b944b9`  
		Last Modified: Tue, 23 Jul 2024 01:31:32 GMT  
		Size: 59.0 MB (58954687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15738e55b04d20078f3d22ceaa5ebfefad42e7e68c55159ba9f1c6c96104c70a`  
		Last Modified: Tue, 23 Jul 2024 02:27:47 GMT  
		Size: 40.9 MB (40945047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1abb9adf68c77ddb45b48d87fa048994b191b50bb3dcdb65c5a1441b09236be1`  
		Last Modified: Tue, 23 Jul 2024 02:27:38 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69537e8ef3c397be4c3c4bbae3f729010605989d0e55e2e34dec154b6236d385`  
		Last Modified: Tue, 23 Jul 2024 02:27:38 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d85520057f355d14f85487174847109082913ae6990ae521b6c4771322126556`  
		Last Modified: Tue, 23 Jul 2024 02:27:38 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49b987d3a64b41a1a379cbae62ba6a452c233dea35255c15a96f51b7b2f2540`  
		Last Modified: Tue, 23 Jul 2024 02:27:38 GMT  
		Size: 1.4 MB (1385236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094977f5661e09079e9461e6361d77eba3c6d34b09f6673b43866e7684c00646`  
		Last Modified: Tue, 23 Jul 2024 02:27:38 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-standalone` - linux; s390x

```console
$ docker pull adminer@sha256:c7bff6b618579c93f078953be91ea47360675dbdb7db286ac4c7c7b7a2c31701
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93739700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ee3166c88912b6a2804b5d2bd37d20f188044e94b6ccf08ac6b5df23de3359`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 23 Jul 2024 02:28:03 GMT
ADD file:67d4db619a1cada17f248642d89d5b55ab04b5dd6885587148dedeb665795154 in / 
# Tue, 23 Jul 2024 02:28:06 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:03:04 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 03:03:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:03:30 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 03:03:30 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 03:03:30 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 03:03:31 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 03:03:31 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 03:03:31 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 03:03:31 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 03:03:40 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 03:03:40 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 03:03:40 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 03:03:41 GMT
USER adminer
# Tue, 23 Jul 2024 03:03:41 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 23 Jul 2024 03:03:41 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:0d03391dea2fdd66bd2c594e41ac7575c5879176469a4d1e7301b8498f5e5351`  
		Last Modified: Tue, 23 Jul 2024 02:32:57 GMT  
		Size: 53.3 MB (53324092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f9b72e50d6e2068c7b209cae11aad4b881a45ca10624ddffa7d47ba3dc5258`  
		Last Modified: Tue, 23 Jul 2024 03:04:21 GMT  
		Size: 39.0 MB (39026243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dab3bcf36e0afe3d1e0873b7ab407e216ba4abd68b83db207492bfcb2d0e49c`  
		Last Modified: Tue, 23 Jul 2024 03:04:14 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4cc17406257aa75797eefdc9f711a2a0ef93e0e8a4aa6fab92d8af10d5c9ef6`  
		Last Modified: Tue, 23 Jul 2024 03:04:14 GMT  
		Size: 1.9 KB (1852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe14ae12a8ee2216ee37cf525b13545cadabdbeb782ce5a62b37414bdca70862`  
		Last Modified: Tue, 23 Jul 2024 03:04:14 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef800a2307cd151cb4f22631273389647cac3f39394e0a093c0517adde471b0`  
		Last Modified: Tue, 23 Jul 2024 03:04:14 GMT  
		Size: 1.4 MB (1385146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5161f60448626f1dd88239bdbbf9a186fa2c1a53279e72e50e5f00a2ae987ae`  
		Last Modified: Tue, 23 Jul 2024 03:04:14 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:fastcgi`

```console
$ docker pull adminer@sha256:cf3d7106f4d11d07a86fb2690a879e522d0561f8136b38a67fdc2bf4eba11c76
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
$ docker pull adminer@sha256:a65f9f3444eecf907fde215fd40219387c99f7d0927ad94fec2fad3d0c91df5c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95962913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b4a63db34258ca6af0f56fcd13e485f38764b0959c6119d1cbda4a1e920532`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:11 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Tue, 02 Jul 2024 01:25:12 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:48:36 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 04:48:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:48:58 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 02 Jul 2024 04:49:18 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 02 Jul 2024 04:49:19 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 04:49:19 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 04:49:19 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 04:49:19 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 04:49:19 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 04:49:19 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 04:49:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 04:49:30 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:49:30 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 04:49:30 GMT
USER adminer
# Tue, 02 Jul 2024 04:49:30 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c31c6689a3eaf2e6cb8a6fcc48fb54fc6190f9a34f8be35dff81a5705565a1`  
		Last Modified: Tue, 02 Jul 2024 04:49:50 GMT  
		Size: 39.5 MB (39489478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15098df20048ca7252eef0cee4b2b60f5b4cfe226b37aee2f86c8b8b49ed12da`  
		Last Modified: Tue, 02 Jul 2024 04:49:43 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7fc47a846479bc3911ccdaed2236fdb846714f9db30dd02d466e224cc5a895`  
		Last Modified: Tue, 02 Jul 2024 04:50:05 GMT  
		Size: 2.7 KB (2711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4d59e9486f131dfc50c56f5ee19dd29849461da1378eab3cb1ffbb7184023f3`  
		Last Modified: Tue, 02 Jul 2024 04:50:05 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f25810dba66fe09876afbcf9e8e39d8456c82613cfc63ac0a7f39738bc27c6`  
		Last Modified: Tue, 02 Jul 2024 04:50:05 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96bea11c7f0698a423d992a197aed5b28d6b8d11d745824720eab682f125c2a`  
		Last Modified: Tue, 02 Jul 2024 04:50:06 GMT  
		Size: 1.4 MB (1385158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d8ec6f28e566eaec9db9f59408e63b3d58c7595bca0c831fa9286ebca0f2e29`  
		Last Modified: Tue, 02 Jul 2024 04:50:05 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; arm variant v5

```console
$ docker pull adminer@sha256:28b821bf07d3288ef8624aba4e348e6c5df13a1c8de63390117bd668767bf873
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91228595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:774685cf6d16dadfa8b111a578dc98947b40415930473f195ea4f3178bbf702f`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Mon, 22 Jul 2024 23:57:12 GMT
ADD file:05c877f820dfe73bd5cecf959b857152065c40802cad0d9a46229bc0d5708339 in / 
# Mon, 22 Jul 2024 23:57:13 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 00:24:42 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 00:25:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 00:25:28 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 00:25:53 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 23 Jul 2024 00:25:54 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 00:25:54 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 00:25:54 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 00:25:54 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 00:25:55 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 00:25:55 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 00:26:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 00:26:10 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 00:26:10 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 00:26:10 GMT
USER adminer
# Tue, 23 Jul 2024 00:26:10 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:6faa199d3f09eecc4762c527abd2e9a5bc86f34a15c78145707b6b0b0ee526d5`  
		Last Modified: Tue, 23 Jul 2024 00:01:42 GMT  
		Size: 52.6 MB (52588961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea175fc25888492446b9545eb11532a36f0d62f3c448de0e72e72a2d4206256`  
		Last Modified: Tue, 23 Jul 2024 00:26:33 GMT  
		Size: 37.2 MB (37247611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aee3033b2b37548a5949367b960e0d3bb49c486d2b4911b024eadb15301d60f`  
		Last Modified: Tue, 23 Jul 2024 00:26:23 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2c14f7e1bfcd1615af505b8319319293cfc170c1feff406f0848d749207bb3`  
		Last Modified: Tue, 23 Jul 2024 00:26:48 GMT  
		Size: 2.7 KB (2715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d26206279c33af8163e48ff66f061c62670069788764b804f76ebdeb5c45be4`  
		Last Modified: Tue, 23 Jul 2024 00:26:48 GMT  
		Size: 1.8 KB (1842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36113ffa34469c443f81198f38fef456743291a808133ba71d7b4724e84a1544`  
		Last Modified: Tue, 23 Jul 2024 00:26:48 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2353bf2bc981df8102745bff3ef704ca29e64af6ac487352ed4123647aed2c26`  
		Last Modified: Tue, 23 Jul 2024 00:26:48 GMT  
		Size: 1.4 MB (1385100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7bc91ac0a2b45c59d8992cc845dfdf83f6876423d1f3a4f128fbf503c7f43b`  
		Last Modified: Tue, 23 Jul 2024 00:26:48 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:940499184855825584dffe9b581a4e3d892cda313e8ba1f06f4c0f184d5bc108
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87825032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04142ce31ca904ea987e19dc4b5162e4f1640898ef5b8e4ff2783137dfd80730`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:18 GMT
ADD file:45e512d8c89ef619a4db87ca11813c5b48e6332c4c281a9f0d4aaf7301e85990 in / 
# Tue, 23 Jul 2024 03:03:18 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:52:31 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 03:53:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:53:47 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 03:54:25 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 23 Jul 2024 03:54:27 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 03:54:27 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 03:54:28 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 03:54:28 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 03:54:29 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 03:54:29 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 03:54:50 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 03:54:50 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 03:54:51 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 03:54:51 GMT
USER adminer
# Tue, 23 Jul 2024 03:54:51 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:57c3fa3d04a48c55117bbc60f2775c978886b3bc89b70e48e85c0516ce060947`  
		Last Modified: Tue, 23 Jul 2024 03:07:14 GMT  
		Size: 50.2 MB (50242355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef802d5de026a32dc791f808ef890fca768eb6e270e042642cf443affacfb85`  
		Last Modified: Tue, 23 Jul 2024 03:55:16 GMT  
		Size: 36.2 MB (36190522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa89f6dcd7fec84e6bdff0fa8ed984aebc82e025446b8d87445c270036259aa9`  
		Last Modified: Tue, 23 Jul 2024 03:55:07 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f0ffae6b7a4e7300b5fcc49bdc2bc9b2ad8b6746611c7e99b291ab33fffb3a`  
		Last Modified: Tue, 23 Jul 2024 03:55:32 GMT  
		Size: 2.7 KB (2715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfddd9483e786ea5d31fb2009e0addd025d8cfa3cc664f3a52753091f01dbe0c`  
		Last Modified: Tue, 23 Jul 2024 03:55:32 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff45e2ad6c3b6e678cc25d6976ac0a3a174d46e13268c21d32e308693ec1831`  
		Last Modified: Tue, 23 Jul 2024 03:55:32 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a8c797535832a99c8d88455fe604811f0c45be3d9d29160b653ad03507acdf`  
		Last Modified: Tue, 23 Jul 2024 03:55:33 GMT  
		Size: 1.4 MB (1385237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e909ef8532fe9e3e6c08fb74bd399bce640eb766fc731570b45abdf9c646eb34`  
		Last Modified: Tue, 23 Jul 2024 03:55:33 GMT  
		Size: 493.0 B  
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
$ docker pull adminer@sha256:8b5a58dc254439c686e7e263f42168f58ed7a06c2af794b7d4d6a5827f0fd314
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92657102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b23cd2579b0ea5c2e2e6391da4fef0599634b6d8e1c0ae92ba67507153281f`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 23 Jul 2024 00:38:26 GMT
ADD file:3fbf62974aea46ff67427fd8996563bef3939ff51df600b4914acf5abb0b6c51 in / 
# Tue, 23 Jul 2024 00:38:32 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:12:17 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 02:14:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:14:15 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 02:16:05 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 23 Jul 2024 02:16:12 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 02:16:16 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 02:16:20 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 02:16:23 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 02:16:27 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 02:16:31 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 02:17:20 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 02:17:24 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:17:27 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 02:17:31 GMT
USER adminer
# Tue, 23 Jul 2024 02:17:35 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:6fba1199d77f2795fad97ca84f3d7030aab307e1ee7b582027c4e146bacdff14`  
		Last Modified: Tue, 23 Jul 2024 00:49:50 GMT  
		Size: 53.3 MB (53310598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb5ccc2e78cafd7a6bae2b97d6510ada07c2b60961937d42810594c7f3013c2`  
		Last Modified: Tue, 23 Jul 2024 02:18:19 GMT  
		Size: 38.0 MB (37953492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a7bda0b2932d324ef514eff7c5614353c086b9ea7ad4d853f8fd399c51b6d5`  
		Last Modified: Tue, 23 Jul 2024 02:17:52 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee2d26e1899d8a8b268f6ef6d98db730bc341ff6913ace137afde90c8f7ba6c`  
		Last Modified: Tue, 23 Jul 2024 02:18:41 GMT  
		Size: 2.7 KB (2713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76695ee7cfcc7aad4ed6cc2ce0a15b5e71207ab0ccae36294cdeac0cc71ddbf`  
		Last Modified: Tue, 23 Jul 2024 02:18:41 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee98dea0703c2f60a2e4bf777be8e50a609fbe5658ef913b93fddbb604d6e96a`  
		Last Modified: Tue, 23 Jul 2024 02:18:41 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e924f48a941a9836a5762905bb73e501a9c08ec789d9975f88590718f6c0ba`  
		Last Modified: Tue, 23 Jul 2024 02:18:43 GMT  
		Size: 1.4 MB (1386197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77965a700523588d06e3d8ab1c0586c82d83796fbe6949c87d3177d7dd97c701`  
		Last Modified: Tue, 23 Jul 2024 02:18:42 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:dee0c7bb9a7b5aaac331c29123d62662d900d6d1e0d1bf0becc95e9dc35d3599
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101291907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ea903255a4ffa78793f81ea18f5a4560af79838030fbf4c55516f80934f152`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 23 Jul 2024 01:27:09 GMT
ADD file:538282e20405c23ce510f30f714f80393534997f12fd1cc25a8d7752dc6f1360 in / 
# Tue, 23 Jul 2024 01:27:11 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:25:37 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 02:26:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:26:23 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 02:27:02 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 23 Jul 2024 02:27:04 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 02:27:04 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 02:27:04 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 02:27:05 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 02:27:05 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 02:27:05 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 02:27:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 02:27:24 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:27:24 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 02:27:24 GMT
USER adminer
# Tue, 23 Jul 2024 02:27:25 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:fb0b8650d20e29c53f770b72d16b7381f876f2a0053fff3e542a0cc3f0b944b9`  
		Last Modified: Tue, 23 Jul 2024 01:31:32 GMT  
		Size: 59.0 MB (58954687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15738e55b04d20078f3d22ceaa5ebfefad42e7e68c55159ba9f1c6c96104c70a`  
		Last Modified: Tue, 23 Jul 2024 02:27:47 GMT  
		Size: 40.9 MB (40945047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1abb9adf68c77ddb45b48d87fa048994b191b50bb3dcdb65c5a1441b09236be1`  
		Last Modified: Tue, 23 Jul 2024 02:27:38 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8cfaf311da16a0e82541813e3f196fbb549b8d3b4c5d00a0706e9bb113ab61`  
		Last Modified: Tue, 23 Jul 2024 02:28:03 GMT  
		Size: 2.7 KB (2712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97ca69cb806636211daf12ba75a96f6dcd060f44f8de9c8c01f4e7603ad16c4`  
		Last Modified: Tue, 23 Jul 2024 02:28:02 GMT  
		Size: 1.8 KB (1847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df0cb83b55519a88ad23c909874d20b54e854376a784207653c4be6f23c73ccc`  
		Last Modified: Tue, 23 Jul 2024 02:28:02 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7531a129bc98acb32209bb040ce99bb7d30fcb76dab8ded8ef5cd08a179854`  
		Last Modified: Tue, 23 Jul 2024 02:28:03 GMT  
		Size: 1.4 MB (1385246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d48a360d8a16035cc5528cd6bc0e45116f172e7c3d935c20ae81eb64111bc3`  
		Last Modified: Tue, 23 Jul 2024 02:28:02 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; s390x

```console
$ docker pull adminer@sha256:5b68c11e23080d7d4f5e745202d62cf73c411b3b6e45519dd1342175e8155e1f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93742391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c221ef6b6f73482a2313e8fe83b8667520970e85e5c41919dbbaa6e72524e1a8`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 23 Jul 2024 02:28:03 GMT
ADD file:67d4db619a1cada17f248642d89d5b55ab04b5dd6885587148dedeb665795154 in / 
# Tue, 23 Jul 2024 02:28:06 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:03:04 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 03:03:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:03:30 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 03:03:51 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 23 Jul 2024 03:03:51 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 03:03:51 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 03:03:51 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 03:03:52 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 03:03:52 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 03:03:52 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 03:04:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 03:04:00 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 03:04:00 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 03:04:00 GMT
USER adminer
# Tue, 23 Jul 2024 03:04:01 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:0d03391dea2fdd66bd2c594e41ac7575c5879176469a4d1e7301b8498f5e5351`  
		Last Modified: Tue, 23 Jul 2024 02:32:57 GMT  
		Size: 53.3 MB (53324092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f9b72e50d6e2068c7b209cae11aad4b881a45ca10624ddffa7d47ba3dc5258`  
		Last Modified: Tue, 23 Jul 2024 03:04:21 GMT  
		Size: 39.0 MB (39026243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dab3bcf36e0afe3d1e0873b7ab407e216ba4abd68b83db207492bfcb2d0e49c`  
		Last Modified: Tue, 23 Jul 2024 03:04:14 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fa842b8d20c971ec35b7b1fd365ebcf06eba7c327f8d3152c8fca17c0e7665`  
		Last Modified: Tue, 23 Jul 2024 03:04:31 GMT  
		Size: 2.7 KB (2709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29efb99675faf1ec4ca57f74dc079ff104548b494b6df8e1ab865f7d1835be99`  
		Last Modified: Tue, 23 Jul 2024 03:04:31 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:769d57125a6627215e8720ac3e31b9de7c9d1c2abc3423baecb12e25a1b5729d`  
		Last Modified: Tue, 23 Jul 2024 03:04:31 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f056b55ddb3c62ad27de0b76cafcb5d832cc6d481b3765f7bf3c372bd23890`  
		Last Modified: Tue, 23 Jul 2024 03:04:31 GMT  
		Size: 1.4 MB (1385141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9c5a5212a250c3a34617fd215b8dd86b707ceacbd89602ca27b62c14d9ad009`  
		Last Modified: Tue, 23 Jul 2024 03:04:31 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:latest`

```console
$ docker pull adminer@sha256:115edb007e0a41e3743a88599b37bd48b8637bb286ef159af4b26f748fc53492
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
$ docker pull adminer@sha256:c31c78818756bdbed9bdaa64dc19e7f7edd51813a8ef89d538f72ea052dca1f1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95960190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b234f0237cfe467ceb1991adc8e536c60e2307752a844117e3506273c3cc70`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:11 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Tue, 02 Jul 2024 01:25:12 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:48:36 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 04:48:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:48:58 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 02 Jul 2024 04:48:59 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 04:48:59 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 04:48:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 04:48:59 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 04:48:59 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 04:48:59 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 04:49:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 04:49:11 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:49:11 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 04:49:11 GMT
USER adminer
# Tue, 02 Jul 2024 04:49:11 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 02 Jul 2024 04:49:11 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c31c6689a3eaf2e6cb8a6fcc48fb54fc6190f9a34f8be35dff81a5705565a1`  
		Last Modified: Tue, 02 Jul 2024 04:49:50 GMT  
		Size: 39.5 MB (39489478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15098df20048ca7252eef0cee4b2b60f5b4cfe226b37aee2f86c8b8b49ed12da`  
		Last Modified: Tue, 02 Jul 2024 04:49:43 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa436138c493f6b280d90f878c5f42e49161c213e07c63239dba3035d53200f`  
		Last Modified: Tue, 02 Jul 2024 04:49:43 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301530bfa5f53b39e40c2a73ab2943a95bb28f04dbd763bb519c82228cdb6330`  
		Last Modified: Tue, 02 Jul 2024 04:49:43 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b7955944f85a8d66bb95cdfbe4839dc329677da60416ebb8c1d09fef5ec295`  
		Last Modified: Tue, 02 Jul 2024 04:49:43 GMT  
		Size: 1.4 MB (1385152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d923a48aa5d0fcde247f30d40164b9ad0d68d576e0c37c3c69eb83e2dab736e5`  
		Last Modified: Tue, 02 Jul 2024 04:49:43 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; arm variant v5

```console
$ docker pull adminer@sha256:0e52bfd1add93668146a0a1a5544187ee1dc9b4d9b0d7368ec3bd97f77037e9b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91225878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5fc5328a78544dcb2f0a078019b0bea7ab255b502c4eddbcbb0564c616436c`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Mon, 22 Jul 2024 23:57:12 GMT
ADD file:05c877f820dfe73bd5cecf959b857152065c40802cad0d9a46229bc0d5708339 in / 
# Mon, 22 Jul 2024 23:57:13 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 00:24:42 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 00:25:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 00:25:28 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 00:25:29 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 00:25:29 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 00:25:30 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 00:25:30 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 00:25:30 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 00:25:31 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 00:25:47 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 00:25:47 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 00:25:47 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 00:25:47 GMT
USER adminer
# Tue, 23 Jul 2024 00:25:47 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 23 Jul 2024 00:25:47 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:6faa199d3f09eecc4762c527abd2e9a5bc86f34a15c78145707b6b0b0ee526d5`  
		Last Modified: Tue, 23 Jul 2024 00:01:42 GMT  
		Size: 52.6 MB (52588961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea175fc25888492446b9545eb11532a36f0d62f3c448de0e72e72a2d4206256`  
		Last Modified: Tue, 23 Jul 2024 00:26:33 GMT  
		Size: 37.2 MB (37247611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aee3033b2b37548a5949367b960e0d3bb49c486d2b4911b024eadb15301d60f`  
		Last Modified: Tue, 23 Jul 2024 00:26:23 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc5b14232a5b77160d3deb0bbad3fab3c8aac724a97c519210b401938ee10a0`  
		Last Modified: Tue, 23 Jul 2024 00:26:23 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84cad97ff757120302d208a8b77f191afed2dc5624b7f563ca50c8894dac89f6`  
		Last Modified: Tue, 23 Jul 2024 00:26:23 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3600c4e5e44f075d5c68b7655b8084853942806b56b0ecd9baf6783a66197c`  
		Last Modified: Tue, 23 Jul 2024 00:26:23 GMT  
		Size: 1.4 MB (1385103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6851d528b265ea638bd0a586551d946177270672608fa4f8578c8420d0385cb9`  
		Last Modified: Tue, 23 Jul 2024 00:26:23 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; arm variant v7

```console
$ docker pull adminer@sha256:02c012a3b47cb2dc2761b06eed691093d9e166216c92df475cbc9f8eadc9e5c8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87822374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8844c2056e0d57feaca4f1be1253bd8f8f2715f937cd842d1ccbef6c2f7fb2`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:18 GMT
ADD file:45e512d8c89ef619a4db87ca11813c5b48e6332c4c281a9f0d4aaf7301e85990 in / 
# Tue, 23 Jul 2024 03:03:18 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:52:31 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 03:53:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:53:47 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 03:53:49 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 03:53:49 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 03:53:50 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 03:53:50 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 03:53:50 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 03:53:51 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 03:54:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 03:54:18 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 03:54:19 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 03:54:19 GMT
USER adminer
# Tue, 23 Jul 2024 03:54:19 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 23 Jul 2024 03:54:19 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:57c3fa3d04a48c55117bbc60f2775c978886b3bc89b70e48e85c0516ce060947`  
		Last Modified: Tue, 23 Jul 2024 03:07:14 GMT  
		Size: 50.2 MB (50242355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef802d5de026a32dc791f808ef890fca768eb6e270e042642cf443affacfb85`  
		Last Modified: Tue, 23 Jul 2024 03:55:16 GMT  
		Size: 36.2 MB (36190522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa89f6dcd7fec84e6bdff0fa8ed984aebc82e025446b8d87445c270036259aa9`  
		Last Modified: Tue, 23 Jul 2024 03:55:07 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d6bc010107086de83c02e3740522ab10058840d9382aba4debea6502e49e1c`  
		Last Modified: Tue, 23 Jul 2024 03:55:07 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a76f8c1f42f47a8f9dc9bcdd1e024abe9951e9b58f03990d325c34484b042d`  
		Last Modified: Tue, 23 Jul 2024 03:55:07 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4fde1c1ed80b1b4ca7d8802b96bd546050fd8e0b862c6cd2f25f5b27655747`  
		Last Modified: Tue, 23 Jul 2024 03:55:07 GMT  
		Size: 1.4 MB (1385292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d19e9266c2d80bfe86943cee6ac09b905d99cba1d9b5c0b1b1b444eac73acfd`  
		Last Modified: Tue, 23 Jul 2024 03:55:07 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:b03c33368be4bba59f14aaf0cded44fcdc50e355c9bfa19cc3c44d106c4713e0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94358345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299c22d3acc4de54d764bad9b1076848198e8e46a67fc4245d04908c6f28e6dd`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Tue, 02 Jul 2024 03:49:31 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 03:49:31 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 03:49:31 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 03:49:31 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 03:49:31 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 03:49:31 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 03:49:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 03:49:41 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:49:41 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 03:49:41 GMT
USER adminer
# Tue, 02 Jul 2024 03:49:41 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 02 Jul 2024 03:49:42 GMT
EXPOSE 8080
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
	-	`sha256:ca7a060c53754e1f602d8bcd48248ebf6552078b1b5399f1e2bc003e28df66a3`  
		Last Modified: Tue, 02 Jul 2024 03:50:04 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fbd5efe441c2e90738651736224a0fe724fd712995f15c157b715b38b9b9b6`  
		Last Modified: Tue, 02 Jul 2024 03:50:04 GMT  
		Size: 1.5 KB (1483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee7687bec909e9911339ab8fc15c7213b444003fd7dbaa0628eea3d211c7834`  
		Last Modified: Tue, 02 Jul 2024 03:50:05 GMT  
		Size: 1.4 MB (1385094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acee67427be79e892393ce058a4d79428ae50d525217d0cceb4b31ad4c46f482`  
		Last Modified: Tue, 02 Jul 2024 03:50:04 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; 386

```console
$ docker pull adminer@sha256:2d74c7eb07a906d8e576f9e2c9971bdb01ab19aeba06478a94a9c273fa0992b6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (97013341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a850c42c8891f85474d75f6a74938ec55e1bad5d98e957cf59b54e8d6261e7`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Tue, 02 Jul 2024 01:40:38 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 01:40:38 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 01:40:38 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 01:40:38 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 01:40:38 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 01:40:38 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 01:40:50 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 01:40:50 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:40:50 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 01:40:51 GMT
USER adminer
# Tue, 02 Jul 2024 01:40:51 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 02 Jul 2024 01:40:51 GMT
EXPOSE 8080
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
	-	`sha256:8ae625b5731fddecf9b61034a28aedc8d9401e752eb6a7d261521555c3481791`  
		Last Modified: Tue, 02 Jul 2024 01:41:24 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a56bc1ddfe4d69136cc994627bbfeff96048814e1f5025b955be353df22753`  
		Last Modified: Tue, 02 Jul 2024 01:41:24 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6972d1f06dce91eb6060a692e744bf4b0e73bdbcebc740ab73f7249763c59101`  
		Last Modified: Tue, 02 Jul 2024 01:41:24 GMT  
		Size: 1.4 MB (1385010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b50df8e2047966f9043744696cacdc3a5735a5400851144fffc0f0d740dc1e`  
		Last Modified: Tue, 02 Jul 2024 01:41:24 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; mips64le

```console
$ docker pull adminer@sha256:8a01711066df85ed070620061fdd9e1631a1046badc61606c1e6ec8bdc01ec26
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92654371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43da756743e71ac148d7b882a8eb215791392ae2b763de8095c051a6cff1980d`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 23 Jul 2024 00:38:26 GMT
ADD file:3fbf62974aea46ff67427fd8996563bef3939ff51df600b4914acf5abb0b6c51 in / 
# Tue, 23 Jul 2024 00:38:32 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:12:17 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 02:14:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:14:15 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 02:14:23 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 02:14:26 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 02:14:30 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 02:14:34 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 02:14:37 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 02:14:41 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 02:15:33 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 02:15:36 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:15:40 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 02:15:44 GMT
USER adminer
# Tue, 23 Jul 2024 02:15:48 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 23 Jul 2024 02:15:51 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:6fba1199d77f2795fad97ca84f3d7030aab307e1ee7b582027c4e146bacdff14`  
		Last Modified: Tue, 23 Jul 2024 00:49:50 GMT  
		Size: 53.3 MB (53310598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb5ccc2e78cafd7a6bae2b97d6510ada07c2b60961937d42810594c7f3013c2`  
		Last Modified: Tue, 23 Jul 2024 02:18:19 GMT  
		Size: 38.0 MB (37953492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a7bda0b2932d324ef514eff7c5614353c086b9ea7ad4d853f8fd399c51b6d5`  
		Last Modified: Tue, 23 Jul 2024 02:17:52 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20433faf9234936c4ea8be2f288e5c392849bf726237f53f1ba83f71ada2288f`  
		Last Modified: Tue, 23 Jul 2024 02:17:52 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6157345705446634090f1dd03196240215199992409caa373077fa87e33a034a`  
		Last Modified: Tue, 23 Jul 2024 02:17:52 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537f5ec680d68403883c13e21ec08015d0e3df367b0efbd3b21f9461e43c9bd2`  
		Last Modified: Tue, 23 Jul 2024 02:17:53 GMT  
		Size: 1.4 MB (1386185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61a03247e49e3d869b1ec2b1062fd0cb20c2c04614d1964690602a169b6733e`  
		Last Modified: Tue, 23 Jul 2024 02:17:52 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; ppc64le

```console
$ docker pull adminer@sha256:062d939387a558e07d69afde16e368e2fc7adc2e0c43700f46a6c448b8251ce3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101289185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0410f06417580c33e565abde408c17dfeed554975d02709ad62c95208b3ddace`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 23 Jul 2024 01:27:09 GMT
ADD file:538282e20405c23ce510f30f714f80393534997f12fd1cc25a8d7752dc6f1360 in / 
# Tue, 23 Jul 2024 01:27:11 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:25:37 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 02:26:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:26:23 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 02:26:24 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 02:26:25 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 02:26:25 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 02:26:25 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 02:26:25 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 02:26:25 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 02:26:44 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 02:26:44 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:26:45 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 02:26:45 GMT
USER adminer
# Tue, 23 Jul 2024 02:26:45 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 23 Jul 2024 02:26:46 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:fb0b8650d20e29c53f770b72d16b7381f876f2a0053fff3e542a0cc3f0b944b9`  
		Last Modified: Tue, 23 Jul 2024 01:31:32 GMT  
		Size: 59.0 MB (58954687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15738e55b04d20078f3d22ceaa5ebfefad42e7e68c55159ba9f1c6c96104c70a`  
		Last Modified: Tue, 23 Jul 2024 02:27:47 GMT  
		Size: 40.9 MB (40945047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1abb9adf68c77ddb45b48d87fa048994b191b50bb3dcdb65c5a1441b09236be1`  
		Last Modified: Tue, 23 Jul 2024 02:27:38 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69537e8ef3c397be4c3c4bbae3f729010605989d0e55e2e34dec154b6236d385`  
		Last Modified: Tue, 23 Jul 2024 02:27:38 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d85520057f355d14f85487174847109082913ae6990ae521b6c4771322126556`  
		Last Modified: Tue, 23 Jul 2024 02:27:38 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49b987d3a64b41a1a379cbae62ba6a452c233dea35255c15a96f51b7b2f2540`  
		Last Modified: Tue, 23 Jul 2024 02:27:38 GMT  
		Size: 1.4 MB (1385236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094977f5661e09079e9461e6361d77eba3c6d34b09f6673b43866e7684c00646`  
		Last Modified: Tue, 23 Jul 2024 02:27:38 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; s390x

```console
$ docker pull adminer@sha256:c7bff6b618579c93f078953be91ea47360675dbdb7db286ac4c7c7b7a2c31701
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93739700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ee3166c88912b6a2804b5d2bd37d20f188044e94b6ccf08ac6b5df23de3359`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 23 Jul 2024 02:28:03 GMT
ADD file:67d4db619a1cada17f248642d89d5b55ab04b5dd6885587148dedeb665795154 in / 
# Tue, 23 Jul 2024 02:28:06 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:03:04 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 03:03:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:03:30 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 03:03:30 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 03:03:30 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 03:03:31 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 03:03:31 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 03:03:31 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 03:03:31 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 03:03:40 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 03:03:40 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 03:03:40 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 03:03:41 GMT
USER adminer
# Tue, 23 Jul 2024 03:03:41 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 23 Jul 2024 03:03:41 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:0d03391dea2fdd66bd2c594e41ac7575c5879176469a4d1e7301b8498f5e5351`  
		Last Modified: Tue, 23 Jul 2024 02:32:57 GMT  
		Size: 53.3 MB (53324092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f9b72e50d6e2068c7b209cae11aad4b881a45ca10624ddffa7d47ba3dc5258`  
		Last Modified: Tue, 23 Jul 2024 03:04:21 GMT  
		Size: 39.0 MB (39026243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dab3bcf36e0afe3d1e0873b7ab407e216ba4abd68b83db207492bfcb2d0e49c`  
		Last Modified: Tue, 23 Jul 2024 03:04:14 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4cc17406257aa75797eefdc9f711a2a0ef93e0e8a4aa6fab92d8af10d5c9ef6`  
		Last Modified: Tue, 23 Jul 2024 03:04:14 GMT  
		Size: 1.9 KB (1852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe14ae12a8ee2216ee37cf525b13545cadabdbeb782ce5a62b37414bdca70862`  
		Last Modified: Tue, 23 Jul 2024 03:04:14 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef800a2307cd151cb4f22631273389647cac3f39394e0a093c0517adde471b0`  
		Last Modified: Tue, 23 Jul 2024 03:04:14 GMT  
		Size: 1.4 MB (1385146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5161f60448626f1dd88239bdbbf9a186fa2c1a53279e72e50e5f00a2ae987ae`  
		Last Modified: Tue, 23 Jul 2024 03:04:14 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:standalone`

```console
$ docker pull adminer@sha256:115edb007e0a41e3743a88599b37bd48b8637bb286ef159af4b26f748fc53492
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
$ docker pull adminer@sha256:c31c78818756bdbed9bdaa64dc19e7f7edd51813a8ef89d538f72ea052dca1f1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95960190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b234f0237cfe467ceb1991adc8e536c60e2307752a844117e3506273c3cc70`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:11 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Tue, 02 Jul 2024 01:25:12 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:48:36 GMT
STOPSIGNAL SIGINT
# Tue, 02 Jul 2024 04:48:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 04:48:58 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 02 Jul 2024 04:48:59 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 04:48:59 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 04:48:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 04:48:59 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 04:48:59 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 04:48:59 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 04:49:11 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 04:49:11 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:49:11 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 04:49:11 GMT
USER adminer
# Tue, 02 Jul 2024 04:49:11 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 02 Jul 2024 04:49:11 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4c31c6689a3eaf2e6cb8a6fcc48fb54fc6190f9a34f8be35dff81a5705565a1`  
		Last Modified: Tue, 02 Jul 2024 04:49:50 GMT  
		Size: 39.5 MB (39489478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15098df20048ca7252eef0cee4b2b60f5b4cfe226b37aee2f86c8b8b49ed12da`  
		Last Modified: Tue, 02 Jul 2024 04:49:43 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa436138c493f6b280d90f878c5f42e49161c213e07c63239dba3035d53200f`  
		Last Modified: Tue, 02 Jul 2024 04:49:43 GMT  
		Size: 1.8 KB (1843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301530bfa5f53b39e40c2a73ab2943a95bb28f04dbd763bb519c82228cdb6330`  
		Last Modified: Tue, 02 Jul 2024 04:49:43 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b7955944f85a8d66bb95cdfbe4839dc329677da60416ebb8c1d09fef5ec295`  
		Last Modified: Tue, 02 Jul 2024 04:49:43 GMT  
		Size: 1.4 MB (1385152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d923a48aa5d0fcde247f30d40164b9ad0d68d576e0c37c3c69eb83e2dab736e5`  
		Last Modified: Tue, 02 Jul 2024 04:49:43 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; arm variant v5

```console
$ docker pull adminer@sha256:0e52bfd1add93668146a0a1a5544187ee1dc9b4d9b0d7368ec3bd97f77037e9b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91225878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5fc5328a78544dcb2f0a078019b0bea7ab255b502c4eddbcbb0564c616436c`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Mon, 22 Jul 2024 23:57:12 GMT
ADD file:05c877f820dfe73bd5cecf959b857152065c40802cad0d9a46229bc0d5708339 in / 
# Mon, 22 Jul 2024 23:57:13 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 00:24:42 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 00:25:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 00:25:28 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 00:25:29 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 00:25:29 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 00:25:30 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 00:25:30 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 00:25:30 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 00:25:31 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 00:25:47 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 00:25:47 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 00:25:47 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 00:25:47 GMT
USER adminer
# Tue, 23 Jul 2024 00:25:47 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 23 Jul 2024 00:25:47 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:6faa199d3f09eecc4762c527abd2e9a5bc86f34a15c78145707b6b0b0ee526d5`  
		Last Modified: Tue, 23 Jul 2024 00:01:42 GMT  
		Size: 52.6 MB (52588961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea175fc25888492446b9545eb11532a36f0d62f3c448de0e72e72a2d4206256`  
		Last Modified: Tue, 23 Jul 2024 00:26:33 GMT  
		Size: 37.2 MB (37247611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aee3033b2b37548a5949367b960e0d3bb49c486d2b4911b024eadb15301d60f`  
		Last Modified: Tue, 23 Jul 2024 00:26:23 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acc5b14232a5b77160d3deb0bbad3fab3c8aac724a97c519210b401938ee10a0`  
		Last Modified: Tue, 23 Jul 2024 00:26:23 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84cad97ff757120302d208a8b77f191afed2dc5624b7f563ca50c8894dac89f6`  
		Last Modified: Tue, 23 Jul 2024 00:26:23 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb3600c4e5e44f075d5c68b7655b8084853942806b56b0ecd9baf6783a66197c`  
		Last Modified: Tue, 23 Jul 2024 00:26:23 GMT  
		Size: 1.4 MB (1385103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6851d528b265ea638bd0a586551d946177270672608fa4f8578c8420d0385cb9`  
		Last Modified: Tue, 23 Jul 2024 00:26:23 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:02c012a3b47cb2dc2761b06eed691093d9e166216c92df475cbc9f8eadc9e5c8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87822374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8844c2056e0d57feaca4f1be1253bd8f8f2715f937cd842d1ccbef6c2f7fb2`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:18 GMT
ADD file:45e512d8c89ef619a4db87ca11813c5b48e6332c4c281a9f0d4aaf7301e85990 in / 
# Tue, 23 Jul 2024 03:03:18 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:52:31 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 03:53:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:53:47 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 03:53:49 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 03:53:49 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 03:53:50 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 03:53:50 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 03:53:50 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 03:53:51 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 03:54:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 03:54:18 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 03:54:19 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 03:54:19 GMT
USER adminer
# Tue, 23 Jul 2024 03:54:19 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 23 Jul 2024 03:54:19 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:57c3fa3d04a48c55117bbc60f2775c978886b3bc89b70e48e85c0516ce060947`  
		Last Modified: Tue, 23 Jul 2024 03:07:14 GMT  
		Size: 50.2 MB (50242355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef802d5de026a32dc791f808ef890fca768eb6e270e042642cf443affacfb85`  
		Last Modified: Tue, 23 Jul 2024 03:55:16 GMT  
		Size: 36.2 MB (36190522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa89f6dcd7fec84e6bdff0fa8ed984aebc82e025446b8d87445c270036259aa9`  
		Last Modified: Tue, 23 Jul 2024 03:55:07 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d6bc010107086de83c02e3740522ab10058840d9382aba4debea6502e49e1c`  
		Last Modified: Tue, 23 Jul 2024 03:55:07 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a76f8c1f42f47a8f9dc9bcdd1e024abe9951e9b58f03990d325c34484b042d`  
		Last Modified: Tue, 23 Jul 2024 03:55:07 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4fde1c1ed80b1b4ca7d8802b96bd546050fd8e0b862c6cd2f25f5b27655747`  
		Last Modified: Tue, 23 Jul 2024 03:55:07 GMT  
		Size: 1.4 MB (1385292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d19e9266c2d80bfe86943cee6ac09b905d99cba1d9b5c0b1b1b444eac73acfd`  
		Last Modified: Tue, 23 Jul 2024 03:55:07 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:b03c33368be4bba59f14aaf0cded44fcdc50e355c9bfa19cc3c44d106c4713e0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94358345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299c22d3acc4de54d764bad9b1076848198e8e46a67fc4245d04908c6f28e6dd`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Tue, 02 Jul 2024 03:49:31 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 03:49:31 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 03:49:31 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 03:49:31 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 03:49:31 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 03:49:31 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 03:49:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 03:49:41 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 03:49:41 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 03:49:41 GMT
USER adminer
# Tue, 02 Jul 2024 03:49:41 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 02 Jul 2024 03:49:42 GMT
EXPOSE 8080
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
	-	`sha256:ca7a060c53754e1f602d8bcd48248ebf6552078b1b5399f1e2bc003e28df66a3`  
		Last Modified: Tue, 02 Jul 2024 03:50:04 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08fbd5efe441c2e90738651736224a0fe724fd712995f15c157b715b38b9b9b6`  
		Last Modified: Tue, 02 Jul 2024 03:50:04 GMT  
		Size: 1.5 KB (1483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee7687bec909e9911339ab8fc15c7213b444003fd7dbaa0628eea3d211c7834`  
		Last Modified: Tue, 02 Jul 2024 03:50:05 GMT  
		Size: 1.4 MB (1385094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acee67427be79e892393ce058a4d79428ae50d525217d0cceb4b31ad4c46f482`  
		Last Modified: Tue, 02 Jul 2024 03:50:04 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; 386

```console
$ docker pull adminer@sha256:2d74c7eb07a906d8e576f9e2c9971bdb01ab19aeba06478a94a9c273fa0992b6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (97013341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a850c42c8891f85474d75f6a74938ec55e1bad5d98e957cf59b54e8d6261e7`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Tue, 02 Jul 2024 01:40:38 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 01:40:38 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 01:40:38 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 01:40:38 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 01:40:38 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 01:40:38 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 01:40:50 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 01:40:50 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:40:50 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 01:40:51 GMT
USER adminer
# Tue, 02 Jul 2024 01:40:51 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 02 Jul 2024 01:40:51 GMT
EXPOSE 8080
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
	-	`sha256:8ae625b5731fddecf9b61034a28aedc8d9401e752eb6a7d261521555c3481791`  
		Last Modified: Tue, 02 Jul 2024 01:41:24 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a56bc1ddfe4d69136cc994627bbfeff96048814e1f5025b955be353df22753`  
		Last Modified: Tue, 02 Jul 2024 01:41:24 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6972d1f06dce91eb6060a692e744bf4b0e73bdbcebc740ab73f7249763c59101`  
		Last Modified: Tue, 02 Jul 2024 01:41:24 GMT  
		Size: 1.4 MB (1385010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b50df8e2047966f9043744696cacdc3a5735a5400851144fffc0f0d740dc1e`  
		Last Modified: Tue, 02 Jul 2024 01:41:24 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; mips64le

```console
$ docker pull adminer@sha256:8a01711066df85ed070620061fdd9e1631a1046badc61606c1e6ec8bdc01ec26
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92654371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43da756743e71ac148d7b882a8eb215791392ae2b763de8095c051a6cff1980d`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 23 Jul 2024 00:38:26 GMT
ADD file:3fbf62974aea46ff67427fd8996563bef3939ff51df600b4914acf5abb0b6c51 in / 
# Tue, 23 Jul 2024 00:38:32 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:12:17 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 02:14:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:14:15 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 02:14:23 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 02:14:26 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 02:14:30 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 02:14:34 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 02:14:37 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 02:14:41 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 02:15:33 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 02:15:36 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:15:40 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 02:15:44 GMT
USER adminer
# Tue, 23 Jul 2024 02:15:48 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 23 Jul 2024 02:15:51 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:6fba1199d77f2795fad97ca84f3d7030aab307e1ee7b582027c4e146bacdff14`  
		Last Modified: Tue, 23 Jul 2024 00:49:50 GMT  
		Size: 53.3 MB (53310598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb5ccc2e78cafd7a6bae2b97d6510ada07c2b60961937d42810594c7f3013c2`  
		Last Modified: Tue, 23 Jul 2024 02:18:19 GMT  
		Size: 38.0 MB (37953492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a7bda0b2932d324ef514eff7c5614353c086b9ea7ad4d853f8fd399c51b6d5`  
		Last Modified: Tue, 23 Jul 2024 02:17:52 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20433faf9234936c4ea8be2f288e5c392849bf726237f53f1ba83f71ada2288f`  
		Last Modified: Tue, 23 Jul 2024 02:17:52 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6157345705446634090f1dd03196240215199992409caa373077fa87e33a034a`  
		Last Modified: Tue, 23 Jul 2024 02:17:52 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537f5ec680d68403883c13e21ec08015d0e3df367b0efbd3b21f9461e43c9bd2`  
		Last Modified: Tue, 23 Jul 2024 02:17:53 GMT  
		Size: 1.4 MB (1386185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61a03247e49e3d869b1ec2b1062fd0cb20c2c04614d1964690602a169b6733e`  
		Last Modified: Tue, 23 Jul 2024 02:17:52 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:062d939387a558e07d69afde16e368e2fc7adc2e0c43700f46a6c448b8251ce3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101289185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0410f06417580c33e565abde408c17dfeed554975d02709ad62c95208b3ddace`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 23 Jul 2024 01:27:09 GMT
ADD file:538282e20405c23ce510f30f714f80393534997f12fd1cc25a8d7752dc6f1360 in / 
# Tue, 23 Jul 2024 01:27:11 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:25:37 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 02:26:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 02:26:23 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 02:26:24 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 02:26:25 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 02:26:25 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 02:26:25 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 02:26:25 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 02:26:25 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 02:26:44 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 02:26:44 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:26:45 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 02:26:45 GMT
USER adminer
# Tue, 23 Jul 2024 02:26:45 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 23 Jul 2024 02:26:46 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:fb0b8650d20e29c53f770b72d16b7381f876f2a0053fff3e542a0cc3f0b944b9`  
		Last Modified: Tue, 23 Jul 2024 01:31:32 GMT  
		Size: 59.0 MB (58954687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15738e55b04d20078f3d22ceaa5ebfefad42e7e68c55159ba9f1c6c96104c70a`  
		Last Modified: Tue, 23 Jul 2024 02:27:47 GMT  
		Size: 40.9 MB (40945047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1abb9adf68c77ddb45b48d87fa048994b191b50bb3dcdb65c5a1441b09236be1`  
		Last Modified: Tue, 23 Jul 2024 02:27:38 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69537e8ef3c397be4c3c4bbae3f729010605989d0e55e2e34dec154b6236d385`  
		Last Modified: Tue, 23 Jul 2024 02:27:38 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d85520057f355d14f85487174847109082913ae6990ae521b6c4771322126556`  
		Last Modified: Tue, 23 Jul 2024 02:27:38 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a49b987d3a64b41a1a379cbae62ba6a452c233dea35255c15a96f51b7b2f2540`  
		Last Modified: Tue, 23 Jul 2024 02:27:38 GMT  
		Size: 1.4 MB (1385236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094977f5661e09079e9461e6361d77eba3c6d34b09f6673b43866e7684c00646`  
		Last Modified: Tue, 23 Jul 2024 02:27:38 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; s390x

```console
$ docker pull adminer@sha256:c7bff6b618579c93f078953be91ea47360675dbdb7db286ac4c7c7b7a2c31701
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93739700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ee3166c88912b6a2804b5d2bd37d20f188044e94b6ccf08ac6b5df23de3359`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 23 Jul 2024 02:28:03 GMT
ADD file:67d4db619a1cada17f248642d89d5b55ab04b5dd6885587148dedeb665795154 in / 
# Tue, 23 Jul 2024 02:28:06 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:03:04 GMT
STOPSIGNAL SIGINT
# Tue, 23 Jul 2024 03:03:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:03:30 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 23 Jul 2024 03:03:30 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 23 Jul 2024 03:03:30 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 03:03:31 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 23 Jul 2024 03:03:31 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 23 Jul 2024 03:03:31 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 23 Jul 2024 03:03:31 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 23 Jul 2024 03:03:40 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 23 Jul 2024 03:03:40 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 23 Jul 2024 03:03:40 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 23 Jul 2024 03:03:41 GMT
USER adminer
# Tue, 23 Jul 2024 03:03:41 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 23 Jul 2024 03:03:41 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:0d03391dea2fdd66bd2c594e41ac7575c5879176469a4d1e7301b8498f5e5351`  
		Last Modified: Tue, 23 Jul 2024 02:32:57 GMT  
		Size: 53.3 MB (53324092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3f9b72e50d6e2068c7b209cae11aad4b881a45ca10624ddffa7d47ba3dc5258`  
		Last Modified: Tue, 23 Jul 2024 03:04:21 GMT  
		Size: 39.0 MB (39026243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dab3bcf36e0afe3d1e0873b7ab407e216ba4abd68b83db207492bfcb2d0e49c`  
		Last Modified: Tue, 23 Jul 2024 03:04:14 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4cc17406257aa75797eefdc9f711a2a0ef93e0e8a4aa6fab92d8af10d5c9ef6`  
		Last Modified: Tue, 23 Jul 2024 03:04:14 GMT  
		Size: 1.9 KB (1852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe14ae12a8ee2216ee37cf525b13545cadabdbeb782ce5a62b37414bdca70862`  
		Last Modified: Tue, 23 Jul 2024 03:04:14 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef800a2307cd151cb4f22631273389647cac3f39394e0a093c0517adde471b0`  
		Last Modified: Tue, 23 Jul 2024 03:04:14 GMT  
		Size: 1.4 MB (1385146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5161f60448626f1dd88239bdbbf9a186fa2c1a53279e72e50e5f00a2ae987ae`  
		Last Modified: Tue, 23 Jul 2024 03:04:14 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
