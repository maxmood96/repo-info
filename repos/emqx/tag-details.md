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
-	[`emqx:5.4.0`](#emqx540)
-	[`emqx:latest`](#emqxlatest)

## `emqx:5`

```console
$ docker pull emqx@sha256:676f233b365830ef66742c0d383fd884567ac75e7c6bbff26ebf99546b40c637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:cfdbde0f24635d1e09fde2a53fa239aea4de4390b362321afa24e906f12498b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118704645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82e59504ccb5bcac252ff370e56db3ba7df90054fc89c24480e71b96eb253db`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:51:43 GMT
ENV EMQX_VERSION=5.4.0
# Thu, 11 Jan 2024 03:51:43 GMT
ENV AMD64_SHA256=5572dccf3704dbd910f145fe19882fa30fdd9132113d0a28110444d4d5685a3f
# Thu, 11 Jan 2024 03:51:43 GMT
ENV ARM64_SHA256=0dbe92966a93054a8dca89762c00b06a44659c7921177feb291a5ddd5340cefc
# Thu, 11 Jan 2024 03:51:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 11 Jan 2024 03:51:57 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:51:58 GMT
WORKDIR /opt/emqx
# Thu, 11 Jan 2024 03:51:58 GMT
USER emqx
# Thu, 11 Jan 2024 03:51:58 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 11 Jan 2024 03:51:58 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 11 Jan 2024 03:51:58 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 11 Jan 2024 03:51:58 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 03:51:58 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6bd74cf76dbd52eed71f206aff9834bd511961c81fdaba937cab6f2b5b11f1`  
		Last Modified: Thu, 11 Jan 2024 03:53:08 GMT  
		Size: 87.3 MB (87285789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a50976e01315da94817de273099e011758e4fcb3a6db08b1c1e557aca7f7a03a`  
		Last Modified: Thu, 11 Jan 2024 03:52:58 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:5ccd09ad8dd1320627283fc479a3b760add3a04d32da2cece1eea1718c541f71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108466312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e221710e68ca5dc18d8b139ca8c1f2fb9d9da2aa793cd9b35a0fad72c6f914b5`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Wed, 03 Jan 2024 19:39:37 GMT
ENV EMQX_VERSION=5.4.0
# Wed, 03 Jan 2024 19:39:37 GMT
ENV AMD64_SHA256=5572dccf3704dbd910f145fe19882fa30fdd9132113d0a28110444d4d5685a3f
# Wed, 03 Jan 2024 19:39:37 GMT
ENV ARM64_SHA256=0dbe92966a93054a8dca89762c00b06a44659c7921177feb291a5ddd5340cefc
# Wed, 03 Jan 2024 19:39:37 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 Jan 2024 19:39:50 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 03 Jan 2024 19:39:51 GMT
WORKDIR /opt/emqx
# Wed, 03 Jan 2024 19:39:51 GMT
USER emqx
# Wed, 03 Jan 2024 19:39:51 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 Jan 2024 19:39:51 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 03 Jan 2024 19:39:51 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 03 Jan 2024 19:39:51 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 Jan 2024 19:39:51 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000db8836b7a4dcf705932e61e11e1c8af7870412c338e39e234bce09ccb3a26`  
		Last Modified: Wed, 03 Jan 2024 19:40:10 GMT  
		Size: 78.4 MB (78401356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f84d1cbfd874e0a6e42d7872df4925361685c19d66d456d85f3b253e6281c6`  
		Last Modified: Wed, 03 Jan 2024 19:40:03 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.1`

```console
$ docker pull emqx@sha256:ae605c7fb8163c60ecc4f90e40e26648198076b90b3f5e24fb1a7f8586e4655b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.1` - linux; amd64

```console
$ docker pull emqx@sha256:6120a6264e7c3d7f018c577de4722e368d76c368404cb2e25a8d77bd90c1b40c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102393885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae194926bb49984a8925fe5d55e6e95a9ac18ac98a7fa665f959750b8f7eb99`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:50:54 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:50:55 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 11 Jan 2024 03:50:55 GMT
ENV EMQX_VERSION=5.1.6
# Thu, 11 Jan 2024 03:50:55 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Thu, 11 Jan 2024 03:50:55 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Thu, 11 Jan 2024 03:50:55 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 11 Jan 2024 03:51:01 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Thu, 11 Jan 2024 03:51:02 GMT
WORKDIR /opt/emqx
# Thu, 11 Jan 2024 03:51:02 GMT
USER emqx
# Thu, 11 Jan 2024 03:51:02 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 11 Jan 2024 03:51:02 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 11 Jan 2024 03:51:02 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 11 Jan 2024 03:51:02 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 03:51:02 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2789a35821cbfdcdde55e6bfc4ae6fecfcce9a60296c5d4e5e5e6e3393b284c4`  
		Last Modified: Thu, 11 Jan 2024 03:52:11 GMT  
		Size: 3.0 MB (2989673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fdcf9c6d35234067e1a6b4d5e745c2901892b1299996e6c63e6177c233d67c`  
		Last Modified: Thu, 11 Jan 2024 03:52:11 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa651b9d48573ffbc964469b078f2d0d084b2ab1671db9a200eab16db06f54b`  
		Last Modified: Thu, 11 Jan 2024 03:52:18 GMT  
		Size: 68.0 MB (67981252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63bf9ca33dfe7f04cfa7453f2304c04adc611d068918727d590c62c15b0dc35d`  
		Last Modified: Thu, 11 Jan 2024 03:52:11 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:820accc8095594a276fe926085eb401bf561bfe3342066e7a607b2290790c032
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92699659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf95ded1811a2c6acb9d51a6f1c63dde209b2156b71d38b2324179d098c32ce9`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 07:32:01 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:32:02 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 19 Dec 2023 07:32:11 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 19 Dec 2023 07:32:11 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 19 Dec 2023 07:32:11 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 19 Dec 2023 07:32:11 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 19 Dec 2023 07:32:18 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Tue, 19 Dec 2023 07:32:18 GMT
WORKDIR /opt/emqx
# Tue, 19 Dec 2023 07:32:18 GMT
USER emqx
# Tue, 19 Dec 2023 07:32:18 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 19 Dec 2023 07:32:18 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 19 Dec 2023 07:32:18 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 19 Dec 2023 07:32:18 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 07:32:18 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ad4fef290fd2d2ffd265ffa1a96ebf05acaab5740f182976858a9945ccc6b8`  
		Last Modified: Tue, 19 Dec 2023 07:33:04 GMT  
		Size: 3.0 MB (3005919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74fa4eb99d3b32a70e69c8e163febc253d6aacff81300978c1c97a0f1650eb4`  
		Last Modified: Tue, 19 Dec 2023 07:33:03 GMT  
		Size: 4.1 KB (4117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:697b32ab0cc5a20325f2fb6a5bdf4a5a880798781e23d7ea38b56061cc7d31a3`  
		Last Modified: Tue, 19 Dec 2023 07:33:22 GMT  
		Size: 59.6 MB (59624667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48465f006d8d1f5cbd66bc3f8ba1b11f89f184aecae1158a4085fbcb469a74bb`  
		Last Modified: Tue, 19 Dec 2023 07:33:17 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.1.6`

```console
$ docker pull emqx@sha256:ae605c7fb8163c60ecc4f90e40e26648198076b90b3f5e24fb1a7f8586e4655b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.1.6` - linux; amd64

```console
$ docker pull emqx@sha256:6120a6264e7c3d7f018c577de4722e368d76c368404cb2e25a8d77bd90c1b40c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102393885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae194926bb49984a8925fe5d55e6e95a9ac18ac98a7fa665f959750b8f7eb99`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:50:54 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:50:55 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 11 Jan 2024 03:50:55 GMT
ENV EMQX_VERSION=5.1.6
# Thu, 11 Jan 2024 03:50:55 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Thu, 11 Jan 2024 03:50:55 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Thu, 11 Jan 2024 03:50:55 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 11 Jan 2024 03:51:01 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Thu, 11 Jan 2024 03:51:02 GMT
WORKDIR /opt/emqx
# Thu, 11 Jan 2024 03:51:02 GMT
USER emqx
# Thu, 11 Jan 2024 03:51:02 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 11 Jan 2024 03:51:02 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 11 Jan 2024 03:51:02 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 11 Jan 2024 03:51:02 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 03:51:02 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2789a35821cbfdcdde55e6bfc4ae6fecfcce9a60296c5d4e5e5e6e3393b284c4`  
		Last Modified: Thu, 11 Jan 2024 03:52:11 GMT  
		Size: 3.0 MB (2989673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fdcf9c6d35234067e1a6b4d5e745c2901892b1299996e6c63e6177c233d67c`  
		Last Modified: Thu, 11 Jan 2024 03:52:11 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fa651b9d48573ffbc964469b078f2d0d084b2ab1671db9a200eab16db06f54b`  
		Last Modified: Thu, 11 Jan 2024 03:52:18 GMT  
		Size: 68.0 MB (67981252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63bf9ca33dfe7f04cfa7453f2304c04adc611d068918727d590c62c15b0dc35d`  
		Last Modified: Thu, 11 Jan 2024 03:52:11 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.1.6` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:820accc8095594a276fe926085eb401bf561bfe3342066e7a607b2290790c032
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92699659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf95ded1811a2c6acb9d51a6f1c63dde209b2156b71d38b2324179d098c32ce9`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 07:32:01 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:32:02 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 19 Dec 2023 07:32:11 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 19 Dec 2023 07:32:11 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 19 Dec 2023 07:32:11 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 19 Dec 2023 07:32:11 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 19 Dec 2023 07:32:18 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Tue, 19 Dec 2023 07:32:18 GMT
WORKDIR /opt/emqx
# Tue, 19 Dec 2023 07:32:18 GMT
USER emqx
# Tue, 19 Dec 2023 07:32:18 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 19 Dec 2023 07:32:18 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 19 Dec 2023 07:32:18 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 19 Dec 2023 07:32:18 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 07:32:18 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ad4fef290fd2d2ffd265ffa1a96ebf05acaab5740f182976858a9945ccc6b8`  
		Last Modified: Tue, 19 Dec 2023 07:33:04 GMT  
		Size: 3.0 MB (3005919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74fa4eb99d3b32a70e69c8e163febc253d6aacff81300978c1c97a0f1650eb4`  
		Last Modified: Tue, 19 Dec 2023 07:33:03 GMT  
		Size: 4.1 KB (4117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:697b32ab0cc5a20325f2fb6a5bdf4a5a880798781e23d7ea38b56061cc7d31a3`  
		Last Modified: Tue, 19 Dec 2023 07:33:22 GMT  
		Size: 59.6 MB (59624667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48465f006d8d1f5cbd66bc3f8ba1b11f89f184aecae1158a4085fbcb469a74bb`  
		Last Modified: Tue, 19 Dec 2023 07:33:17 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.2`

```console
$ docker pull emqx@sha256:a94a3ddf7d177c6b1da2a4ae8fa9973c47249798a53ad837a28940e99aa5b445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.2` - linux; amd64

```console
$ docker pull emqx@sha256:a80f9b946b4d5872af8e1a6c2ded8bd4ea401efd713c3ef7306521ab08f45622
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101165546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f226ebda7b16ffa0f5cbe846510d5dc432594a41114ac939cffa7737f67425e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:51:10 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:51:11 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 11 Jan 2024 03:51:11 GMT
ENV EMQX_VERSION=5.2.1
# Thu, 11 Jan 2024 03:51:11 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Thu, 11 Jan 2024 03:51:11 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Thu, 11 Jan 2024 03:51:11 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 11 Jan 2024 03:51:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Thu, 11 Jan 2024 03:51:21 GMT
WORKDIR /opt/emqx
# Thu, 11 Jan 2024 03:51:21 GMT
USER emqx
# Thu, 11 Jan 2024 03:51:22 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 11 Jan 2024 03:51:22 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 11 Jan 2024 03:51:22 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 11 Jan 2024 03:51:22 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 03:51:22 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d347b18f88b86d6bce30c056990d99a21b11497e35e9c72181a2126b4c0d2ba6`  
		Last Modified: Thu, 11 Jan 2024 03:52:27 GMT  
		Size: 1.6 MB (1631587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5554736f4aa28d42467db16368695cff6c06c4c03e21eca2f9c316f84f85998`  
		Last Modified: Thu, 11 Jan 2024 03:52:27 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69afda8564ce6a131b2e7f1cef87c82a517e9f07345b4f8792453822d55cf4ba`  
		Last Modified: Thu, 11 Jan 2024 03:52:34 GMT  
		Size: 68.1 MB (68110991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4654a1f980cbf958c7015915b406793140fbcd0cd63666d2c04e5163fb546af`  
		Last Modified: Thu, 11 Jan 2024 03:52:27 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:780502a6185121b439de8af0b17ef7eacdc9b0e7592c3caa0fc4c9707da8495b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91466792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06ad2bad3bcb7c1f56d51fb4c5f20742b0741f9b937c1ba03286cb093e14d39`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 07:32:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:32:24 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 19 Dec 2023 07:32:25 GMT
ENV EMQX_VERSION=5.2.1
# Tue, 19 Dec 2023 07:32:25 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Tue, 19 Dec 2023 07:32:25 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Tue, 19 Dec 2023 07:32:25 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 19 Dec 2023 07:32:34 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Tue, 19 Dec 2023 07:32:34 GMT
WORKDIR /opt/emqx
# Tue, 19 Dec 2023 07:32:34 GMT
USER emqx
# Tue, 19 Dec 2023 07:32:35 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 19 Dec 2023 07:32:35 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 19 Dec 2023 07:32:35 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 19 Dec 2023 07:32:35 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 07:32:35 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b7055e37e3bad5de6bd747fc0c942693c86989fd7d3c820c864e901ebe9a5d`  
		Last Modified: Tue, 19 Dec 2023 07:33:30 GMT  
		Size: 1.6 MB (1645892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6bce98705c9d5d07b0d00c2217db5b626ddb30f240abe020cec7993ba981a0`  
		Last Modified: Tue, 19 Dec 2023 07:33:30 GMT  
		Size: 4.1 KB (4116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54511baaf9f18f1feb1f4fc00978bb508e17b88d8685ae5e80386de0357ed62`  
		Last Modified: Tue, 19 Dec 2023 07:33:35 GMT  
		Size: 59.8 MB (59751829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6e3deb5e84e1a7d4f555778a41aaaf9ab48a123a10e69147148853fcba1a6b`  
		Last Modified: Tue, 19 Dec 2023 07:33:30 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.2.1`

```console
$ docker pull emqx@sha256:a94a3ddf7d177c6b1da2a4ae8fa9973c47249798a53ad837a28940e99aa5b445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.2.1` - linux; amd64

```console
$ docker pull emqx@sha256:a80f9b946b4d5872af8e1a6c2ded8bd4ea401efd713c3ef7306521ab08f45622
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101165546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f226ebda7b16ffa0f5cbe846510d5dc432594a41114ac939cffa7737f67425e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:51:10 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:51:11 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 11 Jan 2024 03:51:11 GMT
ENV EMQX_VERSION=5.2.1
# Thu, 11 Jan 2024 03:51:11 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Thu, 11 Jan 2024 03:51:11 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Thu, 11 Jan 2024 03:51:11 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 11 Jan 2024 03:51:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Thu, 11 Jan 2024 03:51:21 GMT
WORKDIR /opt/emqx
# Thu, 11 Jan 2024 03:51:21 GMT
USER emqx
# Thu, 11 Jan 2024 03:51:22 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 11 Jan 2024 03:51:22 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 11 Jan 2024 03:51:22 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 11 Jan 2024 03:51:22 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 03:51:22 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d347b18f88b86d6bce30c056990d99a21b11497e35e9c72181a2126b4c0d2ba6`  
		Last Modified: Thu, 11 Jan 2024 03:52:27 GMT  
		Size: 1.6 MB (1631587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5554736f4aa28d42467db16368695cff6c06c4c03e21eca2f9c316f84f85998`  
		Last Modified: Thu, 11 Jan 2024 03:52:27 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69afda8564ce6a131b2e7f1cef87c82a517e9f07345b4f8792453822d55cf4ba`  
		Last Modified: Thu, 11 Jan 2024 03:52:34 GMT  
		Size: 68.1 MB (68110991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4654a1f980cbf958c7015915b406793140fbcd0cd63666d2c04e5163fb546af`  
		Last Modified: Thu, 11 Jan 2024 03:52:27 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.2.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:780502a6185121b439de8af0b17ef7eacdc9b0e7592c3caa0fc4c9707da8495b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91466792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06ad2bad3bcb7c1f56d51fb4c5f20742b0741f9b937c1ba03286cb093e14d39`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 07:32:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:32:24 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 19 Dec 2023 07:32:25 GMT
ENV EMQX_VERSION=5.2.1
# Tue, 19 Dec 2023 07:32:25 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Tue, 19 Dec 2023 07:32:25 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Tue, 19 Dec 2023 07:32:25 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 19 Dec 2023 07:32:34 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Tue, 19 Dec 2023 07:32:34 GMT
WORKDIR /opt/emqx
# Tue, 19 Dec 2023 07:32:34 GMT
USER emqx
# Tue, 19 Dec 2023 07:32:35 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 19 Dec 2023 07:32:35 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 19 Dec 2023 07:32:35 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 19 Dec 2023 07:32:35 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 07:32:35 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b7055e37e3bad5de6bd747fc0c942693c86989fd7d3c820c864e901ebe9a5d`  
		Last Modified: Tue, 19 Dec 2023 07:33:30 GMT  
		Size: 1.6 MB (1645892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6bce98705c9d5d07b0d00c2217db5b626ddb30f240abe020cec7993ba981a0`  
		Last Modified: Tue, 19 Dec 2023 07:33:30 GMT  
		Size: 4.1 KB (4116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54511baaf9f18f1feb1f4fc00978bb508e17b88d8685ae5e80386de0357ed62`  
		Last Modified: Tue, 19 Dec 2023 07:33:35 GMT  
		Size: 59.8 MB (59751829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6e3deb5e84e1a7d4f555778a41aaaf9ab48a123a10e69147148853fcba1a6b`  
		Last Modified: Tue, 19 Dec 2023 07:33:30 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.3`

```console
$ docker pull emqx@sha256:7d0c7e8908f8625412ae62ba42618a8bbe5214932752f73e57b749ef04af4fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.3` - linux; amd64

```console
$ docker pull emqx@sha256:1814b17af1ff30e1b6bc2b0ca8453b34824c081bf6c0d92a22adf7ff75c164bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101780844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555a6a7cd8e6202acf03b8a996bf03afbb2b775f23cd56f69e37106e83b221d8`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:51:26 GMT
ENV EMQX_VERSION=5.3.2
# Thu, 11 Jan 2024 03:51:26 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Thu, 11 Jan 2024 03:51:26 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Thu, 11 Jan 2024 03:51:26 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 11 Jan 2024 03:51:39 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:51:39 GMT
WORKDIR /opt/emqx
# Thu, 11 Jan 2024 03:51:39 GMT
USER emqx
# Thu, 11 Jan 2024 03:51:40 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 11 Jan 2024 03:51:40 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 11 Jan 2024 03:51:40 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 11 Jan 2024 03:51:40 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 03:51:40 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca43a596413bd7e9036028c7d428e7886d258c2a9e3e87d93d03e14efe7fb40`  
		Last Modified: Thu, 11 Jan 2024 03:52:50 GMT  
		Size: 70.4 MB (70361986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bf15ef41e58bca694848d0f9b1363ec4591dcd615df89485da0cda75fe4f95`  
		Last Modified: Thu, 11 Jan 2024 03:52:43 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.3` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:6176aaaee7b4b6e6f3e7211550a35d5325ce1ce46b75abee65b27eba78ba0cea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92080755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea886e3a913dcd4a0ed731caae05e52a4d36694070bcb4435df7338d0ebd8904`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 07:32:36 GMT
ENV EMQX_VERSION=5.3.2
# Tue, 19 Dec 2023 07:32:37 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Tue, 19 Dec 2023 07:32:37 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Tue, 19 Dec 2023 07:32:37 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 19 Dec 2023 07:32:48 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:32:48 GMT
WORKDIR /opt/emqx
# Tue, 19 Dec 2023 07:32:48 GMT
USER emqx
# Tue, 19 Dec 2023 07:32:48 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 19 Dec 2023 07:32:48 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 19 Dec 2023 07:32:48 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 19 Dec 2023 07:32:49 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 07:32:49 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ff49abb8e64c1ed2e11b76890bc5263236543367a5c644aeb798711592690c`  
		Last Modified: Tue, 19 Dec 2023 07:33:50 GMT  
		Size: 62.0 MB (62015801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a9b506f5feb36dea14e522c2ee7ffa5c379b6f1a670711f86856bad5043709`  
		Last Modified: Tue, 19 Dec 2023 07:33:43 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.3.2`

```console
$ docker pull emqx@sha256:7d0c7e8908f8625412ae62ba42618a8bbe5214932752f73e57b749ef04af4fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.3.2` - linux; amd64

```console
$ docker pull emqx@sha256:1814b17af1ff30e1b6bc2b0ca8453b34824c081bf6c0d92a22adf7ff75c164bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101780844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555a6a7cd8e6202acf03b8a996bf03afbb2b775f23cd56f69e37106e83b221d8`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:51:26 GMT
ENV EMQX_VERSION=5.3.2
# Thu, 11 Jan 2024 03:51:26 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Thu, 11 Jan 2024 03:51:26 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Thu, 11 Jan 2024 03:51:26 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 11 Jan 2024 03:51:39 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:51:39 GMT
WORKDIR /opt/emqx
# Thu, 11 Jan 2024 03:51:39 GMT
USER emqx
# Thu, 11 Jan 2024 03:51:40 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 11 Jan 2024 03:51:40 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 11 Jan 2024 03:51:40 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 11 Jan 2024 03:51:40 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 03:51:40 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca43a596413bd7e9036028c7d428e7886d258c2a9e3e87d93d03e14efe7fb40`  
		Last Modified: Thu, 11 Jan 2024 03:52:50 GMT  
		Size: 70.4 MB (70361986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8bf15ef41e58bca694848d0f9b1363ec4591dcd615df89485da0cda75fe4f95`  
		Last Modified: Thu, 11 Jan 2024 03:52:43 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.3.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:6176aaaee7b4b6e6f3e7211550a35d5325ce1ce46b75abee65b27eba78ba0cea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92080755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea886e3a913dcd4a0ed731caae05e52a4d36694070bcb4435df7338d0ebd8904`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 07:32:36 GMT
ENV EMQX_VERSION=5.3.2
# Tue, 19 Dec 2023 07:32:37 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Tue, 19 Dec 2023 07:32:37 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Tue, 19 Dec 2023 07:32:37 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 19 Dec 2023 07:32:48 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 07:32:48 GMT
WORKDIR /opt/emqx
# Tue, 19 Dec 2023 07:32:48 GMT
USER emqx
# Tue, 19 Dec 2023 07:32:48 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 19 Dec 2023 07:32:48 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 19 Dec 2023 07:32:48 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 19 Dec 2023 07:32:49 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 07:32:49 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ff49abb8e64c1ed2e11b76890bc5263236543367a5c644aeb798711592690c`  
		Last Modified: Tue, 19 Dec 2023 07:33:50 GMT  
		Size: 62.0 MB (62015801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a9b506f5feb36dea14e522c2ee7ffa5c379b6f1a670711f86856bad5043709`  
		Last Modified: Tue, 19 Dec 2023 07:33:43 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.4`

```console
$ docker pull emqx@sha256:676f233b365830ef66742c0d383fd884567ac75e7c6bbff26ebf99546b40c637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.4` - linux; amd64

```console
$ docker pull emqx@sha256:cfdbde0f24635d1e09fde2a53fa239aea4de4390b362321afa24e906f12498b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118704645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82e59504ccb5bcac252ff370e56db3ba7df90054fc89c24480e71b96eb253db`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:51:43 GMT
ENV EMQX_VERSION=5.4.0
# Thu, 11 Jan 2024 03:51:43 GMT
ENV AMD64_SHA256=5572dccf3704dbd910f145fe19882fa30fdd9132113d0a28110444d4d5685a3f
# Thu, 11 Jan 2024 03:51:43 GMT
ENV ARM64_SHA256=0dbe92966a93054a8dca89762c00b06a44659c7921177feb291a5ddd5340cefc
# Thu, 11 Jan 2024 03:51:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 11 Jan 2024 03:51:57 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:51:58 GMT
WORKDIR /opt/emqx
# Thu, 11 Jan 2024 03:51:58 GMT
USER emqx
# Thu, 11 Jan 2024 03:51:58 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 11 Jan 2024 03:51:58 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 11 Jan 2024 03:51:58 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 11 Jan 2024 03:51:58 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 03:51:58 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6bd74cf76dbd52eed71f206aff9834bd511961c81fdaba937cab6f2b5b11f1`  
		Last Modified: Thu, 11 Jan 2024 03:53:08 GMT  
		Size: 87.3 MB (87285789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a50976e01315da94817de273099e011758e4fcb3a6db08b1c1e557aca7f7a03a`  
		Last Modified: Thu, 11 Jan 2024 03:52:58 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:5ccd09ad8dd1320627283fc479a3b760add3a04d32da2cece1eea1718c541f71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108466312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e221710e68ca5dc18d8b139ca8c1f2fb9d9da2aa793cd9b35a0fad72c6f914b5`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Wed, 03 Jan 2024 19:39:37 GMT
ENV EMQX_VERSION=5.4.0
# Wed, 03 Jan 2024 19:39:37 GMT
ENV AMD64_SHA256=5572dccf3704dbd910f145fe19882fa30fdd9132113d0a28110444d4d5685a3f
# Wed, 03 Jan 2024 19:39:37 GMT
ENV ARM64_SHA256=0dbe92966a93054a8dca89762c00b06a44659c7921177feb291a5ddd5340cefc
# Wed, 03 Jan 2024 19:39:37 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 Jan 2024 19:39:50 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 03 Jan 2024 19:39:51 GMT
WORKDIR /opt/emqx
# Wed, 03 Jan 2024 19:39:51 GMT
USER emqx
# Wed, 03 Jan 2024 19:39:51 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 Jan 2024 19:39:51 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 03 Jan 2024 19:39:51 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 03 Jan 2024 19:39:51 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 Jan 2024 19:39:51 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000db8836b7a4dcf705932e61e11e1c8af7870412c338e39e234bce09ccb3a26`  
		Last Modified: Wed, 03 Jan 2024 19:40:10 GMT  
		Size: 78.4 MB (78401356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f84d1cbfd874e0a6e42d7872df4925361685c19d66d456d85f3b253e6281c6`  
		Last Modified: Wed, 03 Jan 2024 19:40:03 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.4.0`

```console
$ docker pull emqx@sha256:676f233b365830ef66742c0d383fd884567ac75e7c6bbff26ebf99546b40c637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.4.0` - linux; amd64

```console
$ docker pull emqx@sha256:cfdbde0f24635d1e09fde2a53fa239aea4de4390b362321afa24e906f12498b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118704645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82e59504ccb5bcac252ff370e56db3ba7df90054fc89c24480e71b96eb253db`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:51:43 GMT
ENV EMQX_VERSION=5.4.0
# Thu, 11 Jan 2024 03:51:43 GMT
ENV AMD64_SHA256=5572dccf3704dbd910f145fe19882fa30fdd9132113d0a28110444d4d5685a3f
# Thu, 11 Jan 2024 03:51:43 GMT
ENV ARM64_SHA256=0dbe92966a93054a8dca89762c00b06a44659c7921177feb291a5ddd5340cefc
# Thu, 11 Jan 2024 03:51:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 11 Jan 2024 03:51:57 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:51:58 GMT
WORKDIR /opt/emqx
# Thu, 11 Jan 2024 03:51:58 GMT
USER emqx
# Thu, 11 Jan 2024 03:51:58 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 11 Jan 2024 03:51:58 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 11 Jan 2024 03:51:58 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 11 Jan 2024 03:51:58 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 03:51:58 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6bd74cf76dbd52eed71f206aff9834bd511961c81fdaba937cab6f2b5b11f1`  
		Last Modified: Thu, 11 Jan 2024 03:53:08 GMT  
		Size: 87.3 MB (87285789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a50976e01315da94817de273099e011758e4fcb3a6db08b1c1e557aca7f7a03a`  
		Last Modified: Thu, 11 Jan 2024 03:52:58 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.4.0` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:5ccd09ad8dd1320627283fc479a3b760add3a04d32da2cece1eea1718c541f71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108466312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e221710e68ca5dc18d8b139ca8c1f2fb9d9da2aa793cd9b35a0fad72c6f914b5`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Wed, 03 Jan 2024 19:39:37 GMT
ENV EMQX_VERSION=5.4.0
# Wed, 03 Jan 2024 19:39:37 GMT
ENV AMD64_SHA256=5572dccf3704dbd910f145fe19882fa30fdd9132113d0a28110444d4d5685a3f
# Wed, 03 Jan 2024 19:39:37 GMT
ENV ARM64_SHA256=0dbe92966a93054a8dca89762c00b06a44659c7921177feb291a5ddd5340cefc
# Wed, 03 Jan 2024 19:39:37 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 Jan 2024 19:39:50 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 03 Jan 2024 19:39:51 GMT
WORKDIR /opt/emqx
# Wed, 03 Jan 2024 19:39:51 GMT
USER emqx
# Wed, 03 Jan 2024 19:39:51 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 Jan 2024 19:39:51 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 03 Jan 2024 19:39:51 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 03 Jan 2024 19:39:51 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 Jan 2024 19:39:51 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000db8836b7a4dcf705932e61e11e1c8af7870412c338e39e234bce09ccb3a26`  
		Last Modified: Wed, 03 Jan 2024 19:40:10 GMT  
		Size: 78.4 MB (78401356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f84d1cbfd874e0a6e42d7872df4925361685c19d66d456d85f3b253e6281c6`  
		Last Modified: Wed, 03 Jan 2024 19:40:03 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:latest`

```console
$ docker pull emqx@sha256:676f233b365830ef66742c0d383fd884567ac75e7c6bbff26ebf99546b40c637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:cfdbde0f24635d1e09fde2a53fa239aea4de4390b362321afa24e906f12498b6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118704645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82e59504ccb5bcac252ff370e56db3ba7df90054fc89c24480e71b96eb253db`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:51:43 GMT
ENV EMQX_VERSION=5.4.0
# Thu, 11 Jan 2024 03:51:43 GMT
ENV AMD64_SHA256=5572dccf3704dbd910f145fe19882fa30fdd9132113d0a28110444d4d5685a3f
# Thu, 11 Jan 2024 03:51:43 GMT
ENV ARM64_SHA256=0dbe92966a93054a8dca89762c00b06a44659c7921177feb291a5ddd5340cefc
# Thu, 11 Jan 2024 03:51:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 11 Jan 2024 03:51:57 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 03:51:58 GMT
WORKDIR /opt/emqx
# Thu, 11 Jan 2024 03:51:58 GMT
USER emqx
# Thu, 11 Jan 2024 03:51:58 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 11 Jan 2024 03:51:58 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 11 Jan 2024 03:51:58 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 11 Jan 2024 03:51:58 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 03:51:58 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6bd74cf76dbd52eed71f206aff9834bd511961c81fdaba937cab6f2b5b11f1`  
		Last Modified: Thu, 11 Jan 2024 03:53:08 GMT  
		Size: 87.3 MB (87285789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a50976e01315da94817de273099e011758e4fcb3a6db08b1c1e557aca7f7a03a`  
		Last Modified: Thu, 11 Jan 2024 03:52:58 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:5ccd09ad8dd1320627283fc479a3b760add3a04d32da2cece1eea1718c541f71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108466312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e221710e68ca5dc18d8b139ca8c1f2fb9d9da2aa793cd9b35a0fad72c6f914b5`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Wed, 03 Jan 2024 19:39:37 GMT
ENV EMQX_VERSION=5.4.0
# Wed, 03 Jan 2024 19:39:37 GMT
ENV AMD64_SHA256=5572dccf3704dbd910f145fe19882fa30fdd9132113d0a28110444d4d5685a3f
# Wed, 03 Jan 2024 19:39:37 GMT
ENV ARM64_SHA256=0dbe92966a93054a8dca89762c00b06a44659c7921177feb291a5ddd5340cefc
# Wed, 03 Jan 2024 19:39:37 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 Jan 2024 19:39:50 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 03 Jan 2024 19:39:51 GMT
WORKDIR /opt/emqx
# Wed, 03 Jan 2024 19:39:51 GMT
USER emqx
# Wed, 03 Jan 2024 19:39:51 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 Jan 2024 19:39:51 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Wed, 03 Jan 2024 19:39:51 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 03 Jan 2024 19:39:51 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 Jan 2024 19:39:51 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:000db8836b7a4dcf705932e61e11e1c8af7870412c338e39e234bce09ccb3a26`  
		Last Modified: Wed, 03 Jan 2024 19:40:10 GMT  
		Size: 78.4 MB (78401356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60f84d1cbfd874e0a6e42d7872df4925361685c19d66d456d85f3b253e6281c6`  
		Last Modified: Wed, 03 Jan 2024 19:40:03 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
