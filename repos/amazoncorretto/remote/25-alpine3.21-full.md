## `amazoncorretto:25-alpine3.21-full`

```console
$ docker pull amazoncorretto@sha256:673ffea0c9185f5dff95de2a0991ad2de6365c1ce5cc15607502ceb7d351ec8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine3.21-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e26476a726ec0d42a25f088fbb7b78d99e78cb622b28b272e0121b7df7da293d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184359100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c858ae0163f6af2ef2595291f01e243ecdfb573d0c7b600b92073e6260ee84a0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=25.0.1.8.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=25.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebfc0b54202f6d622ca6375536d0ceaf341f4e158cab3cb1f46b7e0e4c5beda`  
		Last Modified: Wed, 22 Oct 2025 01:03:07 GMT  
		Size: 180.7 MB (180716531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.21-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b49c0c9c978d441a382847d2a958f0d46c59a20a58914496cddd0076b94d646d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **605.0 KB (604972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c386a3f25eaf945002d9d69fb26175ed8c0453c41013e5c7420c2451cc2e86b5`

```dockerfile
```

-	Layers:
	-	`sha256:a587f0621e9f17a919646e000341ebdec5e69c2e269bb25e83f392f62677770d`  
		Last Modified: Wed, 22 Oct 2025 00:54:07 GMT  
		Size: 595.6 KB (595558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:051cef79ea7dc7e0557315c3108b3995c1bc15b9d321c557b0b0769dc13368c3`  
		Last Modified: Wed, 22 Oct 2025 00:54:08 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-alpine3.21-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0dbbd901e0da07b0c9bf73487dd103e17721419348735f31a13ec191f0186b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.4 MB (182353630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45d46cbb3c57193574971e50c8433fe4240947800cf70b0d9d49d0bc84d5e5f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=25.0.1.8.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=25.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b2930db70bef7a8ccafaec6cba51e67cb23235825fd81c1d7bcafc5e6e08a0`  
		Last Modified: Wed, 22 Oct 2025 01:03:23 GMT  
		Size: 178.4 MB (178361277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.21-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:02a2fd55d3fb454ff2d8c8f7aec1c9bb06fb2fcb2df5cb112959f69c3cbe4e95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.5 KB (604492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d5fc35453aadf3fc44d2573fbdeb97efd1007c963bb27014252e02db7cd724`

```dockerfile
```

-	Layers:
	-	`sha256:709d35abe4b050568240cab7d10733dbd5a6a28ed8c0c7c6c0b6208528559753`  
		Last Modified: Wed, 22 Oct 2025 00:54:11 GMT  
		Size: 595.0 KB (594974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee1392f2ea85aa08ff97b508f0ad457b8eed8d8f2d3a9f4a0adc73fc889203fa`  
		Last Modified: Wed, 22 Oct 2025 00:54:12 GMT  
		Size: 9.5 KB (9518 bytes)  
		MIME: application/vnd.in-toto+json
