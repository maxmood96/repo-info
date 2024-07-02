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
$ docker pull adminer@sha256:dea3a977f570fb7fa915eb9cc4eff9453b5dec959f5e39b1ff5c263a8ead7931
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

### `adminer:4` - linux; arm variant v5

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

### `adminer:4` - linux; arm variant v7

```console
$ docker pull adminer@sha256:31b7f4466600777a9b1395bd710e29d2678d2532a61e56fd551894087072f10f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87818528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0193d31582175a03fb6ac989ece985874ab467e5cc8316916898e5f1a44c7d4e`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Tue, 02 Jul 2024 01:22:58 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 01:22:58 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 01:22:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 01:22:59 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 01:22:59 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 01:22:59 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 01:23:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 01:23:11 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:23:11 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 01:23:11 GMT
USER adminer
# Tue, 02 Jul 2024 01:23:11 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 02 Jul 2024 01:23:11 GMT
EXPOSE 8080
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
	-	`sha256:495508f90db27371a6d4ccaa9ba5c69eddfcaeaa493843b5ef376b869fe3dd20`  
		Last Modified: Tue, 02 Jul 2024 01:23:38 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f301518741ffbed4d0ac9eb2091ac826d9437b9c34a68629de02322f925b4caf`  
		Last Modified: Tue, 02 Jul 2024 01:23:38 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5072cb5f88f258301d3f46cf391f87de359ac3ad7904079b03a989934f4a210d`  
		Last Modified: Tue, 02 Jul 2024 01:23:38 GMT  
		Size: 1.4 MB (1385065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32d5eb14fba1e7e707e2c53ff379a1b5b8b71a14f85b74a82487fe12f2cc28f`  
		Last Modified: Tue, 02 Jul 2024 01:23:38 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; arm64 variant v8

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

### `adminer:4` - linux; ppc64le

```console
$ docker pull adminer@sha256:df6399a4c8d34fb0e39aec3a4375a1d21e2b07d346b795fca1f38403ae148e7f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101284484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0925bd5b0422096a285bc21fcc8029917047d00ad64ef99480ac57260fb140`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Tue, 02 Jul 2024 01:42:30 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 01:42:31 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 01:42:31 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 01:42:31 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 01:42:32 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 01:42:32 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 01:42:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 01:42:52 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:42:52 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 01:42:52 GMT
USER adminer
# Tue, 02 Jul 2024 01:42:53 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 02 Jul 2024 01:42:53 GMT
EXPOSE 8080
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
	-	`sha256:a5e41133683d93c9a4ee46563fe82cee03027bd953723d07800faf25ab715498`  
		Last Modified: Tue, 02 Jul 2024 01:43:37 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655ab712f8dad329105d998bd635ee6ab7158469a7f7dfa956a2c7537346d0af`  
		Last Modified: Tue, 02 Jul 2024 01:43:37 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fa1313b06b674079cefe8609840e63f4baf5eef2bdf1b3d9439ea8132da849`  
		Last Modified: Tue, 02 Jul 2024 01:43:38 GMT  
		Size: 1.4 MB (1385177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60660ba99b7cabbf459c20e50935112439bb57506185efb5eb322a45b2e75517`  
		Last Modified: Tue, 02 Jul 2024 01:43:37 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4` - linux; s390x

```console
$ docker pull adminer@sha256:847076993f77bd77c8c906e3e200b8a96e6c955ed6dfa896559695a4566ad2f0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93735230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde3806121ccc0e28f3eca6d7d9b7167335ff24b662e9898e61ac37004644346`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Tue, 02 Jul 2024 01:10:16 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 01:10:16 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 01:10:16 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 01:10:16 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 01:10:16 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 01:10:16 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 01:10:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 01:10:27 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:10:27 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 01:10:27 GMT
USER adminer
# Tue, 02 Jul 2024 01:10:27 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 02 Jul 2024 01:10:27 GMT
EXPOSE 8080
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
	-	`sha256:68a1cd83feffb00c5dae989fa0d569958faeca87e9090eae827344012ff1dd10`  
		Last Modified: Tue, 02 Jul 2024 01:11:00 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc1d6a070a94f6e849c71cf7d2577aded8a5c29630d46aff7c9eac6c711a783b`  
		Last Modified: Tue, 02 Jul 2024 01:11:00 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a597ba8dc6826a601f6e136bc4d54e3cabab1c08e7cd0205abff027dc23b0d`  
		Last Modified: Tue, 02 Jul 2024 01:11:00 GMT  
		Size: 1.4 MB (1385107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc2c2d87645cda91fc9ba3f73b5141d0f2150bc194888db6350d0fe43a943e7`  
		Last Modified: Tue, 02 Jul 2024 01:11:00 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4-fastcgi`

```console
$ docker pull adminer@sha256:58e3e6a740a2bae54c17bfbf906286cb49171efc0dea1f2d5a1bd89b2803d479
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

### `adminer:4-fastcgi` - linux; arm variant v5

```console
$ docker pull adminer@sha256:97918751a70215c2d1f7d8709b223f57ca2f90f03bee793c0bf06ba27579fecd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91244727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd3804a7c768a17da07b0a0d8fc1613d945171bc70c7c97cd5e5be5da3477b6e`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

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
# Thu, 13 Jun 2024 01:12:05 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 13 Jun 2024 01:12:06 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 13 Jun 2024 01:12:06 GMT
WORKDIR /var/www/html
# Thu, 13 Jun 2024 01:12:06 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 13 Jun 2024 01:12:06 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 13 Jun 2024 01:12:06 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 13 Jun 2024 01:12:06 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 13 Jun 2024 01:12:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 13 Jun 2024 01:12:19 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 13 Jun 2024 01:12:19 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 13 Jun 2024 01:12:19 GMT
USER adminer
# Thu, 13 Jun 2024 01:12:19 GMT
CMD ["php-fpm7.4"]
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
	-	`sha256:99c71f4149c1ed8abee113bdd5422e974fb3d0e22c9e93dcb3f5f5835ad4a4c9`  
		Last Modified: Thu, 13 Jun 2024 01:12:57 GMT  
		Size: 2.7 KB (2705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39e67b43f91efadf13aaf58c35a8f845571cf9cdfad5bba3dd36804a43032af`  
		Last Modified: Thu, 13 Jun 2024 01:12:57 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c6afc15fdcdd199de9c1d249a3b4f5313bf393174ec7dec9ebc474b736a6c5`  
		Last Modified: Thu, 13 Jun 2024 01:12:57 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e9b7e2d46e0ca7a01ad5a6fc46ee81aa3ed30c91a024b080027b6d8d27e8b4`  
		Last Modified: Thu, 13 Jun 2024 01:12:57 GMT  
		Size: 1.4 MB (1386038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8618e211d113079c461d2ba5730953bfd42d6aaa131fc97957be5bc1f447f16f`  
		Last Modified: Thu, 13 Jun 2024 01:12:57 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm variant v7

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

### `adminer:4-fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:28363b2363b7fbdd59662f893fe4312e2b0606e94d5f964c325ae5305ac89934
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94381355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db5f0d2f82c092aebac0f03cda896da1862dc8388dac3f41179a8d6f64229495`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

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
# Thu, 13 Jun 2024 01:37:59 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 13 Jun 2024 01:37:59 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 13 Jun 2024 01:37:59 GMT
WORKDIR /var/www/html
# Thu, 13 Jun 2024 01:37:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 13 Jun 2024 01:38:00 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 13 Jun 2024 01:38:00 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 13 Jun 2024 01:38:00 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 13 Jun 2024 01:38:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 13 Jun 2024 01:38:09 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 13 Jun 2024 01:38:09 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 13 Jun 2024 01:38:09 GMT
USER adminer
# Thu, 13 Jun 2024 01:38:10 GMT
CMD ["php-fpm7.4"]
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
	-	`sha256:943f8ed3c9beeb12753f536cfa2c075e190f9a06d26af93fa2b383d4a9c6cfaf`  
		Last Modified: Thu, 13 Jun 2024 01:38:42 GMT  
		Size: 2.7 KB (2709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe26db6b399e6ac71bf74c791664ba58d244b15494a5bf92553d39807be33b39`  
		Last Modified: Thu, 13 Jun 2024 01:38:42 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c61b8f9fe2ffac97e384f37df9be3c70ebd85351645f48b92aa82135ad23d2`  
		Last Modified: Thu, 13 Jun 2024 01:38:43 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cba9eefbdf5769a3bf555e37a9e50346d0a4451a25f9fa6b2b38fefdbc592f8`  
		Last Modified: Thu, 13 Jun 2024 01:38:43 GMT  
		Size: 1.4 MB (1386105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee50de080300c80609cc2fdf2df8139d6a811a9be505b7d20fdf3269a7b6316`  
		Last Modified: Thu, 13 Jun 2024 01:38:42 GMT  
		Size: 492.0 B  
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
$ docker pull adminer@sha256:ea1e2264c1fbc00782e1de3d71dd8fd8c62b642e414754408c7666f6f512b92e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92671465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ddb5731783e7529877e7a2fa67eb0f4ad51d395a740efd187c87d29ae6db82`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

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
# Thu, 13 Jun 2024 01:56:33 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 13 Jun 2024 01:56:40 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 13 Jun 2024 01:56:44 GMT
WORKDIR /var/www/html
# Thu, 13 Jun 2024 01:56:48 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 13 Jun 2024 01:56:51 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 13 Jun 2024 01:56:55 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 13 Jun 2024 01:56:59 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 13 Jun 2024 01:57:48 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 13 Jun 2024 01:57:51 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 13 Jun 2024 01:57:55 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 13 Jun 2024 01:57:59 GMT
USER adminer
# Thu, 13 Jun 2024 01:58:03 GMT
CMD ["php-fpm7.4"]
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
	-	`sha256:fb5bef733c205b93660e9ee2f8ac05ede126dd141f1db35768b92fecf1a3ad3c`  
		Last Modified: Thu, 13 Jun 2024 01:59:08 GMT  
		Size: 2.7 KB (2715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d92d2b77ccf11897eb8fab4f18e3cd2468f90f5c41d6f1adbf7f6d3e8b05294`  
		Last Modified: Thu, 13 Jun 2024 01:59:08 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f42827fffa7a0bf44b8a512650ee1671694126721d3d2aaf0467816ea12305c0`  
		Last Modified: Thu, 13 Jun 2024 01:59:08 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e33daaf25dc0d8e68bc182780a57e03f528e693e2cf2a68a249b0cbe97eabf6`  
		Last Modified: Thu, 13 Jun 2024 01:59:09 GMT  
		Size: 1.4 MB (1387109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c829d6f1b0d04015e2900583c5ecf10646e3b5b91285e7c9391cfb70c6f7088f`  
		Last Modified: Thu, 13 Jun 2024 01:59:08 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; ppc64le

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

### `adminer:4-fastcgi` - linux; s390x

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

## `adminer:4-standalone`

```console
$ docker pull adminer@sha256:dea3a977f570fb7fa915eb9cc4eff9453b5dec959f5e39b1ff5c263a8ead7931
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
$ docker pull adminer@sha256:31b7f4466600777a9b1395bd710e29d2678d2532a61e56fd551894087072f10f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87818528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0193d31582175a03fb6ac989ece985874ab467e5cc8316916898e5f1a44c7d4e`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Tue, 02 Jul 2024 01:22:58 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 01:22:58 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 01:22:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 01:22:59 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 01:22:59 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 01:22:59 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 01:23:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 01:23:11 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:23:11 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 01:23:11 GMT
USER adminer
# Tue, 02 Jul 2024 01:23:11 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 02 Jul 2024 01:23:11 GMT
EXPOSE 8080
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
	-	`sha256:495508f90db27371a6d4ccaa9ba5c69eddfcaeaa493843b5ef376b869fe3dd20`  
		Last Modified: Tue, 02 Jul 2024 01:23:38 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f301518741ffbed4d0ac9eb2091ac826d9437b9c34a68629de02322f925b4caf`  
		Last Modified: Tue, 02 Jul 2024 01:23:38 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5072cb5f88f258301d3f46cf391f87de359ac3ad7904079b03a989934f4a210d`  
		Last Modified: Tue, 02 Jul 2024 01:23:38 GMT  
		Size: 1.4 MB (1385065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32d5eb14fba1e7e707e2c53ff379a1b5b8b71a14f85b74a82487fe12f2cc28f`  
		Last Modified: Tue, 02 Jul 2024 01:23:38 GMT  
		Size: 490.0 B  
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
$ docker pull adminer@sha256:df6399a4c8d34fb0e39aec3a4375a1d21e2b07d346b795fca1f38403ae148e7f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101284484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0925bd5b0422096a285bc21fcc8029917047d00ad64ef99480ac57260fb140`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Tue, 02 Jul 2024 01:42:30 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 01:42:31 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 01:42:31 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 01:42:31 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 01:42:32 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 01:42:32 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 01:42:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 01:42:52 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:42:52 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 01:42:52 GMT
USER adminer
# Tue, 02 Jul 2024 01:42:53 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 02 Jul 2024 01:42:53 GMT
EXPOSE 8080
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
	-	`sha256:a5e41133683d93c9a4ee46563fe82cee03027bd953723d07800faf25ab715498`  
		Last Modified: Tue, 02 Jul 2024 01:43:37 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655ab712f8dad329105d998bd635ee6ab7158469a7f7dfa956a2c7537346d0af`  
		Last Modified: Tue, 02 Jul 2024 01:43:37 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fa1313b06b674079cefe8609840e63f4baf5eef2bdf1b3d9439ea8132da849`  
		Last Modified: Tue, 02 Jul 2024 01:43:38 GMT  
		Size: 1.4 MB (1385177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60660ba99b7cabbf459c20e50935112439bb57506185efb5eb322a45b2e75517`  
		Last Modified: Tue, 02 Jul 2024 01:43:37 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; s390x

```console
$ docker pull adminer@sha256:847076993f77bd77c8c906e3e200b8a96e6c955ed6dfa896559695a4566ad2f0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93735230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde3806121ccc0e28f3eca6d7d9b7167335ff24b662e9898e61ac37004644346`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Tue, 02 Jul 2024 01:10:16 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 01:10:16 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 01:10:16 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 01:10:16 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 01:10:16 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 01:10:16 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 01:10:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 01:10:27 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:10:27 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 01:10:27 GMT
USER adminer
# Tue, 02 Jul 2024 01:10:27 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 02 Jul 2024 01:10:27 GMT
EXPOSE 8080
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
	-	`sha256:68a1cd83feffb00c5dae989fa0d569958faeca87e9090eae827344012ff1dd10`  
		Last Modified: Tue, 02 Jul 2024 01:11:00 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc1d6a070a94f6e849c71cf7d2577aded8a5c29630d46aff7c9eac6c711a783b`  
		Last Modified: Tue, 02 Jul 2024 01:11:00 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a597ba8dc6826a601f6e136bc4d54e3cabab1c08e7cd0205abff027dc23b0d`  
		Last Modified: Tue, 02 Jul 2024 01:11:00 GMT  
		Size: 1.4 MB (1385107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc2c2d87645cda91fc9ba3f73b5141d0f2150bc194888db6350d0fe43a943e7`  
		Last Modified: Tue, 02 Jul 2024 01:11:00 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4.8.1`

```console
$ docker pull adminer@sha256:dea3a977f570fb7fa915eb9cc4eff9453b5dec959f5e39b1ff5c263a8ead7931
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

### `adminer:4.8.1` - linux; arm variant v5

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

### `adminer:4.8.1` - linux; arm variant v7

```console
$ docker pull adminer@sha256:31b7f4466600777a9b1395bd710e29d2678d2532a61e56fd551894087072f10f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87818528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0193d31582175a03fb6ac989ece985874ab467e5cc8316916898e5f1a44c7d4e`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Tue, 02 Jul 2024 01:22:58 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 01:22:58 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 01:22:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 01:22:59 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 01:22:59 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 01:22:59 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 01:23:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 01:23:11 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:23:11 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 01:23:11 GMT
USER adminer
# Tue, 02 Jul 2024 01:23:11 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 02 Jul 2024 01:23:11 GMT
EXPOSE 8080
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
	-	`sha256:495508f90db27371a6d4ccaa9ba5c69eddfcaeaa493843b5ef376b869fe3dd20`  
		Last Modified: Tue, 02 Jul 2024 01:23:38 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f301518741ffbed4d0ac9eb2091ac826d9437b9c34a68629de02322f925b4caf`  
		Last Modified: Tue, 02 Jul 2024 01:23:38 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5072cb5f88f258301d3f46cf391f87de359ac3ad7904079b03a989934f4a210d`  
		Last Modified: Tue, 02 Jul 2024 01:23:38 GMT  
		Size: 1.4 MB (1385065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32d5eb14fba1e7e707e2c53ff379a1b5b8b71a14f85b74a82487fe12f2cc28f`  
		Last Modified: Tue, 02 Jul 2024 01:23:38 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1` - linux; arm64 variant v8

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

### `adminer:4.8.1` - linux; ppc64le

```console
$ docker pull adminer@sha256:df6399a4c8d34fb0e39aec3a4375a1d21e2b07d346b795fca1f38403ae148e7f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101284484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0925bd5b0422096a285bc21fcc8029917047d00ad64ef99480ac57260fb140`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Tue, 02 Jul 2024 01:42:30 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 01:42:31 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 01:42:31 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 01:42:31 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 01:42:32 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 01:42:32 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 01:42:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 01:42:52 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:42:52 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 01:42:52 GMT
USER adminer
# Tue, 02 Jul 2024 01:42:53 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 02 Jul 2024 01:42:53 GMT
EXPOSE 8080
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
	-	`sha256:a5e41133683d93c9a4ee46563fe82cee03027bd953723d07800faf25ab715498`  
		Last Modified: Tue, 02 Jul 2024 01:43:37 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655ab712f8dad329105d998bd635ee6ab7158469a7f7dfa956a2c7537346d0af`  
		Last Modified: Tue, 02 Jul 2024 01:43:37 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fa1313b06b674079cefe8609840e63f4baf5eef2bdf1b3d9439ea8132da849`  
		Last Modified: Tue, 02 Jul 2024 01:43:38 GMT  
		Size: 1.4 MB (1385177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60660ba99b7cabbf459c20e50935112439bb57506185efb5eb322a45b2e75517`  
		Last Modified: Tue, 02 Jul 2024 01:43:37 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1` - linux; s390x

```console
$ docker pull adminer@sha256:847076993f77bd77c8c906e3e200b8a96e6c955ed6dfa896559695a4566ad2f0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93735230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde3806121ccc0e28f3eca6d7d9b7167335ff24b662e9898e61ac37004644346`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Tue, 02 Jul 2024 01:10:16 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 01:10:16 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 01:10:16 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 01:10:16 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 01:10:16 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 01:10:16 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 01:10:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 01:10:27 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:10:27 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 01:10:27 GMT
USER adminer
# Tue, 02 Jul 2024 01:10:27 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 02 Jul 2024 01:10:27 GMT
EXPOSE 8080
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
	-	`sha256:68a1cd83feffb00c5dae989fa0d569958faeca87e9090eae827344012ff1dd10`  
		Last Modified: Tue, 02 Jul 2024 01:11:00 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc1d6a070a94f6e849c71cf7d2577aded8a5c29630d46aff7c9eac6c711a783b`  
		Last Modified: Tue, 02 Jul 2024 01:11:00 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a597ba8dc6826a601f6e136bc4d54e3cabab1c08e7cd0205abff027dc23b0d`  
		Last Modified: Tue, 02 Jul 2024 01:11:00 GMT  
		Size: 1.4 MB (1385107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc2c2d87645cda91fc9ba3f73b5141d0f2150bc194888db6350d0fe43a943e7`  
		Last Modified: Tue, 02 Jul 2024 01:11:00 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:4.8.1-fastcgi`

```console
$ docker pull adminer@sha256:58e3e6a740a2bae54c17bfbf906286cb49171efc0dea1f2d5a1bd89b2803d479
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

### `adminer:4.8.1-fastcgi` - linux; arm variant v5

```console
$ docker pull adminer@sha256:97918751a70215c2d1f7d8709b223f57ca2f90f03bee793c0bf06ba27579fecd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91244727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd3804a7c768a17da07b0a0d8fc1613d945171bc70c7c97cd5e5be5da3477b6e`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

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
# Thu, 13 Jun 2024 01:12:05 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 13 Jun 2024 01:12:06 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 13 Jun 2024 01:12:06 GMT
WORKDIR /var/www/html
# Thu, 13 Jun 2024 01:12:06 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 13 Jun 2024 01:12:06 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 13 Jun 2024 01:12:06 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 13 Jun 2024 01:12:06 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 13 Jun 2024 01:12:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 13 Jun 2024 01:12:19 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 13 Jun 2024 01:12:19 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 13 Jun 2024 01:12:19 GMT
USER adminer
# Thu, 13 Jun 2024 01:12:19 GMT
CMD ["php-fpm7.4"]
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
	-	`sha256:99c71f4149c1ed8abee113bdd5422e974fb3d0e22c9e93dcb3f5f5835ad4a4c9`  
		Last Modified: Thu, 13 Jun 2024 01:12:57 GMT  
		Size: 2.7 KB (2705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39e67b43f91efadf13aaf58c35a8f845571cf9cdfad5bba3dd36804a43032af`  
		Last Modified: Thu, 13 Jun 2024 01:12:57 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c6afc15fdcdd199de9c1d249a3b4f5313bf393174ec7dec9ebc474b736a6c5`  
		Last Modified: Thu, 13 Jun 2024 01:12:57 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e9b7e2d46e0ca7a01ad5a6fc46ee81aa3ed30c91a024b080027b6d8d27e8b4`  
		Last Modified: Thu, 13 Jun 2024 01:12:57 GMT  
		Size: 1.4 MB (1386038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8618e211d113079c461d2ba5730953bfd42d6aaa131fc97957be5bc1f447f16f`  
		Last Modified: Thu, 13 Jun 2024 01:12:57 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-fastcgi` - linux; arm variant v7

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

### `adminer:4.8.1-fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:28363b2363b7fbdd59662f893fe4312e2b0606e94d5f964c325ae5305ac89934
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94381355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db5f0d2f82c092aebac0f03cda896da1862dc8388dac3f41179a8d6f64229495`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

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
# Thu, 13 Jun 2024 01:37:59 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 13 Jun 2024 01:37:59 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 13 Jun 2024 01:37:59 GMT
WORKDIR /var/www/html
# Thu, 13 Jun 2024 01:37:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 13 Jun 2024 01:38:00 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 13 Jun 2024 01:38:00 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 13 Jun 2024 01:38:00 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 13 Jun 2024 01:38:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 13 Jun 2024 01:38:09 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 13 Jun 2024 01:38:09 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 13 Jun 2024 01:38:09 GMT
USER adminer
# Thu, 13 Jun 2024 01:38:10 GMT
CMD ["php-fpm7.4"]
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
	-	`sha256:943f8ed3c9beeb12753f536cfa2c075e190f9a06d26af93fa2b383d4a9c6cfaf`  
		Last Modified: Thu, 13 Jun 2024 01:38:42 GMT  
		Size: 2.7 KB (2709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe26db6b399e6ac71bf74c791664ba58d244b15494a5bf92553d39807be33b39`  
		Last Modified: Thu, 13 Jun 2024 01:38:42 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c61b8f9fe2ffac97e384f37df9be3c70ebd85351645f48b92aa82135ad23d2`  
		Last Modified: Thu, 13 Jun 2024 01:38:43 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cba9eefbdf5769a3bf555e37a9e50346d0a4451a25f9fa6b2b38fefdbc592f8`  
		Last Modified: Thu, 13 Jun 2024 01:38:43 GMT  
		Size: 1.4 MB (1386105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee50de080300c80609cc2fdf2df8139d6a811a9be505b7d20fdf3269a7b6316`  
		Last Modified: Thu, 13 Jun 2024 01:38:42 GMT  
		Size: 492.0 B  
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
$ docker pull adminer@sha256:ea1e2264c1fbc00782e1de3d71dd8fd8c62b642e414754408c7666f6f512b92e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92671465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ddb5731783e7529877e7a2fa67eb0f4ad51d395a740efd187c87d29ae6db82`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

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
# Thu, 13 Jun 2024 01:56:33 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 13 Jun 2024 01:56:40 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 13 Jun 2024 01:56:44 GMT
WORKDIR /var/www/html
# Thu, 13 Jun 2024 01:56:48 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 13 Jun 2024 01:56:51 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 13 Jun 2024 01:56:55 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 13 Jun 2024 01:56:59 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 13 Jun 2024 01:57:48 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 13 Jun 2024 01:57:51 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 13 Jun 2024 01:57:55 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 13 Jun 2024 01:57:59 GMT
USER adminer
# Thu, 13 Jun 2024 01:58:03 GMT
CMD ["php-fpm7.4"]
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
	-	`sha256:fb5bef733c205b93660e9ee2f8ac05ede126dd141f1db35768b92fecf1a3ad3c`  
		Last Modified: Thu, 13 Jun 2024 01:59:08 GMT  
		Size: 2.7 KB (2715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d92d2b77ccf11897eb8fab4f18e3cd2468f90f5c41d6f1adbf7f6d3e8b05294`  
		Last Modified: Thu, 13 Jun 2024 01:59:08 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f42827fffa7a0bf44b8a512650ee1671694126721d3d2aaf0467816ea12305c0`  
		Last Modified: Thu, 13 Jun 2024 01:59:08 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e33daaf25dc0d8e68bc182780a57e03f528e693e2cf2a68a249b0cbe97eabf6`  
		Last Modified: Thu, 13 Jun 2024 01:59:09 GMT  
		Size: 1.4 MB (1387109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c829d6f1b0d04015e2900583c5ecf10646e3b5b91285e7c9391cfb70c6f7088f`  
		Last Modified: Thu, 13 Jun 2024 01:59:08 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-fastcgi` - linux; ppc64le

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

### `adminer:4.8.1-fastcgi` - linux; s390x

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

## `adminer:4.8.1-standalone`

```console
$ docker pull adminer@sha256:dea3a977f570fb7fa915eb9cc4eff9453b5dec959f5e39b1ff5c263a8ead7931
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

### `adminer:4.8.1-standalone` - linux; arm variant v5

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

### `adminer:4.8.1-standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:31b7f4466600777a9b1395bd710e29d2678d2532a61e56fd551894087072f10f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87818528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0193d31582175a03fb6ac989ece985874ab467e5cc8316916898e5f1a44c7d4e`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Tue, 02 Jul 2024 01:22:58 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 01:22:58 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 01:22:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 01:22:59 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 01:22:59 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 01:22:59 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 01:23:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 01:23:11 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:23:11 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 01:23:11 GMT
USER adminer
# Tue, 02 Jul 2024 01:23:11 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 02 Jul 2024 01:23:11 GMT
EXPOSE 8080
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
	-	`sha256:495508f90db27371a6d4ccaa9ba5c69eddfcaeaa493843b5ef376b869fe3dd20`  
		Last Modified: Tue, 02 Jul 2024 01:23:38 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f301518741ffbed4d0ac9eb2091ac826d9437b9c34a68629de02322f925b4caf`  
		Last Modified: Tue, 02 Jul 2024 01:23:38 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5072cb5f88f258301d3f46cf391f87de359ac3ad7904079b03a989934f4a210d`  
		Last Modified: Tue, 02 Jul 2024 01:23:38 GMT  
		Size: 1.4 MB (1385065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32d5eb14fba1e7e707e2c53ff379a1b5b8b71a14f85b74a82487fe12f2cc28f`  
		Last Modified: Tue, 02 Jul 2024 01:23:38 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-standalone` - linux; arm64 variant v8

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

### `adminer:4.8.1-standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:df6399a4c8d34fb0e39aec3a4375a1d21e2b07d346b795fca1f38403ae148e7f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101284484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0925bd5b0422096a285bc21fcc8029917047d00ad64ef99480ac57260fb140`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Tue, 02 Jul 2024 01:42:30 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 01:42:31 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 01:42:31 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 01:42:31 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 01:42:32 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 01:42:32 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 01:42:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 01:42:52 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:42:52 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 01:42:52 GMT
USER adminer
# Tue, 02 Jul 2024 01:42:53 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 02 Jul 2024 01:42:53 GMT
EXPOSE 8080
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
	-	`sha256:a5e41133683d93c9a4ee46563fe82cee03027bd953723d07800faf25ab715498`  
		Last Modified: Tue, 02 Jul 2024 01:43:37 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655ab712f8dad329105d998bd635ee6ab7158469a7f7dfa956a2c7537346d0af`  
		Last Modified: Tue, 02 Jul 2024 01:43:37 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fa1313b06b674079cefe8609840e63f4baf5eef2bdf1b3d9439ea8132da849`  
		Last Modified: Tue, 02 Jul 2024 01:43:38 GMT  
		Size: 1.4 MB (1385177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60660ba99b7cabbf459c20e50935112439bb57506185efb5eb322a45b2e75517`  
		Last Modified: Tue, 02 Jul 2024 01:43:37 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4.8.1-standalone` - linux; s390x

```console
$ docker pull adminer@sha256:847076993f77bd77c8c906e3e200b8a96e6c955ed6dfa896559695a4566ad2f0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93735230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde3806121ccc0e28f3eca6d7d9b7167335ff24b662e9898e61ac37004644346`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Tue, 02 Jul 2024 01:10:16 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 01:10:16 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 01:10:16 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 01:10:16 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 01:10:16 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 01:10:16 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 01:10:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 01:10:27 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:10:27 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 01:10:27 GMT
USER adminer
# Tue, 02 Jul 2024 01:10:27 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 02 Jul 2024 01:10:27 GMT
EXPOSE 8080
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
	-	`sha256:68a1cd83feffb00c5dae989fa0d569958faeca87e9090eae827344012ff1dd10`  
		Last Modified: Tue, 02 Jul 2024 01:11:00 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc1d6a070a94f6e849c71cf7d2577aded8a5c29630d46aff7c9eac6c711a783b`  
		Last Modified: Tue, 02 Jul 2024 01:11:00 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a597ba8dc6826a601f6e136bc4d54e3cabab1c08e7cd0205abff027dc23b0d`  
		Last Modified: Tue, 02 Jul 2024 01:11:00 GMT  
		Size: 1.4 MB (1385107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc2c2d87645cda91fc9ba3f73b5141d0f2150bc194888db6350d0fe43a943e7`  
		Last Modified: Tue, 02 Jul 2024 01:11:00 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:fastcgi`

```console
$ docker pull adminer@sha256:58e3e6a740a2bae54c17bfbf906286cb49171efc0dea1f2d5a1bd89b2803d479
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
$ docker pull adminer@sha256:97918751a70215c2d1f7d8709b223f57ca2f90f03bee793c0bf06ba27579fecd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91244727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd3804a7c768a17da07b0a0d8fc1613d945171bc70c7c97cd5e5be5da3477b6e`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

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
# Thu, 13 Jun 2024 01:12:05 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 13 Jun 2024 01:12:06 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 13 Jun 2024 01:12:06 GMT
WORKDIR /var/www/html
# Thu, 13 Jun 2024 01:12:06 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 13 Jun 2024 01:12:06 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 13 Jun 2024 01:12:06 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 13 Jun 2024 01:12:06 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 13 Jun 2024 01:12:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 13 Jun 2024 01:12:19 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 13 Jun 2024 01:12:19 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 13 Jun 2024 01:12:19 GMT
USER adminer
# Thu, 13 Jun 2024 01:12:19 GMT
CMD ["php-fpm7.4"]
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
	-	`sha256:99c71f4149c1ed8abee113bdd5422e974fb3d0e22c9e93dcb3f5f5835ad4a4c9`  
		Last Modified: Thu, 13 Jun 2024 01:12:57 GMT  
		Size: 2.7 KB (2705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39e67b43f91efadf13aaf58c35a8f845571cf9cdfad5bba3dd36804a43032af`  
		Last Modified: Thu, 13 Jun 2024 01:12:57 GMT  
		Size: 1.8 KB (1839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c6afc15fdcdd199de9c1d249a3b4f5313bf393174ec7dec9ebc474b736a6c5`  
		Last Modified: Thu, 13 Jun 2024 01:12:57 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e9b7e2d46e0ca7a01ad5a6fc46ee81aa3ed30c91a024b080027b6d8d27e8b4`  
		Last Modified: Thu, 13 Jun 2024 01:12:57 GMT  
		Size: 1.4 MB (1386038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8618e211d113079c461d2ba5730953bfd42d6aaa131fc97957be5bc1f447f16f`  
		Last Modified: Thu, 13 Jun 2024 01:12:57 GMT  
		Size: 491.0 B  
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
$ docker pull adminer@sha256:28363b2363b7fbdd59662f893fe4312e2b0606e94d5f964c325ae5305ac89934
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94381355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db5f0d2f82c092aebac0f03cda896da1862dc8388dac3f41179a8d6f64229495`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

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
# Thu, 13 Jun 2024 01:37:59 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 13 Jun 2024 01:37:59 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 13 Jun 2024 01:37:59 GMT
WORKDIR /var/www/html
# Thu, 13 Jun 2024 01:37:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 13 Jun 2024 01:38:00 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 13 Jun 2024 01:38:00 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 13 Jun 2024 01:38:00 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 13 Jun 2024 01:38:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 13 Jun 2024 01:38:09 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 13 Jun 2024 01:38:09 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 13 Jun 2024 01:38:09 GMT
USER adminer
# Thu, 13 Jun 2024 01:38:10 GMT
CMD ["php-fpm7.4"]
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
	-	`sha256:943f8ed3c9beeb12753f536cfa2c075e190f9a06d26af93fa2b383d4a9c6cfaf`  
		Last Modified: Thu, 13 Jun 2024 01:38:42 GMT  
		Size: 2.7 KB (2709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe26db6b399e6ac71bf74c791664ba58d244b15494a5bf92553d39807be33b39`  
		Last Modified: Thu, 13 Jun 2024 01:38:42 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c61b8f9fe2ffac97e384f37df9be3c70ebd85351645f48b92aa82135ad23d2`  
		Last Modified: Thu, 13 Jun 2024 01:38:43 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cba9eefbdf5769a3bf555e37a9e50346d0a4451a25f9fa6b2b38fefdbc592f8`  
		Last Modified: Thu, 13 Jun 2024 01:38:43 GMT  
		Size: 1.4 MB (1386105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee50de080300c80609cc2fdf2df8139d6a811a9be505b7d20fdf3269a7b6316`  
		Last Modified: Thu, 13 Jun 2024 01:38:42 GMT  
		Size: 492.0 B  
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
$ docker pull adminer@sha256:ea1e2264c1fbc00782e1de3d71dd8fd8c62b642e414754408c7666f6f512b92e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92671465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ddb5731783e7529877e7a2fa67eb0f4ad51d395a740efd187c87d29ae6db82`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

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
# Thu, 13 Jun 2024 01:56:33 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 13 Jun 2024 01:56:40 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 13 Jun 2024 01:56:44 GMT
WORKDIR /var/www/html
# Thu, 13 Jun 2024 01:56:48 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 13 Jun 2024 01:56:51 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 13 Jun 2024 01:56:55 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 13 Jun 2024 01:56:59 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 13 Jun 2024 01:57:48 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 13 Jun 2024 01:57:51 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 13 Jun 2024 01:57:55 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 13 Jun 2024 01:57:59 GMT
USER adminer
# Thu, 13 Jun 2024 01:58:03 GMT
CMD ["php-fpm7.4"]
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
	-	`sha256:fb5bef733c205b93660e9ee2f8ac05ede126dd141f1db35768b92fecf1a3ad3c`  
		Last Modified: Thu, 13 Jun 2024 01:59:08 GMT  
		Size: 2.7 KB (2715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d92d2b77ccf11897eb8fab4f18e3cd2468f90f5c41d6f1adbf7f6d3e8b05294`  
		Last Modified: Thu, 13 Jun 2024 01:59:08 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f42827fffa7a0bf44b8a512650ee1671694126721d3d2aaf0467816ea12305c0`  
		Last Modified: Thu, 13 Jun 2024 01:59:08 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e33daaf25dc0d8e68bc182780a57e03f528e693e2cf2a68a249b0cbe97eabf6`  
		Last Modified: Thu, 13 Jun 2024 01:59:09 GMT  
		Size: 1.4 MB (1387109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c829d6f1b0d04015e2900583c5ecf10646e3b5b91285e7c9391cfb70c6f7088f`  
		Last Modified: Thu, 13 Jun 2024 01:59:08 GMT  
		Size: 493.0 B  
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

## `adminer:latest`

```console
$ docker pull adminer@sha256:dea3a977f570fb7fa915eb9cc4eff9453b5dec959f5e39b1ff5c263a8ead7931
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

### `adminer:latest` - linux; arm variant v5

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

### `adminer:latest` - linux; arm variant v7

```console
$ docker pull adminer@sha256:31b7f4466600777a9b1395bd710e29d2678d2532a61e56fd551894087072f10f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87818528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0193d31582175a03fb6ac989ece985874ab467e5cc8316916898e5f1a44c7d4e`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Tue, 02 Jul 2024 01:22:58 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 01:22:58 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 01:22:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 01:22:59 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 01:22:59 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 01:22:59 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 01:23:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 01:23:11 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:23:11 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 01:23:11 GMT
USER adminer
# Tue, 02 Jul 2024 01:23:11 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 02 Jul 2024 01:23:11 GMT
EXPOSE 8080
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
	-	`sha256:495508f90db27371a6d4ccaa9ba5c69eddfcaeaa493843b5ef376b869fe3dd20`  
		Last Modified: Tue, 02 Jul 2024 01:23:38 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f301518741ffbed4d0ac9eb2091ac826d9437b9c34a68629de02322f925b4caf`  
		Last Modified: Tue, 02 Jul 2024 01:23:38 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5072cb5f88f258301d3f46cf391f87de359ac3ad7904079b03a989934f4a210d`  
		Last Modified: Tue, 02 Jul 2024 01:23:38 GMT  
		Size: 1.4 MB (1385065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32d5eb14fba1e7e707e2c53ff379a1b5b8b71a14f85b74a82487fe12f2cc28f`  
		Last Modified: Tue, 02 Jul 2024 01:23:38 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; arm64 variant v8

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

### `adminer:latest` - linux; ppc64le

```console
$ docker pull adminer@sha256:df6399a4c8d34fb0e39aec3a4375a1d21e2b07d346b795fca1f38403ae148e7f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101284484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0925bd5b0422096a285bc21fcc8029917047d00ad64ef99480ac57260fb140`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Tue, 02 Jul 2024 01:42:30 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 01:42:31 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 01:42:31 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 01:42:31 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 01:42:32 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 01:42:32 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 01:42:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 01:42:52 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:42:52 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 01:42:52 GMT
USER adminer
# Tue, 02 Jul 2024 01:42:53 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 02 Jul 2024 01:42:53 GMT
EXPOSE 8080
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
	-	`sha256:a5e41133683d93c9a4ee46563fe82cee03027bd953723d07800faf25ab715498`  
		Last Modified: Tue, 02 Jul 2024 01:43:37 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655ab712f8dad329105d998bd635ee6ab7158469a7f7dfa956a2c7537346d0af`  
		Last Modified: Tue, 02 Jul 2024 01:43:37 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fa1313b06b674079cefe8609840e63f4baf5eef2bdf1b3d9439ea8132da849`  
		Last Modified: Tue, 02 Jul 2024 01:43:38 GMT  
		Size: 1.4 MB (1385177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60660ba99b7cabbf459c20e50935112439bb57506185efb5eb322a45b2e75517`  
		Last Modified: Tue, 02 Jul 2024 01:43:37 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; s390x

```console
$ docker pull adminer@sha256:847076993f77bd77c8c906e3e200b8a96e6c955ed6dfa896559695a4566ad2f0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93735230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde3806121ccc0e28f3eca6d7d9b7167335ff24b662e9898e61ac37004644346`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Tue, 02 Jul 2024 01:10:16 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 01:10:16 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 01:10:16 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 01:10:16 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 01:10:16 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 01:10:16 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 01:10:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 01:10:27 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:10:27 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 01:10:27 GMT
USER adminer
# Tue, 02 Jul 2024 01:10:27 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 02 Jul 2024 01:10:27 GMT
EXPOSE 8080
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
	-	`sha256:68a1cd83feffb00c5dae989fa0d569958faeca87e9090eae827344012ff1dd10`  
		Last Modified: Tue, 02 Jul 2024 01:11:00 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc1d6a070a94f6e849c71cf7d2577aded8a5c29630d46aff7c9eac6c711a783b`  
		Last Modified: Tue, 02 Jul 2024 01:11:00 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a597ba8dc6826a601f6e136bc4d54e3cabab1c08e7cd0205abff027dc23b0d`  
		Last Modified: Tue, 02 Jul 2024 01:11:00 GMT  
		Size: 1.4 MB (1385107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc2c2d87645cda91fc9ba3f73b5141d0f2150bc194888db6350d0fe43a943e7`  
		Last Modified: Tue, 02 Jul 2024 01:11:00 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `adminer:standalone`

```console
$ docker pull adminer@sha256:dea3a977f570fb7fa915eb9cc4eff9453b5dec959f5e39b1ff5c263a8ead7931
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

### `adminer:standalone` - linux; arm variant v5

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

### `adminer:standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:31b7f4466600777a9b1395bd710e29d2678d2532a61e56fd551894087072f10f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87818528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0193d31582175a03fb6ac989ece985874ab467e5cc8316916898e5f1a44c7d4e`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Tue, 02 Jul 2024 01:22:58 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 01:22:58 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 01:22:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 01:22:59 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 01:22:59 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 01:22:59 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 01:23:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 01:23:11 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:23:11 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 01:23:11 GMT
USER adminer
# Tue, 02 Jul 2024 01:23:11 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 02 Jul 2024 01:23:11 GMT
EXPOSE 8080
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
	-	`sha256:495508f90db27371a6d4ccaa9ba5c69eddfcaeaa493843b5ef376b869fe3dd20`  
		Last Modified: Tue, 02 Jul 2024 01:23:38 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f301518741ffbed4d0ac9eb2091ac826d9437b9c34a68629de02322f925b4caf`  
		Last Modified: Tue, 02 Jul 2024 01:23:38 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5072cb5f88f258301d3f46cf391f87de359ac3ad7904079b03a989934f4a210d`  
		Last Modified: Tue, 02 Jul 2024 01:23:38 GMT  
		Size: 1.4 MB (1385065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32d5eb14fba1e7e707e2c53ff379a1b5b8b71a14f85b74a82487fe12f2cc28f`  
		Last Modified: Tue, 02 Jul 2024 01:23:38 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; arm64 variant v8

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

### `adminer:standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:df6399a4c8d34fb0e39aec3a4375a1d21e2b07d346b795fca1f38403ae148e7f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101284484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0925bd5b0422096a285bc21fcc8029917047d00ad64ef99480ac57260fb140`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Tue, 02 Jul 2024 01:42:30 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 01:42:31 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 01:42:31 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 01:42:31 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 01:42:32 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 01:42:32 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 01:42:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 01:42:52 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:42:52 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 01:42:52 GMT
USER adminer
# Tue, 02 Jul 2024 01:42:53 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 02 Jul 2024 01:42:53 GMT
EXPOSE 8080
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
	-	`sha256:a5e41133683d93c9a4ee46563fe82cee03027bd953723d07800faf25ab715498`  
		Last Modified: Tue, 02 Jul 2024 01:43:37 GMT  
		Size: 1.8 KB (1848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655ab712f8dad329105d998bd635ee6ab7158469a7f7dfa956a2c7537346d0af`  
		Last Modified: Tue, 02 Jul 2024 01:43:37 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fa1313b06b674079cefe8609840e63f4baf5eef2bdf1b3d9439ea8132da849`  
		Last Modified: Tue, 02 Jul 2024 01:43:38 GMT  
		Size: 1.4 MB (1385177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60660ba99b7cabbf459c20e50935112439bb57506185efb5eb322a45b2e75517`  
		Last Modified: Tue, 02 Jul 2024 01:43:37 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; s390x

```console
$ docker pull adminer@sha256:847076993f77bd77c8c906e3e200b8a96e6c955ed6dfa896559695a4566ad2f0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93735230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde3806121ccc0e28f3eca6d7d9b7167335ff24b662e9898e61ac37004644346`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Tue, 02 Jul 2024 01:10:16 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 02 Jul 2024 01:10:16 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 01:10:16 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 02 Jul 2024 01:10:16 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 02 Jul 2024 01:10:16 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 02 Jul 2024 01:10:16 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 02 Jul 2024 01:10:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 02 Jul 2024 01:10:27 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 02 Jul 2024 01:10:27 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 02 Jul 2024 01:10:27 GMT
USER adminer
# Tue, 02 Jul 2024 01:10:27 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 02 Jul 2024 01:10:27 GMT
EXPOSE 8080
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
	-	`sha256:68a1cd83feffb00c5dae989fa0d569958faeca87e9090eae827344012ff1dd10`  
		Last Modified: Tue, 02 Jul 2024 01:11:00 GMT  
		Size: 1.8 KB (1845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc1d6a070a94f6e849c71cf7d2577aded8a5c29630d46aff7c9eac6c711a783b`  
		Last Modified: Tue, 02 Jul 2024 01:11:00 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a597ba8dc6826a601f6e136bc4d54e3cabab1c08e7cd0205abff027dc23b0d`  
		Last Modified: Tue, 02 Jul 2024 01:11:00 GMT  
		Size: 1.4 MB (1385107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc2c2d87645cda91fc9ba3f73b5141d0f2150bc194888db6350d0fe43a943e7`  
		Last Modified: Tue, 02 Jul 2024 01:11:00 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
