## `amazoncorretto:8-alpine3.19-jdk`

```console
$ docker pull amazoncorretto@sha256:988ee537986666532c5b8581d82a5e7b2ee5c8e0d04a59b2d6e08d8fec945fc6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.19-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d6b2d311a9e356d47e75951a3b3654f3b92dd4478a91a511d92f1e8810c81fcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103616948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3116f342832df3bed7340226c2039b471d4c1fbb4eb50ccd0a9b28e6fe3c8ce1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=8.432.06.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b700b01e0c01a7eaa4c2d32ba640aa5527e1cc03789feb8f2d7321961c88f3e`  
		Last Modified: Tue, 12 Nov 2024 02:11:45 GMT  
		Size: 100.2 MB (100197220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ef4cb14abafe94fdb383a206287fdb9389507f139a9d4c5da40c83cceed5c0be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 KB (255282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efcfcc14941d7ac5796bde0a832f96ed9b6f68619c5c8140dd38b5597aa31a51`

```dockerfile
```

-	Layers:
	-	`sha256:1aca4df51ac3d84810361407f423f61794f532a9d7ec16202d6bf3282cb56536`  
		Last Modified: Tue, 12 Nov 2024 02:11:44 GMT  
		Size: 245.9 KB (245885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78a94c85a82a1e1f05af614c1e9a5b7edd4e7577f6e8f8a58ed900ef8d5142e3`  
		Last Modified: Tue, 12 Nov 2024 02:11:44 GMT  
		Size: 9.4 KB (9397 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.19-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7ece8adbb1c1f9c4ab4de0c9e02d78677a6a56495fa4e56af43258dd39734330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.3 MB (103338324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afada319287cd7b5d29c12f469c2f9e929577a4f0c3e1f176467f92b7182e5fe`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=8.432.06.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc8eee8cc96a9553912c158db877ef4d5c02d81833d0c47cb76cfba118e08ccc`  
		Last Modified: Tue, 12 Nov 2024 11:04:18 GMT  
		Size: 100.0 MB (99979078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f6c4fb8147fe7a6172563c6ad2d5302827fc75d28535daba8096f79be8863dd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 KB (255518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea4d3a4866d70f6ce52664c962f8cadf3fb568ba85d791e39550c7f5b2b4d9e`

```dockerfile
```

-	Layers:
	-	`sha256:22e2cfdec280411ab640c8854f0f26d01f2093e0c03e1f77d539909588346749`  
		Last Modified: Tue, 12 Nov 2024 11:04:16 GMT  
		Size: 246.0 KB (246017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49a95c6295cef24fa781487c80385efe636be2d01d45d959912dcbb5b0d377a9`  
		Last Modified: Tue, 12 Nov 2024 11:04:15 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.in-toto+json
