<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `varnish`

-	[`varnish:6`](#varnish6)
-	[`varnish:6.0`](#varnish60)
-	[`varnish:6.0.6`](#varnish606)
-	[`varnish:6.0.6-1`](#varnish606-1)
-	[`varnish:6.5`](#varnish65)
-	[`varnish:6.5.1`](#varnish651)
-	[`varnish:6.5.1-1`](#varnish651-1)
-	[`varnish:fresh`](#varnishfresh)
-	[`varnish:latest`](#varnishlatest)
-	[`varnish:stable`](#varnishstable)

## `varnish:6`

```console
$ docker pull varnish@sha256:8fa87c400f55a7d7ef79c72c5a27181eea6e1c269ac2ea58ba4175a1167e31b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6` - linux; amd64

```console
$ docker pull varnish@sha256:b230288a4ffa44a8c60fd5da1b7298351bac09cdb568e3ffe245c93957db9b6d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76767316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6efc29b02f9ea5415d19b77f672bac432c52d3e5d324d89bfeb3ef36b707077d`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 20:46:12 GMT
ENV VARNISH_VERSION=6.4.0-1~buster
# Thu, 10 Sep 2020 20:46:12 GMT
ENV VARNISH_SIZE=100M
# Thu, 10 Sep 2020 20:46:36 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A9897320C397E3A60C03E8BF821AD320F71BFF3D; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish64/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 20:46:36 GMT
WORKDIR /etc/varnish
# Thu, 10 Sep 2020 20:46:36 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Thu, 10 Sep 2020 20:46:37 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Thu, 10 Sep 2020 20:46:37 GMT
EXPOSE 80 8443
# Thu, 10 Sep 2020 20:46:37 GMT
CMD []
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c038d5fdc3b60867a1916e0ff78989237dd8c0ac3c9a8fefd34f4d1bd1fb41fc`  
		Last Modified: Thu, 10 Sep 2020 20:47:16 GMT  
		Size: 49.7 MB (49674704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b690c6caf02166ee3c50138688c5b29ddcd3d4c3414a209274cb374f723f779`  
		Last Modified: Thu, 10 Sep 2020 20:47:04 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0`

```console
$ docker pull varnish@sha256:f332d992c3a95f91d62fadbb1acf1a97076411a4f9a25069d1c763e2eb10f41b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.0` - linux; amd64

```console
$ docker pull varnish@sha256:e449d86d736d5f50d6f241f7c2f2dd6c4f508260980f44691232732360420526
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67185782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741853208f0e861c2b154fb057154a4812a599f43007b9595ea9493117e64570`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 10 Sep 2020 00:30:37 GMT
ADD file:83fbd2352bbac612c7a954e19abd295607cea4482c556c225308e0241b58e2bf in / 
# Thu, 10 Sep 2020 00:30:37 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 20:45:38 GMT
ENV VARNISH_VERSION=6.0.6-1~stretch
# Thu, 10 Sep 2020 20:45:38 GMT
ENV VARNISH_SIZE=100M
# Thu, 10 Sep 2020 20:46:03 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ stretch main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 20:46:03 GMT
WORKDIR /etc/varnish
# Thu, 10 Sep 2020 20:46:04 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Thu, 10 Sep 2020 20:46:04 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Thu, 10 Sep 2020 20:46:04 GMT
EXPOSE 80 8443
# Thu, 10 Sep 2020 20:46:04 GMT
CMD []
```

-	Layers:
	-	`sha256:abb454610128b028301ee40af387d31111a1e699e4ea424fd53186ff77067402`  
		Last Modified: Thu, 10 Sep 2020 00:37:40 GMT  
		Size: 22.5 MB (22522274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af7451b6e0fc1ef6f9635b98fb41b0b57ed1ebf19f29fdc40b897c73bd5f62a`  
		Last Modified: Thu, 10 Sep 2020 20:46:59 GMT  
		Size: 44.7 MB (44663046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:335c3d26ec39ced53736f9e55bf9ed12d17abd285e187b3135bc7fc18e661769`  
		Last Modified: Thu, 10 Sep 2020 20:46:50 GMT  
		Size: 462.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0.6`

```console
$ docker pull varnish@sha256:f332d992c3a95f91d62fadbb1acf1a97076411a4f9a25069d1c763e2eb10f41b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.0.6` - linux; amd64

```console
$ docker pull varnish@sha256:e449d86d736d5f50d6f241f7c2f2dd6c4f508260980f44691232732360420526
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67185782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741853208f0e861c2b154fb057154a4812a599f43007b9595ea9493117e64570`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 10 Sep 2020 00:30:37 GMT
ADD file:83fbd2352bbac612c7a954e19abd295607cea4482c556c225308e0241b58e2bf in / 
# Thu, 10 Sep 2020 00:30:37 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 20:45:38 GMT
ENV VARNISH_VERSION=6.0.6-1~stretch
# Thu, 10 Sep 2020 20:45:38 GMT
ENV VARNISH_SIZE=100M
# Thu, 10 Sep 2020 20:46:03 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ stretch main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 20:46:03 GMT
WORKDIR /etc/varnish
# Thu, 10 Sep 2020 20:46:04 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Thu, 10 Sep 2020 20:46:04 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Thu, 10 Sep 2020 20:46:04 GMT
EXPOSE 80 8443
# Thu, 10 Sep 2020 20:46:04 GMT
CMD []
```

-	Layers:
	-	`sha256:abb454610128b028301ee40af387d31111a1e699e4ea424fd53186ff77067402`  
		Last Modified: Thu, 10 Sep 2020 00:37:40 GMT  
		Size: 22.5 MB (22522274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af7451b6e0fc1ef6f9635b98fb41b0b57ed1ebf19f29fdc40b897c73bd5f62a`  
		Last Modified: Thu, 10 Sep 2020 20:46:59 GMT  
		Size: 44.7 MB (44663046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:335c3d26ec39ced53736f9e55bf9ed12d17abd285e187b3135bc7fc18e661769`  
		Last Modified: Thu, 10 Sep 2020 20:46:50 GMT  
		Size: 462.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0.6-1`

```console
$ docker pull varnish@sha256:f332d992c3a95f91d62fadbb1acf1a97076411a4f9a25069d1c763e2eb10f41b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.0.6-1` - linux; amd64

```console
$ docker pull varnish@sha256:e449d86d736d5f50d6f241f7c2f2dd6c4f508260980f44691232732360420526
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67185782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741853208f0e861c2b154fb057154a4812a599f43007b9595ea9493117e64570`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 10 Sep 2020 00:30:37 GMT
ADD file:83fbd2352bbac612c7a954e19abd295607cea4482c556c225308e0241b58e2bf in / 
# Thu, 10 Sep 2020 00:30:37 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 20:45:38 GMT
ENV VARNISH_VERSION=6.0.6-1~stretch
# Thu, 10 Sep 2020 20:45:38 GMT
ENV VARNISH_SIZE=100M
# Thu, 10 Sep 2020 20:46:03 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ stretch main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 20:46:03 GMT
WORKDIR /etc/varnish
# Thu, 10 Sep 2020 20:46:04 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Thu, 10 Sep 2020 20:46:04 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Thu, 10 Sep 2020 20:46:04 GMT
EXPOSE 80 8443
# Thu, 10 Sep 2020 20:46:04 GMT
CMD []
```

-	Layers:
	-	`sha256:abb454610128b028301ee40af387d31111a1e699e4ea424fd53186ff77067402`  
		Last Modified: Thu, 10 Sep 2020 00:37:40 GMT  
		Size: 22.5 MB (22522274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af7451b6e0fc1ef6f9635b98fb41b0b57ed1ebf19f29fdc40b897c73bd5f62a`  
		Last Modified: Thu, 10 Sep 2020 20:46:59 GMT  
		Size: 44.7 MB (44663046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:335c3d26ec39ced53736f9e55bf9ed12d17abd285e187b3135bc7fc18e661769`  
		Last Modified: Thu, 10 Sep 2020 20:46:50 GMT  
		Size: 462.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.5`

```console
$ docker pull varnish@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `varnish:6.5.1`

```console
$ docker pull varnish@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `varnish:6.5.1-1`

```console
$ docker pull varnish@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `varnish:fresh`

```console
$ docker pull varnish@sha256:8fa87c400f55a7d7ef79c72c5a27181eea6e1c269ac2ea58ba4175a1167e31b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:fresh` - linux; amd64

```console
$ docker pull varnish@sha256:b230288a4ffa44a8c60fd5da1b7298351bac09cdb568e3ffe245c93957db9b6d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76767316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6efc29b02f9ea5415d19b77f672bac432c52d3e5d324d89bfeb3ef36b707077d`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 20:46:12 GMT
ENV VARNISH_VERSION=6.4.0-1~buster
# Thu, 10 Sep 2020 20:46:12 GMT
ENV VARNISH_SIZE=100M
# Thu, 10 Sep 2020 20:46:36 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A9897320C397E3A60C03E8BF821AD320F71BFF3D; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish64/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 20:46:36 GMT
WORKDIR /etc/varnish
# Thu, 10 Sep 2020 20:46:36 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Thu, 10 Sep 2020 20:46:37 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Thu, 10 Sep 2020 20:46:37 GMT
EXPOSE 80 8443
# Thu, 10 Sep 2020 20:46:37 GMT
CMD []
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c038d5fdc3b60867a1916e0ff78989237dd8c0ac3c9a8fefd34f4d1bd1fb41fc`  
		Last Modified: Thu, 10 Sep 2020 20:47:16 GMT  
		Size: 49.7 MB (49674704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b690c6caf02166ee3c50138688c5b29ddcd3d4c3414a209274cb374f723f779`  
		Last Modified: Thu, 10 Sep 2020 20:47:04 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:latest`

```console
$ docker pull varnish@sha256:8fa87c400f55a7d7ef79c72c5a27181eea6e1c269ac2ea58ba4175a1167e31b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:latest` - linux; amd64

```console
$ docker pull varnish@sha256:b230288a4ffa44a8c60fd5da1b7298351bac09cdb568e3ffe245c93957db9b6d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76767316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6efc29b02f9ea5415d19b77f672bac432c52d3e5d324d89bfeb3ef36b707077d`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 10 Sep 2020 00:23:29 GMT
ADD file:e7407f2294ad23634565820b9669b18ff2a2ca0212a7ec84b9c89d8550859954 in / 
# Thu, 10 Sep 2020 00:23:30 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 20:46:12 GMT
ENV VARNISH_VERSION=6.4.0-1~buster
# Thu, 10 Sep 2020 20:46:12 GMT
ENV VARNISH_SIZE=100M
# Thu, 10 Sep 2020 20:46:36 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A9897320C397E3A60C03E8BF821AD320F71BFF3D; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish64/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 20:46:36 GMT
WORKDIR /etc/varnish
# Thu, 10 Sep 2020 20:46:36 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Thu, 10 Sep 2020 20:46:37 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Thu, 10 Sep 2020 20:46:37 GMT
EXPOSE 80 8443
# Thu, 10 Sep 2020 20:46:37 GMT
CMD []
```

-	Layers:
	-	`sha256:d121f8d1c4128ebc1e95e5bfad90a0189b84eadbbb2fbaad20cbb26d20b2c8a2`  
		Last Modified: Thu, 10 Sep 2020 00:34:02 GMT  
		Size: 27.1 MB (27092161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c038d5fdc3b60867a1916e0ff78989237dd8c0ac3c9a8fefd34f4d1bd1fb41fc`  
		Last Modified: Thu, 10 Sep 2020 20:47:16 GMT  
		Size: 49.7 MB (49674704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b690c6caf02166ee3c50138688c5b29ddcd3d4c3414a209274cb374f723f779`  
		Last Modified: Thu, 10 Sep 2020 20:47:04 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:stable`

```console
$ docker pull varnish@sha256:f332d992c3a95f91d62fadbb1acf1a97076411a4f9a25069d1c763e2eb10f41b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:stable` - linux; amd64

```console
$ docker pull varnish@sha256:e449d86d736d5f50d6f241f7c2f2dd6c4f508260980f44691232732360420526
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67185782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741853208f0e861c2b154fb057154a4812a599f43007b9595ea9493117e64570`
-	Entrypoint: `["docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Thu, 10 Sep 2020 00:30:37 GMT
ADD file:83fbd2352bbac612c7a954e19abd295607cea4482c556c225308e0241b58e2bf in / 
# Thu, 10 Sep 2020 00:30:37 GMT
CMD ["bash"]
# Thu, 10 Sep 2020 20:45:38 GMT
ENV VARNISH_VERSION=6.0.6-1~stretch
# Thu, 10 Sep 2020 20:45:38 GMT
ENV VARNISH_SIZE=100M
# Thu, 10 Sep 2020 20:46:03 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ stretch main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Thu, 10 Sep 2020 20:46:03 GMT
WORKDIR /etc/varnish
# Thu, 10 Sep 2020 20:46:04 GMT
COPY file:4156d91450dca54febf2b6908a0871cf84271dba1069d9641be798ec9f560393 in /usr/local/bin/ 
# Thu, 10 Sep 2020 20:46:04 GMT
ENTRYPOINT ["docker-varnish-entrypoint"]
# Thu, 10 Sep 2020 20:46:04 GMT
EXPOSE 80 8443
# Thu, 10 Sep 2020 20:46:04 GMT
CMD []
```

-	Layers:
	-	`sha256:abb454610128b028301ee40af387d31111a1e699e4ea424fd53186ff77067402`  
		Last Modified: Thu, 10 Sep 2020 00:37:40 GMT  
		Size: 22.5 MB (22522274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af7451b6e0fc1ef6f9635b98fb41b0b57ed1ebf19f29fdc40b897c73bd5f62a`  
		Last Modified: Thu, 10 Sep 2020 20:46:59 GMT  
		Size: 44.7 MB (44663046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:335c3d26ec39ced53736f9e55bf9ed12d17abd285e187b3135bc7fc18e661769`  
		Last Modified: Thu, 10 Sep 2020 20:46:50 GMT  
		Size: 462.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
