<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:5`](#emqx5)
-	[`emqx:5.1`](#emqx51)
-	[`emqx:5.1.6`](#emqx516)
-	[`emqx:5.2`](#emqx52)
-	[`emqx:5.2.1`](#emqx521)
-	[`emqx:5.3`](#emqx53)
-	[`emqx:5.3.2`](#emqx532)
-	[`emqx:5.4`](#emqx54)
-	[`emqx:5.4.1`](#emqx541)
-	[`emqx:5.5`](#emqx55)
-	[`emqx:5.5.0`](#emqx550)
-	[`emqx:latest`](#emqxlatest)

## `emqx:5`

```console
$ docker pull emqx@sha256:a0a1023420cc3ea9d5330eab022f8ccc4caee4169d4f51aa5146f87c519c7ec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:def8ae6a5900ce6efb85637960d72adb6b4db69f8fbe821dc943945bb2ccf506
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121252485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffff2f88287e4af7f6d60933cf4c1f9f2019d716ac346a210d133f2275d94d72`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Tue, 06 Feb 2024 01:54:28 GMT
ENV EMQX_VERSION=5.5.0
# Tue, 06 Feb 2024 01:54:28 GMT
ENV AMD64_SHA256=31af6514bcd30cab68272e1ff9553f652520cf82afed8894b3c4fe0fae55da88
# Tue, 06 Feb 2024 01:54:28 GMT
ENV ARM64_SHA256=45f46c99ae9561aac13b25f909df6ac1f971d4ce4aa594ff3711a1c95e8d9d9e
# Tue, 06 Feb 2024 01:54:28 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 06 Feb 2024 01:54:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Feb 2024 01:54:43 GMT
WORKDIR /opt/emqx
# Tue, 06 Feb 2024 01:54:43 GMT
USER emqx
# Tue, 06 Feb 2024 01:54:43 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 06 Feb 2024 01:54:43 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 06 Feb 2024 01:54:43 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 06 Feb 2024 01:54:44 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 06 Feb 2024 01:54:44 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8901d41c85ca9ebab394246426c72c13c3dfc1435f591082316c22b7a03b3715`  
		Last Modified: Tue, 06 Feb 2024 01:55:12 GMT  
		Size: 89.8 MB (89833753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c30c0994c3f3db0039c666c744f93f85a59f3805a664ae7857a134576186216`  
		Last Modified: Tue, 06 Feb 2024 01:55:03 GMT  
		Size: 905.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8df89a3698b4a72941fa1ff3580da7c33e1dfd37652bc0ec20ec5323be4e07f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116785334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27fae1dc82850c4fd1546147133034ffcc62ec208e0a7f2cd00fc627a7c50303`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:42 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Wed, 31 Jan 2024 22:44:42 GMT
CMD ["bash"]
# Mon, 05 Feb 2024 19:39:34 GMT
ENV EMQX_VERSION=5.5.0
# Mon, 05 Feb 2024 19:39:34 GMT
ENV AMD64_SHA256=31af6514bcd30cab68272e1ff9553f652520cf82afed8894b3c4fe0fae55da88
# Mon, 05 Feb 2024 19:39:34 GMT
ENV ARM64_SHA256=45f46c99ae9561aac13b25f909df6ac1f971d4ce4aa594ff3711a1c95e8d9d9e
# Mon, 05 Feb 2024 19:39:34 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 05 Feb 2024 19:39:47 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Mon, 05 Feb 2024 19:39:48 GMT
WORKDIR /opt/emqx
# Mon, 05 Feb 2024 19:39:48 GMT
USER emqx
# Mon, 05 Feb 2024 19:39:48 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 05 Feb 2024 19:39:48 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Mon, 05 Feb 2024 19:39:48 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Mon, 05 Feb 2024 19:39:48 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 05 Feb 2024 19:39:48 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:731ff59e9ae9c27353a4caf2f7a4bc1e3c1eb2a148b49912d2638271bcdeeed6`  
		Last Modified: Mon, 05 Feb 2024 19:40:12 GMT  
		Size: 86.7 MB (86720094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb7a5e31767d758e0fbc4886da9ad4fbbfdadb2b3ff1567f6797086454167e4`  
		Last Modified: Mon, 05 Feb 2024 19:40:05 GMT  
		Size: 906.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.1`

```console
$ docker pull emqx@sha256:8c05d076d8841ab87352c7bae2a3acd40b3b0a9989022c7529094f59ea40fd75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.1` - linux; amd64

```console
$ docker pull emqx@sha256:1c50ffb930e4abeb9eb90f21c1d411770d790a69d653378c2244838a637efc68
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102393780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd1c5696c618a29acf122bcb91ed726f41999d23566c44a324ce4efe5246a01d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 00:19:02 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 00:19:03 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 01 Feb 2024 00:19:03 GMT
ENV EMQX_VERSION=5.1.6
# Thu, 01 Feb 2024 00:19:03 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Thu, 01 Feb 2024 00:19:03 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Thu, 01 Feb 2024 00:19:03 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 01 Feb 2024 00:19:09 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Thu, 01 Feb 2024 00:19:09 GMT
WORKDIR /opt/emqx
# Thu, 01 Feb 2024 00:19:10 GMT
USER emqx
# Thu, 01 Feb 2024 00:19:10 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 01 Feb 2024 00:19:10 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 01 Feb 2024 00:19:10 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 01 Feb 2024 00:19:10 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 01 Feb 2024 00:19:10 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1ea124470962a0d95c2d41c00207581896c240680afc852dae2a58553e0087`  
		Last Modified: Thu, 01 Feb 2024 00:20:22 GMT  
		Size: 3.0 MB (2989672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26d988df2a049c827d5c51ebbd35ac4b1a4d796daf6478d6247fa05884f5e02`  
		Last Modified: Thu, 01 Feb 2024 00:20:21 GMT  
		Size: 4.1 KB (4110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c7516b4ac2815159f317363145557b65515bd42a9c83f8dd70eaf0cd395294`  
		Last Modified: Thu, 01 Feb 2024 00:20:28 GMT  
		Size: 68.0 MB (67981267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a9d23e0bb0a6a7c2156c6a0fbbb319eb8c720fd4dc8432b6a2e2f908fb57bf`  
		Last Modified: Thu, 01 Feb 2024 00:20:21 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:2cb25f9bc335f1ff642aead39421fadee1e736f67e97d55f360258ec5395e86b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92700157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0d77fefb0c002f9591263589e6e0108f967c763ed264e61fc3cd3f4e29d033`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:42 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Wed, 31 Jan 2024 22:44:42 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 00:02:06 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 00:02:07 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 01 Feb 2024 00:02:07 GMT
ENV EMQX_VERSION=5.1.6
# Thu, 01 Feb 2024 00:02:07 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Thu, 01 Feb 2024 00:02:07 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Thu, 01 Feb 2024 00:02:07 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 01 Feb 2024 00:02:13 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Thu, 01 Feb 2024 00:02:13 GMT
WORKDIR /opt/emqx
# Thu, 01 Feb 2024 00:02:13 GMT
USER emqx
# Thu, 01 Feb 2024 00:02:13 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 01 Feb 2024 00:02:13 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 01 Feb 2024 00:02:13 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 01 Feb 2024 00:02:13 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 01 Feb 2024 00:02:13 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c7efa1236df4442d8a16b73ae12407834b7f073108b1f086cb61f795528fe8`  
		Last Modified: Thu, 01 Feb 2024 00:03:14 GMT  
		Size: 3.0 MB (3006174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa813d1b283a68eae173579d047cc380684d221b4d4f795704dacaec84c0a42f`  
		Last Modified: Thu, 01 Feb 2024 00:03:14 GMT  
		Size: 4.1 KB (4113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c06331d0182f18e0e6c10059a68da96b9cb17883ad292c48799b57336c8d6a`  
		Last Modified: Thu, 01 Feb 2024 00:03:19 GMT  
		Size: 59.6 MB (59624631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa416b7714d90948dff8e4b12d583fde75e6796dd9271f013008556f54b897b`  
		Last Modified: Thu, 01 Feb 2024 00:03:14 GMT  
		Size: 905.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.1.6`

```console
$ docker pull emqx@sha256:8c05d076d8841ab87352c7bae2a3acd40b3b0a9989022c7529094f59ea40fd75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.1.6` - linux; amd64

```console
$ docker pull emqx@sha256:1c50ffb930e4abeb9eb90f21c1d411770d790a69d653378c2244838a637efc68
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102393780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd1c5696c618a29acf122bcb91ed726f41999d23566c44a324ce4efe5246a01d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 00:19:02 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 00:19:03 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 01 Feb 2024 00:19:03 GMT
ENV EMQX_VERSION=5.1.6
# Thu, 01 Feb 2024 00:19:03 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Thu, 01 Feb 2024 00:19:03 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Thu, 01 Feb 2024 00:19:03 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 01 Feb 2024 00:19:09 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Thu, 01 Feb 2024 00:19:09 GMT
WORKDIR /opt/emqx
# Thu, 01 Feb 2024 00:19:10 GMT
USER emqx
# Thu, 01 Feb 2024 00:19:10 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 01 Feb 2024 00:19:10 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 01 Feb 2024 00:19:10 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 01 Feb 2024 00:19:10 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 01 Feb 2024 00:19:10 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1ea124470962a0d95c2d41c00207581896c240680afc852dae2a58553e0087`  
		Last Modified: Thu, 01 Feb 2024 00:20:22 GMT  
		Size: 3.0 MB (2989672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26d988df2a049c827d5c51ebbd35ac4b1a4d796daf6478d6247fa05884f5e02`  
		Last Modified: Thu, 01 Feb 2024 00:20:21 GMT  
		Size: 4.1 KB (4110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c7516b4ac2815159f317363145557b65515bd42a9c83f8dd70eaf0cd395294`  
		Last Modified: Thu, 01 Feb 2024 00:20:28 GMT  
		Size: 68.0 MB (67981267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a9d23e0bb0a6a7c2156c6a0fbbb319eb8c720fd4dc8432b6a2e2f908fb57bf`  
		Last Modified: Thu, 01 Feb 2024 00:20:21 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.1.6` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:2cb25f9bc335f1ff642aead39421fadee1e736f67e97d55f360258ec5395e86b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92700157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0d77fefb0c002f9591263589e6e0108f967c763ed264e61fc3cd3f4e29d033`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:42 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Wed, 31 Jan 2024 22:44:42 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 00:02:06 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 00:02:07 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 01 Feb 2024 00:02:07 GMT
ENV EMQX_VERSION=5.1.6
# Thu, 01 Feb 2024 00:02:07 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Thu, 01 Feb 2024 00:02:07 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Thu, 01 Feb 2024 00:02:07 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 01 Feb 2024 00:02:13 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Thu, 01 Feb 2024 00:02:13 GMT
WORKDIR /opt/emqx
# Thu, 01 Feb 2024 00:02:13 GMT
USER emqx
# Thu, 01 Feb 2024 00:02:13 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 01 Feb 2024 00:02:13 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 01 Feb 2024 00:02:13 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 01 Feb 2024 00:02:13 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 01 Feb 2024 00:02:13 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c7efa1236df4442d8a16b73ae12407834b7f073108b1f086cb61f795528fe8`  
		Last Modified: Thu, 01 Feb 2024 00:03:14 GMT  
		Size: 3.0 MB (3006174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa813d1b283a68eae173579d047cc380684d221b4d4f795704dacaec84c0a42f`  
		Last Modified: Thu, 01 Feb 2024 00:03:14 GMT  
		Size: 4.1 KB (4113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c06331d0182f18e0e6c10059a68da96b9cb17883ad292c48799b57336c8d6a`  
		Last Modified: Thu, 01 Feb 2024 00:03:19 GMT  
		Size: 59.6 MB (59624631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa416b7714d90948dff8e4b12d583fde75e6796dd9271f013008556f54b897b`  
		Last Modified: Thu, 01 Feb 2024 00:03:14 GMT  
		Size: 905.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.2`

```console
$ docker pull emqx@sha256:ad4eaab9e8d743310d0d5aa1725aa3fd5c8020b1a97c39ddf78ae4a83fc9a90e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.2` - linux; amd64

```console
$ docker pull emqx@sha256:7a48200f24767b491945aa6d7dc03bac5d97fc8942cb0fd10b3e29c73d6c0002
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101165472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22907d49a254d50418c2ace35bc4bc200a30ffeac20e251c8ad174103557d936`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 00:19:19 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 00:19:19 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 01 Feb 2024 00:19:19 GMT
ENV EMQX_VERSION=5.2.1
# Thu, 01 Feb 2024 00:19:19 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Thu, 01 Feb 2024 00:19:19 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Thu, 01 Feb 2024 00:19:19 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 01 Feb 2024 00:19:30 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Thu, 01 Feb 2024 00:19:30 GMT
WORKDIR /opt/emqx
# Thu, 01 Feb 2024 00:19:30 GMT
USER emqx
# Thu, 01 Feb 2024 00:19:30 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 01 Feb 2024 00:19:30 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 01 Feb 2024 00:19:30 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 01 Feb 2024 00:19:30 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 01 Feb 2024 00:19:30 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ee3d941bacc67c2d8508d914b26912940758e681e8e1603b4c88755a848e20`  
		Last Modified: Thu, 01 Feb 2024 00:20:37 GMT  
		Size: 1.6 MB (1631626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc8e42401a2fb7652aa17cb774731387b00c132bb0a75e7f7a3797f346f829a`  
		Last Modified: Thu, 01 Feb 2024 00:20:37 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a26a7ce77cf69b6561dd6e2773c39a824386e45f09b7dab0a49e2991de84a92c`  
		Last Modified: Thu, 01 Feb 2024 00:20:44 GMT  
		Size: 68.1 MB (68111007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602e4c5d9209c03a7e099e65e36fc639bfe41fd95e17b866098dbf1097c06adb`  
		Last Modified: Thu, 01 Feb 2024 00:20:37 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:3f2f7aa2c362cf9ed3d44408232693833021d6f026592d561bb59e144b33fee4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91467129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087b06202787ffcf1791c418b639df8273333b91c285932c1310a6a852cbbdc0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:42 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Wed, 31 Jan 2024 22:44:42 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 00:02:20 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 00:02:20 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 01 Feb 2024 00:02:20 GMT
ENV EMQX_VERSION=5.2.1
# Thu, 01 Feb 2024 00:02:20 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Thu, 01 Feb 2024 00:02:20 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Thu, 01 Feb 2024 00:02:20 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 01 Feb 2024 00:02:29 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Thu, 01 Feb 2024 00:02:29 GMT
WORKDIR /opt/emqx
# Thu, 01 Feb 2024 00:02:29 GMT
USER emqx
# Thu, 01 Feb 2024 00:02:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 01 Feb 2024 00:02:29 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 01 Feb 2024 00:02:29 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 01 Feb 2024 00:02:29 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 01 Feb 2024 00:02:30 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83ee1a8bca00247e89738be8ccf497ee5d155c724a3c51a6a8d7fd924bca131`  
		Last Modified: Thu, 01 Feb 2024 00:03:28 GMT  
		Size: 1.6 MB (1645905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a09e62b2e2e2513987dcde294b206e3ff419fce84d1e904528b68b932b6d5ec`  
		Last Modified: Thu, 01 Feb 2024 00:03:28 GMT  
		Size: 4.1 KB (4114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5c16e0525086d0376c1dff019ba29384d7dc6eb85137b9b02864fc67aa6c54`  
		Last Modified: Thu, 01 Feb 2024 00:03:33 GMT  
		Size: 59.8 MB (59751873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c0d0de301baf12838185cf61a51e12fd899263a060ed9db212da341b9820d2`  
		Last Modified: Thu, 01 Feb 2024 00:03:28 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.2.1`

```console
$ docker pull emqx@sha256:ad4eaab9e8d743310d0d5aa1725aa3fd5c8020b1a97c39ddf78ae4a83fc9a90e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.2.1` - linux; amd64

```console
$ docker pull emqx@sha256:7a48200f24767b491945aa6d7dc03bac5d97fc8942cb0fd10b3e29c73d6c0002
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101165472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22907d49a254d50418c2ace35bc4bc200a30ffeac20e251c8ad174103557d936`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 00:19:19 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 00:19:19 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 01 Feb 2024 00:19:19 GMT
ENV EMQX_VERSION=5.2.1
# Thu, 01 Feb 2024 00:19:19 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Thu, 01 Feb 2024 00:19:19 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Thu, 01 Feb 2024 00:19:19 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 01 Feb 2024 00:19:30 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Thu, 01 Feb 2024 00:19:30 GMT
WORKDIR /opt/emqx
# Thu, 01 Feb 2024 00:19:30 GMT
USER emqx
# Thu, 01 Feb 2024 00:19:30 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 01 Feb 2024 00:19:30 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 01 Feb 2024 00:19:30 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 01 Feb 2024 00:19:30 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 01 Feb 2024 00:19:30 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ee3d941bacc67c2d8508d914b26912940758e681e8e1603b4c88755a848e20`  
		Last Modified: Thu, 01 Feb 2024 00:20:37 GMT  
		Size: 1.6 MB (1631626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc8e42401a2fb7652aa17cb774731387b00c132bb0a75e7f7a3797f346f829a`  
		Last Modified: Thu, 01 Feb 2024 00:20:37 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a26a7ce77cf69b6561dd6e2773c39a824386e45f09b7dab0a49e2991de84a92c`  
		Last Modified: Thu, 01 Feb 2024 00:20:44 GMT  
		Size: 68.1 MB (68111007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602e4c5d9209c03a7e099e65e36fc639bfe41fd95e17b866098dbf1097c06adb`  
		Last Modified: Thu, 01 Feb 2024 00:20:37 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.2.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:3f2f7aa2c362cf9ed3d44408232693833021d6f026592d561bb59e144b33fee4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91467129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087b06202787ffcf1791c418b639df8273333b91c285932c1310a6a852cbbdc0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:42 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Wed, 31 Jan 2024 22:44:42 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 00:02:20 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 00:02:20 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 01 Feb 2024 00:02:20 GMT
ENV EMQX_VERSION=5.2.1
# Thu, 01 Feb 2024 00:02:20 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Thu, 01 Feb 2024 00:02:20 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Thu, 01 Feb 2024 00:02:20 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 01 Feb 2024 00:02:29 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Thu, 01 Feb 2024 00:02:29 GMT
WORKDIR /opt/emqx
# Thu, 01 Feb 2024 00:02:29 GMT
USER emqx
# Thu, 01 Feb 2024 00:02:29 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 01 Feb 2024 00:02:29 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 01 Feb 2024 00:02:29 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 01 Feb 2024 00:02:29 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 01 Feb 2024 00:02:30 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83ee1a8bca00247e89738be8ccf497ee5d155c724a3c51a6a8d7fd924bca131`  
		Last Modified: Thu, 01 Feb 2024 00:03:28 GMT  
		Size: 1.6 MB (1645905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a09e62b2e2e2513987dcde294b206e3ff419fce84d1e904528b68b932b6d5ec`  
		Last Modified: Thu, 01 Feb 2024 00:03:28 GMT  
		Size: 4.1 KB (4114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5c16e0525086d0376c1dff019ba29384d7dc6eb85137b9b02864fc67aa6c54`  
		Last Modified: Thu, 01 Feb 2024 00:03:33 GMT  
		Size: 59.8 MB (59751873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c0d0de301baf12838185cf61a51e12fd899263a060ed9db212da341b9820d2`  
		Last Modified: Thu, 01 Feb 2024 00:03:28 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.3`

```console
$ docker pull emqx@sha256:93ed8e0f80e470e6bfb21f6e8f1b08b3ca6b09b9dc674f2dbfdd0db7b8e17563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.3` - linux; amd64

```console
$ docker pull emqx@sha256:f65a8e2e9fa733b3396f91d889d18f9c67cb83885edbc59e8934550d7c605127
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101780819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c19ed98825eb531e4e24aca5d617f15ce3b5c8a7adfd67a1d6aa10590a8251`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 00:19:35 GMT
ENV EMQX_VERSION=5.3.2
# Thu, 01 Feb 2024 00:19:35 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Thu, 01 Feb 2024 00:19:35 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Thu, 01 Feb 2024 00:19:35 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 01 Feb 2024 00:19:48 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 00:19:48 GMT
WORKDIR /opt/emqx
# Thu, 01 Feb 2024 00:19:48 GMT
USER emqx
# Thu, 01 Feb 2024 00:19:49 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 01 Feb 2024 00:19:49 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 01 Feb 2024 00:19:49 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 01 Feb 2024 00:19:49 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 01 Feb 2024 00:19:49 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dadcbaa0d9347255d40e4ef7e78f3971d40a5b339670fd6a044fb9318e10312c`  
		Last Modified: Thu, 01 Feb 2024 00:21:00 GMT  
		Size: 70.4 MB (70362088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cc38b82c18875134b7ff73a10eabc31b570cfabb7f386ac12f349a45902e08`  
		Last Modified: Thu, 01 Feb 2024 00:20:52 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.3` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:c2378db42ad1666b2bf9b24564bc2b0cfa616393e68a72f7eda662c2529bd293
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92081016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e2d4e0ea2adab44583c22ac7ea4ef1eacf10eed4ca073a99c06ab8220b51214`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:42 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Wed, 31 Jan 2024 22:44:42 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 00:02:32 GMT
ENV EMQX_VERSION=5.3.2
# Thu, 01 Feb 2024 00:02:32 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Thu, 01 Feb 2024 00:02:32 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Thu, 01 Feb 2024 00:02:32 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 01 Feb 2024 00:02:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 00:02:43 GMT
WORKDIR /opt/emqx
# Thu, 01 Feb 2024 00:02:44 GMT
USER emqx
# Thu, 01 Feb 2024 00:02:44 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 01 Feb 2024 00:02:44 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 01 Feb 2024 00:02:44 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 01 Feb 2024 00:02:44 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 01 Feb 2024 00:02:44 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa6209eb45329979ce0759cf75a9a648f1d9321f9dd9106fb9b17f066a008e4`  
		Last Modified: Thu, 01 Feb 2024 00:03:47 GMT  
		Size: 62.0 MB (62015779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae335dedb823fd521f604a2fa268145735b9bdee3b6dc67040182a4946fe39e`  
		Last Modified: Thu, 01 Feb 2024 00:03:42 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.3.2`

```console
$ docker pull emqx@sha256:93ed8e0f80e470e6bfb21f6e8f1b08b3ca6b09b9dc674f2dbfdd0db7b8e17563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.3.2` - linux; amd64

```console
$ docker pull emqx@sha256:f65a8e2e9fa733b3396f91d889d18f9c67cb83885edbc59e8934550d7c605127
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101780819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c19ed98825eb531e4e24aca5d617f15ce3b5c8a7adfd67a1d6aa10590a8251`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 00:19:35 GMT
ENV EMQX_VERSION=5.3.2
# Thu, 01 Feb 2024 00:19:35 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Thu, 01 Feb 2024 00:19:35 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Thu, 01 Feb 2024 00:19:35 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 01 Feb 2024 00:19:48 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 00:19:48 GMT
WORKDIR /opt/emqx
# Thu, 01 Feb 2024 00:19:48 GMT
USER emqx
# Thu, 01 Feb 2024 00:19:49 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 01 Feb 2024 00:19:49 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 01 Feb 2024 00:19:49 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 01 Feb 2024 00:19:49 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 01 Feb 2024 00:19:49 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dadcbaa0d9347255d40e4ef7e78f3971d40a5b339670fd6a044fb9318e10312c`  
		Last Modified: Thu, 01 Feb 2024 00:21:00 GMT  
		Size: 70.4 MB (70362088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cc38b82c18875134b7ff73a10eabc31b570cfabb7f386ac12f349a45902e08`  
		Last Modified: Thu, 01 Feb 2024 00:20:52 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.3.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:c2378db42ad1666b2bf9b24564bc2b0cfa616393e68a72f7eda662c2529bd293
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92081016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e2d4e0ea2adab44583c22ac7ea4ef1eacf10eed4ca073a99c06ab8220b51214`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:42 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Wed, 31 Jan 2024 22:44:42 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 00:02:32 GMT
ENV EMQX_VERSION=5.3.2
# Thu, 01 Feb 2024 00:02:32 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Thu, 01 Feb 2024 00:02:32 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Thu, 01 Feb 2024 00:02:32 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 01 Feb 2024 00:02:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 00:02:43 GMT
WORKDIR /opt/emqx
# Thu, 01 Feb 2024 00:02:44 GMT
USER emqx
# Thu, 01 Feb 2024 00:02:44 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 01 Feb 2024 00:02:44 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 01 Feb 2024 00:02:44 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 01 Feb 2024 00:02:44 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 01 Feb 2024 00:02:44 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa6209eb45329979ce0759cf75a9a648f1d9321f9dd9106fb9b17f066a008e4`  
		Last Modified: Thu, 01 Feb 2024 00:03:47 GMT  
		Size: 62.0 MB (62015779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ae335dedb823fd521f604a2fa268145735b9bdee3b6dc67040182a4946fe39e`  
		Last Modified: Thu, 01 Feb 2024 00:03:42 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.4`

```console
$ docker pull emqx@sha256:f6bd1d9e14416e09bca6fa1beab0e80ef196449eba1f828de44f012bba87ffc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.4` - linux; amd64

```console
$ docker pull emqx@sha256:c0fdd90c417aa93c53ec0f98f594931e4d3848230c41820ebd157c42f39e2a40
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118695004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16826d107fe6f2cd3c7c3413009bf8dc5b1e0231df08d41820f7128b1e12f82`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 00:19:52 GMT
ENV EMQX_VERSION=5.4.1
# Thu, 01 Feb 2024 00:19:52 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Thu, 01 Feb 2024 00:19:52 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Thu, 01 Feb 2024 00:19:52 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 01 Feb 2024 00:20:06 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 00:20:06 GMT
WORKDIR /opt/emqx
# Thu, 01 Feb 2024 00:20:07 GMT
USER emqx
# Thu, 01 Feb 2024 00:20:07 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 01 Feb 2024 00:20:07 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 01 Feb 2024 00:20:07 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 01 Feb 2024 00:20:07 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 01 Feb 2024 00:20:07 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bbc534d97bc3b27ba207eae3a140270ee21b861293c644470942adc8cc4c69`  
		Last Modified: Thu, 01 Feb 2024 00:21:17 GMT  
		Size: 87.3 MB (87276273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929fa0e862212d8c7e973ed21b652662a34ceb0ee1eaa67e00634e03699795d3`  
		Last Modified: Thu, 01 Feb 2024 00:21:08 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:543c112ea8017c2604518ec00d74a56f83912ba74ac7938873ff46d66a30b057
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108476636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c40f212d9ad82222c0035532b6f8b3e6e6b2ab10e9129fa6798c089a5c19b6aa`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:42 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Wed, 31 Jan 2024 22:44:42 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 00:02:46 GMT
ENV EMQX_VERSION=5.4.1
# Thu, 01 Feb 2024 00:02:46 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Thu, 01 Feb 2024 00:02:46 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Thu, 01 Feb 2024 00:02:46 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 01 Feb 2024 00:02:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 00:02:58 GMT
WORKDIR /opt/emqx
# Thu, 01 Feb 2024 00:02:58 GMT
USER emqx
# Thu, 01 Feb 2024 00:02:59 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 01 Feb 2024 00:02:59 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 01 Feb 2024 00:02:59 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 01 Feb 2024 00:02:59 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 01 Feb 2024 00:02:59 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d7b6f206ea859ddec90bbdd61079f3f2e7fc1832cf9891d316da8b6ee57fe56`  
		Last Modified: Thu, 01 Feb 2024 00:04:03 GMT  
		Size: 78.4 MB (78411399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2edb843ee112cdb9ef94ae2f060ddbeb6f797d2c26aaf1920ef5ef7dfba250f1`  
		Last Modified: Thu, 01 Feb 2024 00:03:57 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.4.1`

```console
$ docker pull emqx@sha256:f6bd1d9e14416e09bca6fa1beab0e80ef196449eba1f828de44f012bba87ffc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.4.1` - linux; amd64

```console
$ docker pull emqx@sha256:c0fdd90c417aa93c53ec0f98f594931e4d3848230c41820ebd157c42f39e2a40
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118695004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16826d107fe6f2cd3c7c3413009bf8dc5b1e0231df08d41820f7128b1e12f82`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 00:19:52 GMT
ENV EMQX_VERSION=5.4.1
# Thu, 01 Feb 2024 00:19:52 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Thu, 01 Feb 2024 00:19:52 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Thu, 01 Feb 2024 00:19:52 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 01 Feb 2024 00:20:06 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 00:20:06 GMT
WORKDIR /opt/emqx
# Thu, 01 Feb 2024 00:20:07 GMT
USER emqx
# Thu, 01 Feb 2024 00:20:07 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 01 Feb 2024 00:20:07 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 01 Feb 2024 00:20:07 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 01 Feb 2024 00:20:07 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 01 Feb 2024 00:20:07 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bbc534d97bc3b27ba207eae3a140270ee21b861293c644470942adc8cc4c69`  
		Last Modified: Thu, 01 Feb 2024 00:21:17 GMT  
		Size: 87.3 MB (87276273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929fa0e862212d8c7e973ed21b652662a34ceb0ee1eaa67e00634e03699795d3`  
		Last Modified: Thu, 01 Feb 2024 00:21:08 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.4.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:543c112ea8017c2604518ec00d74a56f83912ba74ac7938873ff46d66a30b057
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108476636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c40f212d9ad82222c0035532b6f8b3e6e6b2ab10e9129fa6798c089a5c19b6aa`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:42 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Wed, 31 Jan 2024 22:44:42 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 00:02:46 GMT
ENV EMQX_VERSION=5.4.1
# Thu, 01 Feb 2024 00:02:46 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Thu, 01 Feb 2024 00:02:46 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Thu, 01 Feb 2024 00:02:46 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 01 Feb 2024 00:02:58 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 00:02:58 GMT
WORKDIR /opt/emqx
# Thu, 01 Feb 2024 00:02:58 GMT
USER emqx
# Thu, 01 Feb 2024 00:02:59 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 01 Feb 2024 00:02:59 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 01 Feb 2024 00:02:59 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 01 Feb 2024 00:02:59 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 01 Feb 2024 00:02:59 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d7b6f206ea859ddec90bbdd61079f3f2e7fc1832cf9891d316da8b6ee57fe56`  
		Last Modified: Thu, 01 Feb 2024 00:04:03 GMT  
		Size: 78.4 MB (78411399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2edb843ee112cdb9ef94ae2f060ddbeb6f797d2c26aaf1920ef5ef7dfba250f1`  
		Last Modified: Thu, 01 Feb 2024 00:03:57 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.5`

```console
$ docker pull emqx@sha256:a0a1023420cc3ea9d5330eab022f8ccc4caee4169d4f51aa5146f87c519c7ec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.5` - linux; amd64

```console
$ docker pull emqx@sha256:def8ae6a5900ce6efb85637960d72adb6b4db69f8fbe821dc943945bb2ccf506
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121252485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffff2f88287e4af7f6d60933cf4c1f9f2019d716ac346a210d133f2275d94d72`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Tue, 06 Feb 2024 01:54:28 GMT
ENV EMQX_VERSION=5.5.0
# Tue, 06 Feb 2024 01:54:28 GMT
ENV AMD64_SHA256=31af6514bcd30cab68272e1ff9553f652520cf82afed8894b3c4fe0fae55da88
# Tue, 06 Feb 2024 01:54:28 GMT
ENV ARM64_SHA256=45f46c99ae9561aac13b25f909df6ac1f971d4ce4aa594ff3711a1c95e8d9d9e
# Tue, 06 Feb 2024 01:54:28 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 06 Feb 2024 01:54:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Feb 2024 01:54:43 GMT
WORKDIR /opt/emqx
# Tue, 06 Feb 2024 01:54:43 GMT
USER emqx
# Tue, 06 Feb 2024 01:54:43 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 06 Feb 2024 01:54:43 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 06 Feb 2024 01:54:43 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 06 Feb 2024 01:54:44 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 06 Feb 2024 01:54:44 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8901d41c85ca9ebab394246426c72c13c3dfc1435f591082316c22b7a03b3715`  
		Last Modified: Tue, 06 Feb 2024 01:55:12 GMT  
		Size: 89.8 MB (89833753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c30c0994c3f3db0039c666c744f93f85a59f3805a664ae7857a134576186216`  
		Last Modified: Tue, 06 Feb 2024 01:55:03 GMT  
		Size: 905.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8df89a3698b4a72941fa1ff3580da7c33e1dfd37652bc0ec20ec5323be4e07f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116785334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27fae1dc82850c4fd1546147133034ffcc62ec208e0a7f2cd00fc627a7c50303`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:42 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Wed, 31 Jan 2024 22:44:42 GMT
CMD ["bash"]
# Mon, 05 Feb 2024 19:39:34 GMT
ENV EMQX_VERSION=5.5.0
# Mon, 05 Feb 2024 19:39:34 GMT
ENV AMD64_SHA256=31af6514bcd30cab68272e1ff9553f652520cf82afed8894b3c4fe0fae55da88
# Mon, 05 Feb 2024 19:39:34 GMT
ENV ARM64_SHA256=45f46c99ae9561aac13b25f909df6ac1f971d4ce4aa594ff3711a1c95e8d9d9e
# Mon, 05 Feb 2024 19:39:34 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 05 Feb 2024 19:39:47 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Mon, 05 Feb 2024 19:39:48 GMT
WORKDIR /opt/emqx
# Mon, 05 Feb 2024 19:39:48 GMT
USER emqx
# Mon, 05 Feb 2024 19:39:48 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 05 Feb 2024 19:39:48 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Mon, 05 Feb 2024 19:39:48 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Mon, 05 Feb 2024 19:39:48 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 05 Feb 2024 19:39:48 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:731ff59e9ae9c27353a4caf2f7a4bc1e3c1eb2a148b49912d2638271bcdeeed6`  
		Last Modified: Mon, 05 Feb 2024 19:40:12 GMT  
		Size: 86.7 MB (86720094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb7a5e31767d758e0fbc4886da9ad4fbbfdadb2b3ff1567f6797086454167e4`  
		Last Modified: Mon, 05 Feb 2024 19:40:05 GMT  
		Size: 906.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.5.0`

```console
$ docker pull emqx@sha256:a0a1023420cc3ea9d5330eab022f8ccc4caee4169d4f51aa5146f87c519c7ec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.5.0` - linux; amd64

```console
$ docker pull emqx@sha256:def8ae6a5900ce6efb85637960d72adb6b4db69f8fbe821dc943945bb2ccf506
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121252485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffff2f88287e4af7f6d60933cf4c1f9f2019d716ac346a210d133f2275d94d72`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Tue, 06 Feb 2024 01:54:28 GMT
ENV EMQX_VERSION=5.5.0
# Tue, 06 Feb 2024 01:54:28 GMT
ENV AMD64_SHA256=31af6514bcd30cab68272e1ff9553f652520cf82afed8894b3c4fe0fae55da88
# Tue, 06 Feb 2024 01:54:28 GMT
ENV ARM64_SHA256=45f46c99ae9561aac13b25f909df6ac1f971d4ce4aa594ff3711a1c95e8d9d9e
# Tue, 06 Feb 2024 01:54:28 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 06 Feb 2024 01:54:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Feb 2024 01:54:43 GMT
WORKDIR /opt/emqx
# Tue, 06 Feb 2024 01:54:43 GMT
USER emqx
# Tue, 06 Feb 2024 01:54:43 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 06 Feb 2024 01:54:43 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 06 Feb 2024 01:54:43 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 06 Feb 2024 01:54:44 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 06 Feb 2024 01:54:44 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8901d41c85ca9ebab394246426c72c13c3dfc1435f591082316c22b7a03b3715`  
		Last Modified: Tue, 06 Feb 2024 01:55:12 GMT  
		Size: 89.8 MB (89833753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c30c0994c3f3db0039c666c744f93f85a59f3805a664ae7857a134576186216`  
		Last Modified: Tue, 06 Feb 2024 01:55:03 GMT  
		Size: 905.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.5.0` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8df89a3698b4a72941fa1ff3580da7c33e1dfd37652bc0ec20ec5323be4e07f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116785334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27fae1dc82850c4fd1546147133034ffcc62ec208e0a7f2cd00fc627a7c50303`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:42 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Wed, 31 Jan 2024 22:44:42 GMT
CMD ["bash"]
# Mon, 05 Feb 2024 19:39:34 GMT
ENV EMQX_VERSION=5.5.0
# Mon, 05 Feb 2024 19:39:34 GMT
ENV AMD64_SHA256=31af6514bcd30cab68272e1ff9553f652520cf82afed8894b3c4fe0fae55da88
# Mon, 05 Feb 2024 19:39:34 GMT
ENV ARM64_SHA256=45f46c99ae9561aac13b25f909df6ac1f971d4ce4aa594ff3711a1c95e8d9d9e
# Mon, 05 Feb 2024 19:39:34 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 05 Feb 2024 19:39:47 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Mon, 05 Feb 2024 19:39:48 GMT
WORKDIR /opt/emqx
# Mon, 05 Feb 2024 19:39:48 GMT
USER emqx
# Mon, 05 Feb 2024 19:39:48 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 05 Feb 2024 19:39:48 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Mon, 05 Feb 2024 19:39:48 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Mon, 05 Feb 2024 19:39:48 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 05 Feb 2024 19:39:48 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:731ff59e9ae9c27353a4caf2f7a4bc1e3c1eb2a148b49912d2638271bcdeeed6`  
		Last Modified: Mon, 05 Feb 2024 19:40:12 GMT  
		Size: 86.7 MB (86720094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb7a5e31767d758e0fbc4886da9ad4fbbfdadb2b3ff1567f6797086454167e4`  
		Last Modified: Mon, 05 Feb 2024 19:40:05 GMT  
		Size: 906.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:latest`

```console
$ docker pull emqx@sha256:a0a1023420cc3ea9d5330eab022f8ccc4caee4169d4f51aa5146f87c519c7ec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:def8ae6a5900ce6efb85637960d72adb6b4db69f8fbe821dc943945bb2ccf506
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121252485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffff2f88287e4af7f6d60933cf4c1f9f2019d716ac346a210d133f2275d94d72`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:41 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
# Wed, 31 Jan 2024 22:35:41 GMT
CMD ["bash"]
# Tue, 06 Feb 2024 01:54:28 GMT
ENV EMQX_VERSION=5.5.0
# Tue, 06 Feb 2024 01:54:28 GMT
ENV AMD64_SHA256=31af6514bcd30cab68272e1ff9553f652520cf82afed8894b3c4fe0fae55da88
# Tue, 06 Feb 2024 01:54:28 GMT
ENV ARM64_SHA256=45f46c99ae9561aac13b25f909df6ac1f971d4ce4aa594ff3711a1c95e8d9d9e
# Tue, 06 Feb 2024 01:54:28 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 06 Feb 2024 01:54:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 06 Feb 2024 01:54:43 GMT
WORKDIR /opt/emqx
# Tue, 06 Feb 2024 01:54:43 GMT
USER emqx
# Tue, 06 Feb 2024 01:54:43 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 06 Feb 2024 01:54:43 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 06 Feb 2024 01:54:43 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 06 Feb 2024 01:54:44 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 06 Feb 2024 01:54:44 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8901d41c85ca9ebab394246426c72c13c3dfc1435f591082316c22b7a03b3715`  
		Last Modified: Tue, 06 Feb 2024 01:55:12 GMT  
		Size: 89.8 MB (89833753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c30c0994c3f3db0039c666c744f93f85a59f3805a664ae7857a134576186216`  
		Last Modified: Tue, 06 Feb 2024 01:55:03 GMT  
		Size: 905.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8df89a3698b4a72941fa1ff3580da7c33e1dfd37652bc0ec20ec5323be4e07f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116785334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27fae1dc82850c4fd1546147133034ffcc62ec208e0a7f2cd00fc627a7c50303`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:42 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
# Wed, 31 Jan 2024 22:44:42 GMT
CMD ["bash"]
# Mon, 05 Feb 2024 19:39:34 GMT
ENV EMQX_VERSION=5.5.0
# Mon, 05 Feb 2024 19:39:34 GMT
ENV AMD64_SHA256=31af6514bcd30cab68272e1ff9553f652520cf82afed8894b3c4fe0fae55da88
# Mon, 05 Feb 2024 19:39:34 GMT
ENV ARM64_SHA256=45f46c99ae9561aac13b25f909df6ac1f971d4ce4aa594ff3711a1c95e8d9d9e
# Mon, 05 Feb 2024 19:39:34 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Mon, 05 Feb 2024 19:39:47 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Mon, 05 Feb 2024 19:39:48 GMT
WORKDIR /opt/emqx
# Mon, 05 Feb 2024 19:39:48 GMT
USER emqx
# Mon, 05 Feb 2024 19:39:48 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Mon, 05 Feb 2024 19:39:48 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Mon, 05 Feb 2024 19:39:48 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Mon, 05 Feb 2024 19:39:48 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Mon, 05 Feb 2024 19:39:48 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:731ff59e9ae9c27353a4caf2f7a4bc1e3c1eb2a148b49912d2638271bcdeeed6`  
		Last Modified: Mon, 05 Feb 2024 19:40:12 GMT  
		Size: 86.7 MB (86720094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb7a5e31767d758e0fbc4886da9ad4fbbfdadb2b3ff1567f6797086454167e4`  
		Last Modified: Mon, 05 Feb 2024 19:40:05 GMT  
		Size: 906.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
