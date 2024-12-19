<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `registry`

-	[`registry:2`](#registry2)
-	[`registry:2.8`](#registry28)
-	[`registry:2.8.3`](#registry283)
-	[`registry:3.0.0-rc.2`](#registry300-rc2)
-	[`registry:latest`](#registrylatest)

## `registry:2`

```console
$ docker pull registry@sha256:543dade69668e02e5768d7ea2b0aa4fae6aa7384c9a5a8dbecc2be5136079ddb
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

### `registry:2` - linux; amd64

```console
$ docker pull registry@sha256:d252b0c9a9409bb1e10a98a6b79d8f2a082284a113bc33f49121bb2fb0797cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10114147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18a86d35e983225b84aae3bb15c84bd9e47506dd0102975c0ed97958703bb73`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-x86_64.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:dc0decf4841d19b14e836c2d82bd5cb9540fb5e0d1359549ca243f49036557e9`  
		Last Modified: Mon, 09 Sep 2024 07:02:43 GMT  
		Size: 3.4 MB (3416401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb0aa443e23aedd28f0818f7a18de9911383d0b9b621bc448070ded1d6c81c3`  
		Last Modified: Tue, 12 Nov 2024 02:37:06 GMT  
		Size: 293.4 KB (293379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813676e291ef88d6de121b9a67d4b546585c87f2b89df39d4fd14ba984cd655f`  
		Last Modified: Tue, 12 Nov 2024 02:37:06 GMT  
		Size: 6.4 MB (6403784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2fb7dcec6119c150b59df0550dc646f6a45351470a7b74f0a904df40418a12`  
		Last Modified: Tue, 12 Nov 2024 02:37:05 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916205650bfe545ec2ac378e84f53759e0c977a77e583f0525e05cf3c8923df5`  
		Last Modified: Tue, 12 Nov 2024 02:37:06 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:ef807d6ab3ae145cb40e6bc86fbd8de0fb6f4c6726ac88e619634da80dd35994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.1 KB (193072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e7ad24d9321d0ba3df236bcc6d5bf0a26dc6b4069c58745f6d491db169526b`

```dockerfile
```

-	Layers:
	-	`sha256:547ee2ce16efcc56c2f70e31f7327b246f129ae9e0e0f5393b19da960f910466`  
		Last Modified: Tue, 12 Nov 2024 02:37:06 GMT  
		Size: 179.0 KB (179007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8e019b81fd4a44bcc35582450d9aeddbdb46be2e2b6e0e5bd6cbe0dcc431d8b`  
		Last Modified: Tue, 12 Nov 2024 02:37:05 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; arm variant v6

```console
$ docker pull registry@sha256:8351e958c42f9de2b77889506fae68712813fb6bc5f4e1579cf103bec35d41b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9477718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646ed268fea06904233caf5921a317743a80856db79e456db3956b70cc1a7b1b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-armhf.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:1ce61877166753d951080511a4649a7a9674d00fdd71569057a7f3099f39e6d8`  
		Last Modified: Mon, 09 Sep 2024 07:02:44 GMT  
		Size: 3.2 MB (3158999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b739e776fe9e57644b5e4e99c00c4dbb4a039c894137288a095e5adcc3f78d8`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 294.0 KB (294026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5afee98ad80b18cdcc1e4f610c4b5f499b6c55c68ea75a4743e1e680fa910f4`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 6.0 MB (6024109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7f5e00a1807cf3e9f780608fcb4b45baf5e9735de16505b91749f287e31298`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3adbb8c5936d65b71c7da2c2cabe8705bd496d982f440619bbe8c594d5c3f02d`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:2d1adb226ba38d47f5571423f8a72ab46d1e47a64a2274c699f648077cb956dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 KB (13939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88f40fc59ce3d885eed54f4550aa108d5a9a860953d6fa19396d6bb55174da9`

```dockerfile
```

-	Layers:
	-	`sha256:5c26b5cde765c90b744538bf4a6ca95d05a2fb38fd9029fe5688ec806b0f1c18`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 13.9 KB (13939 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; arm variant v7

```console
$ docker pull registry@sha256:47ef7710ba9f4fbd700872c21eab27a5dfa893a0e0911715852cdd2868ef21df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9222173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6200c959b354647eaf359eec9856aba78d2f961b1429c5cdcfa94c358192dbf2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-armv7.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:7e2a8985a55f5e4f3b3ae472c5b93ce2792c73bcc72c5b6d704ccb5fb434a07b`  
		Last Modified: Mon, 09 Sep 2024 07:02:44 GMT  
		Size: 2.9 MB (2911454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2862979d3b8c65bc60344e1997591bded8ed142bd7fd405120128eca7f49ca44`  
		Last Modified: Tue, 12 Nov 2024 15:29:49 GMT  
		Size: 292.9 KB (292920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4518dd25cdc89f46b95212b0f8e670f000254dc3db5b67aade21b5b01391faa`  
		Last Modified: Tue, 12 Nov 2024 15:29:50 GMT  
		Size: 6.0 MB (6017216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636f5962f66761865cdcee4ec702fda4f4dbe8fb126939f83ec2992209d0b66f`  
		Last Modified: Tue, 12 Nov 2024 15:29:49 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a61ee3ce5af7f700529f55881a97ca5cebdc8c11c768d681b35e4bd9860c1c`  
		Last Modified: Tue, 12 Nov 2024 15:29:49 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:78b317756a86aa4c6aeb9088c93296bfaa48d4c4cbc06a0ca11c7fd65e62a6a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.2 KB (193197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72878d323f86f97f5c0701a676fd961d4b6c6a25d2f67b24461e2aaa011a824d`

```dockerfile
```

-	Layers:
	-	`sha256:e791e9085d9badcc51e175cf9eb345929d3837ee061f19a89772b55d1009f974`  
		Last Modified: Tue, 12 Nov 2024 15:29:49 GMT  
		Size: 179.0 KB (179043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:898f7fdd08c3b472b4e5cff35cbe6e5139db5eb1bc94259a80e14b98868bac1b`  
		Last Modified: Tue, 12 Nov 2024 15:29:49 GMT  
		Size: 14.2 KB (14154 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:1ef66c49c952ab0d20c905634d50d3a0da70133b0cdb52732a30a0fd89f01a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6adc34955df9f22da1fdc0474dcbab66dfce57ded89499201125f7dc1b9924`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-aarch64.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:0dfcae9cb3f09031e3687535f2d3e3c2f08533799b67ed61076e79e4ed1c7c4a`  
		Last Modified: Mon, 09 Sep 2024 07:02:44 GMT  
		Size: 3.3 MB (3340451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe29ef241d9fe87b99b77f4d96972773b3ae04f1a46c6fea0e0a60800f5f1e1`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 295.8 KB (295832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2787542bdb41f6b8315204be8ea01cb7ff82d9e6de97e9283e8af8dc6ce650e`  
		Last Modified: Tue, 12 Nov 2024 10:28:26 GMT  
		Size: 5.8 MB (5824734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b69fee0ac896543d4936d9c57aea16e665df781ec13ec5257f8bea258da7c79`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb2de197705d02128cc248e6540d752209fe9ed73a32bfb6b19947205030524`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:bbf9ae6a42e4d8aef2759420301cfcc7ed642ba200ae3bf030fd5fdb9d0d2a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.2 KB (193247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8bd06db3380d6a4af9f2d942917235c0df5b1a02aec67120ee470ae2e11a94`

```dockerfile
```

-	Layers:
	-	`sha256:1b1f1a3aa2b9f06c429988bbdfa0c781210c0d81d6befa0769051742b9607830`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 179.1 KB (179063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a601ce5a2c5491c5fd401d93594ecbf76515407f52ce37185f82be3efee56e04`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 14.2 KB (14184 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; ppc64le

```console
$ docker pull registry@sha256:86cdf44fa43a89e6031fc50e516d886c0b257f9f8463548218f7aa0cddca35a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9344901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe03a1f8a043cc0d142b1dbfc0701eb12d5888e6714d95ef5de3ee3f66c3637`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-ppc64le.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:bf19dcb5e2f7e7518032e1f3abc91f7a0f014fc0f3a03de278aca2c9a523ea4f`  
		Last Modified: Tue, 12 Nov 2024 00:56:06 GMT  
		Size: 3.4 MB (3358858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3792e3246e50751fd99db95bd81487f4ff267e527d2bdd744a8f15002029e84b`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 296.2 KB (296245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4725d46af85c7a6abba2419cef1cd0a36956cf13a020d059ba8751a3a0687006`  
		Last Modified: Tue, 12 Nov 2024 08:06:05 GMT  
		Size: 5.7 MB (5689215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a6f196c518d25b0537d6b92276855a0f837b6f99bc09e9cd2854e83070c872`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6030f6d937516639db015c42c56128b1c45f80405aa31d885d4e91fc8cd0ea17`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:63ebe77f6c587302b3a687db1d46b6b9e8b5d89b573cfc083d1f9dad199991b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 KB (191198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0e17de964dc185bfd1b49f65e7621e00c8c3a999513e31042bd22d6f293d26`

```dockerfile
```

-	Layers:
	-	`sha256:191655aad642e846fe9649b077d09cf1d11d1be5742cefe8be2036f8ceafe72f`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 177.1 KB (177087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47532ea0bac7cfc58e078cb792bdb9e1222186b96f8de6519bd95c04af4441b9`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 14.1 KB (14111 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2` - linux; s390x

```console
$ docker pull registry@sha256:cad4fdf4a03376ba0904fafcb75e16e3468c10f61e3c64a4cfbb372470c8b891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9684971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d7cccb184b781c20bdbb9ceff63cafb03db8074fdc32bac40da22617b729bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-s390x.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:2cf6287c29b40fb867eb63db5d7189724563e69538ef303e15274f8139042129`  
		Last Modified: Tue, 12 Nov 2024 00:56:53 GMT  
		Size: 3.2 MB (3230439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9149be30168d1b1aa8ec6b23c36dcdc39c2b2dcd978c5e0a2d8ca86109a0df7a`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 293.9 KB (293899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2ded3165ca2acf8ea3ca820d45d88d54ade5de9f1264cc65acbe94b26d0b26`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878ae226c4b32247c8b552259cd2ff67e2c68b8c6dfe9af0b0785d28d04a9618`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277269a6b2649ecc19571438083237ee6b8b605bcb79eb5d2de467a0ab86a175`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2` - unknown; unknown

```console
$ docker pull registry@sha256:1c55fb5b8a1b682c0cb9ca173aa7fd36a7a8a0686c87592d298c085ba1bf31c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 KB (191118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8431cec168c6e8aeb1395b10dad52b6f9cdcadef36d4c1b5a36532ee574595ad`

```dockerfile
```

-	Layers:
	-	`sha256:7068d24c38f441b8c1a3dca81bc616b32e4c6eea0489aa2e68837a2b1d02973c`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 177.1 KB (177053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5953f2e3297796f4051786b247167696c4fdc409fca54425806f0ac4df56219`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:2.8`

```console
$ docker pull registry@sha256:543dade69668e02e5768d7ea2b0aa4fae6aa7384c9a5a8dbecc2be5136079ddb
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

### `registry:2.8` - linux; amd64

```console
$ docker pull registry@sha256:d252b0c9a9409bb1e10a98a6b79d8f2a082284a113bc33f49121bb2fb0797cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10114147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18a86d35e983225b84aae3bb15c84bd9e47506dd0102975c0ed97958703bb73`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-x86_64.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:dc0decf4841d19b14e836c2d82bd5cb9540fb5e0d1359549ca243f49036557e9`  
		Last Modified: Mon, 09 Sep 2024 07:02:43 GMT  
		Size: 3.4 MB (3416401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb0aa443e23aedd28f0818f7a18de9911383d0b9b621bc448070ded1d6c81c3`  
		Last Modified: Tue, 12 Nov 2024 02:37:06 GMT  
		Size: 293.4 KB (293379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813676e291ef88d6de121b9a67d4b546585c87f2b89df39d4fd14ba984cd655f`  
		Last Modified: Tue, 12 Nov 2024 02:37:06 GMT  
		Size: 6.4 MB (6403784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2fb7dcec6119c150b59df0550dc646f6a45351470a7b74f0a904df40418a12`  
		Last Modified: Tue, 12 Nov 2024 02:37:05 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916205650bfe545ec2ac378e84f53759e0c977a77e583f0525e05cf3c8923df5`  
		Last Modified: Tue, 12 Nov 2024 02:37:06 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:ef807d6ab3ae145cb40e6bc86fbd8de0fb6f4c6726ac88e619634da80dd35994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.1 KB (193072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e7ad24d9321d0ba3df236bcc6d5bf0a26dc6b4069c58745f6d491db169526b`

```dockerfile
```

-	Layers:
	-	`sha256:547ee2ce16efcc56c2f70e31f7327b246f129ae9e0e0f5393b19da960f910466`  
		Last Modified: Tue, 12 Nov 2024 02:37:06 GMT  
		Size: 179.0 KB (179007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8e019b81fd4a44bcc35582450d9aeddbdb46be2e2b6e0e5bd6cbe0dcc431d8b`  
		Last Modified: Tue, 12 Nov 2024 02:37:05 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; arm variant v6

```console
$ docker pull registry@sha256:8351e958c42f9de2b77889506fae68712813fb6bc5f4e1579cf103bec35d41b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9477718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646ed268fea06904233caf5921a317743a80856db79e456db3956b70cc1a7b1b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-armhf.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:1ce61877166753d951080511a4649a7a9674d00fdd71569057a7f3099f39e6d8`  
		Last Modified: Mon, 09 Sep 2024 07:02:44 GMT  
		Size: 3.2 MB (3158999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b739e776fe9e57644b5e4e99c00c4dbb4a039c894137288a095e5adcc3f78d8`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 294.0 KB (294026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5afee98ad80b18cdcc1e4f610c4b5f499b6c55c68ea75a4743e1e680fa910f4`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 6.0 MB (6024109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7f5e00a1807cf3e9f780608fcb4b45baf5e9735de16505b91749f287e31298`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3adbb8c5936d65b71c7da2c2cabe8705bd496d982f440619bbe8c594d5c3f02d`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:2d1adb226ba38d47f5571423f8a72ab46d1e47a64a2274c699f648077cb956dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 KB (13939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88f40fc59ce3d885eed54f4550aa108d5a9a860953d6fa19396d6bb55174da9`

```dockerfile
```

-	Layers:
	-	`sha256:5c26b5cde765c90b744538bf4a6ca95d05a2fb38fd9029fe5688ec806b0f1c18`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 13.9 KB (13939 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; arm variant v7

```console
$ docker pull registry@sha256:47ef7710ba9f4fbd700872c21eab27a5dfa893a0e0911715852cdd2868ef21df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9222173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6200c959b354647eaf359eec9856aba78d2f961b1429c5cdcfa94c358192dbf2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-armv7.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:7e2a8985a55f5e4f3b3ae472c5b93ce2792c73bcc72c5b6d704ccb5fb434a07b`  
		Last Modified: Mon, 09 Sep 2024 07:02:44 GMT  
		Size: 2.9 MB (2911454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2862979d3b8c65bc60344e1997591bded8ed142bd7fd405120128eca7f49ca44`  
		Last Modified: Tue, 12 Nov 2024 15:29:49 GMT  
		Size: 292.9 KB (292920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4518dd25cdc89f46b95212b0f8e670f000254dc3db5b67aade21b5b01391faa`  
		Last Modified: Tue, 12 Nov 2024 15:29:50 GMT  
		Size: 6.0 MB (6017216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636f5962f66761865cdcee4ec702fda4f4dbe8fb126939f83ec2992209d0b66f`  
		Last Modified: Tue, 12 Nov 2024 15:29:49 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a61ee3ce5af7f700529f55881a97ca5cebdc8c11c768d681b35e4bd9860c1c`  
		Last Modified: Tue, 12 Nov 2024 15:29:49 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:78b317756a86aa4c6aeb9088c93296bfaa48d4c4cbc06a0ca11c7fd65e62a6a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.2 KB (193197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72878d323f86f97f5c0701a676fd961d4b6c6a25d2f67b24461e2aaa011a824d`

```dockerfile
```

-	Layers:
	-	`sha256:e791e9085d9badcc51e175cf9eb345929d3837ee061f19a89772b55d1009f974`  
		Last Modified: Tue, 12 Nov 2024 15:29:49 GMT  
		Size: 179.0 KB (179043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:898f7fdd08c3b472b4e5cff35cbe6e5139db5eb1bc94259a80e14b98868bac1b`  
		Last Modified: Tue, 12 Nov 2024 15:29:49 GMT  
		Size: 14.2 KB (14154 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:1ef66c49c952ab0d20c905634d50d3a0da70133b0cdb52732a30a0fd89f01a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6adc34955df9f22da1fdc0474dcbab66dfce57ded89499201125f7dc1b9924`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-aarch64.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:0dfcae9cb3f09031e3687535f2d3e3c2f08533799b67ed61076e79e4ed1c7c4a`  
		Last Modified: Mon, 09 Sep 2024 07:02:44 GMT  
		Size: 3.3 MB (3340451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe29ef241d9fe87b99b77f4d96972773b3ae04f1a46c6fea0e0a60800f5f1e1`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 295.8 KB (295832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2787542bdb41f6b8315204be8ea01cb7ff82d9e6de97e9283e8af8dc6ce650e`  
		Last Modified: Tue, 12 Nov 2024 10:28:26 GMT  
		Size: 5.8 MB (5824734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b69fee0ac896543d4936d9c57aea16e665df781ec13ec5257f8bea258da7c79`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb2de197705d02128cc248e6540d752209fe9ed73a32bfb6b19947205030524`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:bbf9ae6a42e4d8aef2759420301cfcc7ed642ba200ae3bf030fd5fdb9d0d2a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.2 KB (193247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8bd06db3380d6a4af9f2d942917235c0df5b1a02aec67120ee470ae2e11a94`

```dockerfile
```

-	Layers:
	-	`sha256:1b1f1a3aa2b9f06c429988bbdfa0c781210c0d81d6befa0769051742b9607830`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 179.1 KB (179063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a601ce5a2c5491c5fd401d93594ecbf76515407f52ce37185f82be3efee56e04`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 14.2 KB (14184 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; ppc64le

```console
$ docker pull registry@sha256:86cdf44fa43a89e6031fc50e516d886c0b257f9f8463548218f7aa0cddca35a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9344901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe03a1f8a043cc0d142b1dbfc0701eb12d5888e6714d95ef5de3ee3f66c3637`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-ppc64le.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:bf19dcb5e2f7e7518032e1f3abc91f7a0f014fc0f3a03de278aca2c9a523ea4f`  
		Last Modified: Tue, 12 Nov 2024 00:56:06 GMT  
		Size: 3.4 MB (3358858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3792e3246e50751fd99db95bd81487f4ff267e527d2bdd744a8f15002029e84b`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 296.2 KB (296245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4725d46af85c7a6abba2419cef1cd0a36956cf13a020d059ba8751a3a0687006`  
		Last Modified: Tue, 12 Nov 2024 08:06:05 GMT  
		Size: 5.7 MB (5689215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a6f196c518d25b0537d6b92276855a0f837b6f99bc09e9cd2854e83070c872`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6030f6d937516639db015c42c56128b1c45f80405aa31d885d4e91fc8cd0ea17`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:63ebe77f6c587302b3a687db1d46b6b9e8b5d89b573cfc083d1f9dad199991b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 KB (191198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0e17de964dc185bfd1b49f65e7621e00c8c3a999513e31042bd22d6f293d26`

```dockerfile
```

-	Layers:
	-	`sha256:191655aad642e846fe9649b077d09cf1d11d1be5742cefe8be2036f8ceafe72f`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 177.1 KB (177087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47532ea0bac7cfc58e078cb792bdb9e1222186b96f8de6519bd95c04af4441b9`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 14.1 KB (14111 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8` - linux; s390x

```console
$ docker pull registry@sha256:cad4fdf4a03376ba0904fafcb75e16e3468c10f61e3c64a4cfbb372470c8b891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9684971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d7cccb184b781c20bdbb9ceff63cafb03db8074fdc32bac40da22617b729bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-s390x.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:2cf6287c29b40fb867eb63db5d7189724563e69538ef303e15274f8139042129`  
		Last Modified: Tue, 12 Nov 2024 00:56:53 GMT  
		Size: 3.2 MB (3230439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9149be30168d1b1aa8ec6b23c36dcdc39c2b2dcd978c5e0a2d8ca86109a0df7a`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 293.9 KB (293899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2ded3165ca2acf8ea3ca820d45d88d54ade5de9f1264cc65acbe94b26d0b26`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878ae226c4b32247c8b552259cd2ff67e2c68b8c6dfe9af0b0785d28d04a9618`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277269a6b2649ecc19571438083237ee6b8b605bcb79eb5d2de467a0ab86a175`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8` - unknown; unknown

```console
$ docker pull registry@sha256:1c55fb5b8a1b682c0cb9ca173aa7fd36a7a8a0686c87592d298c085ba1bf31c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 KB (191118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8431cec168c6e8aeb1395b10dad52b6f9cdcadef36d4c1b5a36532ee574595ad`

```dockerfile
```

-	Layers:
	-	`sha256:7068d24c38f441b8c1a3dca81bc616b32e4c6eea0489aa2e68837a2b1d02973c`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 177.1 KB (177053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5953f2e3297796f4051786b247167696c4fdc409fca54425806f0ac4df56219`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:2.8.3`

```console
$ docker pull registry@sha256:543dade69668e02e5768d7ea2b0aa4fae6aa7384c9a5a8dbecc2be5136079ddb
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

### `registry:2.8.3` - linux; amd64

```console
$ docker pull registry@sha256:d252b0c9a9409bb1e10a98a6b79d8f2a082284a113bc33f49121bb2fb0797cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10114147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18a86d35e983225b84aae3bb15c84bd9e47506dd0102975c0ed97958703bb73`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-x86_64.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:dc0decf4841d19b14e836c2d82bd5cb9540fb5e0d1359549ca243f49036557e9`  
		Last Modified: Mon, 09 Sep 2024 07:02:43 GMT  
		Size: 3.4 MB (3416401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb0aa443e23aedd28f0818f7a18de9911383d0b9b621bc448070ded1d6c81c3`  
		Last Modified: Tue, 12 Nov 2024 02:37:06 GMT  
		Size: 293.4 KB (293379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813676e291ef88d6de121b9a67d4b546585c87f2b89df39d4fd14ba984cd655f`  
		Last Modified: Tue, 12 Nov 2024 02:37:06 GMT  
		Size: 6.4 MB (6403784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2fb7dcec6119c150b59df0550dc646f6a45351470a7b74f0a904df40418a12`  
		Last Modified: Tue, 12 Nov 2024 02:37:05 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916205650bfe545ec2ac378e84f53759e0c977a77e583f0525e05cf3c8923df5`  
		Last Modified: Tue, 12 Nov 2024 02:37:06 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:ef807d6ab3ae145cb40e6bc86fbd8de0fb6f4c6726ac88e619634da80dd35994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.1 KB (193072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e7ad24d9321d0ba3df236bcc6d5bf0a26dc6b4069c58745f6d491db169526b`

```dockerfile
```

-	Layers:
	-	`sha256:547ee2ce16efcc56c2f70e31f7327b246f129ae9e0e0f5393b19da960f910466`  
		Last Modified: Tue, 12 Nov 2024 02:37:06 GMT  
		Size: 179.0 KB (179007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8e019b81fd4a44bcc35582450d9aeddbdb46be2e2b6e0e5bd6cbe0dcc431d8b`  
		Last Modified: Tue, 12 Nov 2024 02:37:05 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; arm variant v6

```console
$ docker pull registry@sha256:8351e958c42f9de2b77889506fae68712813fb6bc5f4e1579cf103bec35d41b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9477718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646ed268fea06904233caf5921a317743a80856db79e456db3956b70cc1a7b1b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-armhf.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:1ce61877166753d951080511a4649a7a9674d00fdd71569057a7f3099f39e6d8`  
		Last Modified: Mon, 09 Sep 2024 07:02:44 GMT  
		Size: 3.2 MB (3158999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b739e776fe9e57644b5e4e99c00c4dbb4a039c894137288a095e5adcc3f78d8`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 294.0 KB (294026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5afee98ad80b18cdcc1e4f610c4b5f499b6c55c68ea75a4743e1e680fa910f4`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 6.0 MB (6024109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7f5e00a1807cf3e9f780608fcb4b45baf5e9735de16505b91749f287e31298`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3adbb8c5936d65b71c7da2c2cabe8705bd496d982f440619bbe8c594d5c3f02d`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:2d1adb226ba38d47f5571423f8a72ab46d1e47a64a2274c699f648077cb956dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 KB (13939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88f40fc59ce3d885eed54f4550aa108d5a9a860953d6fa19396d6bb55174da9`

```dockerfile
```

-	Layers:
	-	`sha256:5c26b5cde765c90b744538bf4a6ca95d05a2fb38fd9029fe5688ec806b0f1c18`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 13.9 KB (13939 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; arm variant v7

```console
$ docker pull registry@sha256:47ef7710ba9f4fbd700872c21eab27a5dfa893a0e0911715852cdd2868ef21df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9222173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6200c959b354647eaf359eec9856aba78d2f961b1429c5cdcfa94c358192dbf2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-armv7.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:7e2a8985a55f5e4f3b3ae472c5b93ce2792c73bcc72c5b6d704ccb5fb434a07b`  
		Last Modified: Mon, 09 Sep 2024 07:02:44 GMT  
		Size: 2.9 MB (2911454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2862979d3b8c65bc60344e1997591bded8ed142bd7fd405120128eca7f49ca44`  
		Last Modified: Tue, 12 Nov 2024 15:29:49 GMT  
		Size: 292.9 KB (292920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4518dd25cdc89f46b95212b0f8e670f000254dc3db5b67aade21b5b01391faa`  
		Last Modified: Tue, 12 Nov 2024 15:29:50 GMT  
		Size: 6.0 MB (6017216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636f5962f66761865cdcee4ec702fda4f4dbe8fb126939f83ec2992209d0b66f`  
		Last Modified: Tue, 12 Nov 2024 15:29:49 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a61ee3ce5af7f700529f55881a97ca5cebdc8c11c768d681b35e4bd9860c1c`  
		Last Modified: Tue, 12 Nov 2024 15:29:49 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:78b317756a86aa4c6aeb9088c93296bfaa48d4c4cbc06a0ca11c7fd65e62a6a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.2 KB (193197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72878d323f86f97f5c0701a676fd961d4b6c6a25d2f67b24461e2aaa011a824d`

```dockerfile
```

-	Layers:
	-	`sha256:e791e9085d9badcc51e175cf9eb345929d3837ee061f19a89772b55d1009f974`  
		Last Modified: Tue, 12 Nov 2024 15:29:49 GMT  
		Size: 179.0 KB (179043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:898f7fdd08c3b472b4e5cff35cbe6e5139db5eb1bc94259a80e14b98868bac1b`  
		Last Modified: Tue, 12 Nov 2024 15:29:49 GMT  
		Size: 14.2 KB (14154 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:1ef66c49c952ab0d20c905634d50d3a0da70133b0cdb52732a30a0fd89f01a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6adc34955df9f22da1fdc0474dcbab66dfce57ded89499201125f7dc1b9924`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-aarch64.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:0dfcae9cb3f09031e3687535f2d3e3c2f08533799b67ed61076e79e4ed1c7c4a`  
		Last Modified: Mon, 09 Sep 2024 07:02:44 GMT  
		Size: 3.3 MB (3340451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe29ef241d9fe87b99b77f4d96972773b3ae04f1a46c6fea0e0a60800f5f1e1`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 295.8 KB (295832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2787542bdb41f6b8315204be8ea01cb7ff82d9e6de97e9283e8af8dc6ce650e`  
		Last Modified: Tue, 12 Nov 2024 10:28:26 GMT  
		Size: 5.8 MB (5824734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b69fee0ac896543d4936d9c57aea16e665df781ec13ec5257f8bea258da7c79`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb2de197705d02128cc248e6540d752209fe9ed73a32bfb6b19947205030524`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:bbf9ae6a42e4d8aef2759420301cfcc7ed642ba200ae3bf030fd5fdb9d0d2a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.2 KB (193247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8bd06db3380d6a4af9f2d942917235c0df5b1a02aec67120ee470ae2e11a94`

```dockerfile
```

-	Layers:
	-	`sha256:1b1f1a3aa2b9f06c429988bbdfa0c781210c0d81d6befa0769051742b9607830`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 179.1 KB (179063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a601ce5a2c5491c5fd401d93594ecbf76515407f52ce37185f82be3efee56e04`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 14.2 KB (14184 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; ppc64le

```console
$ docker pull registry@sha256:86cdf44fa43a89e6031fc50e516d886c0b257f9f8463548218f7aa0cddca35a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9344901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe03a1f8a043cc0d142b1dbfc0701eb12d5888e6714d95ef5de3ee3f66c3637`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-ppc64le.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:bf19dcb5e2f7e7518032e1f3abc91f7a0f014fc0f3a03de278aca2c9a523ea4f`  
		Last Modified: Tue, 12 Nov 2024 00:56:06 GMT  
		Size: 3.4 MB (3358858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3792e3246e50751fd99db95bd81487f4ff267e527d2bdd744a8f15002029e84b`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 296.2 KB (296245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4725d46af85c7a6abba2419cef1cd0a36956cf13a020d059ba8751a3a0687006`  
		Last Modified: Tue, 12 Nov 2024 08:06:05 GMT  
		Size: 5.7 MB (5689215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a6f196c518d25b0537d6b92276855a0f837b6f99bc09e9cd2854e83070c872`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6030f6d937516639db015c42c56128b1c45f80405aa31d885d4e91fc8cd0ea17`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:63ebe77f6c587302b3a687db1d46b6b9e8b5d89b573cfc083d1f9dad199991b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 KB (191198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0e17de964dc185bfd1b49f65e7621e00c8c3a999513e31042bd22d6f293d26`

```dockerfile
```

-	Layers:
	-	`sha256:191655aad642e846fe9649b077d09cf1d11d1be5742cefe8be2036f8ceafe72f`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 177.1 KB (177087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47532ea0bac7cfc58e078cb792bdb9e1222186b96f8de6519bd95c04af4441b9`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 14.1 KB (14111 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:2.8.3` - linux; s390x

```console
$ docker pull registry@sha256:cad4fdf4a03376ba0904fafcb75e16e3468c10f61e3c64a4cfbb372470c8b891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9684971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d7cccb184b781c20bdbb9ceff63cafb03db8074fdc32bac40da22617b729bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-s390x.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:2cf6287c29b40fb867eb63db5d7189724563e69538ef303e15274f8139042129`  
		Last Modified: Tue, 12 Nov 2024 00:56:53 GMT  
		Size: 3.2 MB (3230439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9149be30168d1b1aa8ec6b23c36dcdc39c2b2dcd978c5e0a2d8ca86109a0df7a`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 293.9 KB (293899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2ded3165ca2acf8ea3ca820d45d88d54ade5de9f1264cc65acbe94b26d0b26`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878ae226c4b32247c8b552259cd2ff67e2c68b8c6dfe9af0b0785d28d04a9618`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277269a6b2649ecc19571438083237ee6b8b605bcb79eb5d2de467a0ab86a175`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:2.8.3` - unknown; unknown

```console
$ docker pull registry@sha256:1c55fb5b8a1b682c0cb9ca173aa7fd36a7a8a0686c87592d298c085ba1bf31c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 KB (191118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8431cec168c6e8aeb1395b10dad52b6f9cdcadef36d4c1b5a36532ee574595ad`

```dockerfile
```

-	Layers:
	-	`sha256:7068d24c38f441b8c1a3dca81bc616b32e4c6eea0489aa2e68837a2b1d02973c`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 177.1 KB (177053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5953f2e3297796f4051786b247167696c4fdc409fca54425806f0ac4df56219`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:3.0.0-rc.2`

```console
$ docker pull registry@sha256:205e4ed3c41eabd25e94f27843fc7fe17cf8123b0846dcc4a85a5d4f0a9b3539
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `registry:3.0.0-rc.2` - linux; arm variant v6

```console
$ docker pull registry@sha256:35a1ea331fb2f3adf740d139190e4496a3e246f80db3d9f08d9f10ae1c5b84fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17176777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e768f852680542601248ce9817088f8973b0da19b64a7bbfcea6c0b268a1dc8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 15:37:50 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
RUN set -eux; 	version='3.0.0-rc.2'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='79d16fec004780982d65f190c97a8e0f1516bf619bfbbc44975db916a21fa08d' ;; 		aarch64) arch='arm64';   sha256='5564b3aed056bcaf08aac7d696c5643bbc43ddbd3b55a7e129bccda94ae02053' ;; 		armhf)   arch='armv6';   sha256='72ac41a85f45f1e2a5df9bf976a1ee4bf36e9bce9628e9d0f1ee9cef9465f5f7' ;; 		armv7)   arch='armv7';   sha256='e652f8174a7079941826409d86d073e40d49e70ab4519540501cfef770cdfe3e' ;; 		ppc64le) arch='ppc64le'; sha256='c02248db69dbdc0dac1d9b44801198101a19defdfd78223050ab68c0d66d0056' ;; 		s390x)   arch='s390x';   sha256='92163ab2b308a0431fd607bc93df699ec64286725ed7f77925971c30ab965054' ;;                 riscv64) arch='riscv64'; sha256='ac471747ae01c218166265bbb73b4416f8fad5d84dda855ee422804dab71a584' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
VOLUME [/var/lib/registry]
# Wed, 18 Dec 2024 15:37:50 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 18 Dec 2024 15:37:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Dec 2024 15:37:50 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee1e955efadc353062808714cadbf3fbf443a9d39e47a0309d6f795eebdd2a9`  
		Last Modified: Fri, 06 Dec 2024 22:28:55 GMT  
		Size: 300.4 KB (300367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2910aa8fb99a8083e488b4e64f5f53831ebfb61ecc7ad665078fc417064672`  
		Last Modified: Thu, 19 Dec 2024 06:28:20 GMT  
		Size: 13.5 MB (13508619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c20e622058b2bc2244298d3b3c170e0ed77041fc5ff4cd50bb5e5cb615890e`  
		Last Modified: Thu, 19 Dec 2024 06:28:19 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4913fea00606a4171313c83c3292264df13ff04985d55057cbd8e560171b73a`  
		Last Modified: Thu, 19 Dec 2024 06:28:19 GMT  
		Size: 213.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.2` - unknown; unknown

```console
$ docker pull registry@sha256:512f6c2462b67920f4bed262d033ea8a0920e491707d1ea4b91403cc7d3a24b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 KB (13339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0de7e92b62b3902807f6d63e3ccb929ecc1593ea2b1a1bac22396dbd3e3c261`

```dockerfile
```

-	Layers:
	-	`sha256:362bbb95353aeeed3316ed017779db3f3d71e76c2d2ed01f790f44557c7d018c`  
		Last Modified: Thu, 19 Dec 2024 06:28:19 GMT  
		Size: 13.3 KB (13339 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.2` - linux; arm variant v7

```console
$ docker pull registry@sha256:5d77e8a33bdb093947ad4395bc22b9faf7327b01254909bf431d1924a33fe131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16898074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c7574bba18f0dc9903f5189b98f881114656d29a639fbc65cb20c831854eaa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 15:37:50 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
RUN set -eux; 	version='3.0.0-rc.2'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='79d16fec004780982d65f190c97a8e0f1516bf619bfbbc44975db916a21fa08d' ;; 		aarch64) arch='arm64';   sha256='5564b3aed056bcaf08aac7d696c5643bbc43ddbd3b55a7e129bccda94ae02053' ;; 		armhf)   arch='armv6';   sha256='72ac41a85f45f1e2a5df9bf976a1ee4bf36e9bce9628e9d0f1ee9cef9465f5f7' ;; 		armv7)   arch='armv7';   sha256='e652f8174a7079941826409d86d073e40d49e70ab4519540501cfef770cdfe3e' ;; 		ppc64le) arch='ppc64le'; sha256='c02248db69dbdc0dac1d9b44801198101a19defdfd78223050ab68c0d66d0056' ;; 		s390x)   arch='s390x';   sha256='92163ab2b308a0431fd607bc93df699ec64286725ed7f77925971c30ab965054' ;;                 riscv64) arch='riscv64'; sha256='ac471747ae01c218166265bbb73b4416f8fad5d84dda855ee422804dab71a584' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
VOLUME [/var/lib/registry]
# Wed, 18 Dec 2024 15:37:50 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 18 Dec 2024 15:37:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Dec 2024 15:37:50 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a49a2dc34dc55420bb1a7a53fe706b82cd56c9d5e3b8d9be9b00e726a3443a`  
		Last Modified: Fri, 06 Dec 2024 22:29:24 GMT  
		Size: 299.4 KB (299389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf3d1b6e7c5eff08b57f093ce895c5c06cfc34e18516a6a69fed425e1449a2a`  
		Last Modified: Thu, 19 Dec 2024 06:28:01 GMT  
		Size: 13.5 MB (13498038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fbe80db628c0517ac90e1dd032aacae113fa4132d74b4afcd160051f89c0e3`  
		Last Modified: Thu, 19 Dec 2024 06:27:59 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2162874ad442d877f30944395e8ff817cbe6c725f7b8ea00becca50235ee163`  
		Last Modified: Thu, 19 Dec 2024 06:28:00 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.2` - unknown; unknown

```console
$ docker pull registry@sha256:edf5d2fdfee9719479ee89eeb6db6466dc86b97274521f7f9f91667677773277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.9 KB (281942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea7ee060e35709d8dc500a81274a6f33db9af1404de7516a3768c68988fde40`

```dockerfile
```

-	Layers:
	-	`sha256:83f14b8cf903b56899c706e69d6e2c246693078a18815736f4784e6ea8aeb48d`  
		Last Modified: Thu, 19 Dec 2024 06:28:00 GMT  
		Size: 268.4 KB (268389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d5c73ddf305fe520f99fe3805ce14320d00c3da8f6cd48451b4ffbd0b273604`  
		Last Modified: Thu, 19 Dec 2024 06:28:00 GMT  
		Size: 13.6 KB (13553 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.2` - linux; ppc64le

```console
$ docker pull registry@sha256:3c6d15f89b2923000e9aa10b56ac7218ed2b2035b681034e6914c38f4ed7fce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16839452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc0692fc2fef5feefeb67d78977d187fa21976a8968f786efccf93fb819a3159`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 15:37:50 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
RUN set -eux; 	version='3.0.0-rc.2'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='79d16fec004780982d65f190c97a8e0f1516bf619bfbbc44975db916a21fa08d' ;; 		aarch64) arch='arm64';   sha256='5564b3aed056bcaf08aac7d696c5643bbc43ddbd3b55a7e129bccda94ae02053' ;; 		armhf)   arch='armv6';   sha256='72ac41a85f45f1e2a5df9bf976a1ee4bf36e9bce9628e9d0f1ee9cef9465f5f7' ;; 		armv7)   arch='armv7';   sha256='e652f8174a7079941826409d86d073e40d49e70ab4519540501cfef770cdfe3e' ;; 		ppc64le) arch='ppc64le'; sha256='c02248db69dbdc0dac1d9b44801198101a19defdfd78223050ab68c0d66d0056' ;; 		s390x)   arch='s390x';   sha256='92163ab2b308a0431fd607bc93df699ec64286725ed7f77925971c30ab965054' ;;                 riscv64) arch='riscv64'; sha256='ac471747ae01c218166265bbb73b4416f8fad5d84dda855ee422804dab71a584' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
VOLUME [/var/lib/registry]
# Wed, 18 Dec 2024 15:37:50 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 18 Dec 2024 15:37:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Dec 2024 15:37:50 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86434423e35b71b2614f2aba7be1ceb3dc68f2ffacf6c01b905ef3942901cfa6`  
		Last Modified: Thu, 19 Dec 2024 06:27:42 GMT  
		Size: 302.1 KB (302149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6d904e59479db9461f1e3530c677637dce352bab49a59a17a8228363d617b7`  
		Last Modified: Thu, 19 Dec 2024 06:27:42 GMT  
		Size: 13.0 MB (12959584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d209477860307fbd47d874c40c68126fcedb7856e234c21a3c6e48c9b4c9884c`  
		Last Modified: Thu, 19 Dec 2024 06:27:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce68bd4ab4502457c7f5300dfadeb1f8e539388cad706054c80a60a0bcb5830c`  
		Last Modified: Thu, 19 Dec 2024 06:27:42 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.2` - unknown; unknown

```console
$ docker pull registry@sha256:470a29837ce3c1ad3e487060d49961d0c22caecc5dfdfe1f0991baae8a1e2bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.0 KB (279959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad1019139a13e6cdd405a804b1fa5e242f43b683fba50882bcb3a674df1d9e5`

```dockerfile
```

-	Layers:
	-	`sha256:23e29caac9be0b1f48855c339c2c42e3a3147fe7d661fc2a6b41b8a43c9d5c59`  
		Last Modified: Thu, 19 Dec 2024 06:27:42 GMT  
		Size: 266.4 KB (266442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc7b8676bacc7370852234111787d2fafacc3018b7ad72e7f2566620eff2f7c5`  
		Last Modified: Thu, 19 Dec 2024 06:27:42 GMT  
		Size: 13.5 KB (13517 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.2` - linux; riscv64

```console
$ docker pull registry@sha256:14539ed2e75a71290875ecaafe5265c96e9fea788339fefbcb640b1dff1b0277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17320358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fafb47fe39616521b03ac91bdf375de8b7a2dd179c50dd5053c21e89a2a84d7f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 15:37:50 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
RUN set -eux; 	version='3.0.0-rc.2'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='79d16fec004780982d65f190c97a8e0f1516bf619bfbbc44975db916a21fa08d' ;; 		aarch64) arch='arm64';   sha256='5564b3aed056bcaf08aac7d696c5643bbc43ddbd3b55a7e129bccda94ae02053' ;; 		armhf)   arch='armv6';   sha256='72ac41a85f45f1e2a5df9bf976a1ee4bf36e9bce9628e9d0f1ee9cef9465f5f7' ;; 		armv7)   arch='armv7';   sha256='e652f8174a7079941826409d86d073e40d49e70ab4519540501cfef770cdfe3e' ;; 		ppc64le) arch='ppc64le'; sha256='c02248db69dbdc0dac1d9b44801198101a19defdfd78223050ab68c0d66d0056' ;; 		s390x)   arch='s390x';   sha256='92163ab2b308a0431fd607bc93df699ec64286725ed7f77925971c30ab965054' ;;                 riscv64) arch='riscv64'; sha256='ac471747ae01c218166265bbb73b4416f8fad5d84dda855ee422804dab71a584' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
VOLUME [/var/lib/registry]
# Wed, 18 Dec 2024 15:37:50 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 18 Dec 2024 15:37:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Dec 2024 15:37:50 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352d2aed11821bec39048fd95800ed8324f4ffbc936cc77681114832e36fdb97`  
		Last Modified: Fri, 06 Dec 2024 22:31:00 GMT  
		Size: 299.6 KB (299638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf63c2df3c6854583b64ea49993152004ff39f0c230370eca815fca6495d5649`  
		Last Modified: Thu, 19 Dec 2024 06:29:24 GMT  
		Size: 13.7 MB (13666087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd33c4db783cfc3577a8b0eb797331b8d9095e4880631797be76c2d8eff637b`  
		Last Modified: Thu, 19 Dec 2024 06:29:22 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3e3d9547781d9a3da6db638e7bc904ff603a35389168b11ffa27124122d339`  
		Last Modified: Thu, 19 Dec 2024 06:29:22 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.2` - unknown; unknown

```console
$ docker pull registry@sha256:1c689ac0499ff5455e2af642ad38c01efd7dc3ec5226e057d53a64775edc7ebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.0 KB (279955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe1c8660293640fc31cb59b91e26f79b0df0169438ccb905677efe30d8d9e50`

```dockerfile
```

-	Layers:
	-	`sha256:3c081ebdc1d1f64f2f33e219adfb72f319dc66e2fc10f4d9bad22b3ac570533e`  
		Last Modified: Thu, 19 Dec 2024 06:29:22 GMT  
		Size: 266.4 KB (266438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcc81fc93710c2acf4735c4c1f5e5f1a9f5b407023267abed377546ab9155df6`  
		Last Modified: Thu, 19 Dec 2024 06:29:22 GMT  
		Size: 13.5 KB (13517 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:3.0.0-rc.2` - linux; s390x

```console
$ docker pull registry@sha256:7ae77b91df20b486f3ca052486d127073e310f98a521d8789d3b94bd00746d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17615138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6e3b86c235a5b614b0d08f55bc4c408dd5563f43bed09369ed3e78d781fae9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/distribution\/config.yml"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Wed, 18 Dec 2024 15:37:50 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
RUN set -eux; 	version='3.0.0-rc.2'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='79d16fec004780982d65f190c97a8e0f1516bf619bfbbc44975db916a21fa08d' ;; 		aarch64) arch='arm64';   sha256='5564b3aed056bcaf08aac7d696c5643bbc43ddbd3b55a7e129bccda94ae02053' ;; 		armhf)   arch='armv6';   sha256='72ac41a85f45f1e2a5df9bf976a1ee4bf36e9bce9628e9d0f1ee9cef9465f5f7' ;; 		armv7)   arch='armv7';   sha256='e652f8174a7079941826409d86d073e40d49e70ab4519540501cfef770cdfe3e' ;; 		ppc64le) arch='ppc64le'; sha256='c02248db69dbdc0dac1d9b44801198101a19defdfd78223050ab68c0d66d0056' ;; 		s390x)   arch='s390x';   sha256='92163ab2b308a0431fd607bc93df699ec64286725ed7f77925971c30ab965054' ;;                 riscv64) arch='riscv64'; sha256='ac471747ae01c218166265bbb73b4416f8fad5d84dda855ee422804dab71a584' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
COPY ./config-example.yml /etc/distribution/config.yml # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
VOLUME [/var/lib/registry]
# Wed, 18 Dec 2024 15:37:50 GMT
EXPOSE map[5000/tcp:{}]
# Wed, 18 Dec 2024 15:37:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 18 Dec 2024 15:37:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 18 Dec 2024 15:37:50 GMT
CMD ["/etc/distribution/config.yml"]
```

-	Layers:
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f82495024d9a8579f15a17159de8fe1011aa2dc02d718c9ddede18ae591e4a8a`  
		Last Modified: Thu, 19 Dec 2024 06:28:38 GMT  
		Size: 300.4 KB (300390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9695dacfba9c5aebbe41878ddd1e83a5aff97ca1f7edbd634bb17eb90f26c4`  
		Last Modified: Thu, 19 Dec 2024 06:28:39 GMT  
		Size: 13.8 MB (13844617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5fe3c3bc36f27b514a9c27430d2a137c4163e9267ed72f9a240f128bf81bbc`  
		Last Modified: Thu, 19 Dec 2024 06:28:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9de77d6e77389c8d89456749cbb0f3b74478ed22f71c4f1969925d8ff14221a`  
		Last Modified: Thu, 19 Dec 2024 06:28:39 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:3.0.0-rc.2` - unknown; unknown

```console
$ docker pull registry@sha256:1a041b7713caa35b4c53e3e81d812b120a2f0913409d5e09e101681454def0d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.9 KB (279904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad162d25247e96868cae61476c38396bc278a30b0fc986d3010ff2738fd0f03c`

```dockerfile
```

-	Layers:
	-	`sha256:29bb371deb30ab893c2cc08e1b4471676ef9b65127e7787f700d13ded1b8b760`  
		Last Modified: Thu, 19 Dec 2024 06:28:39 GMT  
		Size: 266.4 KB (266416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:983980c9b45a085848b82f115693301270502bd0d8a3f702b3116e5df119dadb`  
		Last Modified: Thu, 19 Dec 2024 06:28:38 GMT  
		Size: 13.5 KB (13488 bytes)  
		MIME: application/vnd.in-toto+json

## `registry:latest`

```console
$ docker pull registry@sha256:543dade69668e02e5768d7ea2b0aa4fae6aa7384c9a5a8dbecc2be5136079ddb
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

### `registry:latest` - linux; amd64

```console
$ docker pull registry@sha256:d252b0c9a9409bb1e10a98a6b79d8f2a082284a113bc33f49121bb2fb0797cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10114147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18a86d35e983225b84aae3bb15c84bd9e47506dd0102975c0ed97958703bb73`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-x86_64.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:dc0decf4841d19b14e836c2d82bd5cb9540fb5e0d1359549ca243f49036557e9`  
		Last Modified: Mon, 09 Sep 2024 07:02:43 GMT  
		Size: 3.4 MB (3416401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb0aa443e23aedd28f0818f7a18de9911383d0b9b621bc448070ded1d6c81c3`  
		Last Modified: Tue, 12 Nov 2024 02:37:06 GMT  
		Size: 293.4 KB (293379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813676e291ef88d6de121b9a67d4b546585c87f2b89df39d4fd14ba984cd655f`  
		Last Modified: Tue, 12 Nov 2024 02:37:06 GMT  
		Size: 6.4 MB (6403784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2fb7dcec6119c150b59df0550dc646f6a45351470a7b74f0a904df40418a12`  
		Last Modified: Tue, 12 Nov 2024 02:37:05 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916205650bfe545ec2ac378e84f53759e0c977a77e583f0525e05cf3c8923df5`  
		Last Modified: Tue, 12 Nov 2024 02:37:06 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:ef807d6ab3ae145cb40e6bc86fbd8de0fb6f4c6726ac88e619634da80dd35994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.1 KB (193072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e7ad24d9321d0ba3df236bcc6d5bf0a26dc6b4069c58745f6d491db169526b`

```dockerfile
```

-	Layers:
	-	`sha256:547ee2ce16efcc56c2f70e31f7327b246f129ae9e0e0f5393b19da960f910466`  
		Last Modified: Tue, 12 Nov 2024 02:37:06 GMT  
		Size: 179.0 KB (179007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8e019b81fd4a44bcc35582450d9aeddbdb46be2e2b6e0e5bd6cbe0dcc431d8b`  
		Last Modified: Tue, 12 Nov 2024 02:37:05 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm variant v6

```console
$ docker pull registry@sha256:8351e958c42f9de2b77889506fae68712813fb6bc5f4e1579cf103bec35d41b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9477718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646ed268fea06904233caf5921a317743a80856db79e456db3956b70cc1a7b1b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-armhf.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:1ce61877166753d951080511a4649a7a9674d00fdd71569057a7f3099f39e6d8`  
		Last Modified: Mon, 09 Sep 2024 07:02:44 GMT  
		Size: 3.2 MB (3158999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b739e776fe9e57644b5e4e99c00c4dbb4a039c894137288a095e5adcc3f78d8`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 294.0 KB (294026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5afee98ad80b18cdcc1e4f610c4b5f499b6c55c68ea75a4743e1e680fa910f4`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 6.0 MB (6024109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7f5e00a1807cf3e9f780608fcb4b45baf5e9735de16505b91749f287e31298`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3adbb8c5936d65b71c7da2c2cabe8705bd496d982f440619bbe8c594d5c3f02d`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:2d1adb226ba38d47f5571423f8a72ab46d1e47a64a2274c699f648077cb956dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 KB (13939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b88f40fc59ce3d885eed54f4550aa108d5a9a860953d6fa19396d6bb55174da9`

```dockerfile
```

-	Layers:
	-	`sha256:5c26b5cde765c90b744538bf4a6ca95d05a2fb38fd9029fe5688ec806b0f1c18`  
		Last Modified: Tue, 12 Nov 2024 06:28:42 GMT  
		Size: 13.9 KB (13939 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm variant v7

```console
$ docker pull registry@sha256:47ef7710ba9f4fbd700872c21eab27a5dfa893a0e0911715852cdd2868ef21df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9222173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6200c959b354647eaf359eec9856aba78d2f961b1429c5cdcfa94c358192dbf2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-armv7.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:7e2a8985a55f5e4f3b3ae472c5b93ce2792c73bcc72c5b6d704ccb5fb434a07b`  
		Last Modified: Mon, 09 Sep 2024 07:02:44 GMT  
		Size: 2.9 MB (2911454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2862979d3b8c65bc60344e1997591bded8ed142bd7fd405120128eca7f49ca44`  
		Last Modified: Tue, 12 Nov 2024 15:29:49 GMT  
		Size: 292.9 KB (292920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4518dd25cdc89f46b95212b0f8e670f000254dc3db5b67aade21b5b01391faa`  
		Last Modified: Tue, 12 Nov 2024 15:29:50 GMT  
		Size: 6.0 MB (6017216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636f5962f66761865cdcee4ec702fda4f4dbe8fb126939f83ec2992209d0b66f`  
		Last Modified: Tue, 12 Nov 2024 15:29:49 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a61ee3ce5af7f700529f55881a97ca5cebdc8c11c768d681b35e4bd9860c1c`  
		Last Modified: Tue, 12 Nov 2024 15:29:49 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:78b317756a86aa4c6aeb9088c93296bfaa48d4c4cbc06a0ca11c7fd65e62a6a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.2 KB (193197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72878d323f86f97f5c0701a676fd961d4b6c6a25d2f67b24461e2aaa011a824d`

```dockerfile
```

-	Layers:
	-	`sha256:e791e9085d9badcc51e175cf9eb345929d3837ee061f19a89772b55d1009f974`  
		Last Modified: Tue, 12 Nov 2024 15:29:49 GMT  
		Size: 179.0 KB (179043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:898f7fdd08c3b472b4e5cff35cbe6e5139db5eb1bc94259a80e14b98868bac1b`  
		Last Modified: Tue, 12 Nov 2024 15:29:49 GMT  
		Size: 14.2 KB (14154 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; arm64 variant v8

```console
$ docker pull registry@sha256:1ef66c49c952ab0d20c905634d50d3a0da70133b0cdb52732a30a0fd89f01a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9461601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6adc34955df9f22da1fdc0474dcbab66dfce57ded89499201125f7dc1b9924`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-aarch64.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:0dfcae9cb3f09031e3687535f2d3e3c2f08533799b67ed61076e79e4ed1c7c4a`  
		Last Modified: Mon, 09 Sep 2024 07:02:44 GMT  
		Size: 3.3 MB (3340451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe29ef241d9fe87b99b77f4d96972773b3ae04f1a46c6fea0e0a60800f5f1e1`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 295.8 KB (295832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2787542bdb41f6b8315204be8ea01cb7ff82d9e6de97e9283e8af8dc6ce650e`  
		Last Modified: Tue, 12 Nov 2024 10:28:26 GMT  
		Size: 5.8 MB (5824734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b69fee0ac896543d4936d9c57aea16e665df781ec13ec5257f8bea258da7c79`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb2de197705d02128cc248e6540d752209fe9ed73a32bfb6b19947205030524`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:bbf9ae6a42e4d8aef2759420301cfcc7ed642ba200ae3bf030fd5fdb9d0d2a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.2 KB (193247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8bd06db3380d6a4af9f2d942917235c0df5b1a02aec67120ee470ae2e11a94`

```dockerfile
```

-	Layers:
	-	`sha256:1b1f1a3aa2b9f06c429988bbdfa0c781210c0d81d6befa0769051742b9607830`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 179.1 KB (179063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a601ce5a2c5491c5fd401d93594ecbf76515407f52ce37185f82be3efee56e04`  
		Last Modified: Tue, 12 Nov 2024 10:28:25 GMT  
		Size: 14.2 KB (14184 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; ppc64le

```console
$ docker pull registry@sha256:86cdf44fa43a89e6031fc50e516d886c0b257f9f8463548218f7aa0cddca35a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9344901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe03a1f8a043cc0d142b1dbfc0701eb12d5888e6714d95ef5de3ee3f66c3637`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-ppc64le.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:bf19dcb5e2f7e7518032e1f3abc91f7a0f014fc0f3a03de278aca2c9a523ea4f`  
		Last Modified: Tue, 12 Nov 2024 00:56:06 GMT  
		Size: 3.4 MB (3358858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3792e3246e50751fd99db95bd81487f4ff267e527d2bdd744a8f15002029e84b`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 296.2 KB (296245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4725d46af85c7a6abba2419cef1cd0a36956cf13a020d059ba8751a3a0687006`  
		Last Modified: Tue, 12 Nov 2024 08:06:05 GMT  
		Size: 5.7 MB (5689215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a6f196c518d25b0537d6b92276855a0f837b6f99bc09e9cd2854e83070c872`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 369.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6030f6d937516639db015c42c56128b1c45f80405aa31d885d4e91fc8cd0ea17`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:63ebe77f6c587302b3a687db1d46b6b9e8b5d89b573cfc083d1f9dad199991b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 KB (191198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0e17de964dc185bfd1b49f65e7621e00c8c3a999513e31042bd22d6f293d26`

```dockerfile
```

-	Layers:
	-	`sha256:191655aad642e846fe9649b077d09cf1d11d1be5742cefe8be2036f8ceafe72f`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 177.1 KB (177087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47532ea0bac7cfc58e078cb792bdb9e1222186b96f8de6519bd95c04af4441b9`  
		Last Modified: Tue, 12 Nov 2024 08:06:04 GMT  
		Size: 14.1 KB (14111 bytes)  
		MIME: application/vnd.in-toto+json

### `registry:latest` - linux; s390x

```console
$ docker pull registry@sha256:cad4fdf4a03376ba0904fafcb75e16e3468c10f61e3c64a4cfbb372470c8b891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9684971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d7cccb184b781c20bdbb9ceff63cafb03db8074fdc32bac40da22617b729bb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["\/etc\/docker\/registry\/config.yml"]`

```dockerfile
# Mon, 02 Oct 2023 18:42:41 GMT
ADD alpine-minirootfs-3.18.9-s390x.tar.gz / # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/bin/sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
RUN set -eux; 	version='2.8.3'; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64)  arch='amd64';   sha256='b1f750ecbe09f38e2143e22c61a25e3da2afe1510d9522859230b480e642ceff' ;; 		aarch64) arch='arm64';   sha256='7d2252eeeac97dd60fb9b36bebd15b95d7f947c4c82b8e0824cb55233ece9cd0' ;; 		armhf)   arch='armv6';   sha256='b00606466f976b6757268f1e7691918cbeca4af6fd4093a114b9186744ee8ef0' ;; 		armv7)   arch='armv7';   sha256='d3d7d958a7cc04159d43871261b1ed470ba72531d345fada311068962b967517' ;; 		ppc64le) arch='ppc64le'; sha256='9003659e5571bee89ee6d686057d02e9c0896d327276f268189922036e1ca84b' ;; 		s390x)   arch='s390x';   sha256='2c1347c73f881c320ff707055aecf649a888df39252e8bdc4fdfac7f59a383f1' ;; 		*) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;; 	esac; 	wget -O registry.tar.gz "https://github.com/distribution/distribution/releases/download/v${version}/registry_${version}_linux_${arch}.tar.gz"; 	echo "$sha256 *registry.tar.gz" | sha256sum -c -; 	tar --extract --verbose --file registry.tar.gz --directory /bin/ registry; 	rm registry.tar.gz; 	registry --version # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
COPY ./config-example.yml /etc/docker/registry/config.yml # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
VOLUME [/var/lib/registry]
# Mon, 02 Oct 2023 18:42:41 GMT
EXPOSE map[5000/tcp:{}]
# Mon, 02 Oct 2023 18:42:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 02 Oct 2023 18:42:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 02 Oct 2023 18:42:41 GMT
CMD ["/etc/docker/registry/config.yml"]
```

-	Layers:
	-	`sha256:2cf6287c29b40fb867eb63db5d7189724563e69538ef303e15274f8139042129`  
		Last Modified: Tue, 12 Nov 2024 00:56:53 GMT  
		Size: 3.2 MB (3230439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9149be30168d1b1aa8ec6b23c36dcdc39c2b2dcd978c5e0a2d8ca86109a0df7a`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 293.9 KB (293899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2ded3165ca2acf8ea3ca820d45d88d54ade5de9f1264cc65acbe94b26d0b26`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 6.2 MB (6160049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878ae226c4b32247c8b552259cd2ff67e2c68b8c6dfe9af0b0785d28d04a9618`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 370.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277269a6b2649ecc19571438083237ee6b8b605bcb79eb5d2de467a0ab86a175`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `registry:latest` - unknown; unknown

```console
$ docker pull registry@sha256:1c55fb5b8a1b682c0cb9ca173aa7fd36a7a8a0686c87592d298c085ba1bf31c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 KB (191118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8431cec168c6e8aeb1395b10dad52b6f9cdcadef36d4c1b5a36532ee574595ad`

```dockerfile
```

-	Layers:
	-	`sha256:7068d24c38f441b8c1a3dca81bc616b32e4c6eea0489aa2e68837a2b1d02973c`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 177.1 KB (177053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5953f2e3297796f4051786b247167696c4fdc409fca54425806f0ac4df56219`  
		Last Modified: Tue, 12 Nov 2024 08:41:21 GMT  
		Size: 14.1 KB (14065 bytes)  
		MIME: application/vnd.in-toto+json
