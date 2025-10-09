## `amazoncorretto:11-alpine3.20`

```console
$ docker pull amazoncorretto@sha256:2df75c5087ef6525ba3f96bd47d2326a61d157c31f7d8ec8493b05df2bdbf67d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.20` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4964c79e0b0acbd29d54952aef6fd72fc7a10c30e1b6106b3704dbd56e4b948b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.7 MB (145697221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8f20c33a6d7501d7f6fea1b4fdb948a39093e150f5182cf588b7d760a55b404`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=11.0.28.6.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=11.0.28.6.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8670d04c60d2a8d641d1fd22b358bbfbdb1c1d9184b793ef87e80519d6980e8e`  
		Last Modified: Thu, 09 Oct 2025 02:03:53 GMT  
		Size: 142.1 MB (142070165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7954b839de642c65e2f8d9d32303e9232b2f877601fff3c7f5f9950f7424f154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.3 KB (394296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736b77a6638e277af9917f96097fd5e8aba08813177cd12f3c6250db9073bc5d`

```dockerfile
```

-	Layers:
	-	`sha256:e4fb2b6ec5d3a2af302b983593f3c458016067e9ed61bf7978151529cc6abd65`  
		Last Modified: Thu, 09 Oct 2025 00:47:44 GMT  
		Size: 384.9 KB (384879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b295c02d5e6160545702543767b430376423a8ee01af1328bd0d0ca01983e39`  
		Last Modified: Thu, 09 Oct 2025 00:47:45 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5e8b6b360b8453ab5b2b6e912b699f5e114b22ba157d395c45370b70cbf9c593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144330022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7cd59e612bdba0f5509599ab6225d8515998896f32dd5d60a52000f8ab63620`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=11.0.28.6.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=11.0.28.6.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Wed, 08 Oct 2025 12:03:09 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f5c52df819fca20102318c149cf923f668ed574d6fc4ed6cf5aae1638e140f`  
		Last Modified: Wed, 08 Oct 2025 22:24:29 GMT  
		Size: 140.2 MB (140240645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:413e62df9bbb8f31b2132ae3a86eb3fffc3cc03b2ff24f45b3a4b6a059a68033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.5 KB (394456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb703982aa1980019169e376cd489a533962818e79289da0f1bfa2dd5d47070`

```dockerfile
```

-	Layers:
	-	`sha256:652c971d9beb992e7e7172fe40ab3fbdcccbc6ee770541b03c7814df605f8430`  
		Last Modified: Thu, 09 Oct 2025 00:47:48 GMT  
		Size: 384.9 KB (384935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b15fa89de080897e311c22b2fbc46942392fbfa26e490fe433f80dc909d5488`  
		Last Modified: Thu, 09 Oct 2025 00:47:49 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.in-toto+json
