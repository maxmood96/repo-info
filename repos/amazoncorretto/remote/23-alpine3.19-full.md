## `amazoncorretto:23-alpine3.19-full`

```console
$ docker pull amazoncorretto@sha256:07902b3fa3f7d4af47d194e5803c94af25aae086f0cd808ba8de1ae5ccbf20f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-alpine3.19-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:fcb07166b9a6cbd06c8da696c0170abb7cc3998e1fc63592ce6721253bbdc0d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170078175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26553beebc29781353f41fe43ea5959ef107be06ffb3b3869c80e7fe8c96d6ac`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=23.0.1.8.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=23.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:35225bd680c3a257c7710272e8788cf89a5523d1e1a74c0553ce753d9cb06001`  
		Last Modified: Tue, 12 Nov 2024 02:13:04 GMT  
		Size: 166.7 MB (166658447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:257bdd8ae1bdb09cd50cf20cf8edbc1906fb9eb6d41d787f21e6936decee3fcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.8 KB (392783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c603f77f4bc3083126bca48b088c15ea80916e767dd02e60de669bccaf18918`

```dockerfile
```

-	Layers:
	-	`sha256:c26b127321d9bc48f154071e80e0cc9ace22d7028e355447d7439b0374314e50`  
		Size: 383.4 KB (383369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:093743622eccd6dfd1fe887cda090762a7d5a37d21f968eda60f799e2d8d0446`  
		Last Modified: Tue, 12 Nov 2024 02:13:02 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-alpine3.19-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e511832d9e7509cb40c0dbc6e9c753177ed09c1bc3760fcf65735a1fcb29cd9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.7 MB (167712322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bae4e372f2c90505ac4bb3413e09c46091a89457d434a919129acec8afedba7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=23.0.1.8.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=23.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbd0c45c6eea259598817c87ad8dc951eb824127bad36995733e93fef73fe33`  
		Last Modified: Tue, 12 Nov 2024 11:15:04 GMT  
		Size: 164.4 MB (164353076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:aca9bcd8ea8bd4a42f227557af22be9c45a6ccf8c6653ba23a9616f14080aa93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.7 KB (391664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd6fab89ef40f09a267f4a16ce771c758c004c1c7ae66495537188f643c9a9e`

```dockerfile
```

-	Layers:
	-	`sha256:71afbd348deef6ba48dd99339178fabb3e917fc3db8292dc4f2cc023d50b15b7`  
		Last Modified: Tue, 12 Nov 2024 11:15:00 GMT  
		Size: 382.1 KB (382146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdce43b8728de939fb4749ef46e4e69fc698dbd911f6cce43d775de13dfd29c2`  
		Last Modified: Tue, 12 Nov 2024 11:15:00 GMT  
		Size: 9.5 KB (9518 bytes)  
		MIME: application/vnd.in-toto+json
