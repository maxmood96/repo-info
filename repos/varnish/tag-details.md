<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `varnish`

-	[`varnish:6`](#varnish6)
-	[`varnish:6.0`](#varnish60)
-	[`varnish:6.0.7`](#varnish607)
-	[`varnish:6.0.7-1`](#varnish607-1)
-	[`varnish:6.5`](#varnish65)
-	[`varnish:6.5.1`](#varnish651)
-	[`varnish:6.5.1-1`](#varnish651-1)
-	[`varnish:fresh`](#varnishfresh)
-	[`varnish:latest`](#varnishlatest)
-	[`varnish:stable`](#varnishstable)

## `varnish:6`

```console
$ docker pull varnish@sha256:7fd83f8170a13b1f205576c2e1c6b8e984b5d899c4e0224e2fd1d37950bf0881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6` - linux; amd64

```console
$ docker pull varnish@sha256:c51e5bde9b13c603aa207081daf3c35a8caaa56f2769942c25e7c833545c3149
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76864281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c3bb4ac2f2056f37f6253ce70dcd6e84f7172902e7bbc182031b8e9d061b84`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:32:09 GMT
ENV VARNISH_VERSION=6.5.1~buster-1
# Fri, 11 Dec 2020 20:32:09 GMT
ENV VARNISH_SIZE=100M
# Fri, 11 Dec 2020 20:32:29 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A487F9BE81D9DF5121488CFE1C7B4E9FF149D65B; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish65/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 20:32:29 GMT
WORKDIR /etc/varnish
# Fri, 11 Dec 2020 20:32:29 GMT
COPY file:f2d309dd6f06236e6a883ab100c62fc6396ac93510452f7833d2089b005f3213 in /usr/local/bin/ 
# Fri, 11 Dec 2020 20:32:30 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Fri, 11 Dec 2020 20:32:30 GMT
EXPOSE 80 8443
# Fri, 11 Dec 2020 20:32:30 GMT
CMD []
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0624c537b3b61e43af4ee95db3e2e8b31d190d4f26c9fe3e10602158fff181`  
		Last Modified: Fri, 11 Dec 2020 20:33:13 GMT  
		Size: 49.8 MB (49764512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001085aa2a4334790c316b75bb95b2fdb80b523656a82dcb908b2168574917d4`  
		Last Modified: Fri, 11 Dec 2020 20:33:04 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0`

```console
$ docker pull varnish@sha256:40b0e0963922f64dc529c1fb9ab95c0fbbc57e169408631108f148295833f511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.0` - linux; amd64

```console
$ docker pull varnish@sha256:9b6dad86ac86604851660167dbd956bc771e212e7eb181483aea85c0e82ef463
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76411915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d7ed6cdeae3b47d53665815aef58854128c6aff8d63d4725e4c85f86fbb4a0`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:31:39 GMT
ENV VARNISH_VERSION=6.0.7-1~buster
# Fri, 11 Dec 2020 20:31:40 GMT
ENV VARNISH_SIZE=100M
# Fri, 11 Dec 2020 20:32:01 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 20:32:01 GMT
WORKDIR /etc/varnish
# Fri, 11 Dec 2020 20:32:01 GMT
COPY file:f2d309dd6f06236e6a883ab100c62fc6396ac93510452f7833d2089b005f3213 in /usr/local/bin/ 
# Fri, 11 Dec 2020 20:32:01 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Fri, 11 Dec 2020 20:32:02 GMT
EXPOSE 80 8443
# Fri, 11 Dec 2020 20:32:02 GMT
CMD []
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886ee72c834ffc51c8b7fcdc25dddad6a767b9ad92a0d6ae2044a67cb202fea8`  
		Last Modified: Fri, 11 Dec 2020 20:32:56 GMT  
		Size: 49.3 MB (49312146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba164a89f57b74f47a3af0a5ceb9368aaf66bed5dcc62c44a6ceb5aa828c71ec`  
		Last Modified: Fri, 11 Dec 2020 20:32:48 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0.7`

```console
$ docker pull varnish@sha256:40b0e0963922f64dc529c1fb9ab95c0fbbc57e169408631108f148295833f511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.0.7` - linux; amd64

```console
$ docker pull varnish@sha256:9b6dad86ac86604851660167dbd956bc771e212e7eb181483aea85c0e82ef463
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76411915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d7ed6cdeae3b47d53665815aef58854128c6aff8d63d4725e4c85f86fbb4a0`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:31:39 GMT
ENV VARNISH_VERSION=6.0.7-1~buster
# Fri, 11 Dec 2020 20:31:40 GMT
ENV VARNISH_SIZE=100M
# Fri, 11 Dec 2020 20:32:01 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 20:32:01 GMT
WORKDIR /etc/varnish
# Fri, 11 Dec 2020 20:32:01 GMT
COPY file:f2d309dd6f06236e6a883ab100c62fc6396ac93510452f7833d2089b005f3213 in /usr/local/bin/ 
# Fri, 11 Dec 2020 20:32:01 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Fri, 11 Dec 2020 20:32:02 GMT
EXPOSE 80 8443
# Fri, 11 Dec 2020 20:32:02 GMT
CMD []
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886ee72c834ffc51c8b7fcdc25dddad6a767b9ad92a0d6ae2044a67cb202fea8`  
		Last Modified: Fri, 11 Dec 2020 20:32:56 GMT  
		Size: 49.3 MB (49312146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba164a89f57b74f47a3af0a5ceb9368aaf66bed5dcc62c44a6ceb5aa828c71ec`  
		Last Modified: Fri, 11 Dec 2020 20:32:48 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0.7-1`

```console
$ docker pull varnish@sha256:40b0e0963922f64dc529c1fb9ab95c0fbbc57e169408631108f148295833f511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.0.7-1` - linux; amd64

```console
$ docker pull varnish@sha256:9b6dad86ac86604851660167dbd956bc771e212e7eb181483aea85c0e82ef463
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76411915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d7ed6cdeae3b47d53665815aef58854128c6aff8d63d4725e4c85f86fbb4a0`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:31:39 GMT
ENV VARNISH_VERSION=6.0.7-1~buster
# Fri, 11 Dec 2020 20:31:40 GMT
ENV VARNISH_SIZE=100M
# Fri, 11 Dec 2020 20:32:01 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 20:32:01 GMT
WORKDIR /etc/varnish
# Fri, 11 Dec 2020 20:32:01 GMT
COPY file:f2d309dd6f06236e6a883ab100c62fc6396ac93510452f7833d2089b005f3213 in /usr/local/bin/ 
# Fri, 11 Dec 2020 20:32:01 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Fri, 11 Dec 2020 20:32:02 GMT
EXPOSE 80 8443
# Fri, 11 Dec 2020 20:32:02 GMT
CMD []
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886ee72c834ffc51c8b7fcdc25dddad6a767b9ad92a0d6ae2044a67cb202fea8`  
		Last Modified: Fri, 11 Dec 2020 20:32:56 GMT  
		Size: 49.3 MB (49312146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba164a89f57b74f47a3af0a5ceb9368aaf66bed5dcc62c44a6ceb5aa828c71ec`  
		Last Modified: Fri, 11 Dec 2020 20:32:48 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.5`

```console
$ docker pull varnish@sha256:7fd83f8170a13b1f205576c2e1c6b8e984b5d899c4e0224e2fd1d37950bf0881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.5` - linux; amd64

```console
$ docker pull varnish@sha256:c51e5bde9b13c603aa207081daf3c35a8caaa56f2769942c25e7c833545c3149
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76864281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c3bb4ac2f2056f37f6253ce70dcd6e84f7172902e7bbc182031b8e9d061b84`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:32:09 GMT
ENV VARNISH_VERSION=6.5.1~buster-1
# Fri, 11 Dec 2020 20:32:09 GMT
ENV VARNISH_SIZE=100M
# Fri, 11 Dec 2020 20:32:29 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A487F9BE81D9DF5121488CFE1C7B4E9FF149D65B; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish65/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 20:32:29 GMT
WORKDIR /etc/varnish
# Fri, 11 Dec 2020 20:32:29 GMT
COPY file:f2d309dd6f06236e6a883ab100c62fc6396ac93510452f7833d2089b005f3213 in /usr/local/bin/ 
# Fri, 11 Dec 2020 20:32:30 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Fri, 11 Dec 2020 20:32:30 GMT
EXPOSE 80 8443
# Fri, 11 Dec 2020 20:32:30 GMT
CMD []
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0624c537b3b61e43af4ee95db3e2e8b31d190d4f26c9fe3e10602158fff181`  
		Last Modified: Fri, 11 Dec 2020 20:33:13 GMT  
		Size: 49.8 MB (49764512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001085aa2a4334790c316b75bb95b2fdb80b523656a82dcb908b2168574917d4`  
		Last Modified: Fri, 11 Dec 2020 20:33:04 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.5.1`

```console
$ docker pull varnish@sha256:7fd83f8170a13b1f205576c2e1c6b8e984b5d899c4e0224e2fd1d37950bf0881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.5.1` - linux; amd64

```console
$ docker pull varnish@sha256:c51e5bde9b13c603aa207081daf3c35a8caaa56f2769942c25e7c833545c3149
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76864281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c3bb4ac2f2056f37f6253ce70dcd6e84f7172902e7bbc182031b8e9d061b84`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:32:09 GMT
ENV VARNISH_VERSION=6.5.1~buster-1
# Fri, 11 Dec 2020 20:32:09 GMT
ENV VARNISH_SIZE=100M
# Fri, 11 Dec 2020 20:32:29 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A487F9BE81D9DF5121488CFE1C7B4E9FF149D65B; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish65/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 20:32:29 GMT
WORKDIR /etc/varnish
# Fri, 11 Dec 2020 20:32:29 GMT
COPY file:f2d309dd6f06236e6a883ab100c62fc6396ac93510452f7833d2089b005f3213 in /usr/local/bin/ 
# Fri, 11 Dec 2020 20:32:30 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Fri, 11 Dec 2020 20:32:30 GMT
EXPOSE 80 8443
# Fri, 11 Dec 2020 20:32:30 GMT
CMD []
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0624c537b3b61e43af4ee95db3e2e8b31d190d4f26c9fe3e10602158fff181`  
		Last Modified: Fri, 11 Dec 2020 20:33:13 GMT  
		Size: 49.8 MB (49764512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001085aa2a4334790c316b75bb95b2fdb80b523656a82dcb908b2168574917d4`  
		Last Modified: Fri, 11 Dec 2020 20:33:04 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.5.1-1`

```console
$ docker pull varnish@sha256:7fd83f8170a13b1f205576c2e1c6b8e984b5d899c4e0224e2fd1d37950bf0881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.5.1-1` - linux; amd64

```console
$ docker pull varnish@sha256:c51e5bde9b13c603aa207081daf3c35a8caaa56f2769942c25e7c833545c3149
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76864281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c3bb4ac2f2056f37f6253ce70dcd6e84f7172902e7bbc182031b8e9d061b84`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:32:09 GMT
ENV VARNISH_VERSION=6.5.1~buster-1
# Fri, 11 Dec 2020 20:32:09 GMT
ENV VARNISH_SIZE=100M
# Fri, 11 Dec 2020 20:32:29 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A487F9BE81D9DF5121488CFE1C7B4E9FF149D65B; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish65/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 20:32:29 GMT
WORKDIR /etc/varnish
# Fri, 11 Dec 2020 20:32:29 GMT
COPY file:f2d309dd6f06236e6a883ab100c62fc6396ac93510452f7833d2089b005f3213 in /usr/local/bin/ 
# Fri, 11 Dec 2020 20:32:30 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Fri, 11 Dec 2020 20:32:30 GMT
EXPOSE 80 8443
# Fri, 11 Dec 2020 20:32:30 GMT
CMD []
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0624c537b3b61e43af4ee95db3e2e8b31d190d4f26c9fe3e10602158fff181`  
		Last Modified: Fri, 11 Dec 2020 20:33:13 GMT  
		Size: 49.8 MB (49764512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001085aa2a4334790c316b75bb95b2fdb80b523656a82dcb908b2168574917d4`  
		Last Modified: Fri, 11 Dec 2020 20:33:04 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:fresh`

```console
$ docker pull varnish@sha256:7fd83f8170a13b1f205576c2e1c6b8e984b5d899c4e0224e2fd1d37950bf0881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:fresh` - linux; amd64

```console
$ docker pull varnish@sha256:c51e5bde9b13c603aa207081daf3c35a8caaa56f2769942c25e7c833545c3149
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76864281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c3bb4ac2f2056f37f6253ce70dcd6e84f7172902e7bbc182031b8e9d061b84`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:32:09 GMT
ENV VARNISH_VERSION=6.5.1~buster-1
# Fri, 11 Dec 2020 20:32:09 GMT
ENV VARNISH_SIZE=100M
# Fri, 11 Dec 2020 20:32:29 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A487F9BE81D9DF5121488CFE1C7B4E9FF149D65B; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish65/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 20:32:29 GMT
WORKDIR /etc/varnish
# Fri, 11 Dec 2020 20:32:29 GMT
COPY file:f2d309dd6f06236e6a883ab100c62fc6396ac93510452f7833d2089b005f3213 in /usr/local/bin/ 
# Fri, 11 Dec 2020 20:32:30 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Fri, 11 Dec 2020 20:32:30 GMT
EXPOSE 80 8443
# Fri, 11 Dec 2020 20:32:30 GMT
CMD []
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0624c537b3b61e43af4ee95db3e2e8b31d190d4f26c9fe3e10602158fff181`  
		Last Modified: Fri, 11 Dec 2020 20:33:13 GMT  
		Size: 49.8 MB (49764512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001085aa2a4334790c316b75bb95b2fdb80b523656a82dcb908b2168574917d4`  
		Last Modified: Fri, 11 Dec 2020 20:33:04 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:latest`

```console
$ docker pull varnish@sha256:7fd83f8170a13b1f205576c2e1c6b8e984b5d899c4e0224e2fd1d37950bf0881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:latest` - linux; amd64

```console
$ docker pull varnish@sha256:c51e5bde9b13c603aa207081daf3c35a8caaa56f2769942c25e7c833545c3149
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76864281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c3bb4ac2f2056f37f6253ce70dcd6e84f7172902e7bbc182031b8e9d061b84`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:32:09 GMT
ENV VARNISH_VERSION=6.5.1~buster-1
# Fri, 11 Dec 2020 20:32:09 GMT
ENV VARNISH_SIZE=100M
# Fri, 11 Dec 2020 20:32:29 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A487F9BE81D9DF5121488CFE1C7B4E9FF149D65B; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish65/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 20:32:29 GMT
WORKDIR /etc/varnish
# Fri, 11 Dec 2020 20:32:29 GMT
COPY file:f2d309dd6f06236e6a883ab100c62fc6396ac93510452f7833d2089b005f3213 in /usr/local/bin/ 
# Fri, 11 Dec 2020 20:32:30 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Fri, 11 Dec 2020 20:32:30 GMT
EXPOSE 80 8443
# Fri, 11 Dec 2020 20:32:30 GMT
CMD []
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0624c537b3b61e43af4ee95db3e2e8b31d190d4f26c9fe3e10602158fff181`  
		Last Modified: Fri, 11 Dec 2020 20:33:13 GMT  
		Size: 49.8 MB (49764512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001085aa2a4334790c316b75bb95b2fdb80b523656a82dcb908b2168574917d4`  
		Last Modified: Fri, 11 Dec 2020 20:33:04 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:stable`

```console
$ docker pull varnish@sha256:40b0e0963922f64dc529c1fb9ab95c0fbbc57e169408631108f148295833f511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:stable` - linux; amd64

```console
$ docker pull varnish@sha256:9b6dad86ac86604851660167dbd956bc771e212e7eb181483aea85c0e82ef463
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76411915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d7ed6cdeae3b47d53665815aef58854128c6aff8d63d4725e4c85f86fbb4a0`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 20:31:39 GMT
ENV VARNISH_VERSION=6.0.7-1~buster
# Fri, 11 Dec 2020 20:31:40 GMT
ENV VARNISH_SIZE=100M
# Fri, 11 Dec 2020 20:32:01 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 20:32:01 GMT
WORKDIR /etc/varnish
# Fri, 11 Dec 2020 20:32:01 GMT
COPY file:f2d309dd6f06236e6a883ab100c62fc6396ac93510452f7833d2089b005f3213 in /usr/local/bin/ 
# Fri, 11 Dec 2020 20:32:01 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Fri, 11 Dec 2020 20:32:02 GMT
EXPOSE 80 8443
# Fri, 11 Dec 2020 20:32:02 GMT
CMD []
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886ee72c834ffc51c8b7fcdc25dddad6a767b9ad92a0d6ae2044a67cb202fea8`  
		Last Modified: Fri, 11 Dec 2020 20:32:56 GMT  
		Size: 49.3 MB (49312146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba164a89f57b74f47a3af0a5ceb9368aaf66bed5dcc62c44a6ceb5aa828c71ec`  
		Last Modified: Fri, 11 Dec 2020 20:32:48 GMT  
		Size: 474.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
