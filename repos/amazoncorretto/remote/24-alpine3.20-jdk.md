## `amazoncorretto:24-alpine3.20-jdk`

```console
$ docker pull amazoncorretto@sha256:1f677155f58307602d742168a8b877f9998e1a9602f34cde4b2db49a505c5210
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-alpine3.20-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d61faecd51e9af6cfc177f1e37a9d614644e8f1cb0240a12d88eca3572e3010e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.2 MB (180237644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ddaee344276e512b512dc9c99f8b907e1ee947764cce06a811fa44cfa10492`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
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
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320da916d2fc6c701e55ec82886d98100a8f962315cc8d1862a68d8cb0b75a7a`  
		Last Modified: Mon, 24 Mar 2025 17:04:13 GMT  
		Size: 176.6 MB (176610747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c1f78f07713039649ebb1ecf22af524a32a033d856ecfc93d5e83b5ba75f2001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.1 KB (395061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ebfb4983f8758aa6737e3ead879b6d1b53ab56d10153040b5be9458ddffea9`

```dockerfile
```

-	Layers:
	-	`sha256:ccdfcaecb11c23c0e5071c362e40ad17543ebb28f1554516fa605898cfbe6f89`  
		Last Modified: Mon, 24 Mar 2025 17:04:06 GMT  
		Size: 385.6 KB (385646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:561551b60c196df4f643c8a6155369dce6dc24b6aad9adb0ef64f8e79826aa03`  
		Last Modified: Mon, 24 Mar 2025 17:04:07 GMT  
		Size: 9.4 KB (9415 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-alpine3.20-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:46b3fd9d77d7c532f4028ca8fcd18acde9e0b292a9a74f7bcb13d22257d4f020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.4 MB (178386972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f5239b214cc44661269e4429d75cd4625199615037479f2a1ee1f0632c652df`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
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
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:574f8df7517930845e7be43ad15c7a87e46a67888cc5c53c011f043e7044bc3b`  
		Last Modified: Mon, 24 Mar 2025 17:37:03 GMT  
		Size: 174.3 MB (174295807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:503473164a287d36d7400f4f532d4bf3d6ee3d6ff5a22a2788c0a2ade712ff69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.6 KB (394581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1482293566ce93dc6236bcdc84479678054752fbb7e86f7a02bf022789b14428`

```dockerfile
```

-	Layers:
	-	`sha256:01c0a4e0bc3e34de7eb4b936f9a5c85f3acc6d74838dc4cf662e9ccc9574e41b`  
		Last Modified: Mon, 24 Mar 2025 17:36:59 GMT  
		Size: 385.1 KB (385062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f57c7ec145f8ddbe2ec69cc996a3dd1afedca869bee800753b7662fa5016cb91`  
		Last Modified: Mon, 24 Mar 2025 17:36:59 GMT  
		Size: 9.5 KB (9519 bytes)  
		MIME: application/vnd.in-toto+json
