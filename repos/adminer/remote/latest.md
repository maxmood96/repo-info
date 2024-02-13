## `adminer:latest`

```console
$ docker pull adminer@sha256:43ff0c22c20aa2b6b3c0c51711cc61c420dc9af8a50c206aa9c8a3dfc0ebc1b9
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
$ docker pull adminer@sha256:eca896f1c1523108500905e8d082aba8d1c63d649597fdbe9adae6a4c85ec3ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91223872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0425b17536d2a93709c9bbd94baf6566963a9d3698ab0554b0a1edd5d4e509`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 13 Feb 2024 01:08:36 GMT
ADD file:e60f5be11728cbf36bc5b1ee8a186ec55fb8e6bbc13d939c76ff03e91e934e90 in / 
# Tue, 13 Feb 2024 01:08:37 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:59:44 GMT
STOPSIGNAL SIGINT
# Tue, 13 Feb 2024 02:00:54 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:00:55 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 13 Feb 2024 02:00:57 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 13 Feb 2024 02:00:57 GMT
WORKDIR /var/www/html
# Tue, 13 Feb 2024 02:00:57 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 13 Feb 2024 02:00:57 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 13 Feb 2024 02:00:58 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 13 Feb 2024 02:00:58 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 13 Feb 2024 02:01:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 02:01:21 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 13 Feb 2024 02:01:21 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 13 Feb 2024 02:01:21 GMT
USER adminer
# Tue, 13 Feb 2024 02:01:22 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 13 Feb 2024 02:01:22 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:bbf2c22df990ef0a734a6681b9078a2b5c2ea21e9fee5c8e62c2171859d433d8`  
		Last Modified: Tue, 13 Feb 2024 01:13:53 GMT  
		Size: 52.6 MB (52586881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ddd64715bfc7a52ee47ef33638aa50b6ddc9a1e9f7bf68b142adf6d33cf3d6`  
		Last Modified: Tue, 13 Feb 2024 02:02:41 GMT  
		Size: 37.2 MB (37247477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804bae3b0b7a6e38bf57f209d3381cca9d6b31c79e63ef481710d5c6b1241eb8`  
		Last Modified: Tue, 13 Feb 2024 02:02:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e847d5e81bfa005890ee60ac3ace2d7f6ce513c9e5be5be6f822e39b2d4b724`  
		Last Modified: Tue, 13 Feb 2024 02:02:30 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce524bcf84caecbaf9cc459fe8df84621ece8e1cc496fe665a0faa91df23ca0d`  
		Last Modified: Tue, 13 Feb 2024 02:02:30 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8fab0a3896f357c8f36f1fb2993cf231cedc396de1c1c7cacbec5fe9847cc31`  
		Last Modified: Tue, 13 Feb 2024 02:02:30 GMT  
		Size: 1.4 MB (1385281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8765eb30ce13099878b709a2853475428b1e6b6ee75f2b33a2f7b93f976496b8`  
		Last Modified: Tue, 13 Feb 2024 02:02:30 GMT  
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
$ docker pull adminer@sha256:e9017710135541f33284a212e236596e33c3f187fbca6deb0fbdf8b742f0ee42
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94352379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05eadd03e3f770f612d45caef2366e819c50e379df657ec77564ac803344a670`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:27 GMT
ADD file:46791e28a2eef97a17393ff5cf2928d2e721f9380340a34c7d2e85053edec7c1 in / 
# Tue, 13 Feb 2024 00:41:27 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:35:35 GMT
STOPSIGNAL SIGINT
# Tue, 13 Feb 2024 01:35:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:35:54 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 13 Feb 2024 01:35:54 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 13 Feb 2024 01:35:54 GMT
WORKDIR /var/www/html
# Tue, 13 Feb 2024 01:35:55 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 13 Feb 2024 01:35:55 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 13 Feb 2024 01:35:55 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 13 Feb 2024 01:35:55 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 13 Feb 2024 01:36:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 01:36:06 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 13 Feb 2024 01:36:06 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 13 Feb 2024 01:36:06 GMT
USER adminer
# Tue, 13 Feb 2024 01:36:06 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 13 Feb 2024 01:36:06 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:4245faf914201feff648b048cbaf6c46414d24a56e29e4cff1f82ac1b151d326`  
		Last Modified: Tue, 13 Feb 2024 00:45:14 GMT  
		Size: 53.7 MB (53721486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253942c235484cc0a80af52e0bf1671cb46515d3975f82904e8cfb31b04dd86c`  
		Last Modified: Tue, 13 Feb 2024 01:36:35 GMT  
		Size: 39.2 MB (39241479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef721d8b12382974bb7949ddfb312189924381e469ca9ed214c03a67f99c309`  
		Last Modified: Tue, 13 Feb 2024 01:36:29 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec02038973f872203f725b1360ed9f8966b403eddfc915c0d6e7a5e52ad42ddf`  
		Last Modified: Tue, 13 Feb 2024 01:36:29 GMT  
		Size: 1.9 KB (1875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5663c8f911681df69babdd5b99b2ca9002c54b451e2fd88d2086bb3a0407479`  
		Last Modified: Tue, 13 Feb 2024 01:36:29 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b74eb7d72a15de1c42acac6521e35dbb706881908dd27b7b1ef687baad6be5d`  
		Last Modified: Tue, 13 Feb 2024 01:36:29 GMT  
		Size: 1.4 MB (1385184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c068390e0c29f1eb53115892500066c342cace827d4c5ba3afa3eae2be96a3f`  
		Last Modified: Tue, 13 Feb 2024 01:36:29 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; 386

```console
$ docker pull adminer@sha256:8f0b7ed944befb3b1c14277892b6ed4129665fb82d13e4ebe3882044bea6b258
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (97004528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cc1f088fe11c79cacf73053f9b26c517e62a384c186ccd9a83ff0b54ed70d56`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:08 GMT
ADD file:357a898c0f7038f486b4958deafdca917cd52fe835643c888f731e981b2862dc in / 
# Tue, 13 Feb 2024 00:39:08 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:14:54 GMT
STOPSIGNAL SIGINT
# Tue, 13 Feb 2024 01:15:24 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:15:25 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Tue, 13 Feb 2024 01:15:25 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Tue, 13 Feb 2024 01:15:26 GMT
WORKDIR /var/www/html
# Tue, 13 Feb 2024 01:15:26 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Tue, 13 Feb 2024 01:15:26 GMT
ENV ADMINER_VERSION=4.8.1
# Tue, 13 Feb 2024 01:15:26 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Tue, 13 Feb 2024 01:15:26 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Tue, 13 Feb 2024 01:15:41 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 01:15:41 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Tue, 13 Feb 2024 01:15:41 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 13 Feb 2024 01:15:41 GMT
USER adminer
# Tue, 13 Feb 2024 01:15:41 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Tue, 13 Feb 2024 01:15:41 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:dfd8f591553599fb1e7856eb5c0c822bdff33905eff3003ef95a2281f1003454`  
		Last Modified: Tue, 13 Feb 2024 00:44:10 GMT  
		Size: 56.1 MB (56057784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96d19401fa8382bd461439880f08a01ddd17b92fcbb3203cd8a9e0e75e9c2014`  
		Last Modified: Tue, 13 Feb 2024 01:16:30 GMT  
		Size: 39.6 MB (39557399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9974308b672f6b2b4009c5c4dd560915083c0c3a2d7458b3f80ba49ca8d7d3ed`  
		Last Modified: Tue, 13 Feb 2024 01:16:19 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0da466c45e31faefeb5b0e9547a34b537271140fc4818fe8c3914a3b3d4c44`  
		Last Modified: Tue, 13 Feb 2024 01:16:19 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a580b1308148ca45d34a31ad50af48dcbdf82b083c6493d345fd5f41daaec52`  
		Last Modified: Tue, 13 Feb 2024 01:16:19 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8092089507521db3d028f0f782947040494e3a668ce644501078ba6ac2140b74`  
		Last Modified: Tue, 13 Feb 2024 01:16:19 GMT  
		Size: 1.4 MB (1385122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc057d6962fb2e1fd678af108bbc0b61f1cdb1ed24040377436c8805d48c9e3e`  
		Last Modified: Tue, 13 Feb 2024 01:16:19 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:latest` - linux; mips64le

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
