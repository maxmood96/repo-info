## `adminer:latest`

```console
$ docker pull adminer@sha256:b296751fea88b25888499392deabc8ff884c509ecdeeec1282ed4f2755923385
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
$ docker pull adminer@sha256:6c2a4bac611e933e9ac318592d6caa7c4d4895a2ef1acec9383288844c6b7c6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95942081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3b195a8d7922d460ebcfd81eb1e073dbe520b22309013628baed8ce61d0b3c`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Thu, 11 Jan 2024 04:30:29 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 11 Jan 2024 04:30:29 GMT
WORKDIR /var/www/html
# Thu, 11 Jan 2024 04:30:30 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 11 Jan 2024 04:30:30 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 11 Jan 2024 04:30:30 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 11 Jan 2024 04:30:30 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 11 Jan 2024 04:30:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 04:30:41 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 11 Jan 2024 04:30:42 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 11 Jan 2024 04:30:42 GMT
USER adminer
# Thu, 11 Jan 2024 04:30:42 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 11 Jan 2024 04:30:42 GMT
EXPOSE 8080
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
	-	`sha256:f54e1b456a9191b4fe1afc2f9b6cd311791ae16c145f56342f1a9dcdc3c64cda`  
		Last Modified: Thu, 11 Jan 2024 04:31:13 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce56aa1add831136c91e53265c2466e6b7646e597dc379b60bfea1da52b48b81`  
		Last Modified: Thu, 11 Jan 2024 04:31:13 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295fc39699fb570a034336fb459423e3a7eca49213b83e357ce95def703477e1`  
		Last Modified: Thu, 11 Jan 2024 04:31:14 GMT  
		Size: 1.4 MB (1386421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac6b3fb3f9dbd30e52ede17b156b08f370ea6b99dd67885a14a8bb2aaa579ac6`  
		Last Modified: Thu, 11 Jan 2024 04:31:13 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; arm variant v5

```console
$ docker pull adminer@sha256:bfc5454a4fdd6972a466494a7a5af0a13ddebae467a4dda0d434b18477d923fa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91203885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1652d6aa00408ef59372627881fb322336da8e41fb051458857db3886ce22ac6`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:29 GMT
ADD file:b3de5afb7e9c6d6d7f3bca38d87575a8f510b9eb6ee1aca78b37cd5792f6cd3d in / 
# Wed, 31 Jan 2024 22:44:31 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:08:49 GMT
STOPSIGNAL SIGINT
# Wed, 31 Jan 2024 23:09:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:09:24 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 31 Jan 2024 23:09:24 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 31 Jan 2024 23:09:24 GMT
WORKDIR /var/www/html
# Wed, 31 Jan 2024 23:09:24 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 31 Jan 2024 23:09:25 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 31 Jan 2024 23:09:25 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 31 Jan 2024 23:09:25 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 31 Jan 2024 23:09:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 31 Jan 2024 23:09:41 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 31 Jan 2024 23:09:42 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 31 Jan 2024 23:09:42 GMT
USER adminer
# Wed, 31 Jan 2024 23:09:42 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 31 Jan 2024 23:09:42 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:3613d41e91f9f86b71a10338dcfe412e314cd29bee2d9674a0b53f59989b5a42`  
		Last Modified: Wed, 31 Jan 2024 22:48:22 GMT  
		Size: 52.6 MB (52560866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f998995de3a21d1d4bbbf96164d94dec1f79792407d6432c1a87e0efbed21f60`  
		Last Modified: Wed, 31 Jan 2024 23:10:24 GMT  
		Size: 37.3 MB (37252499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6714e922b85f20486e6b8d3ff6e8eb489a55a946e43d9a0998499351f76522f8`  
		Last Modified: Wed, 31 Jan 2024 23:10:15 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151dbd50db992ee4315f81a219009d63157a02e0ea056b4d44923e0e6e51b2d0`  
		Last Modified: Wed, 31 Jan 2024 23:10:15 GMT  
		Size: 1.9 KB (1869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76da4830c6ccc67089893f3bd9cb0fad40346cb0d616851317e303c89c22ff13`  
		Last Modified: Wed, 31 Jan 2024 23:10:15 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db861dd56596d5fa1d541c6192e585b5ffb882cb27286194946b6ac56e49bafd`  
		Last Modified: Wed, 31 Jan 2024 23:10:16 GMT  
		Size: 1.4 MB (1386294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8852f4fe80e0b24cd39943db1bd84a10674f2a49cc1cd2a346c9932376ce81ea`  
		Last Modified: Wed, 31 Jan 2024 23:10:15 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; arm variant v7

```console
$ docker pull adminer@sha256:a6a18ec2bb6c5f395cbb39dfdb72448c3837682571b328dc077460ac548f21de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87797612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:322856d125c49762ab000fac593bc6b8cab3c7164e2be74dea54b6c9c7437cc7`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:31 GMT
ADD file:7a3ca444fa582cdedade49cd6262ee982b6da86eafe22b1b77326c8eab3f88cf in / 
# Wed, 31 Jan 2024 22:44:31 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:11:27 GMT
STOPSIGNAL SIGINT
# Wed, 31 Jan 2024 23:12:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:12:07 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 31 Jan 2024 23:12:07 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 31 Jan 2024 23:12:07 GMT
WORKDIR /var/www/html
# Wed, 31 Jan 2024 23:12:08 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 31 Jan 2024 23:12:08 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 31 Jan 2024 23:12:08 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 31 Jan 2024 23:12:08 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 31 Jan 2024 23:12:20 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 31 Jan 2024 23:12:20 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 31 Jan 2024 23:12:20 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 31 Jan 2024 23:12:20 GMT
USER adminer
# Wed, 31 Jan 2024 23:12:20 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 31 Jan 2024 23:12:21 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:413453d204f637339c7a4727b614537000709bb2ff00a6307e262cf37237761c`  
		Last Modified: Wed, 31 Jan 2024 22:49:12 GMT  
		Size: 50.2 MB (50216178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577e712ec62291b178dfc6bb01dff5324b100194a041b8709982ff1db3d0d731`  
		Last Modified: Wed, 31 Jan 2024 23:13:02 GMT  
		Size: 36.2 MB (36190840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54442ed6f1ce45c47a270c4dcd71c1dd0fb13a21e6155cf766338913496f006`  
		Last Modified: Wed, 31 Jan 2024 23:12:53 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6744128e35fc68592b4aebd1cef6694931a09e2ac009878b0d265cbb3626c720`  
		Last Modified: Wed, 31 Jan 2024 23:12:53 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c30adc849538faaf014cf296a892a9e4237442a2a2ce85fd69f5922076ba4f58`  
		Last Modified: Wed, 31 Jan 2024 23:12:53 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffbb08061ab32b6bb559b0f01dd66f7368137ff3723b09206baf5f27c10745c`  
		Last Modified: Wed, 31 Jan 2024 23:12:53 GMT  
		Size: 1.4 MB (1386359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7355f2ca4f285e8947359c71eead004a7b120266b67551b2ea71cc2323a01a4b`  
		Last Modified: Wed, 31 Jan 2024 23:12:53 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:4e13979f7393db461fbc935f80f984ba0bdf1c876bbb669af216a2426f9ab5a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94346544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6458ce3446a1be2c158bc904302de57eda5b1e4d3f249d65bab50b44833364c`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:33 GMT
ADD file:81cb49e646b9feb1ddeddea1cb6dbafa672a250f1553cc28eae09c955607236d in / 
# Wed, 31 Jan 2024 22:44:34 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:39:31 GMT
STOPSIGNAL SIGINT
# Wed, 31 Jan 2024 23:39:50 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:39:51 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 31 Jan 2024 23:39:51 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 31 Jan 2024 23:39:51 GMT
WORKDIR /var/www/html
# Wed, 31 Jan 2024 23:39:52 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 31 Jan 2024 23:39:52 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 31 Jan 2024 23:39:52 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 31 Jan 2024 23:39:52 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 31 Jan 2024 23:40:03 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 31 Jan 2024 23:40:03 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 31 Jan 2024 23:40:03 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 31 Jan 2024 23:40:03 GMT
USER adminer
# Wed, 31 Jan 2024 23:40:04 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 31 Jan 2024 23:40:04 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:4b6eb2d0256d18652f84fd30c1db34ce9462e535a2d96fbf2f9044db000b13f5`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 53.7 MB (53708267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dcab4611e6e9bc9e76b5ddbbd81ca3baf5cb70814fe1b34df87eef73bb63bca`  
		Last Modified: Wed, 31 Jan 2024 23:40:40 GMT  
		Size: 39.2 MB (39247761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b10547e981deceb63a9bf920fbdd4ddc5277c4be1fb51b6639d50a3aa87c49`  
		Last Modified: Wed, 31 Jan 2024 23:40:33 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db8c2b2093440c652493011f5c94fdb1c3cf297085b7ec3dc8ce61c203d801a4`  
		Last Modified: Wed, 31 Jan 2024 23:40:33 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1aecf328e7a80dd27ab86232950cc806fb9b47350af0e69ae1af7cedb5c1c78`  
		Last Modified: Wed, 31 Jan 2024 23:40:33 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32e83238d2d1f63d96633cd58238261fdd559577633baf593a54b3db3d911cc`  
		Last Modified: Wed, 31 Jan 2024 23:40:34 GMT  
		Size: 1.4 MB (1386276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44bb1b2f1456533f5fb758f02d57345699e1cf634209503bec4d482a71137ebd`  
		Last Modified: Wed, 31 Jan 2024 23:40:33 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; 386

```console
$ docker pull adminer@sha256:74ad6a6371ddf83ef8948031bff2827631de11825a87e1aaf5bbaf5492c9dc8f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96999039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:858bcf7c05e972ec708c13306c71b455fc6c58109636c500d5b45467fd31c101`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 31 Jan 2024 22:39:11 GMT
ADD file:52ba8552e4cd0d950c9eb8ab6bf54413f34e4ef697dc4ae766a04f22b7ea1a38 in / 
# Wed, 31 Jan 2024 22:39:12 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:30:07 GMT
STOPSIGNAL SIGINT
# Wed, 31 Jan 2024 23:30:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:30:36 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 31 Jan 2024 23:30:37 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 31 Jan 2024 23:30:37 GMT
WORKDIR /var/www/html
# Wed, 31 Jan 2024 23:30:37 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 31 Jan 2024 23:30:37 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 31 Jan 2024 23:30:37 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 31 Jan 2024 23:30:38 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 31 Jan 2024 23:30:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 31 Jan 2024 23:30:53 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 31 Jan 2024 23:30:53 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 31 Jan 2024 23:30:53 GMT
USER adminer
# Wed, 31 Jan 2024 23:30:53 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 31 Jan 2024 23:30:54 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:3f04d4a4d4fa39eba128eb2d49424bb31d43a6258c318d2547e85c723fd692f7`  
		Last Modified: Wed, 31 Jan 2024 22:44:11 GMT  
		Size: 56.0 MB (56046343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d4ecf6f18b7a964fc4e63682e235e525f211c9354daee63d8dc0215ac72226`  
		Last Modified: Wed, 31 Jan 2024 23:31:42 GMT  
		Size: 39.6 MB (39562123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c6aabf89d7ccb5293d3778c260fc21aed536ad4c1b890eaa69b8da851b7cf6f`  
		Last Modified: Wed, 31 Jan 2024 23:31:31 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bcee8d359b169e740ddfe05d12e08dead15538e8082b4210f0a6975ce240b46`  
		Last Modified: Wed, 31 Jan 2024 23:31:31 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2acd255ed593f931f4461db4fdb539f88092a1f749e3a78ec4878e9915b5be`  
		Last Modified: Wed, 31 Jan 2024 23:31:31 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e34f96ce2e350db55cc0a7852e46f32526cab3d1a5e7804413554fdb15129a`  
		Last Modified: Wed, 31 Jan 2024 23:31:31 GMT  
		Size: 1.4 MB (1386338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d7155c5b6a63ddd1c583acefa92672d87938500484d8d1aded02b081926d95b`  
		Last Modified: Wed, 31 Jan 2024 23:31:31 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; mips64le

```console
$ docker pull adminer@sha256:2d8bacc623549ee1f4de8c69f5adb3651eba0dba33d684c8dd1bd566e505bd56
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92634168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa20824de4d301aa8314f13e1ead6e06e5c89021a6c1788925877dfe0d649efb`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Thu, 11 Jan 2024 03:40:57 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 11 Jan 2024 03:41:00 GMT
WORKDIR /var/www/html
# Thu, 11 Jan 2024 03:41:04 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 11 Jan 2024 03:41:07 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 11 Jan 2024 03:41:10 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 11 Jan 2024 03:41:14 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 11 Jan 2024 03:42:05 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 03:42:08 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 11 Jan 2024 03:42:11 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 11 Jan 2024 03:42:14 GMT
USER adminer
# Thu, 11 Jan 2024 03:42:18 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 11 Jan 2024 03:42:21 GMT
EXPOSE 8080
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
	-	`sha256:b7264b5e4909a7afe28700e2106e27f957588a5a7be228a074fcc77d0775f493`  
		Last Modified: Thu, 11 Jan 2024 03:44:23 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f20dd4cea35b39537006934065f29c5dabe39cf35d8736b826177d6b69245b`  
		Last Modified: Thu, 11 Jan 2024 03:44:23 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042bdb00dd813542ae29c45bf43115af193d42ed14edc55b7c5a4a79a7fec844`  
		Last Modified: Thu, 11 Jan 2024 03:44:24 GMT  
		Size: 1.4 MB (1387146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cdac192e1f82eb79737a12efbb967356719be1e696fc114dc02886713d2f40`  
		Last Modified: Thu, 11 Jan 2024 03:44:23 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; ppc64le

```console
$ docker pull adminer@sha256:2416329bb917c3c985412304acc186ba963c5799ebd88e645b82ab77c7207dda
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101266485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e405a1736be59126707cd565ecfbf04e2bfc69094e4b7e325d5c8d19d3f75a`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 31 Jan 2024 22:29:53 GMT
ADD file:feff7236892a5ed9be64b73bb7748b1b8017599aad443cae41dfdc07dce2bb8e in / 
# Wed, 31 Jan 2024 22:29:57 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:21:47 GMT
STOPSIGNAL SIGINT
# Wed, 31 Jan 2024 23:22:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:23:02 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 31 Jan 2024 23:23:04 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 31 Jan 2024 23:23:05 GMT
WORKDIR /var/www/html
# Wed, 31 Jan 2024 23:23:06 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 31 Jan 2024 23:23:06 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 31 Jan 2024 23:23:07 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 31 Jan 2024 23:23:07 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 31 Jan 2024 23:23:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 31 Jan 2024 23:23:38 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 31 Jan 2024 23:23:39 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 31 Jan 2024 23:23:40 GMT
USER adminer
# Wed, 31 Jan 2024 23:23:41 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 31 Jan 2024 23:23:41 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:59e847189f64174916c93398cc517f0b07c2a03b89a56fc88a1216415420047a`  
		Last Modified: Wed, 31 Jan 2024 22:34:47 GMT  
		Size: 58.9 MB (58930288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab16b2511b1aec10e19d3b025e04e40ab7686e557c54a23ca300869bca96b950`  
		Last Modified: Wed, 31 Jan 2024 23:24:55 GMT  
		Size: 40.9 MB (40945422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f7dbfd37860ae7b3392d342df05d678c10f5065d58a5049b9831438df39536`  
		Last Modified: Wed, 31 Jan 2024 23:24:46 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e38eeda6e9d50856f3b30e934836855f8d897051fa3bc2f0f2037461657a4d1`  
		Last Modified: Wed, 31 Jan 2024 23:24:46 GMT  
		Size: 1.9 KB (1890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55bd0916a40a05396754180e1901e83215f660de3cad94e645292ad490d954a4`  
		Last Modified: Wed, 31 Jan 2024 23:24:46 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cbc2100c44b8569d3794ea8f5b2866971f3030260d5695c8985479790e714f`  
		Last Modified: Wed, 31 Jan 2024 23:24:47 GMT  
		Size: 1.4 MB (1386514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4771e85ca6aa3c0953106cd09085a3b452133400afc05dc4fd381dabb4076898`  
		Last Modified: Wed, 31 Jan 2024 23:24:46 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; s390x

```console
$ docker pull adminer@sha256:14640da939f095a6013910724845601e03c815cf3ab24ddc06d0d1278b3a6e1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93709060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c0c44d78abc099ded346669710bce42236420ba351ae0f10ee4dde0943e8009`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Thu, 11 Jan 2024 05:11:54 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 11 Jan 2024 05:11:54 GMT
WORKDIR /var/www/html
# Thu, 11 Jan 2024 05:11:54 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 11 Jan 2024 05:11:54 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 11 Jan 2024 05:11:55 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 11 Jan 2024 05:11:55 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 11 Jan 2024 05:12:04 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 05:12:04 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 11 Jan 2024 05:12:05 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 11 Jan 2024 05:12:05 GMT
USER adminer
# Thu, 11 Jan 2024 05:12:05 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 11 Jan 2024 05:12:05 GMT
EXPOSE 8080
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
	-	`sha256:5a521e7f86e9b89edcb437c2602639541e088f7707e33672cb3a858ef3748240`  
		Last Modified: Thu, 11 Jan 2024 05:12:47 GMT  
		Size: 1.9 KB (1877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5902f96db2fe4197d888e5e4192272e4e04adb2851ebfe3a7f6df8ea8f3d0b8`  
		Last Modified: Thu, 11 Jan 2024 05:12:46 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9ef3dde1ff95bc8585448f3ca6952f6822ee5cc64f1c95f0b1e207d63ea8fd4`  
		Last Modified: Thu, 11 Jan 2024 05:12:47 GMT  
		Size: 1.4 MB (1386454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aef7970d31ff0f80b7f7c205a2cfed1e2e3149deefcf77adae73f88cbca247a`  
		Last Modified: Thu, 11 Jan 2024 05:12:46 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
