## `adminer:standalone`

```console
$ docker pull adminer@sha256:16d5b637e94d2e3206c531d0dc22207467dc1160c071d4d75c64b7ccee08f360
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

### `adminer:standalone` - linux; arm variant v5

```console
$ docker pull adminer@sha256:16ab9de2e7e16fc6cdf304477c141f0849e8a5928e3f190a182b6a3cb1b4dafd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91206140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58fbe6c9b61953645d31f5c37535e56ed082c35f98c5641d9cb6a781b7beaa01`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Thu, 11 Jan 2024 06:47:41 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 11 Jan 2024 06:47:42 GMT
WORKDIR /var/www/html
# Thu, 11 Jan 2024 06:47:42 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 11 Jan 2024 06:47:42 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 11 Jan 2024 06:47:42 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 11 Jan 2024 06:47:43 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 11 Jan 2024 06:48:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 06:48:10 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 11 Jan 2024 06:48:10 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 11 Jan 2024 06:48:10 GMT
USER adminer
# Thu, 11 Jan 2024 06:48:11 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 11 Jan 2024 06:48:11 GMT
EXPOSE 8080
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
	-	`sha256:1db949b5da4be7262fe93040b8d35b30a66813155e604af1d536857558c79971`  
		Last Modified: Thu, 11 Jan 2024 06:49:11 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a961ef321c1fe85d41ae4ff749d9ac6d68f9b55865ee4cbecc4e11db03e66ec1`  
		Last Modified: Thu, 11 Jan 2024 06:49:11 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1cb23f5ade8e040bece58f4d16eeca6fa4c6ffa0e2a3c65f31c9423837ea819`  
		Last Modified: Thu, 11 Jan 2024 06:49:11 GMT  
		Size: 1.4 MB (1386403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a212b3b585b57797a9be43f3361c44cb5a39626d39ddbea9a681a4ef6de9a312`  
		Last Modified: Thu, 11 Jan 2024 06:49:11 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:caaaa585eb7d76ac209bc932b1c619fe4af6837fb820fc5cabcbd830814fcc08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87797430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b664e06ea4a9cdfff6f716dcd0019595f7c453c70abc5801ab1a99e814c4660`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Thu, 11 Jan 2024 03:41:04 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 11 Jan 2024 03:41:04 GMT
WORKDIR /var/www/html
# Thu, 11 Jan 2024 03:41:05 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 11 Jan 2024 03:41:05 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 11 Jan 2024 03:41:05 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 11 Jan 2024 03:41:05 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 11 Jan 2024 03:41:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 03:41:31 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 11 Jan 2024 03:41:31 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 11 Jan 2024 03:41:31 GMT
USER adminer
# Thu, 11 Jan 2024 03:41:31 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 11 Jan 2024 03:41:31 GMT
EXPOSE 8080
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
	-	`sha256:ee2a36fc92b47b35ae70e2ec87fe4e471037dcc7afde3e5ba9b3c77e9c4132dd`  
		Last Modified: Thu, 11 Jan 2024 03:42:24 GMT  
		Size: 1.9 KB (1869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ae5d8295e12648dff135899d351ba2a3660bab9a88add9869fea94b5416175`  
		Last Modified: Thu, 11 Jan 2024 03:42:24 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6059422275888f60e52c8961c9483b5d3f6ae84613f9bdd977b7ccdd9de3e45c`  
		Last Modified: Thu, 11 Jan 2024 03:42:24 GMT  
		Size: 1.4 MB (1386399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec45ad210c1f8bb4c88054f306ef0a6a30a4095cedfbb7f8158670e8c4d4ea6b`  
		Last Modified: Thu, 11 Jan 2024 03:42:24 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:1ad77d0ee17a0cfb014837ab2a049f2fb5a645fa500d7932001c4f28f1385cfe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94346078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb100583c4b47dc0404ac42b327e7a9103870e9b19f0cfbd176df334944773c`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Thu, 11 Jan 2024 06:04:19 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 11 Jan 2024 06:04:19 GMT
WORKDIR /var/www/html
# Thu, 11 Jan 2024 06:04:20 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 11 Jan 2024 06:04:20 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 11 Jan 2024 06:04:20 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 11 Jan 2024 06:04:20 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 11 Jan 2024 06:04:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 06:04:31 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 11 Jan 2024 06:04:31 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 11 Jan 2024 06:04:31 GMT
USER adminer
# Thu, 11 Jan 2024 06:04:31 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 11 Jan 2024 06:04:31 GMT
EXPOSE 8080
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
	-	`sha256:e8139bb8fb2c520c7376beeef15d32c0949c77b88a6d1a2c63837ad6660f6059`  
		Last Modified: Thu, 11 Jan 2024 06:04:54 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4841af3dd32c6c1eed37bda7da9a264f1f4f16de82398ea1fb250039bc56ad7d`  
		Last Modified: Thu, 11 Jan 2024 06:04:54 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0809dec229c9cbeb08b9dbca9f86daec4143377f0e8248e9e1b88b58e1f5f3b`  
		Last Modified: Thu, 11 Jan 2024 06:04:54 GMT  
		Size: 1.4 MB (1386288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e699d50432f29e4520da6c4398bf1da266f642726c180d60c0cb6809005c1686`  
		Last Modified: Thu, 11 Jan 2024 06:04:54 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; 386

```console
$ docker pull adminer@sha256:d8808bff11e5d0e91bb1ca649abfad4c752f23a8b7e5078399482c9cbbd8f481
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96999107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5e59625efe622f4500df02d8c1a12f3b3d4e233023e8cf9422b69f67f837fad`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Thu, 11 Jan 2024 03:06:19 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 11 Jan 2024 03:06:19 GMT
WORKDIR /var/www/html
# Thu, 11 Jan 2024 03:06:19 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 11 Jan 2024 03:06:19 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 11 Jan 2024 03:06:19 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 11 Jan 2024 03:06:19 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 11 Jan 2024 03:06:34 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 03:06:34 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 11 Jan 2024 03:06:34 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 11 Jan 2024 03:06:34 GMT
USER adminer
# Thu, 11 Jan 2024 03:06:35 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 11 Jan 2024 03:06:35 GMT
EXPOSE 8080
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
	-	`sha256:b78e8112cdf1d8a98ddbb98c5bded37ae0fc1ef67d36c2b0b77087565d2516ed`  
		Last Modified: Thu, 11 Jan 2024 03:07:10 GMT  
		Size: 1.9 KB (1869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c35be29e51ec4da96361349ed6ee0d19bdc016b4608bd7e90da110e148e3ad68`  
		Last Modified: Thu, 11 Jan 2024 03:07:10 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ce22e8d760c5d059e509ff10dc8d51cb5dece49c4e2f3fc9a5284aac9d67e9`  
		Last Modified: Thu, 11 Jan 2024 03:07:10 GMT  
		Size: 1.4 MB (1386335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b636bd01d7510cd67411f9dce54c8308d3d459b97292e88b53ba300b00f7d72`  
		Last Modified: Thu, 11 Jan 2024 03:07:10 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; mips64le

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

### `adminer:standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:4d365e57938927e10b6e9ec77d3466db92f8c0daff11102bbe70ad6c9d76de0e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101265418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a330b36a8e5f39762fab68e5a4203fe2ee7753a1691d442a6be557eb05f667c9`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

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
# Thu, 11 Jan 2024 03:27:58 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 11 Jan 2024 03:27:59 GMT
WORKDIR /var/www/html
# Thu, 11 Jan 2024 03:27:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 11 Jan 2024 03:28:00 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 11 Jan 2024 03:28:00 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 11 Jan 2024 03:28:01 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 11 Jan 2024 03:28:26 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 03:28:27 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 11 Jan 2024 03:28:28 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 11 Jan 2024 03:28:30 GMT
USER adminer
# Thu, 11 Jan 2024 03:28:31 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 11 Jan 2024 03:28:32 GMT
EXPOSE 8080
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
	-	`sha256:47f1840589602f384b5a3058dd6e1e3884afe74faee0ac1c73a515684fb0701c`  
		Last Modified: Thu, 11 Jan 2024 03:29:35 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16883a74e121045dc837b6f19f5c955714b8d12110b73daee5bfb98d982f9c1d`  
		Last Modified: Thu, 11 Jan 2024 03:29:35 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0806c660480feb686533b92aacd489ca31754ef0cd460da88f8f24768e28d89`  
		Last Modified: Thu, 11 Jan 2024 03:29:36 GMT  
		Size: 1.4 MB (1386439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8053323de71cc08d4c9256d6cba46fa871e9ca692ce7b2731a3bbcb6702fcdb`  
		Last Modified: Thu, 11 Jan 2024 03:29:35 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:standalone` - linux; s390x

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
