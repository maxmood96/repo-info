## `adminer:latest`

```console
$ docker pull adminer@sha256:24ecd0f9bdc8124af6779181df2e5910c7f6aa07125f77215bd60c80e38dc6c0
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
$ docker pull adminer@sha256:0e5ecbdb8a261405b2b547358df7b761a754c576d9cb2f73aef78769080b203c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95960899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3f0dfcc2c9c983e68493a0ce1a9b7ca4d1a7e7a0b249e0fe8a8ce6d9df4c5d`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:32 GMT
ADD file:1bf1a123da85382e70ea251091b98fd8b4a1972e4c4e84d392443a4e20b7a135 in / 
# Tue, 13 Feb 2024 00:37:32 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:41:55 GMT
STOPSIGNAL SIGINT
# Tue, 13 Feb 2024 01:42:15 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:42:16 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 13 Feb 2024 01:42:17 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 13 Feb 2024 01:42:17 GMT
WORKDIR /var/www/html
# Tue, 13 Feb 2024 01:42:17 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 13 Feb 2024 01:42:17 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 13 Feb 2024 01:42:17 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 13 Feb 2024 01:42:18 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 13 Feb 2024 01:42:28 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 01:42:28 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 13 Feb 2024 01:42:29 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 13 Feb 2024 01:42:29 GMT
USER adminer
# Tue, 13 Feb 2024 01:42:29 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 13 Feb 2024 01:42:29 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:09e2bc8a597c33b54cccaf52f2e21798e2e0df79ab6cb33d3b1dfd4b33a57512`  
		Last Modified: Tue, 13 Feb 2024 00:42:21 GMT  
		Size: 55.1 MB (55084838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:092a59d5d6497166f3dbba32aa205aaa78ddfd080243695a000fc05b7988d184`  
		Last Modified: Tue, 13 Feb 2024 01:43:08 GMT  
		Size: 39.5 MB (39486506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4dca1b56763151283fbe5bc268620ccb9bca392661422e8628f497c3b6863dc`  
		Last Modified: Tue, 13 Feb 2024 01:43:01 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:378feffe51977bfd96a7127b85106e200b87c08cb026c8c356fce9d66e852b87`  
		Last Modified: Tue, 13 Feb 2024 01:43:00 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd4de3ac847581057ca572dc7430a2332990fe19c89a05bbec1b4ba5488f237`  
		Last Modified: Tue, 13 Feb 2024 01:43:00 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d5566ceca77acada33a7a73e873b8fda79e48ccd94d973d6872cefb4f90589`  
		Last Modified: Tue, 13 Feb 2024 01:43:01 GMT  
		Size: 1.4 MB (1385328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dafa7b9d4fc8fcfeaf4fa71f1c93dcec6586059a3e86724ad11bb070c228e09`  
		Last Modified: Tue, 13 Feb 2024 01:43:00 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; arm variant v5

```console
$ docker pull adminer@sha256:2a675273b58c369e23f41edecd39faa2a1f0fba59163530edc76fe54382fb2bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91223801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb04f56cc01d28f027940e99160466cfb1e3faf26c743ccef1bb964abd8121a8`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 12 Mar 2024 00:48:38 GMT
ADD file:e13a63ed3af4c4dcb74dfa2a2b12a285563b8c905dbac41b538492e1e100f93e in / 
# Tue, 12 Mar 2024 00:48:39 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:59:47 GMT
STOPSIGNAL SIGINT
# Tue, 12 Mar 2024 08:00:28 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 08:00:29 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 12 Mar 2024 08:00:30 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 12 Mar 2024 08:00:31 GMT
WORKDIR /var/www/html
# Tue, 12 Mar 2024 08:00:31 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 12 Mar 2024 08:00:31 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 12 Mar 2024 08:00:31 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 12 Mar 2024 08:00:31 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 12 Mar 2024 08:00:50 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Mar 2024 08:00:51 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 12 Mar 2024 08:00:51 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 12 Mar 2024 08:00:51 GMT
USER adminer
# Tue, 12 Mar 2024 08:00:51 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 12 Mar 2024 08:00:51 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:57e872a0ca7dbab84f7804705a96154de6b3cffcdb4f8946d4387764bfc1e307`  
		Last Modified: Tue, 12 Mar 2024 00:52:01 GMT  
		Size: 52.6 MB (52586778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46fef05abde7f7546bcf6aa4a5a743326f0406fa97e4cdca50db8a1c65a8ff2`  
		Last Modified: Tue, 12 Mar 2024 08:01:33 GMT  
		Size: 37.2 MB (37247610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c104cb471832f6d326ad627fa96dc2c1e597161ea2e40b7971d631f9ffaf0bb`  
		Last Modified: Tue, 12 Mar 2024 08:01:23 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0388dbb019094ae8162ab1b1ae67afd3b04b90aaa60b15e6b5c3cf7842420066`  
		Last Modified: Tue, 12 Mar 2024 08:01:23 GMT  
		Size: 1.9 KB (1868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c65be19b0bd2859b07e871fa1a1df4b000c20a969dafa2072b370893ad4e0c`  
		Last Modified: Tue, 12 Mar 2024 08:01:23 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9cb5105e06f2053df6c492b341c05514d7c86e86a1bf16ce6390f377288ac41`  
		Last Modified: Tue, 12 Mar 2024 08:01:24 GMT  
		Size: 1.4 MB (1385184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ef43a469894d4f04d1625c75f6bdf79bda40123f945947132979c6632e761e`  
		Last Modified: Tue, 12 Mar 2024 08:01:23 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; arm variant v7

```console
$ docker pull adminer@sha256:650ab18f06454b7cbce10d6bcea77bc5dad138c9d7a559ecf6fc3784cbb9bf48
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87819303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aefaf12409778aa84a6ac66a73428a7a4b85252fc19b0acf09dac3b388e8d4e6`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:25 GMT
ADD file:477c339ed6ec658bb1d0025e1568290c3cbbc98d9f973379f3133b83c2de9128 in / 
# Tue, 12 Mar 2024 00:59:28 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:31:44 GMT
STOPSIGNAL SIGINT
# Tue, 12 Mar 2024 02:32:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:32:10 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 12 Mar 2024 02:32:10 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 12 Mar 2024 02:32:11 GMT
WORKDIR /var/www/html
# Tue, 12 Mar 2024 02:32:11 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 12 Mar 2024 02:32:11 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 12 Mar 2024 02:32:11 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 12 Mar 2024 02:32:11 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 12 Mar 2024 02:32:23 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Mar 2024 02:32:23 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 12 Mar 2024 02:32:23 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 12 Mar 2024 02:32:23 GMT
USER adminer
# Tue, 12 Mar 2024 02:32:23 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 12 Mar 2024 02:32:23 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:ab40cb80ac5229a1c48dfbfe9aaa04da29109444982d90d4bca2c7b6842beceb`  
		Last Modified: Tue, 12 Mar 2024 01:03:56 GMT  
		Size: 50.2 MB (50241442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7327478c4231aa77cf7cab36cd2f0c3c0f9a6db93dfbf55e5c90cde6524bbe9`  
		Last Modified: Tue, 12 Mar 2024 02:33:03 GMT  
		Size: 36.2 MB (36188441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35d66055a894a3e6c6467b18c4eebfaae710cf56b2c0aa6de4cc2ecd1e0f31e`  
		Last Modified: Tue, 12 Mar 2024 02:32:55 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1dc3716909c2d734d6208a9c4c46d0c8b5c6ef3545f8f503de139cbd2e5b735`  
		Last Modified: Tue, 12 Mar 2024 02:32:55 GMT  
		Size: 1.9 KB (1870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a0d2c13616257d89bc6309af56fa661e59a92c1ad0150f3ce5b625c828114b`  
		Last Modified: Tue, 12 Mar 2024 02:32:55 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66e71c5c362e9bbf8b337b9978032c9601832657e03020633dc93f9425fcb45`  
		Last Modified: Tue, 12 Mar 2024 02:32:56 GMT  
		Size: 1.4 MB (1385190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55556fb0ee2109edd641e8ce3fc27f2179aa3d90fabe4104b86103ff25a34e2e`  
		Last Modified: Tue, 12 Mar 2024 02:32:55 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:c66e7a0383337888a5d3e7c0a98c5065d4e1eaccb856e8d754eb9ad32514ce58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94353371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3854c61dd35a611a16c83b21f6a28dc94d666b2cee6c51470ca02a92cdba870a`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:43 GMT
ADD file:7cb312b5f676a37f5c3172be6eb95e30986e5da0dcf21985d2176f8a9a037012 in / 
# Tue, 12 Mar 2024 00:45:44 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:22:42 GMT
STOPSIGNAL SIGINT
# Tue, 12 Mar 2024 01:23:03 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:23:04 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 12 Mar 2024 01:23:05 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 12 Mar 2024 01:23:05 GMT
WORKDIR /var/www/html
# Tue, 12 Mar 2024 01:23:05 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 12 Mar 2024 01:23:05 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 12 Mar 2024 01:23:05 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 12 Mar 2024 01:23:05 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 12 Mar 2024 01:23:16 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Mar 2024 01:23:16 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 12 Mar 2024 01:23:16 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 12 Mar 2024 01:23:16 GMT
USER adminer
# Tue, 12 Mar 2024 01:23:16 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 12 Mar 2024 01:23:16 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:f53ee134f2f58aa9d86f682cbedb185619a5b857474f430e6dc3384fafdec81c`  
		Last Modified: Tue, 12 Mar 2024 00:49:12 GMT  
		Size: 53.7 MB (53722099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736b482dff10e5ae34b256f9ed0b77b11b5035086d16b5d83dd547493a421e25`  
		Last Modified: Tue, 12 Mar 2024 01:23:50 GMT  
		Size: 39.2 MB (39241856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbc285c8fa7ada768fea15139bd3696c7a85037ad5509364ca3cc8edd38e1ed`  
		Last Modified: Tue, 12 Mar 2024 01:23:44 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02df7875cdf1d049f50b181d28e167b775621d5f8064fa973a7469d8f404a08`  
		Last Modified: Tue, 12 Mar 2024 01:23:44 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb37b99054a54e1e09c0622c46240ea0b21248a8e08bd86bed969b49bdf39672`  
		Last Modified: Tue, 12 Mar 2024 01:23:44 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01ed715c1eac9777380dbe6377aa83927423630c8195d018a5da35f776252bd`  
		Last Modified: Tue, 12 Mar 2024 01:23:44 GMT  
		Size: 1.4 MB (1385172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e47c569a290e69ed6824fd13e4efc527ef653772c82c35db720677cfaf29846`  
		Last Modified: Tue, 12 Mar 2024 01:23:44 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; 386

```console
$ docker pull adminer@sha256:c8c29f923cc0f3f09b340d148b4c998f4d1612ab1c7e85a0ce7fb870e69421c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (97004915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db520ffc677201b74c7f840d98a386863e98210a695df0968395d25008128677`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 12 Mar 2024 00:58:12 GMT
ADD file:e7e92b37650e4d33c3374ca47bc378c2b4e15f7c7e0a7c7fc659a29c5b3fc583 in / 
# Tue, 12 Mar 2024 00:58:12 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:37:48 GMT
STOPSIGNAL SIGINT
# Tue, 12 Mar 2024 07:38:20 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 07:38:21 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 12 Mar 2024 07:38:22 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 12 Mar 2024 07:38:22 GMT
WORKDIR /var/www/html
# Tue, 12 Mar 2024 07:38:22 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 12 Mar 2024 07:38:22 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 12 Mar 2024 07:38:22 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 12 Mar 2024 07:38:22 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 12 Mar 2024 07:38:36 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Mar 2024 07:38:37 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 12 Mar 2024 07:38:37 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 12 Mar 2024 07:38:37 GMT
USER adminer
# Tue, 12 Mar 2024 07:38:37 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 12 Mar 2024 07:38:37 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:ec2ed44737cc768246d63628c6de48f2d223cdb3a6c218bddd11786679e34647`  
		Last Modified: Tue, 12 Mar 2024 01:03:04 GMT  
		Size: 56.1 MB (56057973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b5b8a89beb8d9af3fd72c598548b86fb747e74608c80010d9da412be22ad3f1`  
		Last Modified: Tue, 12 Mar 2024 07:39:25 GMT  
		Size: 39.6 MB (39557502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0deeb7243b1ff117bee9da35536cde769f37e39536a2bc1403cc939fcaa09deb`  
		Last Modified: Tue, 12 Mar 2024 07:39:15 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae934c6d17132f012269200831b50c0f50ef6c7a6fde9ec6dc5b996787d0bd8`  
		Last Modified: Tue, 12 Mar 2024 07:39:15 GMT  
		Size: 1.9 KB (1862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7852183cf9986c73e8bf6a1fcd6e5705a861dd564b355987f12ffe1bbe9d02`  
		Last Modified: Tue, 12 Mar 2024 07:39:14 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a5ea3eb8e834bf72f33e1b6b6fd85b8ead3cf87040b8d11e87ddacefe9b7b2`  
		Last Modified: Tue, 12 Mar 2024 07:39:15 GMT  
		Size: 1.4 MB (1385219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca38217a696a8c1c5fac54611582893687cf07c4f4b7ef135b4d9abc7d074927`  
		Last Modified: Tue, 12 Mar 2024 07:39:15 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; mips64le

```console
$ docker pull adminer@sha256:dce4d8ba1a894b92cf98746f9564e5b1e706d3e4968e725c42f48ea9c44536cf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92646789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0171d393ed6deda21436755d8da4774db76f0134784a276e5ea87c7b07771af`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 12 Mar 2024 01:06:53 GMT
ADD file:ceaac889009e9d867969b5a568939eb0f6e136303e3438d9747193d6ef4755ab in / 
# Tue, 12 Mar 2024 01:06:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:57:07 GMT
STOPSIGNAL SIGINT
# Tue, 12 Mar 2024 01:59:04 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:59:10 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 12 Mar 2024 01:59:17 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 12 Mar 2024 01:59:20 GMT
WORKDIR /var/www/html
# Tue, 12 Mar 2024 01:59:23 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 12 Mar 2024 01:59:27 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 12 Mar 2024 01:59:30 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 12 Mar 2024 01:59:33 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 12 Mar 2024 02:00:25 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Mar 2024 02:00:28 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 12 Mar 2024 02:00:31 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 12 Mar 2024 02:00:34 GMT
USER adminer
# Tue, 12 Mar 2024 02:00:38 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 12 Mar 2024 02:00:41 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:3856c0b5cf8a29fd86ef6fe0c2a36a38020518c2e120457769b9044974ec1ca8`  
		Last Modified: Tue, 12 Mar 2024 01:17:56 GMT  
		Size: 53.3 MB (53303519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cec6da94bd0c183de93bb08aac547c356f09e634431834b4dfd1df66fd16c7`  
		Last Modified: Tue, 12 Mar 2024 02:03:08 GMT  
		Size: 38.0 MB (37952997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c8e5180951d1e6bd7af5bdc785b54eea4aa18aee55ac41064a79a214bd0fdb`  
		Last Modified: Tue, 12 Mar 2024 02:02:41 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c540ddcd4638c076d8b2a563f26fb73b202dcddb991c19bad4f1914181be07e`  
		Last Modified: Tue, 12 Mar 2024 02:02:41 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a760d93c3323fc8cc42f59f6a2ee5d3513c1cfdf82a68310d1b988e4b0cad797`  
		Last Modified: Tue, 12 Mar 2024 02:02:41 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de20c912e5fd9033668584e42d14a0aa3d0ef908619cb0aafb008d0593c0e97`  
		Last Modified: Tue, 12 Mar 2024 02:02:42 GMT  
		Size: 1.4 MB (1386185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d59e50593c5cdbb265e3771a5eaeee0ea6cd974f7d8dd7944bc9aa31e2961a82`  
		Last Modified: Tue, 12 Mar 2024 02:02:42 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; ppc64le

```console
$ docker pull adminer@sha256:841d2cfd7ee3db01d2884711327fe749d9a095b0d5975e10a97f9f540e49c799
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101287531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7cd215c84c4492b55bf4fdfc2f23cc6b1afad3c91877d6dcc548d5d6b80be49`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:15 GMT
ADD file:de34873811ec1071766dcf77b8d1180714c8e5b4373bed3aaf9a9e742ade2fee in / 
# Tue, 13 Feb 2024 00:39:19 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:24:00 GMT
STOPSIGNAL SIGINT
# Tue, 13 Feb 2024 01:24:58 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:25:01 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 13 Feb 2024 01:25:03 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 13 Feb 2024 01:25:03 GMT
WORKDIR /var/www/html
# Tue, 13 Feb 2024 01:25:04 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 13 Feb 2024 01:25:04 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 13 Feb 2024 01:25:05 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 13 Feb 2024 01:25:06 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 13 Feb 2024 01:25:30 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 01:25:31 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 13 Feb 2024 01:25:31 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 13 Feb 2024 01:25:31 GMT
USER adminer
# Tue, 13 Feb 2024 01:25:31 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 13 Feb 2024 01:25:32 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:5b3ca2d45f6b2df666b88854e431316a856c6ecacdd29894dd599694e415a1eb`  
		Last Modified: Tue, 13 Feb 2024 00:44:22 GMT  
		Size: 59.0 MB (58954488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e029c5ea562dd6d357c1bed2443ac90c451b2253527daa6b56663826d249ad4e`  
		Last Modified: Tue, 13 Feb 2024 01:26:39 GMT  
		Size: 40.9 MB (40943323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e511f8603016ae4f5e261cad68ea477938c886b5b18dfc125a8e3bb6bce7c957`  
		Last Modified: Tue, 13 Feb 2024 01:26:30 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d17898a24037ab93703e6a805aa2fff6aa00cdd6ba28b7b41275d3ee89293d`  
		Last Modified: Tue, 13 Feb 2024 01:26:30 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585d75275ea78c8cb343d199810488890933fce25ed6581e4acf145ceb42f0b1`  
		Last Modified: Tue, 13 Feb 2024 01:26:30 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb9a764172cb7d8d02d1924bbf9beb0f365c758bf559c5be692a88b574b6fb0`  
		Last Modified: Tue, 13 Feb 2024 01:26:30 GMT  
		Size: 1.4 MB (1385478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b57d2c3a064263f5b2cebb6c3fd2b1a35746cf7e5b904ab67d2e46ac3f61c35`  
		Last Modified: Tue, 13 Feb 2024 01:26:30 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; s390x

```console
$ docker pull adminer@sha256:6663ebab729ccd738428d780108a6be5d91354df73f9e4eac1dc2a738e91e1fa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93734101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:415a5db9954bbf85a83602d6b83d74e9b3c5507aa8f276b2a2b3dbf9bd993236`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 13 Feb 2024 01:03:43 GMT
ADD file:baaec0dbf612f7bd9d783527a940d73b2148b2ceb1e6770a7be62a51d3bc72e8 in / 
# Tue, 13 Feb 2024 01:03:46 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:16:26 GMT
STOPSIGNAL SIGINT
# Tue, 13 Feb 2024 04:16:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 04:17:03 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 13 Feb 2024 04:17:04 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 13 Feb 2024 04:17:04 GMT
WORKDIR /var/www/html
# Tue, 13 Feb 2024 04:17:05 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 13 Feb 2024 04:17:05 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 13 Feb 2024 04:17:05 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 13 Feb 2024 04:17:06 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 13 Feb 2024 04:17:18 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 04:17:19 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 13 Feb 2024 04:17:19 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 13 Feb 2024 04:17:20 GMT
USER adminer
# Tue, 13 Feb 2024 04:17:20 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 13 Feb 2024 04:17:20 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:75a00755bfcec7b096a7f2fdb8374002f3bbc7076571213a985c40116dbabb6a`  
		Last Modified: Tue, 13 Feb 2024 01:30:37 GMT  
		Size: 53.3 MB (53319325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:112506421ca98b25ac74bb82254c5406cab8eea61fb8d62db39073657f432759`  
		Last Modified: Tue, 13 Feb 2024 04:20:04 GMT  
		Size: 39.0 MB (39025245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c10724d9fbf328dd1ef3e8442af2f41eb0a3c6b7026b365af89ae6404d73c7cf`  
		Last Modified: Tue, 13 Feb 2024 04:19:56 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:950b46a79ea3f5ab31e90c7bb922768c5725785186cb08e9224ba10c8d6d2fb3`  
		Last Modified: Tue, 13 Feb 2024 04:19:56 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1d7e14a13577e5955894da82fdb5ba23527c26f6bab2ff867be0b0e7ab51cb`  
		Last Modified: Tue, 13 Feb 2024 04:19:57 GMT  
		Size: 1.5 KB (1479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2d41a4c4deb028de4ced44d1f8757ec4e964ba269512418c952b390b380e35`  
		Last Modified: Tue, 13 Feb 2024 04:19:57 GMT  
		Size: 1.4 MB (1385292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d0213ea52d6e34ca60f042ed0708d943eaad299857bbc5e4434b8788366f548`  
		Last Modified: Tue, 13 Feb 2024 04:19:56 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
