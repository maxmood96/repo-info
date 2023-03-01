## `adminer:4-fastcgi`

```console
$ docker pull adminer@sha256:42624dbe35bd71a1177f29906d52559dbc6493220ac7aafe6d9d3c347c29a931
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
$ docker pull adminer@sha256:fee1a5594b8cad17aefd541522176bc13b576fa899aca5d5b461e660db7c09a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95924741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678a67ecc92d01f841de8bb9a80467bcf3c482ec115f2e939a993881e25cc3bb`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:45 GMT
ADD file:513c5d5e501279c21a05c1d8b66e5f0b02ee4b27f0b928706d92fd9ce11c1be6 in / 
# Wed, 01 Mar 2023 04:09:46 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 04:35:47 GMT
STOPSIGNAL SIGINT
# Wed, 01 Mar 2023 04:36:13 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 04:36:13 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 01 Mar 2023 04:36:36 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 01 Mar 2023 04:36:36 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 01 Mar 2023 04:36:36 GMT
WORKDIR /var/www/html
# Wed, 01 Mar 2023 04:36:36 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 01 Mar 2023 04:36:37 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 01 Mar 2023 04:36:37 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 01 Mar 2023 04:36:37 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 01 Mar 2023 04:36:48 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 01 Mar 2023 04:36:48 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 01 Mar 2023 04:36:48 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 01 Mar 2023 04:36:48 GMT
USER adminer
# Wed, 01 Mar 2023 04:36:48 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:32fb02163b6bb519a30f909008e852354dae10bdfd6b34190dbdfe8f15403ea0`  
		Last Modified: Wed, 01 Mar 2023 04:13:58 GMT  
		Size: 55.0 MB (55045922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211049d859ddab95a9cf0582a13a527f2147c1e372de0eb3e0fac8a90aada145`  
		Last Modified: Wed, 01 Mar 2023 04:37:11 GMT  
		Size: 39.5 MB (39486615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad21449981741416fc36fc6398aa758c923a016a62db78fd95b037088150c48`  
		Last Modified: Wed, 01 Mar 2023 04:37:03 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94cf939c1922d2d1ab17b24e14a5d44958e24594e43280d527c351b2e03d3afc`  
		Last Modified: Wed, 01 Mar 2023 04:37:28 GMT  
		Size: 2.7 KB (2712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c3621387be5234f0fd1b5ad5f691d9cb063f5ca6ef302e2f589bbc3f2d54b70`  
		Last Modified: Wed, 01 Mar 2023 04:37:28 GMT  
		Size: 1.9 KB (1880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad49e3938c114ca569130958d86e901da7ab443a6f446ea6e3c73c905c352ae`  
		Last Modified: Wed, 01 Mar 2023 04:37:28 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de469810d9b4f3519299297c03700ef8d3535f214402662e16003fb87a63832e`  
		Last Modified: Wed, 01 Mar 2023 04:37:28 GMT  
		Size: 1.4 MB (1385258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b4dc8be257f858e87b66225e2fba2e0ec74e808a3f1434d127c86245c5d0b42`  
		Last Modified: Wed, 01 Mar 2023 04:37:28 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm variant v5

```console
$ docker pull adminer@sha256:576d41a68e1710a81cf9e3af2fe4dd0beda2b410606e9d73a5acfa574cde2c84
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91187893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee833e0ba60a7db539c5d22a6875870d5606099fa3d392706d2bcb88ca390595`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 01 Mar 2023 01:48:43 GMT
ADD file:a4c8194220314bdada02b2e8d4a2aaa01f89c69eb66013a81a42903b7fa82e7a in / 
# Wed, 01 Mar 2023 01:48:44 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:11:09 GMT
STOPSIGNAL SIGINT
# Wed, 01 Mar 2023 02:11:45 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:11:45 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 01 Mar 2023 02:12:09 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 01 Mar 2023 02:12:09 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 01 Mar 2023 02:12:09 GMT
WORKDIR /var/www/html
# Wed, 01 Mar 2023 02:12:10 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 01 Mar 2023 02:12:10 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 01 Mar 2023 02:12:10 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 01 Mar 2023 02:12:10 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 01 Mar 2023 02:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 01 Mar 2023 02:12:23 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 01 Mar 2023 02:12:23 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 01 Mar 2023 02:12:23 GMT
USER adminer
# Wed, 01 Mar 2023 02:12:23 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:0e646b3de69bc5bf194fa10012b1ebb12aba169270858575517eba4a0019e696`  
		Last Modified: Wed, 01 Mar 2023 01:52:26 GMT  
		Size: 52.5 MB (52549820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00bf4027abeab611368338e45f58f4642e1d83d5a87ef8a375c2d83d02969dc6`  
		Last Modified: Wed, 01 Mar 2023 02:13:03 GMT  
		Size: 37.2 MB (37245976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c99bca1d37f231fa8bd33ea49e65ebf96ca034502f8985f0cbcc8c0a637f02d`  
		Last Modified: Wed, 01 Mar 2023 02:12:53 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc19b9fea08b00209f967ce59c60e232b059d80cb57d2b4880936a5386c2443`  
		Last Modified: Wed, 01 Mar 2023 02:13:27 GMT  
		Size: 2.7 KB (2714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7636acdd3857ae780305818aea911a8f62cc9f660763ce541fde005b970efb57`  
		Last Modified: Wed, 01 Mar 2023 02:13:27 GMT  
		Size: 1.9 KB (1871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e7382cb81ffd9a790df1945e642d6f5c7d56a27b6f47b4b0c69956ce547cc7`  
		Last Modified: Wed, 01 Mar 2023 02:13:27 GMT  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e62446efb05e74489c74a225561e3eba1bfbde8c0a03a2eb24764de2ab60c9`  
		Last Modified: Wed, 01 Mar 2023 02:13:27 GMT  
		Size: 1.4 MB (1385153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35b2770b134e81dba3dee499738b2d2b5ef50e3defcf6b1defec60c9e5e3e83`  
		Last Modified: Wed, 01 Mar 2023 02:13:26 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm variant v7

```console
$ docker pull adminer@sha256:175894202c22ab097313fea371062301ed41d3009e7f302d215a680c18aebf61
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87785417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b20205dda8d3d6fb8a46280e4f00525ab29656de6624c1f0961d84b0949934`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 01 Mar 2023 01:57:45 GMT
ADD file:95a5e178e353a9a46c230d78b0ef83309dd487651c34e47e972ed3dae08ea00b in / 
# Wed, 01 Mar 2023 01:57:45 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:22:38 GMT
STOPSIGNAL SIGINT
# Wed, 01 Mar 2023 02:23:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:23:03 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 01 Mar 2023 02:23:20 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 01 Mar 2023 02:23:21 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 01 Mar 2023 02:23:21 GMT
WORKDIR /var/www/html
# Wed, 01 Mar 2023 02:23:21 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 01 Mar 2023 02:23:21 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 01 Mar 2023 02:23:21 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 01 Mar 2023 02:23:21 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 01 Mar 2023 02:23:31 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 01 Mar 2023 02:23:32 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 01 Mar 2023 02:23:32 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 01 Mar 2023 02:23:32 GMT
USER adminer
# Wed, 01 Mar 2023 02:23:32 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:30bee4bd8986478b5a9ecaaaba83525049f0b9b5a63ca88de878568bb6b83292`  
		Last Modified: Wed, 01 Mar 2023 02:02:32 GMT  
		Size: 50.2 MB (50212046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd6b6627724e14462f46d693d6e6d571c26e42748a0d12b23dceb3bb3f76f38`  
		Last Modified: Wed, 01 Mar 2023 02:24:10 GMT  
		Size: 36.2 MB (36181310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:631947dc8f6343e1805e1c67d899e226d4747686ef46c6fc7902b90edc41c652`  
		Last Modified: Wed, 01 Mar 2023 02:24:01 GMT  
		Size: 386.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94016960d23f16b8e4c08693832c28a1b27a16c7689aaa5d2e2a3df48478e2ac`  
		Last Modified: Wed, 01 Mar 2023 02:24:32 GMT  
		Size: 2.7 KB (2709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35cbd4d09f6fd5b7806c65c00f7bc0911d43e9b771e6d58deb38f3ae25ec803`  
		Last Modified: Wed, 01 Mar 2023 02:24:32 GMT  
		Size: 1.9 KB (1872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24aeea35ac553a7fbe3eb35a1f5f922be3a47ecda0c6e06995c3fce818fcfea`  
		Last Modified: Wed, 01 Mar 2023 02:24:32 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141fc097e4906ea286512b936a26a6ef1ea376edf341fd3e363c54bd9872cf8e`  
		Last Modified: Wed, 01 Mar 2023 02:24:33 GMT  
		Size: 1.4 MB (1385123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af66d62bffd92a2f6dbf6aa3187aea1c15fcddb7ceb4ae9856863f36094d3c83`  
		Last Modified: Wed, 01 Mar 2023 02:24:32 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; arm64 variant v8

```console
$ docker pull adminer@sha256:98e4a5f8c75976ff9a94699f0ef928f09632d8d33c4e7476f001cc71f7b8552a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94338146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:644a766cfad249d0e5073b6eca2bd7ef2ed350e40a82007c3dcb17d15f371063`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:30 GMT
ADD file:a6a1df499d0d5b07fb366d776a11c42ddee6261e2425a921041b38e868192770 in / 
# Wed, 01 Mar 2023 02:20:30 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:43:01 GMT
STOPSIGNAL SIGINT
# Wed, 01 Mar 2023 02:43:21 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:43:22 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 01 Mar 2023 02:43:42 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 01 Mar 2023 02:43:42 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 01 Mar 2023 02:43:42 GMT
WORKDIR /var/www/html
# Wed, 01 Mar 2023 02:43:42 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 01 Mar 2023 02:43:43 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 01 Mar 2023 02:43:43 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 01 Mar 2023 02:43:43 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 01 Mar 2023 02:43:52 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 01 Mar 2023 02:43:52 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 01 Mar 2023 02:43:53 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 01 Mar 2023 02:43:53 GMT
USER adminer
# Wed, 01 Mar 2023 02:43:53 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:0f5fe16b1836feccd4765ac5685fc7a7b9c73445cac94fc595d2ffbc3cb59a7a`  
		Last Modified: Wed, 01 Mar 2023 02:23:53 GMT  
		Size: 53.7 MB (53703215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e18d9ec6fef375124d6b5dcd750b44aef139171fc92ce3427cf0f16f9fd7413`  
		Last Modified: Wed, 01 Mar 2023 02:44:13 GMT  
		Size: 39.2 MB (39242798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f873bf2d54d8e0f04cbff219553d84bed228d65b4f1380a8e6242fc3f927a3a`  
		Last Modified: Wed, 01 Mar 2023 02:44:07 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3f5a2f6aaeeedaaec6b8e880adb8e3de61eca4b38a3d322643b4ef851f0daf`  
		Last Modified: Wed, 01 Mar 2023 02:44:32 GMT  
		Size: 2.7 KB (2713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b1b34de8f386ec157565846e01270f86dfa48007f1e48cb2053ded8ffd1e3c`  
		Last Modified: Wed, 01 Mar 2023 02:44:32 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17fadc9f1506bf526d43e8eae6edb484cabe7650f93aa216c713d051322537d9`  
		Last Modified: Wed, 01 Mar 2023 02:44:32 GMT  
		Size: 1.5 KB (1476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b78d0d43bb01fce74476f467c21cc5b01571371c0a35b9e6a9ac7aa31de131`  
		Last Modified: Wed, 01 Mar 2023 02:44:32 GMT  
		Size: 1.4 MB (1385179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773bbf60583def2f37ac88ca03237395428a0d4e44a813ed4d5bd18815eb71c3`  
		Last Modified: Wed, 01 Mar 2023 02:44:32 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; 386

```console
$ docker pull adminer@sha256:4bb7248da6c090ba190bd5a98bc9e7ad3ff7537cc6003782708e5dc932145212
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96978062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8889460a964987e3a8fe6191a528657050dd26bdcba0d93f783929b97804577`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 01 Mar 2023 01:39:01 GMT
ADD file:881e5812ed9664defe9745d26894a268ec27de907c9a615a5204bbb5e8e94262 in / 
# Wed, 01 Mar 2023 01:39:02 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 09:17:34 GMT
STOPSIGNAL SIGINT
# Wed, 01 Mar 2023 09:18:02 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 09:18:03 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 01 Mar 2023 09:18:24 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 01 Mar 2023 09:18:24 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 01 Mar 2023 09:18:24 GMT
WORKDIR /var/www/html
# Wed, 01 Mar 2023 09:18:24 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 01 Mar 2023 09:18:25 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 01 Mar 2023 09:18:25 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 01 Mar 2023 09:18:25 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 01 Mar 2023 09:18:37 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 01 Mar 2023 09:18:37 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 01 Mar 2023 09:18:37 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 01 Mar 2023 09:18:37 GMT
USER adminer
# Wed, 01 Mar 2023 09:18:37 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:0a0c64c8f15c57499fa240b509d736a6e6b861478b11e52aadbc9551cfd10638`  
		Last Modified: Wed, 01 Mar 2023 01:44:12 GMT  
		Size: 56.0 MB (56028076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b148edf759c5b2d96f9a97d10d1b05c057dbb4d8ac7ffe3cbc726038bfb5c4d`  
		Last Modified: Wed, 01 Mar 2023 09:19:11 GMT  
		Size: 39.6 MB (39557973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2009ec4302073d8a17b85aceb5ccaa1390d5f03027f4f35ff831ad7f66afe9c`  
		Last Modified: Wed, 01 Mar 2023 09:19:01 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5319f5373678a2ab5fd41d84bffbeccb94650b5f383482de52206773890db0d3`  
		Last Modified: Wed, 01 Mar 2023 09:19:33 GMT  
		Size: 2.7 KB (2708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9349cd03ec5ab9e10483f38aac2d403a1a9b35a082e55aeef3889c8fa42de2a0`  
		Last Modified: Wed, 01 Mar 2023 09:19:33 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf1ba15c5b41f6ed686227f37f79dba94ed4448fb83cdab5d3dad31e0a3d193`  
		Last Modified: Wed, 01 Mar 2023 09:19:33 GMT  
		Size: 1.5 KB (1478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f319a7fdb59d809a38553806801e94672f4d7cca3c0a69984ea6f1dd772dd1`  
		Last Modified: Wed, 01 Mar 2023 09:19:34 GMT  
		Size: 1.4 MB (1385082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca5b4ab49a268ed0016d0ef16a367efb43051c8993767896ff5283d9e1b9cb4`  
		Last Modified: Wed, 01 Mar 2023 09:19:33 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; mips64le

```console
$ docker pull adminer@sha256:d49eaa95df7a4b3b648e490d31d318b52533773169fecbc5a057d0012ea43a55
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92613258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cbd3305cd6fd59e4170383251a3e22ee9ca9c66bae9ba0b1914c9ffae1b23f6`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Thu, 09 Feb 2023 02:44:36 GMT
ADD file:0cc085dc00beb990e7bfcdd8b37dceccb8f6d62d7c5ce2d7e736cdf4d52ab799 in / 
# Thu, 09 Feb 2023 02:44:41 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 06:13:03 GMT
STOPSIGNAL SIGINT
# Thu, 09 Feb 2023 06:14:56 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 06:15:02 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Thu, 09 Feb 2023 06:16:50 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Thu, 09 Feb 2023 06:16:56 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Thu, 09 Feb 2023 06:16:59 GMT
WORKDIR /var/www/html
# Thu, 09 Feb 2023 06:17:02 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Thu, 09 Feb 2023 06:17:05 GMT
ENV ADMINER_VERSION=4.8.1
# Thu, 09 Feb 2023 06:17:08 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Thu, 09 Feb 2023 06:17:11 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Thu, 09 Feb 2023 06:17:59 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Thu, 09 Feb 2023 06:18:02 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Thu, 09 Feb 2023 06:18:05 GMT
ENTRYPOINT ["entrypoint.sh"]
# Thu, 09 Feb 2023 06:18:09 GMT
USER adminer
# Thu, 09 Feb 2023 06:18:12 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:11a4758105e306ed24134ddf12f4d813426845c37a0ab14cb71de94c2858f09c`  
		Last Modified: Thu, 09 Feb 2023 02:53:05 GMT  
		Size: 53.3 MB (53266784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daca01da5691398087a3bfc7f953540cff885f22074e0129fda0d5e578a7a64`  
		Last Modified: Thu, 09 Feb 2023 06:19:06 GMT  
		Size: 38.0 MB (37953476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53cfc05716a9d1f679b734de3bff7a1b9714f5eb4b5040d6e143defb24f4975b`  
		Last Modified: Thu, 09 Feb 2023 06:18:37 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df2d2de23d5a64cae787901af3f38fcaf86ab721824c7226d9bb8586ddba9fa`  
		Last Modified: Thu, 09 Feb 2023 06:19:25 GMT  
		Size: 2.7 KB (2714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7734475a7c59ac576ed3322ac3274c2a727bb9a6c660381c515c9bf8ded7c0`  
		Last Modified: Thu, 09 Feb 2023 06:19:25 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b439c2c16da41627079e7dc7e3e2618e41b7ac3019f33d234ac6a50e1271e8c`  
		Last Modified: Thu, 09 Feb 2023 06:19:25 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de57b503c9c79ca9d98a1575e8b2a2fec4f4f34a8184502f8a1697d783873671`  
		Last Modified: Thu, 09 Feb 2023 06:19:26 GMT  
		Size: 1.4 MB (1386183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27aac5c4950f7dd7352e76a2718d3c9d2974ba7ea1b383509d9a235534ccf422`  
		Last Modified: Thu, 09 Feb 2023 06:19:25 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; ppc64le

```console
$ docker pull adminer@sha256:b9635b6cdd73918be41d66b5a58b646052c93f3ab35db6b358414639702ffec9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101252925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25820ceafebb3292bf04122872747b95a0b519eb5b9370a0c2f273c06d5800a9`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 01 Mar 2023 04:47:01 GMT
ADD file:40523b7b16ccf1ff245b11e11f92d24e9e6e9dfbdbc755d4361cf55c7ec26244 in / 
# Wed, 01 Mar 2023 04:47:11 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:13:05 GMT
STOPSIGNAL SIGINT
# Wed, 01 Mar 2023 05:14:17 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:14:21 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 01 Mar 2023 05:15:17 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 01 Mar 2023 05:15:20 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 01 Mar 2023 05:15:21 GMT
WORKDIR /var/www/html
# Wed, 01 Mar 2023 05:15:21 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 01 Mar 2023 05:15:22 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 01 Mar 2023 05:15:23 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 01 Mar 2023 05:15:23 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 01 Mar 2023 05:16:09 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 01 Mar 2023 05:16:10 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 01 Mar 2023 05:16:10 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 01 Mar 2023 05:16:10 GMT
USER adminer
# Wed, 01 Mar 2023 05:16:11 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:3b7949e1acd104233f80137ab3a92a148b0d48e41b3075c70a2d636c3b4c60bf`  
		Last Modified: Wed, 01 Mar 2023 04:53:18 GMT  
		Size: 58.9 MB (58921304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a01fc5486f410d6c6fc4955fd479835fce430ae1288deee46d741852f9e8a3`  
		Last Modified: Wed, 01 Mar 2023 05:16:49 GMT  
		Size: 40.9 MB (40939167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2632443eb517c94b572664e022426b9a37d3451ef96805e8edc7e3ed55afab97`  
		Last Modified: Wed, 01 Mar 2023 05:16:36 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1daa1fd9ef205854cc63b8a8445aaf2aae27ef44730abe17f98ee3f8ea913e11`  
		Last Modified: Wed, 01 Mar 2023 05:17:14 GMT  
		Size: 2.7 KB (2712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84cffba7c8ed70822aceb1aa113731d03a50e50495e468e20f550e82ef0ebde5`  
		Last Modified: Wed, 01 Mar 2023 05:17:14 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424025bc99186c19f61c5628f6c80cf5ce9a0e60ea1cc68de1d1693bf94e5a69`  
		Last Modified: Wed, 01 Mar 2023 05:17:14 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7315d23f21ebf3a6e9175942f2ea7104ac91fe34f321e3c3faff107865e5ebb6`  
		Last Modified: Wed, 01 Mar 2023 05:17:15 GMT  
		Size: 1.4 MB (1385495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e021a8157ddba13d9b96b8da1296f3d0c90d0a63c4eb89f9a2b82e5311e90180`  
		Last Modified: Wed, 01 Mar 2023 05:17:14 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adminer:4-fastcgi` - linux; s390x

```console
$ docker pull adminer@sha256:46cf38d41cec280ba262d22622c5dc63eb04cd0fa6e8e421682a9e6d23095c01
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93686760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36c19d853af3bd5d90dc71b203db921de077dd2fc268f0b99a723bd8c023d4a`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["php-fpm7.4"]`

```dockerfile
# Wed, 01 Mar 2023 02:50:07 GMT
ADD file:e5f01d8f88c8134571e8998672a504ecad259a9a8322df73aed4a93ffac08ebd in / 
# Wed, 01 Mar 2023 02:50:10 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 07:13:08 GMT
STOPSIGNAL SIGINT
# Wed, 01 Mar 2023 07:13:26 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y 		php7.4-cli 		php7.4-fpm 		php7.4-mbstring 		php7.4-mysql 		php7.4-odbc 		php7.4-pdo-dblib 		php7.4-pgsql 		php7.4-sqlite3 &&	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 07:13:28 GMT
RUN echo "upload_max_filesize = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "post_max_size = 128M" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "memory_limit = 1G" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_execution_time = 600" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "max_input_vars = 5000" >> /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini &&	echo "variables_order = \"EGPCS\"" >> /etc/php/7.4/cli/conf.d/0-env.ini &&	cp /etc/php/7.4/cli/conf.d/0-upload_large_dumps.ini /etc/php/7.4/fpm/conf.d/0-upload_large_dumps.ini
# Wed, 01 Mar 2023 07:13:44 GMT
RUN set -ex;	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee /etc/php/7.4/fpm/pool.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee /etc/php/7.4/fpm/pool.d/zz-docker.conf; 	sed -i '/^pid =/d' /etc/php/7.4/fpm/php-fpm.conf
# Wed, 01 Mar 2023 07:13:44 GMT
RUN groupadd -r adminer &&	useradd -r -g adminer adminer &&	mkdir -p /var/www/html &&	mkdir /var/www/html/plugins-enabled &&	chown -R adminer:adminer /var/www/html
# Wed, 01 Mar 2023 07:13:45 GMT
WORKDIR /var/www/html
# Wed, 01 Mar 2023 07:13:45 GMT
COPY multi:8e2583c31626149dac766c1e81b6ba87f4289e683e42823f52b952fbab069922 in /var/www/html/ 
# Wed, 01 Mar 2023 07:13:45 GMT
ENV ADMINER_VERSION=4.8.1
# Wed, 01 Mar 2023 07:13:45 GMT
ENV ADMINER_DOWNLOAD_SHA256=2fd7e6d8f987b243ab1839249551f62adce19704c47d3d0c8dd9e57ea5b9c6b3
# Wed, 01 Mar 2023 07:13:45 GMT
ENV ADMINER_COMMIT=1f173e18bdf0be29182e0d67989df56eadea4754
# Wed, 01 Mar 2023 07:13:53 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='git curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://github.com/vrana/adminer/releases/download/v$ADMINER_VERSION/adminer-$ADMINER_VERSION.php" -o adminer.php &&	echo "$ADMINER_DOWNLOAD_SHA256  adminer.php" |sha256sum -c - &&	git clone --recurse-submodules=designs --depth 1 --shallow-submodules --branch "v$ADMINER_VERSION" https://github.com/vrana/adminer.git /tmp/adminer &&	commit="$(git -C /tmp/adminer/ rev-parse HEAD)" &&	[ "$commit" = "$ADMINER_COMMIT" ] &&	cp -r /tmp/adminer/designs/ /tmp/adminer/plugins/ . &&	rm -rf /tmp/adminer/ &&	apt-get purge -y --auto-remove $buildDeps
# Wed, 01 Mar 2023 07:13:53 GMT
COPY file:5ff0be587f5dd9166f7a558457b0e656c889de46d3bb2afd41f1714ab2c02ceb in /usr/local/bin/ 
# Wed, 01 Mar 2023 07:13:53 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 01 Mar 2023 07:13:53 GMT
USER adminer
# Wed, 01 Mar 2023 07:13:53 GMT
CMD ["php-fpm7.4"]
```

-	Layers:
	-	`sha256:51f6de0debe6daa552b12c9951f6529a870979d923187c1ba62ff66cee3450ac`  
		Last Modified: Wed, 01 Mar 2023 02:54:25 GMT  
		Size: 53.3 MB (53277694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1f1dd4ba66f49d0fb9be9a4f899749440a6757c1431f248949c832c40b4bec`  
		Last Modified: Wed, 01 Mar 2023 07:14:25 GMT  
		Size: 39.0 MB (39016995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9aa64efd5af1f3e23fb14d932e0eb9534b1aef2907225c4351bab9a3be830c`  
		Last Modified: Wed, 01 Mar 2023 07:14:18 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7ccd8ba674e52864ed8e57353cc100e2b4c808c628ae998d671bbc5e463dd1`  
		Last Modified: Wed, 01 Mar 2023 07:14:37 GMT  
		Size: 2.7 KB (2706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b7fac1cd818e0c1e6846651a65210740d70fca843e05c023c5da134b219e85`  
		Last Modified: Wed, 01 Mar 2023 07:14:37 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ab5deca6c3cfa8f0bddab465b9068b3b28a7d1f0cc261028f692a710ad25d0`  
		Last Modified: Wed, 01 Mar 2023 07:14:37 GMT  
		Size: 1.5 KB (1481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae89fd1ed586c04a2f9143a55c635d61f5a7ce9f13a9478332f4d10633e33a32`  
		Last Modified: Wed, 01 Mar 2023 07:14:37 GMT  
		Size: 1.4 MB (1385122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0332efb125d3809a9b24f8a1a09d6bee70e55fc0d84fd931bf78536711ee572d`  
		Last Modified: Wed, 01 Mar 2023 07:14:37 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
