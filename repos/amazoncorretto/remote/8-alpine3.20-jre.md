## `amazoncorretto:8-alpine3.20-jre`

```console
$ docker pull amazoncorretto@sha256:3bf0c6136ecb7af85e7b45da429d66365004e4c3044850d64ef96978be33abdd
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
$ docker pull amazoncorretto@sha256:4778d6ca136ef9b5dfb838a60fced50df3e4047e835a71f82be7e5eac3e69797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45394830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a72fb0b0ca4d7f300f9fb40fedd4087e2daae04b84d6f3b696cb3f046537141`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
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
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8736d61726983c72c9967b2ad4bf8b494c2e76e8dadeb52282cdc86c9f0a6c`  
		Last Modified: Thu, 18 Jul 2024 01:01:50 GMT  
		Size: 41.3 MB (41306030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:73bdad02d77e53696ba539241534f6b89523412c9f330daeb6a5a65724f00a4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 KB (191357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8bfb352fe8d16d3b2d94d5eb6c38d9c065a22df4d2195878e3636baa9851fce`

```dockerfile
```

-	Layers:
	-	`sha256:65f8aa2262885995e1e99b5b947d2a9eab2858ec5eb207c79127b39295cfc272`  
		Last Modified: Thu, 18 Jul 2024 01:01:49 GMT  
		Size: 181.9 KB (181943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:153f9e1c5e94723049867df980348f723d2152ec6f0ae341d371e4758babb304`  
		Last Modified: Thu, 18 Jul 2024 01:01:49 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.in-toto+json
