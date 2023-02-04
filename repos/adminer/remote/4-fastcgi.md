## `adminer:4-fastcgi`

```console
$ docker pull adminer@sha256:4b520ad7dff7e1d1ec379d7cf644b2ff81e58873b13693c8b622006e0ddca03c
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
$ docker pull adminer@sha256:fe7586c7f9201c013f842e3281ed59d97ad5b2d3da12aae7cd0561898a9838b2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95903582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3605760e54fb8a7b27328a41e2e9171519e51f046e725080862cc83d0b93aaf0`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

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
# Wed, 11 Jan 2023 02:58:53 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 11 Jan 2023 02:58:53 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 11 Jan 2023 02:58:53 GMT
WORKDIR /var/www/html
# Wed, 11 Jan 2023 02:58:54 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 11 Jan 2023 02:58:54 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 11 Jan 2023 02:58:54 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 11 Jan 2023 02:58:54 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 11 Jan 2023 02:59:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 11 Jan 2023 02:59:06 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 11 Jan 2023 02:59:06 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 11 Jan 2023 02:59:06 GMT
USER adminer
# Wed, 11 Jan 2023 02:59:06 GMT
CMD ["php-fpm7.4"]
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
	-	`sha256:b47d8c722243dc3dd034efa743f98e50f7c6b1831133033f57610c8c4e7d79bc`  
		Last Modified: Wed, 11 Jan 2023 02:59:45 GMT  
		Size: 2.7 KB (2710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049898b4b05e6ea9cf719265cd593cc81939bb7deee1239b5e76ce2b0d93f957`  
		Last Modified: Wed, 11 Jan 2023 02:59:45 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d4fa539a8b3b7ad218f00a30c07cd04d376a8529eecebc60c17d7958662391`  
		Last Modified: Wed, 11 Jan 2023 02:59:45 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227322c8714d62aac558b9178a2cb76d7275c982cdcbb8e8e59379d983a481d3`  
		Last Modified: Wed, 11 Jan 2023 02:59:45 GMT  
		Size: 1.4 MB (1385250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60b1df330342c30a64a96b26940eeb40aced5e19ed3a9ae3fc25c2a7b95369c`  
		Last Modified: Wed, 11 Jan 2023 02:59:45 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm variant v5

```console
$ docker pull adminer@sha256:b0faee76d460250e5da70124df7400d6269459be2387a36fd70b4742cdb652f1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91168809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:686a1776dd4ebd5758ff511277a1ef3974927a6d48927cfd672cfe711b48901b`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

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
# Sat, 04 Feb 2023 03:11:06 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Sat, 04 Feb 2023 03:11:06 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 04 Feb 2023 03:11:06 GMT
WORKDIR /var/www/html
# Sat, 04 Feb 2023 03:11:06 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 04 Feb 2023 03:11:07 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 04 Feb 2023 03:11:07 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 04 Feb 2023 03:11:07 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Sat, 04 Feb 2023 03:11:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 04 Feb 2023 03:11:21 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 04 Feb 2023 03:11:21 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 04 Feb 2023 03:11:21 GMT
USER adminer
# Sat, 04 Feb 2023 03:11:21 GMT
CMD ["php-fpm7.4"]
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
	-	`sha256:b04c478a1338ba9cce40382cc051437bcb4eeebd188cdc41a2757609bd13a35d`  
		Last Modified: Sat, 04 Feb 2023 03:12:27 GMT  
		Size: 2.7 KB (2711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60684a0e72468ee14fd8a78d38bafa1e47ffa59e928b5ca43b567296d4e2e5ec`  
		Last Modified: Sat, 04 Feb 2023 03:12:27 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded008237b3a29c4aade74186cfb2937b5bedaa8962a885c6f24fba730b1c8a0`  
		Last Modified: Sat, 04 Feb 2023 03:12:27 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613048c62be0f9fe2d9baa69c469a56ce814e213ab521933ca34e2015c896df0`  
		Last Modified: Sat, 04 Feb 2023 03:12:27 GMT  
		Size: 1.4 MB (1384976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c141e4c1202dff4b82625db55bde8b836c1c3b6bb256de0b0d8517852a780b35`  
		Last Modified: Sat, 04 Feb 2023 03:12:27 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:b0d41a7ade132b9b25996d1f60cfb755d45846368e81da7cc261cc61e2f78292
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87765636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5636566827d25f7bd03186193ac45ea48276dfb56df5f90c15f7ed73b668bf93`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

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
# Wed, 11 Jan 2023 04:28:40 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 11 Jan 2023 04:28:41 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 11 Jan 2023 04:28:41 GMT
WORKDIR /var/www/html
# Wed, 11 Jan 2023 04:28:41 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 11 Jan 2023 04:28:41 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 11 Jan 2023 04:28:41 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 11 Jan 2023 04:28:41 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 11 Jan 2023 04:28:55 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 11 Jan 2023 04:28:55 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 11 Jan 2023 04:28:55 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 11 Jan 2023 04:28:55 GMT
USER adminer
# Wed, 11 Jan 2023 04:28:55 GMT
CMD ["php-fpm7.4"]
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
	-	`sha256:ddf57d35dd2103610ee70b0055c03c06c9fcf4e0cf4ddeeb2e344fc7bd1a3e98`  
		Last Modified: Wed, 11 Jan 2023 04:30:01 GMT  
		Size: 2.7 KB (2714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4511803861df5a66898b60c2806338b16ddcea85fee54722d58e3b03033c82`  
		Last Modified: Wed, 11 Jan 2023 04:30:01 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:312439bb2ffa3d5ddf10fbf5698b3efc7c03f02cef6fd5f486f767f2ec504303`  
		Last Modified: Wed, 11 Jan 2023 04:30:01 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e0ef458f063a985bfcb61fbeb26ea767fa1578d3444c2ecfde68288eda0a29d`  
		Last Modified: Wed, 11 Jan 2023 04:30:01 GMT  
		Size: 1.4 MB (1385027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ab7bf1ed16aefc7ae5faf562132d18ed4b3204e16cd6c1381ed98b2655aa0e6`  
		Last Modified: Wed, 11 Jan 2023 04:30:01 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:14e5c9e9653cd354401e9d672d76e6462430024848ee435c02d0ff4332126317
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94316110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa0825c1e857cf1eab6178105270bd008b049eb53696b1d94ed671c6284c846`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

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
# Sat, 04 Feb 2023 06:40:47 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Sat, 04 Feb 2023 06:40:48 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 04 Feb 2023 06:40:48 GMT
WORKDIR /var/www/html
# Sat, 04 Feb 2023 06:40:48 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 04 Feb 2023 06:40:48 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 04 Feb 2023 06:40:48 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 04 Feb 2023 06:40:48 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Sat, 04 Feb 2023 06:40:57 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 04 Feb 2023 06:40:57 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 04 Feb 2023 06:40:58 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 04 Feb 2023 06:40:58 GMT
USER adminer
# Sat, 04 Feb 2023 06:40:58 GMT
CMD ["php-fpm7.4"]
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
	-	`sha256:d66723d85a15a95d2bc016413f1fb69ae885d83e587a97d2043d370cf67e2db1`  
		Last Modified: Sat, 04 Feb 2023 06:41:36 GMT  
		Size: 2.7 KB (2707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7d226beb0ae597acd7e2647b0f4d4fc5227c69df6dff1165b4fe514cfad8130`  
		Last Modified: Sat, 04 Feb 2023 06:41:36 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def3ff5795d638c86eb1ce6b33aa5b7ac1991a913a5795be71a67c8f0bc1eab6`  
		Last Modified: Sat, 04 Feb 2023 06:41:36 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:277a8bd87f658c231dabf9f7c494772cd03abace79d86737b913b73e89ee7bac`  
		Last Modified: Sat, 04 Feb 2023 06:41:37 GMT  
		Size: 1.4 MB (1385063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e95c557117dcc88c76c221f757a0f3404ad012a7726a260eadd4aba9b4e3341`  
		Last Modified: Sat, 04 Feb 2023 06:41:37 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:b0a3d3e0b21c7f00206ed8268c4dd0c6f085e410f729fb795bb885f8cac1098f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96956091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9fa3646b337edc6af84c9cd6a950e859eaf4183842f124b5742da2f3495e257`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

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
# Sat, 04 Feb 2023 08:15:27 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Sat, 04 Feb 2023 08:15:28 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 04 Feb 2023 08:15:29 GMT
WORKDIR /var/www/html
# Sat, 04 Feb 2023 08:15:31 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 04 Feb 2023 08:15:31 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 04 Feb 2023 08:15:32 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 04 Feb 2023 08:15:33 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Sat, 04 Feb 2023 08:15:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 04 Feb 2023 08:15:47 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 04 Feb 2023 08:15:47 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 04 Feb 2023 08:15:48 GMT
USER adminer
# Sat, 04 Feb 2023 08:15:49 GMT
CMD ["php-fpm7.4"]
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
	-	`sha256:9fb386372d050d61199d8b69f8eba0503204b1435c14765dcc7391690f40e104`  
		Last Modified: Sat, 04 Feb 2023 08:16:47 GMT  
		Size: 2.7 KB (2709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92775617fc6814142b985df263b604974edc157e129229cd23234c9ea1e661e6`  
		Last Modified: Sat, 04 Feb 2023 08:16:47 GMT  
		Size: 1.7 KB (1714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95cd3c9ca70db181013ee630ed1999515d90622129ffa1cffcb8610f0f456f7`  
		Last Modified: Sat, 04 Feb 2023 08:16:48 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe214dd6c4ba9b73bd44278fa41542b21e1144c6ff3ac53e197896801e87d48`  
		Last Modified: Sat, 04 Feb 2023 08:16:48 GMT  
		Size: 1.4 MB (1385428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469bbb9c9519bc4c9fbd635879319fa1b6f74e4a9f271572fb23cbc31bcd739c`  
		Last Modified: Sat, 04 Feb 2023 08:16:47 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; mips64le

```console
$ docker pull adminer@sha256:958ca687500575c0459c29bd469d648353382c4073c2da26d64b5d7c9226eef7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92591226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597bcf08927c15302d341ba766c5e8b1492be2efd8442dd805a5cf6d3fb95e11`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

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
# Wed, 11 Jan 2023 17:07:50 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 11 Jan 2023 17:07:56 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 11 Jan 2023 17:08:00 GMT
WORKDIR /var/www/html
# Wed, 11 Jan 2023 17:08:02 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 11 Jan 2023 17:08:06 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 11 Jan 2023 17:08:09 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 11 Jan 2023 17:08:12 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 11 Jan 2023 17:09:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 11 Jan 2023 17:09:03 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 11 Jan 2023 17:09:06 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 11 Jan 2023 17:09:09 GMT
USER adminer
# Wed, 11 Jan 2023 17:09:12 GMT
CMD ["php-fpm7.4"]
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
	-	`sha256:5670ada6f99a6a9f66af8788a6e5781c3cf4979054bd3c3146bc6eb002d2f5f5`  
		Last Modified: Wed, 11 Jan 2023 17:10:25 GMT  
		Size: 2.7 KB (2716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09602a3d917421b29c826264219d1a0753c3e3e58449e6dcbfe8e3036bf96593`  
		Last Modified: Wed, 11 Jan 2023 17:10:25 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b679d8420a1d52c14948fd75ff4eaae6f031da5b19c940959816643c79eb9ac3`  
		Last Modified: Wed, 11 Jan 2023 17:10:25 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249e05195616ffaf5b26997e231c00b6e2821509220c28ea4361644e5dcda10e`  
		Last Modified: Wed, 11 Jan 2023 17:10:26 GMT  
		Size: 1.4 MB (1386169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c6d788d417d8dd6978e75893c62652f7fd0bf3f81419f7d6a4f5bf645b64d0`  
		Last Modified: Wed, 11 Jan 2023 17:10:25 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:11f04cf3466d358dce99e40edc912c53ecef6b6c94b26eac2d879ad7c02d99bb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101229238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ddf53e4c6f7763ba8fd1cd7a193c967518f17fe2d77819ecbd010055cf4d05a`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

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
# Wed, 11 Jan 2023 04:15:52 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 11 Jan 2023 04:15:53 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 11 Jan 2023 04:15:53 GMT
WORKDIR /var/www/html
# Wed, 11 Jan 2023 04:15:54 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 11 Jan 2023 04:15:54 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 11 Jan 2023 04:15:54 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 11 Jan 2023 04:15:55 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 11 Jan 2023 04:16:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 11 Jan 2023 04:16:17 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 11 Jan 2023 04:16:18 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 11 Jan 2023 04:16:18 GMT
USER adminer
# Wed, 11 Jan 2023 04:16:18 GMT
CMD ["php-fpm7.4"]
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
	-	`sha256:3851c2238b71619a46f4dbfaee242f76f5a8c4fff0b5917c0c2c2a5156625a31`  
		Last Modified: Wed, 11 Jan 2023 04:17:24 GMT  
		Size: 2.7 KB (2712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe83934881a81faa5033f13ea13f6edd0cb2302343a8efb9ea62635bd5ea872`  
		Last Modified: Wed, 11 Jan 2023 04:17:24 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d93423113b7614f7f62f330d7184a9b32dcc402af2678b134006121c1fb0597`  
		Last Modified: Wed, 11 Jan 2023 04:17:24 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd503ebdad568b857060f4a3448693948587c0be5f50c889ddd4f90be3194004`  
		Last Modified: Wed, 11 Jan 2023 04:17:27 GMT  
		Size: 1.4 MB (1385195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5cb61bb3dc0c1528e54d9c701665c9bc0b609055e11715b491b16607b291a2`  
		Last Modified: Wed, 11 Jan 2023 04:17:24 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; s390x

```console
$ docker pull adminer@sha256:1ab109f0d62ae9d1f632f64521d2b9c6bdd874936e381f5719bbb2f10d477adb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93669880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae533c8fd022e51fb36a09a261b07448ed0f776823c53100c05a74f04b702915`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

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
# Sat, 04 Feb 2023 04:28:48 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Sat, 04 Feb 2023 04:28:49 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Sat, 04 Feb 2023 04:28:49 GMT
WORKDIR /var/www/html
# Sat, 04 Feb 2023 04:28:49 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Sat, 04 Feb 2023 04:28:49 GMT
ENV ADMINER_VERSION=4.8.1
# Sat, 04 Feb 2023 04:28:49 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Sat, 04 Feb 2023 04:28:50 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Sat, 04 Feb 2023 04:28:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Sat, 04 Feb 2023 04:28:58 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Sat, 04 Feb 2023 04:28:58 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 04 Feb 2023 04:28:58 GMT
USER adminer
# Sat, 04 Feb 2023 04:28:58 GMT
CMD ["php-fpm7.4"]
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
	-	`sha256:1f26a88bf4960b44ad6d12c21999addb85dce5c8be7e7136debf4e387f92a4d0`  
		Last Modified: Sat, 04 Feb 2023 04:29:43 GMT  
		Size: 2.7 KB (2704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71728256a2268f2e10fa1e25931b860cd4992dd8538f7827943423c185911bd7`  
		Last Modified: Sat, 04 Feb 2023 04:29:43 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c129a190c5dd11a2cbde291af646cea194183aecc0fe9d9abd74d519b513e93`  
		Last Modified: Sat, 04 Feb 2023 04:29:43 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61555581092a6e535beb7ec3d53f495b27ea5e68400194b765e7070914fa112b`  
		Last Modified: Sat, 04 Feb 2023 04:29:43 GMT  
		Size: 1.4 MB (1385143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1586890cce0a53ad1c2656f461ba801fec113a74a4778dbdfdacc5f96c7e3a2b`  
		Last Modified: Sat, 04 Feb 2023 04:29:43 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
