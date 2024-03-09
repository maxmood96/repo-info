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
$ docker pull emqx@sha256:cd2d3222c6c87c1a5eeacf88de9182db5a7ee4022ecff6acd77fae7c2da223e1
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
$ docker pull emqx@sha256:a86bc0c8d9e829d26de7ca175c3e8d8d55030b2bd37c9fbf64cd2f230b150fa6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116791097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316fc321c7c9d7a356a94d179428a4bad2016d9332fe72977bcc3135b1bb38b8`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:52:19 GMT
ENV EMQX_VERSION=5.5.0
# Tue, 13 Feb 2024 02:52:20 GMT
ENV AMD64_SHA256=31af6514bcd30cab68272e1ff9553f652520cf82afed8894b3c4fe0fae55da88
# Tue, 13 Feb 2024 02:52:20 GMT
ENV ARM64_SHA256=45f46c99ae9561aac13b25f909df6ac1f971d4ce4aa594ff3711a1c95e8d9d9e
# Tue, 13 Feb 2024 02:52:20 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Feb 2024 02:52:32 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:52:33 GMT
WORKDIR /opt/emqx
# Tue, 13 Feb 2024 02:52:33 GMT
USER emqx
# Tue, 13 Feb 2024 02:52:33 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Feb 2024 02:52:33 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 13 Feb 2024 02:52:33 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 13 Feb 2024 02:52:33 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Feb 2024 02:52:33 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac635ae7385224f3101500831ecaac23cba61776c61fe69e7afacdf12a4f974`  
		Last Modified: Tue, 13 Feb 2024 02:53:47 GMT  
		Size: 86.7 MB (86719119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c83163d34b32eec8ac4ed86c3837eff9cc7f407f90060bb8ed11738d98c1fd`  
		Last Modified: Tue, 13 Feb 2024 02:53:39 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.1`

```console
$ docker pull emqx@sha256:ab0f13c63986ce715ec9baeb5851b47f440dfb29d1fe8c02dbda809a9fcca1f1
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
$ docker pull emqx@sha256:39378ab9019eb7e408d045390ecd2b5745990f8b884525f66d4bc392201ae0ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92705270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b719d606980dcb455b6a724995c5f933f91024fe64effd68786f1d2b7f04184`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:51:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:51:25 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 13 Feb 2024 02:51:25 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 13 Feb 2024 02:51:25 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 13 Feb 2024 02:51:25 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 13 Feb 2024 02:51:25 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Feb 2024 02:51:30 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Tue, 13 Feb 2024 02:51:31 GMT
WORKDIR /opt/emqx
# Tue, 13 Feb 2024 02:51:31 GMT
USER emqx
# Tue, 13 Feb 2024 02:51:31 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Feb 2024 02:51:31 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 13 Feb 2024 02:51:31 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 13 Feb 2024 02:51:31 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Feb 2024 02:51:31 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec81ad80e4df95d407b43ed00a8b7fd0ab5332b43b91fe9a8d556bd5cfb2c367`  
		Last Modified: Tue, 13 Feb 2024 02:52:46 GMT  
		Size: 3.0 MB (3004494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133d55f4dc7dfb599a5e60df1e9bd4b4315452af87b2540e7207eb498a857fe1`  
		Last Modified: Tue, 13 Feb 2024 02:52:46 GMT  
		Size: 4.1 KB (4108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9df506ce52a6190b50d1ef03545abb40852c296c479ef13d26c3a19194c18a9`  
		Last Modified: Tue, 13 Feb 2024 02:52:51 GMT  
		Size: 59.6 MB (59624690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee2de44a5dd37c20e2541091445e612460d9f47301e63362e6ac9bec579061f`  
		Last Modified: Tue, 13 Feb 2024 02:52:46 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.1.6`

```console
$ docker pull emqx@sha256:ab0f13c63986ce715ec9baeb5851b47f440dfb29d1fe8c02dbda809a9fcca1f1
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
$ docker pull emqx@sha256:39378ab9019eb7e408d045390ecd2b5745990f8b884525f66d4bc392201ae0ea
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92705270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b719d606980dcb455b6a724995c5f933f91024fe64effd68786f1d2b7f04184`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:51:24 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:51:25 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 13 Feb 2024 02:51:25 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 13 Feb 2024 02:51:25 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 13 Feb 2024 02:51:25 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 13 Feb 2024 02:51:25 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Feb 2024 02:51:30 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Tue, 13 Feb 2024 02:51:31 GMT
WORKDIR /opt/emqx
# Tue, 13 Feb 2024 02:51:31 GMT
USER emqx
# Tue, 13 Feb 2024 02:51:31 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Feb 2024 02:51:31 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 13 Feb 2024 02:51:31 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 13 Feb 2024 02:51:31 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Feb 2024 02:51:31 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec81ad80e4df95d407b43ed00a8b7fd0ab5332b43b91fe9a8d556bd5cfb2c367`  
		Last Modified: Tue, 13 Feb 2024 02:52:46 GMT  
		Size: 3.0 MB (3004494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133d55f4dc7dfb599a5e60df1e9bd4b4315452af87b2540e7207eb498a857fe1`  
		Last Modified: Tue, 13 Feb 2024 02:52:46 GMT  
		Size: 4.1 KB (4108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9df506ce52a6190b50d1ef03545abb40852c296c479ef13d26c3a19194c18a9`  
		Last Modified: Tue, 13 Feb 2024 02:52:51 GMT  
		Size: 59.6 MB (59624690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee2de44a5dd37c20e2541091445e612460d9f47301e63362e6ac9bec579061f`  
		Last Modified: Tue, 13 Feb 2024 02:52:46 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.2`

```console
$ docker pull emqx@sha256:6b22626df3a61a30d9329f26b8c83fdd27e7af2046f5d32f627ad0567906a39e
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
$ docker pull emqx@sha256:d20ee06299ae2f507df9d482a6ee38afb2a0fd9f10b3eff3f78e7ed61aa040dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91471265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b3b24cfe3a9f73aabc51d0f2a972e7f50441d372d60d1d446a808d2c3c0285`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:51:37 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:51:38 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 13 Feb 2024 02:51:38 GMT
ENV EMQX_VERSION=5.2.1
# Tue, 13 Feb 2024 02:51:38 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Tue, 13 Feb 2024 02:51:38 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Tue, 13 Feb 2024 02:51:38 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Feb 2024 02:51:46 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Tue, 13 Feb 2024 02:51:47 GMT
WORKDIR /opt/emqx
# Tue, 13 Feb 2024 02:51:47 GMT
USER emqx
# Tue, 13 Feb 2024 02:51:47 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Feb 2024 02:51:47 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 13 Feb 2024 02:51:47 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 13 Feb 2024 02:51:47 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Feb 2024 02:51:47 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4960a5199746a1d6592df540d934e8ee37aa05b6a7ce2d749c099252d8e2b0`  
		Last Modified: Tue, 13 Feb 2024 02:52:59 GMT  
		Size: 1.6 MB (1644153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44ef446a0ae6a162676dbfa79c51fdd325e75d7dcc82417afc913c3cfb6684db`  
		Last Modified: Tue, 13 Feb 2024 02:52:59 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba44f58f4cbda9aa0731a4348860e44ebf90e804e9736573386e4cd470bdb1b1`  
		Last Modified: Tue, 13 Feb 2024 02:53:04 GMT  
		Size: 59.8 MB (59751024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:264b5d129c0074af77b80304e93c13635ab50bad38fdceff271ff19ed8436789`  
		Last Modified: Tue, 13 Feb 2024 02:52:59 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.2.1`

```console
$ docker pull emqx@sha256:6b22626df3a61a30d9329f26b8c83fdd27e7af2046f5d32f627ad0567906a39e
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
$ docker pull emqx@sha256:d20ee06299ae2f507df9d482a6ee38afb2a0fd9f10b3eff3f78e7ed61aa040dc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91471265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b3b24cfe3a9f73aabc51d0f2a972e7f50441d372d60d1d446a808d2c3c0285`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:51:37 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:51:38 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 13 Feb 2024 02:51:38 GMT
ENV EMQX_VERSION=5.2.1
# Tue, 13 Feb 2024 02:51:38 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Tue, 13 Feb 2024 02:51:38 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Tue, 13 Feb 2024 02:51:38 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Feb 2024 02:51:46 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Tue, 13 Feb 2024 02:51:47 GMT
WORKDIR /opt/emqx
# Tue, 13 Feb 2024 02:51:47 GMT
USER emqx
# Tue, 13 Feb 2024 02:51:47 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Feb 2024 02:51:47 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 13 Feb 2024 02:51:47 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 13 Feb 2024 02:51:47 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Feb 2024 02:51:47 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4960a5199746a1d6592df540d934e8ee37aa05b6a7ce2d749c099252d8e2b0`  
		Last Modified: Tue, 13 Feb 2024 02:52:59 GMT  
		Size: 1.6 MB (1644153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44ef446a0ae6a162676dbfa79c51fdd325e75d7dcc82417afc913c3cfb6684db`  
		Last Modified: Tue, 13 Feb 2024 02:52:59 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba44f58f4cbda9aa0731a4348860e44ebf90e804e9736573386e4cd470bdb1b1`  
		Last Modified: Tue, 13 Feb 2024 02:53:04 GMT  
		Size: 59.8 MB (59751024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:264b5d129c0074af77b80304e93c13635ab50bad38fdceff271ff19ed8436789`  
		Last Modified: Tue, 13 Feb 2024 02:52:59 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.3`

```console
$ docker pull emqx@sha256:e3cdcd6727037e4ac1c10cd9a8acd0c5486df3519eafc6af08f8e3916142ae4e
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
$ docker pull emqx@sha256:55b58c5797966a3ad0d1668c68bb0282f538fdb3882491e6d99b1ebbb0d4a11a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92085942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fea0cc9725c5b6c7ecb98c80c53abf3cae2c12736420c1fde71efdad54c419b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:51:49 GMT
ENV EMQX_VERSION=5.3.2
# Tue, 13 Feb 2024 02:51:50 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Tue, 13 Feb 2024 02:51:50 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Tue, 13 Feb 2024 02:51:50 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Feb 2024 02:52:01 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:52:01 GMT
WORKDIR /opt/emqx
# Tue, 13 Feb 2024 02:52:01 GMT
USER emqx
# Tue, 13 Feb 2024 02:52:01 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Feb 2024 02:52:01 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 13 Feb 2024 02:52:01 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 13 Feb 2024 02:52:01 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Feb 2024 02:52:01 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fede9e00676366d3c650da7284e9441f6b3505623b7ad34e870655f9e232803a`  
		Last Modified: Tue, 13 Feb 2024 02:53:16 GMT  
		Size: 62.0 MB (62013964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0176b38cfb18e3e5118697cfdc0ca8ad283559c72a4e79899cae2fbb7218f496`  
		Last Modified: Tue, 13 Feb 2024 02:53:11 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.3.2`

```console
$ docker pull emqx@sha256:e3cdcd6727037e4ac1c10cd9a8acd0c5486df3519eafc6af08f8e3916142ae4e
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
$ docker pull emqx@sha256:55b58c5797966a3ad0d1668c68bb0282f538fdb3882491e6d99b1ebbb0d4a11a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92085942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fea0cc9725c5b6c7ecb98c80c53abf3cae2c12736420c1fde71efdad54c419b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:51:49 GMT
ENV EMQX_VERSION=5.3.2
# Tue, 13 Feb 2024 02:51:50 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Tue, 13 Feb 2024 02:51:50 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Tue, 13 Feb 2024 02:51:50 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Feb 2024 02:52:01 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:52:01 GMT
WORKDIR /opt/emqx
# Tue, 13 Feb 2024 02:52:01 GMT
USER emqx
# Tue, 13 Feb 2024 02:52:01 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Feb 2024 02:52:01 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 13 Feb 2024 02:52:01 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 13 Feb 2024 02:52:01 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Feb 2024 02:52:01 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fede9e00676366d3c650da7284e9441f6b3505623b7ad34e870655f9e232803a`  
		Last Modified: Tue, 13 Feb 2024 02:53:16 GMT  
		Size: 62.0 MB (62013964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0176b38cfb18e3e5118697cfdc0ca8ad283559c72a4e79899cae2fbb7218f496`  
		Last Modified: Tue, 13 Feb 2024 02:53:11 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.4`

```console
$ docker pull emqx@sha256:7863b8f0d623b23f96e7a5cf47c9e2d9118fdc15bfefdaaead15e7438ca05f71
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
$ docker pull emqx@sha256:9e3b55e98bc5860083e69a2178e3e04399fbf83dcd5e2e3e38656be3ed6f3c03
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108481292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2acc318213c85e7c0383c4800c34d8a35d6c00ac7c265db5a7225efb92efe0c3`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:52:03 GMT
ENV EMQX_VERSION=5.4.1
# Tue, 13 Feb 2024 02:52:03 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Tue, 13 Feb 2024 02:52:03 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Tue, 13 Feb 2024 02:52:03 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Feb 2024 02:52:15 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:52:16 GMT
WORKDIR /opt/emqx
# Tue, 13 Feb 2024 02:52:16 GMT
USER emqx
# Tue, 13 Feb 2024 02:52:16 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Feb 2024 02:52:16 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 13 Feb 2024 02:52:16 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 13 Feb 2024 02:52:16 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Feb 2024 02:52:16 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24f1f0c2ca933a75b9c42f86481d5aac7202983e108822b1d8ad1980ad746a7`  
		Last Modified: Tue, 13 Feb 2024 02:53:31 GMT  
		Size: 78.4 MB (78409315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd24acee5b68e1315b7431f329771209d02564061263cf37eb47ec7384916b3`  
		Last Modified: Tue, 13 Feb 2024 02:53:24 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.4.1`

```console
$ docker pull emqx@sha256:7863b8f0d623b23f96e7a5cf47c9e2d9118fdc15bfefdaaead15e7438ca05f71
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
$ docker pull emqx@sha256:9e3b55e98bc5860083e69a2178e3e04399fbf83dcd5e2e3e38656be3ed6f3c03
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.5 MB (108481292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2acc318213c85e7c0383c4800c34d8a35d6c00ac7c265db5a7225efb92efe0c3`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:52:03 GMT
ENV EMQX_VERSION=5.4.1
# Tue, 13 Feb 2024 02:52:03 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Tue, 13 Feb 2024 02:52:03 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Tue, 13 Feb 2024 02:52:03 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Feb 2024 02:52:15 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:52:16 GMT
WORKDIR /opt/emqx
# Tue, 13 Feb 2024 02:52:16 GMT
USER emqx
# Tue, 13 Feb 2024 02:52:16 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Feb 2024 02:52:16 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 13 Feb 2024 02:52:16 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 13 Feb 2024 02:52:16 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Feb 2024 02:52:16 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24f1f0c2ca933a75b9c42f86481d5aac7202983e108822b1d8ad1980ad746a7`  
		Last Modified: Tue, 13 Feb 2024 02:53:31 GMT  
		Size: 78.4 MB (78409315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd24acee5b68e1315b7431f329771209d02564061263cf37eb47ec7384916b3`  
		Last Modified: Tue, 13 Feb 2024 02:53:24 GMT  
		Size: 900.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.5`

```console
$ docker pull emqx@sha256:cd2d3222c6c87c1a5eeacf88de9182db5a7ee4022ecff6acd77fae7c2da223e1
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
$ docker pull emqx@sha256:a86bc0c8d9e829d26de7ca175c3e8d8d55030b2bd37c9fbf64cd2f230b150fa6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116791097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316fc321c7c9d7a356a94d179428a4bad2016d9332fe72977bcc3135b1bb38b8`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:52:19 GMT
ENV EMQX_VERSION=5.5.0
# Tue, 13 Feb 2024 02:52:20 GMT
ENV AMD64_SHA256=31af6514bcd30cab68272e1ff9553f652520cf82afed8894b3c4fe0fae55da88
# Tue, 13 Feb 2024 02:52:20 GMT
ENV ARM64_SHA256=45f46c99ae9561aac13b25f909df6ac1f971d4ce4aa594ff3711a1c95e8d9d9e
# Tue, 13 Feb 2024 02:52:20 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Feb 2024 02:52:32 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:52:33 GMT
WORKDIR /opt/emqx
# Tue, 13 Feb 2024 02:52:33 GMT
USER emqx
# Tue, 13 Feb 2024 02:52:33 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Feb 2024 02:52:33 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 13 Feb 2024 02:52:33 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 13 Feb 2024 02:52:33 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Feb 2024 02:52:33 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac635ae7385224f3101500831ecaac23cba61776c61fe69e7afacdf12a4f974`  
		Last Modified: Tue, 13 Feb 2024 02:53:47 GMT  
		Size: 86.7 MB (86719119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c83163d34b32eec8ac4ed86c3837eff9cc7f407f90060bb8ed11738d98c1fd`  
		Last Modified: Tue, 13 Feb 2024 02:53:39 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.5.1`

```console
$ docker pull emqx@sha256:597ad9d2639e4d14cd80d704f6de533e98e17ab309df51cb9403b83b94ff07ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

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

## `emqx:latest`

```console
$ docker pull emqx@sha256:cd2d3222c6c87c1a5eeacf88de9182db5a7ee4022ecff6acd77fae7c2da223e1
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
$ docker pull emqx@sha256:a86bc0c8d9e829d26de7ca175c3e8d8d55030b2bd37c9fbf64cd2f230b150fa6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.8 MB (116791097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316fc321c7c9d7a356a94d179428a4bad2016d9332fe72977bcc3135b1bb38b8`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:34 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Tue, 13 Feb 2024 00:41:35 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:52:19 GMT
ENV EMQX_VERSION=5.5.0
# Tue, 13 Feb 2024 02:52:20 GMT
ENV AMD64_SHA256=31af6514bcd30cab68272e1ff9553f652520cf82afed8894b3c4fe0fae55da88
# Tue, 13 Feb 2024 02:52:20 GMT
ENV ARM64_SHA256=45f46c99ae9561aac13b25f909df6ac1f971d4ce4aa594ff3711a1c95e8d9d9e
# Tue, 13 Feb 2024 02:52:20 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 13 Feb 2024 02:52:32 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 02:52:33 GMT
WORKDIR /opt/emqx
# Tue, 13 Feb 2024 02:52:33 GMT
USER emqx
# Tue, 13 Feb 2024 02:52:33 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 13 Feb 2024 02:52:33 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 13 Feb 2024 02:52:33 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 13 Feb 2024 02:52:33 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 13 Feb 2024 02:52:33 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac635ae7385224f3101500831ecaac23cba61776c61fe69e7afacdf12a4f974`  
		Last Modified: Tue, 13 Feb 2024 02:53:47 GMT  
		Size: 86.7 MB (86719119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c83163d34b32eec8ac4ed86c3837eff9cc7f407f90060bb8ed11738d98c1fd`  
		Last Modified: Tue, 13 Feb 2024 02:53:39 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
