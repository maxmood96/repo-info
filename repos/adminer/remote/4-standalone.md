## `adminer:4-standalone`

```console
$ docker pull adminer@sha256:ceca91abccc1fcd97d66cd4e8994e6f0a97a92c0e3dbdc8200d5d735e3088cd1
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
$ docker pull adminer@sha256:3b00f709c59f684aba0a77f23b835307e2884a96ea83b26eb318c0a9d77431b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95967418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b108b9a25fa671e591fb7df00214a46db122f8502901e42828e11bd5bcebb97a`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:59 GMT
ADD file:8efdcc3201e79c8a09fc9c1ade08492ea33f838047332a7c61988f6357339dee in / 
# Wed, 10 Apr 2024 01:50:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:21:07 GMT
STOPSIGNAL SIGINT
# Wed, 10 Apr 2024 05:21:28 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:21:29 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 10 Apr 2024 05:21:29 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 10 Apr 2024 05:21:30 GMT
WORKDIR /var/www/html
# Wed, 10 Apr 2024 05:21:30 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 10 Apr 2024 05:21:30 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 10 Apr 2024 05:21:30 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 10 Apr 2024 05:21:30 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 10 Apr 2024 05:21:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 05:21:42 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 10 Apr 2024 05:21:42 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 10 Apr 2024 05:21:42 GMT
USER adminer
# Wed, 10 Apr 2024 05:21:43 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 10 Apr 2024 05:21:43 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:ac323bdaa10f869bd9e7adecd8f5326e44acc4c59168868108b1cdf3891089cc`  
		Last Modified: Wed, 10 Apr 2024 01:55:52 GMT  
		Size: 55.1 MB (55090264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b529097b53fcfd0216ea1f21a4cd03ccecc5375e060b4db77c22c027df29128e`  
		Last Modified: Wed, 10 Apr 2024 05:22:20 GMT  
		Size: 39.5 MB (39487585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b75f460f48e18c15cf199b0b03ca362ec80c297191f8d334b14692aeeb1e0f7`  
		Last Modified: Wed, 10 Apr 2024 05:22:12 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4706f034e22669ca0b14047087d307d7fdbb18e5b6373d580f0a6e50f8b199c2`  
		Last Modified: Wed, 10 Apr 2024 05:22:13 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27feb402e7aa2348f04ca5e1b052d970032b93a6648fb507551fe5a3106c0a11`  
		Last Modified: Wed, 10 Apr 2024 05:22:12 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966923a29652db6692c880e9033bd279019e4d30e26297a85ebe3f517fe14f20`  
		Last Modified: Wed, 10 Apr 2024 05:22:13 GMT  
		Size: 1.4 MB (1385326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2744415ff8b5324c2b1d87c42910d11b7bb1075b4b580f2ecdf2ed52f1200152`  
		Last Modified: Wed, 10 Apr 2024 05:22:12 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; arm variant v5

```console
$ docker pull adminer@sha256:0f9cb3fe315b99c52d1499b9273c0e60bc3196063549c5f616d53ec70cb576e6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91228341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bf439bd011c5295357e34e3ca9770274fec4444a76bc65b68c868ca71510c81`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 10 Apr 2024 00:49:22 GMT
ADD file:1eb31b3bcff4decb2d77374005bc7e0451f76188c3586232986a3f72e069dd04 in / 
# Wed, 10 Apr 2024 00:49:23 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:00:16 GMT
STOPSIGNAL SIGINT
# Wed, 10 Apr 2024 05:00:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:00:44 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 10 Apr 2024 05:00:45 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 10 Apr 2024 05:00:45 GMT
WORKDIR /var/www/html
# Wed, 10 Apr 2024 05:00:45 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 10 Apr 2024 05:00:45 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 10 Apr 2024 05:00:45 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 10 Apr 2024 05:00:45 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 10 Apr 2024 05:00:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 05:00:58 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 10 Apr 2024 05:00:58 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 10 Apr 2024 05:00:58 GMT
USER adminer
# Wed, 10 Apr 2024 05:00:59 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 10 Apr 2024 05:00:59 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:73e28a24bff6aad570d221d844a24c5be13f1afcd4819e3c4842ae6b4ae928ed`  
		Last Modified: Wed, 10 Apr 2024 00:54:59 GMT  
		Size: 52.6 MB (52591634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db6a4720358e2dcbaabd57f437b185f6e07b978463d243b5ef9fb2025e762e36`  
		Last Modified: Wed, 10 Apr 2024 05:01:38 GMT  
		Size: 37.2 MB (37247393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d5ccd425db6cf0e512be2eab2f5864ce06b128457b81721648151215fae6de`  
		Last Modified: Wed, 10 Apr 2024 05:01:29 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a78b73ff8276d977fed62d3e4d19544946fa6209f8761ef66257144c8ef7d012`  
		Last Modified: Wed, 10 Apr 2024 05:01:29 GMT  
		Size: 1.9 KB (1868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1211a6a0380b5037ccd4bf6ead72211a74c5a41eec1b72b781a8eecc766594`  
		Last Modified: Wed, 10 Apr 2024 05:01:29 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97c2298077484104fee9efdb1d53ab9a89b5e3990a63f8de37d7a6e3115b09b9`  
		Last Modified: Wed, 10 Apr 2024 05:01:30 GMT  
		Size: 1.4 MB (1385084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100a582806a801b09258137914fc409eeb81a81c194933e33450a9c62a09fc6f`  
		Last Modified: Wed, 10 Apr 2024 05:01:29 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:1875d1aa261df801e1e77f8d36110739aa175d12f2dd449a4e2defbd95c753fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87825305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1f094718dec25ba3e9548891d1e07a6036c47d22912dae0f372b19ec15d028e`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 10 Apr 2024 00:58:28 GMT
ADD file:eb53aade3ed19f72413045948cad3084902fe630cc20789d2c2b5bc334679575 in / 
# Wed, 10 Apr 2024 00:58:29 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:38:43 GMT
STOPSIGNAL SIGINT
# Wed, 10 Apr 2024 07:39:48 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:39:49 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 10 Apr 2024 07:39:50 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 10 Apr 2024 07:39:50 GMT
WORKDIR /var/www/html
# Wed, 10 Apr 2024 07:39:51 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 10 Apr 2024 07:39:51 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 10 Apr 2024 07:39:51 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 10 Apr 2024 07:39:51 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 10 Apr 2024 07:40:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 07:40:16 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 10 Apr 2024 07:40:17 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 10 Apr 2024 07:40:17 GMT
USER adminer
# Wed, 10 Apr 2024 07:40:17 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 10 Apr 2024 07:40:17 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:23ca580217f1a6b17dba868e7ec34ae7fff221e07640fca532510daca8ed46f6`  
		Last Modified: Wed, 10 Apr 2024 01:04:48 GMT  
		Size: 50.2 MB (50246481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c6f8bf279ebbebddc5d910bd81e8ee8eef8f191d28f0dd548fabc50b954ee5`  
		Last Modified: Wed, 10 Apr 2024 07:41:16 GMT  
		Size: 36.2 MB (36189278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49abb3144049a6b704327e8d85a193c1cc629ab93143db816139dc43127e6981`  
		Last Modified: Wed, 10 Apr 2024 07:41:06 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74f18841e6a72ac0775ff5d8bcd639ea73a0e1b66aa9fc7f4d49a869aca50f3`  
		Last Modified: Wed, 10 Apr 2024 07:41:06 GMT  
		Size: 1.9 KB (1868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b7324938ec40db674545097a9bf7f03c7553164fc40e22f0f6afad51c0ec35e`  
		Last Modified: Wed, 10 Apr 2024 07:41:06 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f357fd292cbc746ce770c59183285843488f47010e7c57ec94c0b21b1c6c664`  
		Last Modified: Wed, 10 Apr 2024 07:41:06 GMT  
		Size: 1.4 MB (1385314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38fe216fcc28a6ce43ab54e612a63f89ab82fd842ebdfec7f784e4793775ea90`  
		Last Modified: Wed, 10 Apr 2024 07:41:06 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:7b66098b701c4288cd61f1d4967a6f94e758f1a34fc5953baf47db52d6a77191
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94360351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b251b02d80004d905b4c663ea5608f57c4b677a77b2223babde46609cc1bffda`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:30 GMT
ADD file:6fedb173fe261ff0e13b004ca692b7edcc74dcc3c4384fee092b96ef9508992c in / 
# Wed, 10 Apr 2024 00:40:30 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:17:06 GMT
STOPSIGNAL SIGINT
# Wed, 10 Apr 2024 04:17:25 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:17:26 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 10 Apr 2024 04:17:27 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 10 Apr 2024 04:17:27 GMT
WORKDIR /var/www/html
# Wed, 10 Apr 2024 04:17:27 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 10 Apr 2024 04:17:27 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 10 Apr 2024 04:17:27 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 10 Apr 2024 04:17:27 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 10 Apr 2024 04:17:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 04:17:38 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 10 Apr 2024 04:17:38 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 10 Apr 2024 04:17:38 GMT
USER adminer
# Wed, 10 Apr 2024 04:17:38 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 10 Apr 2024 04:17:38 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:197947a07d5f6c6ff020ca65dcea4e52671f85f67bee1b59af46cb0dc36580d9`  
		Last Modified: Wed, 10 Apr 2024 00:44:24 GMT  
		Size: 53.7 MB (53729176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87309044ed7dad762cb5b0c59410e017714c6e8a2426f1824765e787d5c4d004`  
		Last Modified: Wed, 10 Apr 2024 04:18:08 GMT  
		Size: 39.2 MB (39241798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ba919f6d13ea8467192a77457026ebaeafbafb1894c53ae0df7432ee3f1cfa`  
		Last Modified: Wed, 10 Apr 2024 04:18:02 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443744a65b6c59b42bad9299bc33b8d4168ae275e941914fa94a737ec4dc9dea`  
		Last Modified: Wed, 10 Apr 2024 04:18:02 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d532fdaa843c5adf35ddd4b4a6e659d301c74fb508b570edda27d0d3956a918`  
		Last Modified: Wed, 10 Apr 2024 04:18:02 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40766e87774ef8d97cbf7e44eb405a9756652b9021d6093e21e11cebc21bdaed`  
		Last Modified: Wed, 10 Apr 2024 04:18:02 GMT  
		Size: 1.4 MB (1385129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cbc7b28cef1e3732f9caefc680bb1c49fccb9267104989634757bcfc8e296b`  
		Last Modified: Wed, 10 Apr 2024 04:18:02 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; 386

```console
$ docker pull adminer@sha256:b2cbb3589885400eafa20ced11368ce884ef451acf11a4eb36e07940c028843a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (97013064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f45b19a728a195dbe7be6a8b1743be717e0590b74127ed434b824eedcb209b1`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 10 Apr 2024 00:57:22 GMT
ADD file:34b6b0eca66bdded42723d3cb7b488ca726fedb7fd2a42c047e2790ccf93f08b in / 
# Wed, 10 Apr 2024 00:57:23 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:50:18 GMT
STOPSIGNAL SIGINT
# Wed, 10 Apr 2024 07:50:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:50:50 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 10 Apr 2024 07:50:51 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 10 Apr 2024 07:50:51 GMT
WORKDIR /var/www/html
# Wed, 10 Apr 2024 07:50:51 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 10 Apr 2024 07:50:52 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 10 Apr 2024 07:50:52 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 10 Apr 2024 07:50:52 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 10 Apr 2024 07:51:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 07:51:06 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 10 Apr 2024 07:51:06 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 10 Apr 2024 07:51:06 GMT
USER adminer
# Wed, 10 Apr 2024 07:51:06 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 10 Apr 2024 07:51:06 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:1dc10b34406db63eacc8d006ba4d0103014a3a863134cdfe43622d4706753fa7`  
		Last Modified: Wed, 10 Apr 2024 01:02:27 GMT  
		Size: 56.1 MB (56066188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ffae7771047c7bdc607ca31435c9c6009b3bd44bcdfcb17c534b0466402254`  
		Last Modified: Wed, 10 Apr 2024 07:51:55 GMT  
		Size: 39.6 MB (39557486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad6b4c4b7317ca3d6a7d48946da857bf7741671dec26f292d5b2b9aa194029d`  
		Last Modified: Wed, 10 Apr 2024 07:51:44 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddef67e361c689422d3a05c9953b30907f2442d1213bf4977d7813165483151`  
		Last Modified: Wed, 10 Apr 2024 07:51:44 GMT  
		Size: 1.9 KB (1869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e16422457b6d6ec572c9e56865cef2faaef23bcab5a1bd04d1104eb923f4da8`  
		Last Modified: Wed, 10 Apr 2024 07:51:43 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f816e32ec7346a634c0e1f6b64d92553691aace865dbda4c7165148133e6f96c`  
		Last Modified: Wed, 10 Apr 2024 07:51:44 GMT  
		Size: 1.4 MB (1385160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1bd8d6d37ffa9d42a82941f82ed6704fa31875c4e881f74781546c8656f0372`  
		Last Modified: Wed, 10 Apr 2024 07:51:43 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; mips64le

```console
$ docker pull adminer@sha256:dc9ad28daed35a5b5ef563f94e91664009c738a13ee9169df173bf93445aa110
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92653161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62b79d1ddd52100f2ac1f305213f8cf45477c3618012d29fe84e99474239297c`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 10 Apr 2024 01:10:45 GMT
ADD file:b9ae0499407c5db6a4d213452b2b485d2f0c9fae0792c77a629177988969faa3 in / 
# Wed, 10 Apr 2024 01:10:52 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 02:39:09 GMT
STOPSIGNAL SIGINT
# Wed, 10 Apr 2024 02:41:05 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 02:41:11 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 10 Apr 2024 02:41:18 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 10 Apr 2024 02:41:22 GMT
WORKDIR /var/www/html
# Wed, 10 Apr 2024 02:41:25 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 10 Apr 2024 02:41:28 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 10 Apr 2024 02:41:31 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 10 Apr 2024 02:41:35 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 10 Apr 2024 02:42:26 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 02:42:29 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 10 Apr 2024 02:42:32 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 10 Apr 2024 02:42:36 GMT
USER adminer
# Wed, 10 Apr 2024 02:42:39 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 10 Apr 2024 02:42:43 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:eade21836c93150a05690be18ba07f9d56297d4f2b59f348647ec05e7c1435cc`  
		Last Modified: Wed, 10 Apr 2024 01:22:42 GMT  
		Size: 53.3 MB (53309804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd1902d9e940ca4f985ab4b15d03c10c1c41e25341e2d799d6377bd84fdf46b`  
		Last Modified: Wed, 10 Apr 2024 02:45:11 GMT  
		Size: 38.0 MB (37953054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfea05f8b6b2a727cf803190d314cfe081a05dc3c761b172fa1ed2fe9f796545`  
		Last Modified: Wed, 10 Apr 2024 02:44:44 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764e1676e4c5fd49d420288450dcb8005826fd8aa7444dba2606c551c5757a4e`  
		Last Modified: Wed, 10 Apr 2024 02:44:44 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4055216153022814d1fc92382438d7a435bb922fbc98e65ebf0fcc8ca7f5ce`  
		Last Modified: Wed, 10 Apr 2024 02:44:45 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2239f6ac05f686d4f5e4fcd85217b38a462a4dd4d1276544471694a38c8ee9dc`  
		Last Modified: Wed, 10 Apr 2024 02:44:45 GMT  
		Size: 1.4 MB (1386193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a7ee10ebd61983ec9f2bfd09957a7ae82fe39a3324e1d63cbd4f13745de165`  
		Last Modified: Wed, 10 Apr 2024 02:44:44 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:68aa731eaa6e6d92d50a34044b8faadc308c5be746324e2f7e1fad23c04f546d
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101292444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0725ee97ca1c61da4f001c20b4359a22cecffca4c0dd282701589b63a2dd6f0`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 10 Apr 2024 01:26:45 GMT
ADD file:774dc7f7db45435bfddcc1ff7bb4ae0716252e8f7c3d074ff7611070207b8314 in / 
# Wed, 10 Apr 2024 01:26:48 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:24:30 GMT
STOPSIGNAL SIGINT
# Wed, 10 Apr 2024 06:25:28 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:25:31 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 10 Apr 2024 06:25:33 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 10 Apr 2024 06:25:33 GMT
WORKDIR /var/www/html
# Wed, 10 Apr 2024 06:25:34 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 10 Apr 2024 06:25:34 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 10 Apr 2024 06:25:35 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 10 Apr 2024 06:25:35 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 10 Apr 2024 06:26:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 06:26:03 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 10 Apr 2024 06:26:03 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 10 Apr 2024 06:26:03 GMT
USER adminer
# Wed, 10 Apr 2024 06:26:04 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 10 Apr 2024 06:26:05 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:eed533dbdbda3df66dcde8a75fb0ab317466f575d116ffa4e053da66ab0dd942`  
		Last Modified: Wed, 10 Apr 2024 01:31:35 GMT  
		Size: 59.0 MB (58959030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26552f5d2351a0c45d5b9744e57abd1dd0261a30c9400736773c5efa076e4bf2`  
		Last Modified: Wed, 10 Apr 2024 06:27:16 GMT  
		Size: 40.9 MB (40943678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c3f35c0eb0724fbc0e7790d15b7827abb3336e5c39db17ac6020a449fffa84f`  
		Last Modified: Wed, 10 Apr 2024 06:27:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac2d1cbe290baa3f42515ed639120a7b65f7c081c7a66d81fefc5cc58f79a19`  
		Last Modified: Wed, 10 Apr 2024 06:27:06 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567216cb4907017f73326c032b9cd19dd0a4b7286c609569bdda630d2957f702`  
		Last Modified: Wed, 10 Apr 2024 06:27:06 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d2de9025eac46f7f04efac02e8aa2e2b1a2e91ad401633959848763416908f9`  
		Last Modified: Wed, 10 Apr 2024 06:27:07 GMT  
		Size: 1.4 MB (1385484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb8f8f7681f70e94d03aff37f7e1227f6618dc48576ee62ee0ebe06f4d31f3b`  
		Last Modified: Wed, 10 Apr 2024 06:27:06 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; s390x

```console
$ docker pull adminer@sha256:59b3a8210186c94969c67273356bbeb74277a39ffbf5df2e4f260060ac4e06f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93739411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0425f6bfc73b8c4a35777f8b972496c2330d5331ac8c4e150e2c4eec6dc0ffb5`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 10 Apr 2024 01:16:37 GMT
ADD file:ca4cd0bb2344426b8777da3ac3278e42efb1e15064ff144111d7ecacdf3cbd4a in / 
# Wed, 10 Apr 2024 01:16:44 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:42:57 GMT
STOPSIGNAL SIGINT
# Wed, 10 Apr 2024 06:43:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:43:19 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 10 Apr 2024 06:43:20 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 10 Apr 2024 06:43:20 GMT
WORKDIR /var/www/html
# Wed, 10 Apr 2024 06:43:20 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 10 Apr 2024 06:43:20 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 10 Apr 2024 06:43:20 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 10 Apr 2024 06:43:20 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 10 Apr 2024 06:43:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 10 Apr 2024 06:43:30 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 10 Apr 2024 06:43:30 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 10 Apr 2024 06:43:30 GMT
USER adminer
# Wed, 10 Apr 2024 06:43:30 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 10 Apr 2024 06:43:30 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:8d59905935c60c8e62d2bce55ff58a911d9ceda48b95f8209712af92b63b5ceb`  
		Last Modified: Wed, 10 Apr 2024 01:48:44 GMT  
		Size: 53.3 MB (53324935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee66275d019cbf865f8b0dac2bbdab8a69561a689e26211dcf277bf0f1e923e4`  
		Last Modified: Wed, 10 Apr 2024 06:46:08 GMT  
		Size: 39.0 MB (39025068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34bc558ce9db86b1083de56e39b582232e90b98f234a54087d6760e9c15b58a`  
		Last Modified: Wed, 10 Apr 2024 06:46:01 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e449b0fa9b7b32ea80fe221a58bed2a15b28110991ac349bbfb59faebd00d0a`  
		Last Modified: Wed, 10 Apr 2024 06:46:01 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bacb0da8da68a8cbc2b8bd4f913cb7a39c1731459de20d426803e0324187ae`  
		Last Modified: Wed, 10 Apr 2024 06:46:01 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ec27ab49df9b088fe36537395875cd26e2d23b588cc644b3783fa04941b92b`  
		Last Modified: Wed, 10 Apr 2024 06:46:01 GMT  
		Size: 1.4 MB (1385167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be36f2400841c415497b25e4acb056a976b4999b20145692d25bfa97c27ee2e0`  
		Last Modified: Wed, 10 Apr 2024 06:46:01 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
