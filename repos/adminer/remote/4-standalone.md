## `adminer:4-standalone`

```console
$ docker pull adminer@sha256:ee90fd19757e0f89bb991f63bf04fd0530a0f98f408605d2b88f812fc0c3ec7b
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
$ docker pull adminer@sha256:7f067e709784fdeff58c0c9886e9e47aacb068752df545f24e55af4f1839de53
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95980607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c59cbdd3c9210d0e6596a8dc12d83cbfbeabc19e361ed137c370af126e1527c5`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Thu, 13 Jun 2024 03:38:06 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 13 Jun 2024 03:38:06 GMT
WORKDIR /var/www/html
# Thu, 13 Jun 2024 03:38:06 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 13 Jun 2024 03:38:06 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 13 Jun 2024 03:38:06 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 13 Jun 2024 03:38:07 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 13 Jun 2024 03:38:19 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 13 Jun 2024 03:38:19 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 13 Jun 2024 03:38:19 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 13 Jun 2024 03:38:19 GMT
USER adminer
# Thu, 13 Jun 2024 03:38:19 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 13 Jun 2024 03:38:19 GMT
EXPOSE 8080
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
	-	`sha256:ccfd0fbe2da46323aa23751c09a6a05c37fa9deb93f18a95821ab45336f19d23`  
		Last Modified: Thu, 13 Jun 2024 03:38:49 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e266a26993fdb22c531e801f3e5b2be0b11ea27cab3b87eab81ed5b9f4e0b802`  
		Last Modified: Thu, 13 Jun 2024 03:38:49 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbaef99f8f4d609751ab5b104c11512eab045fc67e25333e23458f9a03c26423`  
		Last Modified: Thu, 13 Jun 2024 03:38:49 GMT  
		Size: 1.4 MB (1386161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05056e60dfdd1633793a4651155b93cd33b46febe6bd50a1c09d6c112615d0bf`  
		Last Modified: Thu, 13 Jun 2024 03:38:49 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; arm variant v5

```console
$ docker pull adminer@sha256:00a7b2c760d87447cd3d4a7766bdef3e3389bd7cf6cbfc684b38a6f17d60c785
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91242056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aadfb3c72638b401b531e02d8dad69a9483412a6d133f7e324be7b1498bb17d`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 13 Jun 2024 00:48:40 GMT
ADD file:e9d8f0f7fb10978e8599b4d65173747a249b36470beb002a75b03faf3b15e953 in / 
# Thu, 13 Jun 2024 00:48:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:11:07 GMT
STOPSIGNAL SIGINT
# Thu, 13 Jun 2024 01:11:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:11:43 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 13 Jun 2024 01:11:43 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 13 Jun 2024 01:11:43 GMT
WORKDIR /var/www/html
# Thu, 13 Jun 2024 01:11:43 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 13 Jun 2024 01:11:44 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 13 Jun 2024 01:11:44 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 13 Jun 2024 01:11:44 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 13 Jun 2024 01:11:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 13 Jun 2024 01:11:59 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 13 Jun 2024 01:11:59 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 13 Jun 2024 01:11:59 GMT
USER adminer
# Thu, 13 Jun 2024 01:12:00 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 13 Jun 2024 01:12:00 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:257495c53b4c673d8b6401bad898f12d6b9f0119d3414c2dbb1f82162a4269c8`  
		Last Modified: Thu, 13 Jun 2024 00:51:58 GMT  
		Size: 52.6 MB (52603036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:689967f66d3f8016bce3f4173a49aaab862f325c01f55139218c6aabfac7cf04`  
		Last Modified: Thu, 13 Jun 2024 01:12:39 GMT  
		Size: 37.2 MB (37248748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3774d0f4bfc05d551da83bf11e640dd669b15560cd690d0001aa36548a6bd9`  
		Last Modified: Thu, 13 Jun 2024 01:12:31 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373cc7b5f3d0931241f4b4ada1741c65dd6139ccc35edcfba51960cb3cefd888`  
		Last Modified: Thu, 13 Jun 2024 01:12:31 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706250013f48f399131152ac9286072b5f227f42d1f630673b0e0fc63b478dc9`  
		Last Modified: Thu, 13 Jun 2024 01:12:31 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0815177ca3e803f1239440f5ee9ceeacc09405dffda14c6c9b8a0b681c4c3c9`  
		Last Modified: Thu, 13 Jun 2024 01:12:31 GMT  
		Size: 1.4 MB (1386067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7509669f96db51a8bbd798651c97a5958ed9561350dc1c48b99f15a83530ce4b`  
		Last Modified: Thu, 13 Jun 2024 01:12:31 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:46119c4be664e74c1f09c55fe415a9e524221533ca761933a07cc2eb9e3b5ec2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87838285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39711daf6117e5104aff429f7a80f53e53851aae332901a633f67ab312346b98`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 13 Jun 2024 00:57:50 GMT
ADD file:4993add96e8cc180b89e1b978fddc0b0876a303bce87dc08120edbe9513432bd in / 
# Thu, 13 Jun 2024 00:57:51 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:38:54 GMT
STOPSIGNAL SIGINT
# Thu, 13 Jun 2024 01:39:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:39:16 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 13 Jun 2024 01:39:17 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 13 Jun 2024 01:39:17 GMT
WORKDIR /var/www/html
# Thu, 13 Jun 2024 01:39:17 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 13 Jun 2024 01:39:17 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 13 Jun 2024 01:39:18 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 13 Jun 2024 01:39:18 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 13 Jun 2024 01:39:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 13 Jun 2024 01:39:29 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 13 Jun 2024 01:39:29 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 13 Jun 2024 01:39:29 GMT
USER adminer
# Thu, 13 Jun 2024 01:39:29 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 13 Jun 2024 01:39:29 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:45c5e98886f73bd45565e271bba1de66ffee1cfe17345d38a8e7179841133d4f`  
		Last Modified: Thu, 13 Jun 2024 01:01:59 GMT  
		Size: 50.3 MB (50256430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be7c03abe451662cecaafba0d9ea9cffb28db6c77f4bb54a74b8aeb6e3b8a574`  
		Last Modified: Thu, 13 Jun 2024 01:40:07 GMT  
		Size: 36.2 MB (36191617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45819ae15eef2635fc226357752114fd5a834892c8a18de4f632114326049de`  
		Last Modified: Thu, 13 Jun 2024 01:39:58 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a65eb0a51a6a255173d079b1dcc3636bcb9b0118ff1d3f18cf015668e1f7348`  
		Last Modified: Thu, 13 Jun 2024 01:39:58 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c10d9d59d6cd31dbad33467b7e7fc0a780dd45671a39cc0527bdcdcef1682df`  
		Last Modified: Thu, 13 Jun 2024 01:39:58 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a39503cd34eca96b40ee44af9311a70f5b3f6b112e6792729451518b8696ea`  
		Last Modified: Thu, 13 Jun 2024 01:39:58 GMT  
		Size: 1.4 MB (1386035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382a92b507c0d10702bbd43a3f2e37f5d8ebc76ee182a7f08bb6c6533a6733d3`  
		Last Modified: Thu, 13 Jun 2024 01:39:58 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:d8af1a6e4790dda0736f5faf22197c7fe1ee5abe2cf42726bd49f2bccbb00267
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94378641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc288a658b1fbbe3a1432d63572d022d962b59505d92f3d29896408c14a5e02a`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:57 GMT
ADD file:cd3edc79f93d09aa5daffba99cc698c3fe0e02348e8dc284ef466b7e6596e68c in / 
# Thu, 13 Jun 2024 00:39:58 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:37:25 GMT
STOPSIGNAL SIGINT
# Thu, 13 Jun 2024 01:37:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:37:43 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 13 Jun 2024 01:37:44 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 13 Jun 2024 01:37:44 GMT
WORKDIR /var/www/html
# Thu, 13 Jun 2024 01:37:44 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 13 Jun 2024 01:37:44 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 13 Jun 2024 01:37:44 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 13 Jun 2024 01:37:44 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 13 Jun 2024 01:37:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 13 Jun 2024 01:37:54 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 13 Jun 2024 01:37:54 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 13 Jun 2024 01:37:54 GMT
USER adminer
# Thu, 13 Jun 2024 01:37:54 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 13 Jun 2024 01:37:54 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:f975e52008de385eb513258b4912477b214cddf1c8e87877f85028d940bfcdae`  
		Last Modified: Thu, 13 Jun 2024 00:43:32 GMT  
		Size: 53.7 MB (53739581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f641c28bc730b8d437852101fa93688c6eb9335b6539bd5052f2ea87bcd4b11b`  
		Last Modified: Thu, 13 Jun 2024 01:38:27 GMT  
		Size: 39.2 MB (39248753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e66f05563a3653bba4ad66a6a05dfca75dc1429eab3f45c6614365e7d02493f`  
		Last Modified: Thu, 13 Jun 2024 01:38:20 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87aedf58643a09b0a2a84cd4edcc90043aab9fb4b208abf921ce255e65729bb`  
		Last Modified: Thu, 13 Jun 2024 01:38:20 GMT  
		Size: 1.9 KB (1850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d54ed2524cec1d2fe3ede2c7fa20fe3a3c94bc18f9e7019a1145d75f6bc1be`  
		Last Modified: Thu, 13 Jun 2024 01:38:20 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:790a0f0de86e6dcbbf353e32ed060a9cebcb71e2c534663a74f0344c16ece4d1`  
		Last Modified: Thu, 13 Jun 2024 01:38:21 GMT  
		Size: 1.4 MB (1386097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53dfc7bb2d3d9c76a6a81b5c41309b69c035f1620748b4acca7d1280a5553468`  
		Last Modified: Thu, 13 Jun 2024 01:38:20 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; 386

```console
$ docker pull adminer@sha256:6eed96cc26b65ae3badbf706c4089c27f69a714dbe2e1f33c538c6be4c0788ed
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (97027521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429ae822080a387b296d0ee72f12171f25ed959775928a69683edb9549209235`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:07 GMT
ADD file:fc81ef6f19f37bfa7f991304cb9f2ad236462384e498e18c844726149b1fbf03 in / 
# Thu, 13 Jun 2024 00:39:07 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:05:04 GMT
STOPSIGNAL SIGINT
# Thu, 13 Jun 2024 01:05:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:05:36 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 13 Jun 2024 01:05:37 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 13 Jun 2024 01:05:37 GMT
WORKDIR /var/www/html
# Thu, 13 Jun 2024 01:05:37 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 13 Jun 2024 01:05:37 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 13 Jun 2024 01:05:38 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 13 Jun 2024 01:05:38 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 13 Jun 2024 01:05:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 13 Jun 2024 01:05:51 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 13 Jun 2024 01:05:52 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 13 Jun 2024 01:05:52 GMT
USER adminer
# Thu, 13 Jun 2024 01:05:52 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 13 Jun 2024 01:05:52 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:ab8c2df85dcd39d367cf1116e6aa73c53bbbd9e40b1c09e65b70b58871ceff91`  
		Last Modified: Thu, 13 Jun 2024 00:43:45 GMT  
		Size: 56.1 MB (56076538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd70adc0979b6c70e579bbb9744550948b6e315805e8467deb41ac430e42745c`  
		Last Modified: Thu, 13 Jun 2024 01:06:38 GMT  
		Size: 39.6 MB (39560733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911a41e8fea7f7307d289c2d85c05d794803f1940a0a0af5bc0b10869de3ecf5`  
		Last Modified: Thu, 13 Jun 2024 01:06:28 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3688ef69aeb754715b4d5e83bb96975fc12438574d7f31e2f248033eeac89f08`  
		Last Modified: Thu, 13 Jun 2024 01:06:28 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07790203972cf5b1cd6fb239165a5ecc59b867b3116aad22120fcb652078b99f`  
		Last Modified: Thu, 13 Jun 2024 01:06:28 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:491fefe05fe8d7cce3c977b2f6593e4a81ccbf9b0e045899d65997cdcda9019e`  
		Last Modified: Thu, 13 Jun 2024 01:06:28 GMT  
		Size: 1.4 MB (1386059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44bc7becc13f38e635e0e6044a4653a2255b12ed6920c2256554dcbaeacc313b`  
		Last Modified: Thu, 13 Jun 2024 01:06:28 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; mips64le

```console
$ docker pull adminer@sha256:0fb469193f6ef5dd797e94b4a5d26c3ccc445a7ebafb33cd94fa2e92d31f213d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92668752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c096b4d3da36463c7ff019748a3fc9d658ac47882b527bb2d0d4ed919a821995`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 13 Jun 2024 01:11:08 GMT
ADD file:2fd9c13efc7b13ca68928f53acc0c79d5841bd49e5aea46b2e1906120bba2a4f in / 
# Thu, 13 Jun 2024 01:11:14 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:52:45 GMT
STOPSIGNAL SIGINT
# Thu, 13 Jun 2024 01:54:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:54:42 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 13 Jun 2024 01:54:49 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 13 Jun 2024 01:54:53 GMT
WORKDIR /var/www/html
# Thu, 13 Jun 2024 01:54:57 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 13 Jun 2024 01:55:00 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 13 Jun 2024 01:55:04 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 13 Jun 2024 01:55:08 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 13 Jun 2024 01:55:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 13 Jun 2024 01:56:02 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 13 Jun 2024 01:56:06 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 13 Jun 2024 01:56:10 GMT
USER adminer
# Thu, 13 Jun 2024 01:56:13 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 13 Jun 2024 01:56:17 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:6c9f7b7d6baf92c8cec25b325ea14db33b8c298218a5bcd368bb24184c5645b6`  
		Last Modified: Thu, 13 Jun 2024 01:22:39 GMT  
		Size: 53.3 MB (53322503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6286ef03f5f44db3091cf10550155fcd766aad35a34e953e45d1cfa6fd40097a`  
		Last Modified: Thu, 13 Jun 2024 01:58:49 GMT  
		Size: 38.0 MB (37955041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34520f680390c3a57d5c964566ee1a2d7be0387cd3623d59e17c9562c4b79ea1`  
		Last Modified: Thu, 13 Jun 2024 01:58:22 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a291a14bec22546cd0ffc44989b7066716ac71cc7d672223e87b641c915429`  
		Last Modified: Thu, 13 Jun 2024 01:58:22 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86ccfbc39445fe917d1bf1ea517fd405b4c7015b31448363c887fd735e7e0af`  
		Last Modified: Thu, 13 Jun 2024 01:58:22 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ff8ac698f7f6f819281e102d83a76df73a8404cfe23f25910308e7cf33e015`  
		Last Modified: Thu, 13 Jun 2024 01:58:23 GMT  
		Size: 1.4 MB (1387106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617f08a852a43f41121e002e13819c86e599d1c8e8f3e3f435ea9e886594062b`  
		Last Modified: Thu, 13 Jun 2024 01:58:22 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:cd82996bfd25c69f8649a25f4a2c2e101aa5fad843371a36c4becf622b8355f2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101305766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b49a2cc952e881816fd1a4a46458e47fa0a932f042ccdb982bc247772fe154`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 13 Jun 2024 01:17:16 GMT
ADD file:32733696002797fb377d3d8094c21c0f41f25da6f371eb4a8ecb6fa5c3ef1048 in / 
# Thu, 13 Jun 2024 01:17:19 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 02:04:49 GMT
STOPSIGNAL SIGINT
# Thu, 13 Jun 2024 02:05:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 02:05:31 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 13 Jun 2024 02:05:33 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 13 Jun 2024 02:05:33 GMT
WORKDIR /var/www/html
# Thu, 13 Jun 2024 02:05:33 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 13 Jun 2024 02:05:34 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 13 Jun 2024 02:05:34 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 13 Jun 2024 02:05:34 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 13 Jun 2024 02:05:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 13 Jun 2024 02:05:52 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 13 Jun 2024 02:05:52 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 13 Jun 2024 02:05:53 GMT
USER adminer
# Thu, 13 Jun 2024 02:05:53 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 13 Jun 2024 02:05:54 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:7afd12f588c414c122b8d3022d60effda2738a394347f5b3cbdebfe1420a8bf8`  
		Last Modified: Thu, 13 Jun 2024 01:21:54 GMT  
		Size: 59.0 MB (58968957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14936484da494cd94959d98589233d33c9fda4b772203b3adc700475061adca8`  
		Last Modified: Thu, 13 Jun 2024 02:06:45 GMT  
		Size: 40.9 MB (40946433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b967f7e47f6c097aa46ee5427be959a143047870338854795dc84bc5ccbe6e5`  
		Last Modified: Thu, 13 Jun 2024 02:06:36 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720870c5acc421db0558be88f8020c999a8b6c2feb6ba9c48a3359cc6506961d`  
		Last Modified: Thu, 13 Jun 2024 02:06:36 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e55a8311beeccd39c01a921d71ce1633abbf3e370556c120f59902e15683bb5`  
		Last Modified: Thu, 13 Jun 2024 02:06:36 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a637894516909a7eb6378575be506b94699be388ca74bb7b26ed9b51d45cd22`  
		Last Modified: Thu, 13 Jun 2024 02:06:37 GMT  
		Size: 1.4 MB (1386165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9c30254a2fca639379006394e2d9351e74e4f16292b18721ff6008cd6471ab`  
		Last Modified: Thu, 13 Jun 2024 02:06:36 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; s390x

```console
$ docker pull adminer@sha256:4de2ed5a38980b8ca17aac53a4b0af83c65f7e26d2a753aa190a9fbfec5d4276
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.8 MB (93755430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb61a320ed0bd3cea5ab0f85d9a2a99f3197054c0f685fcf3dd7998f839871ce`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 13 Jun 2024 00:42:50 GMT
ADD file:1f0333c084fe60bf682ad64dd7db93b2ca069c7e1d09bf26e7e65dedbd65b0f3 in / 
# Thu, 13 Jun 2024 00:42:53 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:45:29 GMT
STOPSIGNAL SIGINT
# Thu, 13 Jun 2024 03:45:48 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 03:45:50 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 13 Jun 2024 03:45:51 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 13 Jun 2024 03:45:51 GMT
WORKDIR /var/www/html
# Thu, 13 Jun 2024 03:45:51 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 13 Jun 2024 03:45:51 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 13 Jun 2024 03:45:51 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 13 Jun 2024 03:45:51 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 13 Jun 2024 03:46:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 13 Jun 2024 03:46:00 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 13 Jun 2024 03:46:00 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 13 Jun 2024 03:46:00 GMT
USER adminer
# Thu, 13 Jun 2024 03:46:00 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 13 Jun 2024 03:46:01 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:db300ed0c60856815a390ef84dc7c5441283ec11483c9da25ac0daf34bac6e83`  
		Last Modified: Thu, 13 Jun 2024 00:47:59 GMT  
		Size: 53.3 MB (53337540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc6cd8c792e2c5de320a773d4afbdf5678ca7e6885aeff2fe7589799bf031862`  
		Last Modified: Thu, 13 Jun 2024 03:46:41 GMT  
		Size: 39.0 MB (39027515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620f7dcea0dd3c169c6b5c485c4e04e00e4d8df5c54f9c00a213dea7611e3f54`  
		Last Modified: Thu, 13 Jun 2024 03:46:34 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31107d93c69e3ae69f57d322526ee8fb1d9d83e9831768f65408147d62853ff`  
		Last Modified: Thu, 13 Jun 2024 03:46:34 GMT  
		Size: 1.8 KB (1849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a255709c0e45e68b52fa251a2d8e7da034536d5dba096ee5f3377467eefa6b`  
		Last Modified: Thu, 13 Jun 2024 03:46:34 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed97d663856f2fa27506ab0181515848c9ea14c55f3daf519714099f66aee64`  
		Last Modified: Thu, 13 Jun 2024 03:46:35 GMT  
		Size: 1.4 MB (1386173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e439207f962ad3270d9ebea44c769b765b252448d3d4bf53757f3347aed69504`  
		Last Modified: Thu, 13 Jun 2024 03:46:34 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
