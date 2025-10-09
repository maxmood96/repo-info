## `nats:alpine3.22`

```console
$ docker pull nats@sha256:4372059f8121acd60d370fccda873109c51e849c4432deadfe86460684832354
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:alpine3.22` - linux; amd64

```console
$ docker pull nats@sha256:72100bb9c3af46712a7ef13ab91a2245898de9c9b3269c515331bf61fe0aa516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10813376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ccf382e08933a0203eff6df376b8eee583308c681559f6cc63a3aa2fcbe330`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 30 Sep 2025 15:44:04 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 30 Sep 2025 15:44:04 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 15:44:04 GMT
ENV NATS_SERVER=2.12.0
# Tue, 30 Sep 2025 15:44:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='67051df32cd22ae830811ebb8574f431094e26a458fa7562e486b1cf37316915' ;;     armhf) natsArch='arm6'; sha256='23a20ef82d9437c159a38c68f6e463545aaa7085286d104398ae71f0153d4a51' ;;     armv7) natsArch='arm7'; sha256='82e0c757dff71c0593dc8ae45afadbf5bab5835b98134e9b2973750f9849ca6c' ;;     x86_64) natsArch='amd64'; sha256='42f233b3e883ff96e9fa9ba0882b958138534bc5dd6c4da7318e296afc0da909' ;;     x86) natsArch='386'; sha256='56eccfd5c4e9b3b31dae1bbe0c71b83cfb5a74f5990694dbc7557549df0f6c88' ;;     s390x) natsArch='s390x'; sha256='c1902cd6faf29babd917bbffe1b287747659249ca4eefd2d786b0502524782c3' ;;     ppc64le) natsArch='ppc64le'; sha256='2b7490b3b05392b69a8e55f8873a7be4663b03eecb0ca001ffcd97d1b3c91f8d' ;;     loong64) natsArch='loong64'; sha256='d632ed768d645c0e58b0ff52eec14ff2a51c5f8690639457d4a92747ee9edc32' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 30 Sep 2025 15:44:04 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 30 Sep 2025 15:44:04 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 30 Sep 2025 15:44:04 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 30 Sep 2025 15:44:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 15:44:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4f53fd467fc6d37900b02d1ff65e39d360b8decaa5212f098bc193f84dbb09`  
		Last Modified: Wed, 08 Oct 2025 22:40:04 GMT  
		Size: 7.0 MB (7009955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e2d1552e38f6f5070c1c3f8fd3a9bcc9de59c41b57f48916f22f5444520ee09`  
		Last Modified: Wed, 08 Oct 2025 22:40:04 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e59a953a375270b1efa384654c68ea18c0e3f78cdb6e4d955bb4dfc5afd9aa2`  
		Last Modified: Wed, 08 Oct 2025 22:40:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:ae0a0c3a6d651c2b027f112c8540e29b1c3a24edf517b1e1565c3b775111090f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646cb2febbbf89fdb5568a7075a12ec8b61ae271486d3b9983c6a93095cb7bc5`

```dockerfile
```

-	Layers:
	-	`sha256:ca74a58f731a126980aa72705d6025631fcbc53e738b212fa9febd01179ec7ab`  
		Last Modified: Wed, 08 Oct 2025 23:56:36 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v6

```console
$ docker pull nats@sha256:30fe5d18514085eab4e62cd669d6b62a25a07f2666f563c3309a14cd65d3552d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10238318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:162d00f824d1216a39fb797709f0819f812b886f3c327a1fd15fc7ce301a54c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 30 Sep 2025 15:44:04 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Tue, 30 Sep 2025 15:44:04 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 15:44:04 GMT
ENV NATS_SERVER=2.12.0
# Tue, 30 Sep 2025 15:44:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='67051df32cd22ae830811ebb8574f431094e26a458fa7562e486b1cf37316915' ;;     armhf) natsArch='arm6'; sha256='23a20ef82d9437c159a38c68f6e463545aaa7085286d104398ae71f0153d4a51' ;;     armv7) natsArch='arm7'; sha256='82e0c757dff71c0593dc8ae45afadbf5bab5835b98134e9b2973750f9849ca6c' ;;     x86_64) natsArch='amd64'; sha256='42f233b3e883ff96e9fa9ba0882b958138534bc5dd6c4da7318e296afc0da909' ;;     x86) natsArch='386'; sha256='56eccfd5c4e9b3b31dae1bbe0c71b83cfb5a74f5990694dbc7557549df0f6c88' ;;     s390x) natsArch='s390x'; sha256='c1902cd6faf29babd917bbffe1b287747659249ca4eefd2d786b0502524782c3' ;;     ppc64le) natsArch='ppc64le'; sha256='2b7490b3b05392b69a8e55f8873a7be4663b03eecb0ca001ffcd97d1b3c91f8d' ;;     loong64) natsArch='loong64'; sha256='d632ed768d645c0e58b0ff52eec14ff2a51c5f8690639457d4a92747ee9edc32' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 30 Sep 2025 15:44:04 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 30 Sep 2025 15:44:04 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 30 Sep 2025 15:44:04 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 30 Sep 2025 15:44:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 15:44:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01baf89ac9708a45214cb733e657dea8e8fdb8eef2e87f4be5e7b55d443c858`  
		Last Modified: Wed, 08 Oct 2025 21:42:09 GMT  
		Size: 6.7 MB (6733270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60bb712f0562d9a5fedbbbf8f377f6487f85a7f40e3a1b1b89695ad3927f132`  
		Last Modified: Wed, 08 Oct 2025 21:42:07 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf31aa4ba7b7fb818552cf7d314a9e81622127888619d3f5c4ef5e5299f826d`  
		Last Modified: Wed, 08 Oct 2025 21:42:07 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:06d6ad32f7af44f6278b45448657da67635537ea22792862d85364600723f965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ff2a7f70caab037cdb9a7bf3552abfc82ec053ea0dc9f9f01d9af10f0da1b4`

```dockerfile
```

-	Layers:
	-	`sha256:08388647336d97b9fc2aae46f0609920b48a4610a6eaaef7c43418a1520985ee`  
		Last Modified: Wed, 08 Oct 2025 23:56:39 GMT  
		Size: 14.8 KB (14825 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm variant v7

```console
$ docker pull nats@sha256:979813f463297125aeac2f64430d27d42eccfa835962c858d37e0b768b0e4109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9946537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80337bc3b6b0dd2de3fea53ad421cffc96a0689f718937ad111066b95d8e8741`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 30 Sep 2025 15:44:04 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Tue, 30 Sep 2025 15:44:04 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 15:44:04 GMT
ENV NATS_SERVER=2.12.0
# Tue, 30 Sep 2025 15:44:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='67051df32cd22ae830811ebb8574f431094e26a458fa7562e486b1cf37316915' ;;     armhf) natsArch='arm6'; sha256='23a20ef82d9437c159a38c68f6e463545aaa7085286d104398ae71f0153d4a51' ;;     armv7) natsArch='arm7'; sha256='82e0c757dff71c0593dc8ae45afadbf5bab5835b98134e9b2973750f9849ca6c' ;;     x86_64) natsArch='amd64'; sha256='42f233b3e883ff96e9fa9ba0882b958138534bc5dd6c4da7318e296afc0da909' ;;     x86) natsArch='386'; sha256='56eccfd5c4e9b3b31dae1bbe0c71b83cfb5a74f5990694dbc7557549df0f6c88' ;;     s390x) natsArch='s390x'; sha256='c1902cd6faf29babd917bbffe1b287747659249ca4eefd2d786b0502524782c3' ;;     ppc64le) natsArch='ppc64le'; sha256='2b7490b3b05392b69a8e55f8873a7be4663b03eecb0ca001ffcd97d1b3c91f8d' ;;     loong64) natsArch='loong64'; sha256='d632ed768d645c0e58b0ff52eec14ff2a51c5f8690639457d4a92747ee9edc32' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 30 Sep 2025 15:44:04 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 30 Sep 2025 15:44:04 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 30 Sep 2025 15:44:04 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 30 Sep 2025 15:44:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 15:44:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c01324d8ccb7e01f019d641b01aa29d50bd2fc9849e4e727aa422e8314a98d7`  
		Last Modified: Wed, 08 Oct 2025 23:14:13 GMT  
		Size: 6.7 MB (6724015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2215f9e3aff97633c33b02e9386bd1d81f920caa172b364572646820ff294c2d`  
		Last Modified: Wed, 08 Oct 2025 22:27:27 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92fd9d436b4a3f5295da0abb3d4d7d5caf82efd4b8006e5db789253e348c5dc7`  
		Last Modified: Wed, 08 Oct 2025 22:27:30 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:2504eaa63666f52e287eb7fd4a90d7df8d047ce4d983c7a41562613ee50a49d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dae05e84ef199d3e38d0bcb012c81187636a8ababfc738b71b468e7b3a7dfd6`

```dockerfile
```

-	Layers:
	-	`sha256:2d95c794e8f016dc2db1c64198b994b973a8dad8779381b27ba1717991594bd7`  
		Last Modified: Wed, 08 Oct 2025 23:56:42 GMT  
		Size: 14.8 KB (14825 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:397f228737feed53723e2c6a10b8ee56acf1935dd1e3e21676bfec017cae4ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10563262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b6ef974abc34659fe8e614e8ecaffed0611a899dbf07d107e86f32f37b9b5b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 30 Sep 2025 15:44:04 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 30 Sep 2025 15:44:04 GMT
CMD ["/bin/sh"]
# Tue, 30 Sep 2025 15:44:04 GMT
ENV NATS_SERVER=2.12.0
# Tue, 30 Sep 2025 15:44:04 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='67051df32cd22ae830811ebb8574f431094e26a458fa7562e486b1cf37316915' ;;     armhf) natsArch='arm6'; sha256='23a20ef82d9437c159a38c68f6e463545aaa7085286d104398ae71f0153d4a51' ;;     armv7) natsArch='arm7'; sha256='82e0c757dff71c0593dc8ae45afadbf5bab5835b98134e9b2973750f9849ca6c' ;;     x86_64) natsArch='amd64'; sha256='42f233b3e883ff96e9fa9ba0882b958138534bc5dd6c4da7318e296afc0da909' ;;     x86) natsArch='386'; sha256='56eccfd5c4e9b3b31dae1bbe0c71b83cfb5a74f5990694dbc7557549df0f6c88' ;;     s390x) natsArch='s390x'; sha256='c1902cd6faf29babd917bbffe1b287747659249ca4eefd2d786b0502524782c3' ;;     ppc64le) natsArch='ppc64le'; sha256='2b7490b3b05392b69a8e55f8873a7be4663b03eecb0ca001ffcd97d1b3c91f8d' ;;     loong64) natsArch='loong64'; sha256='d632ed768d645c0e58b0ff52eec14ff2a51c5f8690639457d4a92747ee9edc32' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 30 Sep 2025 15:44:04 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 30 Sep 2025 15:44:04 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 30 Sep 2025 15:44:04 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 30 Sep 2025 15:44:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Sep 2025 15:44:04 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56817013169f9b2bdd8766887a4888942396046ead039d568266a2930e781e1a`  
		Last Modified: Wed, 08 Oct 2025 21:13:06 GMT  
		Size: 6.4 MB (6424225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe79467b4c1ec2f9d7feb6e33db207c3357b1529104ac3b2b62b9397de5d5d6`  
		Last Modified: Wed, 08 Oct 2025 21:13:06 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c102cb59a14a36a24b39a90113f3034af934cf5cf82b7b3046af1815741d251`  
		Last Modified: Wed, 08 Oct 2025 21:13:06 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:7627666cb2be6e475619c3059870f118709dd5a85e9e273ae2e212d82fbd8b3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1deacfc1560a60f1b70abd88f9ce9c9979e46bad0b2a5054dc23ffb491c91c6f`

```dockerfile
```

-	Layers:
	-	`sha256:a43f8e560ac141d5faf06f1b42e645cd65b8447a569acba6197ce6f950ecd6d7`  
		Last Modified: Wed, 08 Oct 2025 23:56:45 GMT  
		Size: 14.9 KB (14865 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; ppc64le

```console
$ docker pull nats@sha256:330c1e0af8d37e016c299a67a72d4a4bf274ea7cdc2aa19ebf2abc140e354a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10195084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82391b8bbf316b21052a47ac99a821e8bd3a9280e71b91ee772717e4d37952a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 22 Sep 2025 12:53:23 GMT
ENV NATS_SERVER=2.12.0
# Mon, 22 Sep 2025 12:53:23 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='67051df32cd22ae830811ebb8574f431094e26a458fa7562e486b1cf37316915' ;;     armhf) natsArch='arm6'; sha256='23a20ef82d9437c159a38c68f6e463545aaa7085286d104398ae71f0153d4a51' ;;     armv7) natsArch='arm7'; sha256='82e0c757dff71c0593dc8ae45afadbf5bab5835b98134e9b2973750f9849ca6c' ;;     x86_64) natsArch='amd64'; sha256='42f233b3e883ff96e9fa9ba0882b958138534bc5dd6c4da7318e296afc0da909' ;;     x86) natsArch='386'; sha256='56eccfd5c4e9b3b31dae1bbe0c71b83cfb5a74f5990694dbc7557549df0f6c88' ;;     s390x) natsArch='s390x'; sha256='c1902cd6faf29babd917bbffe1b287747659249ca4eefd2d786b0502524782c3' ;;     ppc64le) natsArch='ppc64le'; sha256='2b7490b3b05392b69a8e55f8873a7be4663b03eecb0ca001ffcd97d1b3c91f8d' ;;     loong64) natsArch='loong64'; sha256='d632ed768d645c0e58b0ff52eec14ff2a51c5f8690639457d4a92747ee9edc32' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 22 Sep 2025 12:53:23 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 22 Sep 2025 12:53:23 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 22 Sep 2025 12:53:23 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Sep 2025 12:53:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Sep 2025 12:53:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53715feca00522eeeb904e688ba46f9f6a7ca9b6296a30b53624f44e87767c1a`  
		Last Modified: Mon, 22 Sep 2025 20:34:57 GMT  
		Size: 6.5 MB (6466999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca0a82da5e24e78bd841dae1c330ef27961eb20b67052d7a8b8860e691cce6a`  
		Last Modified: Mon, 22 Sep 2025 20:34:56 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34351d43aaa584a0095b23b56fec3e1974b355d04a8e914effab9b9be157378`  
		Last Modified: Mon, 22 Sep 2025 20:34:57 GMT  
		Size: 413.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:899deddacf3750575ff12afb9c0cfd7935fd7f9498ddcdd746b9ec32c1b9d8e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 KB (14781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec6f94be82b5be62fc466087ed7687bd8c4a19fc15cef7e202aaf9bcd626d502`

```dockerfile
```

-	Layers:
	-	`sha256:62cc13bd933e633a0e1599be27f10658d936f4363e25aab9f4807c81470c54ce`  
		Last Modified: Mon, 22 Sep 2025 20:56:58 GMT  
		Size: 14.8 KB (14781 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:alpine3.22` - linux; s390x

```console
$ docker pull nats@sha256:583dc6023bd46b29da71524c0905d64ecaadfeabf6c56c658037b44fc81c1e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10484938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b886097b67112e71dc338f6cad861ccd6f23973b53c216d3d1e0e91637d6fff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Mon, 22 Sep 2025 12:53:23 GMT
ENV NATS_SERVER=2.12.0
# Mon, 22 Sep 2025 12:53:23 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in     aarch64) natsArch='arm64'; sha256='67051df32cd22ae830811ebb8574f431094e26a458fa7562e486b1cf37316915' ;;     armhf) natsArch='arm6'; sha256='23a20ef82d9437c159a38c68f6e463545aaa7085286d104398ae71f0153d4a51' ;;     armv7) natsArch='arm7'; sha256='82e0c757dff71c0593dc8ae45afadbf5bab5835b98134e9b2973750f9849ca6c' ;;     x86_64) natsArch='amd64'; sha256='42f233b3e883ff96e9fa9ba0882b958138534bc5dd6c4da7318e296afc0da909' ;;     x86) natsArch='386'; sha256='56eccfd5c4e9b3b31dae1bbe0c71b83cfb5a74f5990694dbc7557549df0f6c88' ;;     s390x) natsArch='s390x'; sha256='c1902cd6faf29babd917bbffe1b287747659249ca4eefd2d786b0502524782c3' ;;     ppc64le) natsArch='ppc64le'; sha256='2b7490b3b05392b69a8e55f8873a7be4663b03eecb0ca001ffcd97d1b3c91f8d' ;;     loong64) natsArch='loong64'; sha256='d632ed768d645c0e58b0ff52eec14ff2a51c5f8690639457d4a92747ee9edc32' ;;     *) echo >&2 "error: $apkArch is not supported!"; exit 1 ;;     esac;         wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz";     echo "${sha256} *nats-server.tar.gz" | sha256sum -c -;         apk add --no-cache ca-certificates tzdata;         tar -xf nats-server.tar.gz;     rm nats-server.tar.gz;     mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin;     rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Mon, 22 Sep 2025 12:53:23 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Mon, 22 Sep 2025 12:53:23 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Mon, 22 Sep 2025 12:53:23 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Mon, 22 Sep 2025 12:53:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Sep 2025 12:53:23 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68a38c35c25851432e548e4f6311468d5e8019abd9f074be9d4f0421dbcb030`  
		Last Modified: Mon, 22 Sep 2025 20:34:58 GMT  
		Size: 6.8 MB (6838998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2978644e153684bc482789a42dfd9b53faf1ee77e354dc186afcb4f800a8813`  
		Last Modified: Mon, 22 Sep 2025 20:34:57 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c405b5135b2f42101c52e11f5872bc2628d9242aa1a8932d7e713b584180f46`  
		Last Modified: Mon, 22 Sep 2025 20:34:58 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:alpine3.22` - unknown; unknown

```console
$ docker pull nats@sha256:409730408a05c6b7c29cd2d9b79e803353c9bbbff4464e04d6a50d2d386bf574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 KB (14713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbc3102ff081b3780f5a927ffd0058fa22ee80e5afb023c3e6fe8c2159d0698e`

```dockerfile
```

-	Layers:
	-	`sha256:3fef583e358f058c5506e42e759c5763fdf1c3edc3e284872bb1d4f0657a121b`  
		Last Modified: Mon, 22 Sep 2025 20:57:01 GMT  
		Size: 14.7 KB (14713 bytes)  
		MIME: application/vnd.in-toto+json
