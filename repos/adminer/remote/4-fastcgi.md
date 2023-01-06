## `adminer:4-fastcgi`

```console
$ docker pull adminer@sha256:f0e27bea05c888b0a66df57e3f9a867420d946d16f30c273f3998e03985af292
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
$ docker pull adminer@sha256:e06aee3dccf5dc627614fb55f9f65d150c343da3062d57361946d8a82a7a546c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95903918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada61419ab056a93d2728e728b19edc7f7f1b1ec2c82e5116fd822c095d08a6e`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:21 GMT
ADD file:c13b430c8699df107ffd9ea5230b92238bc037a8e1cbbe35d6ab664941d575da in / 
# Wed, 21 Dec 2022 01:20:22 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:43:34 GMT
STOPSIGNAL SIGINT
# Fri, 06 Jan 2023 20:19:38 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Fri, 06 Jan 2023 20:19:39 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Fri, 06 Jan 2023 20:19:57 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Fri, 06 Jan 2023 20:19:57 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 06 Jan 2023 20:19:57 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 20:19:57 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 06 Jan 2023 20:19:58 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 06 Jan 2023 20:19:58 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 06 Jan 2023 20:19:58 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Fri, 06 Jan 2023 20:20:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 06 Jan 2023 20:20:14 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 06 Jan 2023 20:20:14 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 06 Jan 2023 20:20:14 GMT
USER adminer
# Fri, 06 Jan 2023 20:20:14 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:32de3c850997ce03b6ff4ae8fb00b34b9d7d7f9a35bfcdb8538e22cc7b77c29d`  
		Last Modified: Wed, 21 Dec 2022 01:24:10 GMT  
		Size: 55.0 MB (55025166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec10a039d0b26eb276346517e765c0aebc772d7be430d1c49f512b5bfc807fb3`  
		Last Modified: Fri, 06 Jan 2023 20:20:35 GMT  
		Size: 39.5 MB (39486591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:774f483c4a1c1ed1df80d22a3a208285b746ecba04d2edc8b6a48d5bc19a7a7a`  
		Last Modified: Fri, 06 Jan 2023 20:20:28 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e352441d66733a0b348373e148a23f19907626cd7570d38965e7b7c5a28e1654`  
		Last Modified: Fri, 06 Jan 2023 20:20:52 GMT  
		Size: 2.7 KB (2706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62ff6cff5199f2d214fccf45bbc869e2ea51861cc8ea318846ac7ed6ad9ab378`  
		Last Modified: Fri, 06 Jan 2023 20:20:52 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d575406ea1f849cb75a86933126a8b248206da27e43aed8b4e317b015ca5cad9`  
		Last Modified: Fri, 06 Jan 2023 20:20:52 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a4894913a604f3db46fc56294f6fcd78766f8ca890471a042393fb7f578b7b2`  
		Last Modified: Fri, 06 Jan 2023 20:20:53 GMT  
		Size: 1.4 MB (1385224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b62be5fd17c7f225768f5fe7fff5f5983a405a43ce85ec72b9e33a18ee4060`  
		Last Modified: Fri, 06 Jan 2023 20:20:52 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm variant v5

```console
$ docker pull adminer@sha256:d63be784d7dd2c00b72a0af4bc39f3b0b8829c50f8dbaae17b076717121a406a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91169283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a4eb6ff273df05e394aa761021ae85d0d82103dd2ddf54f8cac9e8ccf2a7919`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 21 Dec 2022 01:48:53 GMT
ADD file:81ccc74e0ea343972e2f3f46d2da7e9b808d9718be44d4afa7bec6904b7ab9c6 in / 
# Wed, 21 Dec 2022 01:48:55 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:12:35 GMT
STOPSIGNAL SIGINT
# Fri, 06 Jan 2023 19:49:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Fri, 06 Jan 2023 19:49:18 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Fri, 06 Jan 2023 19:49:51 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Fri, 06 Jan 2023 19:49:52 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 06 Jan 2023 19:49:52 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 19:49:53 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 06 Jan 2023 19:49:53 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 06 Jan 2023 19:49:53 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 06 Jan 2023 19:49:54 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Fri, 06 Jan 2023 19:50:14 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 06 Jan 2023 19:50:14 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 06 Jan 2023 19:50:14 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 06 Jan 2023 19:50:15 GMT
USER adminer
# Fri, 06 Jan 2023 19:50:15 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:89b6e4f9f2f811282495a047e873c20d6ac2d53c72ad576a6907b1449eb3e635`  
		Last Modified: Wed, 21 Dec 2022 01:53:30 GMT  
		Size: 52.5 MB (52529974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b72cae19914dcc1857f2a3e4175d1e5f01ad7f2eb66388e05e0c1b3d5e3f09`  
		Last Modified: Fri, 06 Jan 2023 19:51:00 GMT  
		Size: 37.2 MB (37247333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8a93a9f9efb156fd9eeef076788687925e501c7b35131ff72f303c249ed71b`  
		Last Modified: Fri, 06 Jan 2023 19:50:50 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04fd23bca6e2d24de4297e795fc30847c5f46abd9c9c03562eba9bfbb4bab391`  
		Last Modified: Fri, 06 Jan 2023 19:51:26 GMT  
		Size: 2.7 KB (2711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ad49744abfcbde15b1156d827857264d0f0f39227b073e715476b4aa56b1c6`  
		Last Modified: Fri, 06 Jan 2023 19:51:26 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bf7bef3dfa987c6849a0fbab4659f8b3aa787a26c94474f44abe077e3ef54b`  
		Last Modified: Fri, 06 Jan 2023 19:51:26 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a61d18ed6b2371e40ccd5a0958dc4d740b05b2ff412afc44712b2cb266b6fab`  
		Last Modified: Fri, 06 Jan 2023 19:51:27 GMT  
		Size: 1.4 MB (1385062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c1b982105a339ebc2a6fb0bf15dca2231f940bc7b42c1347d022096b219777`  
		Last Modified: Fri, 06 Jan 2023 19:51:26 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:9928846ee8fb76c681b35c87ebfed49499f447a0c1c81393d30ab2bcba70a6c2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87528433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99681162737fb62edc07a8e79538b32ebe15b415a91f8e6c9e8d2c0f6f224b9a`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 21 Dec 2022 01:58:09 GMT
ADD file:4b6f71680de34554595f062f9e52037b48edf19ca8f34c75877caa85c42caad3 in / 
# Wed, 21 Dec 2022 01:58:10 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 16:55:05 GMT
STOPSIGNAL SIGINT
# Wed, 21 Dec 2022 16:55:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 16:55:28 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 21 Dec 2022 16:55:49 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 21 Dec 2022 16:55:50 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 21 Dec 2022 16:55:50 GMT
WORKDIR /var/www/html
# Wed, 21 Dec 2022 16:55:50 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 21 Dec 2022 16:55:50 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 21 Dec 2022 16:55:50 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 21 Dec 2022 16:55:50 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 21 Dec 2022 16:56:04 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 21 Dec 2022 16:56:04 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 21 Dec 2022 16:56:04 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 21 Dec 2022 16:56:04 GMT
USER adminer
# Wed, 21 Dec 2022 16:56:04 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:706bb1d74512e1fb9ba97aa9212a32d07726fbfe77e4c7e609406d2065418f57`  
		Last Modified: Wed, 21 Dec 2022 02:04:37 GMT  
		Size: 50.2 MB (50190771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1c5cd5ac0e733e02567c893f1028628f441423281df1c54fa1042b317bb758`  
		Last Modified: Wed, 21 Dec 2022 16:56:48 GMT  
		Size: 35.9 MB (35947077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d69909ab6c9fd65668b2d644bbb5375f5617c8bba9e82704145b53e895ad98`  
		Last Modified: Wed, 21 Dec 2022 16:56:39 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e39a1a73560e658bd05d5621c5e241ea6c658eeb4d6d40fab42c2d0e049dd9`  
		Last Modified: Wed, 21 Dec 2022 16:57:11 GMT  
		Size: 2.7 KB (2707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570ddb9aaf5affd1f0db7ce02160f1220f1f786028eb2dc3304d29faec9a812c`  
		Last Modified: Wed, 21 Dec 2022 16:57:11 GMT  
		Size: 1.8 KB (1841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5278a6d095ca223fab850a965a90f10b571dee63613450a5c305743288a3db7`  
		Last Modified: Wed, 21 Dec 2022 16:57:11 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f0a1888014f0f3ae5844f8d80c0707d886f7e951a2583d43345fb59abe5e97c`  
		Last Modified: Wed, 21 Dec 2022 16:57:12 GMT  
		Size: 1.4 MB (1383680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6e719bcd08751a23a74658e85fc4e47ae42d98213576128a573499661a743b9`  
		Last Modified: Wed, 21 Dec 2022 16:57:11 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:3183f3e800b810102e90567427f392494d934939c536ff3ec0dc93957507374f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94316107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ead8b6c4c33c917f4fdf3f736610eb663fc6c8816793b032f471bdbcec44a1`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:40 GMT
ADD file:5bbdc914ec8ed60ac85293e88ee1aafc3f0290762e320fc86dc9d79fa201834e in / 
# Wed, 21 Dec 2022 01:39:41 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:01:54 GMT
STOPSIGNAL SIGINT
# Fri, 06 Jan 2023 21:36:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Fri, 06 Jan 2023 21:36:31 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Fri, 06 Jan 2023 21:36:49 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Fri, 06 Jan 2023 21:36:49 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 06 Jan 2023 21:36:49 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 21:36:49 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 06 Jan 2023 21:36:49 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 06 Jan 2023 21:36:50 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 06 Jan 2023 21:36:50 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Fri, 06 Jan 2023 21:37:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 06 Jan 2023 21:37:00 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 06 Jan 2023 21:37:00 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 06 Jan 2023 21:37:00 GMT
USER adminer
# Fri, 06 Jan 2023 21:37:00 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:c3e6129b48b69d14c5e7a5605e2b94003fb71aac82eac46b8689f5b8007af2c5`  
		Last Modified: Wed, 21 Dec 2022 01:42:49 GMT  
		Size: 53.7 MB (53681797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af8b0a3bc4f30a4fe48ee4bdb56f42632fb25667e9513a39a4fe63041a6eb4c`  
		Last Modified: Fri, 06 Jan 2023 21:37:24 GMT  
		Size: 39.2 MB (39242272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50798d551bc1256ad40278b81cd317a3cda62ee857933f96f4bbbdd35bd2ac52`  
		Last Modified: Fri, 06 Jan 2023 21:37:17 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659d25bed19f7a37e6789555798f190f255473c43de862c59f670bd17775bc29`  
		Last Modified: Fri, 06 Jan 2023 21:37:41 GMT  
		Size: 2.7 KB (2704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1b08a704a756b8e7a802d680b631cc644790526691ede61171e06d1f2a55a2`  
		Last Modified: Fri, 06 Jan 2023 21:37:41 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead06ab887225be725c74fa493d117400f8c10ff4af65caf53f55ac54b57cf73`  
		Last Modified: Fri, 06 Jan 2023 21:37:41 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0583bd6cc88c1b66b82483b8fcec7cb81529c6dc2e4820c0c2d29f22da699db6`  
		Last Modified: Fri, 06 Jan 2023 21:37:42 GMT  
		Size: 1.4 MB (1385099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f85356d82ce55b115f7331dfc65a7aed13642291f7fab22f63b875098111d2`  
		Last Modified: Fri, 06 Jan 2023 21:37:41 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:0dd9378cba30b8904bfcbe9d60ca31ba98b2d69e894f5c68e6b2f7da5801c63a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96956259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10c40a95b907007ee64e9c6421cba268d074d8fcceb185d2034e778929f93baf`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:08 GMT
ADD file:10d2f443f55d8ba9512899b3dff08f6e9a6c7ca096f407e3477e9798e1063785 in / 
# Wed, 21 Dec 2022 01:39:09 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:04:14 GMT
STOPSIGNAL SIGINT
# Fri, 06 Jan 2023 19:50:26 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Fri, 06 Jan 2023 19:50:26 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Fri, 06 Jan 2023 19:50:56 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Fri, 06 Jan 2023 19:50:57 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 06 Jan 2023 19:50:58 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 19:51:00 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 06 Jan 2023 19:51:00 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 06 Jan 2023 19:51:01 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 06 Jan 2023 19:51:02 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Fri, 06 Jan 2023 19:51:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 06 Jan 2023 19:51:16 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 06 Jan 2023 19:51:16 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 06 Jan 2023 19:51:17 GMT
USER adminer
# Fri, 06 Jan 2023 19:51:18 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:bde501e1d960005aee2bdf2fc8c89b26bf694dace8740c72deda4d7705995ab7`  
		Last Modified: Wed, 21 Dec 2022 01:44:18 GMT  
		Size: 56.0 MB (56005267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83479e0157aa35d66253ff9cd26e34f4bfa78c1f98e932f8a2f3ba531bd372f6`  
		Last Modified: Fri, 06 Jan 2023 19:51:50 GMT  
		Size: 39.6 MB (39558781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c00fd278cdb927bf06658b7ae202361e198e7505330fda919646c334bd2443f`  
		Last Modified: Fri, 06 Jan 2023 19:51:42 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66887e30d3aecc3c76d24bc2a7c2aaf73486b66958e5ee7e800ddb63d45fe0e4`  
		Last Modified: Fri, 06 Jan 2023 19:52:12 GMT  
		Size: 2.7 KB (2712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b643e8f93e175490e3ace6cb01afe8c533ba3f6faf4f673d926fd66b5eef74ce`  
		Last Modified: Fri, 06 Jan 2023 19:52:12 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb32ce0cfd874bf696a59cb1c062ca800fca1972273e682fd2c807749da81387`  
		Last Modified: Fri, 06 Jan 2023 19:52:12 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651783ef541352541b940053b497363a00ebb8d6192641d96fef985992d9f3c0`  
		Last Modified: Fri, 06 Jan 2023 19:52:12 GMT  
		Size: 1.4 MB (1385414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d42709b635aad3be9a569863aac881c62516b8b26de4cbf0bb93ade76f7fd3a`  
		Last Modified: Fri, 06 Jan 2023 19:52:12 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; mips64le

```console
$ docker pull adminer@sha256:585684b9b2732b194b3759554ffbdd27fc094a71e3ee13e604d66a9e9cf196fd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92591693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ebeb1b62b1e9f24ce4aa00895b2667b1abb752fbe0edfb974213562098fc225`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 21 Dec 2022 01:09:53 GMT
ADD file:972bcf9c0f583e92c03e74f66acec816703788fcc96e3a43357262f69e552ce5 in / 
# Wed, 21 Dec 2022 01:09:59 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 23:26:29 GMT
STOPSIGNAL SIGINT
# Fri, 06 Jan 2023 20:09:19 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Fri, 06 Jan 2023 20:09:25 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Fri, 06 Jan 2023 20:11:23 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Fri, 06 Jan 2023 20:11:30 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 06 Jan 2023 20:11:33 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 20:11:36 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 06 Jan 2023 20:11:39 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 06 Jan 2023 20:11:43 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 06 Jan 2023 20:11:46 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Fri, 06 Jan 2023 20:12:40 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 06 Jan 2023 20:12:43 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 06 Jan 2023 20:12:46 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 06 Jan 2023 20:12:49 GMT
USER adminer
# Fri, 06 Jan 2023 20:12:53 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:977ef99ba351dc6668a8aa09ee6ce134ad6e6d0d9cdf1083465b1effaa1969d2`  
		Last Modified: Wed, 21 Dec 2022 01:18:00 GMT  
		Size: 53.2 MB (53245083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c727f80356790b4fd9247593d5c85cfe42e070e1291f6769e90d0256c65710e1`  
		Last Modified: Fri, 06 Jan 2023 20:13:37 GMT  
		Size: 38.0 MB (37953652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674ea8f324ffc5bbce209caf0af212f0dbd6be82379773f31a4a8f763e336399`  
		Last Modified: Fri, 06 Jan 2023 20:13:09 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0c60b9b572e44c43a0de2558d566f10a975c9a11852cd28b75d5d341a55279`  
		Last Modified: Fri, 06 Jan 2023 20:13:56 GMT  
		Size: 2.7 KB (2718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69134700fa38743d3f4838a8f519ed4c1fb99d580850c42abe51cdbbe679b82`  
		Last Modified: Fri, 06 Jan 2023 20:13:55 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7e9aa5447bf49a6de7155363b5087b46f125da75f2a7449605282719ac744c`  
		Last Modified: Fri, 06 Jan 2023 20:13:56 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25084d0fb822db05890cf87a0efc05f11a50968978bffe65b881e398be9dfc00`  
		Last Modified: Fri, 06 Jan 2023 20:13:56 GMT  
		Size: 1.4 MB (1386140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1d094f25ab4e7c5f1ecde00c2499f8a3beb78ce48e19a5bef5fab00c1fed6e4`  
		Last Modified: Fri, 06 Jan 2023 20:13:56 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:7ef3d5acfd5d642f6646b19754bf119516baa24785aca3ba13eb8bb357ed777f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101229279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0103913f58c3f54a13927e8de909b9173d9600dd124cb85ccd96e46907419087`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 21 Dec 2022 01:17:21 GMT
ADD file:c95bdb0df70fa9ce48b31a7ceb8a7be0c5b925efcf01c43595868b86994dc192 in / 
# Wed, 21 Dec 2022 01:17:25 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 05:10:17 GMT
STOPSIGNAL SIGINT
# Fri, 06 Jan 2023 20:45:35 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Fri, 06 Jan 2023 20:45:38 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Fri, 06 Jan 2023 20:46:24 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Fri, 06 Jan 2023 20:46:26 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Fri, 06 Jan 2023 20:46:26 GMT
WORKDIR /var/www/html
# Fri, 06 Jan 2023 20:46:26 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Fri, 06 Jan 2023 20:46:27 GMT
ENV ADMINER_VERSION=4.8.1
# Fri, 06 Jan 2023 20:46:27 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Fri, 06 Jan 2023 20:46:28 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Fri, 06 Jan 2023 20:46:49 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Fri, 06 Jan 2023 20:46:49 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Fri, 06 Jan 2023 20:46:49 GMT
ENTRYPOINT ["entrypoint.sh"]
# Fri, 06 Jan 2023 20:46:50 GMT
USER adminer
# Fri, 06 Jan 2023 20:46:50 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:542880f4d15404af17d342ecbb76bb92724fc7cb8a91a5e18f26bd8f8811a38a`  
		Last Modified: Wed, 21 Dec 2022 01:22:46 GMT  
		Size: 58.9 MB (58897040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0799b781ce677e5c56f43e96eb2e9970451f76deadb2327a6a2734c37e17575`  
		Last Modified: Fri, 06 Jan 2023 20:47:33 GMT  
		Size: 40.9 MB (40939912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b4ac2fc935fdfffb06f463b45b30714ff8625267b8c4c47e7ceef708de23a26`  
		Last Modified: Fri, 06 Jan 2023 20:47:20 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b5fcbe2ee7909db7fafb9cce40e7154452e76fdac0714ba7d051a80250248c`  
		Last Modified: Fri, 06 Jan 2023 20:47:56 GMT  
		Size: 2.7 KB (2715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3c3c0e1fbdb327f4717d0de1ad48a88f7216c3c7e9afacc64c2b49a34ba72d`  
		Last Modified: Fri, 06 Jan 2023 20:47:56 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28d118ea358d2383c8ec7ab9ed699fcf6be74933a115bd5adcad50a174d94fb`  
		Last Modified: Fri, 06 Jan 2023 20:47:56 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44752f039b929ed7f9339e7d75e28bb30cd93921eef2f4ca07eeb2085999b86`  
		Last Modified: Fri, 06 Jan 2023 20:47:56 GMT  
		Size: 1.4 MB (1385366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c12a5b43dbf041d0d966caa747365607dc6922c99edcbb6a9bddd627de728b9`  
		Last Modified: Fri, 06 Jan 2023 20:47:56 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; s390x

```console
$ docker pull adminer@sha256:a1fa0d120584828c961ce0b29ab5d38c4bd62a7c4832051e8a59bdd185eaa72e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93404712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:078ace26e901a591bccbb767862313e0b30444a61969a6f9563f56d8172155d7`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 21 Dec 2022 01:42:51 GMT
ADD file:22c4f2d41083ce4433bec4a71e7e6ddc5bec8e44e9cf2c9f93d0874b5b4de7c3 in / 
# Wed, 21 Dec 2022 01:42:54 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:06:42 GMT
STOPSIGNAL SIGINT
# Wed, 21 Dec 2022 02:07:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:08:00 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 21 Dec 2022 02:08:48 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 21 Dec 2022 02:08:50 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 21 Dec 2022 02:08:51 GMT
WORKDIR /var/www/html
# Wed, 21 Dec 2022 02:08:51 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 21 Dec 2022 02:08:52 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 21 Dec 2022 02:08:53 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 21 Dec 2022 02:08:53 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 21 Dec 2022 02:09:20 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 21 Dec 2022 02:09:21 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 21 Dec 2022 02:09:21 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 21 Dec 2022 02:09:22 GMT
USER adminer
# Wed, 21 Dec 2022 02:09:23 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:7f45294776f4c97d23f8dbfca98d4b57701b478eedfcb154a7e7dc6d6954ba44`  
		Last Modified: Wed, 21 Dec 2022 01:48:50 GMT  
		Size: 53.3 MB (53258472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8610ee81c430b6503a5ee2d7cc451175bdfc868fc17ef5a675b43679da433867`  
		Last Modified: Wed, 21 Dec 2022 02:10:03 GMT  
		Size: 38.8 MB (38755148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211b726eee70a0c5ff85337d1e98c7987025435a41ca5421f47d96fc164b5b27`  
		Last Modified: Wed, 21 Dec 2022 02:09:56 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:548dc4ca6b10efd03438d3ef399c3d858053ec103194dba6350126f59b0cc988`  
		Last Modified: Wed, 21 Dec 2022 02:10:20 GMT  
		Size: 2.7 KB (2713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd20979228556508e9e2424f45667a2246d9c409f2557492271740f4840e889`  
		Last Modified: Wed, 21 Dec 2022 02:10:20 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e7ff5c1ff35711cc296fbbe902ca0db4bc13c6b5863ba4c3adc2640e16177e`  
		Last Modified: Wed, 21 Dec 2022 02:10:20 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334c0739b3be2b837dcd345afc1a5bd12f907a3080d438abf00d8706d01e99c8`  
		Last Modified: Wed, 21 Dec 2022 02:10:20 GMT  
		Size: 1.4 MB (1384126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd966444e211f7ff2ff5aca0482cee29884580acd8b4114e8bd25b616618c89c`  
		Last Modified: Wed, 21 Dec 2022 02:10:21 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
