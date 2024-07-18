## `amazoncorretto:8u422-alpine3.17-jre`

```console
$ docker pull amazoncorretto@sha256:837d6b9222c9f03fe8069229cda1a26be644b8b587a0e5ab9f980844f28378a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u422-alpine3.17-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:be1f8bb09503dcf194bda58c37385735f561aa6fd134a091281ab76c3c91ebde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44989324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0901056c919de4463f0918df89a4478fc1e4a6f87fde1db02573ffd048c70250`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:15 GMT
ADD file:cbcddefa487fb5085857fbba16854e06e53f93295bbf36ef1968a0b89835cad7 in / 
# Thu, 20 Jun 2024 20:17:16 GMT
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
	-	`sha256:f9202480295a4ef9cc62343dea568a5840b58bc68a1970045d30f3077a46a471`  
		Last Modified: Thu, 20 Jun 2024 20:18:01 GMT  
		Size: 3.4 MB (3389963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53dd8e216aa6801631189f57bd4549c4925fa7a4bd3fd656c9b656b9c935d3f`  
		Last Modified: Thu, 18 Jul 2024 00:55:25 GMT  
		Size: 41.6 MB (41599361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-alpine3.17-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:51026ba6d627fa95f957d309a4d23af19d9b846f6a4312124c08d3622b4f8352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.6 KB (192578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:013aa4912d01439721e731a99cbbeafa3f696779bff77521128cf001150833d4`

```dockerfile
```

-	Layers:
	-	`sha256:136ca563f3b819f7277f149e4b5e4f8fd823af384b2856666c9cb0ae7fbeb69c`  
		Last Modified: Thu, 18 Jul 2024 00:55:24 GMT  
		Size: 184.1 KB (184124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b27f6a62765898a3685113f887c5370e0c2bae81cf71cbf12b6f12b450b7bb8b`  
		Last Modified: Thu, 18 Jul 2024 00:55:24 GMT  
		Size: 8.5 KB (8454 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u422-alpine3.17-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:80cebc22bbc7bd425b8531bff1f5826ec785a6ff66b31369d7d49ff2316f4a53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44578628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d9aa593f860a52caf4d819709428149a8649d06305d4ad7a34d0d39edbe9c5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:45 GMT
ADD file:deb5b1c3cd4e7a5be179620c767b9d7bfac29f2544596a65b760460e7a645c51 in / 
# Thu, 20 Jun 2024 17:40:45 GMT
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
	-	`sha256:e45a60384f0269bd8514e16cf71591639353996e62a144763c5e519b386ac31c`  
		Last Modified: Thu, 20 Jun 2024 17:41:39 GMT  
		Size: 3.3 MB (3272586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd4551a81efcf753b7f1ec21bd1a0251b16dfec0a64c9232b1343c9238c733f`  
		Last Modified: Thu, 18 Jul 2024 02:13:57 GMT  
		Size: 41.3 MB (41306042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-alpine3.17-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:466321fec4d73ab197924e553ef19d40a017ef2c740008f9618b14ff54bc7830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 KB (192962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5a685482a23cf397d02c63a92a95b09b3f623a6ea59b53bb315177a6aebfb2`

```dockerfile
```

-	Layers:
	-	`sha256:0e6896ca98a08c1ca8ada4b5200a0e6c4ac445c020b900a13e4c1442f6b1f412`  
		Last Modified: Thu, 18 Jul 2024 02:13:56 GMT  
		Size: 184.2 KB (184232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e490b596a970d07d34401636e06f77b3fb1840b9f5905556fe154f7b09165caf`  
		Last Modified: Thu, 18 Jul 2024 02:13:56 GMT  
		Size: 8.7 KB (8730 bytes)  
		MIME: application/vnd.in-toto+json
