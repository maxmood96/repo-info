<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `varnish`

-	[`varnish:6`](#varnish6)
-	[`varnish:6.0`](#varnish60)
-	[`varnish:6.0.6`](#varnish606)
-	[`varnish:6.0.6-1`](#varnish606-1)
-	[`varnish:6.4`](#varnish64)
-	[`varnish:6.4.0`](#varnish640)
-	[`varnish:6.4.0-1`](#varnish640-1)
-	[`varnish:fresh`](#varnishfresh)
-	[`varnish:latest`](#varnishlatest)
-	[`varnish:stable`](#varnishstable)

## `varnish:6`

```console
$ docker pull varnish@sha256:a1964bfeeabd88f4171f85066383428bfc80d84fe5a8a35f859cefa392ccccb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6` - linux; amd64

```console
$ docker pull varnish@sha256:d08caa66f650c1cf7848b02a0204e015299914b99553911debb0ade0df8102de
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76773403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5699a582cb897e7cc061716a78809a5aeaa1afc8f306c144fcab685c33cdbb81`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:18:39 GMT
ENV VARNISH_VERSION=6.4.0-1~buster
# Tue, 09 Jun 2020 02:18:40 GMT
ENV VARNISH_SIZE=100M
# Tue, 09 Jun 2020 02:19:04 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A9897320C397E3A60C03E8BF821AD320F71BFF3D; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish64/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:19:05 GMT
WORKDIR /etc/varnish
# Tue, 09 Jun 2020 02:19:05 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Tue, 09 Jun 2020 02:19:05 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Tue, 09 Jun 2020 02:19:05 GMT
EXPOSE 80 8443
# Tue, 09 Jun 2020 02:19:06 GMT
CMD []
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2813d20ac69dc5dcb5acd860dd457dc404ca403deb1668c85877b53a042cd151`  
		Last Modified: Tue, 09 Jun 2020 02:19:42 GMT  
		Size: 49.7 MB (49674687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e2d6cfc6ab097304333c8437d005d4efef3bf5e3ae8dc1c71cfe46ea50e253`  
		Last Modified: Tue, 09 Jun 2020 02:19:33 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0`

```console
$ docker pull varnish@sha256:2b51cb720a3277ff15d10ec67e7bf8a417fdb782df731c0e5e92a6e97536b7aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.0` - linux; amd64

```console
$ docker pull varnish@sha256:5054430b542db7e207a124fd491a6b468585b8b9ce2c8385aa60175aa3987800
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67182409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03ec5845def7cd0960039723994384c4811a118d66e0bbbf5eb1c790ebe4f64`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:18:05 GMT
ENV VARNISH_VERSION=6.0.6-1~stretch
# Tue, 09 Jun 2020 02:18:05 GMT
ENV VARNISH_SIZE=100M
# Tue, 09 Jun 2020 02:18:32 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ stretch main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:18:32 GMT
WORKDIR /etc/varnish
# Tue, 09 Jun 2020 02:18:33 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Tue, 09 Jun 2020 02:18:33 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Tue, 09 Jun 2020 02:18:34 GMT
EXPOSE 80 8443
# Tue, 09 Jun 2020 02:18:34 GMT
CMD []
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552c7e657c95e7eab3d8aa333845f45f85effe0475ccbe07f2c15f7465fb462e`  
		Last Modified: Tue, 09 Jun 2020 02:19:26 GMT  
		Size: 44.7 MB (44662349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a2007aacf31c12801a387400f28190aaf6eed5ab5b7a5816653fc06e602479`  
		Last Modified: Tue, 09 Jun 2020 02:19:19 GMT  
		Size: 460.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0.6`

```console
$ docker pull varnish@sha256:2b51cb720a3277ff15d10ec67e7bf8a417fdb782df731c0e5e92a6e97536b7aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.0.6` - linux; amd64

```console
$ docker pull varnish@sha256:5054430b542db7e207a124fd491a6b468585b8b9ce2c8385aa60175aa3987800
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67182409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03ec5845def7cd0960039723994384c4811a118d66e0bbbf5eb1c790ebe4f64`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:18:05 GMT
ENV VARNISH_VERSION=6.0.6-1~stretch
# Tue, 09 Jun 2020 02:18:05 GMT
ENV VARNISH_SIZE=100M
# Tue, 09 Jun 2020 02:18:32 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ stretch main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:18:32 GMT
WORKDIR /etc/varnish
# Tue, 09 Jun 2020 02:18:33 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Tue, 09 Jun 2020 02:18:33 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Tue, 09 Jun 2020 02:18:34 GMT
EXPOSE 80 8443
# Tue, 09 Jun 2020 02:18:34 GMT
CMD []
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552c7e657c95e7eab3d8aa333845f45f85effe0475ccbe07f2c15f7465fb462e`  
		Last Modified: Tue, 09 Jun 2020 02:19:26 GMT  
		Size: 44.7 MB (44662349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a2007aacf31c12801a387400f28190aaf6eed5ab5b7a5816653fc06e602479`  
		Last Modified: Tue, 09 Jun 2020 02:19:19 GMT  
		Size: 460.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0.6-1`

```console
$ docker pull varnish@sha256:2b51cb720a3277ff15d10ec67e7bf8a417fdb782df731c0e5e92a6e97536b7aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.0.6-1` - linux; amd64

```console
$ docker pull varnish@sha256:5054430b542db7e207a124fd491a6b468585b8b9ce2c8385aa60175aa3987800
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67182409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03ec5845def7cd0960039723994384c4811a118d66e0bbbf5eb1c790ebe4f64`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:18:05 GMT
ENV VARNISH_VERSION=6.0.6-1~stretch
# Tue, 09 Jun 2020 02:18:05 GMT
ENV VARNISH_SIZE=100M
# Tue, 09 Jun 2020 02:18:32 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ stretch main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:18:32 GMT
WORKDIR /etc/varnish
# Tue, 09 Jun 2020 02:18:33 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Tue, 09 Jun 2020 02:18:33 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Tue, 09 Jun 2020 02:18:34 GMT
EXPOSE 80 8443
# Tue, 09 Jun 2020 02:18:34 GMT
CMD []
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552c7e657c95e7eab3d8aa333845f45f85effe0475ccbe07f2c15f7465fb462e`  
		Last Modified: Tue, 09 Jun 2020 02:19:26 GMT  
		Size: 44.7 MB (44662349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a2007aacf31c12801a387400f28190aaf6eed5ab5b7a5816653fc06e602479`  
		Last Modified: Tue, 09 Jun 2020 02:19:19 GMT  
		Size: 460.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.4`

```console
$ docker pull varnish@sha256:a1964bfeeabd88f4171f85066383428bfc80d84fe5a8a35f859cefa392ccccb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.4` - linux; amd64

```console
$ docker pull varnish@sha256:d08caa66f650c1cf7848b02a0204e015299914b99553911debb0ade0df8102de
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76773403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5699a582cb897e7cc061716a78809a5aeaa1afc8f306c144fcab685c33cdbb81`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:18:39 GMT
ENV VARNISH_VERSION=6.4.0-1~buster
# Tue, 09 Jun 2020 02:18:40 GMT
ENV VARNISH_SIZE=100M
# Tue, 09 Jun 2020 02:19:04 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A9897320C397E3A60C03E8BF821AD320F71BFF3D; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish64/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:19:05 GMT
WORKDIR /etc/varnish
# Tue, 09 Jun 2020 02:19:05 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Tue, 09 Jun 2020 02:19:05 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Tue, 09 Jun 2020 02:19:05 GMT
EXPOSE 80 8443
# Tue, 09 Jun 2020 02:19:06 GMT
CMD []
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2813d20ac69dc5dcb5acd860dd457dc404ca403deb1668c85877b53a042cd151`  
		Last Modified: Tue, 09 Jun 2020 02:19:42 GMT  
		Size: 49.7 MB (49674687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e2d6cfc6ab097304333c8437d005d4efef3bf5e3ae8dc1c71cfe46ea50e253`  
		Last Modified: Tue, 09 Jun 2020 02:19:33 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.4.0`

```console
$ docker pull varnish@sha256:a1964bfeeabd88f4171f85066383428bfc80d84fe5a8a35f859cefa392ccccb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.4.0` - linux; amd64

```console
$ docker pull varnish@sha256:d08caa66f650c1cf7848b02a0204e015299914b99553911debb0ade0df8102de
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76773403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5699a582cb897e7cc061716a78809a5aeaa1afc8f306c144fcab685c33cdbb81`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:18:39 GMT
ENV VARNISH_VERSION=6.4.0-1~buster
# Tue, 09 Jun 2020 02:18:40 GMT
ENV VARNISH_SIZE=100M
# Tue, 09 Jun 2020 02:19:04 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A9897320C397E3A60C03E8BF821AD320F71BFF3D; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish64/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:19:05 GMT
WORKDIR /etc/varnish
# Tue, 09 Jun 2020 02:19:05 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Tue, 09 Jun 2020 02:19:05 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Tue, 09 Jun 2020 02:19:05 GMT
EXPOSE 80 8443
# Tue, 09 Jun 2020 02:19:06 GMT
CMD []
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2813d20ac69dc5dcb5acd860dd457dc404ca403deb1668c85877b53a042cd151`  
		Last Modified: Tue, 09 Jun 2020 02:19:42 GMT  
		Size: 49.7 MB (49674687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e2d6cfc6ab097304333c8437d005d4efef3bf5e3ae8dc1c71cfe46ea50e253`  
		Last Modified: Tue, 09 Jun 2020 02:19:33 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.4.0-1`

```console
$ docker pull varnish@sha256:a1964bfeeabd88f4171f85066383428bfc80d84fe5a8a35f859cefa392ccccb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.4.0-1` - linux; amd64

```console
$ docker pull varnish@sha256:d08caa66f650c1cf7848b02a0204e015299914b99553911debb0ade0df8102de
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76773403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5699a582cb897e7cc061716a78809a5aeaa1afc8f306c144fcab685c33cdbb81`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:18:39 GMT
ENV VARNISH_VERSION=6.4.0-1~buster
# Tue, 09 Jun 2020 02:18:40 GMT
ENV VARNISH_SIZE=100M
# Tue, 09 Jun 2020 02:19:04 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A9897320C397E3A60C03E8BF821AD320F71BFF3D; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish64/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:19:05 GMT
WORKDIR /etc/varnish
# Tue, 09 Jun 2020 02:19:05 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Tue, 09 Jun 2020 02:19:05 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Tue, 09 Jun 2020 02:19:05 GMT
EXPOSE 80 8443
# Tue, 09 Jun 2020 02:19:06 GMT
CMD []
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2813d20ac69dc5dcb5acd860dd457dc404ca403deb1668c85877b53a042cd151`  
		Last Modified: Tue, 09 Jun 2020 02:19:42 GMT  
		Size: 49.7 MB (49674687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e2d6cfc6ab097304333c8437d005d4efef3bf5e3ae8dc1c71cfe46ea50e253`  
		Last Modified: Tue, 09 Jun 2020 02:19:33 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:fresh`

```console
$ docker pull varnish@sha256:a1964bfeeabd88f4171f85066383428bfc80d84fe5a8a35f859cefa392ccccb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:fresh` - linux; amd64

```console
$ docker pull varnish@sha256:d08caa66f650c1cf7848b02a0204e015299914b99553911debb0ade0df8102de
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76773403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5699a582cb897e7cc061716a78809a5aeaa1afc8f306c144fcab685c33cdbb81`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:18:39 GMT
ENV VARNISH_VERSION=6.4.0-1~buster
# Tue, 09 Jun 2020 02:18:40 GMT
ENV VARNISH_SIZE=100M
# Tue, 09 Jun 2020 02:19:04 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A9897320C397E3A60C03E8BF821AD320F71BFF3D; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish64/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:19:05 GMT
WORKDIR /etc/varnish
# Tue, 09 Jun 2020 02:19:05 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Tue, 09 Jun 2020 02:19:05 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Tue, 09 Jun 2020 02:19:05 GMT
EXPOSE 80 8443
# Tue, 09 Jun 2020 02:19:06 GMT
CMD []
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2813d20ac69dc5dcb5acd860dd457dc404ca403deb1668c85877b53a042cd151`  
		Last Modified: Tue, 09 Jun 2020 02:19:42 GMT  
		Size: 49.7 MB (49674687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e2d6cfc6ab097304333c8437d005d4efef3bf5e3ae8dc1c71cfe46ea50e253`  
		Last Modified: Tue, 09 Jun 2020 02:19:33 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:latest`

```console
$ docker pull varnish@sha256:a1964bfeeabd88f4171f85066383428bfc80d84fe5a8a35f859cefa392ccccb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:latest` - linux; amd64

```console
$ docker pull varnish@sha256:d08caa66f650c1cf7848b02a0204e015299914b99553911debb0ade0df8102de
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76773403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5699a582cb897e7cc061716a78809a5aeaa1afc8f306c144fcab685c33cdbb81`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 09 Jun 2020 01:20:56 GMT
ADD file:4d35f6c8bbbe6801cc5f44989730fb6d349a644ecb36eca481e7df25842d6321 in / 
# Tue, 09 Jun 2020 01:20:56 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:18:39 GMT
ENV VARNISH_VERSION=6.4.0-1~buster
# Tue, 09 Jun 2020 02:18:40 GMT
ENV VARNISH_SIZE=100M
# Tue, 09 Jun 2020 02:19:04 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A9897320C397E3A60C03E8BF821AD320F71BFF3D; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish64/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:19:05 GMT
WORKDIR /etc/varnish
# Tue, 09 Jun 2020 02:19:05 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Tue, 09 Jun 2020 02:19:05 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Tue, 09 Jun 2020 02:19:05 GMT
EXPOSE 80 8443
# Tue, 09 Jun 2020 02:19:06 GMT
CMD []
```

-	Layers:
	-	`sha256:8559a31e96f442f2c7b6da49d6c84705f98a39d8be10b3f5f14821d0ee8417df`  
		Last Modified: Tue, 09 Jun 2020 01:25:50 GMT  
		Size: 27.1 MB (27098265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2813d20ac69dc5dcb5acd860dd457dc404ca403deb1668c85877b53a042cd151`  
		Last Modified: Tue, 09 Jun 2020 02:19:42 GMT  
		Size: 49.7 MB (49674687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e2d6cfc6ab097304333c8437d005d4efef3bf5e3ae8dc1c71cfe46ea50e253`  
		Last Modified: Tue, 09 Jun 2020 02:19:33 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:stable`

```console
$ docker pull varnish@sha256:2b51cb720a3277ff15d10ec67e7bf8a417fdb782df731c0e5e92a6e97536b7aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:stable` - linux; amd64

```console
$ docker pull varnish@sha256:5054430b542db7e207a124fd491a6b468585b8b9ce2c8385aa60175aa3987800
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67182409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03ec5845def7cd0960039723994384c4811a118d66e0bbbf5eb1c790ebe4f64`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Tue, 09 Jun 2020 01:23:35 GMT
ADD file:57b431451a292755d0f13673f5f3bea9f62aea36c7a1b59d34d7d200ba134fea in / 
# Tue, 09 Jun 2020 01:23:35 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:18:05 GMT
ENV VARNISH_VERSION=6.0.6-1~stretch
# Tue, 09 Jun 2020 02:18:05 GMT
ENV VARNISH_SIZE=100M
# Tue, 09 Jun 2020 02:18:32 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://hkps.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ stretch main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:18:32 GMT
WORKDIR /etc/varnish
# Tue, 09 Jun 2020 02:18:33 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Tue, 09 Jun 2020 02:18:33 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Tue, 09 Jun 2020 02:18:34 GMT
EXPOSE 80 8443
# Tue, 09 Jun 2020 02:18:34 GMT
CMD []
```

-	Layers:
	-	`sha256:7d2977b12acb33f192e3f20b7e15a467cc8f3f5124a15d975a6d4afe5fa3d258`  
		Last Modified: Tue, 09 Jun 2020 01:28:13 GMT  
		Size: 22.5 MB (22519600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552c7e657c95e7eab3d8aa333845f45f85effe0475ccbe07f2c15f7465fb462e`  
		Last Modified: Tue, 09 Jun 2020 02:19:26 GMT  
		Size: 44.7 MB (44662349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a2007aacf31c12801a387400f28190aaf6eed5ab5b7a5816653fc06e602479`  
		Last Modified: Tue, 09 Jun 2020 02:19:19 GMT  
		Size: 460.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
