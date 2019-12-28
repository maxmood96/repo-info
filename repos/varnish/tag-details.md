<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `varnish`

-	[`varnish:6`](#varnish6)
-	[`varnish:6.0`](#varnish60)
-	[`varnish:6.0.5`](#varnish605)
-	[`varnish:6.0.5-1`](#varnish605-1)
-	[`varnish:6.3`](#varnish63)
-	[`varnish:6.3.1`](#varnish631)
-	[`varnish:6.3.1-1`](#varnish631-1)
-	[`varnish:fresh`](#varnishfresh)
-	[`varnish:latest`](#varnishlatest)
-	[`varnish:stable`](#varnishstable)

## `varnish:6`

```console
$ docker pull varnish@sha256:82ca458edf9556dc63361568ef7dcd2eab27941826fcc13c61e9f68919ca9bcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6` - linux; amd64

```console
$ docker pull varnish@sha256:cc2ec6bb137e66b8597c187e6d3b970d1b6a60285a283aaac538a486ba18e514
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67422052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1da00c66cf15cc0c521896f822779d978844ab4ae4dc683d114f4636d8a47071`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `["varnishd","-F","-f","\/etc\/varnish\/default.vcl"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:39:01 GMT
ENV VARNISH_VERSION=6.3.1-1~stretch
# Sat, 28 Dec 2019 08:39:36 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=920A8A7AA7120A8604BCCD294A42CD6EB810E55D; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver http://ha.pool.sks-keyservers.net/ --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish63/debian/ stretch main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:39:37 GMT
WORKDIR /etc/varnish
# Sat, 28 Dec 2019 08:39:37 GMT
COPY file:0301ec458d312e5c085462f916888bc85bb94c134ed6116667d225487db56cac in /usr/local/bin/ 
# Sat, 28 Dec 2019 08:39:37 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Sat, 28 Dec 2019 08:39:37 GMT
EXPOSE 80
# Sat, 28 Dec 2019 08:39:38 GMT
CMD ["varnishd" "-F" "-f" "/etc/varnish/default.vcl"]
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cae3b79eb09474b8f1af0d0ba7a7eb8a00d9ae59f4db2571867d9253ff231ec`  
		Last Modified: Sat, 28 Dec 2019 08:40:51 GMT  
		Size: 44.9 MB (44897060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa563190ed24836e8c76af45484cbbce1417d698d8738c2107b68e1aaeb3e73`  
		Last Modified: Sat, 28 Dec 2019 08:40:40 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0`

```console
$ docker pull varnish@sha256:1a86025e3297b692f1be2308ae82606c717c17265249d93ff2e31afad7f0cf2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.0` - linux; amd64

```console
$ docker pull varnish@sha256:97b65d85d8423d0b69b18b018f5ce0737eda0e2888551081dbd2bf3540970a75
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67212471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3dce924eb9db51468c49f4d46d6336b6eb25bb0c3494facef30a331302289f`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `["varnishd","-F","-f","\/etc\/varnish\/default.vcl"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:39:47 GMT
ENV VARNISH_VERSION=6.0.5-1~stretch
# Sat, 28 Dec 2019 08:40:22 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver http://ha.pool.sks-keyservers.net/ --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ stretch main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:40:22 GMT
WORKDIR /etc/varnish
# Sat, 28 Dec 2019 08:40:22 GMT
COPY file:0301ec458d312e5c085462f916888bc85bb94c134ed6116667d225487db56cac in /usr/local/bin/ 
# Sat, 28 Dec 2019 08:40:23 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Sat, 28 Dec 2019 08:40:23 GMT
EXPOSE 80
# Sat, 28 Dec 2019 08:40:23 GMT
CMD ["varnishd" "-F" "-f" "/etc/varnish/default.vcl"]
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75d3befb2551921acda03c74674a8ab18e802c7c1ad172029b8270d43c9df75`  
		Last Modified: Sat, 28 Dec 2019 08:41:15 GMT  
		Size: 44.7 MB (44687480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6afdeb276efd7cf4b698b42db8557d9c36634bbcb95f22017e9792de5424a8`  
		Last Modified: Sat, 28 Dec 2019 08:40:59 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0.5`

```console
$ docker pull varnish@sha256:1a86025e3297b692f1be2308ae82606c717c17265249d93ff2e31afad7f0cf2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.0.5` - linux; amd64

```console
$ docker pull varnish@sha256:97b65d85d8423d0b69b18b018f5ce0737eda0e2888551081dbd2bf3540970a75
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67212471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3dce924eb9db51468c49f4d46d6336b6eb25bb0c3494facef30a331302289f`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `["varnishd","-F","-f","\/etc\/varnish\/default.vcl"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:39:47 GMT
ENV VARNISH_VERSION=6.0.5-1~stretch
# Sat, 28 Dec 2019 08:40:22 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver http://ha.pool.sks-keyservers.net/ --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ stretch main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:40:22 GMT
WORKDIR /etc/varnish
# Sat, 28 Dec 2019 08:40:22 GMT
COPY file:0301ec458d312e5c085462f916888bc85bb94c134ed6116667d225487db56cac in /usr/local/bin/ 
# Sat, 28 Dec 2019 08:40:23 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Sat, 28 Dec 2019 08:40:23 GMT
EXPOSE 80
# Sat, 28 Dec 2019 08:40:23 GMT
CMD ["varnishd" "-F" "-f" "/etc/varnish/default.vcl"]
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75d3befb2551921acda03c74674a8ab18e802c7c1ad172029b8270d43c9df75`  
		Last Modified: Sat, 28 Dec 2019 08:41:15 GMT  
		Size: 44.7 MB (44687480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6afdeb276efd7cf4b698b42db8557d9c36634bbcb95f22017e9792de5424a8`  
		Last Modified: Sat, 28 Dec 2019 08:40:59 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0.5-1`

```console
$ docker pull varnish@sha256:1a86025e3297b692f1be2308ae82606c717c17265249d93ff2e31afad7f0cf2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.0.5-1` - linux; amd64

```console
$ docker pull varnish@sha256:97b65d85d8423d0b69b18b018f5ce0737eda0e2888551081dbd2bf3540970a75
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67212471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3dce924eb9db51468c49f4d46d6336b6eb25bb0c3494facef30a331302289f`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `["varnishd","-F","-f","\/etc\/varnish\/default.vcl"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:39:47 GMT
ENV VARNISH_VERSION=6.0.5-1~stretch
# Sat, 28 Dec 2019 08:40:22 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver http://ha.pool.sks-keyservers.net/ --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ stretch main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:40:22 GMT
WORKDIR /etc/varnish
# Sat, 28 Dec 2019 08:40:22 GMT
COPY file:0301ec458d312e5c085462f916888bc85bb94c134ed6116667d225487db56cac in /usr/local/bin/ 
# Sat, 28 Dec 2019 08:40:23 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Sat, 28 Dec 2019 08:40:23 GMT
EXPOSE 80
# Sat, 28 Dec 2019 08:40:23 GMT
CMD ["varnishd" "-F" "-f" "/etc/varnish/default.vcl"]
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75d3befb2551921acda03c74674a8ab18e802c7c1ad172029b8270d43c9df75`  
		Last Modified: Sat, 28 Dec 2019 08:41:15 GMT  
		Size: 44.7 MB (44687480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6afdeb276efd7cf4b698b42db8557d9c36634bbcb95f22017e9792de5424a8`  
		Last Modified: Sat, 28 Dec 2019 08:40:59 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.3`

```console
$ docker pull varnish@sha256:82ca458edf9556dc63361568ef7dcd2eab27941826fcc13c61e9f68919ca9bcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.3` - linux; amd64

```console
$ docker pull varnish@sha256:cc2ec6bb137e66b8597c187e6d3b970d1b6a60285a283aaac538a486ba18e514
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67422052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1da00c66cf15cc0c521896f822779d978844ab4ae4dc683d114f4636d8a47071`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `["varnishd","-F","-f","\/etc\/varnish\/default.vcl"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:39:01 GMT
ENV VARNISH_VERSION=6.3.1-1~stretch
# Sat, 28 Dec 2019 08:39:36 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=920A8A7AA7120A8604BCCD294A42CD6EB810E55D; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver http://ha.pool.sks-keyservers.net/ --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish63/debian/ stretch main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:39:37 GMT
WORKDIR /etc/varnish
# Sat, 28 Dec 2019 08:39:37 GMT
COPY file:0301ec458d312e5c085462f916888bc85bb94c134ed6116667d225487db56cac in /usr/local/bin/ 
# Sat, 28 Dec 2019 08:39:37 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Sat, 28 Dec 2019 08:39:37 GMT
EXPOSE 80
# Sat, 28 Dec 2019 08:39:38 GMT
CMD ["varnishd" "-F" "-f" "/etc/varnish/default.vcl"]
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cae3b79eb09474b8f1af0d0ba7a7eb8a00d9ae59f4db2571867d9253ff231ec`  
		Last Modified: Sat, 28 Dec 2019 08:40:51 GMT  
		Size: 44.9 MB (44897060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa563190ed24836e8c76af45484cbbce1417d698d8738c2107b68e1aaeb3e73`  
		Last Modified: Sat, 28 Dec 2019 08:40:40 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.3.1`

```console
$ docker pull varnish@sha256:82ca458edf9556dc63361568ef7dcd2eab27941826fcc13c61e9f68919ca9bcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.3.1` - linux; amd64

```console
$ docker pull varnish@sha256:cc2ec6bb137e66b8597c187e6d3b970d1b6a60285a283aaac538a486ba18e514
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67422052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1da00c66cf15cc0c521896f822779d978844ab4ae4dc683d114f4636d8a47071`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `["varnishd","-F","-f","\/etc\/varnish\/default.vcl"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:39:01 GMT
ENV VARNISH_VERSION=6.3.1-1~stretch
# Sat, 28 Dec 2019 08:39:36 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=920A8A7AA7120A8604BCCD294A42CD6EB810E55D; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver http://ha.pool.sks-keyservers.net/ --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish63/debian/ stretch main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:39:37 GMT
WORKDIR /etc/varnish
# Sat, 28 Dec 2019 08:39:37 GMT
COPY file:0301ec458d312e5c085462f916888bc85bb94c134ed6116667d225487db56cac in /usr/local/bin/ 
# Sat, 28 Dec 2019 08:39:37 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Sat, 28 Dec 2019 08:39:37 GMT
EXPOSE 80
# Sat, 28 Dec 2019 08:39:38 GMT
CMD ["varnishd" "-F" "-f" "/etc/varnish/default.vcl"]
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cae3b79eb09474b8f1af0d0ba7a7eb8a00d9ae59f4db2571867d9253ff231ec`  
		Last Modified: Sat, 28 Dec 2019 08:40:51 GMT  
		Size: 44.9 MB (44897060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa563190ed24836e8c76af45484cbbce1417d698d8738c2107b68e1aaeb3e73`  
		Last Modified: Sat, 28 Dec 2019 08:40:40 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.3.1-1`

```console
$ docker pull varnish@sha256:82ca458edf9556dc63361568ef7dcd2eab27941826fcc13c61e9f68919ca9bcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.3.1-1` - linux; amd64

```console
$ docker pull varnish@sha256:cc2ec6bb137e66b8597c187e6d3b970d1b6a60285a283aaac538a486ba18e514
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67422052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1da00c66cf15cc0c521896f822779d978844ab4ae4dc683d114f4636d8a47071`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `["varnishd","-F","-f","\/etc\/varnish\/default.vcl"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:39:01 GMT
ENV VARNISH_VERSION=6.3.1-1~stretch
# Sat, 28 Dec 2019 08:39:36 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=920A8A7AA7120A8604BCCD294A42CD6EB810E55D; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver http://ha.pool.sks-keyservers.net/ --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish63/debian/ stretch main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:39:37 GMT
WORKDIR /etc/varnish
# Sat, 28 Dec 2019 08:39:37 GMT
COPY file:0301ec458d312e5c085462f916888bc85bb94c134ed6116667d225487db56cac in /usr/local/bin/ 
# Sat, 28 Dec 2019 08:39:37 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Sat, 28 Dec 2019 08:39:37 GMT
EXPOSE 80
# Sat, 28 Dec 2019 08:39:38 GMT
CMD ["varnishd" "-F" "-f" "/etc/varnish/default.vcl"]
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cae3b79eb09474b8f1af0d0ba7a7eb8a00d9ae59f4db2571867d9253ff231ec`  
		Last Modified: Sat, 28 Dec 2019 08:40:51 GMT  
		Size: 44.9 MB (44897060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa563190ed24836e8c76af45484cbbce1417d698d8738c2107b68e1aaeb3e73`  
		Last Modified: Sat, 28 Dec 2019 08:40:40 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:fresh`

```console
$ docker pull varnish@sha256:82ca458edf9556dc63361568ef7dcd2eab27941826fcc13c61e9f68919ca9bcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:fresh` - linux; amd64

```console
$ docker pull varnish@sha256:cc2ec6bb137e66b8597c187e6d3b970d1b6a60285a283aaac538a486ba18e514
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67422052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1da00c66cf15cc0c521896f822779d978844ab4ae4dc683d114f4636d8a47071`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `["varnishd","-F","-f","\/etc\/varnish\/default.vcl"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:39:01 GMT
ENV VARNISH_VERSION=6.3.1-1~stretch
# Sat, 28 Dec 2019 08:39:36 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=920A8A7AA7120A8604BCCD294A42CD6EB810E55D; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver http://ha.pool.sks-keyservers.net/ --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish63/debian/ stretch main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:39:37 GMT
WORKDIR /etc/varnish
# Sat, 28 Dec 2019 08:39:37 GMT
COPY file:0301ec458d312e5c085462f916888bc85bb94c134ed6116667d225487db56cac in /usr/local/bin/ 
# Sat, 28 Dec 2019 08:39:37 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Sat, 28 Dec 2019 08:39:37 GMT
EXPOSE 80
# Sat, 28 Dec 2019 08:39:38 GMT
CMD ["varnishd" "-F" "-f" "/etc/varnish/default.vcl"]
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cae3b79eb09474b8f1af0d0ba7a7eb8a00d9ae59f4db2571867d9253ff231ec`  
		Last Modified: Sat, 28 Dec 2019 08:40:51 GMT  
		Size: 44.9 MB (44897060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa563190ed24836e8c76af45484cbbce1417d698d8738c2107b68e1aaeb3e73`  
		Last Modified: Sat, 28 Dec 2019 08:40:40 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:latest`

```console
$ docker pull varnish@sha256:82ca458edf9556dc63361568ef7dcd2eab27941826fcc13c61e9f68919ca9bcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:latest` - linux; amd64

```console
$ docker pull varnish@sha256:cc2ec6bb137e66b8597c187e6d3b970d1b6a60285a283aaac538a486ba18e514
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67422052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1da00c66cf15cc0c521896f822779d978844ab4ae4dc683d114f4636d8a47071`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `["varnishd","-F","-f","\/etc\/varnish\/default.vcl"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:39:01 GMT
ENV VARNISH_VERSION=6.3.1-1~stretch
# Sat, 28 Dec 2019 08:39:36 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=920A8A7AA7120A8604BCCD294A42CD6EB810E55D; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver http://ha.pool.sks-keyservers.net/ --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish63/debian/ stretch main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:39:37 GMT
WORKDIR /etc/varnish
# Sat, 28 Dec 2019 08:39:37 GMT
COPY file:0301ec458d312e5c085462f916888bc85bb94c134ed6116667d225487db56cac in /usr/local/bin/ 
# Sat, 28 Dec 2019 08:39:37 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Sat, 28 Dec 2019 08:39:37 GMT
EXPOSE 80
# Sat, 28 Dec 2019 08:39:38 GMT
CMD ["varnishd" "-F" "-f" "/etc/varnish/default.vcl"]
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cae3b79eb09474b8f1af0d0ba7a7eb8a00d9ae59f4db2571867d9253ff231ec`  
		Last Modified: Sat, 28 Dec 2019 08:40:51 GMT  
		Size: 44.9 MB (44897060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa563190ed24836e8c76af45484cbbce1417d698d8738c2107b68e1aaeb3e73`  
		Last Modified: Sat, 28 Dec 2019 08:40:40 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:stable`

```console
$ docker pull varnish@sha256:1a86025e3297b692f1be2308ae82606c717c17265249d93ff2e31afad7f0cf2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:stable` - linux; amd64

```console
$ docker pull varnish@sha256:97b65d85d8423d0b69b18b018f5ce0737eda0e2888551081dbd2bf3540970a75
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67212471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3dce924eb9db51468c49f4d46d6336b6eb25bb0c3494facef30a331302289f`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `["varnishd","-F","-f","\/etc\/varnish\/default.vcl"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:47 GMT
ADD file:90a2c81769a336bed3f731f44a385f2a65b0916f517a0b77c06c224579bf9a9a in / 
# Sat, 28 Dec 2019 04:23:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 08:39:47 GMT
ENV VARNISH_VERSION=6.0.5-1~stretch
# Sat, 28 Dec 2019 08:40:22 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver http://ha.pool.sks-keyservers.net/ --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ stretch main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 08:40:22 GMT
WORKDIR /etc/varnish
# Sat, 28 Dec 2019 08:40:22 GMT
COPY file:0301ec458d312e5c085462f916888bc85bb94c134ed6116667d225487db56cac in /usr/local/bin/ 
# Sat, 28 Dec 2019 08:40:23 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Sat, 28 Dec 2019 08:40:23 GMT
EXPOSE 80
# Sat, 28 Dec 2019 08:40:23 GMT
CMD ["varnishd" "-F" "-f" "/etc/varnish/default.vcl"]
```

-	Layers:
	-	`sha256:804555ee037604c40de144f9f8da0d826d38db82f15d74cded32790fe279a8f6`  
		Last Modified: Sat, 28 Dec 2019 04:28:38 GMT  
		Size: 22.5 MB (22524609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75d3befb2551921acda03c74674a8ab18e802c7c1ad172029b8270d43c9df75`  
		Last Modified: Sat, 28 Dec 2019 08:41:15 GMT  
		Size: 44.7 MB (44687480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6afdeb276efd7cf4b698b42db8557d9c36634bbcb95f22017e9792de5424a8`  
		Last Modified: Sat, 28 Dec 2019 08:40:59 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
