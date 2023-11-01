<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:5`](#emqx5)
-	[`emqx:5.0`](#emqx50)
-	[`emqx:5.0.26`](#emqx5026)
-	[`emqx:5.1`](#emqx51)
-	[`emqx:5.1.6`](#emqx516)
-	[`emqx:5.2`](#emqx52)
-	[`emqx:5.2.1`](#emqx521)
-	[`emqx:5.3`](#emqx53)
-	[`emqx:5.3.0`](#emqx530)
-	[`emqx:latest`](#emqxlatest)

## `emqx:5`

```console
$ docker pull emqx@sha256:e65d073e6cdff681b143d1d8e32eeda7343ad327f0590e48cd355a783610b2b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:21ef166de954fa3d5e484d246397f566f81925dd6e342b0cbe3cb37c752de903
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101097450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a27e33fd542808bbc5aa2f3a9215a0d59cb745b3c04ac921b4e21b75b7132a8`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 04:59:24 GMT
ENV EMQX_VERSION=5.3.0
# Wed, 01 Nov 2023 04:59:24 GMT
ENV AMD64_SHA256=c534711d2a2b278e93dea33c2019f6e3b647f372a67e7a987ed7b0ca0984394d
# Wed, 01 Nov 2023 04:59:24 GMT
ENV ARM64_SHA256=1aa299f0ff04ed08af1fe4de37adbe888616ae203b7e38e81ef1f78b6f10527b
# Wed, 01 Nov 2023 04:59:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 01 Nov 2023 04:59:42 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 04:59:42 GMT
WORKDIR /opt/emqx
# Wed, 01 Nov 2023 04:59:42 GMT
USER emqx
# Wed, 01 Nov 2023 04:59:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 01 Nov 2023 04:59:42 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 01 Nov 2023 04:59:42 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 01 Nov 2023 04:59:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 01 Nov 2023 04:59:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa951f191d90609bdcffbad9dcbb57fb7bdd9f33c68aefc212df6f1d4cf58cc`  
		Last Modified: Wed, 01 Nov 2023 05:00:56 GMT  
		Size: 69.7 MB (69678633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c035ed70287908defdf38f8b1389b5f19a20fc3a23c6f778a1fd96f023e8cad`  
		Last Modified: Wed, 01 Nov 2023 05:00:48 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:434f538a77274155c3c36e769cf85061587ea13646b228007f9341d65a18b6a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91392162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33af0ed47222a6b07b7c37173a8804b2453adcc7fdfe9a4802e3c39f3994d6b4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 22:33:23 GMT
ENV EMQX_VERSION=5.3.0
# Wed, 11 Oct 2023 22:33:23 GMT
ENV AMD64_SHA256=c534711d2a2b278e93dea33c2019f6e3b647f372a67e7a987ed7b0ca0984394d
# Wed, 11 Oct 2023 22:33:23 GMT
ENV ARM64_SHA256=1aa299f0ff04ed08af1fe4de37adbe888616ae203b7e38e81ef1f78b6f10527b
# Wed, 11 Oct 2023 22:33:23 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 11 Oct 2023 22:33:36 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 22:33:36 GMT
WORKDIR /opt/emqx
# Wed, 11 Oct 2023 22:33:36 GMT
USER emqx
# Wed, 11 Oct 2023 22:33:36 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 Oct 2023 22:33:37 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 11 Oct 2023 22:33:37 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 11 Oct 2023 22:33:37 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 Oct 2023 22:33:37 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c22a6b8bf4a0abd905adc5e5daf5df01b957d842cb3823a1d641434cf4afd4`  
		Last Modified: Wed, 11 Oct 2023 22:34:39 GMT  
		Size: 61.3 MB (61327172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748d2956a29ac7156af4516b9eacab5be3a3a666f4a7b52aa57c15d4b768f3b4`  
		Last Modified: Wed, 11 Oct 2023 22:34:33 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.0`

```console
$ docker pull emqx@sha256:6d5e3955c5b85121070407527db266dae487a18a61aad2cd3777f3133d1c2b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.0` - linux; amd64

```console
$ docker pull emqx@sha256:9c5491db12ef2ca83926d7ef125b7ca5caf7dd35b459112cad5cccc494c0f84e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101984009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76351e155569a72186d600f1c58b439c1f14ad7ce971fabb3c5496ba2817108b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 04:58:27 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 04:58:27 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 01 Nov 2023 04:58:27 GMT
ENV EMQX_VERSION=5.0.26
# Wed, 01 Nov 2023 04:58:28 GMT
ENV AMD64_SHA256=00f954065fe7fd2f678f2e561578234240cc2cace49fb5cbb5aa7fb450825ffa
# Wed, 01 Nov 2023 04:58:28 GMT
ENV ARM64_SHA256=0b013f0b900e687c1ef3ed73bd6fef268b5492d12a3083ffd0d75c8e3935b4ae
# Wed, 01 Nov 2023 04:58:28 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 01 Nov 2023 04:58:38 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 01 Nov 2023 04:58:39 GMT
WORKDIR /opt/emqx
# Wed, 01 Nov 2023 04:58:39 GMT
USER emqx
# Wed, 01 Nov 2023 04:58:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 01 Nov 2023 04:58:39 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 01 Nov 2023 04:58:39 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 01 Nov 2023 04:58:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 01 Nov 2023 04:58:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fe217836c5687c572b72a280ad71deb220e59ddcecc1922c819c5f83b1f6e5`  
		Last Modified: Wed, 01 Nov 2023 04:59:57 GMT  
		Size: 3.0 MB (2989237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38063d59296b0772b4e82c2bebe3c9e90c5370fa533729ffc8ed7162ef2fb44d`  
		Last Modified: Wed, 01 Nov 2023 04:59:56 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bfd36fad3723fd34b5df7332c78ae3bfa76ed3f85b7e65ac77a6b811585a4a9`  
		Last Modified: Wed, 01 Nov 2023 05:00:05 GMT  
		Size: 67.6 MB (67571850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:333968be826d130d0a687abf9c69d9b0e7b3ad0120226c4ddd78d8c1dbf848ae`  
		Last Modified: Wed, 01 Nov 2023 04:59:56 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.0` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:48b2874e7042acd5a05c6177871b2958a3849b6dee2b5d7ead8773ff034944d2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93064035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f992584d5bbda0a07c75ac49519545f10340b8d8a50c9c1f1d2a6a43c939b9ce`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 22:32:40 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 22:32:41 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 11 Oct 2023 22:32:41 GMT
ENV EMQX_VERSION=5.0.26
# Wed, 11 Oct 2023 22:32:41 GMT
ENV AMD64_SHA256=00f954065fe7fd2f678f2e561578234240cc2cace49fb5cbb5aa7fb450825ffa
# Wed, 11 Oct 2023 22:32:41 GMT
ENV ARM64_SHA256=0b013f0b900e687c1ef3ed73bd6fef268b5492d12a3083ffd0d75c8e3935b4ae
# Wed, 11 Oct 2023 22:32:41 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 11 Oct 2023 22:32:48 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 11 Oct 2023 22:32:48 GMT
WORKDIR /opt/emqx
# Wed, 11 Oct 2023 22:32:48 GMT
USER emqx
# Wed, 11 Oct 2023 22:32:48 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 Oct 2023 22:32:48 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 11 Oct 2023 22:32:48 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 11 Oct 2023 22:32:49 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 Oct 2023 22:32:49 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35268b46a5017b4ab4a19d82fdbce7cf5eebc19812e0371aa196060b28b83e4`  
		Last Modified: Wed, 11 Oct 2023 22:33:51 GMT  
		Size: 3.0 MB (3005523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca7a4a4168e436f382bad41939f1b1f7e26a5fd9993b98e3f9c771f53b0544b`  
		Last Modified: Wed, 11 Oct 2023 22:33:50 GMT  
		Size: 4.1 KB (4118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0669ace7d5cb617ec98e323ee2f9c127a9ab7e10d0712ea5193e27259d51d78`  
		Last Modified: Wed, 11 Oct 2023 22:33:56 GMT  
		Size: 60.0 MB (59989406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:116d4a2cec76fb4f9635c6667466156b75b3a3366ccf768a8da18c02e27c42b7`  
		Last Modified: Wed, 11 Oct 2023 22:33:50 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.0.26`

```console
$ docker pull emqx@sha256:6d5e3955c5b85121070407527db266dae487a18a61aad2cd3777f3133d1c2b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.0.26` - linux; amd64

```console
$ docker pull emqx@sha256:9c5491db12ef2ca83926d7ef125b7ca5caf7dd35b459112cad5cccc494c0f84e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101984009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76351e155569a72186d600f1c58b439c1f14ad7ce971fabb3c5496ba2817108b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 04:58:27 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 04:58:27 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 01 Nov 2023 04:58:27 GMT
ENV EMQX_VERSION=5.0.26
# Wed, 01 Nov 2023 04:58:28 GMT
ENV AMD64_SHA256=00f954065fe7fd2f678f2e561578234240cc2cace49fb5cbb5aa7fb450825ffa
# Wed, 01 Nov 2023 04:58:28 GMT
ENV ARM64_SHA256=0b013f0b900e687c1ef3ed73bd6fef268b5492d12a3083ffd0d75c8e3935b4ae
# Wed, 01 Nov 2023 04:58:28 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 01 Nov 2023 04:58:38 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 01 Nov 2023 04:58:39 GMT
WORKDIR /opt/emqx
# Wed, 01 Nov 2023 04:58:39 GMT
USER emqx
# Wed, 01 Nov 2023 04:58:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 01 Nov 2023 04:58:39 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 01 Nov 2023 04:58:39 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 01 Nov 2023 04:58:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 01 Nov 2023 04:58:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fe217836c5687c572b72a280ad71deb220e59ddcecc1922c819c5f83b1f6e5`  
		Last Modified: Wed, 01 Nov 2023 04:59:57 GMT  
		Size: 3.0 MB (2989237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38063d59296b0772b4e82c2bebe3c9e90c5370fa533729ffc8ed7162ef2fb44d`  
		Last Modified: Wed, 01 Nov 2023 04:59:56 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bfd36fad3723fd34b5df7332c78ae3bfa76ed3f85b7e65ac77a6b811585a4a9`  
		Last Modified: Wed, 01 Nov 2023 05:00:05 GMT  
		Size: 67.6 MB (67571850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:333968be826d130d0a687abf9c69d9b0e7b3ad0120226c4ddd78d8c1dbf848ae`  
		Last Modified: Wed, 01 Nov 2023 04:59:56 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.0.26` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:48b2874e7042acd5a05c6177871b2958a3849b6dee2b5d7ead8773ff034944d2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93064035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f992584d5bbda0a07c75ac49519545f10340b8d8a50c9c1f1d2a6a43c939b9ce`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 22:32:40 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 22:32:41 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 11 Oct 2023 22:32:41 GMT
ENV EMQX_VERSION=5.0.26
# Wed, 11 Oct 2023 22:32:41 GMT
ENV AMD64_SHA256=00f954065fe7fd2f678f2e561578234240cc2cace49fb5cbb5aa7fb450825ffa
# Wed, 11 Oct 2023 22:32:41 GMT
ENV ARM64_SHA256=0b013f0b900e687c1ef3ed73bd6fef268b5492d12a3083ffd0d75c8e3935b4ae
# Wed, 11 Oct 2023 22:32:41 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 11 Oct 2023 22:32:48 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 11 Oct 2023 22:32:48 GMT
WORKDIR /opt/emqx
# Wed, 11 Oct 2023 22:32:48 GMT
USER emqx
# Wed, 11 Oct 2023 22:32:48 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 Oct 2023 22:32:48 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 11 Oct 2023 22:32:48 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 11 Oct 2023 22:32:49 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 Oct 2023 22:32:49 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35268b46a5017b4ab4a19d82fdbce7cf5eebc19812e0371aa196060b28b83e4`  
		Last Modified: Wed, 11 Oct 2023 22:33:51 GMT  
		Size: 3.0 MB (3005523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca7a4a4168e436f382bad41939f1b1f7e26a5fd9993b98e3f9c771f53b0544b`  
		Last Modified: Wed, 11 Oct 2023 22:33:50 GMT  
		Size: 4.1 KB (4118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0669ace7d5cb617ec98e323ee2f9c127a9ab7e10d0712ea5193e27259d51d78`  
		Last Modified: Wed, 11 Oct 2023 22:33:56 GMT  
		Size: 60.0 MB (59989406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:116d4a2cec76fb4f9635c6667466156b75b3a3366ccf768a8da18c02e27c42b7`  
		Last Modified: Wed, 11 Oct 2023 22:33:50 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.1`

```console
$ docker pull emqx@sha256:2081b63ababf991cd8cce122e7946aedcadbef793d80111052fdbeed7b2e3b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.1` - linux; amd64

```console
$ docker pull emqx@sha256:c2a23946e6bbf14aa7fae5586d35821e8842c67369878a2f5d82ed004b050775
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102393414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ea1ae47560586da9327a21bf7acd1b465fa79a777271d44ee31e0a6d6ecbef`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 04:58:27 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 04:58:27 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 01 Nov 2023 04:58:45 GMT
ENV EMQX_VERSION=5.1.6
# Wed, 01 Nov 2023 04:58:45 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Wed, 01 Nov 2023 04:58:45 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Wed, 01 Nov 2023 04:58:45 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 01 Nov 2023 04:58:56 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Wed, 01 Nov 2023 04:58:56 GMT
WORKDIR /opt/emqx
# Wed, 01 Nov 2023 04:58:56 GMT
USER emqx
# Wed, 01 Nov 2023 04:58:56 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 01 Nov 2023 04:58:57 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 01 Nov 2023 04:58:57 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 01 Nov 2023 04:58:57 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 01 Nov 2023 04:58:57 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fe217836c5687c572b72a280ad71deb220e59ddcecc1922c819c5f83b1f6e5`  
		Last Modified: Wed, 01 Nov 2023 04:59:57 GMT  
		Size: 3.0 MB (2989237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38063d59296b0772b4e82c2bebe3c9e90c5370fa533729ffc8ed7162ef2fb44d`  
		Last Modified: Wed, 01 Nov 2023 04:59:56 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03b7b5c3ba5b27a3db8de9bca56ad6d403808a562845c3682e66401ccf6022f`  
		Last Modified: Wed, 01 Nov 2023 05:00:25 GMT  
		Size: 68.0 MB (67981255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c373e252eafc3c62198309776738ab870e37b407fe34d854678738d5898eca19`  
		Last Modified: Wed, 01 Nov 2023 05:00:18 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:42ac54b2e3905656b356eb477be029e60465993616415e6bfd5b81d449891f8a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92699258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97c3cdab9ccb2f24ae341fe0422496ae37a057969e30a5a9515c91195add17d8`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 22:32:40 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 22:32:41 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 11 Oct 2023 22:32:52 GMT
ENV EMQX_VERSION=5.1.6
# Wed, 11 Oct 2023 22:32:52 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Wed, 11 Oct 2023 22:32:52 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Wed, 11 Oct 2023 22:32:52 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 11 Oct 2023 22:32:59 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Wed, 11 Oct 2023 22:32:59 GMT
WORKDIR /opt/emqx
# Wed, 11 Oct 2023 22:32:59 GMT
USER emqx
# Wed, 11 Oct 2023 22:33:00 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 Oct 2023 22:33:00 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 11 Oct 2023 22:33:00 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 11 Oct 2023 22:33:00 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 Oct 2023 22:33:00 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35268b46a5017b4ab4a19d82fdbce7cf5eebc19812e0371aa196060b28b83e4`  
		Last Modified: Wed, 11 Oct 2023 22:33:51 GMT  
		Size: 3.0 MB (3005523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca7a4a4168e436f382bad41939f1b1f7e26a5fd9993b98e3f9c771f53b0544b`  
		Last Modified: Wed, 11 Oct 2023 22:33:50 GMT  
		Size: 4.1 KB (4118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7560261d159ae5d277deb73dceb52f1981eebf07f1b9e82c2c8a46aad317a4`  
		Last Modified: Wed, 11 Oct 2023 22:34:10 GMT  
		Size: 59.6 MB (59624630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f68b9c410de16d5181c03b376c69fee5185e244bc067cba6ff3f80e17383ac54`  
		Last Modified: Wed, 11 Oct 2023 22:34:05 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.1.6`

```console
$ docker pull emqx@sha256:2081b63ababf991cd8cce122e7946aedcadbef793d80111052fdbeed7b2e3b0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.1.6` - linux; amd64

```console
$ docker pull emqx@sha256:c2a23946e6bbf14aa7fae5586d35821e8842c67369878a2f5d82ed004b050775
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102393414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ea1ae47560586da9327a21bf7acd1b465fa79a777271d44ee31e0a6d6ecbef`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 04:58:27 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 04:58:27 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 01 Nov 2023 04:58:45 GMT
ENV EMQX_VERSION=5.1.6
# Wed, 01 Nov 2023 04:58:45 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Wed, 01 Nov 2023 04:58:45 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Wed, 01 Nov 2023 04:58:45 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 01 Nov 2023 04:58:56 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Wed, 01 Nov 2023 04:58:56 GMT
WORKDIR /opt/emqx
# Wed, 01 Nov 2023 04:58:56 GMT
USER emqx
# Wed, 01 Nov 2023 04:58:56 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 01 Nov 2023 04:58:57 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 01 Nov 2023 04:58:57 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 01 Nov 2023 04:58:57 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 01 Nov 2023 04:58:57 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fe217836c5687c572b72a280ad71deb220e59ddcecc1922c819c5f83b1f6e5`  
		Last Modified: Wed, 01 Nov 2023 04:59:57 GMT  
		Size: 3.0 MB (2989237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38063d59296b0772b4e82c2bebe3c9e90c5370fa533729ffc8ed7162ef2fb44d`  
		Last Modified: Wed, 01 Nov 2023 04:59:56 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03b7b5c3ba5b27a3db8de9bca56ad6d403808a562845c3682e66401ccf6022f`  
		Last Modified: Wed, 01 Nov 2023 05:00:25 GMT  
		Size: 68.0 MB (67981255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c373e252eafc3c62198309776738ab870e37b407fe34d854678738d5898eca19`  
		Last Modified: Wed, 01 Nov 2023 05:00:18 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.1.6` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:42ac54b2e3905656b356eb477be029e60465993616415e6bfd5b81d449891f8a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92699258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97c3cdab9ccb2f24ae341fe0422496ae37a057969e30a5a9515c91195add17d8`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 22:32:40 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 22:32:41 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 11 Oct 2023 22:32:52 GMT
ENV EMQX_VERSION=5.1.6
# Wed, 11 Oct 2023 22:32:52 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Wed, 11 Oct 2023 22:32:52 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Wed, 11 Oct 2023 22:32:52 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 11 Oct 2023 22:32:59 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Wed, 11 Oct 2023 22:32:59 GMT
WORKDIR /opt/emqx
# Wed, 11 Oct 2023 22:32:59 GMT
USER emqx
# Wed, 11 Oct 2023 22:33:00 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 Oct 2023 22:33:00 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 11 Oct 2023 22:33:00 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 11 Oct 2023 22:33:00 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 Oct 2023 22:33:00 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35268b46a5017b4ab4a19d82fdbce7cf5eebc19812e0371aa196060b28b83e4`  
		Last Modified: Wed, 11 Oct 2023 22:33:51 GMT  
		Size: 3.0 MB (3005523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca7a4a4168e436f382bad41939f1b1f7e26a5fd9993b98e3f9c771f53b0544b`  
		Last Modified: Wed, 11 Oct 2023 22:33:50 GMT  
		Size: 4.1 KB (4118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7560261d159ae5d277deb73dceb52f1981eebf07f1b9e82c2c8a46aad317a4`  
		Last Modified: Wed, 11 Oct 2023 22:34:10 GMT  
		Size: 59.6 MB (59624630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f68b9c410de16d5181c03b376c69fee5185e244bc067cba6ff3f80e17383ac54`  
		Last Modified: Wed, 11 Oct 2023 22:34:05 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.2`

```console
$ docker pull emqx@sha256:d586570f24f02e30da14820332a336461393c241eda0eab8df401f1b18efabf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.2` - linux; amd64

```console
$ docker pull emqx@sha256:6eb3ec201bff1b88852458b87c2c644a1a8d46f99ce8b2fbb2e667f38ae8846f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101165579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1fc404ec6700153e988d82c2556c233b80aa04bb4f1c32ec844f6fadffe154`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 04:59:04 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 04:59:04 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 01 Nov 2023 04:59:05 GMT
ENV EMQX_VERSION=5.2.1
# Wed, 01 Nov 2023 04:59:05 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Wed, 01 Nov 2023 04:59:05 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Wed, 01 Nov 2023 04:59:05 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 01 Nov 2023 04:59:18 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Wed, 01 Nov 2023 04:59:19 GMT
WORKDIR /opt/emqx
# Wed, 01 Nov 2023 04:59:19 GMT
USER emqx
# Wed, 01 Nov 2023 04:59:19 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 01 Nov 2023 04:59:19 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 01 Nov 2023 04:59:19 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 01 Nov 2023 04:59:19 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 01 Nov 2023 04:59:19 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573138db7004555fa87d2527352cb1283a3618a572a284110bbddc2e76c61521`  
		Last Modified: Wed, 01 Nov 2023 05:00:34 GMT  
		Size: 1.6 MB (1631629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:999d1079ec0e6dfb1224326f8e2ed602bbe4e131dd1aca6af62eb28f51349678`  
		Last Modified: Wed, 01 Nov 2023 05:00:33 GMT  
		Size: 4.1 KB (4108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d3806e327889811435ede521c3961118d6f06531c6557526f058582e579322`  
		Last Modified: Wed, 01 Nov 2023 05:00:40 GMT  
		Size: 68.1 MB (68111024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabcb7a88a5ee8f7497a999d3b7c99492b448ee627d2e5e974b6e377c348cbf3`  
		Last Modified: Wed, 01 Nov 2023 05:00:34 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:fa56287144f52e9706770276a5d46fd504205d55f2ecfe13c35d8a5a56c054e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91466856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e4991302a34a702d8ccb84000284e1e397d01a423d78774cf23d646011767b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 22:33:07 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 22:33:08 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 11 Oct 2023 22:33:08 GMT
ENV EMQX_VERSION=5.2.1
# Wed, 11 Oct 2023 22:33:08 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Wed, 11 Oct 2023 22:33:08 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Wed, 11 Oct 2023 22:33:08 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 11 Oct 2023 22:33:18 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Wed, 11 Oct 2023 22:33:19 GMT
WORKDIR /opt/emqx
# Wed, 11 Oct 2023 22:33:19 GMT
USER emqx
# Wed, 11 Oct 2023 22:33:19 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 Oct 2023 22:33:19 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 11 Oct 2023 22:33:19 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 11 Oct 2023 22:33:19 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 Oct 2023 22:33:19 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a2025c21d9db013c6c95e5faa344643ed0394567adf59154265c2c8d4b6e2c`  
		Last Modified: Wed, 11 Oct 2023 22:34:19 GMT  
		Size: 1.6 MB (1645882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad368c43a6f78e25d2dfd4138c309fc07bc80af2177013c6f0490e1bcef3074a`  
		Last Modified: Wed, 11 Oct 2023 22:34:18 GMT  
		Size: 4.1 KB (4122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:decf55894f79f74740bf727a8c43931d07169e08a0460adb4bf32542a6218a79`  
		Last Modified: Wed, 11 Oct 2023 22:34:23 GMT  
		Size: 59.8 MB (59751864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1a684a60f05707fd564ba059ffcc57d9b1763a7cae76f957ef10cae1fb8c42`  
		Last Modified: Wed, 11 Oct 2023 22:34:18 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.2.1`

```console
$ docker pull emqx@sha256:d586570f24f02e30da14820332a336461393c241eda0eab8df401f1b18efabf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.2.1` - linux; amd64

```console
$ docker pull emqx@sha256:6eb3ec201bff1b88852458b87c2c644a1a8d46f99ce8b2fbb2e667f38ae8846f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101165579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1fc404ec6700153e988d82c2556c233b80aa04bb4f1c32ec844f6fadffe154`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 04:59:04 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 04:59:04 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 01 Nov 2023 04:59:05 GMT
ENV EMQX_VERSION=5.2.1
# Wed, 01 Nov 2023 04:59:05 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Wed, 01 Nov 2023 04:59:05 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Wed, 01 Nov 2023 04:59:05 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 01 Nov 2023 04:59:18 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Wed, 01 Nov 2023 04:59:19 GMT
WORKDIR /opt/emqx
# Wed, 01 Nov 2023 04:59:19 GMT
USER emqx
# Wed, 01 Nov 2023 04:59:19 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 01 Nov 2023 04:59:19 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 01 Nov 2023 04:59:19 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 01 Nov 2023 04:59:19 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 01 Nov 2023 04:59:19 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573138db7004555fa87d2527352cb1283a3618a572a284110bbddc2e76c61521`  
		Last Modified: Wed, 01 Nov 2023 05:00:34 GMT  
		Size: 1.6 MB (1631629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:999d1079ec0e6dfb1224326f8e2ed602bbe4e131dd1aca6af62eb28f51349678`  
		Last Modified: Wed, 01 Nov 2023 05:00:33 GMT  
		Size: 4.1 KB (4108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d3806e327889811435ede521c3961118d6f06531c6557526f058582e579322`  
		Last Modified: Wed, 01 Nov 2023 05:00:40 GMT  
		Size: 68.1 MB (68111024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabcb7a88a5ee8f7497a999d3b7c99492b448ee627d2e5e974b6e377c348cbf3`  
		Last Modified: Wed, 01 Nov 2023 05:00:34 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.2.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:fa56287144f52e9706770276a5d46fd504205d55f2ecfe13c35d8a5a56c054e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91466856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e4991302a34a702d8ccb84000284e1e397d01a423d78774cf23d646011767b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 22:33:07 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 22:33:08 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 11 Oct 2023 22:33:08 GMT
ENV EMQX_VERSION=5.2.1
# Wed, 11 Oct 2023 22:33:08 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Wed, 11 Oct 2023 22:33:08 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Wed, 11 Oct 2023 22:33:08 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 11 Oct 2023 22:33:18 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Wed, 11 Oct 2023 22:33:19 GMT
WORKDIR /opt/emqx
# Wed, 11 Oct 2023 22:33:19 GMT
USER emqx
# Wed, 11 Oct 2023 22:33:19 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 Oct 2023 22:33:19 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 11 Oct 2023 22:33:19 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 11 Oct 2023 22:33:19 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 Oct 2023 22:33:19 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a2025c21d9db013c6c95e5faa344643ed0394567adf59154265c2c8d4b6e2c`  
		Last Modified: Wed, 11 Oct 2023 22:34:19 GMT  
		Size: 1.6 MB (1645882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad368c43a6f78e25d2dfd4138c309fc07bc80af2177013c6f0490e1bcef3074a`  
		Last Modified: Wed, 11 Oct 2023 22:34:18 GMT  
		Size: 4.1 KB (4122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:decf55894f79f74740bf727a8c43931d07169e08a0460adb4bf32542a6218a79`  
		Last Modified: Wed, 11 Oct 2023 22:34:23 GMT  
		Size: 59.8 MB (59751864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c1a684a60f05707fd564ba059ffcc57d9b1763a7cae76f957ef10cae1fb8c42`  
		Last Modified: Wed, 11 Oct 2023 22:34:18 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.3`

```console
$ docker pull emqx@sha256:e65d073e6cdff681b143d1d8e32eeda7343ad327f0590e48cd355a783610b2b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.3` - linux; amd64

```console
$ docker pull emqx@sha256:21ef166de954fa3d5e484d246397f566f81925dd6e342b0cbe3cb37c752de903
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101097450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a27e33fd542808bbc5aa2f3a9215a0d59cb745b3c04ac921b4e21b75b7132a8`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 04:59:24 GMT
ENV EMQX_VERSION=5.3.0
# Wed, 01 Nov 2023 04:59:24 GMT
ENV AMD64_SHA256=c534711d2a2b278e93dea33c2019f6e3b647f372a67e7a987ed7b0ca0984394d
# Wed, 01 Nov 2023 04:59:24 GMT
ENV ARM64_SHA256=1aa299f0ff04ed08af1fe4de37adbe888616ae203b7e38e81ef1f78b6f10527b
# Wed, 01 Nov 2023 04:59:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 01 Nov 2023 04:59:42 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 04:59:42 GMT
WORKDIR /opt/emqx
# Wed, 01 Nov 2023 04:59:42 GMT
USER emqx
# Wed, 01 Nov 2023 04:59:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 01 Nov 2023 04:59:42 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 01 Nov 2023 04:59:42 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 01 Nov 2023 04:59:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 01 Nov 2023 04:59:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa951f191d90609bdcffbad9dcbb57fb7bdd9f33c68aefc212df6f1d4cf58cc`  
		Last Modified: Wed, 01 Nov 2023 05:00:56 GMT  
		Size: 69.7 MB (69678633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c035ed70287908defdf38f8b1389b5f19a20fc3a23c6f778a1fd96f023e8cad`  
		Last Modified: Wed, 01 Nov 2023 05:00:48 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.3` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:434f538a77274155c3c36e769cf85061587ea13646b228007f9341d65a18b6a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91392162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33af0ed47222a6b07b7c37173a8804b2453adcc7fdfe9a4802e3c39f3994d6b4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 22:33:23 GMT
ENV EMQX_VERSION=5.3.0
# Wed, 11 Oct 2023 22:33:23 GMT
ENV AMD64_SHA256=c534711d2a2b278e93dea33c2019f6e3b647f372a67e7a987ed7b0ca0984394d
# Wed, 11 Oct 2023 22:33:23 GMT
ENV ARM64_SHA256=1aa299f0ff04ed08af1fe4de37adbe888616ae203b7e38e81ef1f78b6f10527b
# Wed, 11 Oct 2023 22:33:23 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 11 Oct 2023 22:33:36 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 22:33:36 GMT
WORKDIR /opt/emqx
# Wed, 11 Oct 2023 22:33:36 GMT
USER emqx
# Wed, 11 Oct 2023 22:33:36 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 Oct 2023 22:33:37 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 11 Oct 2023 22:33:37 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 11 Oct 2023 22:33:37 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 Oct 2023 22:33:37 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c22a6b8bf4a0abd905adc5e5daf5df01b957d842cb3823a1d641434cf4afd4`  
		Last Modified: Wed, 11 Oct 2023 22:34:39 GMT  
		Size: 61.3 MB (61327172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748d2956a29ac7156af4516b9eacab5be3a3a666f4a7b52aa57c15d4b768f3b4`  
		Last Modified: Wed, 11 Oct 2023 22:34:33 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.3.0`

```console
$ docker pull emqx@sha256:e65d073e6cdff681b143d1d8e32eeda7343ad327f0590e48cd355a783610b2b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.3.0` - linux; amd64

```console
$ docker pull emqx@sha256:21ef166de954fa3d5e484d246397f566f81925dd6e342b0cbe3cb37c752de903
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101097450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a27e33fd542808bbc5aa2f3a9215a0d59cb745b3c04ac921b4e21b75b7132a8`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 04:59:24 GMT
ENV EMQX_VERSION=5.3.0
# Wed, 01 Nov 2023 04:59:24 GMT
ENV AMD64_SHA256=c534711d2a2b278e93dea33c2019f6e3b647f372a67e7a987ed7b0ca0984394d
# Wed, 01 Nov 2023 04:59:24 GMT
ENV ARM64_SHA256=1aa299f0ff04ed08af1fe4de37adbe888616ae203b7e38e81ef1f78b6f10527b
# Wed, 01 Nov 2023 04:59:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 01 Nov 2023 04:59:42 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 04:59:42 GMT
WORKDIR /opt/emqx
# Wed, 01 Nov 2023 04:59:42 GMT
USER emqx
# Wed, 01 Nov 2023 04:59:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 01 Nov 2023 04:59:42 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 01 Nov 2023 04:59:42 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 01 Nov 2023 04:59:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 01 Nov 2023 04:59:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa951f191d90609bdcffbad9dcbb57fb7bdd9f33c68aefc212df6f1d4cf58cc`  
		Last Modified: Wed, 01 Nov 2023 05:00:56 GMT  
		Size: 69.7 MB (69678633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c035ed70287908defdf38f8b1389b5f19a20fc3a23c6f778a1fd96f023e8cad`  
		Last Modified: Wed, 01 Nov 2023 05:00:48 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.3.0` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:434f538a77274155c3c36e769cf85061587ea13646b228007f9341d65a18b6a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91392162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33af0ed47222a6b07b7c37173a8804b2453adcc7fdfe9a4802e3c39f3994d6b4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 22:33:23 GMT
ENV EMQX_VERSION=5.3.0
# Wed, 11 Oct 2023 22:33:23 GMT
ENV AMD64_SHA256=c534711d2a2b278e93dea33c2019f6e3b647f372a67e7a987ed7b0ca0984394d
# Wed, 11 Oct 2023 22:33:23 GMT
ENV ARM64_SHA256=1aa299f0ff04ed08af1fe4de37adbe888616ae203b7e38e81ef1f78b6f10527b
# Wed, 11 Oct 2023 22:33:23 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 11 Oct 2023 22:33:36 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 22:33:36 GMT
WORKDIR /opt/emqx
# Wed, 11 Oct 2023 22:33:36 GMT
USER emqx
# Wed, 11 Oct 2023 22:33:36 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 Oct 2023 22:33:37 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 11 Oct 2023 22:33:37 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 11 Oct 2023 22:33:37 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 Oct 2023 22:33:37 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c22a6b8bf4a0abd905adc5e5daf5df01b957d842cb3823a1d641434cf4afd4`  
		Last Modified: Wed, 11 Oct 2023 22:34:39 GMT  
		Size: 61.3 MB (61327172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748d2956a29ac7156af4516b9eacab5be3a3a666f4a7b52aa57c15d4b768f3b4`  
		Last Modified: Wed, 11 Oct 2023 22:34:33 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:latest`

```console
$ docker pull emqx@sha256:e65d073e6cdff681b143d1d8e32eeda7343ad327f0590e48cd355a783610b2b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:21ef166de954fa3d5e484d246397f566f81925dd6e342b0cbe3cb37c752de903
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.1 MB (101097450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a27e33fd542808bbc5aa2f3a9215a0d59cb745b3c04ac921b4e21b75b7132a8`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 01 Nov 2023 00:21:11 GMT
ADD file:5fb15e28ab9cd52a4c1371f9273d159579710f4efb955c1e6d76c0403e36967c in / 
# Wed, 01 Nov 2023 00:21:12 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 04:59:24 GMT
ENV EMQX_VERSION=5.3.0
# Wed, 01 Nov 2023 04:59:24 GMT
ENV AMD64_SHA256=c534711d2a2b278e93dea33c2019f6e3b647f372a67e7a987ed7b0ca0984394d
# Wed, 01 Nov 2023 04:59:24 GMT
ENV ARM64_SHA256=1aa299f0ff04ed08af1fe4de37adbe888616ae203b7e38e81ef1f78b6f10527b
# Wed, 01 Nov 2023 04:59:24 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 01 Nov 2023 04:59:42 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 01 Nov 2023 04:59:42 GMT
WORKDIR /opt/emqx
# Wed, 01 Nov 2023 04:59:42 GMT
USER emqx
# Wed, 01 Nov 2023 04:59:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 01 Nov 2023 04:59:42 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 01 Nov 2023 04:59:42 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 01 Nov 2023 04:59:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 01 Nov 2023 04:59:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:0bc8ff246cb8ff91066742f8f7ded40397e7aaaa925200b7bec5382d1ffcd6a0`  
		Last Modified: Wed, 01 Nov 2023 00:26:12 GMT  
		Size: 31.4 MB (31417915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa951f191d90609bdcffbad9dcbb57fb7bdd9f33c68aefc212df6f1d4cf58cc`  
		Last Modified: Wed, 01 Nov 2023 05:00:56 GMT  
		Size: 69.7 MB (69678633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c035ed70287908defdf38f8b1389b5f19a20fc3a23c6f778a1fd96f023e8cad`  
		Last Modified: Wed, 01 Nov 2023 05:00:48 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:434f538a77274155c3c36e769cf85061587ea13646b228007f9341d65a18b6a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91392162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33af0ed47222a6b07b7c37173a8804b2453adcc7fdfe9a4802e3c39f3994d6b4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 22:33:23 GMT
ENV EMQX_VERSION=5.3.0
# Wed, 11 Oct 2023 22:33:23 GMT
ENV AMD64_SHA256=c534711d2a2b278e93dea33c2019f6e3b647f372a67e7a987ed7b0ca0984394d
# Wed, 11 Oct 2023 22:33:23 GMT
ENV ARM64_SHA256=1aa299f0ff04ed08af1fe4de37adbe888616ae203b7e38e81ef1f78b6f10527b
# Wed, 11 Oct 2023 22:33:23 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 11 Oct 2023 22:33:36 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 22:33:36 GMT
WORKDIR /opt/emqx
# Wed, 11 Oct 2023 22:33:36 GMT
USER emqx
# Wed, 11 Oct 2023 22:33:36 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 Oct 2023 22:33:37 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 11 Oct 2023 22:33:37 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 11 Oct 2023 22:33:37 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 Oct 2023 22:33:37 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c22a6b8bf4a0abd905adc5e5daf5df01b957d842cb3823a1d641434cf4afd4`  
		Last Modified: Wed, 11 Oct 2023 22:34:39 GMT  
		Size: 61.3 MB (61327172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748d2956a29ac7156af4516b9eacab5be3a3a666f4a7b52aa57c15d4b768f3b4`  
		Last Modified: Wed, 11 Oct 2023 22:34:33 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
