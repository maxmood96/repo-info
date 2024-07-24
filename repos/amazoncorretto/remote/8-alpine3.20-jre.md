## `amazoncorretto:8-alpine3.20-jre`

```console
$ docker pull amazoncorretto@sha256:9c9340adf3f63915052fe256bf0eaa44d1145fb23ed00984204bc0e2d9a31f8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.20-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9350fd444609b5c7def5f349fd30b1c17346509be83469bc574d82928219824c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45222551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57b7f737d641c3146161254f2d81d805891ca8ad1e988a304c53749c50abe14`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:129cd1d8324178f662422a9706c48afd03d783b870045a6423c8ff7137f7b581`  
		Last Modified: Mon, 22 Jul 2024 23:04:27 GMT  
		Size: 41.6 MB (41599659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d020357431e54dc10f97a114637d1b3d99f0babddee9f22d4477f59458cc82e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.9 KB (190925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ce5b1d25832ef93f37a8d10f616d84c56f30463bf38c47e8c8aec5ecd2be1c7`

```dockerfile
```

-	Layers:
	-	`sha256:d5d2be38b4369b00c99bfad976b21ae021ad6810e59db6c36670a9243c498860`  
		Last Modified: Mon, 22 Jul 2024 23:04:25 GMT  
		Size: 181.8 KB (181811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe0582aa41d9196c0b65516aecdc68d937c958dfefa59213cc709ecc44db3a01`  
		Last Modified: Mon, 22 Jul 2024 23:04:25 GMT  
		Size: 9.1 KB (9114 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.20-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7893b3fd7f39e99160dcccdbead6ea49ab1ae99e6d634afff57eee5665d259d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45393001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8687f445814a0c39b9cf913c2cc492b51b2736fb74c0a410d2eb28a1b5429e79`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17277bbeb2222bb58f548ed656a91bb4ad3615ea5cacec81efe0091045e090cd`  
		Last Modified: Wed, 24 Jul 2024 16:29:55 GMT  
		Size: 41.3 MB (41306067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9e0e218fbacab07aa92e25cd946e8f989b2cc7d2876e8e3bf44f87459e8ec23e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 KB (191357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8466f36c4d0a4e01ab29fdb77cddb5191ca72e59a8bb1163c9001ce29468f13`

```dockerfile
```

-	Layers:
	-	`sha256:f2afb5645dcd7a52f567f09029dcca20632b7e935de409e8fd9e8fbcfe206cb2`  
		Last Modified: Wed, 24 Jul 2024 16:29:53 GMT  
		Size: 181.9 KB (181943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f2842dea1bc50f19e83f0ead892d646eeb858f3fc2bcc0b5c84c46e50d09dce`  
		Last Modified: Wed, 24 Jul 2024 16:29:53 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.in-toto+json
