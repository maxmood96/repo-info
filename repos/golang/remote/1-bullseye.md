## `golang:1-bullseye`

```console
$ docker pull golang@sha256:dfa24f4e2a5422a2e8d09a3fa3928c2a0424524bd0db93358b39c8ec0e00e2a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:1-bullseye` - linux; amd64

```console
$ docker pull golang@sha256:66907aebbd96ee2e40567e1bc729ffe80e8f4f6ac9d458f7f2ba3881caf953ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.4 MB (285361936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48f8b7439c53d7753bbee1667ccb0d4a90fbcdbd7d0e1c58cd3b74df51a5ffa2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:20:29 GMT
ADD file:6648a8158bbf4a36244eb9e936fbed4ea29f2f090fb0a97a6a737be2d85a5333 in / 
# Tue, 13 Aug 2024 00:20:30 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:44:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 00:44:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 17:10:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOLANG_VERSION=1.23.0
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOPATH=/go
# Tue, 13 Aug 2024 17:10:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 17:10:31 GMT
COPY /target/ / # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3438c04e457d7cf49dfbfe92aa9c64df2c0d9dc8ac53a7dbda0c620c405d9f`  
		Last Modified: Tue, 13 Aug 2024 00:50:52 GMT  
		Size: 15.8 MB (15764253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6665b6f4bd774e6a4c9738f0532ee622cf3bc07679e5a4449ba05c1f395e4f75`  
		Last Modified: Tue, 13 Aug 2024 00:51:07 GMT  
		Size: 54.6 MB (54588802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c67c0e0bb78afb601cf7688e9a0844cc84a3eccb605fbc2002977385888e1d`  
		Last Modified: Tue, 13 Aug 2024 20:02:41 GMT  
		Size: 86.0 MB (85958730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b14fb4020d7e427735797bf663a02a5a028e40fae0f8993ed5dfe75f15417a`  
		Last Modified: Tue, 13 Aug 2024 20:02:18 GMT  
		Size: 74.0 MB (73965318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647bf4d5f4747f519416a62e335f580a6f6a4eec29a33b32309bdd0d55840b48`  
		Last Modified: Tue, 13 Aug 2024 20:02:39 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:1636d7f5d4480bbfe895aa466c09ffc3ad3d5658bac818024c89c582459a67c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10281383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc940ed5b8bd67e21f62e99b2784c94bc8b1e10a1f6aa2105ab85a92cb4fbca`

```dockerfile
```

-	Layers:
	-	`sha256:7afe8a9310222070ca6ed9fafe2e940c8df2889e5d2446a6427433f237534a0b`  
		Last Modified: Tue, 13 Aug 2024 20:02:39 GMT  
		Size: 10.3 MB (10255034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ca98da8a343d1b5524597e1907088b5ac2d9cc07adee225c741a094950b28d5`  
		Last Modified: Tue, 13 Aug 2024 20:02:38 GMT  
		Size: 26.3 KB (26349 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:6951a314f8134f3de569728bcb92d8717a79317e75f0e20486e1d8a120b1589b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.5 MB (252485569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8e9b30f54f7465a15929ed39f96c110452631d17aa2a7cef9864a43fade27c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:57:45 GMT
ADD file:7674761630f1c6dfdf95da576bd19dbfe7bc4d942d11d31eff2012ec8b2c7ff1 in / 
# Tue, 13 Aug 2024 00:57:45 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:25:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:26:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 17:10:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOLANG_VERSION=1.23.0
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOPATH=/go
# Tue, 13 Aug 2024 17:10:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 17:10:31 GMT
COPY /target/ / # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a986643b6b9d356e3c44ee35fdd352a1064e1fb2a1524c0627e84ba34207b8e2`  
		Last Modified: Tue, 13 Aug 2024 01:01:15 GMT  
		Size: 50.2 MB (50242333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8868560f8e978ee832f67027b7330376be350ffacd30a199b730c72d9550757`  
		Last Modified: Tue, 13 Aug 2024 01:33:28 GMT  
		Size: 14.9 MB (14879497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7deb3ed53b620f0871f5051050fe0d850fd52da94803425820e75bb7b8d4e2e`  
		Last Modified: Tue, 13 Aug 2024 01:33:45 GMT  
		Size: 50.4 MB (50357748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1643dd34ded149a805ac35a064b9b839f8d6c57bbd3669535881a455fcb86305`  
		Last Modified: Tue, 13 Aug 2024 11:31:56 GMT  
		Size: 64.9 MB (64878285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc6363114f7204e8b9cd3cb47febe5a3082ffb85a82d8c47efb0021f3f9323f`  
		Last Modified: Wed, 14 Aug 2024 01:59:55 GMT  
		Size: 72.1 MB (72127549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fcc933875f5060f89baeae5b1b5c6954bbd9741d38d62160d6872f0494e5f53`  
		Last Modified: Wed, 14 Aug 2024 02:00:50 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:92d098e1fa4ad31f88bb74daa1f47777769cc63e759a8943bfd8ef73e7fbc4e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10088028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:818e85a236e43efe77d115d88f63c7e4782f94590a9fdbda904e527a8c9ab9ca`

```dockerfile
```

-	Layers:
	-	`sha256:fb300a5eee3be36d736e405b680c9972932cf05e21a5878654dd502420a6e6a0`  
		Last Modified: Wed, 14 Aug 2024 02:00:50 GMT  
		Size: 10.1 MB (10061584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b44e2b0cb14c3663c8dda6e4596d82d4ef68cf3198eeeda36e22ac402ee094eb`  
		Last Modified: Wed, 14 Aug 2024 02:00:49 GMT  
		Size: 26.4 KB (26444 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:a32cde79bccdc89a01ff240889523eda8e0442fddadd40e965f1b574cda04764
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.1 MB (276148757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87f0914bbaf74120823036626d992a585234ba280dca7a0e85572c22bb5a0bad`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:58 GMT
ADD file:4a2aa1b23402547c558d14f98384342f2e98460b659cd211609373f5408e83bc in / 
# Tue, 13 Aug 2024 00:39:58 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:03:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:04:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 17:10:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOLANG_VERSION=1.23.0
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOPATH=/go
# Tue, 13 Aug 2024 17:10:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 17:10:31 GMT
COPY /target/ / # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5d8903d6126c38fefcb1196b9998da0798f56cbdf18a91c00d822144c232af6b`  
		Last Modified: Tue, 13 Aug 2024 00:43:03 GMT  
		Size: 53.7 MB (53729921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3db3ee6245513b1422983db21d89f4f743f300e726af9eff6c9f7e2dddcb67`  
		Last Modified: Tue, 13 Aug 2024 01:10:18 GMT  
		Size: 15.7 MB (15749505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5265d6983e8ed11fd8dc48e17209d3479015214ac92f89f4ac51b2e65060840`  
		Last Modified: Tue, 13 Aug 2024 01:10:33 GMT  
		Size: 54.7 MB (54694302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27e7d7a79feec231823b511ba25c01901672406c5080ad01bb2c4fca2b07975`  
		Last Modified: Tue, 13 Aug 2024 21:37:22 GMT  
		Size: 81.4 MB (81366956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f9ed64c24993ada6c5d1b00ea7fbf5720c6cc30c9ae14d18134989fa7a08a7`  
		Last Modified: Tue, 13 Aug 2024 21:36:27 GMT  
		Size: 70.6 MB (70607916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1916d45749e32b21b8df0751b6b03f4e4d164f16aa96c383a65fe3f7a0ad2580`  
		Last Modified: Tue, 13 Aug 2024 21:37:20 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:9298f6ec93276ddcabbc0fdc08c3c5ff9ab2ddfbe81314768290eb8f51cc7f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10283403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeed45cca2f23088c46062aca8cb1f7dc874786ecaf8e46db339cd95583da157`

```dockerfile
```

-	Layers:
	-	`sha256:7157aa7d0488244bb214cc44da61b8d29611e0ef603b8448d1fae7d024982906`  
		Last Modified: Tue, 13 Aug 2024 21:37:20 GMT  
		Size: 10.3 MB (10256738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4021c67abbecd4331eb5558501e745fabcb1d935ccbf480a3e33f7fd3b575b8`  
		Last Modified: Tue, 13 Aug 2024 21:37:20 GMT  
		Size: 26.7 KB (26665 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; 386

```console
$ docker pull golang@sha256:fa6a22ef0537e56e275b3132ccc0c0a5d963683dd4062d66befd9c4c782b87da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.5 MB (287509150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb098f263bf4689c46d156e4ed84c1f274e64f5723edee95bacb8fa48a4a293`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:06 GMT
ADD file:b4823f40fb9693690d7dfe07f6179ae1ea0a288d8912f4f8365d372e27134f0e in / 
# Tue, 13 Aug 2024 00:39:07 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:07:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:07:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 17:10:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOLANG_VERSION=1.23.0
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOPATH=/go
# Tue, 13 Aug 2024 17:10:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 17:10:31 GMT
COPY /target/ / # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c99355adbbcd3ac4e44cd6fb2596fed1658ea87be87df9894ec5aaf076a548b2`  
		Last Modified: Tue, 13 Aug 2024 00:42:55 GMT  
		Size: 56.1 MB (56074104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d740897ef0cfebeecea08cfc67998814e44c45164f9dc7c044e9e2a0507541f4`  
		Last Modified: Tue, 13 Aug 2024 01:15:00 GMT  
		Size: 16.3 MB (16267943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dab982039e3c0ad98af0fa361fb64e7b9635b80923dca6744c230e0994f2bf3`  
		Last Modified: Tue, 13 Aug 2024 01:15:21 GMT  
		Size: 55.9 MB (55927707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68bd7e6d073a2deca8ca3a91bb92ccc196293e1db29e8940c19e6b444b312d0`  
		Last Modified: Tue, 13 Aug 2024 20:02:44 GMT  
		Size: 87.4 MB (87382605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948a02128519d4902024135fc03b12145f389fd4b2b393eb6499f6f10486bc83`  
		Last Modified: Tue, 13 Aug 2024 20:02:22 GMT  
		Size: 71.9 MB (71856633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0445d3061e561d913d286255c313b2434c6e44870395a776d8ca131baf653b2d`  
		Last Modified: Tue, 13 Aug 2024 20:02:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:41a388e08b5235e36f9953a3abb42a34623bd1569f102e7cdb074dd435ea587b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10271348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52036da9fb7304b2a2be7927dfa7af20d710b6f1dabe101062dded83980f6577`

```dockerfile
```

-	Layers:
	-	`sha256:1a5614a8b4205e08d40b109520e49f37c908dcab82f148bc4faad24f3765cb91`  
		Last Modified: Tue, 13 Aug 2024 20:02:42 GMT  
		Size: 10.2 MB (10245032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66aaffcd50b7c2ee12528e5cc7c8ec99ab6ac748d7c06a6a937cc8e078cfeb46`  
		Last Modified: Tue, 13 Aug 2024 20:02:42 GMT  
		Size: 26.3 KB (26316 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; mips64le

```console
$ docker pull golang@sha256:917aa41eadb2c16a2b531696dec5f406e26641a50644666492ea29086b0a5f8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.5 MB (253536158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fccffa01b0a71dc4a19b6c8a960ad635fbdf4d717e2371bbbdd5f6fe4b32a274`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:38:26 GMT
ADD file:3fbf62974aea46ff67427fd8996563bef3939ff51df600b4914acf5abb0b6c51 in / 
# Tue, 23 Jul 2024 00:38:32 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:32:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 01:33:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Aug 2024 18:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOLANG_VERSION=1.22.6
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Aug 2024 18:18:42 GMT
ENV GOPATH=/go
# Tue, 06 Aug 2024 18:18:42 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Aug 2024 18:18:42 GMT
COPY /target/ / # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Aug 2024 18:18:42 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6fba1199d77f2795fad97ca84f3d7030aab307e1ee7b582027c4e146bacdff14`  
		Last Modified: Tue, 23 Jul 2024 00:49:50 GMT  
		Size: 53.3 MB (53310598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0646dddb656b3203c87e17a010db53fc72755b3570f3fc2647722af3c3b2e958`  
		Last Modified: Tue, 23 Jul 2024 02:02:00 GMT  
		Size: 15.7 MB (15734545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99842c367e8366da5cce8062955a8adc51f02bf39119fe6c706b6971d2a9d218`  
		Last Modified: Tue, 23 Jul 2024 02:02:48 GMT  
		Size: 53.3 MB (53311607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45f10704d6ef79317d15a1db10975d66729bcc302bbbcffb5416405dea7fd77`  
		Last Modified: Tue, 06 Aug 2024 23:04:03 GMT  
		Size: 67.1 MB (67053611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ec510b2b8fe8d60e2b414c455523b255d2db4e07537481fb550635278f8c2a`  
		Last Modified: Tue, 06 Aug 2024 23:00:16 GMT  
		Size: 64.1 MB (64125639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e190e6cab5fe1a35da8a17440579ffadcd82ac8b8daabe3c5a9f02f8ee7bd18`  
		Last Modified: Tue, 06 Aug 2024 23:03:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:6226f804c11f6136b4ebdd79441b651763d0033ce7d0880f45e854a88af7a731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:562da041bfe8737b6f4098c94e881828beb9795f17ecd2fbd6ab971c0d0e6dd3`

```dockerfile
```

-	Layers:
	-	`sha256:d3b428cce75a60cd71fcbde61c2014c0ac2268740547359c2dbbb75ce103a31b`  
		Last Modified: Tue, 06 Aug 2024 23:03:56 GMT  
		Size: 26.2 KB (26193 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; ppc64le

```console
$ docker pull golang@sha256:2578e4c21a891042d2ab0479932a5134756b8b5586f11d9b37f33600c10affca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285768949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a1ca0dd176443eb3758168a711e9f3dacab504703201fc5ee0228eb511287f5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:22:14 GMT
ADD file:25dc93c8090a0afba4b41321f81883857bfdd6b30ea9f278833c5a5d9d16ad52 in / 
# Tue, 13 Aug 2024 00:22:18 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:22:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:23:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 17:10:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOLANG_VERSION=1.23.0
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOPATH=/go
# Tue, 13 Aug 2024 17:10:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 17:10:31 GMT
COPY /target/ / # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:dad1c3eca3bf4b2a67cef1dbad507d7a913df7bbe1e3f88044230dd291ada39d`  
		Last Modified: Tue, 13 Aug 2024 00:26:46 GMT  
		Size: 59.0 MB (58954654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b50eef4accfc66462c4cf81c03bb57857b5f3ac891da5b87bfdf1ba826c9677`  
		Last Modified: Tue, 13 Aug 2024 01:36:03 GMT  
		Size: 16.8 MB (16765928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df0e65d951ce5d0b07cbb65477bbb01cfa607241b5c5855f4fb361bedfd1247`  
		Last Modified: Tue, 13 Aug 2024 01:36:21 GMT  
		Size: 58.9 MB (58872586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5da82bba9c777a861193f47fe8d6bc9c7445d28ffb8b38f9d7b5c1906f81409`  
		Last Modified: Tue, 13 Aug 2024 16:56:42 GMT  
		Size: 80.4 MB (80402682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00804d58ee01dde250ba214452343e0ba5cd0f3e98c64328395648d07b4df92`  
		Last Modified: Wed, 14 Aug 2024 00:13:23 GMT  
		Size: 70.8 MB (70772941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf44389c5afd3a224ac797d6934c81c4622d92665b9fb9cbe8a454580981f124`  
		Last Modified: Wed, 14 Aug 2024 00:14:29 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:48f90536d91126aafbc3ee09113d4b2c56fa7c3ef80dbee451ce23ec9f1552c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10247124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2356e330d1a15cfa0b29d0501705ae05366a804030fd129f8387544b95d568e`

```dockerfile
```

-	Layers:
	-	`sha256:eed5532da01b2198cd85c18fdb05f573132bda75b73eae60d481252295895a18`  
		Last Modified: Wed, 14 Aug 2024 00:14:29 GMT  
		Size: 10.2 MB (10220733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5aec5afdc7e913e1148367dd28bc23a93af0f20113e828c124d7dc4e76bb33ad`  
		Last Modified: Wed, 14 Aug 2024 00:14:28 GMT  
		Size: 26.4 KB (26391 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; s390x

```console
$ docker pull golang@sha256:d323eed8edfc8ae9ef2aa723913c926497bb627cc2d123489608ef094ab7fa35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261597301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:319b9e050d33ad6fb9486ef032599e61728ba907964ccf8f0f6cf91ee1c7c05a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:42:51 GMT
ADD file:993091e64467ec0ea9bcecdd744da64284d459b933863322bd011dd2111f47c1 in / 
# Tue, 13 Aug 2024 00:42:53 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:17:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:18:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 17:10:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOLANG_VERSION=1.23.0
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 13 Aug 2024 17:10:31 GMT
ENV GOPATH=/go
# Tue, 13 Aug 2024 17:10:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Aug 2024 17:10:31 GMT
COPY /target/ / # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 13 Aug 2024 17:10:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9c1a2da0ad07de8657187bee6e4fad1ff817bafdbac14fb77a3953cd7f50038c`  
		Last Modified: Tue, 13 Aug 2024 00:47:43 GMT  
		Size: 53.3 MB (53324089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c695efccb58000e04eb154deca02ce22ea52fd05ee4246281c66bb7a42d20a96`  
		Last Modified: Tue, 13 Aug 2024 01:25:32 GMT  
		Size: 15.6 MB (15641934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f3f87ffa253b4cb357637ad56494facf5bf533f6fd3bdf78f1066c6fb0fb23`  
		Last Modified: Tue, 13 Aug 2024 01:25:44 GMT  
		Size: 54.1 MB (54075217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b221ab5055e6a918a4e1c366fec50c506c9321c39753b3200e0078544b9667`  
		Last Modified: Tue, 13 Aug 2024 23:09:43 GMT  
		Size: 65.7 MB (65656693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d766dfa346f9569deddaa862bfcc6c453c61295fa0688cff4cf096f917447678`  
		Last Modified: Tue, 13 Aug 2024 23:07:38 GMT  
		Size: 72.9 MB (72899210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0793901093e9e38c2f74f79a13b9277ce352968977f2131779837101cc21045f`  
		Last Modified: Tue, 13 Aug 2024 23:09:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:b48ac46c888809fe774f709b8bb05c3abc1c8d05a4fd676dc773993073740e9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10110537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a471a3079c91aafd5c438a1e628106f1d07881794efe7767573f0b8b6ccff74`

```dockerfile
```

-	Layers:
	-	`sha256:2928b9b860349f01f75cc72e000fbc931bb17965eefcc42350bd78992f6da559`  
		Last Modified: Tue, 13 Aug 2024 23:09:42 GMT  
		Size: 10.1 MB (10084188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd6ea58e109686b37ad1a4e2acadb47dbcc62fb8622918d75f5eac7c78606b91`  
		Last Modified: Tue, 13 Aug 2024 23:09:42 GMT  
		Size: 26.3 KB (26349 bytes)  
		MIME: application/vnd.in-toto+json
