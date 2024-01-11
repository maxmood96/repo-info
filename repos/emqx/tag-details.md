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
$ docker pull emqx@sha256:0e49d60b7272bb5bf8b26b545d3b360775b616f6be658d88a1b36826cc87e9ff
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
$ docker pull emqx@sha256:6a0096f9b9b3f102898935709b000e71417a2eca8023556f85864532150688b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108465759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f33409a87fe69d87a4d6529af86540b8a7d74d839f565e17422742f5e22d2d1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:07:39 GMT
ENV EMQX_VERSION=5.4.0
# Thu, 11 Jan 2024 06:07:39 GMT
ENV AMD64_SHA256=5572dccf3704dbd910f145fe19882fa30fdd9132113d0a28110444d4d5685a3f
# Thu, 11 Jan 2024 06:07:39 GMT
ENV ARM64_SHA256=0dbe92966a93054a8dca89762c00b06a44659c7921177feb291a5ddd5340cefc
# Thu, 11 Jan 2024 06:07:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 11 Jan 2024 06:07:50 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:07:50 GMT
WORKDIR /opt/emqx
# Thu, 11 Jan 2024 06:07:50 GMT
USER emqx
# Thu, 11 Jan 2024 06:07:51 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 11 Jan 2024 06:07:51 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 11 Jan 2024 06:07:51 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 11 Jan 2024 06:07:51 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:07:51 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3d26b33db37cf44cbbf1baebbc7209ca524b0725e91f53a022e83bea45e3c3`  
		Last Modified: Thu, 11 Jan 2024 06:08:53 GMT  
		Size: 78.4 MB (78400848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51165c3bea9a3baf7f28b5f94dff104c70881233ffd56055d8c6dcc9ac249835`  
		Last Modified: Thu, 11 Jan 2024 06:08:46 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.1`

```console
$ docker pull emqx@sha256:26c1a834e9990951896453658bd51dd4069fb229c587e54a9752e959327ff793
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
$ docker pull emqx@sha256:ac3a1aa9762d5f930c5c6f4fb4b8e56d7764c658b1a3584549465cc45aa108fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92699823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c29e13c034ef058f5ae6356e7dfc9dc26048377933539963b1c25ca55fc6cad0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:07:00 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:07:00 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 11 Jan 2024 06:07:00 GMT
ENV EMQX_VERSION=5.1.6
# Thu, 11 Jan 2024 06:07:00 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Thu, 11 Jan 2024 06:07:00 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Thu, 11 Jan 2024 06:07:00 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 11 Jan 2024 06:07:06 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Thu, 11 Jan 2024 06:07:07 GMT
WORKDIR /opt/emqx
# Thu, 11 Jan 2024 06:07:07 GMT
USER emqx
# Thu, 11 Jan 2024 06:07:07 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 11 Jan 2024 06:07:07 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 11 Jan 2024 06:07:07 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 11 Jan 2024 06:07:07 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:07:07 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243be10585e2ffaa98b633fef823f1da642fc16beffa1dadf83ce06b15143081`  
		Last Modified: Thu, 11 Jan 2024 06:08:07 GMT  
		Size: 3.0 MB (3006107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607aafca45006f2d26b75e65adae8473b59bb5e2e177804a499354122e7e6f0b`  
		Last Modified: Thu, 11 Jan 2024 06:08:07 GMT  
		Size: 4.1 KB (4110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f165a638108846701a32e657a075057ad05dfd25ddfa855d9f1f8083cc0d3fd`  
		Last Modified: Thu, 11 Jan 2024 06:08:12 GMT  
		Size: 59.6 MB (59624694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca6405ad586ed35ff961a196acd97f88d852393af07b06287ae03e7a5a02706`  
		Last Modified: Thu, 11 Jan 2024 06:08:08 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.1.6`

```console
$ docker pull emqx@sha256:26c1a834e9990951896453658bd51dd4069fb229c587e54a9752e959327ff793
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
$ docker pull emqx@sha256:ac3a1aa9762d5f930c5c6f4fb4b8e56d7764c658b1a3584549465cc45aa108fd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92699823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c29e13c034ef058f5ae6356e7dfc9dc26048377933539963b1c25ca55fc6cad0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:07:00 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:07:00 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 11 Jan 2024 06:07:00 GMT
ENV EMQX_VERSION=5.1.6
# Thu, 11 Jan 2024 06:07:00 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Thu, 11 Jan 2024 06:07:00 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Thu, 11 Jan 2024 06:07:00 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 11 Jan 2024 06:07:06 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Thu, 11 Jan 2024 06:07:07 GMT
WORKDIR /opt/emqx
# Thu, 11 Jan 2024 06:07:07 GMT
USER emqx
# Thu, 11 Jan 2024 06:07:07 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 11 Jan 2024 06:07:07 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 11 Jan 2024 06:07:07 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 11 Jan 2024 06:07:07 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:07:07 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243be10585e2ffaa98b633fef823f1da642fc16beffa1dadf83ce06b15143081`  
		Last Modified: Thu, 11 Jan 2024 06:08:07 GMT  
		Size: 3.0 MB (3006107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607aafca45006f2d26b75e65adae8473b59bb5e2e177804a499354122e7e6f0b`  
		Last Modified: Thu, 11 Jan 2024 06:08:07 GMT  
		Size: 4.1 KB (4110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f165a638108846701a32e657a075057ad05dfd25ddfa855d9f1f8083cc0d3fd`  
		Last Modified: Thu, 11 Jan 2024 06:08:12 GMT  
		Size: 59.6 MB (59624694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca6405ad586ed35ff961a196acd97f88d852393af07b06287ae03e7a5a02706`  
		Last Modified: Thu, 11 Jan 2024 06:08:08 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.2`

```console
$ docker pull emqx@sha256:e0be0b0e3e68f7aa6bb03843875ee161f27f0144b8f88e7ecbecf2ba7bf1d6fc
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
$ docker pull emqx@sha256:bb66beddb2c601e6d922b5dc4f5273e83323b2c36bb8df4a2bc6b06012cb1f49
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91466655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4d6f5a396d301b07cd76e3ba6c365f57ff9ba536b7746e055f177e9085d601`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:07:13 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:07:13 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 11 Jan 2024 06:07:13 GMT
ENV EMQX_VERSION=5.2.1
# Thu, 11 Jan 2024 06:07:13 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Thu, 11 Jan 2024 06:07:13 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Thu, 11 Jan 2024 06:07:13 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 11 Jan 2024 06:07:22 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Thu, 11 Jan 2024 06:07:22 GMT
WORKDIR /opt/emqx
# Thu, 11 Jan 2024 06:07:22 GMT
USER emqx
# Thu, 11 Jan 2024 06:07:22 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 11 Jan 2024 06:07:22 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 11 Jan 2024 06:07:22 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 11 Jan 2024 06:07:22 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:07:22 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bece5197b9ec66fc444d87105bda035bdd67a5ade7c716285febb714e2a2169`  
		Last Modified: Thu, 11 Jan 2024 06:08:20 GMT  
		Size: 1.6 MB (1645840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935cf5d594e7ffd400c27a3bb73a6746c5f1ad11c7d982ce1b09b1ee94efcf50`  
		Last Modified: Thu, 11 Jan 2024 06:08:20 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07a2862aeff7c0c3eeee50766f4c1a3c3929b8d0330076e9c92b48232d459be`  
		Last Modified: Thu, 11 Jan 2024 06:08:25 GMT  
		Size: 59.8 MB (59751792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c8ee01e81d441bed1c9063342221a15af640a5c244fae064a16a951a5815f8a`  
		Last Modified: Thu, 11 Jan 2024 06:08:20 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.2.1`

```console
$ docker pull emqx@sha256:e0be0b0e3e68f7aa6bb03843875ee161f27f0144b8f88e7ecbecf2ba7bf1d6fc
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
$ docker pull emqx@sha256:bb66beddb2c601e6d922b5dc4f5273e83323b2c36bb8df4a2bc6b06012cb1f49
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91466655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4d6f5a396d301b07cd76e3ba6c365f57ff9ba536b7746e055f177e9085d601`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:07:13 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:07:13 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 11 Jan 2024 06:07:13 GMT
ENV EMQX_VERSION=5.2.1
# Thu, 11 Jan 2024 06:07:13 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Thu, 11 Jan 2024 06:07:13 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Thu, 11 Jan 2024 06:07:13 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 11 Jan 2024 06:07:22 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Thu, 11 Jan 2024 06:07:22 GMT
WORKDIR /opt/emqx
# Thu, 11 Jan 2024 06:07:22 GMT
USER emqx
# Thu, 11 Jan 2024 06:07:22 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 11 Jan 2024 06:07:22 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 11 Jan 2024 06:07:22 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 11 Jan 2024 06:07:22 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:07:22 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bece5197b9ec66fc444d87105bda035bdd67a5ade7c716285febb714e2a2169`  
		Last Modified: Thu, 11 Jan 2024 06:08:20 GMT  
		Size: 1.6 MB (1645840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935cf5d594e7ffd400c27a3bb73a6746c5f1ad11c7d982ce1b09b1ee94efcf50`  
		Last Modified: Thu, 11 Jan 2024 06:08:20 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07a2862aeff7c0c3eeee50766f4c1a3c3929b8d0330076e9c92b48232d459be`  
		Last Modified: Thu, 11 Jan 2024 06:08:25 GMT  
		Size: 59.8 MB (59751792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c8ee01e81d441bed1c9063342221a15af640a5c244fae064a16a951a5815f8a`  
		Last Modified: Thu, 11 Jan 2024 06:08:20 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.3`

```console
$ docker pull emqx@sha256:931bc1894c38043108e11f8cee7974a73ef8e5cfe1fc60da908fa8f40e63020b
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
$ docker pull emqx@sha256:b17072651f372b19203096ba9800a02d84cf203ced29c6993d97233dde89149d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92080641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b0ba45aeceec60b972701afa530a8b97714d406a2568ad6521c7b8bf3fb546`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:07:25 GMT
ENV EMQX_VERSION=5.3.2
# Thu, 11 Jan 2024 06:07:25 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Thu, 11 Jan 2024 06:07:25 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Thu, 11 Jan 2024 06:07:25 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 11 Jan 2024 06:07:36 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:07:36 GMT
WORKDIR /opt/emqx
# Thu, 11 Jan 2024 06:07:36 GMT
USER emqx
# Thu, 11 Jan 2024 06:07:36 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 11 Jan 2024 06:07:36 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 11 Jan 2024 06:07:36 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 11 Jan 2024 06:07:36 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:07:36 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7133d2d7fc2a0ad267f6a630e6881a28a78dabab29c30f41c69c35ea303be125`  
		Last Modified: Thu, 11 Jan 2024 06:08:38 GMT  
		Size: 62.0 MB (62015730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74fad41365af361b9908fbeeba52d1ba9daf0a28832653823690c198e9b289b5`  
		Last Modified: Thu, 11 Jan 2024 06:08:33 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.3.2`

```console
$ docker pull emqx@sha256:931bc1894c38043108e11f8cee7974a73ef8e5cfe1fc60da908fa8f40e63020b
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
$ docker pull emqx@sha256:b17072651f372b19203096ba9800a02d84cf203ced29c6993d97233dde89149d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92080641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b0ba45aeceec60b972701afa530a8b97714d406a2568ad6521c7b8bf3fb546`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:07:25 GMT
ENV EMQX_VERSION=5.3.2
# Thu, 11 Jan 2024 06:07:25 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Thu, 11 Jan 2024 06:07:25 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Thu, 11 Jan 2024 06:07:25 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 11 Jan 2024 06:07:36 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:07:36 GMT
WORKDIR /opt/emqx
# Thu, 11 Jan 2024 06:07:36 GMT
USER emqx
# Thu, 11 Jan 2024 06:07:36 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 11 Jan 2024 06:07:36 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 11 Jan 2024 06:07:36 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 11 Jan 2024 06:07:36 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:07:36 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7133d2d7fc2a0ad267f6a630e6881a28a78dabab29c30f41c69c35ea303be125`  
		Last Modified: Thu, 11 Jan 2024 06:08:38 GMT  
		Size: 62.0 MB (62015730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74fad41365af361b9908fbeeba52d1ba9daf0a28832653823690c198e9b289b5`  
		Last Modified: Thu, 11 Jan 2024 06:08:33 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.4`

```console
$ docker pull emqx@sha256:0e49d60b7272bb5bf8b26b545d3b360775b616f6be658d88a1b36826cc87e9ff
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
$ docker pull emqx@sha256:6a0096f9b9b3f102898935709b000e71417a2eca8023556f85864532150688b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108465759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f33409a87fe69d87a4d6529af86540b8a7d74d839f565e17422742f5e22d2d1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:07:39 GMT
ENV EMQX_VERSION=5.4.0
# Thu, 11 Jan 2024 06:07:39 GMT
ENV AMD64_SHA256=5572dccf3704dbd910f145fe19882fa30fdd9132113d0a28110444d4d5685a3f
# Thu, 11 Jan 2024 06:07:39 GMT
ENV ARM64_SHA256=0dbe92966a93054a8dca89762c00b06a44659c7921177feb291a5ddd5340cefc
# Thu, 11 Jan 2024 06:07:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 11 Jan 2024 06:07:50 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:07:50 GMT
WORKDIR /opt/emqx
# Thu, 11 Jan 2024 06:07:50 GMT
USER emqx
# Thu, 11 Jan 2024 06:07:51 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 11 Jan 2024 06:07:51 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 11 Jan 2024 06:07:51 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 11 Jan 2024 06:07:51 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:07:51 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3d26b33db37cf44cbbf1baebbc7209ca524b0725e91f53a022e83bea45e3c3`  
		Last Modified: Thu, 11 Jan 2024 06:08:53 GMT  
		Size: 78.4 MB (78400848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51165c3bea9a3baf7f28b5f94dff104c70881233ffd56055d8c6dcc9ac249835`  
		Last Modified: Thu, 11 Jan 2024 06:08:46 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.4.0`

```console
$ docker pull emqx@sha256:0e49d60b7272bb5bf8b26b545d3b360775b616f6be658d88a1b36826cc87e9ff
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
$ docker pull emqx@sha256:6a0096f9b9b3f102898935709b000e71417a2eca8023556f85864532150688b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108465759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f33409a87fe69d87a4d6529af86540b8a7d74d839f565e17422742f5e22d2d1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:07:39 GMT
ENV EMQX_VERSION=5.4.0
# Thu, 11 Jan 2024 06:07:39 GMT
ENV AMD64_SHA256=5572dccf3704dbd910f145fe19882fa30fdd9132113d0a28110444d4d5685a3f
# Thu, 11 Jan 2024 06:07:39 GMT
ENV ARM64_SHA256=0dbe92966a93054a8dca89762c00b06a44659c7921177feb291a5ddd5340cefc
# Thu, 11 Jan 2024 06:07:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 11 Jan 2024 06:07:50 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:07:50 GMT
WORKDIR /opt/emqx
# Thu, 11 Jan 2024 06:07:50 GMT
USER emqx
# Thu, 11 Jan 2024 06:07:51 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 11 Jan 2024 06:07:51 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 11 Jan 2024 06:07:51 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 11 Jan 2024 06:07:51 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:07:51 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3d26b33db37cf44cbbf1baebbc7209ca524b0725e91f53a022e83bea45e3c3`  
		Last Modified: Thu, 11 Jan 2024 06:08:53 GMT  
		Size: 78.4 MB (78400848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51165c3bea9a3baf7f28b5f94dff104c70881233ffd56055d8c6dcc9ac249835`  
		Last Modified: Thu, 11 Jan 2024 06:08:46 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:latest`

```console
$ docker pull emqx@sha256:0e49d60b7272bb5bf8b26b545d3b360775b616f6be658d88a1b36826cc87e9ff
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
$ docker pull emqx@sha256:6a0096f9b9b3f102898935709b000e71417a2eca8023556f85864532150688b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108465759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f33409a87fe69d87a4d6529af86540b8a7d74d839f565e17422742f5e22d2d1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:59 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Thu, 11 Jan 2024 02:40:59 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 06:07:39 GMT
ENV EMQX_VERSION=5.4.0
# Thu, 11 Jan 2024 06:07:39 GMT
ENV AMD64_SHA256=5572dccf3704dbd910f145fe19882fa30fdd9132113d0a28110444d4d5685a3f
# Thu, 11 Jan 2024 06:07:39 GMT
ENV ARM64_SHA256=0dbe92966a93054a8dca89762c00b06a44659c7921177feb291a5ddd5340cefc
# Thu, 11 Jan 2024 06:07:39 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 11 Jan 2024 06:07:50 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Thu, 11 Jan 2024 06:07:50 GMT
WORKDIR /opt/emqx
# Thu, 11 Jan 2024 06:07:50 GMT
USER emqx
# Thu, 11 Jan 2024 06:07:51 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 11 Jan 2024 06:07:51 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Thu, 11 Jan 2024 06:07:51 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 11 Jan 2024 06:07:51 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 11 Jan 2024 06:07:51 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3d26b33db37cf44cbbf1baebbc7209ca524b0725e91f53a022e83bea45e3c3`  
		Last Modified: Thu, 11 Jan 2024 06:08:53 GMT  
		Size: 78.4 MB (78400848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51165c3bea9a3baf7f28b5f94dff104c70881233ffd56055d8c6dcc9ac249835`  
		Last Modified: Thu, 11 Jan 2024 06:08:46 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
