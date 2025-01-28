## `amazoncorretto:8-alpine3.21-jre`

```console
$ docker pull amazoncorretto@sha256:50016ea4a57f924c7dda09015644bc5ae4fcc55582c7dd97b3b8b70c6426759b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.21-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:778688b47155c80dc698ffeabfd21876aacaf31ef23263c35a5a7d4210b3f0d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45296184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:393216eb263d722f529f9a6060aab76a2bc5b1a2ffe2fecae7e272d03cafd7fc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=8.442.06.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=8.442.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a618fa98535ac8c83d7b3919d8c4529f8fe5c9203da3af8a3e3dacd84f1aee`  
		Last Modified: Fri, 24 Jan 2025 23:26:06 GMT  
		Size: 41.7 MB (41654469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.21-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:07dffa9a4a20c314c88435315b96cd55996172416affeae8fc62759e835f235a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 KB (196839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4aea6378ad5714ecf1832e3f3feb95d963a2aa80df5eca869c8f4012b9cd499`

```dockerfile
```

-	Layers:
	-	`sha256:b5a455a1c9e4cf3d042c2b574df9ef4d7f67b356901f143353f7bc43184589eb`  
		Last Modified: Fri, 24 Jan 2025 23:26:06 GMT  
		Size: 187.5 KB (187481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8147c69505f57b3294a032dc1f48fccfeb3ef80f5f25afde54c8f4cf7b2679d9`  
		Last Modified: Fri, 24 Jan 2025 23:26:06 GMT  
		Size: 9.4 KB (9358 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.21-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5834a95cddfd7bfd807c4f3235b1010bedaac2f8a97f9fce7c451ba188e9995a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45354847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c7178373f705f13980fd9eba4bbf72d11419574d628c565bc2b159be038d7ba`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=8.442.06.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=8.442.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2859d01c70183d0b7ec19fcb2444ca00cf6ef55f2a82a29024c57c45b59ac2`  
		Last Modified: Fri, 24 Jan 2025 23:27:00 GMT  
		Size: 41.4 MB (41362488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.21-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4c4ee09a7f484ca40f4bea6d6957c63ef810f67d136333b171085d4b14e35289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.1 KB (197076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3814631252f691ad5a142c9185427c8b7616205e63c20eef3b6f4cc9f6f135b`

```dockerfile
```

-	Layers:
	-	`sha256:6aa750f9d30812489051df193b1cd3f4c6c5b7caa091f46e13480d35788c3cb7`  
		Last Modified: Fri, 24 Jan 2025 23:26:59 GMT  
		Size: 187.6 KB (187613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b36a989ebb85f28937d081e47853af1f94bcb4b96ad7d6e359534817d45cd53b`  
		Last Modified: Fri, 24 Jan 2025 23:26:59 GMT  
		Size: 9.5 KB (9463 bytes)  
		MIME: application/vnd.in-toto+json
