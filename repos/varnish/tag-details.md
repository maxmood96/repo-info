<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `varnish`

-	[`varnish:6`](#varnish6)
-	[`varnish:6.0`](#varnish60)
-	[`varnish:6.0.7`](#varnish607)
-	[`varnish:6.0.7-1`](#varnish607-1)
-	[`varnish:6.6`](#varnish66)
-	[`varnish:6.6.0`](#varnish660)
-	[`varnish:6.6.0-1`](#varnish660-1)
-	[`varnish:fresh`](#varnishfresh)
-	[`varnish:latest`](#varnishlatest)
-	[`varnish:stable`](#varnishstable)

## `varnish:6`

```console
$ docker pull varnish@sha256:71a81db8bdf24dd90914d53c38eafd441d1e1ef9a939e1e3a92266e871bd44ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6` - linux; amd64

```console
$ docker pull varnish@sha256:f3b546c1a2b9c692d747e19f3a253e1dbc30af708a2f1c84fde211ef65d1e64e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77059845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48dd3aac2d9d901d6be746cd2523ea6449d58aa3549ab494da071db835275a6e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 18:28:09 GMT
ENV VARNISH_VERSION=6.6.0-1~buster
# Sat, 10 Apr 2021 18:28:09 GMT
ENV VARNISH_SIZE=100M
# Sat, 10 Apr 2021 18:28:30 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A0378A38E4EACA3660789E570BAC19E3F6C90CD5; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish66/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 18:28:31 GMT
WORKDIR /etc/varnish
# Thu, 15 Apr 2021 09:31:37 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 15 Apr 2021 09:31:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 15 Apr 2021 09:31:38 GMT
EXPOSE 80 8443
# Thu, 15 Apr 2021 09:31:38 GMT
CMD []
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02bdb7e1f8cd4b21cf0142ef5bdede74348a97eb0a15afed783d24138b22ddf8`  
		Last Modified: Sat, 10 Apr 2021 18:29:21 GMT  
		Size: 49.9 MB (49919779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5819de27b48cee692679eb70f5c88f3a4c7e1528625e559642b0369b23fbdc18`  
		Last Modified: Thu, 15 Apr 2021 09:32:12 GMT  
		Size: 693.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0`

```console
$ docker pull varnish@sha256:49efe520b39e2218daf2d4998faaefb4cf865f9050ded1734c400abbfa06703d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.0` - linux; amd64

```console
$ docker pull varnish@sha256:8f0fbdb41d3d1ade4ffdf21558443f4c03342010563bb8c43ccc09594d507012
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76475432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad385eb764cc7dc465d7f041f7bce1746b1d2d9e46aeaee670bee65382bd5ea3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 18:27:43 GMT
ENV VARNISH_VERSION=6.0.7-1~buster
# Sat, 10 Apr 2021 18:27:44 GMT
ENV VARNISH_SIZE=100M
# Sat, 10 Apr 2021 18:28:02 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 18:28:03 GMT
WORKDIR /etc/varnish
# Thu, 15 Apr 2021 09:31:33 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 15 Apr 2021 09:31:33 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 15 Apr 2021 09:31:34 GMT
EXPOSE 80 8443
# Thu, 15 Apr 2021 09:31:34 GMT
CMD []
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcc88e2995613aecaf8e035ae3995fc5ff4eccdd84c5e4a36c1e2cb92ab1dc8`  
		Last Modified: Sat, 10 Apr 2021 18:28:59 GMT  
		Size: 49.3 MB (49335366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2902b45b1d060f276b6e35a15842e98ada8ca51c2c18b6c0f12a7a6d394ee031`  
		Last Modified: Thu, 15 Apr 2021 09:31:57 GMT  
		Size: 693.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0.7`

```console
$ docker pull varnish@sha256:49efe520b39e2218daf2d4998faaefb4cf865f9050ded1734c400abbfa06703d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.0.7` - linux; amd64

```console
$ docker pull varnish@sha256:8f0fbdb41d3d1ade4ffdf21558443f4c03342010563bb8c43ccc09594d507012
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76475432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad385eb764cc7dc465d7f041f7bce1746b1d2d9e46aeaee670bee65382bd5ea3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 18:27:43 GMT
ENV VARNISH_VERSION=6.0.7-1~buster
# Sat, 10 Apr 2021 18:27:44 GMT
ENV VARNISH_SIZE=100M
# Sat, 10 Apr 2021 18:28:02 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 18:28:03 GMT
WORKDIR /etc/varnish
# Thu, 15 Apr 2021 09:31:33 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 15 Apr 2021 09:31:33 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 15 Apr 2021 09:31:34 GMT
EXPOSE 80 8443
# Thu, 15 Apr 2021 09:31:34 GMT
CMD []
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcc88e2995613aecaf8e035ae3995fc5ff4eccdd84c5e4a36c1e2cb92ab1dc8`  
		Last Modified: Sat, 10 Apr 2021 18:28:59 GMT  
		Size: 49.3 MB (49335366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2902b45b1d060f276b6e35a15842e98ada8ca51c2c18b6c0f12a7a6d394ee031`  
		Last Modified: Thu, 15 Apr 2021 09:31:57 GMT  
		Size: 693.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.0.7-1`

```console
$ docker pull varnish@sha256:49efe520b39e2218daf2d4998faaefb4cf865f9050ded1734c400abbfa06703d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.0.7-1` - linux; amd64

```console
$ docker pull varnish@sha256:8f0fbdb41d3d1ade4ffdf21558443f4c03342010563bb8c43ccc09594d507012
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76475432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad385eb764cc7dc465d7f041f7bce1746b1d2d9e46aeaee670bee65382bd5ea3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 18:27:43 GMT
ENV VARNISH_VERSION=6.0.7-1~buster
# Sat, 10 Apr 2021 18:27:44 GMT
ENV VARNISH_SIZE=100M
# Sat, 10 Apr 2021 18:28:02 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 18:28:03 GMT
WORKDIR /etc/varnish
# Thu, 15 Apr 2021 09:31:33 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 15 Apr 2021 09:31:33 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 15 Apr 2021 09:31:34 GMT
EXPOSE 80 8443
# Thu, 15 Apr 2021 09:31:34 GMT
CMD []
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcc88e2995613aecaf8e035ae3995fc5ff4eccdd84c5e4a36c1e2cb92ab1dc8`  
		Last Modified: Sat, 10 Apr 2021 18:28:59 GMT  
		Size: 49.3 MB (49335366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2902b45b1d060f276b6e35a15842e98ada8ca51c2c18b6c0f12a7a6d394ee031`  
		Last Modified: Thu, 15 Apr 2021 09:31:57 GMT  
		Size: 693.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.6`

```console
$ docker pull varnish@sha256:71a81db8bdf24dd90914d53c38eafd441d1e1ef9a939e1e3a92266e871bd44ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.6` - linux; amd64

```console
$ docker pull varnish@sha256:f3b546c1a2b9c692d747e19f3a253e1dbc30af708a2f1c84fde211ef65d1e64e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77059845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48dd3aac2d9d901d6be746cd2523ea6449d58aa3549ab494da071db835275a6e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 18:28:09 GMT
ENV VARNISH_VERSION=6.6.0-1~buster
# Sat, 10 Apr 2021 18:28:09 GMT
ENV VARNISH_SIZE=100M
# Sat, 10 Apr 2021 18:28:30 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A0378A38E4EACA3660789E570BAC19E3F6C90CD5; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish66/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 18:28:31 GMT
WORKDIR /etc/varnish
# Thu, 15 Apr 2021 09:31:37 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 15 Apr 2021 09:31:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 15 Apr 2021 09:31:38 GMT
EXPOSE 80 8443
# Thu, 15 Apr 2021 09:31:38 GMT
CMD []
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02bdb7e1f8cd4b21cf0142ef5bdede74348a97eb0a15afed783d24138b22ddf8`  
		Last Modified: Sat, 10 Apr 2021 18:29:21 GMT  
		Size: 49.9 MB (49919779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5819de27b48cee692679eb70f5c88f3a4c7e1528625e559642b0369b23fbdc18`  
		Last Modified: Thu, 15 Apr 2021 09:32:12 GMT  
		Size: 693.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.6.0`

```console
$ docker pull varnish@sha256:71a81db8bdf24dd90914d53c38eafd441d1e1ef9a939e1e3a92266e871bd44ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.6.0` - linux; amd64

```console
$ docker pull varnish@sha256:f3b546c1a2b9c692d747e19f3a253e1dbc30af708a2f1c84fde211ef65d1e64e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77059845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48dd3aac2d9d901d6be746cd2523ea6449d58aa3549ab494da071db835275a6e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 18:28:09 GMT
ENV VARNISH_VERSION=6.6.0-1~buster
# Sat, 10 Apr 2021 18:28:09 GMT
ENV VARNISH_SIZE=100M
# Sat, 10 Apr 2021 18:28:30 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A0378A38E4EACA3660789E570BAC19E3F6C90CD5; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish66/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 18:28:31 GMT
WORKDIR /etc/varnish
# Thu, 15 Apr 2021 09:31:37 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 15 Apr 2021 09:31:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 15 Apr 2021 09:31:38 GMT
EXPOSE 80 8443
# Thu, 15 Apr 2021 09:31:38 GMT
CMD []
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02bdb7e1f8cd4b21cf0142ef5bdede74348a97eb0a15afed783d24138b22ddf8`  
		Last Modified: Sat, 10 Apr 2021 18:29:21 GMT  
		Size: 49.9 MB (49919779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5819de27b48cee692679eb70f5c88f3a4c7e1528625e559642b0369b23fbdc18`  
		Last Modified: Thu, 15 Apr 2021 09:32:12 GMT  
		Size: 693.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:6.6.0-1`

```console
$ docker pull varnish@sha256:71a81db8bdf24dd90914d53c38eafd441d1e1ef9a939e1e3a92266e871bd44ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:6.6.0-1` - linux; amd64

```console
$ docker pull varnish@sha256:f3b546c1a2b9c692d747e19f3a253e1dbc30af708a2f1c84fde211ef65d1e64e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77059845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48dd3aac2d9d901d6be746cd2523ea6449d58aa3549ab494da071db835275a6e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 18:28:09 GMT
ENV VARNISH_VERSION=6.6.0-1~buster
# Sat, 10 Apr 2021 18:28:09 GMT
ENV VARNISH_SIZE=100M
# Sat, 10 Apr 2021 18:28:30 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A0378A38E4EACA3660789E570BAC19E3F6C90CD5; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish66/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 18:28:31 GMT
WORKDIR /etc/varnish
# Thu, 15 Apr 2021 09:31:37 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 15 Apr 2021 09:31:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 15 Apr 2021 09:31:38 GMT
EXPOSE 80 8443
# Thu, 15 Apr 2021 09:31:38 GMT
CMD []
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02bdb7e1f8cd4b21cf0142ef5bdede74348a97eb0a15afed783d24138b22ddf8`  
		Last Modified: Sat, 10 Apr 2021 18:29:21 GMT  
		Size: 49.9 MB (49919779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5819de27b48cee692679eb70f5c88f3a4c7e1528625e559642b0369b23fbdc18`  
		Last Modified: Thu, 15 Apr 2021 09:32:12 GMT  
		Size: 693.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:fresh`

```console
$ docker pull varnish@sha256:71a81db8bdf24dd90914d53c38eafd441d1e1ef9a939e1e3a92266e871bd44ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:fresh` - linux; amd64

```console
$ docker pull varnish@sha256:f3b546c1a2b9c692d747e19f3a253e1dbc30af708a2f1c84fde211ef65d1e64e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77059845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48dd3aac2d9d901d6be746cd2523ea6449d58aa3549ab494da071db835275a6e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 18:28:09 GMT
ENV VARNISH_VERSION=6.6.0-1~buster
# Sat, 10 Apr 2021 18:28:09 GMT
ENV VARNISH_SIZE=100M
# Sat, 10 Apr 2021 18:28:30 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A0378A38E4EACA3660789E570BAC19E3F6C90CD5; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish66/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 18:28:31 GMT
WORKDIR /etc/varnish
# Thu, 15 Apr 2021 09:31:37 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 15 Apr 2021 09:31:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 15 Apr 2021 09:31:38 GMT
EXPOSE 80 8443
# Thu, 15 Apr 2021 09:31:38 GMT
CMD []
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02bdb7e1f8cd4b21cf0142ef5bdede74348a97eb0a15afed783d24138b22ddf8`  
		Last Modified: Sat, 10 Apr 2021 18:29:21 GMT  
		Size: 49.9 MB (49919779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5819de27b48cee692679eb70f5c88f3a4c7e1528625e559642b0369b23fbdc18`  
		Last Modified: Thu, 15 Apr 2021 09:32:12 GMT  
		Size: 693.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:latest`

```console
$ docker pull varnish@sha256:71a81db8bdf24dd90914d53c38eafd441d1e1ef9a939e1e3a92266e871bd44ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:latest` - linux; amd64

```console
$ docker pull varnish@sha256:f3b546c1a2b9c692d747e19f3a253e1dbc30af708a2f1c84fde211ef65d1e64e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77059845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48dd3aac2d9d901d6be746cd2523ea6449d58aa3549ab494da071db835275a6e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 18:28:09 GMT
ENV VARNISH_VERSION=6.6.0-1~buster
# Sat, 10 Apr 2021 18:28:09 GMT
ENV VARNISH_SIZE=100M
# Sat, 10 Apr 2021 18:28:30 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=A0378A38E4EACA3660789E570BAC19E3F6C90CD5; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish66/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 18:28:31 GMT
WORKDIR /etc/varnish
# Thu, 15 Apr 2021 09:31:37 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 15 Apr 2021 09:31:37 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 15 Apr 2021 09:31:38 GMT
EXPOSE 80 8443
# Thu, 15 Apr 2021 09:31:38 GMT
CMD []
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02bdb7e1f8cd4b21cf0142ef5bdede74348a97eb0a15afed783d24138b22ddf8`  
		Last Modified: Sat, 10 Apr 2021 18:29:21 GMT  
		Size: 49.9 MB (49919779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5819de27b48cee692679eb70f5c88f3a4c7e1528625e559642b0369b23fbdc18`  
		Last Modified: Thu, 15 Apr 2021 09:32:12 GMT  
		Size: 693.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `varnish:stable`

```console
$ docker pull varnish@sha256:49efe520b39e2218daf2d4998faaefb4cf865f9050ded1734c400abbfa06703d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `varnish:stable` - linux; amd64

```console
$ docker pull varnish@sha256:8f0fbdb41d3d1ade4ffdf21558443f4c03342010563bb8c43ccc09594d507012
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76475432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad385eb764cc7dc465d7f041f7bce1746b1d2d9e46aeaee670bee65382bd5ea3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-varnish-entrypoint"]`
-	Default Command: `[]`

```dockerfile
# Sat, 10 Apr 2021 01:20:22 GMT
ADD file:c855b3c65f5ba94d548d7d2659094eeb63fbf7f8419ac8e07712c3320c38b62c in / 
# Sat, 10 Apr 2021 01:20:22 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 18:27:43 GMT
ENV VARNISH_VERSION=6.0.7-1~buster
# Sat, 10 Apr 2021 18:27:44 GMT
ENV VARNISH_SIZE=100M
# Sat, 10 Apr 2021 18:28:02 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends apt-transport-https ca-certificates $fetchDeps; 	key=48D81A24CB0456F5D59431D94CFCFD6BA750EDCD; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys $key; 	gpg --batch --export export $key > /etc/apt/trusted.gpg.d/varnish.gpg; 	gpgconf --kill all; 	rm -rf $GNUPGHOME; 	echo deb https://packagecloud.io/varnishcache/varnish60lts/debian/ buster main > /etc/apt/sources.list.d/varnish.list; 	apt-get update; 	apt-get install -y --no-install-recommends varnish=$VARNISH_VERSION; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 18:28:03 GMT
WORKDIR /etc/varnish
# Thu, 15 Apr 2021 09:31:33 GMT
COPY dir:81cfdf3570a33a2213eb3396395161c2375769c233d0e51a4b70c65b389fabfa in /usr/local/bin/ 
# Thu, 15 Apr 2021 09:31:33 GMT
ENTRYPOINT ["/usr/local/bin/docker-varnish-entrypoint"]
# Thu, 15 Apr 2021 09:31:34 GMT
EXPOSE 80 8443
# Thu, 15 Apr 2021 09:31:34 GMT
CMD []
```

-	Layers:
	-	`sha256:f7ec5a41d630a33a2d1db59b95d89d93de7ae5a619a3a8571b78457e48266eba`  
		Last Modified: Sat, 10 Apr 2021 01:25:20 GMT  
		Size: 27.1 MB (27139373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcc88e2995613aecaf8e035ae3995fc5ff4eccdd84c5e4a36c1e2cb92ab1dc8`  
		Last Modified: Sat, 10 Apr 2021 18:28:59 GMT  
		Size: 49.3 MB (49335366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2902b45b1d060f276b6e35a15842e98ada8ca51c2c18b6c0f12a7a6d394ee031`  
		Last Modified: Thu, 15 Apr 2021 09:31:57 GMT  
		Size: 693.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
