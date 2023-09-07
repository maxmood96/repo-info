## `adminer:4-standalone`

```console
$ docker pull adminer@sha256:44d118751e8542c0feb020cb1f4612d1c97ce53fb1eb5743c67ee807d865d943
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
$ docker pull adminer@sha256:9425248036f84c766be7ad564108fb92efe3d5744965dcfccf4b3a620461c2c1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95934004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f95e22ea33363f920444f99f0d5821865efafa5e585ef3d1324f8e7d1845c2e`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 16 Aug 2023 00:59:57 GMT
ADD file:20f89ff93bfbd6c9fb1a97058a1f3de4485a8974e8a83892072c511fbd2e4134 in / 
# Wed, 16 Aug 2023 00:59:58 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 06:53:20 GMT
STOPSIGNAL SIGINT
# Wed, 16 Aug 2023 06:53:39 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 06:53:40 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 16 Aug 2023 06:53:41 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 16 Aug 2023 06:53:41 GMT
WORKDIR /var/www/html
# Wed, 16 Aug 2023 06:53:41 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 16 Aug 2023 06:53:41 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 16 Aug 2023 06:53:41 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 16 Aug 2023 06:53:41 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 16 Aug 2023 06:53:52 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 16 Aug 2023 06:53:52 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 16 Aug 2023 06:53:52 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 16 Aug 2023 06:53:52 GMT
USER adminer
# Wed, 16 Aug 2023 06:53:52 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 16 Aug 2023 06:53:52 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:6a70103cc499a199e10e379794c60aa524d9598587cc2bdfe2995642c2da8df7`  
		Last Modified: Wed, 16 Aug 2023 01:04:50 GMT  
		Size: 55.1 MB (55056621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8a57c267c9896b9b3a23126904b5afa97725963cd737515552f4f0382f0fb8`  
		Last Modified: Wed, 16 Aug 2023 06:54:33 GMT  
		Size: 39.5 MB (39487700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b06d2d5387c889ac3907b3b914ba88ef244281459b91f585f182651fe071988`  
		Last Modified: Wed, 16 Aug 2023 06:54:25 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f454e9d758af3cab52e296b29b4b2834a02b1068634c628ed818e7a2a0262f1`  
		Last Modified: Wed, 16 Aug 2023 06:54:25 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76584d0b042e10b1a4377b5b5383b0e2de3acd6e210aa5995e0c1316c3494a27`  
		Last Modified: Wed, 16 Aug 2023 06:54:25 GMT  
		Size: 1.5 KB (1482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94811d9090123101027253a2c9c8cd707849e7a3172541a3047b08e43642a71b`  
		Last Modified: Wed, 16 Aug 2023 06:54:26 GMT  
		Size: 1.4 MB (1385444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79906cbc9e7cf2bcf86c91d2fb9a4c4c1765d07298ae8e8cf92b2a7b283d21a7`  
		Last Modified: Wed, 16 Aug 2023 06:54:25 GMT  
		Size: 489.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; arm variant v5

```console
$ docker pull adminer@sha256:af5badffa86e9c336396019f12d013465f5dbd9c8278aaa1604f78d69ce590ee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91195737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed132a0fc8bb7ca878cf1d94ddfc31902e58f3e494f5e837b61cbd725af3105`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 15 Aug 2023 23:48:40 GMT
ADD file:d044e64aab907424be649252b5ff1d9f5e8c9494db5b60c0e54f5962bfb73478 in / 
# Tue, 15 Aug 2023 23:48:40 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 00:50:17 GMT
STOPSIGNAL SIGINT
# Wed, 16 Aug 2023 00:50:44 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 00:50:45 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 16 Aug 2023 00:50:46 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 16 Aug 2023 00:50:46 GMT
WORKDIR /var/www/html
# Wed, 16 Aug 2023 00:50:46 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 16 Aug 2023 00:50:46 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 16 Aug 2023 00:50:46 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 16 Aug 2023 00:50:46 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 16 Aug 2023 00:51:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 16 Aug 2023 00:51:01 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 16 Aug 2023 00:51:01 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 16 Aug 2023 00:51:01 GMT
USER adminer
# Wed, 16 Aug 2023 00:51:01 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 16 Aug 2023 00:51:01 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:0b63bbf2e6f6026dfaed9cbedf777472a04812b7d291501b1d416e49e3ce885e`  
		Last Modified: Tue, 15 Aug 2023 23:51:54 GMT  
		Size: 52.6 MB (52558130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f7d19107e1a659808b9cf0e01e8326cb019bad1bd5e6d11666cd1e8a4d58f10`  
		Last Modified: Wed, 16 Aug 2023 00:51:40 GMT  
		Size: 37.2 MB (37248042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3402920c76f848974711afefbf633df8e1e5f0238e9d1923aa35d796a7e39775`  
		Last Modified: Wed, 16 Aug 2023 00:51:31 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e8b5522694d8b0cc1d26eec03ac2f2f97ff57d7f3e9056358d86b1d4b1a6b3`  
		Last Modified: Wed, 16 Aug 2023 00:51:31 GMT  
		Size: 1.9 KB (1874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1905db25ca9335b07bf248a97ffc1d0cd746030a8833f0aa7c276c21fae5a31`  
		Last Modified: Wed, 16 Aug 2023 00:51:31 GMT  
		Size: 1.5 KB (1477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3bd225c7201b09ef66598154ae9aa6fbc5b03eb1e143e1b3da8e48a776d928`  
		Last Modified: Wed, 16 Aug 2023 00:51:32 GMT  
		Size: 1.4 MB (1385333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52be3c490603e9c865e303bdb12043abf070af90b245bc1b2188218ef6ea13fb`  
		Last Modified: Wed, 16 Aug 2023 00:51:31 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; arm variant v7

```console
$ docker pull adminer@sha256:dde88e85f022908e040ce9f5627e989fca6cf4f796fb912e216bc91e85b80e9f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87795922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1de3886b83d0afcea5f67dd340efd76d0ff0d7cc5d4d765d7ac24bdce5ac766`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 07 Sep 2023 00:57:59 GMT
ADD file:931564fb3c8ea78b763a6b98f2739bb7c6a38484122c560a87c7166b7d45c5e6 in / 
# Thu, 07 Sep 2023 00:58:00 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 01:50:52 GMT
STOPSIGNAL SIGINT
# Thu, 07 Sep 2023 01:51:32 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:51:33 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 07 Sep 2023 01:51:34 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 07 Sep 2023 01:51:34 GMT
WORKDIR /var/www/html
# Thu, 07 Sep 2023 01:51:34 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 07 Sep 2023 01:51:34 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 07 Sep 2023 01:51:34 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 07 Sep 2023 01:51:34 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 07 Sep 2023 01:51:48 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 07 Sep 2023 01:51:48 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 07 Sep 2023 01:51:48 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 07 Sep 2023 01:51:48 GMT
USER adminer
# Thu, 07 Sep 2023 01:51:48 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 07 Sep 2023 01:51:48 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:5826e0d927336e7231f9d05ec48f075045fb51f9b3f16f1e20972f2a3634d102`  
		Last Modified: Thu, 07 Sep 2023 01:02:50 GMT  
		Size: 50.2 MB (50219233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64126d7f6d5bc4ca6d42b71dc00598c67b9f6f17d6919fcce1f03a613722e16d`  
		Last Modified: Thu, 07 Sep 2023 01:52:33 GMT  
		Size: 36.2 MB (36187001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd3d57a54c1b1fa49ef5fdece23637a20b7f8e985a804fc2c5135f097a549bb`  
		Last Modified: Thu, 07 Sep 2023 01:52:25 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2440750817c8e724091323e3903329ccc274561f1f1e61c49d9da560960899bb`  
		Last Modified: Thu, 07 Sep 2023 01:52:25 GMT  
		Size: 1.9 KB (1869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c56be7ee3fb4f5d4eec7601e51e91b41bf76a5ead2b87c1026930214ba51c2b8`  
		Last Modified: Thu, 07 Sep 2023 01:52:25 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e56804b3ad37bd9f7ff556ddf336fe3b2ed8503cb32b0dfee800e4c76d9451`  
		Last Modified: Thu, 07 Sep 2023 01:52:25 GMT  
		Size: 1.4 MB (1385452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288264a2552805e7baa2b8233fa1aad54720bdba711d9147660fe31f59cc2f32`  
		Last Modified: Thu, 07 Sep 2023 01:52:25 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:9af34f1f23a0f4545e9c8a8c25b96f752722ccba2f4009884b342c6abc821cfd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94337581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceaf57ddeaa0bc790c02948c5b1496cfb51217e6f7a736329cea0d9b6bf68657`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:03 GMT
ADD file:8973cddb2d84a543b71001635599951bea6485a3526ae4ff916443b584864c83 in / 
# Tue, 15 Aug 2023 23:40:04 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:18:33 GMT
STOPSIGNAL SIGINT
# Wed, 16 Aug 2023 01:18:50 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 01:18:51 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 16 Aug 2023 01:18:51 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 16 Aug 2023 01:18:51 GMT
WORKDIR /var/www/html
# Wed, 16 Aug 2023 01:18:51 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 16 Aug 2023 01:18:51 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 16 Aug 2023 01:18:51 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 16 Aug 2023 01:18:52 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 16 Aug 2023 01:19:01 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 16 Aug 2023 01:19:01 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 16 Aug 2023 01:19:01 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 16 Aug 2023 01:19:01 GMT
USER adminer
# Wed, 16 Aug 2023 01:19:01 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 16 Aug 2023 01:19:01 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:e837d9f05c625de5b814b851adbc03559ba02ea7078f57c81a01e18fc65bf42b`  
		Last Modified: Tue, 15 Aug 2023 23:43:37 GMT  
		Size: 53.7 MB (53704779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff6bad57ecba5e0579dd6bd721667f3324e23a3ac5b9bc982bd0dc37a0aac41`  
		Last Modified: Wed, 16 Aug 2023 01:19:36 GMT  
		Size: 39.2 MB (39243216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973b3c539dd5c8609744bf1dfcf0263ed819d43d42b1c7f966a7061631d16973`  
		Last Modified: Wed, 16 Aug 2023 01:19:29 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35373a7e6f06f9c65bd009346d157ef68551477b1e8e69ee02b327b758410fd3`  
		Last Modified: Wed, 16 Aug 2023 01:19:29 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f0e4e65576bf9748b2afc91c98f1c8a3b329fe242ebbb4121fd0bb35330384`  
		Last Modified: Wed, 16 Aug 2023 01:19:29 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:287a444e72e39e2823868a7ea5000b6bb3ea13793adab1f8e6bb510b275a78e3`  
		Last Modified: Wed, 16 Aug 2023 01:19:30 GMT  
		Size: 1.4 MB (1385347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6ddf076b8c62e818266a757bfb81507ec9a219fecf5c0bb790419e67d9b982`  
		Last Modified: Wed, 16 Aug 2023 01:19:29 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; 386

```console
$ docker pull adminer@sha256:664fc6a11ece4d60a18492c17eeb4ffffb3d6fe19d3c4f4c4c3cab52b83f3ec6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96988434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ecc3592e5ee3a2de07572724acd9167630fa736fd16b373959b3f5e2297736`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Tue, 15 Aug 2023 23:39:11 GMT
ADD file:efc88a19b31e68ca41f555bcc51338b0f135cbbd72b90637d8c73969d53addd2 in / 
# Tue, 15 Aug 2023 23:39:12 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 00:23:36 GMT
STOPSIGNAL SIGINT
# Wed, 16 Aug 2023 00:24:03 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 00:24:04 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 16 Aug 2023 00:24:05 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 16 Aug 2023 00:24:05 GMT
WORKDIR /var/www/html
# Wed, 16 Aug 2023 00:24:05 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 16 Aug 2023 00:24:05 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 16 Aug 2023 00:24:05 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 16 Aug 2023 00:24:05 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 16 Aug 2023 00:24:19 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 16 Aug 2023 00:24:19 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 16 Aug 2023 00:24:19 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 16 Aug 2023 00:24:19 GMT
USER adminer
# Wed, 16 Aug 2023 00:24:19 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 16 Aug 2023 00:24:19 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:822e033fa7b169545d5890de01438a9dd87774ff938ff440e823a3ec3f73996d`  
		Last Modified: Tue, 15 Aug 2023 23:43:47 GMT  
		Size: 56.0 MB (56040520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7644269f7e699d335219a554e561f3817b7816e99351232b3646176246991895`  
		Last Modified: Wed, 16 Aug 2023 00:25:00 GMT  
		Size: 39.6 MB (39558428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d96338ff936c667ce1c89a75f7fd111e722685d882b1f36e7b26dcb33007029`  
		Last Modified: Wed, 16 Aug 2023 00:24:50 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5339c86a7bc7031718f83f0a9af19ad028c2fa751748057f9d97d9c94c5075f6`  
		Last Modified: Wed, 16 Aug 2023 00:24:50 GMT  
		Size: 1.9 KB (1868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cbd1ad590a03bbc3ee08a1c944135c7bf81b103067417f79cdb1f8d271b4472`  
		Last Modified: Wed, 16 Aug 2023 00:24:50 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:225fb2c801a3d35820604ab9c5d6c19a65e18fca4c76dd468e7015b6cb7d5d6c`  
		Last Modified: Wed, 16 Aug 2023 00:24:50 GMT  
		Size: 1.4 MB (1385258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:367f82cd1a3d30bffd1420e0c950c92f859f903ad0b0711848862db96f363ff7`  
		Last Modified: Wed, 16 Aug 2023 00:24:50 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; mips64le

```console
$ docker pull adminer@sha256:c30e112a18d740bba282b7482cb0abaa2bad7e50b5522fa34ad4d8c380a66528
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92615842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c19be1facd6063ce5879a23b645f5a5bb98560af333d425904563bde321c37`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 16 Aug 2023 00:09:18 GMT
ADD file:c0b984cd41325dc5f83fb228f8b95bd38027d8860098ac574a960400eaf0d976 in / 
# Wed, 16 Aug 2023 00:09:23 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 14:25:28 GMT
STOPSIGNAL SIGINT
# Wed, 16 Aug 2023 14:27:29 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 14:27:35 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 16 Aug 2023 14:27:42 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 16 Aug 2023 14:27:45 GMT
WORKDIR /var/www/html
# Wed, 16 Aug 2023 14:27:49 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 16 Aug 2023 14:27:52 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 16 Aug 2023 14:27:55 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 16 Aug 2023 14:27:59 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 16 Aug 2023 14:28:51 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 16 Aug 2023 14:28:54 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 16 Aug 2023 14:28:57 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 16 Aug 2023 14:29:01 GMT
USER adminer
# Wed, 16 Aug 2023 14:29:04 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 16 Aug 2023 14:29:08 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:4a039678eb41cc8e7dbd73bbab533513108157d96943588a97c7fac7c940eaca`  
		Last Modified: Wed, 16 Aug 2023 00:20:18 GMT  
		Size: 53.3 MB (53271564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4d9418c8fb7d90292127c5b7a92fc3888569695cb02a9ee6840121d35e5aca`  
		Last Modified: Wed, 16 Aug 2023 14:31:44 GMT  
		Size: 38.0 MB (37953856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97db3503d08d441f3ef436fbf353bcd28273595f8a8b7dbd406c307f8cc23375`  
		Last Modified: Wed, 16 Aug 2023 14:31:18 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9bfb7a9b92e49c8360aab5b1af60686ca5344b3952bea45f877dac006ea37a`  
		Last Modified: Wed, 16 Aug 2023 14:31:18 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d65a5ff01cbc35dccc25b40f79e38afb0c3a0cc450a02cf912b3f03155574cc`  
		Last Modified: Wed, 16 Aug 2023 14:31:18 GMT  
		Size: 1.5 KB (1483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdb09b25e442cc6ec9812188ec358e2ab3e53d652bb6e8f55a833cbd6daa02c`  
		Last Modified: Wed, 16 Aug 2023 14:31:18 GMT  
		Size: 1.4 MB (1386314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37199907cda908c0acf0827db1a775b8d158c324263c81da7ce7ad8f5a550e38`  
		Last Modified: Wed, 16 Aug 2023 14:31:18 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; ppc64le

```console
$ docker pull adminer@sha256:35461ee1c4df47891d1d35bd2d648d4d245a55b316dfe5d3186dd573538bfb87
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101258641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b56f4c94153759bfe2aa36d689c35f5e1679497dc947e5132939ed8ef7335603`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Wed, 16 Aug 2023 01:09:50 GMT
ADD file:23fe4ecb2d3d302e0df50109aee416120a138fad47d1614500f98b65fa288281 in / 
# Wed, 16 Aug 2023 01:09:54 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 09:18:07 GMT
STOPSIGNAL SIGINT
# Wed, 16 Aug 2023 09:19:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 09:19:26 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 16 Aug 2023 09:19:28 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 16 Aug 2023 09:19:29 GMT
WORKDIR /var/www/html
# Wed, 16 Aug 2023 09:19:30 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 16 Aug 2023 09:19:30 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 16 Aug 2023 09:19:31 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 16 Aug 2023 09:19:31 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 16 Aug 2023 09:20:06 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 16 Aug 2023 09:20:07 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 16 Aug 2023 09:20:07 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 16 Aug 2023 09:20:08 GMT
USER adminer
# Wed, 16 Aug 2023 09:20:08 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Wed, 16 Aug 2023 09:20:09 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:148c97e5e41c60dd4fc440664aeee1e57ab7158b53ea7d1f9132198b3d35bc5e`  
		Last Modified: Wed, 16 Aug 2023 01:16:30 GMT  
		Size: 58.9 MB (58928436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e2dd2b972f168bb69bd9b0b6b496e0ba0dc6de2e8f5ce1281f16e8c28706d0`  
		Last Modified: Wed, 16 Aug 2023 09:21:42 GMT  
		Size: 40.9 MB (40940289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c2b8a2a2675ea037355330739dae88692643e65ad0bcccf2a68709d97b9e52e`  
		Last Modified: Wed, 16 Aug 2023 09:21:27 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7994aa659ae5c37825e5b7688e12ffed17e86b402ec30a1d1f2d8dcf4dd25fe1`  
		Last Modified: Wed, 16 Aug 2023 09:21:28 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8c853fc94fb30e7b10225fa384e8e61924f73857ec0baac703134c45640d84`  
		Last Modified: Wed, 16 Aug 2023 09:21:27 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab1c2adf3cd704572195de25cda430e186770e8439c12ab1e808b40758bbeaf`  
		Last Modified: Wed, 16 Aug 2023 09:21:28 GMT  
		Size: 1.4 MB (1385663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a15f00ad475dab1bf11a6542f36b652c9444283a2f59cdc04071f08a34ea4e`  
		Last Modified: Wed, 16 Aug 2023 09:21:27 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-standalone` - linux; s390x

```console
$ docker pull adminer@sha256:b3028b06f7c78024603ab547558cf83d4fe518c6bfd10a107ee923081d45c3a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93700732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40878d5b42fdc65d89e9d563be958aad831592c92455633ce54a025dc6bac4eb`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php","-S","[::]:8080","-t","\/var\/www\/html"]`

```dockerfile
# Thu, 07 Sep 2023 00:44:03 GMT
ADD file:a0582e191d0265b98e5d46c64ba9b4c46445cfa821c6e41d32db343b0e2a6fec in / 
# Thu, 07 Sep 2023 00:44:12 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 01:26:26 GMT
STOPSIGNAL SIGINT
# Thu, 07 Sep 2023 01:27:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:27:07 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 07 Sep 2023 01:27:08 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 07 Sep 2023 01:27:08 GMT
WORKDIR /var/www/html
# Thu, 07 Sep 2023 01:27:09 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 07 Sep 2023 01:27:09 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 07 Sep 2023 01:27:09 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 07 Sep 2023 01:27:09 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 07 Sep 2023 01:27:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 07 Sep 2023 01:27:22 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 07 Sep 2023 01:27:23 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 07 Sep 2023 01:27:24 GMT
USER adminer
# Thu, 07 Sep 2023 01:27:24 GMT
CMD ["php" "-S" "[::]:8080" "-t" "/var/www/html"]
# Thu, 07 Sep 2023 01:27:24 GMT
EXPOSE 8080
```

-	Layers:
	-	`sha256:6dd2d41f67a6666210e1a34694b8765e945a44014b53252ec0e1b50491e08d69`  
		Last Modified: Thu, 07 Sep 2023 00:49:54 GMT  
		Size: 53.3 MB (53290217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4a876b44eaaf1ba3c702ea08a6af25e23abb30b7fcbef9b957a4c34ec5ad73`  
		Last Modified: Thu, 07 Sep 2023 01:28:21 GMT  
		Size: 39.0 MB (39020691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:529f8a0ebc99b919f45c296bfffe1d9aa35136c91542e626681a898a1e1dabb2`  
		Last Modified: Thu, 07 Sep 2023 01:28:14 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322f53d9402212f75016bdbb862615c373419e902c2b0a0994373659dc9a40dc`  
		Last Modified: Thu, 07 Sep 2023 01:28:14 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c552fc3addf63a6a3c52100ad6a25209610153282a2977fc8234b019e7bfa4b8`  
		Last Modified: Thu, 07 Sep 2023 01:28:14 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4df5368a1108e415af1adad06e9925df044775278212b278f40db0c9e828b6`  
		Last Modified: Thu, 07 Sep 2023 01:28:15 GMT  
		Size: 1.4 MB (1385578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8fa422b756819743a45bc63685472b1df2c01002596e8beb4231c6f1235f34`  
		Last Modified: Thu, 07 Sep 2023 01:28:14 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
