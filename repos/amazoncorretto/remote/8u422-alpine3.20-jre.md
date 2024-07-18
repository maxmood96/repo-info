## `amazoncorretto:8u422-alpine3.20-jre`

```console
$ docker pull amazoncorretto@sha256:52239698c75fcb3651866abdaf7d1aa7c7b6df3fefa9839bf402b4abaf5e96cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u422-alpine3.20-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:dd0e0714f04953224b9ee581be38e6adf3849b29b83447692d4afd8447ec2bea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45223549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507ff2d7ab5a67b448eb4ccb8173151ccd8abd5e3992437f119bde532439edfc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7a4eeefbf15fd4fc10598eb742efaa62e1187cf665ec4f1fe3bec5c320c8e2`  
		Last Modified: Thu, 18 Jul 2024 00:55:36 GMT  
		Size: 41.6 MB (41599705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-alpine3.20-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:317c30a482456c0fab8a6cfca49519535b99b9de2780a384ae6f4921f1affa5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.9 KB (190925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cffceb94f5e49d647cdb8a3f3c139b4f064bf714bd747bb4dfe87f40045fa3b`

```dockerfile
```

-	Layers:
	-	`sha256:c40dccb99924bfc125a04bfa0b71effd9dc85e7f583b31af0e0d03a820d87719`  
		Last Modified: Thu, 18 Jul 2024 00:55:35 GMT  
		Size: 181.8 KB (181811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbac3dfef8f6fe0f16d17b297a9cf512bdb1f3c4996dbc66d0f2e4b566a64841`  
		Last Modified: Thu, 18 Jul 2024 00:55:35 GMT  
		Size: 9.1 KB (9114 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u422-alpine3.20-jre` - linux; arm64 variant v8

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

### `amazoncorretto:8u422-alpine3.20-jre` - unknown; unknown

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
