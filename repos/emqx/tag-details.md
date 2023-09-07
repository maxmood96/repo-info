<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:5`](#emqx5)
-	[`emqx:5.0`](#emqx50)
-	[`emqx:5.0.26`](#emqx5026)
-	[`emqx:5.1`](#emqx51)
-	[`emqx:5.1.6`](#emqx516)
-	[`emqx:latest`](#emqxlatest)

## `emqx:5`

```console
$ docker pull emqx@sha256:2441395920afd654baae1123f686a2e1432db5c7f33a00ca3a379117ec2e0f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:c6f6640ab4ef210e43b87483740e7cb386854e4d5dabb905a00be8597fc0ab24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102391616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a297dd3881e69eb7c2e218822233e640774df0d55fe0c9a42d20b079f8e8f7e8`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:13 GMT
ADD file:cb5fcc80c057b356a31492a20c6e3a75b70ed70a663506c8e97ad730ae32a02d in / 
# Thu, 07 Sep 2023 00:21:13 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 03:15:40 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 03:15:40 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 07 Sep 2023 03:15:55 GMT
ENV EMQX_VERSION=5.1.6
# Thu, 07 Sep 2023 03:15:55 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Thu, 07 Sep 2023 03:15:55 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Thu, 07 Sep 2023 03:15:55 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 07 Sep 2023 03:16:02 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Thu, 07 Sep 2023 03:16:03 GMT
WORKDIR /opt/emqx
# Thu, 07 Sep 2023 03:16:03 GMT
USER emqx
# Thu, 07 Sep 2023 03:16:03 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 07 Sep 2023 03:16:03 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 07 Sep 2023 03:16:03 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 07 Sep 2023 03:16:03 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 03:16:03 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:7d97e254a0461b0a30b3f443f1daa0d620a3cc6ff4e2714cc1cfd96ace5b7a7e`  
		Last Modified: Thu, 07 Sep 2023 00:26:03 GMT  
		Size: 31.4 MB (31417503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01b569a3058d6ac53f11279b7da13ec2b84713f0d8b7db7a6f3d4534b1f5630`  
		Last Modified: Thu, 07 Sep 2023 03:16:15 GMT  
		Size: 3.0 MB (2987848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ecff10efed71e04a1ed02e2d3daccf2f4684a4640941020720749dcb4c0e3f`  
		Last Modified: Thu, 07 Sep 2023 03:16:14 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d5112089b35d1268c6082d34a44ab9ce581e764d1194577d1f2452ab7978e7`  
		Last Modified: Thu, 07 Sep 2023 03:16:38 GMT  
		Size: 68.0 MB (67981258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c681ce97de0d2ada383664f034724f6e3b356fe796fd04554daf3adce4595c`  
		Last Modified: Thu, 07 Sep 2023 03:16:31 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:76016bb8023551c8a06ac73f623d2e8fbba8846b9f319db8f6603116d9836d6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92695391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05a15ee21ef3de0f809487671fc0b7eca746790dde8a7435294594df452f37fa`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 02:04:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 02:04:03 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 05 Sep 2023 23:48:30 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 05 Sep 2023 23:48:30 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 05 Sep 2023 23:48:30 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 05 Sep 2023 23:48:30 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 05 Sep 2023 23:48:37 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Tue, 05 Sep 2023 23:48:37 GMT
WORKDIR /opt/emqx
# Tue, 05 Sep 2023 23:48:37 GMT
USER emqx
# Tue, 05 Sep 2023 23:48:37 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 05 Sep 2023 23:48:37 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 05 Sep 2023 23:48:37 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 05 Sep 2023 23:48:37 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 05 Sep 2023 23:48:38 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf9935b6a5db89f92b605f7f0b0af22fb4cea1dcb2fce17fd4394f0b276031a`  
		Last Modified: Wed, 16 Aug 2023 02:04:31 GMT  
		Size: 3.0 MB (3002946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8af255dcc47cd844d6dc7e8fbb203f8650232883ccaa219fb0b5853b69a5a75`  
		Last Modified: Wed, 16 Aug 2023 02:04:30 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9897f244464d1440c8c5350ba4f8595ccfd3533b413b02e97316223990107fb`  
		Last Modified: Tue, 05 Sep 2023 23:48:53 GMT  
		Size: 59.6 MB (59624616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04abd0d70e05f8e913eb2812af284d74cd18a7524e18a19aa39e9a31643f3571`  
		Last Modified: Tue, 05 Sep 2023 23:48:48 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.0`

```console
$ docker pull emqx@sha256:ef7d9b7888557272ca67ff61c9107b6dddee0a890b2537e0991b767d91a1eed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.0` - linux; amd64

```console
$ docker pull emqx@sha256:e3ce5434ed1186b6615c1eaf9cf2457b258bf6150a92bf7e2d6aebed8c030328
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101982227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ebcc2dfe591b3293bceebd4f0d56dcb1fdb82b5f7f4cac612d1d5bd6444b562`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:13 GMT
ADD file:cb5fcc80c057b356a31492a20c6e3a75b70ed70a663506c8e97ad730ae32a02d in / 
# Thu, 07 Sep 2023 00:21:13 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 03:15:40 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 03:15:40 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 07 Sep 2023 03:15:40 GMT
ENV EMQX_VERSION=5.0.26
# Thu, 07 Sep 2023 03:15:41 GMT
ENV AMD64_SHA256=00f954065fe7fd2f678f2e561578234240cc2cace49fb5cbb5aa7fb450825ffa
# Thu, 07 Sep 2023 03:15:41 GMT
ENV ARM64_SHA256=0b013f0b900e687c1ef3ed73bd6fef268b5492d12a3083ffd0d75c8e3935b4ae
# Thu, 07 Sep 2023 03:15:41 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 07 Sep 2023 03:15:48 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Thu, 07 Sep 2023 03:15:49 GMT
WORKDIR /opt/emqx
# Thu, 07 Sep 2023 03:15:49 GMT
USER emqx
# Thu, 07 Sep 2023 03:15:49 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 07 Sep 2023 03:15:49 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 07 Sep 2023 03:15:49 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 07 Sep 2023 03:15:49 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 03:15:49 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:7d97e254a0461b0a30b3f443f1daa0d620a3cc6ff4e2714cc1cfd96ace5b7a7e`  
		Last Modified: Thu, 07 Sep 2023 00:26:03 GMT  
		Size: 31.4 MB (31417503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01b569a3058d6ac53f11279b7da13ec2b84713f0d8b7db7a6f3d4534b1f5630`  
		Last Modified: Thu, 07 Sep 2023 03:16:15 GMT  
		Size: 3.0 MB (2987848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ecff10efed71e04a1ed02e2d3daccf2f4684a4640941020720749dcb4c0e3f`  
		Last Modified: Thu, 07 Sep 2023 03:16:14 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a64c0f2fea7cc0cc28222502e581ea84b0bffa8c5e28138098b83e784dfb237`  
		Last Modified: Thu, 07 Sep 2023 03:16:22 GMT  
		Size: 67.6 MB (67571869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5feb1175189b10a66c509bd0fab0fdcb8f12e619ab1e067d5ee223d171eab0aa`  
		Last Modified: Thu, 07 Sep 2023 03:16:14 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.0` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:a16517d504734871297cd6bc22f0218c447b38ba186708e30c1b4b13fdb8515d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93060156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a39b7d91dd1c3865cdab2db949ef618aa84b51270dcef9f322596b174b670b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 02:04:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 02:04:03 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 16 Aug 2023 02:04:03 GMT
ENV EMQX_VERSION=5.0.26
# Wed, 16 Aug 2023 02:04:03 GMT
ENV AMD64_SHA256=00f954065fe7fd2f678f2e561578234240cc2cace49fb5cbb5aa7fb450825ffa
# Wed, 16 Aug 2023 02:04:03 GMT
ENV ARM64_SHA256=0b013f0b900e687c1ef3ed73bd6fef268b5492d12a3083ffd0d75c8e3935b4ae
# Wed, 16 Aug 2023 02:04:04 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 16 Aug 2023 02:04:10 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 16 Aug 2023 02:04:10 GMT
WORKDIR /opt/emqx
# Wed, 16 Aug 2023 02:04:10 GMT
USER emqx
# Wed, 16 Aug 2023 02:04:11 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 16 Aug 2023 02:04:11 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 16 Aug 2023 02:04:11 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 16 Aug 2023 02:04:11 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 16 Aug 2023 02:04:11 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf9935b6a5db89f92b605f7f0b0af22fb4cea1dcb2fce17fd4394f0b276031a`  
		Last Modified: Wed, 16 Aug 2023 02:04:31 GMT  
		Size: 3.0 MB (3002946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8af255dcc47cd844d6dc7e8fbb203f8650232883ccaa219fb0b5853b69a5a75`  
		Last Modified: Wed, 16 Aug 2023 02:04:30 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c8d6f86cad7962e873b954b5638499c5b7e4457159d0032cfa7d552e606910`  
		Last Modified: Wed, 16 Aug 2023 02:04:36 GMT  
		Size: 60.0 MB (59989381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57bc415c236d3beef60d59da5052c2daaec999f2f81a314d56ae98182d5d19b`  
		Last Modified: Wed, 16 Aug 2023 02:04:30 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.0.26`

```console
$ docker pull emqx@sha256:ef7d9b7888557272ca67ff61c9107b6dddee0a890b2537e0991b767d91a1eed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.0.26` - linux; amd64

```console
$ docker pull emqx@sha256:e3ce5434ed1186b6615c1eaf9cf2457b258bf6150a92bf7e2d6aebed8c030328
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101982227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ebcc2dfe591b3293bceebd4f0d56dcb1fdb82b5f7f4cac612d1d5bd6444b562`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:13 GMT
ADD file:cb5fcc80c057b356a31492a20c6e3a75b70ed70a663506c8e97ad730ae32a02d in / 
# Thu, 07 Sep 2023 00:21:13 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 03:15:40 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 03:15:40 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 07 Sep 2023 03:15:40 GMT
ENV EMQX_VERSION=5.0.26
# Thu, 07 Sep 2023 03:15:41 GMT
ENV AMD64_SHA256=00f954065fe7fd2f678f2e561578234240cc2cace49fb5cbb5aa7fb450825ffa
# Thu, 07 Sep 2023 03:15:41 GMT
ENV ARM64_SHA256=0b013f0b900e687c1ef3ed73bd6fef268b5492d12a3083ffd0d75c8e3935b4ae
# Thu, 07 Sep 2023 03:15:41 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 07 Sep 2023 03:15:48 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Thu, 07 Sep 2023 03:15:49 GMT
WORKDIR /opt/emqx
# Thu, 07 Sep 2023 03:15:49 GMT
USER emqx
# Thu, 07 Sep 2023 03:15:49 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 07 Sep 2023 03:15:49 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 07 Sep 2023 03:15:49 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 07 Sep 2023 03:15:49 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 03:15:49 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:7d97e254a0461b0a30b3f443f1daa0d620a3cc6ff4e2714cc1cfd96ace5b7a7e`  
		Last Modified: Thu, 07 Sep 2023 00:26:03 GMT  
		Size: 31.4 MB (31417503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01b569a3058d6ac53f11279b7da13ec2b84713f0d8b7db7a6f3d4534b1f5630`  
		Last Modified: Thu, 07 Sep 2023 03:16:15 GMT  
		Size: 3.0 MB (2987848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ecff10efed71e04a1ed02e2d3daccf2f4684a4640941020720749dcb4c0e3f`  
		Last Modified: Thu, 07 Sep 2023 03:16:14 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a64c0f2fea7cc0cc28222502e581ea84b0bffa8c5e28138098b83e784dfb237`  
		Last Modified: Thu, 07 Sep 2023 03:16:22 GMT  
		Size: 67.6 MB (67571869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5feb1175189b10a66c509bd0fab0fdcb8f12e619ab1e067d5ee223d171eab0aa`  
		Last Modified: Thu, 07 Sep 2023 03:16:14 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.0.26` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:a16517d504734871297cd6bc22f0218c447b38ba186708e30c1b4b13fdb8515d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93060156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a39b7d91dd1c3865cdab2db949ef618aa84b51270dcef9f322596b174b670b`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 02:04:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 02:04:03 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 16 Aug 2023 02:04:03 GMT
ENV EMQX_VERSION=5.0.26
# Wed, 16 Aug 2023 02:04:03 GMT
ENV AMD64_SHA256=00f954065fe7fd2f678f2e561578234240cc2cace49fb5cbb5aa7fb450825ffa
# Wed, 16 Aug 2023 02:04:03 GMT
ENV ARM64_SHA256=0b013f0b900e687c1ef3ed73bd6fef268b5492d12a3083ffd0d75c8e3935b4ae
# Wed, 16 Aug 2023 02:04:04 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 16 Aug 2023 02:04:10 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 16 Aug 2023 02:04:10 GMT
WORKDIR /opt/emqx
# Wed, 16 Aug 2023 02:04:10 GMT
USER emqx
# Wed, 16 Aug 2023 02:04:11 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 16 Aug 2023 02:04:11 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 16 Aug 2023 02:04:11 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 16 Aug 2023 02:04:11 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 16 Aug 2023 02:04:11 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf9935b6a5db89f92b605f7f0b0af22fb4cea1dcb2fce17fd4394f0b276031a`  
		Last Modified: Wed, 16 Aug 2023 02:04:31 GMT  
		Size: 3.0 MB (3002946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8af255dcc47cd844d6dc7e8fbb203f8650232883ccaa219fb0b5853b69a5a75`  
		Last Modified: Wed, 16 Aug 2023 02:04:30 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c8d6f86cad7962e873b954b5638499c5b7e4457159d0032cfa7d552e606910`  
		Last Modified: Wed, 16 Aug 2023 02:04:36 GMT  
		Size: 60.0 MB (59989381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57bc415c236d3beef60d59da5052c2daaec999f2f81a314d56ae98182d5d19b`  
		Last Modified: Wed, 16 Aug 2023 02:04:30 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.1`

```console
$ docker pull emqx@sha256:2441395920afd654baae1123f686a2e1432db5c7f33a00ca3a379117ec2e0f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.1` - linux; amd64

```console
$ docker pull emqx@sha256:c6f6640ab4ef210e43b87483740e7cb386854e4d5dabb905a00be8597fc0ab24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102391616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a297dd3881e69eb7c2e218822233e640774df0d55fe0c9a42d20b079f8e8f7e8`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:13 GMT
ADD file:cb5fcc80c057b356a31492a20c6e3a75b70ed70a663506c8e97ad730ae32a02d in / 
# Thu, 07 Sep 2023 00:21:13 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 03:15:40 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 03:15:40 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 07 Sep 2023 03:15:55 GMT
ENV EMQX_VERSION=5.1.6
# Thu, 07 Sep 2023 03:15:55 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Thu, 07 Sep 2023 03:15:55 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Thu, 07 Sep 2023 03:15:55 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 07 Sep 2023 03:16:02 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Thu, 07 Sep 2023 03:16:03 GMT
WORKDIR /opt/emqx
# Thu, 07 Sep 2023 03:16:03 GMT
USER emqx
# Thu, 07 Sep 2023 03:16:03 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 07 Sep 2023 03:16:03 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 07 Sep 2023 03:16:03 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 07 Sep 2023 03:16:03 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 03:16:03 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:7d97e254a0461b0a30b3f443f1daa0d620a3cc6ff4e2714cc1cfd96ace5b7a7e`  
		Last Modified: Thu, 07 Sep 2023 00:26:03 GMT  
		Size: 31.4 MB (31417503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01b569a3058d6ac53f11279b7da13ec2b84713f0d8b7db7a6f3d4534b1f5630`  
		Last Modified: Thu, 07 Sep 2023 03:16:15 GMT  
		Size: 3.0 MB (2987848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ecff10efed71e04a1ed02e2d3daccf2f4684a4640941020720749dcb4c0e3f`  
		Last Modified: Thu, 07 Sep 2023 03:16:14 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d5112089b35d1268c6082d34a44ab9ce581e764d1194577d1f2452ab7978e7`  
		Last Modified: Thu, 07 Sep 2023 03:16:38 GMT  
		Size: 68.0 MB (67981258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c681ce97de0d2ada383664f034724f6e3b356fe796fd04554daf3adce4595c`  
		Last Modified: Thu, 07 Sep 2023 03:16:31 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.1` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:76016bb8023551c8a06ac73f623d2e8fbba8846b9f319db8f6603116d9836d6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92695391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05a15ee21ef3de0f809487671fc0b7eca746790dde8a7435294594df452f37fa`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 02:04:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 02:04:03 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 05 Sep 2023 23:48:30 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 05 Sep 2023 23:48:30 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 05 Sep 2023 23:48:30 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 05 Sep 2023 23:48:30 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 05 Sep 2023 23:48:37 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Tue, 05 Sep 2023 23:48:37 GMT
WORKDIR /opt/emqx
# Tue, 05 Sep 2023 23:48:37 GMT
USER emqx
# Tue, 05 Sep 2023 23:48:37 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 05 Sep 2023 23:48:37 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 05 Sep 2023 23:48:37 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 05 Sep 2023 23:48:37 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 05 Sep 2023 23:48:38 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf9935b6a5db89f92b605f7f0b0af22fb4cea1dcb2fce17fd4394f0b276031a`  
		Last Modified: Wed, 16 Aug 2023 02:04:31 GMT  
		Size: 3.0 MB (3002946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8af255dcc47cd844d6dc7e8fbb203f8650232883ccaa219fb0b5853b69a5a75`  
		Last Modified: Wed, 16 Aug 2023 02:04:30 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9897f244464d1440c8c5350ba4f8595ccfd3533b413b02e97316223990107fb`  
		Last Modified: Tue, 05 Sep 2023 23:48:53 GMT  
		Size: 59.6 MB (59624616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04abd0d70e05f8e913eb2812af284d74cd18a7524e18a19aa39e9a31643f3571`  
		Last Modified: Tue, 05 Sep 2023 23:48:48 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.1.6`

```console
$ docker pull emqx@sha256:2441395920afd654baae1123f686a2e1432db5c7f33a00ca3a379117ec2e0f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.1.6` - linux; amd64

```console
$ docker pull emqx@sha256:c6f6640ab4ef210e43b87483740e7cb386854e4d5dabb905a00be8597fc0ab24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102391616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a297dd3881e69eb7c2e218822233e640774df0d55fe0c9a42d20b079f8e8f7e8`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:13 GMT
ADD file:cb5fcc80c057b356a31492a20c6e3a75b70ed70a663506c8e97ad730ae32a02d in / 
# Thu, 07 Sep 2023 00:21:13 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 03:15:40 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 03:15:40 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 07 Sep 2023 03:15:55 GMT
ENV EMQX_VERSION=5.1.6
# Thu, 07 Sep 2023 03:15:55 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Thu, 07 Sep 2023 03:15:55 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Thu, 07 Sep 2023 03:15:55 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 07 Sep 2023 03:16:02 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Thu, 07 Sep 2023 03:16:03 GMT
WORKDIR /opt/emqx
# Thu, 07 Sep 2023 03:16:03 GMT
USER emqx
# Thu, 07 Sep 2023 03:16:03 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 07 Sep 2023 03:16:03 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 07 Sep 2023 03:16:03 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 07 Sep 2023 03:16:03 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 03:16:03 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:7d97e254a0461b0a30b3f443f1daa0d620a3cc6ff4e2714cc1cfd96ace5b7a7e`  
		Last Modified: Thu, 07 Sep 2023 00:26:03 GMT  
		Size: 31.4 MB (31417503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01b569a3058d6ac53f11279b7da13ec2b84713f0d8b7db7a6f3d4534b1f5630`  
		Last Modified: Thu, 07 Sep 2023 03:16:15 GMT  
		Size: 3.0 MB (2987848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ecff10efed71e04a1ed02e2d3daccf2f4684a4640941020720749dcb4c0e3f`  
		Last Modified: Thu, 07 Sep 2023 03:16:14 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d5112089b35d1268c6082d34a44ab9ce581e764d1194577d1f2452ab7978e7`  
		Last Modified: Thu, 07 Sep 2023 03:16:38 GMT  
		Size: 68.0 MB (67981258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c681ce97de0d2ada383664f034724f6e3b356fe796fd04554daf3adce4595c`  
		Last Modified: Thu, 07 Sep 2023 03:16:31 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.1.6` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:76016bb8023551c8a06ac73f623d2e8fbba8846b9f319db8f6603116d9836d6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92695391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05a15ee21ef3de0f809487671fc0b7eca746790dde8a7435294594df452f37fa`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 02:04:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 02:04:03 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 05 Sep 2023 23:48:30 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 05 Sep 2023 23:48:30 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 05 Sep 2023 23:48:30 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 05 Sep 2023 23:48:30 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 05 Sep 2023 23:48:37 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Tue, 05 Sep 2023 23:48:37 GMT
WORKDIR /opt/emqx
# Tue, 05 Sep 2023 23:48:37 GMT
USER emqx
# Tue, 05 Sep 2023 23:48:37 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 05 Sep 2023 23:48:37 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 05 Sep 2023 23:48:37 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 05 Sep 2023 23:48:37 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 05 Sep 2023 23:48:38 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf9935b6a5db89f92b605f7f0b0af22fb4cea1dcb2fce17fd4394f0b276031a`  
		Last Modified: Wed, 16 Aug 2023 02:04:31 GMT  
		Size: 3.0 MB (3002946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8af255dcc47cd844d6dc7e8fbb203f8650232883ccaa219fb0b5853b69a5a75`  
		Last Modified: Wed, 16 Aug 2023 02:04:30 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9897f244464d1440c8c5350ba4f8595ccfd3533b413b02e97316223990107fb`  
		Last Modified: Tue, 05 Sep 2023 23:48:53 GMT  
		Size: 59.6 MB (59624616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04abd0d70e05f8e913eb2812af284d74cd18a7524e18a19aa39e9a31643f3571`  
		Last Modified: Tue, 05 Sep 2023 23:48:48 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:latest`

```console
$ docker pull emqx@sha256:2441395920afd654baae1123f686a2e1432db5c7f33a00ca3a379117ec2e0f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:c6f6640ab4ef210e43b87483740e7cb386854e4d5dabb905a00be8597fc0ab24
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102391616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a297dd3881e69eb7c2e218822233e640774df0d55fe0c9a42d20b079f8e8f7e8`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:13 GMT
ADD file:cb5fcc80c057b356a31492a20c6e3a75b70ed70a663506c8e97ad730ae32a02d in / 
# Thu, 07 Sep 2023 00:21:13 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 03:15:40 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 03:15:40 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 07 Sep 2023 03:15:55 GMT
ENV EMQX_VERSION=5.1.6
# Thu, 07 Sep 2023 03:15:55 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Thu, 07 Sep 2023 03:15:55 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Thu, 07 Sep 2023 03:15:55 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 07 Sep 2023 03:16:02 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Thu, 07 Sep 2023 03:16:03 GMT
WORKDIR /opt/emqx
# Thu, 07 Sep 2023 03:16:03 GMT
USER emqx
# Thu, 07 Sep 2023 03:16:03 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 07 Sep 2023 03:16:03 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 07 Sep 2023 03:16:03 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 07 Sep 2023 03:16:03 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 07 Sep 2023 03:16:03 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:7d97e254a0461b0a30b3f443f1daa0d620a3cc6ff4e2714cc1cfd96ace5b7a7e`  
		Last Modified: Thu, 07 Sep 2023 00:26:03 GMT  
		Size: 31.4 MB (31417503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01b569a3058d6ac53f11279b7da13ec2b84713f0d8b7db7a6f3d4534b1f5630`  
		Last Modified: Thu, 07 Sep 2023 03:16:15 GMT  
		Size: 3.0 MB (2987848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ecff10efed71e04a1ed02e2d3daccf2f4684a4640941020720749dcb4c0e3f`  
		Last Modified: Thu, 07 Sep 2023 03:16:14 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d5112089b35d1268c6082d34a44ab9ce581e764d1194577d1f2452ab7978e7`  
		Last Modified: Thu, 07 Sep 2023 03:16:38 GMT  
		Size: 68.0 MB (67981258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c681ce97de0d2ada383664f034724f6e3b356fe796fd04554daf3adce4595c`  
		Last Modified: Thu, 07 Sep 2023 03:16:31 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:76016bb8023551c8a06ac73f623d2e8fbba8846b9f319db8f6603116d9836d6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92695391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05a15ee21ef3de0f809487671fc0b7eca746790dde8a7435294594df452f37fa`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 02:04:03 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 02:04:03 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 05 Sep 2023 23:48:30 GMT
ENV EMQX_VERSION=5.1.6
# Tue, 05 Sep 2023 23:48:30 GMT
ENV AMD64_SHA256=5c65f7538141e93d71d1dd7d088589339ef6a091b90f901604a2e0e004f5f4aa
# Tue, 05 Sep 2023 23:48:30 GMT
ENV ARM64_SHA256=ae832d29d6b4e7fa43f3bf04c8c9fad4c9047f079d1587d3ed2a3564d5ea8147
# Tue, 05 Sep 2023 23:48:30 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 05 Sep 2023 23:48:37 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c;     mkdir /opt/emqx;     tar zxf $pkg -C /opt/emqx;     find /opt/emqx -name 'swagger*.js.map' -exec rm {} +;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -f $pkg
# Tue, 05 Sep 2023 23:48:37 GMT
WORKDIR /opt/emqx
# Tue, 05 Sep 2023 23:48:37 GMT
USER emqx
# Tue, 05 Sep 2023 23:48:37 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 05 Sep 2023 23:48:37 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 05 Sep 2023 23:48:37 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 05 Sep 2023 23:48:37 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 05 Sep 2023 23:48:38 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf9935b6a5db89f92b605f7f0b0af22fb4cea1dcb2fce17fd4394f0b276031a`  
		Last Modified: Wed, 16 Aug 2023 02:04:31 GMT  
		Size: 3.0 MB (3002946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8af255dcc47cd844d6dc7e8fbb203f8650232883ccaa219fb0b5853b69a5a75`  
		Last Modified: Wed, 16 Aug 2023 02:04:30 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9897f244464d1440c8c5350ba4f8595ccfd3533b413b02e97316223990107fb`  
		Last Modified: Tue, 05 Sep 2023 23:48:53 GMT  
		Size: 59.6 MB (59624616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04abd0d70e05f8e913eb2812af284d74cd18a7524e18a19aa39e9a31643f3571`  
		Last Modified: Tue, 05 Sep 2023 23:48:48 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
