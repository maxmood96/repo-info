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
$ docker pull emqx@sha256:719787ae27d124f0349b07e62ecccc59b11e825ac2620555e5d9530a465d69d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:73926e41cbdee6877681ca92d63676ea9c3f22ca72055f1d45bf464125cd724f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101375214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe76bd89a252320b8f64452c5f57ef2c8f6636351b503111fa64caf08a1eb65`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:37:59 GMT
ENV EMQX_VERSION=5.3.1
# Tue, 21 Nov 2023 12:37:59 GMT
ENV AMD64_SHA256=1d13906b397e86e7822133d27d124bd06d714002293480047d5ac0e22d193fe2
# Tue, 21 Nov 2023 12:37:59 GMT
ENV ARM64_SHA256=e8aae039125194e9edb5dfbe8cf5c3eaf0e4bd2b9610fa97118d344115e31d2c
# Tue, 21 Nov 2023 12:38:00 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 21 Nov 2023 12:38:14 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:38:14 GMT
WORKDIR /opt/emqx
# Tue, 21 Nov 2023 12:38:14 GMT
USER emqx
# Tue, 21 Nov 2023 12:38:14 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 21 Nov 2023 12:38:14 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 21 Nov 2023 12:38:15 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 21 Nov 2023 12:38:15 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 12:38:15 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dff673b8def2f974461d3a0ed9702247b2a458c19ca6294c3d359577423e3eb`  
		Last Modified: Tue, 21 Nov 2023 12:39:24 GMT  
		Size: 70.0 MB (69956489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f864f6a2e455c756bf1980a7cbc67901d21f45e96e2b2d3f20b04601aaebc473`  
		Last Modified: Tue, 21 Nov 2023 12:39:16 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:cc31195c6e287ea408fe373fc4965c5c1f7c4f429b4fa16527a995ff55aa6646
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91670521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1bc8d0c635b3a9d73f254605b5b742d7d7660cb2654f6408dd6e0013e62b9d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:15:08 GMT
ENV EMQX_VERSION=5.3.1
# Tue, 21 Nov 2023 10:15:08 GMT
ENV AMD64_SHA256=1d13906b397e86e7822133d27d124bd06d714002293480047d5ac0e22d193fe2
# Tue, 21 Nov 2023 10:15:08 GMT
ENV ARM64_SHA256=e8aae039125194e9edb5dfbe8cf5c3eaf0e4bd2b9610fa97118d344115e31d2c
# Tue, 21 Nov 2023 10:15:08 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 21 Nov 2023 10:15:20 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 10:15:21 GMT
WORKDIR /opt/emqx
# Tue, 21 Nov 2023 10:15:21 GMT
USER emqx
# Tue, 21 Nov 2023 10:15:21 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 21 Nov 2023 10:15:21 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 21 Nov 2023 10:15:21 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 21 Nov 2023 10:15:21 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 10:15:21 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56845559447cc0b30e74bba4e898455dc082c47b180e241fbe5fcf29b8aad6a6`  
		Last Modified: Tue, 21 Nov 2023 10:16:19 GMT  
		Size: 61.6 MB (61605495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920711b146ec99aae5eaa1087f4683ff0084f6680c2083921990b8cf776c907c`  
		Last Modified: Tue, 21 Nov 2023 10:16:14 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.0`

```console
$ docker pull emqx@sha256:d110ab51c7ed2001f181f13acba873e51f95429f741077f3b1582d4f091ae973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.0` - linux; amd64

```console
$ docker pull emqx@sha256:6fe7b5a61d5e4320db8287c9a013230cfd4a5cdae1e7437e778b23e96bfe43ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101983919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80fa8e7d034eb66313014e2b887ab389e9ce20a64dc681a1b06fa67d287ea982`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:37:09 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:37:10 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 21 Nov 2023 12:37:10 GMT
ENV EMQX_VERSION=5.0.26
# Tue, 21 Nov 2023 12:37:10 GMT
ENV AMD64_SHA256=00f954065fe7fd2f678f2e561578234240cc2cace49fb5cbb5aa7fb450825ffa
# Tue, 21 Nov 2023 12:37:10 GMT
ENV ARM64_SHA256=0b013f0b900e687c1ef3ed73bd6fef268b5492d12a3083ffd0d75c8e3935b4ae
# Tue, 21 Nov 2023 12:37:10 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 21 Nov 2023 12:37:17 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Tue, 21 Nov 2023 12:37:17 GMT
WORKDIR /opt/emqx
# Tue, 21 Nov 2023 12:37:17 GMT
USER emqx
# Tue, 21 Nov 2023 12:37:18 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 21 Nov 2023 12:37:18 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 21 Nov 2023 12:37:18 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 21 Nov 2023 12:37:18 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 12:37:18 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ba6149926bb71cc3428d146ebbfb25fe3cd9fd78ae4a5320bb846f241c4724`  
		Last Modified: Tue, 21 Nov 2023 12:38:29 GMT  
		Size: 3.0 MB (2989223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7666bea0f52506d7392a7adc94f57e936e141348d2514843de9b8f2563cca86a`  
		Last Modified: Tue, 21 Nov 2023 12:38:28 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d15c0598b55b018e71efa04904775cb25bf843c0d3256bba2c2739525bdbf00`  
		Last Modified: Tue, 21 Nov 2023 12:38:36 GMT  
		Size: 67.6 MB (67571866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f309247349fca52995351454b4bc75dbe15c0662cd5c4c3f1826e581415ea7c`  
		Last Modified: Tue, 21 Nov 2023 12:38:28 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.0` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:f89cb986db2e3730ed2f341e97fdf25884bbc0399d66661e71c113819b97a1f0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93063957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5458df38f77c0776658310f4b43c06d9ca8799009b2a531250034ad9c35ead08`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:14:26 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 10:14:26 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 21 Nov 2023 10:14:26 GMT
ENV EMQX_VERSION=5.0.26
# Tue, 21 Nov 2023 10:14:27 GMT
ENV AMD64_SHA256=00f954065fe7fd2f678f2e561578234240cc2cace49fb5cbb5aa7fb450825ffa
# Tue, 21 Nov 2023 10:14:27 GMT
ENV ARM64_SHA256=0b013f0b900e687c1ef3ed73bd6fef268b5492d12a3083ffd0d75c8e3935b4ae
# Tue, 21 Nov 2023 10:14:27 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 21 Nov 2023 10:14:33 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Tue, 21 Nov 2023 10:14:33 GMT
WORKDIR /opt/emqx
# Tue, 21 Nov 2023 10:14:33 GMT
USER emqx
# Tue, 21 Nov 2023 10:14:34 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 21 Nov 2023 10:14:34 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 21 Nov 2023 10:14:34 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 21 Nov 2023 10:14:34 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 10:14:34 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99616413d6a3c8f46bb1ad7c165f4270383e4f1ab373749dfdf465d4b28d3b1`  
		Last Modified: Tue, 21 Nov 2023 10:15:34 GMT  
		Size: 3.0 MB (3005422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8420832c2bddea6c0722407cc6b4af4dda88c4471574dc495c5c96172c87ee10`  
		Last Modified: Tue, 21 Nov 2023 10:15:33 GMT  
		Size: 4.1 KB (4107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f302690fb5d6c617334f8f427f64bcfa8a096ee5eb1989f9d538bc9b77a743dd`  
		Last Modified: Tue, 21 Nov 2023 10:15:38 GMT  
		Size: 60.0 MB (59989401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc44771791f703c2cbccc632e122959d6ad817cd51760ecbb1330754a534814`  
		Last Modified: Tue, 21 Nov 2023 10:15:33 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.0.26`

```console
$ docker pull emqx@sha256:d110ab51c7ed2001f181f13acba873e51f95429f741077f3b1582d4f091ae973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.0.26` - linux; amd64

```console
$ docker pull emqx@sha256:6fe7b5a61d5e4320db8287c9a013230cfd4a5cdae1e7437e778b23e96bfe43ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101983919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80fa8e7d034eb66313014e2b887ab389e9ce20a64dc681a1b06fa67d287ea982`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:37:09 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:37:10 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 21 Nov 2023 12:37:10 GMT
ENV EMQX_VERSION=5.0.26
# Tue, 21 Nov 2023 12:37:10 GMT
ENV AMD64_SHA256=00f954065fe7fd2f678f2e561578234240cc2cace49fb5cbb5aa7fb450825ffa
# Tue, 21 Nov 2023 12:37:10 GMT
ENV ARM64_SHA256=0b013f0b900e687c1ef3ed73bd6fef268b5492d12a3083ffd0d75c8e3935b4ae
# Tue, 21 Nov 2023 12:37:10 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 21 Nov 2023 12:37:17 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Tue, 21 Nov 2023 12:37:17 GMT
WORKDIR /opt/emqx
# Tue, 21 Nov 2023 12:37:17 GMT
USER emqx
# Tue, 21 Nov 2023 12:37:18 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 21 Nov 2023 12:37:18 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 21 Nov 2023 12:37:18 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 21 Nov 2023 12:37:18 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 12:37:18 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ba6149926bb71cc3428d146ebbfb25fe3cd9fd78ae4a5320bb846f241c4724`  
		Last Modified: Tue, 21 Nov 2023 12:38:29 GMT  
		Size: 3.0 MB (2989223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7666bea0f52506d7392a7adc94f57e936e141348d2514843de9b8f2563cca86a`  
		Last Modified: Tue, 21 Nov 2023 12:38:28 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d15c0598b55b018e71efa04904775cb25bf843c0d3256bba2c2739525bdbf00`  
		Last Modified: Tue, 21 Nov 2023 12:38:36 GMT  
		Size: 67.6 MB (67571866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f309247349fca52995351454b4bc75dbe15c0662cd5c4c3f1826e581415ea7c`  
		Last Modified: Tue, 21 Nov 2023 12:38:28 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.0.26` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:f89cb986db2e3730ed2f341e97fdf25884bbc0399d66661e71c113819b97a1f0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93063957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5458df38f77c0776658310f4b43c06d9ca8799009b2a531250034ad9c35ead08`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:14:26 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 10:14:26 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 21 Nov 2023 10:14:26 GMT
ENV EMQX_VERSION=5.0.26
# Tue, 21 Nov 2023 10:14:27 GMT
ENV AMD64_SHA256=00f954065fe7fd2f678f2e561578234240cc2cace49fb5cbb5aa7fb450825ffa
# Tue, 21 Nov 2023 10:14:27 GMT
ENV ARM64_SHA256=0b013f0b900e687c1ef3ed73bd6fef268b5492d12a3083ffd0d75c8e3935b4ae
# Tue, 21 Nov 2023 10:14:27 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 21 Nov 2023 10:14:33 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Tue, 21 Nov 2023 10:14:33 GMT
WORKDIR /opt/emqx
# Tue, 21 Nov 2023 10:14:33 GMT
USER emqx
# Tue, 21 Nov 2023 10:14:34 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 21 Nov 2023 10:14:34 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 21 Nov 2023 10:14:34 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 21 Nov 2023 10:14:34 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 10:14:34 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99616413d6a3c8f46bb1ad7c165f4270383e4f1ab373749dfdf465d4b28d3b1`  
		Last Modified: Tue, 21 Nov 2023 10:15:34 GMT  
		Size: 3.0 MB (3005422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8420832c2bddea6c0722407cc6b4af4dda88c4471574dc495c5c96172c87ee10`  
		Last Modified: Tue, 21 Nov 2023 10:15:33 GMT  
		Size: 4.1 KB (4107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f302690fb5d6c617334f8f427f64bcfa8a096ee5eb1989f9d538bc9b77a743dd`  
		Last Modified: Tue, 21 Nov 2023 10:15:38 GMT  
		Size: 60.0 MB (59989401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc44771791f703c2cbccc632e122959d6ad817cd51760ecbb1330754a534814`  
		Last Modified: Tue, 21 Nov 2023 10:15:33 GMT  
		Size: 904.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.1`

```console
$ docker pull emqx@sha256:b9ce573c9bdfe47f948fa40796532412cc4e4f096674e1e48cb90897bf6b480e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.1` - linux; amd64

```console
$ docker pull emqx@sha256:0894480c121adb56cbc09eae51d3cde178fe5f650e8c6942effe45154420c180
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102393305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e225172613e03738e60225029551c5798ba23b81c060a8fa3b3ac073d4394ed`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:37:09 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:37:10 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 21 Nov 2023 12:37:23 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 21 Nov 2023 12:37:23 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 21 Nov 2023 12:37:23 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 21 Nov 2023 12:37:23 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 21 Nov 2023 12:37:31 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Tue, 21 Nov 2023 12:37:32 GMT
WORKDIR /opt/emqx
# Tue, 21 Nov 2023 12:37:32 GMT
USER emqx
# Tue, 21 Nov 2023 12:37:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 21 Nov 2023 12:37:32 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 21 Nov 2023 12:37:32 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 21 Nov 2023 12:37:32 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 12:37:32 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ba6149926bb71cc3428d146ebbfb25fe3cd9fd78ae4a5320bb846f241c4724`  
		Last Modified: Tue, 21 Nov 2023 12:38:29 GMT  
		Size: 3.0 MB (2989223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7666bea0f52506d7392a7adc94f57e936e141348d2514843de9b8f2563cca86a`  
		Last Modified: Tue, 21 Nov 2023 12:38:28 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0feca574b243f420192db2433e3a0c091adac0c368ffb0f5fdcd6e3f45d1c868`  
		Last Modified: Tue, 21 Nov 2023 12:38:52 GMT  
		Size: 68.0 MB (67981252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb7e6f127ca53ae81b3e7291dd716efd9789233738e68b379af1fd16bf01539`  
		Last Modified: Tue, 21 Nov 2023 12:38:45 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:07b7a50e930af503db65e70abe86b609c8a15c4a86593445fdc56838e7baf6b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92699251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96763b8adea3608145048364450554f13f7cc6d66f31993b0311d8a3f4ae46c3`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:14:26 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 10:14:26 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 21 Nov 2023 10:14:37 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 21 Nov 2023 10:14:37 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 21 Nov 2023 10:14:37 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 21 Nov 2023 10:14:37 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 21 Nov 2023 10:14:44 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Tue, 21 Nov 2023 10:14:44 GMT
WORKDIR /opt/emqx
# Tue, 21 Nov 2023 10:14:45 GMT
USER emqx
# Tue, 21 Nov 2023 10:14:45 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 21 Nov 2023 10:14:45 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 21 Nov 2023 10:14:45 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 21 Nov 2023 10:14:45 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 10:14:45 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99616413d6a3c8f46bb1ad7c165f4270383e4f1ab373749dfdf465d4b28d3b1`  
		Last Modified: Tue, 21 Nov 2023 10:15:34 GMT  
		Size: 3.0 MB (3005422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8420832c2bddea6c0722407cc6b4af4dda88c4471574dc495c5c96172c87ee10`  
		Last Modified: Tue, 21 Nov 2023 10:15:33 GMT  
		Size: 4.1 KB (4107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6586f1107540b703740d06516743a869e77bf4834608d86df574bbd6a05c5c5`  
		Last Modified: Tue, 21 Nov 2023 10:15:51 GMT  
		Size: 59.6 MB (59624697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e41a453a4e01c0571463168487cc2f093f2dcb9c9b4a582708b8f3d09b4a884`  
		Last Modified: Tue, 21 Nov 2023 10:15:46 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.1.6`

```console
$ docker pull emqx@sha256:b9ce573c9bdfe47f948fa40796532412cc4e4f096674e1e48cb90897bf6b480e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.1.6` - linux; amd64

```console
$ docker pull emqx@sha256:0894480c121adb56cbc09eae51d3cde178fe5f650e8c6942effe45154420c180
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102393305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e225172613e03738e60225029551c5798ba23b81c060a8fa3b3ac073d4394ed`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:37:09 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:37:10 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 21 Nov 2023 12:37:23 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 21 Nov 2023 12:37:23 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 21 Nov 2023 12:37:23 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 21 Nov 2023 12:37:23 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 21 Nov 2023 12:37:31 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Tue, 21 Nov 2023 12:37:32 GMT
WORKDIR /opt/emqx
# Tue, 21 Nov 2023 12:37:32 GMT
USER emqx
# Tue, 21 Nov 2023 12:37:32 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 21 Nov 2023 12:37:32 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 21 Nov 2023 12:37:32 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 21 Nov 2023 12:37:32 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 12:37:32 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ba6149926bb71cc3428d146ebbfb25fe3cd9fd78ae4a5320bb846f241c4724`  
		Last Modified: Tue, 21 Nov 2023 12:38:29 GMT  
		Size: 3.0 MB (2989223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7666bea0f52506d7392a7adc94f57e936e141348d2514843de9b8f2563cca86a`  
		Last Modified: Tue, 21 Nov 2023 12:38:28 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0feca574b243f420192db2433e3a0c091adac0c368ffb0f5fdcd6e3f45d1c868`  
		Last Modified: Tue, 21 Nov 2023 12:38:52 GMT  
		Size: 68.0 MB (67981252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb7e6f127ca53ae81b3e7291dd716efd9789233738e68b379af1fd16bf01539`  
		Last Modified: Tue, 21 Nov 2023 12:38:45 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.1.6` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:07b7a50e930af503db65e70abe86b609c8a15c4a86593445fdc56838e7baf6b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92699251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96763b8adea3608145048364450554f13f7cc6d66f31993b0311d8a3f4ae46c3`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:14:26 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 10:14:26 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 21 Nov 2023 10:14:37 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 21 Nov 2023 10:14:37 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 21 Nov 2023 10:14:37 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 21 Nov 2023 10:14:37 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 21 Nov 2023 10:14:44 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Tue, 21 Nov 2023 10:14:44 GMT
WORKDIR /opt/emqx
# Tue, 21 Nov 2023 10:14:45 GMT
USER emqx
# Tue, 21 Nov 2023 10:14:45 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 21 Nov 2023 10:14:45 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 21 Nov 2023 10:14:45 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 21 Nov 2023 10:14:45 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 10:14:45 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99616413d6a3c8f46bb1ad7c165f4270383e4f1ab373749dfdf465d4b28d3b1`  
		Last Modified: Tue, 21 Nov 2023 10:15:34 GMT  
		Size: 3.0 MB (3005422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8420832c2bddea6c0722407cc6b4af4dda88c4471574dc495c5c96172c87ee10`  
		Last Modified: Tue, 21 Nov 2023 10:15:33 GMT  
		Size: 4.1 KB (4107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6586f1107540b703740d06516743a869e77bf4834608d86df574bbd6a05c5c5`  
		Last Modified: Tue, 21 Nov 2023 10:15:51 GMT  
		Size: 59.6 MB (59624697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e41a453a4e01c0571463168487cc2f093f2dcb9c9b4a582708b8f3d09b4a884`  
		Last Modified: Tue, 21 Nov 2023 10:15:46 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.2`

```console
$ docker pull emqx@sha256:2073cde45741ddad45fe93280c60477ba6caa8a363e1a7984dde89609a53776c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.2` - linux; amd64

```console
$ docker pull emqx@sha256:4e8ae00734b55afc7758b71f3814a35abfe41e99488ea17de9a457cb494ea12c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101165442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25bf6a3ea80e6eea74745458f3007ebca4b89d0f410a07dcf4333f2701600b0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:37:40 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:37:40 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 21 Nov 2023 12:37:40 GMT
ENV EMQX_VERSION=5.2.1
# Tue, 21 Nov 2023 12:37:40 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Tue, 21 Nov 2023 12:37:41 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Tue, 21 Nov 2023 12:37:41 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 21 Nov 2023 12:37:52 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Tue, 21 Nov 2023 12:37:53 GMT
WORKDIR /opt/emqx
# Tue, 21 Nov 2023 12:37:53 GMT
USER emqx
# Tue, 21 Nov 2023 12:37:53 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 21 Nov 2023 12:37:53 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 21 Nov 2023 12:37:53 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 21 Nov 2023 12:37:53 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 12:37:53 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ae73677a72916cf285d9d11d196f1bf9cda397defac20ee73910b23fe55f83`  
		Last Modified: Tue, 21 Nov 2023 12:39:01 GMT  
		Size: 1.6 MB (1631574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e4c76aa085fe7dc32d9d367c521b0ec134e1188a2c064ab427fbb3ccee055d`  
		Last Modified: Tue, 21 Nov 2023 12:39:00 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f468f093cc34406cdee950c4242d7525827be07ac8155939377dc08676a05fd`  
		Last Modified: Tue, 21 Nov 2023 12:39:08 GMT  
		Size: 68.1 MB (68111038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad37736e3ad028f3246bc842764449d6a482158cd31a4d3bc6083f5211f40511`  
		Last Modified: Tue, 21 Nov 2023 12:39:01 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.2` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:338220eed5be331fe32fecf7cbfc097dd13e8bc97cf5942bf85e76ea11cd50e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91466707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab639b8c2c012166fb7a3cf4bf203a500068d017d8e5c02e0e845526f1434168`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:14:52 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 10:14:52 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 21 Nov 2023 10:14:52 GMT
ENV EMQX_VERSION=5.2.1
# Tue, 21 Nov 2023 10:14:53 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Tue, 21 Nov 2023 10:14:53 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Tue, 21 Nov 2023 10:14:53 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 21 Nov 2023 10:15:02 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Tue, 21 Nov 2023 10:15:03 GMT
WORKDIR /opt/emqx
# Tue, 21 Nov 2023 10:15:03 GMT
USER emqx
# Tue, 21 Nov 2023 10:15:03 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 21 Nov 2023 10:15:03 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 21 Nov 2023 10:15:03 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 21 Nov 2023 10:15:03 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 10:15:03 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9faf19c7b902a213dee90b0aec91abaf87bb600d398f3290b8970ece4baa5d0c`  
		Last Modified: Tue, 21 Nov 2023 10:16:00 GMT  
		Size: 1.6 MB (1645840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4370357dc913804e45c84e36d32603b076cef45d22699d6af105f5e53beab8`  
		Last Modified: Tue, 21 Nov 2023 10:16:00 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366a91635bf670cf46d7ccd8b9e31152e2ca016c0db782e8e151ca685ebfbeac`  
		Last Modified: Tue, 21 Nov 2023 10:16:05 GMT  
		Size: 59.8 MB (59751733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b2dddaacaf7357386cb7ab9c5d0557409e70080e99a04fad28dde0d5538cb6`  
		Last Modified: Tue, 21 Nov 2023 10:16:00 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.2.1`

```console
$ docker pull emqx@sha256:2073cde45741ddad45fe93280c60477ba6caa8a363e1a7984dde89609a53776c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.2.1` - linux; amd64

```console
$ docker pull emqx@sha256:4e8ae00734b55afc7758b71f3814a35abfe41e99488ea17de9a457cb494ea12c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101165442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a25bf6a3ea80e6eea74745458f3007ebca4b89d0f410a07dcf4333f2701600b0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:37:40 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:37:40 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 21 Nov 2023 12:37:40 GMT
ENV EMQX_VERSION=5.2.1
# Tue, 21 Nov 2023 12:37:40 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Tue, 21 Nov 2023 12:37:41 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Tue, 21 Nov 2023 12:37:41 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 21 Nov 2023 12:37:52 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Tue, 21 Nov 2023 12:37:53 GMT
WORKDIR /opt/emqx
# Tue, 21 Nov 2023 12:37:53 GMT
USER emqx
# Tue, 21 Nov 2023 12:37:53 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 21 Nov 2023 12:37:53 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 21 Nov 2023 12:37:53 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 21 Nov 2023 12:37:53 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 12:37:53 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ae73677a72916cf285d9d11d196f1bf9cda397defac20ee73910b23fe55f83`  
		Last Modified: Tue, 21 Nov 2023 12:39:01 GMT  
		Size: 1.6 MB (1631574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e4c76aa085fe7dc32d9d367c521b0ec134e1188a2c064ab427fbb3ccee055d`  
		Last Modified: Tue, 21 Nov 2023 12:39:00 GMT  
		Size: 4.1 KB (4104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f468f093cc34406cdee950c4242d7525827be07ac8155939377dc08676a05fd`  
		Last Modified: Tue, 21 Nov 2023 12:39:08 GMT  
		Size: 68.1 MB (68111038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad37736e3ad028f3246bc842764449d6a482158cd31a4d3bc6083f5211f40511`  
		Last Modified: Tue, 21 Nov 2023 12:39:01 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.2.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:338220eed5be331fe32fecf7cbfc097dd13e8bc97cf5942bf85e76ea11cd50e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91466707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab639b8c2c012166fb7a3cf4bf203a500068d017d8e5c02e0e845526f1434168`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:14:52 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 10:14:52 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 21 Nov 2023 10:14:52 GMT
ENV EMQX_VERSION=5.2.1
# Tue, 21 Nov 2023 10:14:53 GMT
ENV AMD64_SHA256=359a12811e5e6725e4269d9484abd348effdde35c0f2af1f5b63cae790c73020
# Tue, 21 Nov 2023 10:14:53 GMT
ENV ARM64_SHA256=2e0a3e0b33669c9b6da488970a2f92d08d7bd0824295822b205b83461ba4728d
# Tue, 21 Nov 2023 10:14:53 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 21 Nov 2023 10:15:02 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl;     rm -rf /var/lib/apt/lists/*;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl
# Tue, 21 Nov 2023 10:15:03 GMT
WORKDIR /opt/emqx
# Tue, 21 Nov 2023 10:15:03 GMT
USER emqx
# Tue, 21 Nov 2023 10:15:03 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 21 Nov 2023 10:15:03 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 21 Nov 2023 10:15:03 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 21 Nov 2023 10:15:03 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 10:15:03 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9faf19c7b902a213dee90b0aec91abaf87bb600d398f3290b8970ece4baa5d0c`  
		Last Modified: Tue, 21 Nov 2023 10:16:00 GMT  
		Size: 1.6 MB (1645840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4370357dc913804e45c84e36d32603b076cef45d22699d6af105f5e53beab8`  
		Last Modified: Tue, 21 Nov 2023 10:16:00 GMT  
		Size: 4.1 KB (4109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366a91635bf670cf46d7ccd8b9e31152e2ca016c0db782e8e151ca685ebfbeac`  
		Last Modified: Tue, 21 Nov 2023 10:16:05 GMT  
		Size: 59.8 MB (59751733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b2dddaacaf7357386cb7ab9c5d0557409e70080e99a04fad28dde0d5538cb6`  
		Last Modified: Tue, 21 Nov 2023 10:16:00 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.3`

```console
$ docker pull emqx@sha256:719787ae27d124f0349b07e62ecccc59b11e825ac2620555e5d9530a465d69d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.3` - linux; amd64

```console
$ docker pull emqx@sha256:73926e41cbdee6877681ca92d63676ea9c3f22ca72055f1d45bf464125cd724f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101375214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe76bd89a252320b8f64452c5f57ef2c8f6636351b503111fa64caf08a1eb65`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:37:59 GMT
ENV EMQX_VERSION=5.3.1
# Tue, 21 Nov 2023 12:37:59 GMT
ENV AMD64_SHA256=1d13906b397e86e7822133d27d124bd06d714002293480047d5ac0e22d193fe2
# Tue, 21 Nov 2023 12:37:59 GMT
ENV ARM64_SHA256=e8aae039125194e9edb5dfbe8cf5c3eaf0e4bd2b9610fa97118d344115e31d2c
# Tue, 21 Nov 2023 12:38:00 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 21 Nov 2023 12:38:14 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:38:14 GMT
WORKDIR /opt/emqx
# Tue, 21 Nov 2023 12:38:14 GMT
USER emqx
# Tue, 21 Nov 2023 12:38:14 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 21 Nov 2023 12:38:14 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 21 Nov 2023 12:38:15 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 21 Nov 2023 12:38:15 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 12:38:15 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dff673b8def2f974461d3a0ed9702247b2a458c19ca6294c3d359577423e3eb`  
		Last Modified: Tue, 21 Nov 2023 12:39:24 GMT  
		Size: 70.0 MB (69956489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f864f6a2e455c756bf1980a7cbc67901d21f45e96e2b2d3f20b04601aaebc473`  
		Last Modified: Tue, 21 Nov 2023 12:39:16 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.3` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:cc31195c6e287ea408fe373fc4965c5c1f7c4f429b4fa16527a995ff55aa6646
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91670521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1bc8d0c635b3a9d73f254605b5b742d7d7660cb2654f6408dd6e0013e62b9d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:15:08 GMT
ENV EMQX_VERSION=5.3.1
# Tue, 21 Nov 2023 10:15:08 GMT
ENV AMD64_SHA256=1d13906b397e86e7822133d27d124bd06d714002293480047d5ac0e22d193fe2
# Tue, 21 Nov 2023 10:15:08 GMT
ENV ARM64_SHA256=e8aae039125194e9edb5dfbe8cf5c3eaf0e4bd2b9610fa97118d344115e31d2c
# Tue, 21 Nov 2023 10:15:08 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 21 Nov 2023 10:15:20 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 10:15:21 GMT
WORKDIR /opt/emqx
# Tue, 21 Nov 2023 10:15:21 GMT
USER emqx
# Tue, 21 Nov 2023 10:15:21 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 21 Nov 2023 10:15:21 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 21 Nov 2023 10:15:21 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 21 Nov 2023 10:15:21 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 10:15:21 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56845559447cc0b30e74bba4e898455dc082c47b180e241fbe5fcf29b8aad6a6`  
		Last Modified: Tue, 21 Nov 2023 10:16:19 GMT  
		Size: 61.6 MB (61605495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920711b146ec99aae5eaa1087f4683ff0084f6680c2083921990b8cf776c907c`  
		Last Modified: Tue, 21 Nov 2023 10:16:14 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.3.2`

**does not exist** (yet?)

## `emqx:latest`

```console
$ docker pull emqx@sha256:719787ae27d124f0349b07e62ecccc59b11e825ac2620555e5d9530a465d69d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:73926e41cbdee6877681ca92d63676ea9c3f22ca72055f1d45bf464125cd724f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101375214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbe76bd89a252320b8f64452c5f57ef2c8f6636351b503111fa64caf08a1eb65`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 12:37:59 GMT
ENV EMQX_VERSION=5.3.1
# Tue, 21 Nov 2023 12:37:59 GMT
ENV AMD64_SHA256=1d13906b397e86e7822133d27d124bd06d714002293480047d5ac0e22d193fe2
# Tue, 21 Nov 2023 12:37:59 GMT
ENV ARM64_SHA256=e8aae039125194e9edb5dfbe8cf5c3eaf0e4bd2b9610fa97118d344115e31d2c
# Tue, 21 Nov 2023 12:38:00 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 21 Nov 2023 12:38:14 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 12:38:14 GMT
WORKDIR /opt/emqx
# Tue, 21 Nov 2023 12:38:14 GMT
USER emqx
# Tue, 21 Nov 2023 12:38:14 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 21 Nov 2023 12:38:14 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 21 Nov 2023 12:38:15 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 21 Nov 2023 12:38:15 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 12:38:15 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dff673b8def2f974461d3a0ed9702247b2a458c19ca6294c3d359577423e3eb`  
		Last Modified: Tue, 21 Nov 2023 12:39:24 GMT  
		Size: 70.0 MB (69956489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f864f6a2e455c756bf1980a7cbc67901d21f45e96e2b2d3f20b04601aaebc473`  
		Last Modified: Tue, 21 Nov 2023 12:39:16 GMT  
		Size: 901.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:cc31195c6e287ea408fe373fc4965c5c1f7c4f429b4fa16527a995ff55aa6646
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.7 MB (91670521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1bc8d0c635b3a9d73f254605b5b742d7d7660cb2654f6408dd6e0013e62b9d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:15:08 GMT
ENV EMQX_VERSION=5.3.1
# Tue, 21 Nov 2023 10:15:08 GMT
ENV AMD64_SHA256=1d13906b397e86e7822133d27d124bd06d714002293480047d5ac0e22d193fe2
# Tue, 21 Nov 2023 10:15:08 GMT
ENV ARM64_SHA256=e8aae039125194e9edb5dfbe8cf5c3eaf0e4bd2b9610fa97118d344115e31d2c
# Tue, 21 Nov 2023 10:15:08 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 21 Nov 2023 10:15:20 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends ca-certificates procps curl;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg;     apt-get purge -y --auto-remove curl;     rm -rf /var/lib/apt/lists/*
# Tue, 21 Nov 2023 10:15:21 GMT
WORKDIR /opt/emqx
# Tue, 21 Nov 2023 10:15:21 GMT
USER emqx
# Tue, 21 Nov 2023 10:15:21 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 21 Nov 2023 10:15:21 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 21 Nov 2023 10:15:21 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 21 Nov 2023 10:15:21 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 21 Nov 2023 10:15:21 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56845559447cc0b30e74bba4e898455dc082c47b180e241fbe5fcf29b8aad6a6`  
		Last Modified: Tue, 21 Nov 2023 10:16:19 GMT  
		Size: 61.6 MB (61605495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920711b146ec99aae5eaa1087f4683ff0084f6680c2083921990b8cf776c907c`  
		Last Modified: Tue, 21 Nov 2023 10:16:14 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
