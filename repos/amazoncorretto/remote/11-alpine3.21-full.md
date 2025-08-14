## `amazoncorretto:11-alpine3.21-full`

```console
$ docker pull amazoncorretto@sha256:ba7eb23bd679f29eeeeaf63d2d5ad706760169bf7a5ac297307cdc2faa9898c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.21-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:fca670d5e310bf38e6ac0116b57dfb994918be1c9784063c2bdbddca9d27bfd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.7 MB (145707980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2874313c2daf7e542b8683ede1d73e134475cd939df763171d6591e6d7adc3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
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
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdde68ebab917c99652a28e4ef94368ffd2c38d5a09242bdb7563b62ea60f65a`  
		Last Modified: Wed, 16 Jul 2025 21:08:42 GMT  
		Size: 142.1 MB (142070410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.21-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c9b52d0e504fd1a2affe7ec9efd1f327086c08c79a30f028e43f58420ef3132b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.8 KB (402812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3b266a822091ad12143394344f56dd4bae34e16a34c4b31f4b292ecc33b62d`

```dockerfile
```

-	Layers:
	-	`sha256:6a105c3d8ece27d3e4f91ff0d91c9c2ff8c52ef7f6b074dbf316dc2f0417db4f`  
		Last Modified: Wed, 16 Jul 2025 21:47:45 GMT  
		Size: 392.1 KB (392090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51c55f34985e0df2739515939a44cabd1413e9e14dec77b8102daef012a2b1d1`  
		Last Modified: Wed, 16 Jul 2025 21:47:46 GMT  
		Size: 10.7 KB (10722 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.21-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:73dded60da62564ed8f26888580528bb06f39b85c6cdf433d14a39b4f8d0f0db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.2 MB (144228787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eff6f7ef1302334591a1a232a14c68067575968dd1accacc1cefb3733436715`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
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
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97acd4945919de2184cfe465caca4f9f7554d6cff5805d778c39174fee296d2c`  
		Last Modified: Thu, 17 Jul 2025 04:17:48 GMT  
		Size: 140.2 MB (140241850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.21-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:db2317e2b2601c3ff63028928e75ad4b0ff903ad56d55d98e2fbab3c532a4634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.1 KB (403071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f5f5edc808d152a389089739e4cea758d77feff75f279d262cd5987df449c35`

```dockerfile
```

-	Layers:
	-	`sha256:0b1d0c871b9fdd13e2be3b63d596ba03715cda3a6f35c5de2bc06ff438bbf6f4`  
		Last Modified: Thu, 17 Jul 2025 03:47:43 GMT  
		Size: 392.2 KB (392194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4087a543992494afdf6ceabf767b5536afbf86b1e641d0e874cafd49969f91be`  
		Last Modified: Thu, 17 Jul 2025 03:47:43 GMT  
		Size: 10.9 KB (10877 bytes)  
		MIME: application/vnd.in-toto+json
