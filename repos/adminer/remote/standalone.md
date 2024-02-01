## `adminer:standalone`

```console
$ docker pull adminer@sha256:e6016420357dd7889ad127265cdbde2c535ae28517958e93ac31a097c5953101
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
$ docker pull adminer@sha256:0d84fb86f1a1d7b20b6d94a23c379e71b77a36920321d662077516c514d582c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95940560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a66230741737b26aab4daca8ad25bb7f3e5f69ecc9de193615c7a36725a18038`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:29 GMT
ADD file:4fa73c8d113df02c8656b74ab87563432215332f3de78446a02e5ab7d6e2ab7a in / 
# Wed, 31 Jan 2024 22:35:29 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:43:06 GMT
STOPSIGNAL SIGINT
# Thu, 01 Feb 2024 06:43:26 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 06:43:26 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 01 Feb 2024 06:43:27 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 01 Feb 2024 06:43:27 GMT
WORKDIR /var/www/html
# Thu, 01 Feb 2024 06:43:27 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 01 Feb 2024 06:43:27 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 01 Feb 2024 06:43:27 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 01 Feb 2024 06:43:27 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 01 Feb 2024 06:43:38 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 01 Feb 2024 06:43:39 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 01 Feb 2024 06:43:39 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 01 Feb 2024 06:43:39 GMT
USER adminer
# Thu, 01 Feb 2024 06:43:39 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 01 Feb 2024 06:43:39 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:7faaa42ac0c18c9baf539c97a5c8f042d02a77b05380cb57759e4407385710dc`  
		Last Modified: Wed, 31 Jan 2024 22:40:15 GMT  
		Size: 55.1 MB (55056963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1e2d8c87a53c173980fa6d2e4225188a6e89c0b08c5dee0d60b25ed1d8f78cc`  
		Last Modified: Thu, 01 Feb 2024 06:44:20 GMT  
		Size: 39.5 MB (39492989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecd63f4061c27d7cf320c825fc0a016fcf185031bc9b3226210743119f15ea57`  
		Last Modified: Thu, 01 Feb 2024 06:44:13 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed2c0a9cc37c8c74644e6599d405734e48512d2f0944be6e63d2f1555e2524e`  
		Last Modified: Thu, 01 Feb 2024 06:44:13 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3fce535d3cc486b0b94f76462e3c9ba56a34b892d3e94cb9826c33883fd78c0`  
		Last Modified: Thu, 01 Feb 2024 06:44:13 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9b6dabfbc2d56260397f702418af5569dbcb53f1ecd978e26b1c2445919757`  
		Last Modified: Thu, 01 Feb 2024 06:44:13 GMT  
		Size: 1.4 MB (1386374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab8ef174e317343a1b6a2d825aa6c3a0b795b87604f720194dd57d0752d94dc`  
		Last Modified: Thu, 01 Feb 2024 06:44:13 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; arm variant v5

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

### `adminer:standalone` - linux; arm variant v7

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

### `adminer:standalone` - linux; arm64 variant v8

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

### `adminer:standalone` - linux; 386

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

### `adminer:standalone` - linux; mips64le

```console
$ docker pull adminer@sha256:881247a12cc715d788538af544c27ab3ad9d5b231b8134142cfc83078da0c50b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92634406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:224946899f742621020eabc4c768599867c967ef996cbbeb4ced552f0af89d25`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 31 Jan 2024 22:27:47 GMT
ADD file:646762dde2578506254f2b52895972c76193565971632fabb304bfd0d84e4301 in / 
# Wed, 31 Jan 2024 22:27:53 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 07:00:21 GMT
STOPSIGNAL SIGINT
# Thu, 01 Feb 2024 07:02:14 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:02:21 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 01 Feb 2024 07:02:28 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 01 Feb 2024 07:02:31 GMT
WORKDIR /var/www/html
# Thu, 01 Feb 2024 07:02:34 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 01 Feb 2024 07:02:37 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 01 Feb 2024 07:02:41 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 01 Feb 2024 07:02:44 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 01 Feb 2024 07:03:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 01 Feb 2024 07:03:39 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 01 Feb 2024 07:03:42 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 01 Feb 2024 07:03:45 GMT
USER adminer
# Thu, 01 Feb 2024 07:03:49 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 01 Feb 2024 07:03:52 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:c1282b8885af09f8f21ef0080afd2b77263b28d997ded5c3e116452fb071674d`  
		Last Modified: Wed, 31 Jan 2024 22:39:06 GMT  
		Size: 53.3 MB (53289105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22bc3eb28207e1bf292199c5cd7bfc2a78eed869efa35a203eb05641f1d6ed2c`  
		Last Modified: Thu, 01 Feb 2024 07:06:23 GMT  
		Size: 38.0 MB (37954036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9577f85887f91bbc6aeec092d9ca6ea8d50b8a06dc1e6d3a9497bfe68d90d3`  
		Last Modified: Thu, 01 Feb 2024 07:05:56 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab0f3d96c9fa50eab0bef974f91a4d167259af57e8ecb33ad8425c260b79acf`  
		Last Modified: Thu, 01 Feb 2024 07:05:56 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cdbf6212d226b682731b04025612c25b6b286a78069d09bad3529e20f7eaba1`  
		Last Modified: Thu, 01 Feb 2024 07:05:57 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dcc028a9b057e6647d70c73576507174b96aea97b57644a43f3fa67a56d4fa3`  
		Last Modified: Thu, 01 Feb 2024 07:05:57 GMT  
		Size: 1.4 MB (1387172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b26ed8a53b4871adf9a9f822ee6a03c10d99e4e44b4697782d0350d6d06ab4bf`  
		Last Modified: Thu, 01 Feb 2024 07:05:56 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; ppc64le

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

### `adminer:standalone` - linux; s390x

```console
$ docker pull adminer@sha256:84aa0cbc223ad1302a83d2409f2e14f407a8a74cf5906c1d8d240f9447ef24d5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93708339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7707ac4d4de19d013eb2bf16ea4e8c01080896844d769a6f33053e21202d80c`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 31 Jan 2024 23:00:14 GMT
ADD file:dabd3f74723e205f5c7918d395104495ae736b6dea76f8e097cea5fecfb5afb1 in / 
# Wed, 31 Jan 2024 23:00:18 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 06:27:59 GMT
STOPSIGNAL SIGINT
# Thu, 01 Feb 2024 06:29:07 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 06:29:17 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 01 Feb 2024 06:29:19 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 01 Feb 2024 06:29:20 GMT
WORKDIR /var/www/html
# Thu, 01 Feb 2024 06:29:21 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 01 Feb 2024 06:29:21 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 01 Feb 2024 06:29:22 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 01 Feb 2024 06:29:22 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 01 Feb 2024 06:29:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 01 Feb 2024 06:29:52 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 01 Feb 2024 06:29:52 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 01 Feb 2024 06:29:53 GMT
USER adminer
# Thu, 01 Feb 2024 06:29:54 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 01 Feb 2024 06:29:55 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:7014cd04a53b5809417ad8478246286af7c09e19b05597a0f119e96f7e859b1f`  
		Last Modified: Wed, 31 Jan 2024 23:29:24 GMT  
		Size: 53.3 MB (53294682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088d9551934693762adba509f0bd73dcf7e8b00756756458110417f3dee3de5b`  
		Last Modified: Thu, 01 Feb 2024 06:33:20 GMT  
		Size: 39.0 MB (39022871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec218d40ba0e902548d839299bb16e04d1a863b06d238985ae871b121c42eaa`  
		Last Modified: Thu, 01 Feb 2024 06:33:13 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e97fb0f3e03207afecab59f2356f0ebeff3a4d012c02bc01df05a63479b0eb`  
		Last Modified: Thu, 01 Feb 2024 06:33:13 GMT  
		Size: 1.9 KB (1890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c87c8641974135dbb91b9eb8d577d52ace2bac61764a30602ed107dcfe3a80fe`  
		Last Modified: Thu, 01 Feb 2024 06:33:13 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d61b76093e3108d25460ebf8fb8bcd3331a473dace3785f3f7b2fa34f70fc8`  
		Last Modified: Thu, 01 Feb 2024 06:33:13 GMT  
		Size: 1.4 MB (1386530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b6e80a545919f83283fef15565a6bc30e051e5459eee36c0d33600abcaf751`  
		Last Modified: Thu, 01 Feb 2024 06:33:13 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
