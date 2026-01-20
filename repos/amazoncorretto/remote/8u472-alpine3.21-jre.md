## `amazoncorretto:8u472-alpine3.21-jre`

```console
$ docker pull amazoncorretto@sha256:7fe3ea9ea0740596d5e1994e3d06a25955744e5afeb5653ee8faa0b3933a093a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u472-alpine3.21-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c0775d06caf1d21cff3d7571b66ffbaba046c8901cdd0c9cf8d0ffafe4b8daee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45377890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1402c645e52637d3ae5c530049e513f182465b78b980e3657550fcea3a2b5d3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=8.472.08.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=8.472.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Sun, 07 Dec 2025 13:55:07 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7bc8dc684614dd7cc8db5e39c446c4d019551b34991370988f4708972bd67a`  
		Last Modified: Mon, 22 Dec 2025 01:07:09 GMT  
		Size: 41.7 MB (41735321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u472-alpine3.21-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fe6aa39b9803ee45f0b553c486751f8873e095c6b000ce0b0d12988f12a3edd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.4 KB (197419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c9843bf8a7e398551e258a097fb8f275ed146342f4a58f7433de5165267535`

```dockerfile
```

-	Layers:
	-	`sha256:8909ce96110838c7aed8e7e31f676062da6fc07411a248ad27e5ca869c0c32fa`  
		Last Modified: Sat, 27 Dec 2025 19:10:16 GMT  
		Size: 188.7 KB (188721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81124ba4c4a056089fc93f48e4da2333d5ad0891d87985ba2d5752e00f887a4e`  
		Last Modified: Sat, 27 Dec 2025 19:10:15 GMT  
		Size: 8.7 KB (8698 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u472-alpine3.21-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d07f004e9996675b2784d61595335ca0aff89fb5a1f0437ce6b6c6d2507dbd7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45425130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e239060070552d10a74906e8cdcf9a68482e743723585ec12349c3e9f6193e48`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=8.472.08.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=8.472.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 12:04:23 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7001f3119f9947776fded5f7cffb44cf40e2536f964e26cc215d5c44a16c2634`  
		Last Modified: Fri, 26 Dec 2025 15:00:25 GMT  
		Size: 41.4 MB (41432777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u472-alpine3.21-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c90b54b016b391579e9c1722465f399f0224f16e0dddb6a283350b3537806234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.6 KB (197608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be75cc70e64f3765819e469a28f8cc868703de7a1f6ee9eec67c41b1e4356f8`

```dockerfile
```

-	Layers:
	-	`sha256:8587207873335361dc3e3f1fa4bcbf08df4692a77ce4c4174e4423d74cabcc8a`  
		Last Modified: Mon, 19 Jan 2026 11:43:00 GMT  
		Size: 188.8 KB (188829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b78c3385898a7bda1e8e0bbaafa1130408f99d37973f55a955697fda32928532`  
		Last Modified: Mon, 19 Jan 2026 11:43:00 GMT  
		Size: 8.8 KB (8779 bytes)  
		MIME: application/vnd.in-toto+json
