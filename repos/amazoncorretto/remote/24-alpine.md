## `amazoncorretto:24-alpine`

```console
$ docker pull amazoncorretto@sha256:34d26eacc2c93bc6884f60ab0f57d12a2908a2eb6e0086957da10e7d289d8ff0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:09a3fb73c7a816a0f25f20c267d73e218ebdf4fcd0d294d1b849f1770f1b489c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180251468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b612a6e74d97bfc5df87acaa1103a2ce86d569bc16d975d574e9e4db725e0c7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=24.0.0.36.2
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=24.0.0.36.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-24=$version-r0 &&     rm -rf /usr/lib/jvm/java-24-amazon-corretto/lib/src.zip # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 21 Mar 2025 22:11:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025a806746242dc05a0cabd6f430ddeee7f3326ca3cd0cf82733f763885b199d`  
		Last Modified: Mon, 24 Mar 2025 17:04:13 GMT  
		Size: 176.6 MB (176609221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-alpine` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:336e09116bc74270975486a3ed6e75d34f9ed35a1288e53fe2b03677d2ddb600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.4 KB (403399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:333ea90e3a0a6e51307fde90da0a59e547682462542a411f79ed82c3b9621bcb`

```dockerfile
```

-	Layers:
	-	`sha256:55b58719eb3f631518349f2614fe9535342ea1707425ce1d84db864af167d164`  
		Last Modified: Mon, 24 Mar 2025 17:04:09 GMT  
		Size: 392.7 KB (392678 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b8497bcfdf00e1f0afc03827750fad8e47aceab4fe1dd56f38261606729ed68`  
		Last Modified: Mon, 24 Mar 2025 17:04:09 GMT  
		Size: 10.7 KB (10721 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-alpine` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8a478cab8777e19125cfb24f82bb548945303a5ba8093437897bef4f0df9b7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.3 MB (178289785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8ad855e2ed1b11bfe356c1484bf0b7e38613badd742ffb57d2ead55282f1f8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=24.0.0.36.2
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=24.0.0.36.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-24=$version-r0 &&     rm -rf /usr/lib/jvm/java-24-amazon-corretto/lib/src.zip # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 21 Mar 2025 22:11:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b200419fbb2411dd3c011ec68c33ef49e2454e21c14a549aae4de7fb9256391`  
		Last Modified: Mon, 24 Mar 2025 17:37:38 GMT  
		Size: 174.3 MB (174296756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-alpine` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3fc4a60e5eba6177bf952e03167f54bedfea853f5c2a1601e6d8fa1d4b0a6118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.0 KB (403014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196c4889330cfc496a5fa5f5bee72d872ed364706cad937edacb4c0c5f487cb5`

```dockerfile
```

-	Layers:
	-	`sha256:24ffa8b68f75bac5bc649059a42109e9f56b260ee80d4dd24dc81d9da4941077`  
		Last Modified: Mon, 24 Mar 2025 17:37:34 GMT  
		Size: 392.1 KB (392142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:279fd3d69167e6d84d79f3062c37c046860d6656b5d9057d97bf3c4dcaabd2c4`  
		Last Modified: Mon, 24 Mar 2025 17:37:33 GMT  
		Size: 10.9 KB (10872 bytes)  
		MIME: application/vnd.in-toto+json
