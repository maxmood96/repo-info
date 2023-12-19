## `adminer:fastcgi`

```console
$ docker pull adminer@sha256:2a52370d3468f53419bae781d9c398a6efd685b818c7f1e544f8f439438023c3
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
$ docker pull adminer@sha256:ecffcf061b2447af183b7d7485d66e51df88ef86a6d7168dfd09725e5ef9e231
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95944646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be2570f656a71b1e6ecbced6b045682ecc01aeae88c65caa424fc200fa7cab3d`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:38 GMT
ADD file:d3a2f1f42338ba7066e352cea3b7bf4c7576e6b96fef785e8da763114f337c0e in / 
# Tue, 19 Dec 2023 01:20:38 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:28:09 GMT
STOPSIGNAL SIGINT
# Tue, 19 Dec 2023 04:28:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:28:31 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 19 Dec 2023 04:28:50 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 19 Dec 2023 04:28:51 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 19 Dec 2023 04:28:51 GMT
WORKDIR /var/www/html
# Tue, 19 Dec 2023 04:28:51 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 19 Dec 2023 04:28:51 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 19 Dec 2023 04:28:51 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 19 Dec 2023 04:28:51 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 19 Dec 2023 04:29:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 19 Dec 2023 04:29:02 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 19 Dec 2023 04:29:03 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 19 Dec 2023 04:29:03 GMT
USER adminer
# Tue, 19 Dec 2023 04:29:03 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:18f2c3b7ca52caba205d748b9ce41784eb010ca83ece9e84e2a09130a5ec3cbc`  
		Last Modified: Tue, 19 Dec 2023 01:25:17 GMT  
		Size: 55.1 MB (55057340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bad63e83ac4c7f1414e4ccf6b362fac0878f822163680267ba24479578ac9401`  
		Last Modified: Tue, 19 Dec 2023 04:29:21 GMT  
		Size: 39.5 MB (39493907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:166c45dad258f94381476c950ee7ef88d72c5fda27a88c3ad91ca7c10521feca`  
		Last Modified: Tue, 19 Dec 2023 04:29:14 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c51703986aeb172fe0a74c01cfae3eff9f1fbf7ee06cdb76f3d4da85088272`  
		Last Modified: Tue, 19 Dec 2023 04:29:41 GMT  
		Size: 2.7 KB (2707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029b17d8f7d1da624fdb2eda1fa19be485ebd308707c60b1cade335f26059635`  
		Last Modified: Tue, 19 Dec 2023 04:29:41 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4df3d971b8d50e1ea223e6965c54ce4d167a984909306eeb885c4db4fb76ccf`  
		Last Modified: Tue, 19 Dec 2023 04:29:41 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f19f5a53e58409d1d2553b08bc60c1ef95e3be53461bc9467c7e2cf6065ded`  
		Last Modified: Tue, 19 Dec 2023 04:29:41 GMT  
		Size: 1.4 MB (1386456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c6b58918c3de8b6ef21fbf9b55bb6b70c7898b125c18bf1ae2cae20356fb0f`  
		Last Modified: Tue, 19 Dec 2023 04:29:41 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; arm variant v5

```console
$ docker pull adminer@sha256:fbd2ae4e63153cc394ab1f5129d382f01a4d60e4692ee74b315f8ec99732ab24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91208109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d097ac01b417768fc08ced8789fbb910712d69aa71bb0c2039db0b7a609c753`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 19 Dec 2023 01:55:29 GMT
ADD file:10a67a16f03367965d9105db3d368f8cf27493769f1551c2bfdc274485bd7f6d in / 
# Tue, 19 Dec 2023 01:55:30 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 05:19:19 GMT
STOPSIGNAL SIGINT
# Tue, 19 Dec 2023 05:19:48 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 05:19:49 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 19 Dec 2023 05:20:08 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 19 Dec 2023 05:20:09 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 19 Dec 2023 05:20:09 GMT
WORKDIR /var/www/html
# Tue, 19 Dec 2023 05:20:09 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 19 Dec 2023 05:20:09 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 19 Dec 2023 05:20:09 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 19 Dec 2023 05:20:09 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 19 Dec 2023 05:20:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 19 Dec 2023 05:20:23 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 19 Dec 2023 05:20:23 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 19 Dec 2023 05:20:23 GMT
USER adminer
# Tue, 19 Dec 2023 05:20:23 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:476954b0dbc0bbf3e36983f98ae01dfefa01670a85ffcb7ed6916095b71bdd38`  
		Last Modified: Tue, 19 Dec 2023 01:58:55 GMT  
		Size: 52.6 MB (52562242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44cc4eabb8ab5cb58a1f898eb13f385aed7944d04795cc8f88496258b490372`  
		Last Modified: Tue, 19 Dec 2023 05:20:44 GMT  
		Size: 37.3 MB (37252666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10250a7e9e6e5bf39a628a4d1b5d5bfade40db8d12fcdff38e7f70451f7b90af`  
		Last Modified: Tue, 19 Dec 2023 05:20:34 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b87530626f18a53ee8260143083b979055ed0c9c8e0160b9b6a2123ffd62f23`  
		Last Modified: Tue, 19 Dec 2023 05:21:01 GMT  
		Size: 2.7 KB (2715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753161226bcb1736ef481c0a9490a8ddfb3a664eaa326d3e8e318cdb9c9966e6`  
		Last Modified: Tue, 19 Dec 2023 05:21:01 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a407c614de2b88fc3d2bbe0f20ae3a7a40e80e04fcb6170906e6f87061ee57`  
		Last Modified: Tue, 19 Dec 2023 05:21:01 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5490e8fd9fae149307398b9fc21fb78265b806a07cd8eb9a15d924f8f477f298`  
		Last Modified: Tue, 19 Dec 2023 05:21:01 GMT  
		Size: 1.4 MB (1386252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c3d55e579d7403aaa4cb5efbd235185df23dbde1af330f90a923d796ee2e91`  
		Last Modified: Tue, 19 Dec 2023 05:21:01 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:6f7ff8fc0b37dd4be271500ab853b0dbd47fd4e8b1c997ade3323027b7b872ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87800128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad4f351ecc4d4148c5bebb4c1e209020fb41efb5eda96d86640c83a8282435eb`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 19 Dec 2023 02:07:59 GMT
ADD file:3b623bed8ec2536cb513edda1de6f79d2c8e06d6f82df2543202544dbba3ae3e in / 
# Tue, 19 Dec 2023 02:08:00 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 08:23:04 GMT
STOPSIGNAL SIGINT
# Tue, 19 Dec 2023 08:23:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 08:23:37 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 19 Dec 2023 08:23:52 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 19 Dec 2023 08:23:53 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 19 Dec 2023 08:23:53 GMT
WORKDIR /var/www/html
# Tue, 19 Dec 2023 08:23:53 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 19 Dec 2023 08:23:53 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 19 Dec 2023 08:23:53 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 19 Dec 2023 08:23:54 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 19 Dec 2023 08:24:05 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 19 Dec 2023 08:24:05 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 19 Dec 2023 08:24:05 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 19 Dec 2023 08:24:05 GMT
USER adminer
# Tue, 19 Dec 2023 08:24:05 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:1b42212018867046767b36eb95cf15c4b66bbb7b4fb552aab446d9822de5765c`  
		Last Modified: Tue, 19 Dec 2023 02:12:11 GMT  
		Size: 50.2 MB (50215775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af1df80133b5abe2a3bdb18a519e0d9a46ff65f6d03be8112f7f5d17bbf258f`  
		Last Modified: Tue, 19 Dec 2023 08:24:25 GMT  
		Size: 36.2 MB (36191039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5512945806d39a0f111223c3d619a80e6f2d05ee09e6303ba271d6d978eda49`  
		Last Modified: Tue, 19 Dec 2023 08:24:16 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc25350c278915f9eb90006f2a783aaeb87e97fd89e7a819a3d97bec04100ba`  
		Last Modified: Tue, 19 Dec 2023 08:24:42 GMT  
		Size: 2.7 KB (2707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d516b60c95a5c36ab740d93c6b780a6f42e7f5ac62ff3a36de7d8294423634f7`  
		Last Modified: Tue, 19 Dec 2023 08:24:42 GMT  
		Size: 1.9 KB (1872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f2e499612c82aa03810c3b7ba32dee2bf8aae50a47d9482e9b5fb7ec02f4c9d`  
		Last Modified: Tue, 19 Dec 2023 08:24:42 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93798858f449d0aa60e747f3e22ebf27ca3017a12478a51e882acce9914df7c8`  
		Last Modified: Tue, 19 Dec 2023 08:24:43 GMT  
		Size: 1.4 MB (1386377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29a4a53e47b6a1009955858f82c7f9ae13cea628520db4f56fefd18e8438350`  
		Last Modified: Tue, 19 Dec 2023 08:24:42 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:c86948aaf6df7fbdadf205c5254844a019ab3569336c18db0b965393b16b82f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94349272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d1ae5f2851f1020fdc18055484257e02ac52ef94c7b0433f9f2615d721058b`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:17 GMT
ADD file:06ba7e39a2f8e1a7bcbb929fa9d1e6fb1f8bdcf5096dc903576af8f7014e353b in / 
# Tue, 19 Dec 2023 01:41:18 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:49:50 GMT
STOPSIGNAL SIGINT
# Tue, 19 Dec 2023 06:50:08 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 06:50:09 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 19 Dec 2023 06:50:24 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 19 Dec 2023 06:50:24 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 19 Dec 2023 06:50:24 GMT
WORKDIR /var/www/html
# Tue, 19 Dec 2023 06:50:24 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 19 Dec 2023 06:50:24 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 19 Dec 2023 06:50:24 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 19 Dec 2023 06:50:24 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 19 Dec 2023 06:50:34 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 19 Dec 2023 06:50:34 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 19 Dec 2023 06:50:34 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 19 Dec 2023 06:50:34 GMT
USER adminer
# Tue, 19 Dec 2023 06:50:34 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:396a672fee8bade1a7c9f228d919717447f110f39046d8b5ed21ad45ae13ab61`  
		Last Modified: Tue, 19 Dec 2023 01:44:57 GMT  
		Size: 53.7 MB (53708091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ed26c5188b9e4a04138b32bfd04e17c836f5b1efc61588c60d5bc52345a16c`  
		Last Modified: Tue, 19 Dec 2023 06:50:51 GMT  
		Size: 39.2 MB (39247941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fe407ff0bf13ebf2f07e204841637120d4ecbcad377fd08216b87b29881b08`  
		Last Modified: Tue, 19 Dec 2023 06:50:44 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7954febc4f4ffcd31b9f51d780d120ccea413583e614f3ec1099f49233381eea`  
		Last Modified: Tue, 19 Dec 2023 06:51:08 GMT  
		Size: 2.7 KB (2711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bad03b64ebffae9482028f8bde5f82d0b92306b09330264310cf949db21d11`  
		Last Modified: Tue, 19 Dec 2023 06:51:08 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae31011965e712d6a890af97e5de5701d1f2ab2b0a649cb465e50f6b4600413`  
		Last Modified: Tue, 19 Dec 2023 06:51:08 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db41c67c6d0220362b704a4dac4afa835434ad01e16a5869b7a0560bcc9809d3`  
		Last Modified: Tue, 19 Dec 2023 06:51:08 GMT  
		Size: 1.4 MB (1386291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3885fffcf95a3af285e6c65db5277cad29c1dca4a1d7f1177d5e603c825f97cf`  
		Last Modified: Tue, 19 Dec 2023 06:51:08 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:93f1fa28e99c94e12475feb6f31a1855b4a5903efec1a25fc3a65f72517c3c0f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (97001695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f83692269a7c73907fcf10e8b1f9bb7218447f62eb4ff932ce737877d537b7fe`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 19 Dec 2023 01:39:19 GMT
ADD file:8a328fced7ae3a6fc868bbb95c23191103e595c9d22b2626c16f155bc48b51a8 in / 
# Tue, 19 Dec 2023 01:39:20 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 03:22:24 GMT
STOPSIGNAL SIGINT
# Tue, 19 Dec 2023 03:22:52 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 03:22:53 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 19 Dec 2023 03:23:12 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 19 Dec 2023 03:23:13 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 19 Dec 2023 03:23:13 GMT
WORKDIR /var/www/html
# Tue, 19 Dec 2023 03:23:13 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 19 Dec 2023 03:23:13 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 19 Dec 2023 03:23:14 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 19 Dec 2023 03:23:14 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 19 Dec 2023 03:23:27 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 19 Dec 2023 03:23:27 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 19 Dec 2023 03:23:27 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 19 Dec 2023 03:23:27 GMT
USER adminer
# Tue, 19 Dec 2023 03:23:27 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:a789657fd5416b1ccfd519597a8f5e57bd5a80d04d1b1b7b2770df4469f4dd44`  
		Last Modified: Tue, 19 Dec 2023 01:44:07 GMT  
		Size: 56.0 MB (56046336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036f0911d89d9e328491b83337936442eb0490afd3a8124ae61ff283dcef35f8`  
		Last Modified: Tue, 19 Dec 2023 03:23:51 GMT  
		Size: 39.6 MB (39562137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f22576bb4fcebae9c7f3032c0595103daa8f7aca1cc64ad6afe41b296d7e49b`  
		Last Modified: Tue, 19 Dec 2023 03:23:39 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc92207d59106ae41cf325d4717a869fd9d17cea9b44feeeb857d478367f1a0`  
		Last Modified: Tue, 19 Dec 2023 03:24:10 GMT  
		Size: 2.7 KB (2704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94174952ac40de7ac594f60f77a9ab58b0cb8eca9903fb41a2077ed2ca2b5746`  
		Last Modified: Tue, 19 Dec 2023 03:24:10 GMT  
		Size: 1.9 KB (1872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac28965620d25b83faafc48c256044084cc56b9c709c45c63468f090b06967c`  
		Last Modified: Tue, 19 Dec 2023 03:24:10 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a023732839a480d5ebabc99956d18a5f247c9dfe11e53ebeb89564e44f72545b`  
		Last Modified: Tue, 19 Dec 2023 03:24:10 GMT  
		Size: 1.4 MB (1386291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e03d446b6bc8a7c192ecaca8154a692f5cf526ab8891186848cd2b7f04dfd08`  
		Last Modified: Tue, 19 Dec 2023 03:24:10 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; mips64le

```console
$ docker pull adminer@sha256:a764c136226771f05874d428d466ab7617443109af05761f5a301d774d3d78ef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92637624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dcb8d7570466b2e24f152459f05444501a2db6bec81dd770f36a922da335bf3`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 21 Nov 2023 04:10:25 GMT
ADD file:dbfc3d226166089c4db0c154fdcea8049b8758c6812f1c397dec1444985e8557 in / 
# Tue, 21 Nov 2023 04:10:31 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:14:44 GMT
STOPSIGNAL SIGINT
# Tue, 21 Nov 2023 12:16:43 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:16:50 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 21 Nov 2023 12:18:45 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 21 Nov 2023 12:18:52 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 21 Nov 2023 12:18:55 GMT
WORKDIR /var/www/html
# Tue, 21 Nov 2023 12:18:59 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 21 Nov 2023 12:19:02 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 21 Nov 2023 12:19:05 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 21 Nov 2023 12:19:09 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 21 Nov 2023 12:20:00 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Nov 2023 12:20:03 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 21 Nov 2023 12:20:06 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 21 Nov 2023 12:20:10 GMT
USER adminer
# Tue, 21 Nov 2023 12:20:13 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:ca31218601e95f4aafae0dcadda7600aeb04db374e1e829d5c123f8033ba3472`  
		Last Modified: Tue, 21 Nov 2023 04:21:21 GMT  
		Size: 53.3 MB (53289162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d172a1ce4463b8a1bb14b88d9f7c98a7f06f260dfc2849e77f3d41be6d17db9`  
		Last Modified: Tue, 21 Nov 2023 12:21:00 GMT  
		Size: 38.0 MB (37954467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd3b039fbc0efa77466cfb045c80c120d45355cf2db0dd6533eeb1cee6296e1`  
		Last Modified: Tue, 21 Nov 2023 12:20:33 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:873ce81c2a5a659c6ba90c59b5fdd1a3c215439a655c8efe1b62a042ba6dc956`  
		Last Modified: Tue, 21 Nov 2023 12:21:19 GMT  
		Size: 2.7 KB (2714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046c3c9cda84191a448b5676717eb2efd43aa616bd1a7936fd1ffa7333fe414d`  
		Last Modified: Tue, 21 Nov 2023 12:21:19 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5fb1a0ccda92972577970b93a35e31e87aca9efdf320fe33d64fbb50e5f5be`  
		Last Modified: Tue, 21 Nov 2023 12:21:19 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f226ce3836498318ee4d4f1573efc49e08a2a6cdfd7403a3089f66f24194f3`  
		Last Modified: Tue, 21 Nov 2023 12:21:20 GMT  
		Size: 1.4 MB (1387178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2ef37541c711003007d218f46c929098bfda475d45d9ced2d3700246c0d143`  
		Last Modified: Tue, 21 Nov 2023 12:21:19 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:988a50cb007ef650a43dfb195f4730d2268d36b717db2cdbc731914c725ee8df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101268149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e2a636068dd83fb84a9bcecd6a718528598da747489d7573b02bdfa6f20140`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 21 Nov 2023 04:24:26 GMT
ADD file:c21c2b6cb3f9bdf6cc3641e9ebf810a461174480c6cd1c25515cf9fce4aa2143 in / 
# Tue, 21 Nov 2023 04:24:30 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 06:49:59 GMT
STOPSIGNAL SIGINT
# Tue, 21 Nov 2023 06:50:40 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 06:50:42 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 21 Nov 2023 06:51:10 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 21 Nov 2023 06:51:11 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 21 Nov 2023 06:51:11 GMT
WORKDIR /var/www/html
# Tue, 21 Nov 2023 06:51:12 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 21 Nov 2023 06:51:12 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 21 Nov 2023 06:51:12 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 21 Nov 2023 06:51:13 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 21 Nov 2023 06:51:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 21 Nov 2023 06:51:30 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 21 Nov 2023 06:51:30 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 21 Nov 2023 06:51:31 GMT
USER adminer
# Tue, 21 Nov 2023 06:51:31 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:23ebe74b854f8f6e2671f4c8cc147a6925fb7d929ce5898f7ca2af9781bf7d38`  
		Last Modified: Tue, 21 Nov 2023 04:29:21 GMT  
		Size: 58.9 MB (58929678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa255108512a37e57b2fdf827a0fdb4e3783a0649fb80ecdd431d4921dd6761c`  
		Last Modified: Tue, 21 Nov 2023 06:51:51 GMT  
		Size: 40.9 MB (40945122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5862ce535fc870ad9665c04e9816effde44c5f4469bc852265ba0bfe11ad7001`  
		Last Modified: Tue, 21 Nov 2023 06:51:41 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb07c0427e1d513dc1c2e122ef9b33a7ce04c7f6e7ac25eb3cdc16b7c4f3dd0`  
		Last Modified: Tue, 21 Nov 2023 06:52:10 GMT  
		Size: 2.7 KB (2709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1a3baf382e8ecd698319193729a0416bcdcbe069383e956a41029751483ab8`  
		Last Modified: Tue, 21 Nov 2023 06:52:10 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd36769ccabc572d519d259cd2369096462f35a823d2817c593ce165f30f690b`  
		Last Modified: Tue, 21 Nov 2023 06:52:10 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35256cd8ee36eeca9a95cc2fc4ad45b213f5025c0d7211c00f76beae6c7a0bd`  
		Last Modified: Tue, 21 Nov 2023 06:52:11 GMT  
		Size: 1.4 MB (1386400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417adc53867ad9b9d99a43bc9736c1285bc9af029e2938bd516928b92cad7093`  
		Last Modified: Tue, 21 Nov 2023 06:52:10 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:fastcgi` - linux; s390x

```console
$ docker pull adminer@sha256:b8b4ac1fe36076d5371a3bf6991390733f61881bc02d372307941aef51d585f1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93711502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6406292eecf977cb8e125b20b91e6387d2005d83a25b078cc21cc24d7509c083`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Tue, 19 Dec 2023 01:42:51 GMT
ADD file:f3ff7311d9c8e7c83e0b7746d9402fed156fb05bd0c704d49535b4ece7f33177 in / 
# Tue, 19 Dec 2023 01:42:55 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 08:25:25 GMT
STOPSIGNAL SIGINT
# Tue, 19 Dec 2023 08:25:42 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 08:25:45 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 19 Dec 2023 08:26:05 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Tue, 19 Dec 2023 08:26:05 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 19 Dec 2023 08:26:05 GMT
WORKDIR /var/www/html
# Tue, 19 Dec 2023 08:26:05 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 19 Dec 2023 08:26:06 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 19 Dec 2023 08:26:06 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 19 Dec 2023 08:26:06 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 19 Dec 2023 08:26:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 19 Dec 2023 08:26:13 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 19 Dec 2023 08:26:14 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 19 Dec 2023 08:26:14 GMT
USER adminer
# Tue, 19 Dec 2023 08:26:14 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:a7334865824cce0a21e0af9d1f48eaee160e0ac01a54ca220a9814e8d2059646`  
		Last Modified: Tue, 19 Dec 2023 01:47:52 GMT  
		Size: 53.3 MB (53295959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3db6dd567b86ae988b6977d7df33d24408ada7139b6210b245b6d6464c6158`  
		Last Modified: Tue, 19 Dec 2023 08:26:36 GMT  
		Size: 39.0 MB (39022207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af1c9faf2e463f5a5ccb69a266a470708823f07bf1ac960f8a0628274872110`  
		Last Modified: Tue, 19 Dec 2023 08:26:29 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9515c9eb7f9e6342e26a1fe0143791b49ecea09f58f22428ec4b597ac7b6032f`  
		Last Modified: Tue, 19 Dec 2023 08:26:48 GMT  
		Size: 2.7 KB (2708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3cb387b7491b6c48ae9693356c4493882e4d52f8747e60e24048989ce8ea42`  
		Last Modified: Tue, 19 Dec 2023 08:26:48 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5628d53f2ccb28aeef7cc65795794a583710f953a4d27ce8d499ce406b69afe`  
		Last Modified: Tue, 19 Dec 2023 08:26:48 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65834c3b46ae5d4570526bdd0b94200771afa92ae3bd679c9f7ebf508d4cc27e`  
		Last Modified: Tue, 19 Dec 2023 08:26:48 GMT  
		Size: 1.4 MB (1386385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214052d32954bb84ad11fd22cffd42bf6d5502c7119a413917833d8979602342`  
		Last Modified: Tue, 19 Dec 2023 08:26:48 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
