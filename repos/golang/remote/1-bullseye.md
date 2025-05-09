## `golang:1-bullseye`

```console
$ docker pull golang@sha256:9cf2ca5977b21567c301d2528fc329b1ef1a6e391a50c48f4383feb9019b3a9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `golang:1-bullseye` - linux; amd64

```console
$ docker pull golang@sha256:a5216c6bcd1deadaeba9bf451c8a05fee2e3d2748c005e3da1ad4c8043665fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.0 MB (294962111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca3c50fe705175f30c8ce6133fd1b86e147a10cef7fe71726fa6ae00eb7f0001`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 18:58:00 GMT
ENV GOLANG_VERSION=1.24.3
# Tue, 06 May 2025 18:58:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 May 2025 18:58:00 GMT
ENV GOPATH=/go
# Tue, 06 May 2025 18:58:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 18:58:00 GMT
COPY /target/ / # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 May 2025 18:58:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Thu, 08 May 2025 17:04:45 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee1ef79bfdcd8777f441528bcffb7a16f7a3d0852661baef04456810160e792`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 15.8 MB (15763544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68201ec6e5815a0906ce41187e7e52419a2d2c28d73d199e7612f268f81bbc35`  
		Last Modified: Thu, 08 May 2025 17:04:55 GMT  
		Size: 54.8 MB (54756006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a94610d81a971d8098bf16fa9f78b4f0f5c09e8ff7670cfaae8bd1a58ddeab`  
		Last Modified: Thu, 08 May 2025 17:05:08 GMT  
		Size: 91.7 MB (91713090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b00dc8dfbaa6cd7e39d09d4f1c726259b4d9a29c697192955da032f472d642`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 79.0 MB (78981573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89a7037037deaf63a75df0f62ce0c9d834b005765d57303ab7ced6d1681b77b`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:8106490d207c72616c943521c5e26c86d65c584ae8b23a72ad24795f804c69bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10293186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785a005a1061c21e56daf8f4d6ae200b9e9fedab1c209b1a9e9815ac497fbda8`

```dockerfile
```

-	Layers:
	-	`sha256:67df1d57fa9d7904f947d87de88dfe8747a219ab7243e6b56282be090b3b011a`  
		Last Modified: Fri, 09 May 2025 07:58:56 GMT  
		Size: 10.3 MB (10266718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7206aae1ab9bff9c27ac4336f3bd14bc6c04b26a9f399b8254940589eceee36c`  
		Last Modified: Fri, 09 May 2025 07:58:55 GMT  
		Size: 26.5 KB (26468 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:d9bef4f7df0070a543ca427260550a47df59bd90161e265148f3bf91a8781f1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.6 MB (256611531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a1fee4d0ea04eb99c96fd56ba6b27337bf1a14678f1bc41d03e581a066f1aef`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 18:58:00 GMT
ENV GOLANG_VERSION=1.24.3
# Tue, 06 May 2025 18:58:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 May 2025 18:58:00 GMT
ENV GOPATH=/go
# Tue, 06 May 2025 18:58:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 18:58:00 GMT
COPY /target/ / # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 May 2025 18:58:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:72fa46f1d669ee2de1ffbc36b654bfe8dd0aad49156f4143a5d9edd3a5c3d559`  
		Last Modified: Thu, 08 May 2025 17:18:11 GMT  
		Size: 49.0 MB (49040048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de64850f276e76efd1e91be51cb4b2577218e49bf52707b1bf6de3be76028cd8`  
		Last Modified: Thu, 08 May 2025 20:08:04 GMT  
		Size: 14.9 MB (14879026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc4cecedb434598f97e33a3320b6af6e1676388e6c13b31f0aab4b7c9372012`  
		Last Modified: Thu, 08 May 2025 20:08:14 GMT  
		Size: 50.6 MB (50625161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dc7e83fbdf292bf0238a22da7ed8a7b954d4a791ff1772973394bf28d278ed`  
		Last Modified: Thu, 08 May 2025 20:08:17 GMT  
		Size: 64.9 MB (64922699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f32012e82345c04270d988b1e520857596a775a43ec4b22744ab73bea39d15b`  
		Last Modified: Thu, 08 May 2025 17:05:42 GMT  
		Size: 77.1 MB (77144440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba0fab76309cedc1f1725a8ee8c303fb2414ae4abfb4ba44cbe1c9f294f2e6a`  
		Last Modified: Fri, 09 May 2025 05:00:36 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:cf513273a6120efc8567ebe2b58f90b0f88b85f4b429591aa590124f2eeb926c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10098407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d9c9661023cf500cc694cf3314bed5064cb1807c261e9275389167a0f5c937b`

```dockerfile
```

-	Layers:
	-	`sha256:c5789fb009e09bd1447ecf5d6d97b03c8328c7d980a9541eb8d3d6b002139f42`  
		Last Modified: Fri, 09 May 2025 07:59:07 GMT  
		Size: 10.1 MB (10071837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:773b8cf1567e1fdfef55ca559d0c20cb4ec2fdbd6146d7aa30231c87b51b3a66`  
		Last Modified: Fri, 09 May 2025 07:59:06 GMT  
		Size: 26.6 KB (26570 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:cd43396a4113b21e831c58c5c2b26a41ee942ccbcc9820d3f9ae22b69159fba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 MB (279489927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52f75e6eff2ff925e76a407b344b0c045d4ee155390ddb328fbe3284dcd9321f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 18:58:00 GMT
ENV GOLANG_VERSION=1.24.3
# Tue, 06 May 2025 18:58:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 May 2025 18:58:00 GMT
ENV GOPATH=/go
# Tue, 06 May 2025 18:58:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 18:58:00 GMT
COPY /target/ / # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 May 2025 18:58:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Thu, 08 May 2025 17:08:39 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4b10bbe754ef0579f7ae8162881d71484a39910114f01fdcee0bc53987fec1`  
		Last Modified: Thu, 08 May 2025 17:09:23 GMT  
		Size: 15.7 MB (15749108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b30b3b7ef57604d52a4f287f3a1202fa7094c2c34ba89e66f13f2ef75a47ae`  
		Last Modified: Thu, 08 May 2025 17:09:26 GMT  
		Size: 54.9 MB (54850001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8c6322f6933d3c7c501627d667e914654793c3d67e2daa5122b6519e08d8af`  
		Last Modified: Thu, 08 May 2025 17:09:40 GMT  
		Size: 81.4 MB (81414127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae64884db43f30f8dbc9ec3362124d99c8bad23b957254ac52fb30413bd14a7`  
		Last Modified: Thu, 08 May 2025 17:04:53 GMT  
		Size: 75.2 MB (75230554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fea7092f52a888d967904f6fa489ec3ef38650982185dba25f239783ce10f08`  
		Last Modified: Thu, 08 May 2025 17:10:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:4a380a7beca56a27f760753d75d96752f648b3a5f2ee29cbb9016bc14fb92266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10293675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d74cb17144ca6558cd6a9b9437353350751a07d1f4ca8b21a13e48347654c90`

```dockerfile
```

-	Layers:
	-	`sha256:c76b97eb77fefb79a5fc167ff1aed982e36634f6dd4ad47cd63da366e10ae501`  
		Last Modified: Fri, 09 May 2025 07:59:18 GMT  
		Size: 10.3 MB (10267073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b917759a94f163ff774c39f58ab6d4c1acf5f339d9036e0b5f38f47f96622502`  
		Last Modified: Fri, 09 May 2025 07:59:17 GMT  
		Size: 26.6 KB (26602 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bullseye` - linux; 386

```console
$ docker pull golang@sha256:830849770a07cf089cc88ccce455ed825900696b6ac639273ca0df59ddf7ed30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.6 MB (296608437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c560dfb4898a4061ffa06a7a9fa5fbbb34035784068d442473aa5c9e61f53ee8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 May 2025 18:58:00 GMT
ENV GOLANG_VERSION=1.24.3
# Tue, 06 May 2025 18:58:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 May 2025 18:58:00 GMT
ENV GOPATH=/go
# Tue, 06 May 2025 18:58:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 18:58:00 GMT
COPY /target/ / # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 May 2025 18:58:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4ef50a397f2c0106a3e44d1d1bae16cf52fb5e7e855c588f4098e281321c3e7b`  
		Last Modified: Thu, 08 May 2025 17:55:44 GMT  
		Size: 54.7 MB (54683102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbb48ef4c334135b55fe5dd328911059bfd41eec15edf03ff0ab96ca44fb6a1`  
		Last Modified: Thu, 08 May 2025 20:09:54 GMT  
		Size: 16.3 MB (16267399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229f9ff435d5a831802e386be1d29f22419a5d3951a76711fcdfc9f9bad0e6e3`  
		Last Modified: Thu, 08 May 2025 20:10:01 GMT  
		Size: 56.0 MB (56047280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97a4cff90005552a3c86543c53c96918c351c9c36ff6e5be4337a6dc4c6cfcf`  
		Last Modified: Fri, 09 May 2025 07:59:32 GMT  
		Size: 92.7 MB (92710619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db714197af43811f01d03462392675e848884e82b9483811c21c83a08d3e7834`  
		Last Modified: Thu, 08 May 2025 17:05:08 GMT  
		Size: 76.9 MB (76899879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8030f67f60fe3316f4a8e4f11e8eed6f8b937404125c215a1dd3dbbf4b7eb28`  
		Last Modified: Fri, 09 May 2025 07:59:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:41522df11d37bf0012cb2047cef2c1de1b16bd8c3c5081aa9b4a9d5850471c47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10282934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9133ea8c4e74eda942f2a6aa2f95f9648a9f49ac41011afdbe23a005fe9a3e14`

```dockerfile
```

-	Layers:
	-	`sha256:6e4a3e23ddd4247210bbb47eb3be0f40867a175d338d74351bb211bbcb2504d3`  
		Last Modified: Fri, 09 May 2025 07:59:39 GMT  
		Size: 10.3 MB (10256503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd8fbb6d341f2bbd710966c29461c2d1345862421c8493b78fa521b5d26bf895`  
		Last Modified: Fri, 09 May 2025 07:59:38 GMT  
		Size: 26.4 KB (26431 bytes)  
		MIME: application/vnd.in-toto+json
