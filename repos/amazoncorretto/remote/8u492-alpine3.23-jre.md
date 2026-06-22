## `amazoncorretto:8u492-alpine3.23-jre`

```console
$ docker pull amazoncorretto@sha256:060ec978114fffb0987e41f299db98d5a4b37a3e04fb849e0d3a8bb80dcbc888
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u492-alpine3.23-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3b6229845e5058c0b9414f4341afb69fc6951199206c88f9fab9a52aa40272cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45594508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e94e1190afe39307554446f3f93aede0e693068950c405a6412e35847401858d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:53:42 GMT
ARG version=8.492.09.2
# Mon, 22 Jun 2026 19:53:42 GMT
# ARGS: version=8.492.09.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Mon, 22 Jun 2026 19:53:42 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:53:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5b9c62cac7466089c4fc325165048779c8a1273bb8d00db19b728417f0fcfe`  
		Last Modified: Mon, 22 Jun 2026 19:53:53 GMT  
		Size: 41.8 MB (41750087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-alpine3.23-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:47575b19062f85c605c2347708c1610df1486fe199a8c3776360488e4f371460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.9 KB (195867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b5ae89a9e96fe4a08785f8c12cb45114b329c761022609d39194e5805c527bc`

```dockerfile
```

-	Layers:
	-	`sha256:630d07e18036afb41ac594b1bd4f5bc3df4262e638244d105a57719313f37c0c`  
		Last Modified: Mon, 22 Jun 2026 19:53:51 GMT  
		Size: 187.2 KB (187211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fe763eb17b37999402b916a1c596d78e3305c1b06b3d47749bc8e435fefb451`  
		Last Modified: Mon, 22 Jun 2026 19:53:51 GMT  
		Size: 8.7 KB (8656 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u492-alpine3.23-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:18ba25b4aac303431d1366513f2df9305229d76aaf0c6e48ee9548d30affba4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45649681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66f849cf553464ff4f243d358a5b23fdbb58b78894d9054506491ea51e8b8f39`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:55:12 GMT
ARG version=8.492.09.2
# Mon, 22 Jun 2026 19:55:12 GMT
# ARGS: version=8.492.09.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Mon, 22 Jun 2026 19:55:12 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:55:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c2a825157cfa6a921174e996035d0c2e81e5789f858eeead03952136e8b6b8`  
		Last Modified: Mon, 22 Jun 2026 19:55:23 GMT  
		Size: 41.5 MB (41467821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-alpine3.23-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8d841e5da390b848278ebb0d1d0b6eacbc84c20f0f7b153df1fd08c0836f853f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.4 KB (195405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3751e303ca0e812f67b063d801195780a715f9e99d3fc36a140d3e1f8c94898b`

```dockerfile
```

-	Layers:
	-	`sha256:95eb2fc59ac2a2c9e155adbc457994fc5e96710d695d590e3424a63a9deeb748`  
		Last Modified: Mon, 22 Jun 2026 19:55:22 GMT  
		Size: 186.7 KB (186669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d9fd07ba75ed15bff51bfefd0c11c6f7ef18a55b1bfee1486256a04af92ebce`  
		Last Modified: Mon, 22 Jun 2026 19:55:21 GMT  
		Size: 8.7 KB (8736 bytes)  
		MIME: application/vnd.in-toto+json
