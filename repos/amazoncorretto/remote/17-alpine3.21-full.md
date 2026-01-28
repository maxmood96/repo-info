## `amazoncorretto:17-alpine3.21-full`

```console
$ docker pull amazoncorretto@sha256:a68e21560dd22677e5ca89ed54c49a161a25b33630548b9826e57768effde989
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.21-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3c473c017a25fb17a0f7f16cb63cd57bc279b54d33d21b68df6422400fbfe146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (152009859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:412cee78f3e56bd2be5ffea3c9ec76f4a6e623b225823e07be439c26bbc41160`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:47:28 GMT
ARG version=17.0.18.8.1
# Wed, 28 Jan 2026 02:47:28 GMT
# ARGS: version=17.0.18.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:47:28 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:47:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:47:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4757f79741d37fca729d4fa63bf16ba64fba0d2b9cbc5c7cf039815ac1e954da`  
		Last Modified: Wed, 28 Jan 2026 02:47:45 GMT  
		Size: 148.4 MB (148366117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.21-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7358771e3e9ece7ddc878fdcec4818232cd7ccd03c369c182f602e406ed1da66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.9 KB (595932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37ed0790d9f2a1f36735ef3f4df9ca9fe212d2fb0652dd96fc7076525e953078`

```dockerfile
```

-	Layers:
	-	`sha256:4ea459dbf3b5a8c87a76712dc1017d3a6e4ad2f0c2d33a2907048174db233773`  
		Last Modified: Wed, 28 Jan 2026 02:47:42 GMT  
		Size: 586.6 KB (586559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85f296357277d70686269641776f333969a27a9b5ef2292c81e4d8f5c5fc4837`  
		Last Modified: Wed, 28 Jan 2026 02:47:42 GMT  
		Size: 9.4 KB (9373 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.21-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e7e958f436b125b93f7438df042788274687acad560b5d17bbdfc635dc9406a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.7 MB (150695411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd8b21c794ff354ba510e24490b7cf0a6ae39159e22982e262560e2847bbac9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:07 GMT
ADD alpine-minirootfs-3.21.6-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:07 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:47:59 GMT
ARG version=17.0.18.8.1
# Wed, 28 Jan 2026 02:47:59 GMT
# ARGS: version=17.0.18.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:47:59 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:47:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:47:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:a447a5de8f4eb4a987d81c0afa14d459cc714599c020c08f45fafa9c6c904b30`  
		Last Modified: Wed, 28 Jan 2026 01:18:13 GMT  
		Size: 4.0 MB (3992880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518fc4469a8744437cd8e95030f056f3028d293c3b53c528bf98af80874c9554`  
		Last Modified: Wed, 28 Jan 2026 02:48:18 GMT  
		Size: 146.7 MB (146702531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.21-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5f1bba7c4268c04b87de29868dc02fe64845dc2adecf7b78cad07d3bcd225557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.5 KB (595456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8c51c5882a400e1e8977d3987f6b5356d1acd9f1b23d049d45e25b7a1ac4e8e`

```dockerfile
```

-	Layers:
	-	`sha256:4b17dcb872624a400075caa646c762f75fa1fefdfb1ffd1cedcec239aeafb0e5`  
		Last Modified: Wed, 28 Jan 2026 02:48:15 GMT  
		Size: 586.0 KB (585978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08b041a2b1767c68f44f50096f563d2278f946eec4bc85b257d92ecf02434dd5`  
		Last Modified: Wed, 28 Jan 2026 02:48:14 GMT  
		Size: 9.5 KB (9478 bytes)  
		MIME: application/vnd.in-toto+json
