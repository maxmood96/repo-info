## `amazoncorretto:8-alpine3.21-jdk`

```console
$ docker pull amazoncorretto@sha256:00cc846a2a9321bdb8d2e972201497d4822b633e65217b3b3cb8b2b85ad476dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.21-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9151cd8c7d18cd4da025e9a05718079406eadbd372f21d854a120657d9652a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103937966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ab8ea1f19a02a31046675bd47c3a7e6830101e56b04a71f201bb8aa8401b72`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=8.462.08.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=8.462.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0dfa3a0519cce63e10c2753727bb4c762b5e256adae6aca032b0f31b8ad9c6c`  
		Last Modified: Wed, 08 Oct 2025 22:59:14 GMT  
		Size: 100.3 MB (100295397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.21-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:124c9e4c42f1e6c5bb1caa5a22b6cf8cab4758281577f4530dfd2c5d10c2329d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.3 KB (258296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3834433f0beacac1f5d0ea5ad3b219a8aa50c7e419d5575c9e695150b3753d1`

```dockerfile
```

-	Layers:
	-	`sha256:82a2d118acc4a20873067e4b0130f7d179e20036abff9d031bc41eff80e442b7`  
		Last Modified: Thu, 09 Oct 2025 00:53:45 GMT  
		Size: 248.9 KB (248898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f16359ee938f6be3d7def2c321a9f9eb2d18ca1305c2f2ec6fa2cb711305ede1`  
		Last Modified: Thu, 09 Oct 2025 00:53:46 GMT  
		Size: 9.4 KB (9398 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.21-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:14a5a109daa92375b41f07b112524215100c6e742166a4e5d778f15e8ecf5557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104084520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:205be563bdacccaa9ef4d374348cadf3750fa04b46d76852da96d8d23615c8fa`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=8.462.08.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=8.462.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdad99876f74d94985b2ddaaed57692a3fdf767d1474d075407c6db9d0ee55f2`  
		Last Modified: Wed, 08 Oct 2025 21:46:37 GMT  
		Size: 100.1 MB (100092167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.21-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8ec97b79ff6dc02fb46f778cce20f7965f30df6c1eb5a391621b028c1b713ec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.5 KB (258532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a94b0d3a1c5964f8c1c76c27f2fd03381563d5b30d7bbf4799331e05d55b9eb5`

```dockerfile
```

-	Layers:
	-	`sha256:df7b21a4c579e0e34baf20bac5202818563a16b25da582e5f1929478fc4c216a`  
		Last Modified: Thu, 09 Oct 2025 00:53:49 GMT  
		Size: 249.0 KB (249030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cd30865dcc48f790b90529a62a8b3feeb2e651a6398fe336ced5a65eae205ae`  
		Last Modified: Thu, 09 Oct 2025 00:53:50 GMT  
		Size: 9.5 KB (9502 bytes)  
		MIME: application/vnd.in-toto+json
