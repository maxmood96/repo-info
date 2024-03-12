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
$ docker pull emqx@sha256:bb68eaf2012855cba2e56be831ce733baf84ce091354a8c5c82b147d92aea15d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:e11294885644f3917fd91f5a0ed449d81b0875be83e98ed498aeed4e19025a24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121263937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9772536c9ef3424c9b1eacbe5a14ffcb65e505f1dd193f0007d832337dd771f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:50:42 GMT
ENV EMQX_VERSION=5.5.1
# Tue, 12 Mar 2024 06:50:42 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Tue, 12 Mar 2024 06:50:42 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Tue, 12 Mar 2024 06:50:42 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 12 Mar 2024 06:50:56 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 06:50:57 GMT
WORKDIR /opt/emqx
# Tue, 12 Mar 2024 06:50:57 GMT
USER emqx
# Tue, 12 Mar 2024 06:50:57 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 12 Mar 2024 06:50:57 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 12 Mar 2024 06:50:57 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 12 Mar 2024 06:50:57 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 12 Mar 2024 06:50:57 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbc44956185b5067f6507fe8949ba06dd6ef72c6b2dff9b837acc715535444c`  
		Last Modified: Tue, 12 Mar 2024 06:52:25 GMT  
		Size: 89.8 MB (89840416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909a7a98341752dc7c382f07dcda2c405c4aa45be0179e30a96428e3a998b5cd`  
		Last Modified: Tue, 12 Mar 2024 06:52:16 GMT  
		Size: 1.0 KB (1032 bytes)  
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
$ docker pull emqx@sha256:4d722239755974fb17c1aba982a43fe389598483571d910cdb9302c2cf24917d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.1` - linux; amd64

```console
$ docker pull emqx@sha256:56ad863a608952e81eadc359681b0d77c4181894cd62b613b480a59693cfc78d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102397044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:162d856185c4d84ba5f54cfdae5a0e920ed6a0bc523ea8ef35037158acadd18c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:49:32 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 06:49:33 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 12 Mar 2024 06:49:33 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 12 Mar 2024 06:49:33 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 12 Mar 2024 06:49:33 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 12 Mar 2024 06:49:33 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 12 Mar 2024 06:49:40 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Tue, 12 Mar 2024 06:49:40 GMT
WORKDIR /opt/emqx
# Tue, 12 Mar 2024 06:49:40 GMT
USER emqx
# Tue, 12 Mar 2024 06:49:40 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 12 Mar 2024 06:49:40 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 12 Mar 2024 06:49:40 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 12 Mar 2024 06:49:40 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 12 Mar 2024 06:49:40 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6372e1095a5b3eaa1f6c645cf75ce664304d5b0ec2e18da30e7a97b78d3dd854`  
		Last Modified: Tue, 12 Mar 2024 06:51:14 GMT  
		Size: 3.0 MB (2988293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79d44309f3c7ca310182de031539a3eb68620d559d5b93d4764409cd2167475`  
		Last Modified: Tue, 12 Mar 2024 06:51:13 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493f3d4e47638a68c797f334ed96ca09e521207da40212b2cb7a3ea8fafca3fe`  
		Last Modified: Tue, 12 Mar 2024 06:51:21 GMT  
		Size: 68.0 MB (67981256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e5896a376f9ef0982cabbb2505a18cd8136d6d9411bc9b416fde51cf6f8d0a8`  
		Last Modified: Tue, 12 Mar 2024 06:51:13 GMT  
		Size: 902.0 B  
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
$ docker pull emqx@sha256:4d722239755974fb17c1aba982a43fe389598483571d910cdb9302c2cf24917d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.1.6` - linux; amd64

```console
$ docker pull emqx@sha256:56ad863a608952e81eadc359681b0d77c4181894cd62b613b480a59693cfc78d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102397044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:162d856185c4d84ba5f54cfdae5a0e920ed6a0bc523ea8ef35037158acadd18c`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:49:32 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 06:49:33 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 12 Mar 2024 06:49:33 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 12 Mar 2024 06:49:33 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 12 Mar 2024 06:49:33 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 12 Mar 2024 06:49:33 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 12 Mar 2024 06:49:40 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Tue, 12 Mar 2024 06:49:40 GMT
WORKDIR /opt/emqx
# Tue, 12 Mar 2024 06:49:40 GMT
USER emqx
# Tue, 12 Mar 2024 06:49:40 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 12 Mar 2024 06:49:40 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 12 Mar 2024 06:49:40 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 12 Mar 2024 06:49:40 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 12 Mar 2024 06:49:40 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6372e1095a5b3eaa1f6c645cf75ce664304d5b0ec2e18da30e7a97b78d3dd854`  
		Last Modified: Tue, 12 Mar 2024 06:51:14 GMT  
		Size: 3.0 MB (2988293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79d44309f3c7ca310182de031539a3eb68620d559d5b93d4764409cd2167475`  
		Last Modified: Tue, 12 Mar 2024 06:51:13 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493f3d4e47638a68c797f334ed96ca09e521207da40212b2cb7a3ea8fafca3fe`  
		Last Modified: Tue, 12 Mar 2024 06:51:21 GMT  
		Size: 68.0 MB (67981256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e5896a376f9ef0982cabbb2505a18cd8136d6d9411bc9b416fde51cf6f8d0a8`  
		Last Modified: Tue, 12 Mar 2024 06:51:13 GMT  
		Size: 902.0 B  
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
$ docker pull emqx@sha256:fa64dd7b2efee27c8d7e6239ad24a9d41718bba745507f998303688ad1cbf19d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.2` - linux; amd64

```console
$ docker pull emqx@sha256:ff70a67a029825e9c4b873b2e06e5e2690c4ff7ae04b89a75852bcf8732f1001
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101167133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f0115a5671cf2fd55e6887ffcf59e30d151c8b994c049973f382049e16e9879`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:49:48 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 06:49:49 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 12 Mar 2024 06:49:49 GMT
ENV EMQX_VERSION=5.2.1
# Tue, 12 Mar 2024 06:49:49 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Tue, 12 Mar 2024 06:49:49 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Tue, 12 Mar 2024 06:49:49 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 12 Mar 2024 06:49:59 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Tue, 12 Mar 2024 06:50:00 GMT
WORKDIR /opt/emqx
# Tue, 12 Mar 2024 06:50:00 GMT
USER emqx
# Tue, 12 Mar 2024 06:50:00 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 12 Mar 2024 06:50:00 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 12 Mar 2024 06:50:00 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 12 Mar 2024 06:50:00 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 12 Mar 2024 06:50:00 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bddedecabc29d8133587d4faafc1f23ac3c74dec47d327b7d3331fee66dfba0`  
		Last Modified: Tue, 12 Mar 2024 06:51:29 GMT  
		Size: 1.6 MB (1629593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cd7b448c1dcf393aba3809e64bbed9fd8eac3e809608044210dd6e4c31d1ed`  
		Last Modified: Tue, 12 Mar 2024 06:51:29 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7774560c5b95a97e76432313ec4eb1fd774415b0a468c353553a86550beb7c9`  
		Last Modified: Tue, 12 Mar 2024 06:51:36 GMT  
		Size: 68.1 MB (68110042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd80cf5f3d35d08aeebda7fef9276deff38a4f85c8c77976cec097510ae4905`  
		Last Modified: Tue, 12 Mar 2024 06:51:29 GMT  
		Size: 900.0 B  
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
$ docker pull emqx@sha256:fa64dd7b2efee27c8d7e6239ad24a9d41718bba745507f998303688ad1cbf19d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.2.1` - linux; amd64

```console
$ docker pull emqx@sha256:ff70a67a029825e9c4b873b2e06e5e2690c4ff7ae04b89a75852bcf8732f1001
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101167133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f0115a5671cf2fd55e6887ffcf59e30d151c8b994c049973f382049e16e9879`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:49:48 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 06:49:49 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 12 Mar 2024 06:49:49 GMT
ENV EMQX_VERSION=5.2.1
# Tue, 12 Mar 2024 06:49:49 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Tue, 12 Mar 2024 06:49:49 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Tue, 12 Mar 2024 06:49:49 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 12 Mar 2024 06:49:59 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Tue, 12 Mar 2024 06:50:00 GMT
WORKDIR /opt/emqx
# Tue, 12 Mar 2024 06:50:00 GMT
USER emqx
# Tue, 12 Mar 2024 06:50:00 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 12 Mar 2024 06:50:00 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 12 Mar 2024 06:50:00 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 12 Mar 2024 06:50:00 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 12 Mar 2024 06:50:00 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bddedecabc29d8133587d4faafc1f23ac3c74dec47d327b7d3331fee66dfba0`  
		Last Modified: Tue, 12 Mar 2024 06:51:29 GMT  
		Size: 1.6 MB (1629593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cd7b448c1dcf393aba3809e64bbed9fd8eac3e809608044210dd6e4c31d1ed`  
		Last Modified: Tue, 12 Mar 2024 06:51:29 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7774560c5b95a97e76432313ec4eb1fd774415b0a468c353553a86550beb7c9`  
		Last Modified: Tue, 12 Mar 2024 06:51:36 GMT  
		Size: 68.1 MB (68110042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd80cf5f3d35d08aeebda7fef9276deff38a4f85c8c77976cec097510ae4905`  
		Last Modified: Tue, 12 Mar 2024 06:51:29 GMT  
		Size: 900.0 B  
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
$ docker pull emqx@sha256:f7e9711e107ac2e53789fdc8885a5d7951babc812d8f72d0014ff94bc60c09ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.3` - linux; amd64

```console
$ docker pull emqx@sha256:9c7f3948cbbf6ddb4f1c10e5e5680aa2fa78ed34b85d4b80b70cbd5a9e448beb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101783345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c9a4e0dd81c5f20cb3000d03ffec64b33ccb851fbc5972267fbe70a6dce83f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:50:04 GMT
ENV EMQX_VERSION=5.3.2
# Tue, 12 Mar 2024 06:50:04 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Tue, 12 Mar 2024 06:50:04 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Tue, 12 Mar 2024 06:50:04 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 12 Mar 2024 06:50:17 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 06:50:17 GMT
WORKDIR /opt/emqx
# Tue, 12 Mar 2024 06:50:17 GMT
USER emqx
# Tue, 12 Mar 2024 06:50:17 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 12 Mar 2024 06:50:17 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 12 Mar 2024 06:50:18 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 12 Mar 2024 06:50:18 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 12 Mar 2024 06:50:18 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b70d27fb1571fb5dcf4407f4456a84ad0f372ca27b5301d070ee0847d6fb43`  
		Last Modified: Tue, 12 Mar 2024 06:51:51 GMT  
		Size: 70.4 MB (70359955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ce3d55d7c799ce8f73f151f66048417a9cdc56748abe04451c6f7ac5eefdb7`  
		Last Modified: Tue, 12 Mar 2024 06:51:44 GMT  
		Size: 901.0 B  
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
$ docker pull emqx@sha256:f7e9711e107ac2e53789fdc8885a5d7951babc812d8f72d0014ff94bc60c09ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.3.2` - linux; amd64

```console
$ docker pull emqx@sha256:9c7f3948cbbf6ddb4f1c10e5e5680aa2fa78ed34b85d4b80b70cbd5a9e448beb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101783345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c9a4e0dd81c5f20cb3000d03ffec64b33ccb851fbc5972267fbe70a6dce83f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:50:04 GMT
ENV EMQX_VERSION=5.3.2
# Tue, 12 Mar 2024 06:50:04 GMT
ENV AMD64_SHA256=d5948d4171f57e77756dd6c9eeb745c39e391e75aad3798fce445f44f5690be0
# Tue, 12 Mar 2024 06:50:04 GMT
ENV ARM64_SHA256=82b056bb1c1cd1f16e9d0719150fa8ac19c499d29563738bcd6984b3c395c6ac
# Tue, 12 Mar 2024 06:50:04 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 12 Mar 2024 06:50:17 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 06:50:17 GMT
WORKDIR /opt/emqx
# Tue, 12 Mar 2024 06:50:17 GMT
USER emqx
# Tue, 12 Mar 2024 06:50:17 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 12 Mar 2024 06:50:17 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 12 Mar 2024 06:50:18 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 12 Mar 2024 06:50:18 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 12 Mar 2024 06:50:18 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b70d27fb1571fb5dcf4407f4456a84ad0f372ca27b5301d070ee0847d6fb43`  
		Last Modified: Tue, 12 Mar 2024 06:51:51 GMT  
		Size: 70.4 MB (70359955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ce3d55d7c799ce8f73f151f66048417a9cdc56748abe04451c6f7ac5eefdb7`  
		Last Modified: Tue, 12 Mar 2024 06:51:44 GMT  
		Size: 901.0 B  
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
$ docker pull emqx@sha256:82d5a5d1dfcb275d69a467ba6e74c4323b4f1c25e9cb0cfb35983b3d4658937c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.4` - linux; amd64

```console
$ docker pull emqx@sha256:9e7e22ec0cd1d85ee4f8cacf599f6520c63cd490230e18ec68e9e3af4bf8902c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118698193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f257b2cb6311bb53b3fc9dbc5fb7b8660a0ef6284e09a12265b98ea3c4c3d1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:50:21 GMT
ENV EMQX_VERSION=5.4.1
# Tue, 12 Mar 2024 06:50:21 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Tue, 12 Mar 2024 06:50:21 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Tue, 12 Mar 2024 06:50:21 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 12 Mar 2024 06:50:35 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 06:50:36 GMT
WORKDIR /opt/emqx
# Tue, 12 Mar 2024 06:50:36 GMT
USER emqx
# Tue, 12 Mar 2024 06:50:36 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 12 Mar 2024 06:50:36 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 12 Mar 2024 06:50:36 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 12 Mar 2024 06:50:36 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 12 Mar 2024 06:50:36 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d8be43e72c24b0d873d58c3c3836a53ddbac70ca7cf5480e472b9e3573fe03`  
		Last Modified: Tue, 12 Mar 2024 06:52:07 GMT  
		Size: 87.3 MB (87274805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd99162d9a73eac32a770775c3a16f705efb2a308b96ebd3cbd00d44a51add47`  
		Last Modified: Tue, 12 Mar 2024 06:51:58 GMT  
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
$ docker pull emqx@sha256:82d5a5d1dfcb275d69a467ba6e74c4323b4f1c25e9cb0cfb35983b3d4658937c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.4.1` - linux; amd64

```console
$ docker pull emqx@sha256:9e7e22ec0cd1d85ee4f8cacf599f6520c63cd490230e18ec68e9e3af4bf8902c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118698193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f257b2cb6311bb53b3fc9dbc5fb7b8660a0ef6284e09a12265b98ea3c4c3d1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:50:21 GMT
ENV EMQX_VERSION=5.4.1
# Tue, 12 Mar 2024 06:50:21 GMT
ENV AMD64_SHA256=c2087651d72f17999f52d73ff22cd8f23dc5fa5db8b5a90a8bc4a1410b03affb
# Tue, 12 Mar 2024 06:50:21 GMT
ENV ARM64_SHA256=6c53a68ae907f7b4a3cdcd4dbee4f839b07853695ac1c039b51fd97d993073bc
# Tue, 12 Mar 2024 06:50:21 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 12 Mar 2024 06:50:35 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 06:50:36 GMT
WORKDIR /opt/emqx
# Tue, 12 Mar 2024 06:50:36 GMT
USER emqx
# Tue, 12 Mar 2024 06:50:36 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 12 Mar 2024 06:50:36 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 12 Mar 2024 06:50:36 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 12 Mar 2024 06:50:36 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 12 Mar 2024 06:50:36 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d8be43e72c24b0d873d58c3c3836a53ddbac70ca7cf5480e472b9e3573fe03`  
		Last Modified: Tue, 12 Mar 2024 06:52:07 GMT  
		Size: 87.3 MB (87274805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd99162d9a73eac32a770775c3a16f705efb2a308b96ebd3cbd00d44a51add47`  
		Last Modified: Tue, 12 Mar 2024 06:51:58 GMT  
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
$ docker pull emqx@sha256:bb68eaf2012855cba2e56be831ce733baf84ce091354a8c5c82b147d92aea15d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.5` - linux; amd64

```console
$ docker pull emqx@sha256:e11294885644f3917fd91f5a0ed449d81b0875be83e98ed498aeed4e19025a24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121263937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9772536c9ef3424c9b1eacbe5a14ffcb65e505f1dd193f0007d832337dd771f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:50:42 GMT
ENV EMQX_VERSION=5.5.1
# Tue, 12 Mar 2024 06:50:42 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Tue, 12 Mar 2024 06:50:42 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Tue, 12 Mar 2024 06:50:42 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 12 Mar 2024 06:50:56 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 06:50:57 GMT
WORKDIR /opt/emqx
# Tue, 12 Mar 2024 06:50:57 GMT
USER emqx
# Tue, 12 Mar 2024 06:50:57 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 12 Mar 2024 06:50:57 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 12 Mar 2024 06:50:57 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 12 Mar 2024 06:50:57 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 12 Mar 2024 06:50:57 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbc44956185b5067f6507fe8949ba06dd6ef72c6b2dff9b837acc715535444c`  
		Last Modified: Tue, 12 Mar 2024 06:52:25 GMT  
		Size: 89.8 MB (89840416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909a7a98341752dc7c382f07dcda2c405c4aa45be0179e30a96428e3a998b5cd`  
		Last Modified: Tue, 12 Mar 2024 06:52:16 GMT  
		Size: 1.0 KB (1032 bytes)  
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
$ docker pull emqx@sha256:bb68eaf2012855cba2e56be831ce733baf84ce091354a8c5c82b147d92aea15d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.5.1` - linux; amd64

```console
$ docker pull emqx@sha256:e11294885644f3917fd91f5a0ed449d81b0875be83e98ed498aeed4e19025a24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121263937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9772536c9ef3424c9b1eacbe5a14ffcb65e505f1dd193f0007d832337dd771f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:50:42 GMT
ENV EMQX_VERSION=5.5.1
# Tue, 12 Mar 2024 06:50:42 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Tue, 12 Mar 2024 06:50:42 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Tue, 12 Mar 2024 06:50:42 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 12 Mar 2024 06:50:56 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 06:50:57 GMT
WORKDIR /opt/emqx
# Tue, 12 Mar 2024 06:50:57 GMT
USER emqx
# Tue, 12 Mar 2024 06:50:57 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 12 Mar 2024 06:50:57 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 12 Mar 2024 06:50:57 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 12 Mar 2024 06:50:57 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 12 Mar 2024 06:50:57 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbc44956185b5067f6507fe8949ba06dd6ef72c6b2dff9b837acc715535444c`  
		Last Modified: Tue, 12 Mar 2024 06:52:25 GMT  
		Size: 89.8 MB (89840416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909a7a98341752dc7c382f07dcda2c405c4aa45be0179e30a96428e3a998b5cd`  
		Last Modified: Tue, 12 Mar 2024 06:52:16 GMT  
		Size: 1.0 KB (1032 bytes)  
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
$ docker pull emqx@sha256:bb68eaf2012855cba2e56be831ce733baf84ce091354a8c5c82b147d92aea15d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:e11294885644f3917fd91f5a0ed449d81b0875be83e98ed498aeed4e19025a24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121263937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9772536c9ef3424c9b1eacbe5a14ffcb65e505f1dd193f0007d832337dd771f`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:23 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Tue, 12 Mar 2024 01:21:23 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:50:42 GMT
ENV EMQX_VERSION=5.5.1
# Tue, 12 Mar 2024 06:50:42 GMT
ENV AMD64_SHA256=8bac2886987a632aab1c738aa3de28684b415d3b1e1f9489b458c819254673a6
# Tue, 12 Mar 2024 06:50:42 GMT
ENV ARM64_SHA256=8b962ad8beea50fb92dc0b93d2ab8a5064752147b70bbf46fd221bc4cc29c32d
# Tue, 12 Mar 2024 06:50:42 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 12 Mar 2024 06:50:56 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 06:50:57 GMT
WORKDIR /opt/emqx
# Tue, 12 Mar 2024 06:50:57 GMT
USER emqx
# Tue, 12 Mar 2024 06:50:57 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 12 Mar 2024 06:50:57 GMT
EXPOSE 18083 1883 4370 5369 8083 8084 8883
# Tue, 12 Mar 2024 06:50:57 GMT
COPY file:f0e3faa715cc7e845bbdf3b121a4a8bad40d65e5cef1fac9f1285fec250cedf2 in /usr/bin/ 
# Tue, 12 Mar 2024 06:50:57 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 12 Mar 2024 06:50:57 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbc44956185b5067f6507fe8949ba06dd6ef72c6b2dff9b837acc715535444c`  
		Last Modified: Tue, 12 Mar 2024 06:52:25 GMT  
		Size: 89.8 MB (89840416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909a7a98341752dc7c382f07dcda2c405c4aa45be0179e30a96428e3a998b5cd`  
		Last Modified: Tue, 12 Mar 2024 06:52:16 GMT  
		Size: 1.0 KB (1032 bytes)  
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
