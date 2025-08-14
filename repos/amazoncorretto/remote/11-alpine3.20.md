## `amazoncorretto:11-alpine3.20`

```console
$ docker pull amazoncorretto@sha256:e27fe3484d93270fb1c21316765ce050a296da0f65cd3bde41e79748c07152a6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.20` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d5265420e5a64e74a3c086ee55a9b5a065c8407d98fa050bfaa0c45d1a956071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.7 MB (145690694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d3ea5b2a06d5fd7e66afb26c9f2af85e2678fc4e711d258dd7d357758517128`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 19:33:24 GMT
ARG version=11.0.28.6.1
# Wed, 16 Jul 2025 19:33:24 GMT
# ARGS: version=11.0.28.6.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Jul 2025 19:33:24 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 19:33:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Jul 2025 19:33:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c4ee234fcf03d1f7f8b5c4aa2cb0d17eaa65874bd771fae48af8b414579073`  
		Last Modified: Wed, 16 Jul 2025 22:58:08 GMT  
		Size: 142.1 MB (142070217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9c0e08dc64398baaa086c4ace0454faa112fa6e8d2eafc3e3d3dc037381c9a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.3 KB (394296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d255396a5080f0b8a74c5bcbc867c46940bdcc62ea6bc1f376ec47e49eda6c`

```dockerfile
```

-	Layers:
	-	`sha256:a3ac03d1944f00fab0e6652b62326815ae53b1eb4365d4f69645ea1bc56d1e75`  
		Last Modified: Wed, 16 Jul 2025 21:47:58 GMT  
		Size: 384.9 KB (384879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63e171bc46e42dcd60719197be1922a5f6527b650ad0f660cba7276768f81fbb`  
		Last Modified: Wed, 16 Jul 2025 21:47:59 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:89e1c5821c75a232187c42d8a81631c29b01bce70d2baeded754d21af188083f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144328655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89e6c8018b33de6389a27e1a8779b7cdb18628a60f1438ae7daa3fe7eb296d2b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 19:33:24 GMT
ARG version=11.0.28.6.1
# Wed, 16 Jul 2025 19:33:24 GMT
# ARGS: version=11.0.28.6.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Jul 2025 19:33:24 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 19:33:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Jul 2025 19:33:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:13e713f825654e9e4f57146ec84918d478434f708d4d3d9d18d0e7ba2be56801`  
		Last Modified: Tue, 15 Jul 2025 19:00:10 GMT  
		Size: 4.1 MB (4088368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc1d95bc1ae639c91da684ec165979669aba377aebaa10640acad0d2c31afdf`  
		Last Modified: Thu, 17 Jul 2025 21:06:12 GMT  
		Size: 140.2 MB (140240287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d5f0bfdc0695c604a8576554f3054867d9d3e24315e5cf799e403b89933267ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.5 KB (394456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba31adccc4c468f10a71c361b8adf31951092c315a992dd8b5d1030d84570365`

```dockerfile
```

-	Layers:
	-	`sha256:2a3924c952eb297912337658fbd4cafdd83f863dec387bfeb96a11650dce6eb2`  
		Last Modified: Thu, 17 Jul 2025 03:47:53 GMT  
		Size: 384.9 KB (384935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfef5b6dd5b2f6f1dc3cb38c00f583ec553e27deb71c1c85815a1f2a352a15c8`  
		Last Modified: Thu, 17 Jul 2025 03:47:54 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.in-toto+json
