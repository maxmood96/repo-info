## `amazoncorretto:26-alpine3.20-full`

```console
$ docker pull amazoncorretto@sha256:9ca5af1b30268622f916fb50189de9a7a44afbe80af34d258ea075021a551503
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-alpine3.20-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bd7860265e7605f4a8e8c58dd18ee44d533b98fb7aca644e54cf38ffbdc36df3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.6 MB (188553485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dee7ae36aac3976c6719e39d0cf030efbbfb0e73bf0498ec27b742f9f73640b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:26 GMT
ADD alpine-minirootfs-3.20.10-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:26 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:35:50 GMT
ARG version=26.0.1.8.1
# Wed, 22 Apr 2026 21:35:50 GMT
# ARGS: version=26.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-26=$version-r0 &&     rm -rf /usr/lib/jvm/java-26-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:35:50 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:35:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:35:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:25f1d6b1951ac8eb3740558fe94cb83d377bdadf95fd9f98b50d2e1b96130471`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.6 MB (3630321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a02ff74a69adb36ae64c810a2bfb1b554fde8a35d6a01578465918a4fac98ad`  
		Last Modified: Wed, 22 Apr 2026 21:36:10 GMT  
		Size: 184.9 MB (184923164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:47d91c419cd1d45dafa69e4180a269e52c05f1c6f3c15d52c5d424efa051ea3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.3 KB (594313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f16f9e6fba317d42e790cffef234503cda6ab8f433144e2d40d11a9254ead6`

```dockerfile
```

-	Layers:
	-	`sha256:cf2cd0dcbe0c8772578f5724e1f8932bea864148b9bee3030bea69a6cb4b674f`  
		Last Modified: Wed, 22 Apr 2026 21:36:06 GMT  
		Size: 584.9 KB (584942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c194a01d4bffb97e0c9fa685c1b266827eb0f1f2105830b6e5d99b69091cd87`  
		Last Modified: Wed, 22 Apr 2026 21:36:06 GMT  
		Size: 9.4 KB (9371 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:26-alpine3.20-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:cb583776dea7929cdb7385a008226cb9a6b1b7b4e055a8fab7d867879eed73fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.6 MB (186601159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56fb6690a8075d983c85d86eaa54b70a1047a3279d3a5c054a8180b5f19e469f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:24 GMT
ADD alpine-minirootfs-3.20.10-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:24 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:35:56 GMT
ARG version=26.0.1.8.1
# Wed, 22 Apr 2026 21:35:56 GMT
# ARGS: version=26.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-26=$version-r0 &&     rm -rf /usr/lib/jvm/java-26-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:35:56 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:35:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:35:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:3f26bc2dec0b515f1c2818f6e13a8f1da1f88179a008445d4e587233386bff78`  
		Last Modified: Thu, 16 Apr 2026 23:53:29 GMT  
		Size: 4.1 MB (4092319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb1a74467914ca9c02534f4551645bfc5d26084951e2eb02e4e98b6338ec430`  
		Last Modified: Wed, 22 Apr 2026 21:36:18 GMT  
		Size: 182.5 MB (182508840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:066893e213525066c4b4e5f3710ac1da085ad8f798e040feb762df9d6b39dfb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.8 KB (593833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5377c5661267bd982542236446ddac5ed9c2a547296f831aedb1f69283be64a4`

```dockerfile
```

-	Layers:
	-	`sha256:ad0f6cb117a2b831245fe494403c5c5073765d08ada27d6eaa2a14e628c20aeb`  
		Last Modified: Wed, 22 Apr 2026 21:36:14 GMT  
		Size: 584.4 KB (584358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a5d80002f7c12c5a5f1a6e49e8a6c97891f61ee960953ac53addf98d3a6fb71`  
		Last Modified: Wed, 22 Apr 2026 21:36:13 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json
