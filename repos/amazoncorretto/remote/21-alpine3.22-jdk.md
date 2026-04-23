## `amazoncorretto:21-alpine3.22-jdk`

```console
$ docker pull amazoncorretto@sha256:99b5b506176d5eacbc7febf64ea934df00fe6c9e9e21820f533fc7f09d7b7bfd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.22-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d386fb706dc3d32e70d946f915eacf5fd290a2faa25fa08000ddb2929e81c17e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165623628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a986e772ca0cd780a445c4e4c49272d476352fffa16056912f7801e3673550f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:34:52 GMT
ARG version=21.0.11.10.1
# Wed, 22 Apr 2026 21:34:52 GMT
# ARGS: version=21.0.11.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:34:52 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:34:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:34:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2ce948a3e983c49f58feaa7309cd03268fb53030b47d77cac9e39cd0ff27ff`  
		Last Modified: Wed, 22 Apr 2026 21:35:09 GMT  
		Size: 161.8 MB (161815439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.22-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:42a41e5cbb406568ba7b925cd4648ba28e25d9668f51eb66740b4aee95becccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.1 KB (593064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7e138a42fc9ad8e434aa4a865a49f26091c7688416ec31201f244c45e12990`

```dockerfile
```

-	Layers:
	-	`sha256:ed08e679bc0cb66510e381be2a9cf1a7b35bc8959b48d051d48590ece8b2e436`  
		Last Modified: Wed, 22 Apr 2026 21:35:05 GMT  
		Size: 583.7 KB (583685 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f645fb625560b19cc72ec0af2b597821704e2e2d0cd4e8ed4b218f889b0cfd1`  
		Last Modified: Wed, 22 Apr 2026 21:35:05 GMT  
		Size: 9.4 KB (9379 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.22-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e33128c0a1ec6365150af27923afb09cc1170c11505f730eb1289bd9b533ab6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163970178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690fcb84dc7ccb2a0fc94c80164a2f79548db39fe6bc5361d25221948b329824`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:34:45 GMT
ARG version=21.0.11.10.1
# Wed, 22 Apr 2026 21:34:45 GMT
# ARGS: version=21.0.11.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:34:45 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:34:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:34:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30787b2c31d66cfd7910bf4c5be0ece8a407d52f41b49ab96f0bfdf6f025334a`  
		Last Modified: Wed, 22 Apr 2026 21:35:04 GMT  
		Size: 159.8 MB (159828284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.22-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:afa9c4c156934b6321f26180ab3bfaa997c333438d188dc1f2fb46654d4b423f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.6 KB (592586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78a4038e4d5b425754e759397b32f6ab7a5c3978f25fc1bdceda588a952f1a9`

```dockerfile
```

-	Layers:
	-	`sha256:1e9450e0a9c515d9b355e9dd077c09918ced7780fa361f07ee4411309fc1808c`  
		Last Modified: Wed, 22 Apr 2026 21:35:00 GMT  
		Size: 583.1 KB (583104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cd0c6f89c5b5f6648393225c8bcbd4ccf1dc0b25c97eace78709ba6354be6d2`  
		Last Modified: Wed, 22 Apr 2026 21:35:00 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.in-toto+json
