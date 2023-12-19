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
-	[`emqx:5.3.2`](#emqx532)
-	[`emqx:latest`](#emqxlatest)

## `emqx:5`

```console
$ docker pull emqx@sha256:542a89ddad403cfe705c5a212c59343ee3b13f7e505bf3bf6fb401873afd8d40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:3c82206aac1aaacb33b4dfbac7f02448a55e5f3053a585229fd2a027e44e8e96
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101780864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2318b222abc2a4ab5841d67867fb414afb31b74c577aeecea5b093627319b141`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:50 GMT
ADD file:bb44d67b03db8efaeb0c4171474f441d14ff35f328f13add32b289fca062fa2f in / 
# Tue, 19 Dec 2023 01:20:50 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:53:13 GMT
ENV EMQX_VERSION=5.3.2
# Tue, 19 Dec 2023 04:53:13 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Tue, 19 Dec 2023 04:53:13 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Tue, 19 Dec 2023 04:53:13 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 19 Dec 2023 04:53:27 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:53:27 GMT
WORKDIR /opt/emqx
# Tue, 19 Dec 2023 04:53:27 GMT
USER emqx
# Tue, 19 Dec 2023 04:53:27 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 19 Dec 2023 04:53:28 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 19 Dec 2023 04:53:28 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 19 Dec 2023 04:53:28 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 04:53:28 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b5a0d5c14ba9ece1eecd5137c468d9a123372b0af2ed2c8c4446137730c90e5b`  
		Last Modified: Tue, 19 Dec 2023 01:25:40 GMT  
		Size: 31.4 MB (31417873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c8584f03abcd8dc4f4e74091c8e788a0de343e4e28e45ce61f5c8e7fa8f21f`  
		Last Modified: Tue, 19 Dec 2023 04:54:37 GMT  
		Size: 70.4 MB (70362088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3ad325587982cabb9a450034ff1c3634132a7dd6fe384135965a76c9761f21`  
		Last Modified: Tue, 19 Dec 2023 04:54:29 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5` - linux; arm64 variant v8

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

## `emqx:5.0`

```console
$ docker pull emqx@sha256:37dcbf358fd4dbda2b9c65c7fb134aa6caaa7a0363ebf8bca876a047fe7b054f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.0` - linux; amd64

```console
$ docker pull emqx@sha256:cdb5d0d498c9a5c4dbfeecb52ae6d6d5b0ece96d123db939b61e87c6902ddbc9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101984409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2850a60f42ca2924f7de4c8d39ef1bca056fdb7a38a2f9b5032992ec181b7698`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:50 GMT
ADD file:bb44d67b03db8efaeb0c4171474f441d14ff35f328f13add32b289fca062fa2f in / 
# Tue, 19 Dec 2023 01:20:50 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:52:30 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:52:31 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 19 Dec 2023 04:52:31 GMT
ENV EMQX_VERSION=5.0.26
# Tue, 19 Dec 2023 04:52:31 GMT
ENV AMD64_SHA256=00f954065fe7fd2f678f2e561578234240cc2cace49fb5cbb5aa7fb450825ffa
# Tue, 19 Dec 2023 04:52:31 GMT
ENV ARM64_SHA256=0b013f0b900e687c1ef3ed73bd6fef268b5492d12a3083ffd0d75c8e3935b4ae
# Tue, 19 Dec 2023 04:52:31 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 19 Dec 2023 04:52:38 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Tue, 19 Dec 2023 04:52:39 GMT
WORKDIR /opt/emqx
# Tue, 19 Dec 2023 04:52:39 GMT
USER emqx
# Tue, 19 Dec 2023 04:52:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 19 Dec 2023 04:52:39 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 19 Dec 2023 04:52:39 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 19 Dec 2023 04:52:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 04:52:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b5a0d5c14ba9ece1eecd5137c468d9a123372b0af2ed2c8c4446137730c90e5b`  
		Last Modified: Tue, 19 Dec 2023 01:25:40 GMT  
		Size: 31.4 MB (31417873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81485be977d1d3fe94a5b66b3785b7655ef00b2f45fd07342cd68fc243ae806`  
		Last Modified: Tue, 19 Dec 2023 04:53:43 GMT  
		Size: 3.0 MB (2989650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b109779462b5f5d7c8711d702009c239196c4c3f39bc2ac0ad12eddea7610c`  
		Last Modified: Tue, 19 Dec 2023 04:53:42 GMT  
		Size: 4.1 KB (4112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9815b8a840a0468772652a27aaf7223b2bbc5149c76827b9381f86d513e14dbb`  
		Last Modified: Tue, 19 Dec 2023 04:53:50 GMT  
		Size: 67.6 MB (67571873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b4084859a820e1b6016b1ebc5279bdb729b6470574e4bafffec22daf352fd5`  
		Last Modified: Tue, 19 Dec 2023 04:53:42 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.0` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:0c3514df0316c5dfe2f49c62b1eaf17acfbe5e936669ad149e71c881f21fbebb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93064372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa264c580add5e15f4087007109be7aa63766f4635ffcf42e10c7c9a9ccada4`
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
# Tue, 19 Dec 2023 07:32:02 GMT
ENV EMQX_VERSION=5.0.26
# Tue, 19 Dec 2023 07:32:02 GMT
ENV AMD64_SHA256=00f954065fe7fd2f678f2e561578234240cc2cace49fb5cbb5aa7fb450825ffa
# Tue, 19 Dec 2023 07:32:02 GMT
ENV ARM64_SHA256=0b013f0b900e687c1ef3ed73bd6fef268b5492d12a3083ffd0d75c8e3935b4ae
# Tue, 19 Dec 2023 07:32:02 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 19 Dec 2023 07:32:08 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Tue, 19 Dec 2023 07:32:08 GMT
WORKDIR /opt/emqx
# Tue, 19 Dec 2023 07:32:08 GMT
USER emqx
# Tue, 19 Dec 2023 07:32:08 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 19 Dec 2023 07:32:08 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 19 Dec 2023 07:32:08 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 19 Dec 2023 07:32:09 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 07:32:09 GMT
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
	-	`sha256:8fd2a6105efa4f736b5440082ff88f8f5144636a7ef7272db04f3b42e0c6791a`  
		Last Modified: Tue, 19 Dec 2023 07:33:09 GMT  
		Size: 60.0 MB (59989383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e65b678e0f5f68a185fd3b477dff7a0919bad70b2f406f0160351b138271bee`  
		Last Modified: Tue, 19 Dec 2023 07:33:03 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.0.26`

```console
$ docker pull emqx@sha256:37dcbf358fd4dbda2b9c65c7fb134aa6caaa7a0363ebf8bca876a047fe7b054f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.0.26` - linux; amd64

```console
$ docker pull emqx@sha256:cdb5d0d498c9a5c4dbfeecb52ae6d6d5b0ece96d123db939b61e87c6902ddbc9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101984409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2850a60f42ca2924f7de4c8d39ef1bca056fdb7a38a2f9b5032992ec181b7698`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:50 GMT
ADD file:bb44d67b03db8efaeb0c4171474f441d14ff35f328f13add32b289fca062fa2f in / 
# Tue, 19 Dec 2023 01:20:50 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:52:30 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:52:31 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 19 Dec 2023 04:52:31 GMT
ENV EMQX_VERSION=5.0.26
# Tue, 19 Dec 2023 04:52:31 GMT
ENV AMD64_SHA256=00f954065fe7fd2f678f2e561578234240cc2cace49fb5cbb5aa7fb450825ffa
# Tue, 19 Dec 2023 04:52:31 GMT
ENV ARM64_SHA256=0b013f0b900e687c1ef3ed73bd6fef268b5492d12a3083ffd0d75c8e3935b4ae
# Tue, 19 Dec 2023 04:52:31 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 19 Dec 2023 04:52:38 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Tue, 19 Dec 2023 04:52:39 GMT
WORKDIR /opt/emqx
# Tue, 19 Dec 2023 04:52:39 GMT
USER emqx
# Tue, 19 Dec 2023 04:52:39 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 19 Dec 2023 04:52:39 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 19 Dec 2023 04:52:39 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 19 Dec 2023 04:52:39 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 04:52:39 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b5a0d5c14ba9ece1eecd5137c468d9a123372b0af2ed2c8c4446137730c90e5b`  
		Last Modified: Tue, 19 Dec 2023 01:25:40 GMT  
		Size: 31.4 MB (31417873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81485be977d1d3fe94a5b66b3785b7655ef00b2f45fd07342cd68fc243ae806`  
		Last Modified: Tue, 19 Dec 2023 04:53:43 GMT  
		Size: 3.0 MB (2989650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b109779462b5f5d7c8711d702009c239196c4c3f39bc2ac0ad12eddea7610c`  
		Last Modified: Tue, 19 Dec 2023 04:53:42 GMT  
		Size: 4.1 KB (4112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9815b8a840a0468772652a27aaf7223b2bbc5149c76827b9381f86d513e14dbb`  
		Last Modified: Tue, 19 Dec 2023 04:53:50 GMT  
		Size: 67.6 MB (67571873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b4084859a820e1b6016b1ebc5279bdb729b6470574e4bafffec22daf352fd5`  
		Last Modified: Tue, 19 Dec 2023 04:53:42 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.0.26` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:0c3514df0316c5dfe2f49c62b1eaf17acfbe5e936669ad149e71c881f21fbebb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93064372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa264c580add5e15f4087007109be7aa63766f4635ffcf42e10c7c9a9ccada4`
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
# Tue, 19 Dec 2023 07:32:02 GMT
ENV EMQX_VERSION=5.0.26
# Tue, 19 Dec 2023 07:32:02 GMT
ENV AMD64_SHA256=00f954065fe7fd2f678f2e561578234240cc2cace49fb5cbb5aa7fb450825ffa
# Tue, 19 Dec 2023 07:32:02 GMT
ENV ARM64_SHA256=0b013f0b900e687c1ef3ed73bd6fef268b5492d12a3083ffd0d75c8e3935b4ae
# Tue, 19 Dec 2023 07:32:02 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 19 Dec 2023 07:32:08 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Tue, 19 Dec 2023 07:32:08 GMT
WORKDIR /opt/emqx
# Tue, 19 Dec 2023 07:32:08 GMT
USER emqx
# Tue, 19 Dec 2023 07:32:08 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 19 Dec 2023 07:32:08 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 19 Dec 2023 07:32:08 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 19 Dec 2023 07:32:09 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 07:32:09 GMT
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
	-	`sha256:8fd2a6105efa4f736b5440082ff88f8f5144636a7ef7272db04f3b42e0c6791a`  
		Last Modified: Tue, 19 Dec 2023 07:33:09 GMT  
		Size: 60.0 MB (59989383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e65b678e0f5f68a185fd3b477dff7a0919bad70b2f406f0160351b138271bee`  
		Last Modified: Tue, 19 Dec 2023 07:33:03 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.1`

```console
$ docker pull emqx@sha256:13530879f2df7c6c232a6ee868d945f828819858683857bc16092bcb7c71398f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.1` - linux; amd64

```console
$ docker pull emqx@sha256:931c0dca953709b7c00a0d214231ff8f56128a3e346f02e7859a06725c64ea1f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102393797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbb9d702579271a58adf5cbd49a7259b37f9f9c9597d610b09a3d36c85b0d4a9`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:50 GMT
ADD file:bb44d67b03db8efaeb0c4171474f441d14ff35f328f13add32b289fca062fa2f in / 
# Tue, 19 Dec 2023 01:20:50 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:52:30 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:52:31 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 19 Dec 2023 04:52:42 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 19 Dec 2023 04:52:42 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 19 Dec 2023 04:52:42 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 19 Dec 2023 04:52:42 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 19 Dec 2023 04:52:49 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Tue, 19 Dec 2023 04:52:49 GMT
WORKDIR /opt/emqx
# Tue, 19 Dec 2023 04:52:49 GMT
USER emqx
# Tue, 19 Dec 2023 04:52:49 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 19 Dec 2023 04:52:49 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 19 Dec 2023 04:52:49 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 19 Dec 2023 04:52:50 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 04:52:50 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b5a0d5c14ba9ece1eecd5137c468d9a123372b0af2ed2c8c4446137730c90e5b`  
		Last Modified: Tue, 19 Dec 2023 01:25:40 GMT  
		Size: 31.4 MB (31417873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81485be977d1d3fe94a5b66b3785b7655ef00b2f45fd07342cd68fc243ae806`  
		Last Modified: Tue, 19 Dec 2023 04:53:43 GMT  
		Size: 3.0 MB (2989650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b109779462b5f5d7c8711d702009c239196c4c3f39bc2ac0ad12eddea7610c`  
		Last Modified: Tue, 19 Dec 2023 04:53:42 GMT  
		Size: 4.1 KB (4112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:037cf5dcb5939ce87deb069609859b228c88a3d3d02ce507c670f0392b1a2327`  
		Last Modified: Tue, 19 Dec 2023 04:54:06 GMT  
		Size: 68.0 MB (67981259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44819c1978424924f86ea06aaeba5105688cf831384d43cb43c9281626d97dc9`  
		Last Modified: Tue, 19 Dec 2023 04:53:59 GMT  
		Size: 903.0 B  
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
$ docker pull emqx@sha256:13530879f2df7c6c232a6ee868d945f828819858683857bc16092bcb7c71398f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.1.6` - linux; amd64

```console
$ docker pull emqx@sha256:931c0dca953709b7c00a0d214231ff8f56128a3e346f02e7859a06725c64ea1f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102393797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbb9d702579271a58adf5cbd49a7259b37f9f9c9597d610b09a3d36c85b0d4a9`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:50 GMT
ADD file:bb44d67b03db8efaeb0c4171474f441d14ff35f328f13add32b289fca062fa2f in / 
# Tue, 19 Dec 2023 01:20:50 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:52:30 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:52:31 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 19 Dec 2023 04:52:42 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 19 Dec 2023 04:52:42 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 19 Dec 2023 04:52:42 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 19 Dec 2023 04:52:42 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 19 Dec 2023 04:52:49 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Tue, 19 Dec 2023 04:52:49 GMT
WORKDIR /opt/emqx
# Tue, 19 Dec 2023 04:52:49 GMT
USER emqx
# Tue, 19 Dec 2023 04:52:49 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 19 Dec 2023 04:52:49 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 19 Dec 2023 04:52:49 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 19 Dec 2023 04:52:50 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 04:52:50 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b5a0d5c14ba9ece1eecd5137c468d9a123372b0af2ed2c8c4446137730c90e5b`  
		Last Modified: Tue, 19 Dec 2023 01:25:40 GMT  
		Size: 31.4 MB (31417873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81485be977d1d3fe94a5b66b3785b7655ef00b2f45fd07342cd68fc243ae806`  
		Last Modified: Tue, 19 Dec 2023 04:53:43 GMT  
		Size: 3.0 MB (2989650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b109779462b5f5d7c8711d702009c239196c4c3f39bc2ac0ad12eddea7610c`  
		Last Modified: Tue, 19 Dec 2023 04:53:42 GMT  
		Size: 4.1 KB (4112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:037cf5dcb5939ce87deb069609859b228c88a3d3d02ce507c670f0392b1a2327`  
		Last Modified: Tue, 19 Dec 2023 04:54:06 GMT  
		Size: 68.0 MB (67981259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44819c1978424924f86ea06aaeba5105688cf831384d43cb43c9281626d97dc9`  
		Last Modified: Tue, 19 Dec 2023 04:53:59 GMT  
		Size: 903.0 B  
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
$ docker pull emqx@sha256:da0cad68c5ec03e56ca82db08d0cb95aee8e75200899d02bfad644464b0d46ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.2` - linux; amd64

```console
$ docker pull emqx@sha256:e876c8101026429cab210574ac2bd117511e1d53843361a77f58030df6099ba9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101165575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818b5c7436d0b8729dbf4b26ecd136ef3b2d04b4e5930822a7abcd359f9dac7c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:50 GMT
ADD file:bb44d67b03db8efaeb0c4171474f441d14ff35f328f13add32b289fca062fa2f in / 
# Tue, 19 Dec 2023 01:20:50 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:52:57 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:52:58 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 19 Dec 2023 04:52:58 GMT
ENV EMQX_VERSION=5.2.1
# Tue, 19 Dec 2023 04:52:58 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Tue, 19 Dec 2023 04:52:58 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Tue, 19 Dec 2023 04:52:58 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 19 Dec 2023 04:53:09 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Tue, 19 Dec 2023 04:53:09 GMT
WORKDIR /opt/emqx
# Tue, 19 Dec 2023 04:53:09 GMT
USER emqx
# Tue, 19 Dec 2023 04:53:10 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 19 Dec 2023 04:53:10 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 19 Dec 2023 04:53:10 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 19 Dec 2023 04:53:10 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 04:53:10 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b5a0d5c14ba9ece1eecd5137c468d9a123372b0af2ed2c8c4446137730c90e5b`  
		Last Modified: Tue, 19 Dec 2023 01:25:40 GMT  
		Size: 31.4 MB (31417873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b84215a53870bb5e99e78f157dbed531d5dbcab34bc7cfa9039dbb7b6e0b922`  
		Last Modified: Tue, 19 Dec 2023 04:54:14 GMT  
		Size: 1.6 MB (1631630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0882c638bbfdc7dc76a191bb343f9f4f048b8d6b9575553c138e6a64c56dab3`  
		Last Modified: Tue, 19 Dec 2023 04:54:14 GMT  
		Size: 4.1 KB (4113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13acbcf85d62dc5c3f01551b6f05db1bf332cbdd0e3f562d65ae7a3dbd360e0d`  
		Last Modified: Tue, 19 Dec 2023 04:54:21 GMT  
		Size: 68.1 MB (68111056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e7d6988b322b2c7a63a38b08de3fca5bd98ecf78c8798b32616697c6d967843`  
		Last Modified: Tue, 19 Dec 2023 04:54:14 GMT  
		Size: 903.0 B  
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
$ docker pull emqx@sha256:da0cad68c5ec03e56ca82db08d0cb95aee8e75200899d02bfad644464b0d46ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.2.1` - linux; amd64

```console
$ docker pull emqx@sha256:e876c8101026429cab210574ac2bd117511e1d53843361a77f58030df6099ba9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101165575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818b5c7436d0b8729dbf4b26ecd136ef3b2d04b4e5930822a7abcd359f9dac7c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:50 GMT
ADD file:bb44d67b03db8efaeb0c4171474f441d14ff35f328f13add32b289fca062fa2f in / 
# Tue, 19 Dec 2023 01:20:50 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:52:57 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:52:58 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 19 Dec 2023 04:52:58 GMT
ENV EMQX_VERSION=5.2.1
# Tue, 19 Dec 2023 04:52:58 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Tue, 19 Dec 2023 04:52:58 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Tue, 19 Dec 2023 04:52:58 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 19 Dec 2023 04:53:09 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Tue, 19 Dec 2023 04:53:09 GMT
WORKDIR /opt/emqx
# Tue, 19 Dec 2023 04:53:09 GMT
USER emqx
# Tue, 19 Dec 2023 04:53:10 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 19 Dec 2023 04:53:10 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 19 Dec 2023 04:53:10 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 19 Dec 2023 04:53:10 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 04:53:10 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b5a0d5c14ba9ece1eecd5137c468d9a123372b0af2ed2c8c4446137730c90e5b`  
		Last Modified: Tue, 19 Dec 2023 01:25:40 GMT  
		Size: 31.4 MB (31417873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b84215a53870bb5e99e78f157dbed531d5dbcab34bc7cfa9039dbb7b6e0b922`  
		Last Modified: Tue, 19 Dec 2023 04:54:14 GMT  
		Size: 1.6 MB (1631630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0882c638bbfdc7dc76a191bb343f9f4f048b8d6b9575553c138e6a64c56dab3`  
		Last Modified: Tue, 19 Dec 2023 04:54:14 GMT  
		Size: 4.1 KB (4113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13acbcf85d62dc5c3f01551b6f05db1bf332cbdd0e3f562d65ae7a3dbd360e0d`  
		Last Modified: Tue, 19 Dec 2023 04:54:21 GMT  
		Size: 68.1 MB (68111056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e7d6988b322b2c7a63a38b08de3fca5bd98ecf78c8798b32616697c6d967843`  
		Last Modified: Tue, 19 Dec 2023 04:54:14 GMT  
		Size: 903.0 B  
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
$ docker pull emqx@sha256:542a89ddad403cfe705c5a212c59343ee3b13f7e505bf3bf6fb401873afd8d40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.3` - linux; amd64

```console
$ docker pull emqx@sha256:3c82206aac1aaacb33b4dfbac7f02448a55e5f3053a585229fd2a027e44e8e96
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101780864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2318b222abc2a4ab5841d67867fb414afb31b74c577aeecea5b093627319b141`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:50 GMT
ADD file:bb44d67b03db8efaeb0c4171474f441d14ff35f328f13add32b289fca062fa2f in / 
# Tue, 19 Dec 2023 01:20:50 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:53:13 GMT
ENV EMQX_VERSION=5.3.2
# Tue, 19 Dec 2023 04:53:13 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Tue, 19 Dec 2023 04:53:13 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Tue, 19 Dec 2023 04:53:13 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 19 Dec 2023 04:53:27 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:53:27 GMT
WORKDIR /opt/emqx
# Tue, 19 Dec 2023 04:53:27 GMT
USER emqx
# Tue, 19 Dec 2023 04:53:27 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 19 Dec 2023 04:53:28 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 19 Dec 2023 04:53:28 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 19 Dec 2023 04:53:28 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 04:53:28 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b5a0d5c14ba9ece1eecd5137c468d9a123372b0af2ed2c8c4446137730c90e5b`  
		Last Modified: Tue, 19 Dec 2023 01:25:40 GMT  
		Size: 31.4 MB (31417873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c8584f03abcd8dc4f4e74091c8e788a0de343e4e28e45ce61f5c8e7fa8f21f`  
		Last Modified: Tue, 19 Dec 2023 04:54:37 GMT  
		Size: 70.4 MB (70362088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3ad325587982cabb9a450034ff1c3634132a7dd6fe384135965a76c9761f21`  
		Last Modified: Tue, 19 Dec 2023 04:54:29 GMT  
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
$ docker pull emqx@sha256:542a89ddad403cfe705c5a212c59343ee3b13f7e505bf3bf6fb401873afd8d40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.3.2` - linux; amd64

```console
$ docker pull emqx@sha256:3c82206aac1aaacb33b4dfbac7f02448a55e5f3053a585229fd2a027e44e8e96
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101780864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2318b222abc2a4ab5841d67867fb414afb31b74c577aeecea5b093627319b141`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:50 GMT
ADD file:bb44d67b03db8efaeb0c4171474f441d14ff35f328f13add32b289fca062fa2f in / 
# Tue, 19 Dec 2023 01:20:50 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:53:13 GMT
ENV EMQX_VERSION=5.3.2
# Tue, 19 Dec 2023 04:53:13 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Tue, 19 Dec 2023 04:53:13 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Tue, 19 Dec 2023 04:53:13 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 19 Dec 2023 04:53:27 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:53:27 GMT
WORKDIR /opt/emqx
# Tue, 19 Dec 2023 04:53:27 GMT
USER emqx
# Tue, 19 Dec 2023 04:53:27 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 19 Dec 2023 04:53:28 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 19 Dec 2023 04:53:28 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 19 Dec 2023 04:53:28 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 04:53:28 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b5a0d5c14ba9ece1eecd5137c468d9a123372b0af2ed2c8c4446137730c90e5b`  
		Last Modified: Tue, 19 Dec 2023 01:25:40 GMT  
		Size: 31.4 MB (31417873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c8584f03abcd8dc4f4e74091c8e788a0de343e4e28e45ce61f5c8e7fa8f21f`  
		Last Modified: Tue, 19 Dec 2023 04:54:37 GMT  
		Size: 70.4 MB (70362088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3ad325587982cabb9a450034ff1c3634132a7dd6fe384135965a76c9761f21`  
		Last Modified: Tue, 19 Dec 2023 04:54:29 GMT  
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

## `emqx:latest`

```console
$ docker pull emqx@sha256:542a89ddad403cfe705c5a212c59343ee3b13f7e505bf3bf6fb401873afd8d40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:3c82206aac1aaacb33b4dfbac7f02448a55e5f3053a585229fd2a027e44e8e96
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101780864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2318b222abc2a4ab5841d67867fb414afb31b74c577aeecea5b093627319b141`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:50 GMT
ADD file:bb44d67b03db8efaeb0c4171474f441d14ff35f328f13add32b289fca062fa2f in / 
# Tue, 19 Dec 2023 01:20:50 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 04:53:13 GMT
ENV EMQX_VERSION=5.3.2
# Tue, 19 Dec 2023 04:53:13 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Tue, 19 Dec 2023 04:53:13 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Tue, 19 Dec 2023 04:53:13 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 19 Dec 2023 04:53:27 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 19 Dec 2023 04:53:27 GMT
WORKDIR /opt/emqx
# Tue, 19 Dec 2023 04:53:27 GMT
USER emqx
# Tue, 19 Dec 2023 04:53:27 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 19 Dec 2023 04:53:28 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 19 Dec 2023 04:53:28 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 19 Dec 2023 04:53:28 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 19 Dec 2023 04:53:28 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b5a0d5c14ba9ece1eecd5137c468d9a123372b0af2ed2c8c4446137730c90e5b`  
		Last Modified: Tue, 19 Dec 2023 01:25:40 GMT  
		Size: 31.4 MB (31417873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c8584f03abcd8dc4f4e74091c8e788a0de343e4e28e45ce61f5c8e7fa8f21f`  
		Last Modified: Tue, 19 Dec 2023 04:54:37 GMT  
		Size: 70.4 MB (70362088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3ad325587982cabb9a450034ff1c3634132a7dd6fe384135965a76c9761f21`  
		Last Modified: Tue, 19 Dec 2023 04:54:29 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

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
