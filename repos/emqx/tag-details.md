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
-	[`emqx:5.5.1`](#emqx551)
-	[`emqx:latest`](#emqxlatest)

## `emqx:5`

```console
$ docker pull emqx@sha256:c69f5e42f2372a226969239b072f7cf24196c48c666c46ce3825005c9aed86a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:986417b111b05a9530df6b0321ca4f725ae4d2d08abc45a44396dd47dd60c7f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121263691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1ec485420ee8a94a474647319ead59d8a210bf118c1ce87aa0b352d626849c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Sat, 09 Mar 2024 00:51:21 GMT
ENV EMQX_VERSION=5.5.1
# Sat, 09 Mar 2024 00:51:21 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Sat, 09 Mar 2024 00:51:21 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Sat, 09 Mar 2024 00:51:21 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Sat, 09 Mar 2024 00:51:35 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 09 Mar 2024 00:51:35 GMT
WORKDIR /opt/emqx
# Sat, 09 Mar 2024 00:51:35 GMT
USER emqx
# Sat, 09 Mar 2024 00:51:35 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 09 Mar 2024 00:51:35 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Sat, 09 Mar 2024 00:51:36 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Sat, 09 Mar 2024 00:51:36 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 09 Mar 2024 00:51:36 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba48e43b8ff1ebfdbcb605830bf87ff84a8472fd12b6042a5d38b2dbc5e1600`  
		Last Modified: Sat, 09 Mar 2024 00:52:03 GMT  
		Size: 89.8 MB (89840231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31870e450147f7d21ff9bed96f482413360f1faf3be22ab505f006116ada381b`  
		Last Modified: Sat, 09 Mar 2024 00:51:53 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:6dc6d622ec278abd2b904dfbe33130852dee80d600dff8ac5465011c7f711ce3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116793031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666a03985bdfc8f2c3009c506bbae667ff17228891118fbf7057cba6a9c1db3f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:18:12 GMT
ENV EMQX_VERSION=5.5.1
# Tue, 12 Mar 2024 02:18:13 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Tue, 12 Mar 2024 02:18:13 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Tue, 12 Mar 2024 02:18:13 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 12 Mar 2024 02:18:25 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:18:26 GMT
WORKDIR /opt/emqx
# Tue, 12 Mar 2024 02:18:26 GMT
USER emqx
# Tue, 12 Mar 2024 02:18:26 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 12 Mar 2024 02:18:26 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 12 Mar 2024 02:18:26 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 12 Mar 2024 02:18:26 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 12 Mar 2024 02:18:26 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1603d62cd82c37a25b7da6dd41c8b719207bc6190676d655efc5eb3add42b690`  
		Last Modified: Tue, 12 Mar 2024 02:19:41 GMT  
		Size: 86.7 MB (86720881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750fb90a18d9689f67bf77251592a7a60d5b99945335c7d9bd010a043f1ce0ee`  
		Last Modified: Tue, 12 Mar 2024 02:19:33 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.1`

```console
$ docker pull emqx@sha256:e1128c972d82b0b71a051854a44911ed147b876950dcce22349d736242308bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.1` - linux; amd64

```console
$ docker pull emqx@sha256:27e1b15e0328347afa148586d67b662395a6b5a57207253dcfb602ce3c78478f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102396964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cd319d0ac04383b0eb741282f335c3c1b55a9b7400f3988455fff9a20e7cc49`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:23:33 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:23:34 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 13 Feb 2024 02:23:34 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 13 Feb 2024 02:23:34 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 13 Feb 2024 02:23:34 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 13 Feb 2024 02:23:34 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Feb 2024 02:23:41 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Tue, 13 Feb 2024 02:23:41 GMT
WORKDIR /opt/emqx
# Tue, 13 Feb 2024 02:23:41 GMT
USER emqx
# Tue, 13 Feb 2024 02:23:41 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Feb 2024 02:23:41 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 13 Feb 2024 02:23:41 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 13 Feb 2024 02:23:41 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Feb 2024 02:23:42 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d59f5e3ad4127e8bf1a46826862c24c95fb48a26d33954864de052b5d3d606`  
		Last Modified: Tue, 13 Feb 2024 02:25:21 GMT  
		Size: 3.0 MB (2988276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dee8b6d6f20261a3c282483754a1bab97b57a585f5d27e53d9cacef7bdfd27a`  
		Last Modified: Tue, 13 Feb 2024 02:25:20 GMT  
		Size: 4.1 KB (4110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f094671dd50c275aa9f2ae0af461be75d7a2568c392ba684ad52e3d6327228f`  
		Last Modified: Tue, 13 Feb 2024 02:25:27 GMT  
		Size: 68.0 MB (67981253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffae952ce64129f7fecba0a8ccd9457aaae41e5c10f4bbcc1e636868417f42ab`  
		Last Modified: Tue, 13 Feb 2024 02:25:20 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8430c3e61b2ce88fd1bf4c3d13013a0ff5ab1334b25c89e19aea8d7291d71a85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92705262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d4105a9afd5fa2b537ca291cc22add0fa514606aa521eda21a545a38589e253`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:17:15 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:17:15 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 12 Mar 2024 02:17:15 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 12 Mar 2024 02:17:15 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 12 Mar 2024 02:17:15 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 12 Mar 2024 02:17:16 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 12 Mar 2024 02:17:22 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Tue, 12 Mar 2024 02:17:22 GMT
WORKDIR /opt/emqx
# Tue, 12 Mar 2024 02:17:22 GMT
USER emqx
# Tue, 12 Mar 2024 02:17:22 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 12 Mar 2024 02:17:22 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 12 Mar 2024 02:17:23 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 12 Mar 2024 02:17:23 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 12 Mar 2024 02:17:23 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a62f034509794d0cf59e746308fc478c3a222b3f0be4cc504626f5b78c8b4fd`  
		Last Modified: Tue, 12 Mar 2024 02:18:39 GMT  
		Size: 3.0 MB (3004435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50ea762249680868d468b0e66c29c185fe47e7f113bda1519ac5a6f673c95bd`  
		Last Modified: Tue, 12 Mar 2024 02:18:39 GMT  
		Size: 4.1 KB (4112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf339c734d137af79597212523518989d1182f754a2275a118984f60f06a9f1`  
		Last Modified: Tue, 12 Mar 2024 02:18:44 GMT  
		Size: 59.6 MB (59624698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b69a662bfe25b7b221b62dbb20d8f9c9b493e77bb1bb34bc3d35142ab3766de`  
		Last Modified: Tue, 12 Mar 2024 02:18:39 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.1.6`

```console
$ docker pull emqx@sha256:e1128c972d82b0b71a051854a44911ed147b876950dcce22349d736242308bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.1.6` - linux; amd64

```console
$ docker pull emqx@sha256:27e1b15e0328347afa148586d67b662395a6b5a57207253dcfb602ce3c78478f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102396964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cd319d0ac04383b0eb741282f335c3c1b55a9b7400f3988455fff9a20e7cc49`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:23:33 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:23:34 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 13 Feb 2024 02:23:34 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 13 Feb 2024 02:23:34 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 13 Feb 2024 02:23:34 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 13 Feb 2024 02:23:34 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Feb 2024 02:23:41 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Tue, 13 Feb 2024 02:23:41 GMT
WORKDIR /opt/emqx
# Tue, 13 Feb 2024 02:23:41 GMT
USER emqx
# Tue, 13 Feb 2024 02:23:41 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Feb 2024 02:23:41 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 13 Feb 2024 02:23:41 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 13 Feb 2024 02:23:41 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Feb 2024 02:23:42 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d59f5e3ad4127e8bf1a46826862c24c95fb48a26d33954864de052b5d3d606`  
		Last Modified: Tue, 13 Feb 2024 02:25:21 GMT  
		Size: 3.0 MB (2988276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dee8b6d6f20261a3c282483754a1bab97b57a585f5d27e53d9cacef7bdfd27a`  
		Last Modified: Tue, 13 Feb 2024 02:25:20 GMT  
		Size: 4.1 KB (4110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f094671dd50c275aa9f2ae0af461be75d7a2568c392ba684ad52e3d6327228f`  
		Last Modified: Tue, 13 Feb 2024 02:25:27 GMT  
		Size: 68.0 MB (67981253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffae952ce64129f7fecba0a8ccd9457aaae41e5c10f4bbcc1e636868417f42ab`  
		Last Modified: Tue, 13 Feb 2024 02:25:20 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.1.6` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:8430c3e61b2ce88fd1bf4c3d13013a0ff5ab1334b25c89e19aea8d7291d71a85
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92705262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d4105a9afd5fa2b537ca291cc22add0fa514606aa521eda21a545a38589e253`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:17:15 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:17:15 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 12 Mar 2024 02:17:15 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 12 Mar 2024 02:17:15 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 12 Mar 2024 02:17:15 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 12 Mar 2024 02:17:16 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 12 Mar 2024 02:17:22 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Tue, 12 Mar 2024 02:17:22 GMT
WORKDIR /opt/emqx
# Tue, 12 Mar 2024 02:17:22 GMT
USER emqx
# Tue, 12 Mar 2024 02:17:22 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 12 Mar 2024 02:17:22 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 12 Mar 2024 02:17:23 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 12 Mar 2024 02:17:23 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 12 Mar 2024 02:17:23 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a62f034509794d0cf59e746308fc478c3a222b3f0be4cc504626f5b78c8b4fd`  
		Last Modified: Tue, 12 Mar 2024 02:18:39 GMT  
		Size: 3.0 MB (3004435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50ea762249680868d468b0e66c29c185fe47e7f113bda1519ac5a6f673c95bd`  
		Last Modified: Tue, 12 Mar 2024 02:18:39 GMT  
		Size: 4.1 KB (4112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf339c734d137af79597212523518989d1182f754a2275a118984f60f06a9f1`  
		Last Modified: Tue, 12 Mar 2024 02:18:44 GMT  
		Size: 59.6 MB (59624698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b69a662bfe25b7b221b62dbb20d8f9c9b493e77bb1bb34bc3d35142ab3766de`  
		Last Modified: Tue, 12 Mar 2024 02:18:39 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.2`

```console
$ docker pull emqx@sha256:99e036058499673a4c81c34ee0ea296d8c1e1699c0222ee1ae0dc49cd62e1af7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.2` - linux; amd64

```console
$ docker pull emqx@sha256:52d177b1bee11735e62e0f19cf5a7fd557aca4665401f505b5744ce9bb8c396d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101167049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818ff2a12aa0db6ae0ad9bd71377b4f2cf5a50efdbf8caefcea3cf10440d61a0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:23:52 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:23:53 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 13 Feb 2024 02:23:53 GMT
ENV EMQX_VERSION=5.2.1
# Tue, 13 Feb 2024 02:23:53 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Tue, 13 Feb 2024 02:23:53 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Tue, 13 Feb 2024 02:23:53 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Feb 2024 02:24:04 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Tue, 13 Feb 2024 02:24:04 GMT
WORKDIR /opt/emqx
# Tue, 13 Feb 2024 02:24:04 GMT
USER emqx
# Tue, 13 Feb 2024 02:24:04 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Feb 2024 02:24:04 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 13 Feb 2024 02:24:05 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 13 Feb 2024 02:24:05 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Feb 2024 02:24:05 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7ef7e1ce9db39369517983c6460afcd3f214ee563ff3305c1e6e3719746941`  
		Last Modified: Tue, 13 Feb 2024 02:25:37 GMT  
		Size: 1.6 MB (1629568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f9601062af3434ea8a28b7a23490803ec6479d84515cbb78bb101cf8a9929b`  
		Last Modified: Tue, 13 Feb 2024 02:25:36 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f63ee513434cc0f9a3f171dac0a96cfdf3acf763085104118deb4604b9a9ae`  
		Last Modified: Tue, 13 Feb 2024 02:25:43 GMT  
		Size: 68.1 MB (68110052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a41de839373de860841adf9e7f0821955219a4a4f7c918a4d576e1d8fd29570`  
		Last Modified: Tue, 13 Feb 2024 02:25:36 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:398bbf3d33870b3fd5e4c77e19c07f8fde2230e7b3d06237e82e29373f7c8a2f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91471273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1287aee122920357f487f9a6570138198110312049bd295f104226783618d190`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:17:30 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:17:30 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 12 Mar 2024 02:17:30 GMT
ENV EMQX_VERSION=5.2.1
# Tue, 12 Mar 2024 02:17:31 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Tue, 12 Mar 2024 02:17:31 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Tue, 12 Mar 2024 02:17:31 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 12 Mar 2024 02:17:39 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Tue, 12 Mar 2024 02:17:40 GMT
WORKDIR /opt/emqx
# Tue, 12 Mar 2024 02:17:40 GMT
USER emqx
# Tue, 12 Mar 2024 02:17:40 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 12 Mar 2024 02:17:40 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 12 Mar 2024 02:17:40 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 12 Mar 2024 02:17:40 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 12 Mar 2024 02:17:40 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007e069718125e27b2758a0a96ce61f99a6cd8e2ca503169bd4462afd919323a`  
		Last Modified: Tue, 12 Mar 2024 02:18:53 GMT  
		Size: 1.6 MB (1644126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab74df7146544658a70ea7f340fb296449ff02f8effc4328e9ef4b73eac0cf5`  
		Last Modified: Tue, 12 Mar 2024 02:18:52 GMT  
		Size: 4.1 KB (4114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f11560836f8b46ac6904429b51a75753f80984355ffdba1e432c1fb46aeb471`  
		Last Modified: Tue, 12 Mar 2024 02:18:57 GMT  
		Size: 59.8 MB (59751015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cf4b35331a0aad71e1b5d388f5df6be66a567c7ce1af6009fd06176431ceea`  
		Last Modified: Tue, 12 Mar 2024 02:18:52 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.2.1`

```console
$ docker pull emqx@sha256:99e036058499673a4c81c34ee0ea296d8c1e1699c0222ee1ae0dc49cd62e1af7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.2.1` - linux; amd64

```console
$ docker pull emqx@sha256:52d177b1bee11735e62e0f19cf5a7fd557aca4665401f505b5744ce9bb8c396d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101167049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818ff2a12aa0db6ae0ad9bd71377b4f2cf5a50efdbf8caefcea3cf10440d61a0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:23:52 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:23:53 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 13 Feb 2024 02:23:53 GMT
ENV EMQX_VERSION=5.2.1
# Tue, 13 Feb 2024 02:23:53 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Tue, 13 Feb 2024 02:23:53 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Tue, 13 Feb 2024 02:23:53 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Feb 2024 02:24:04 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Tue, 13 Feb 2024 02:24:04 GMT
WORKDIR /opt/emqx
# Tue, 13 Feb 2024 02:24:04 GMT
USER emqx
# Tue, 13 Feb 2024 02:24:04 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Feb 2024 02:24:04 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 13 Feb 2024 02:24:05 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 13 Feb 2024 02:24:05 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Feb 2024 02:24:05 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7ef7e1ce9db39369517983c6460afcd3f214ee563ff3305c1e6e3719746941`  
		Last Modified: Tue, 13 Feb 2024 02:25:37 GMT  
		Size: 1.6 MB (1629568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f9601062af3434ea8a28b7a23490803ec6479d84515cbb78bb101cf8a9929b`  
		Last Modified: Tue, 13 Feb 2024 02:25:36 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f63ee513434cc0f9a3f171dac0a96cfdf3acf763085104118deb4604b9a9ae`  
		Last Modified: Tue, 13 Feb 2024 02:25:43 GMT  
		Size: 68.1 MB (68110052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a41de839373de860841adf9e7f0821955219a4a4f7c918a4d576e1d8fd29570`  
		Last Modified: Tue, 13 Feb 2024 02:25:36 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.2.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:398bbf3d33870b3fd5e4c77e19c07f8fde2230e7b3d06237e82e29373f7c8a2f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91471273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1287aee122920357f487f9a6570138198110312049bd295f104226783618d190`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:17:30 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:17:30 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 12 Mar 2024 02:17:30 GMT
ENV EMQX_VERSION=5.2.1
# Tue, 12 Mar 2024 02:17:31 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Tue, 12 Mar 2024 02:17:31 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Tue, 12 Mar 2024 02:17:31 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 12 Mar 2024 02:17:39 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Tue, 12 Mar 2024 02:17:40 GMT
WORKDIR /opt/emqx
# Tue, 12 Mar 2024 02:17:40 GMT
USER emqx
# Tue, 12 Mar 2024 02:17:40 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 12 Mar 2024 02:17:40 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 12 Mar 2024 02:17:40 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 12 Mar 2024 02:17:40 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 12 Mar 2024 02:17:40 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007e069718125e27b2758a0a96ce61f99a6cd8e2ca503169bd4462afd919323a`  
		Last Modified: Tue, 12 Mar 2024 02:18:53 GMT  
		Size: 1.6 MB (1644126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ab74df7146544658a70ea7f340fb296449ff02f8effc4328e9ef4b73eac0cf5`  
		Last Modified: Tue, 12 Mar 2024 02:18:52 GMT  
		Size: 4.1 KB (4114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f11560836f8b46ac6904429b51a75753f80984355ffdba1e432c1fb46aeb471`  
		Last Modified: Tue, 12 Mar 2024 02:18:57 GMT  
		Size: 59.8 MB (59751015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36cf4b35331a0aad71e1b5d388f5df6be66a567c7ce1af6009fd06176431ceea`  
		Last Modified: Tue, 12 Mar 2024 02:18:52 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.3`

```console
$ docker pull emqx@sha256:46248a96d81e561c330e3424d91db35e49d7838116baf8eba7c77c856b5c80f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.3` - linux; amd64

```console
$ docker pull emqx@sha256:36d78cdcbca3bbcdac880ad3651b659313f025d83f21286d1a56bc312eb64a6b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101783166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd48eb6abeb368c3e2fe8868c7172c374197e77a413264d4465890eba550752c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:24:08 GMT
ENV EMQX_VERSION=5.3.2
# Tue, 13 Feb 2024 02:24:08 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Tue, 13 Feb 2024 02:24:08 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Tue, 13 Feb 2024 02:24:08 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Feb 2024 02:24:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:24:22 GMT
WORKDIR /opt/emqx
# Tue, 13 Feb 2024 02:24:22 GMT
USER emqx
# Tue, 13 Feb 2024 02:24:22 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Feb 2024 02:24:22 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 13 Feb 2024 02:24:22 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 13 Feb 2024 02:24:22 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Feb 2024 02:24:22 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e14f33ed671bdc4867b4043dc89f4eea00aac5dd206c552cc685af935aeab00`  
		Last Modified: Tue, 13 Feb 2024 02:26:00 GMT  
		Size: 70.4 MB (70359839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1674ab9e79f0214ebf73316b094c3d3cc21a18a5b6fd56e23a2c95b793d6c74`  
		Last Modified: Tue, 13 Feb 2024 02:25:52 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.3` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:31dabf0113b10ffdcdb086b244010e5f3e03d16fb158ca9440a4c1ddc020ae26
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92085829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cd7af769fb4ab0ad5c1d282d924618a80aa83a175d3488784ab31ee843b6c27`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:17:42 GMT
ENV EMQX_VERSION=5.3.2
# Tue, 12 Mar 2024 02:17:42 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Tue, 12 Mar 2024 02:17:43 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Tue, 12 Mar 2024 02:17:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 12 Mar 2024 02:17:53 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:17:54 GMT
WORKDIR /opt/emqx
# Tue, 12 Mar 2024 02:17:54 GMT
USER emqx
# Tue, 12 Mar 2024 02:17:54 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 12 Mar 2024 02:17:54 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 12 Mar 2024 02:17:54 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 12 Mar 2024 02:17:54 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 12 Mar 2024 02:17:54 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d507d8d999b67e3706a3998a931e8df2b4e659c45e84f8132fde441afb5d9b4b`  
		Last Modified: Tue, 12 Mar 2024 02:19:11 GMT  
		Size: 62.0 MB (62013812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ba97da2fe61af521c7c0fcdcd1b5ebdf21f3b3b254183b41920c86a71bfe43`  
		Last Modified: Tue, 12 Mar 2024 02:19:05 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.3.2`

```console
$ docker pull emqx@sha256:46248a96d81e561c330e3424d91db35e49d7838116baf8eba7c77c856b5c80f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.3.2` - linux; amd64

```console
$ docker pull emqx@sha256:36d78cdcbca3bbcdac880ad3651b659313f025d83f21286d1a56bc312eb64a6b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101783166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd48eb6abeb368c3e2fe8868c7172c374197e77a413264d4465890eba550752c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:24:08 GMT
ENV EMQX_VERSION=5.3.2
# Tue, 13 Feb 2024 02:24:08 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Tue, 13 Feb 2024 02:24:08 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Tue, 13 Feb 2024 02:24:08 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Feb 2024 02:24:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:24:22 GMT
WORKDIR /opt/emqx
# Tue, 13 Feb 2024 02:24:22 GMT
USER emqx
# Tue, 13 Feb 2024 02:24:22 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Feb 2024 02:24:22 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 13 Feb 2024 02:24:22 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 13 Feb 2024 02:24:22 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Feb 2024 02:24:22 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e14f33ed671bdc4867b4043dc89f4eea00aac5dd206c552cc685af935aeab00`  
		Last Modified: Tue, 13 Feb 2024 02:26:00 GMT  
		Size: 70.4 MB (70359839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1674ab9e79f0214ebf73316b094c3d3cc21a18a5b6fd56e23a2c95b793d6c74`  
		Last Modified: Tue, 13 Feb 2024 02:25:52 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.3.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:31dabf0113b10ffdcdb086b244010e5f3e03d16fb158ca9440a4c1ddc020ae26
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92085829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cd7af769fb4ab0ad5c1d282d924618a80aa83a175d3488784ab31ee843b6c27`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:17:42 GMT
ENV EMQX_VERSION=5.3.2
# Tue, 12 Mar 2024 02:17:42 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Tue, 12 Mar 2024 02:17:43 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Tue, 12 Mar 2024 02:17:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 12 Mar 2024 02:17:53 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:17:54 GMT
WORKDIR /opt/emqx
# Tue, 12 Mar 2024 02:17:54 GMT
USER emqx
# Tue, 12 Mar 2024 02:17:54 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 12 Mar 2024 02:17:54 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 12 Mar 2024 02:17:54 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 12 Mar 2024 02:17:54 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 12 Mar 2024 02:17:54 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d507d8d999b67e3706a3998a931e8df2b4e659c45e84f8132fde441afb5d9b4b`  
		Last Modified: Tue, 12 Mar 2024 02:19:11 GMT  
		Size: 62.0 MB (62013812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ba97da2fe61af521c7c0fcdcd1b5ebdf21f3b3b254183b41920c86a71bfe43`  
		Last Modified: Tue, 12 Mar 2024 02:19:05 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.4`

```console
$ docker pull emqx@sha256:bd1375b56a2514f3a5a19864303c3563bf808cc83a88d4e5eeee284a3a4dd5fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.4` - linux; amd64

```console
$ docker pull emqx@sha256:02b6c288b1f3d593d9e3fa1c7baf90f83d1c4b23c2f29fd599aa30c4bb519406
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118697990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:562e462575aab5fe61f7edb5bf29f7244e20851363e3dec61e5cb4d274289a4e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:24:28 GMT
ENV EMQX_VERSION=5.4.1
# Tue, 13 Feb 2024 02:24:28 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Tue, 13 Feb 2024 02:24:28 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Tue, 13 Feb 2024 02:24:28 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Feb 2024 02:24:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:24:44 GMT
WORKDIR /opt/emqx
# Tue, 13 Feb 2024 02:24:44 GMT
USER emqx
# Tue, 13 Feb 2024 02:24:44 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Feb 2024 02:24:44 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 13 Feb 2024 02:24:44 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 13 Feb 2024 02:24:44 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Feb 2024 02:24:44 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d677913e15d6fca6736415f3043c0986a509537aa047a7e8929874e5f76015`  
		Last Modified: Tue, 13 Feb 2024 02:26:18 GMT  
		Size: 87.3 MB (87274666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd80467156a42acc28f13bfb82b4147c14d45d42535fd8078b4b2ea47c09d55`  
		Last Modified: Tue, 13 Feb 2024 02:26:09 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:406d2f762d702345233baa09527fa4cb16fc38514e1704d5bbd0982f171494a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108481354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b702434caf6e8f7c9e7394346117e87d0dfba37ad9ffe545ea9ec29c12a21f0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:17:56 GMT
ENV EMQX_VERSION=5.4.1
# Tue, 12 Mar 2024 02:17:56 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Tue, 12 Mar 2024 02:17:56 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Tue, 12 Mar 2024 02:17:56 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 12 Mar 2024 02:18:08 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:18:09 GMT
WORKDIR /opt/emqx
# Tue, 12 Mar 2024 02:18:09 GMT
USER emqx
# Tue, 12 Mar 2024 02:18:09 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 12 Mar 2024 02:18:09 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 12 Mar 2024 02:18:09 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 12 Mar 2024 02:18:09 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 12 Mar 2024 02:18:09 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39cd1c48a9c9547261516981126f8f085bc01c935c29d9f09722edd40ade60fa`  
		Last Modified: Tue, 12 Mar 2024 02:19:26 GMT  
		Size: 78.4 MB (78409337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7af450392d45a0ba0b181eb6ac29cb43ce2d0aaa5b7284045806e4ad27b5bd3`  
		Last Modified: Tue, 12 Mar 2024 02:19:19 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.4.1`

```console
$ docker pull emqx@sha256:bd1375b56a2514f3a5a19864303c3563bf808cc83a88d4e5eeee284a3a4dd5fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.4.1` - linux; amd64

```console
$ docker pull emqx@sha256:02b6c288b1f3d593d9e3fa1c7baf90f83d1c4b23c2f29fd599aa30c4bb519406
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118697990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:562e462575aab5fe61f7edb5bf29f7244e20851363e3dec61e5cb4d274289a4e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:24:28 GMT
ENV EMQX_VERSION=5.4.1
# Tue, 13 Feb 2024 02:24:28 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Tue, 13 Feb 2024 02:24:28 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Tue, 13 Feb 2024 02:24:28 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Feb 2024 02:24:43 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:24:44 GMT
WORKDIR /opt/emqx
# Tue, 13 Feb 2024 02:24:44 GMT
USER emqx
# Tue, 13 Feb 2024 02:24:44 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Feb 2024 02:24:44 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 13 Feb 2024 02:24:44 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 13 Feb 2024 02:24:44 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Feb 2024 02:24:44 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d677913e15d6fca6736415f3043c0986a509537aa047a7e8929874e5f76015`  
		Last Modified: Tue, 13 Feb 2024 02:26:18 GMT  
		Size: 87.3 MB (87274666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbd80467156a42acc28f13bfb82b4147c14d45d42535fd8078b4b2ea47c09d55`  
		Last Modified: Tue, 13 Feb 2024 02:26:09 GMT  
		Size: 899.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.4.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:406d2f762d702345233baa09527fa4cb16fc38514e1704d5bbd0982f171494a4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108481354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b702434caf6e8f7c9e7394346117e87d0dfba37ad9ffe545ea9ec29c12a21f0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:17:56 GMT
ENV EMQX_VERSION=5.4.1
# Tue, 12 Mar 2024 02:17:56 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Tue, 12 Mar 2024 02:17:56 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Tue, 12 Mar 2024 02:17:56 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 12 Mar 2024 02:18:08 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:18:09 GMT
WORKDIR /opt/emqx
# Tue, 12 Mar 2024 02:18:09 GMT
USER emqx
# Tue, 12 Mar 2024 02:18:09 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 12 Mar 2024 02:18:09 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 12 Mar 2024 02:18:09 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 12 Mar 2024 02:18:09 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 12 Mar 2024 02:18:09 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39cd1c48a9c9547261516981126f8f085bc01c935c29d9f09722edd40ade60fa`  
		Last Modified: Tue, 12 Mar 2024 02:19:26 GMT  
		Size: 78.4 MB (78409337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7af450392d45a0ba0b181eb6ac29cb43ce2d0aaa5b7284045806e4ad27b5bd3`  
		Last Modified: Tue, 12 Mar 2024 02:19:19 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.5`

```console
$ docker pull emqx@sha256:c69f5e42f2372a226969239b072f7cf24196c48c666c46ce3825005c9aed86a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.5` - linux; amd64

```console
$ docker pull emqx@sha256:986417b111b05a9530df6b0321ca4f725ae4d2d08abc45a44396dd47dd60c7f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121263691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1ec485420ee8a94a474647319ead59d8a210bf118c1ce87aa0b352d626849c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Sat, 09 Mar 2024 00:51:21 GMT
ENV EMQX_VERSION=5.5.1
# Sat, 09 Mar 2024 00:51:21 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Sat, 09 Mar 2024 00:51:21 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Sat, 09 Mar 2024 00:51:21 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Sat, 09 Mar 2024 00:51:35 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 09 Mar 2024 00:51:35 GMT
WORKDIR /opt/emqx
# Sat, 09 Mar 2024 00:51:35 GMT
USER emqx
# Sat, 09 Mar 2024 00:51:35 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 09 Mar 2024 00:51:35 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Sat, 09 Mar 2024 00:51:36 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Sat, 09 Mar 2024 00:51:36 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 09 Mar 2024 00:51:36 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba48e43b8ff1ebfdbcb605830bf87ff84a8472fd12b6042a5d38b2dbc5e1600`  
		Last Modified: Sat, 09 Mar 2024 00:52:03 GMT  
		Size: 89.8 MB (89840231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31870e450147f7d21ff9bed96f482413360f1faf3be22ab505f006116ada381b`  
		Last Modified: Sat, 09 Mar 2024 00:51:53 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:6dc6d622ec278abd2b904dfbe33130852dee80d600dff8ac5465011c7f711ce3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116793031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666a03985bdfc8f2c3009c506bbae667ff17228891118fbf7057cba6a9c1db3f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:18:12 GMT
ENV EMQX_VERSION=5.5.1
# Tue, 12 Mar 2024 02:18:13 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Tue, 12 Mar 2024 02:18:13 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Tue, 12 Mar 2024 02:18:13 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 12 Mar 2024 02:18:25 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:18:26 GMT
WORKDIR /opt/emqx
# Tue, 12 Mar 2024 02:18:26 GMT
USER emqx
# Tue, 12 Mar 2024 02:18:26 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 12 Mar 2024 02:18:26 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 12 Mar 2024 02:18:26 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 12 Mar 2024 02:18:26 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 12 Mar 2024 02:18:26 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1603d62cd82c37a25b7da6dd41c8b719207bc6190676d655efc5eb3add42b690`  
		Last Modified: Tue, 12 Mar 2024 02:19:41 GMT  
		Size: 86.7 MB (86720881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750fb90a18d9689f67bf77251592a7a60d5b99945335c7d9bd010a043f1ce0ee`  
		Last Modified: Tue, 12 Mar 2024 02:19:33 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.5.1`

```console
$ docker pull emqx@sha256:c69f5e42f2372a226969239b072f7cf24196c48c666c46ce3825005c9aed86a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.5.1` - linux; amd64

```console
$ docker pull emqx@sha256:986417b111b05a9530df6b0321ca4f725ae4d2d08abc45a44396dd47dd60c7f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121263691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1ec485420ee8a94a474647319ead59d8a210bf118c1ce87aa0b352d626849c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Sat, 09 Mar 2024 00:51:21 GMT
ENV EMQX_VERSION=5.5.1
# Sat, 09 Mar 2024 00:51:21 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Sat, 09 Mar 2024 00:51:21 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Sat, 09 Mar 2024 00:51:21 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Sat, 09 Mar 2024 00:51:35 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 09 Mar 2024 00:51:35 GMT
WORKDIR /opt/emqx
# Sat, 09 Mar 2024 00:51:35 GMT
USER emqx
# Sat, 09 Mar 2024 00:51:35 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 09 Mar 2024 00:51:35 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Sat, 09 Mar 2024 00:51:36 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Sat, 09 Mar 2024 00:51:36 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 09 Mar 2024 00:51:36 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba48e43b8ff1ebfdbcb605830bf87ff84a8472fd12b6042a5d38b2dbc5e1600`  
		Last Modified: Sat, 09 Mar 2024 00:52:03 GMT  
		Size: 89.8 MB (89840231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31870e450147f7d21ff9bed96f482413360f1faf3be22ab505f006116ada381b`  
		Last Modified: Sat, 09 Mar 2024 00:51:53 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.5.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:6dc6d622ec278abd2b904dfbe33130852dee80d600dff8ac5465011c7f711ce3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116793031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666a03985bdfc8f2c3009c506bbae667ff17228891118fbf7057cba6a9c1db3f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:18:12 GMT
ENV EMQX_VERSION=5.5.1
# Tue, 12 Mar 2024 02:18:13 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Tue, 12 Mar 2024 02:18:13 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Tue, 12 Mar 2024 02:18:13 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 12 Mar 2024 02:18:25 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:18:26 GMT
WORKDIR /opt/emqx
# Tue, 12 Mar 2024 02:18:26 GMT
USER emqx
# Tue, 12 Mar 2024 02:18:26 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 12 Mar 2024 02:18:26 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 12 Mar 2024 02:18:26 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 12 Mar 2024 02:18:26 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 12 Mar 2024 02:18:26 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1603d62cd82c37a25b7da6dd41c8b719207bc6190676d655efc5eb3add42b690`  
		Last Modified: Tue, 12 Mar 2024 02:19:41 GMT  
		Size: 86.7 MB (86720881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750fb90a18d9689f67bf77251592a7a60d5b99945335c7d9bd010a043f1ce0ee`  
		Last Modified: Tue, 12 Mar 2024 02:19:33 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:latest`

```console
$ docker pull emqx@sha256:c69f5e42f2372a226969239b072f7cf24196c48c666c46ce3825005c9aed86a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:986417b111b05a9530df6b0321ca4f725ae4d2d08abc45a44396dd47dd60c7f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121263691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1ec485420ee8a94a474647319ead59d8a210bf118c1ce87aa0b352d626849c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:43 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Tue, 13 Feb 2024 00:37:44 GMT
CMD ["bash"]
# Sat, 09 Mar 2024 00:51:21 GMT
ENV EMQX_VERSION=5.5.1
# Sat, 09 Mar 2024 00:51:21 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Sat, 09 Mar 2024 00:51:21 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Sat, 09 Mar 2024 00:51:21 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Sat, 09 Mar 2024 00:51:35 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Sat, 09 Mar 2024 00:51:35 GMT
WORKDIR /opt/emqx
# Sat, 09 Mar 2024 00:51:35 GMT
USER emqx
# Sat, 09 Mar 2024 00:51:35 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Sat, 09 Mar 2024 00:51:35 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Sat, 09 Mar 2024 00:51:36 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Sat, 09 Mar 2024 00:51:36 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Sat, 09 Mar 2024 00:51:36 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba48e43b8ff1ebfdbcb605830bf87ff84a8472fd12b6042a5d38b2dbc5e1600`  
		Last Modified: Sat, 09 Mar 2024 00:52:03 GMT  
		Size: 89.8 MB (89840231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31870e450147f7d21ff9bed96f482413360f1faf3be22ab505f006116ada381b`  
		Last Modified: Sat, 09 Mar 2024 00:51:53 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:6dc6d622ec278abd2b904dfbe33130852dee80d600dff8ac5465011c7f711ce3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116793031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:666a03985bdfc8f2c3009c506bbae667ff17228891118fbf7057cba6a9c1db3f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:18:12 GMT
ENV EMQX_VERSION=5.5.1
# Tue, 12 Mar 2024 02:18:13 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Tue, 12 Mar 2024 02:18:13 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Tue, 12 Mar 2024 02:18:13 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 12 Mar 2024 02:18:25 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:18:26 GMT
WORKDIR /opt/emqx
# Tue, 12 Mar 2024 02:18:26 GMT
USER emqx
# Tue, 12 Mar 2024 02:18:26 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 12 Mar 2024 02:18:26 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 12 Mar 2024 02:18:26 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 12 Mar 2024 02:18:26 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 12 Mar 2024 02:18:26 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1603d62cd82c37a25b7da6dd41c8b719207bc6190676d655efc5eb3add42b690`  
		Last Modified: Tue, 12 Mar 2024 02:19:41 GMT  
		Size: 86.7 MB (86720881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750fb90a18d9689f67bf77251592a7a60d5b99945335c7d9bd010a043f1ce0ee`  
		Last Modified: Tue, 12 Mar 2024 02:19:33 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
