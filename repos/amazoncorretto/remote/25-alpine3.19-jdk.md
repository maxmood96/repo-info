## `amazoncorretto:25-alpine3.19-jdk`

```console
$ docker pull amazoncorretto@sha256:7bf1c44a3e7fe93d5afca9db99c77b74a538ff808c5ea7d7a0271e496de3a29c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine3.19-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a776760c60d5f4e6b938c2bb822fefabc3c80cacd51e077cf9f4fb5651cd5944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.9 MB (181940865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f871b023568b17f1abb80ab7b0b85bee4204f5fc57c14e60db47e5b50eb18127`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:32:09 GMT
ADD alpine-minirootfs-3.19.8-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:32:09 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=25.0.0.36.2
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=25.0.0.36.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:1747dece94917ce1b0256ecd60138ce4deaea1bd35dcb6b2e8afe697dd2f5b71`  
		Last Modified: Tue, 15 Jul 2025 18:59:51 GMT  
		Size: 3.4 MB (3415528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41caf809d498273c367e53a8651cc1f7ecb7b82c59fcd86eadf955f1cb03c88a`  
		Last Modified: Wed, 17 Sep 2025 18:58:45 GMT  
		Size: 178.5 MB (178525337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:523cf5211888cb740f6abf0f016eefb5d1d539d8e2ac0d0fb63da1a06d82e039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.9 KB (400894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a88db849abad8447c0036bb6ca4e57c612ca6ea4f2847dc6a104c0436126413`

```dockerfile
```

-	Layers:
	-	`sha256:286d41e7a311768ee94f418aeb96b2635b0e62d368222c08efe72c9484fdbf93`  
		Last Modified: Wed, 17 Sep 2025 18:48:57 GMT  
		Size: 391.5 KB (391479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ee98c2bbc35962dff24599d390e2ab53e2c0e18904b43be1a241376e1500a57`  
		Last Modified: Wed, 17 Sep 2025 18:48:58 GMT  
		Size: 9.4 KB (9415 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-alpine3.19-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:91ef3f7275d5b63991efec877fda9a935df7cd63fcb98619e111a847fe92dbac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.4 MB (179425590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ef572316dce9c2e93d9e2ed4e0356f2addb52c8f134f973c83c384af013d1a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:32:09 GMT
ADD alpine-minirootfs-3.19.8-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:32:09 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=25.0.0.36.2
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=25.0.0.36.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:07e9a47f0c334cceba1b05e86ef0150c84564a9b9e9d4ae9dc9a5ebc85ef2b7c`  
		Last Modified: Tue, 15 Jul 2025 19:00:19 GMT  
		Size: 3.4 MB (3353103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1731f2266fbe470daa7ccfa441a37873749a4176eed1576eda5b0442b611f43d`  
		Last Modified: Wed, 17 Sep 2025 18:58:45 GMT  
		Size: 176.1 MB (176072487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b8cd5d2d43a82c4a5725feac39178e2a48079275e6c07ddba982af9a95af7092
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.4 KB (400413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ec12f6a921c5d480eff89157a30a3238ef033711e407a4c1e9633a0cfc0cf7e`

```dockerfile
```

-	Layers:
	-	`sha256:ed7608f92a905279d4d6f69c8c419437a65b6c7d222cd7bfb5e6416ed343342b`  
		Last Modified: Wed, 17 Sep 2025 18:49:02 GMT  
		Size: 390.9 KB (390895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b19fc2a84a40c79b53f19823f3853a9272eb0fc0ad40bfdc9e9a3c259632f026`  
		Last Modified: Wed, 17 Sep 2025 18:49:02 GMT  
		Size: 9.5 KB (9518 bytes)  
		MIME: application/vnd.in-toto+json
