## `amazoncorretto:8-alpine3.22-jdk`

```console
$ docker pull amazoncorretto@sha256:701762fce1c7df73891b2194dcc99802fd3103cc75ce0cf184a420f3e1cc2363
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.22-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7075877a4bb1386192e95e4d2adab97f35c18dd5059d3091025d426b85a2366d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104579785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144bee287d3a4119ab32b554b41a35c35fd9fc109e14c09882fdbd023e2cc0a6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:42:10 GMT
ARG version=8.482.08.1
# Wed, 28 Jan 2026 02:42:10 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:42:10 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:42:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:42:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f9a43f049ea25a81da607ffb2173ccbd05bf1c4e5e479384ebfd9309a10462`  
		Last Modified: Wed, 28 Jan 2026 02:42:24 GMT  
		Size: 100.8 MB (100774910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.22-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f81ff5cf2f6099591ef2b7bbc99e871dab828f1c6ca599e3f97a82a708545f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.0 KB (257029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c1bf89067f99ca7dfa12cccba7f0432e93b0246dca43be47c61a407214df3c`

```dockerfile
```

-	Layers:
	-	`sha256:f683283eafee5f8b3d7799525197ffb2a50fa722393869110b205e4f7f0e0065`  
		Last Modified: Wed, 28 Jan 2026 02:42:22 GMT  
		Size: 247.7 KB (247674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6682bdd3ef7fb62066a7adf183baa4ce0f1dfb150e7955e70fc8a17103f1705`  
		Last Modified: Wed, 28 Jan 2026 02:42:22 GMT  
		Size: 9.4 KB (9355 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.22-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:416bfccc23ad4d5dbfbe451903e492daa03488820389fe08b6267373037c8fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104699220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18b9ea395f6cf971084e8dd851e0a0f7b27b26059fc7e2b3f5caeaa6e9d26a18`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 18:59:39 GMT
ARG version=8.482.08.1
# Wed, 21 Jan 2026 18:59:39 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 18:59:39 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 18:59:39 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e139de12827dca78824165f354dcc2173b3b0cc2fbe0c68732e30942e998149`  
		Last Modified: Wed, 21 Jan 2026 18:59:53 GMT  
		Size: 100.6 MB (100561151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.22-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6707e99630a58f7a2ec7b17831f695ff9005dc4ecf7ed684f9387743c35b16d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.3 KB (257265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09280a079079a2f9ae601f7310fbc465f52730add8158bd471ffec24439ec7b5`

```dockerfile
```

-	Layers:
	-	`sha256:6f3184d61bcdb9e568cf40653b3c09d9f41a8e17cbb7999fbc50e19a669e9128`  
		Last Modified: Wed, 21 Jan 2026 18:59:50 GMT  
		Size: 247.8 KB (247806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e5e38eb321e9372defc2b7494ef1d6d92870c7ec9487cd490445b495d9b2bf8`  
		Last Modified: Wed, 21 Jan 2026 18:59:51 GMT  
		Size: 9.5 KB (9459 bytes)  
		MIME: application/vnd.in-toto+json
