## `adminer:latest`

```console
$ docker pull adminer@sha256:dd2fa65775169ffed5beecda149cc58433e1e10646b4ae1a2e9299bb32788461
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
$ docker pull adminer@sha256:2ca89c714c8adc4fa870c08198d72f51878039e6dfe974386e0a166814a24f55
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95900890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fed5dcb2cc13f128bce9fde1a99aa635e24eaa95e77033298e9c44e82e71e24f`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:29 GMT
ADD file:917750a82b29f8f7f88a121017bd9dfeb0fbcc8f0697a009f08b6b58246eff4b in / 
# Wed, 11 Jan 2023 02:34:30 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 02:58:04 GMT
STOPSIGNAL SIGINT
# Wed, 11 Jan 2023 02:58:28 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 02:58:28 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 11 Jan 2023 02:58:29 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 11 Jan 2023 02:58:29 GMT
WORKDIR /var/www/html
# Wed, 11 Jan 2023 02:58:29 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 11 Jan 2023 02:58:30 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 11 Jan 2023 02:58:30 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 11 Jan 2023 02:58:30 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 11 Jan 2023 02:58:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 11 Jan 2023 02:58:42 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 11 Jan 2023 02:58:42 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 11 Jan 2023 02:58:42 GMT
USER adminer
# Wed, 11 Jan 2023 02:58:43 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 11 Jan 2023 02:58:43 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:bbeef03cda1f5d6c9e20c310c1c91382a6b0a1a2501c3436b28152f13896f082`  
		Last Modified: Wed, 11 Jan 2023 02:38:42 GMT  
		Size: 55.0 MB (55025206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7b968dccc7e1f4be9e1a535df953f06efddd40acbba207f00137628ba701438`  
		Last Modified: Wed, 11 Jan 2023 02:59:27 GMT  
		Size: 39.5 MB (39486184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd6d69793072538a45ff2c3868c8c885188564c192a7c1dd3b9c857a62ab04e`  
		Last Modified: Wed, 11 Jan 2023 02:59:19 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5694c6147308ec0c980896c76e1aed5ef69c35f81b02020307b3809dafc87eab`  
		Last Modified: Wed, 11 Jan 2023 02:59:19 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03ab2def1a968ffed6e8ec99195a29b4a6ab1f335bfee47f39ae37671da061b`  
		Last Modified: Wed, 11 Jan 2023 02:59:19 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd1cddd5008cb8eab7266f76bed86ee59538eebff3f0a0a6f7fd2b2951ea720`  
		Last Modified: Wed, 11 Jan 2023 02:59:20 GMT  
		Size: 1.4 MB (1385258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f49a2ac8ec9fce44010b42455bc8ed14515fca6cbc2d98e2e547880104f72ab`  
		Last Modified: Wed, 11 Jan 2023 02:59:19 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; arm variant v5

```console
$ docker pull adminer@sha256:7c1fa4cba8de32f8dcd0490b2a2422c631b19bb487e99b086994b5c05a3e5304
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91166086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e49dc547f30520e8cc02bd7952804ffcd3083edcff85583be202968d662f1d30`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Sat, 04 Feb 2023 02:46:21 GMT
ADD file:1c80f7ec931ef9c6fa80892f75b88f6b3aebe7abe65f4a13b9371eb98475ca96 in / 
# Sat, 04 Feb 2023 02:46:23 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 03:10:13 GMT
STOPSIGNAL SIGINT
# Sat, 04 Feb 2023 03:10:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 03:10:43 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Sat, 04 Feb 2023 03:10:43 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 04 Feb 2023 03:10:44 GMT
WORKDIR /var/www/html
# Sat, 04 Feb 2023 03:10:44 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 04 Feb 2023 03:10:44 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 04 Feb 2023 03:10:44 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 04 Feb 2023 03:10:44 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Sat, 04 Feb 2023 03:10:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 04 Feb 2023 03:10:59 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 04 Feb 2023 03:10:59 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 04 Feb 2023 03:10:59 GMT
USER adminer
# Sat, 04 Feb 2023 03:10:59 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 04 Feb 2023 03:10:59 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:193207e81b928808ec6f645dfaf0b61e74f80f891a3bad16651e923e85334c17`  
		Last Modified: Sat, 04 Feb 2023 02:51:10 GMT  
		Size: 52.5 MB (52530008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf1e080dcd3cfdef2852c2a62475d65a3be37771728b0f57be08714f0c60e36`  
		Last Modified: Sat, 04 Feb 2023 03:12:03 GMT  
		Size: 37.2 MB (37246915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4bb45667a6f38868757806bcd165542a734a196db03d91aabbef270ef54210e`  
		Last Modified: Sat, 04 Feb 2023 03:11:53 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e27c4ea0322a359fdb6aeb5d6c9336b31e2ab266d453f594e2372614b70c8f`  
		Last Modified: Sat, 04 Feb 2023 03:11:53 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca440ca86e683467380dce0cca920c799bbfe61964be1764d3259310da89b340`  
		Last Modified: Sat, 04 Feb 2023 03:11:53 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70cef54c0996b2fbcc45896c5b316b1d4d1a0ebaadc7402e4e46fd30bdca6400`  
		Last Modified: Sat, 04 Feb 2023 03:11:54 GMT  
		Size: 1.4 MB (1384960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e498ef275098488f6b8d48d742a015b32577dcd1ac762f40ceb3b035fb4316c`  
		Last Modified: Sat, 04 Feb 2023 03:11:53 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; arm variant v7

```console
$ docker pull adminer@sha256:437107228ad60f45b55604f2338ab10034da43ba2fb0086e346b6f1342846c9a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87762924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fd9fd923e82368ee3bb2b57ed89ca75c98a41a6752d1b966511808f7b4c16a3`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 11 Jan 2023 04:00:17 GMT
ADD file:48f6407691a382c3ad731f05f78d4210efd40f1a00abfd6c043d8401c6ca1811 in / 
# Wed, 11 Jan 2023 04:00:18 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 04:27:48 GMT
STOPSIGNAL SIGINT
# Wed, 11 Jan 2023 04:28:12 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 04:28:13 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 11 Jan 2023 04:28:13 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 11 Jan 2023 04:28:13 GMT
WORKDIR /var/www/html
# Wed, 11 Jan 2023 04:28:14 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 11 Jan 2023 04:28:14 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 11 Jan 2023 04:28:14 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 11 Jan 2023 04:28:14 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 11 Jan 2023 04:28:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 11 Jan 2023 04:28:27 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 11 Jan 2023 04:28:28 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 11 Jan 2023 04:28:28 GMT
USER adminer
# Wed, 11 Jan 2023 04:28:28 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 11 Jan 2023 04:28:28 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:d705c97ea3a2300e9dda9a18ff662a98c2811b41147a15d4f4791f475ce8be47`  
		Last Modified: Wed, 11 Jan 2023 04:07:17 GMT  
		Size: 50.2 MB (50190808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a2b86347028efeeb6736d363a533c0b3250cdc022c20746b4c79c23bdf1774`  
		Last Modified: Wed, 11 Jan 2023 04:29:37 GMT  
		Size: 36.2 MB (36182880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581874ea0a70acb2b346c8fe65db2ed3667a5cf88f17983ae2b3e0837556165d`  
		Last Modified: Wed, 11 Jan 2023 04:29:27 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c9a5092cf50a2bd5703f215b7178860b342cb8f52c1b9aca602a6bc080d806`  
		Last Modified: Wed, 11 Jan 2023 04:29:27 GMT  
		Size: 1.8 KB (1838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba24f7356d13859c57c120ee15ee8688e101ae8d522f73e589202c03a6a74419`  
		Last Modified: Wed, 11 Jan 2023 04:29:27 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34e090ca20fcf19747328e0fb4c884227b25a7fe040388f542ee2d34aabf235`  
		Last Modified: Wed, 11 Jan 2023 04:29:28 GMT  
		Size: 1.4 MB (1385035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613b7766e8beeba0c21b97eebdd745f0f5de818652f99f1f699ae64f39765884`  
		Last Modified: Wed, 11 Jan 2023 04:29:27 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:4f5db61ed6cff7c4d001092c5ce6d5eb7501a356739d77657c28f6b813d428c2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94313416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55903b78a43635b55478abb38f63cd77f3e0ec223947f72aee5c6872a07ffd1`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:26 GMT
ADD file:c5a7c65d67685092faa3456c1a772550aa6d06ac07e1f98a95d39c31e304dbf8 in / 
# Sat, 04 Feb 2023 06:17:27 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 06:40:07 GMT
STOPSIGNAL SIGINT
# Sat, 04 Feb 2023 06:40:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 06:40:28 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Sat, 04 Feb 2023 06:40:29 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 04 Feb 2023 06:40:29 GMT
WORKDIR /var/www/html
# Sat, 04 Feb 2023 06:40:29 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 04 Feb 2023 06:40:29 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 04 Feb 2023 06:40:29 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 04 Feb 2023 06:40:29 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Sat, 04 Feb 2023 06:40:39 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 04 Feb 2023 06:40:39 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 04 Feb 2023 06:40:39 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 04 Feb 2023 06:40:40 GMT
USER adminer
# Sat, 04 Feb 2023 06:40:40 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 04 Feb 2023 06:40:40 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:fac7262b6510529638951e16807cf1758f42c892ed924e334c27bb8bbcf7d7c2`  
		Last Modified: Sat, 04 Feb 2023 06:21:01 GMT  
		Size: 53.7 MB (53681927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3c4993b9ed6a78b02081f8b79138654baa646295eb90d0f09eb178f86f610b`  
		Last Modified: Sat, 04 Feb 2023 06:41:19 GMT  
		Size: 39.2 MB (39242179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77346147b34a65302ad6ba550d6ab4659b2d986cd2c2e57248651460e8a3e589`  
		Last Modified: Sat, 04 Feb 2023 06:41:12 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56563dd7963c36713d65f09a5387503374566d7296c2bfa4422bf2d3ceb3bbeb`  
		Last Modified: Sat, 04 Feb 2023 06:41:12 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa2e6ff1278f9c9246cfedeee571a41de27494a6f3d518f136dbb8a225d7d33`  
		Last Modified: Sat, 04 Feb 2023 06:41:12 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24f727f464d597cc5ae7abb0b697c3807940cf0cca55089c3cbc553eee16523`  
		Last Modified: Sat, 04 Feb 2023 06:41:12 GMT  
		Size: 1.4 MB (1385069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717c6895aefe53599660cfa578fea33535395f3479fdaecb0f2db55b2fa1165a`  
		Last Modified: Sat, 04 Feb 2023 06:41:12 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; 386

```console
$ docker pull adminer@sha256:9aeaa40748b7ce615a50ef6b58624bde25df408d8e05367d32f939a9ebac3a1d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96953374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0059247fefe0e30e3270aaad4163ba4bfc56aa80f66364c27054b4f9bd7ef47`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Sat, 04 Feb 2023 07:49:07 GMT
ADD file:d610d24eb19fe7e275924d58b6dad6b9f3dce21359a4ef81d04298e94382f102 in / 
# Sat, 04 Feb 2023 07:49:07 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 08:14:35 GMT
STOPSIGNAL SIGINT
# Sat, 04 Feb 2023 08:14:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:14:58 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Sat, 04 Feb 2023 08:14:59 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 04 Feb 2023 08:14:59 GMT
WORKDIR /var/www/html
# Sat, 04 Feb 2023 08:15:01 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 04 Feb 2023 08:15:01 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 04 Feb 2023 08:15:02 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 04 Feb 2023 08:15:03 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Sat, 04 Feb 2023 08:15:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 04 Feb 2023 08:15:17 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 04 Feb 2023 08:15:17 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 04 Feb 2023 08:15:18 GMT
USER adminer
# Sat, 04 Feb 2023 08:15:19 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 04 Feb 2023 08:15:20 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:082bfbf393a7a28cd82d531b1903cc5d788ac6af1b972045ad1d0deeff1aa6ab`  
		Last Modified: Sat, 04 Feb 2023 07:54:34 GMT  
		Size: 56.0 MB (56005478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb56dd30a9439c969b4e4698f93d1d6904887b24d016964a7c0857e306cbf507`  
		Last Modified: Sat, 04 Feb 2023 08:16:26 GMT  
		Size: 39.6 MB (39558401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0895a9cfae4403af4769bb7fc2334726c0db5a6929982d11aca84a6fd3b4247`  
		Last Modified: Sat, 04 Feb 2023 08:16:17 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b8ed21414ac18410d2cd7538e45767fefbf32a8719524c47f79dbb6481c58a9`  
		Last Modified: Sat, 04 Feb 2023 08:16:17 GMT  
		Size: 1.7 KB (1718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba129a165b264b065c4c64c28d541b80a301b07360486eeaaa32fffd058c8614`  
		Last Modified: Sat, 04 Feb 2023 08:16:17 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33029a943fe1a9b73a9717bc4636749407077422d7374aa4dddc3a99a9f97a7`  
		Last Modified: Sat, 04 Feb 2023 08:16:17 GMT  
		Size: 1.4 MB (1385416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036ba73b7268a6aed37bd51a00d8c5ffd4f4a71eb03b0aa0e8ed0a6c0123bc82`  
		Last Modified: Sat, 04 Feb 2023 08:16:17 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; mips64le

```console
$ docker pull adminer@sha256:878697ba46a6bd602d27fc6bc9787c13bc5231fa25fa157cfc8a1e87d07a5725
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92588530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52168944cd71fa64c9d4e604add7b44251c8ba8791b94eb57fa7a306cdd1f0ac`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 11 Jan 2023 16:33:42 GMT
ADD file:8c29f17eac3e24c302d9d5569b89e9c08432801b4ae509971a7b4981c1946a6e in / 
# Wed, 11 Jan 2023 16:33:48 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 17:03:49 GMT
STOPSIGNAL SIGINT
# Wed, 11 Jan 2023 17:05:52 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 17:05:59 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 11 Jan 2023 17:06:05 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 11 Jan 2023 17:06:09 GMT
WORKDIR /var/www/html
# Wed, 11 Jan 2023 17:06:12 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 11 Jan 2023 17:06:15 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 11 Jan 2023 17:06:18 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 11 Jan 2023 17:06:21 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 11 Jan 2023 17:07:19 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 11 Jan 2023 17:07:22 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 11 Jan 2023 17:07:25 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 11 Jan 2023 17:07:29 GMT
USER adminer
# Wed, 11 Jan 2023 17:07:32 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 11 Jan 2023 17:07:35 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:ed9c81424eb02ba70b9582fe73080191ccd4486689354a607c1eb45a6129c865`  
		Last Modified: Wed, 11 Jan 2023 16:42:37 GMT  
		Size: 53.2 MB (53245158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc63cc5f5f898481bb1a9e61e5372d4f34eb8e5317e7a85faa2d54a353f06149`  
		Last Modified: Wed, 11 Jan 2023 17:10:07 GMT  
		Size: 38.0 MB (37953089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77b35c2897784bd435e4f049156b411e617d9e14ae9bb5afe5a497659b60ca9`  
		Last Modified: Wed, 11 Jan 2023 17:09:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aef4c44f9c70b74bd43a2cfd4aacb0c704012d5fcb309490126cb6de3833bd31`  
		Last Modified: Wed, 11 Jan 2023 17:09:38 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6b159f8ad7c58d646b8279896838bb21e344956031e9311ae1848f945893ee`  
		Last Modified: Wed, 11 Jan 2023 17:09:38 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f0b54a8fbb621a08bec2c21115be7d15ab3d7da836e42b6aaebbb205d33bc6`  
		Last Modified: Wed, 11 Jan 2023 17:09:39 GMT  
		Size: 1.4 MB (1386187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef56872ddc2c5170d153590c54472e527f3150a008b0fdc243e2d78619060d74`  
		Last Modified: Wed, 11 Jan 2023 17:09:39 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; ppc64le

```console
$ docker pull adminer@sha256:dab44ef9e1d20a6866d7955e60dc19b4a8b842c93231b4ee3a8d4457a505fb16
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101226569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0fc15318deef80dfe3a4e83e157ddd4176e21bdd6264e5531e95d424eae6aa`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 11 Jan 2023 03:49:05 GMT
ADD file:9b8f1afc3870e9ea3bacdbf146017c3fdebee0140a9ad896fca12bc5a1927c0a in / 
# Wed, 11 Jan 2023 03:49:09 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 04:14:26 GMT
STOPSIGNAL SIGINT
# Wed, 11 Jan 2023 04:15:10 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 04:15:12 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 11 Jan 2023 04:15:14 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 11 Jan 2023 04:15:14 GMT
WORKDIR /var/www/html
# Wed, 11 Jan 2023 04:15:14 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 11 Jan 2023 04:15:15 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 11 Jan 2023 04:15:15 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 11 Jan 2023 04:15:15 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 11 Jan 2023 04:15:38 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 11 Jan 2023 04:15:38 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 11 Jan 2023 04:15:38 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 11 Jan 2023 04:15:39 GMT
USER adminer
# Wed, 11 Jan 2023 04:15:39 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 11 Jan 2023 04:15:39 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:ab68a4092b73f1d14a0c9ccbe7c004408a6b0123b637274d22899b983919c917`  
		Last Modified: Wed, 11 Jan 2023 03:54:58 GMT  
		Size: 58.9 MB (58897136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a368dd79573c27388e916dbf14eb7ad7581d62c2211784ce81c75d3bee5ee9`  
		Last Modified: Wed, 11 Jan 2023 04:17:00 GMT  
		Size: 40.9 MB (40939951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f227b594adc79958a0290f7c68ebec84f6920d1e85b4a2b61be9cb148adbf6f0`  
		Last Modified: Wed, 11 Jan 2023 04:16:48 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4967b8407492af28aca88175532dd21cfb06120c7c1583425e06a52840edec0d`  
		Last Modified: Wed, 11 Jan 2023 04:16:48 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89046ef3ab968092ced180d53b970f182baa4bd3fa64c2994c422c1a7e641215`  
		Last Modified: Wed, 11 Jan 2023 04:16:48 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ba54ed8820abcd9e0b415e583b19364ebf154412fd500de805d2e222fab304`  
		Last Modified: Wed, 11 Jan 2023 04:16:48 GMT  
		Size: 1.4 MB (1385233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7cae45479a59539cdfc388166928cd5911d6e99e5bfaa0092c1a721368321e`  
		Last Modified: Wed, 11 Jan 2023 04:16:48 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; s390x

```console
$ docker pull adminer@sha256:c3f405ec472179d37cbb59a97aae02ce8c3664e1ce4f253a6c7389b060a19d5f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93667223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12806fc9688bbfeea1fa8cae1265eac7672deb67de2eaf2c8a710cc21756c6e1`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Sat, 04 Feb 2023 04:05:57 GMT
ADD file:57d389473a23d7f4ecc41746379cb0b904a0ed555b55b4cae8e0ebbb2fdb063b in / 
# Sat, 04 Feb 2023 04:06:00 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 04:28:05 GMT
STOPSIGNAL SIGINT
# Sat, 04 Feb 2023 04:28:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 04:28:29 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Sat, 04 Feb 2023 04:28:30 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 04 Feb 2023 04:28:30 GMT
WORKDIR /var/www/html
# Sat, 04 Feb 2023 04:28:30 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 04 Feb 2023 04:28:30 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 04 Feb 2023 04:28:31 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 04 Feb 2023 04:28:31 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Sat, 04 Feb 2023 04:28:39 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 04 Feb 2023 04:28:39 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 04 Feb 2023 04:28:40 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 04 Feb 2023 04:28:40 GMT
USER adminer
# Sat, 04 Feb 2023 04:28:40 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Sat, 04 Feb 2023 04:28:40 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:20679e968bacc458d63e0ab992076c085ca41e6c4c6d2a152130c347a7604493`  
		Last Modified: Sat, 04 Feb 2023 04:10:08 GMT  
		Size: 53.3 MB (53258422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b3cd564086af4d6785d439bcbd880b22b876f7203406b8c89a2a1ea92b6175`  
		Last Modified: Sat, 04 Feb 2023 04:29:28 GMT  
		Size: 39.0 MB (39019368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331aa0615ad09c32e532edacfd3b679e9803f68103e992b7ba35c6a11735634d`  
		Last Modified: Sat, 04 Feb 2023 04:29:22 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e30624611f807e5e1ebce2fb2c63f0f51a585a417d59e47b6976254425d49ac`  
		Last Modified: Sat, 04 Feb 2023 04:29:22 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b896b54b83150710468b71246e462f41af780297c4244290a154600a7ef2e3`  
		Last Modified: Sat, 04 Feb 2023 04:29:22 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be63f66c0e34a26ea76521a7355373ee9f89088f867afe1beaa51634fe65949`  
		Last Modified: Sat, 04 Feb 2023 04:29:22 GMT  
		Size: 1.4 MB (1385196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649e2be8d8568f532bdec719c417f06eaf4f6dea7a60a251d691fe718b97b5f4`  
		Last Modified: Sat, 04 Feb 2023 04:29:22 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
