## `amazoncorretto:21-alpine3.20`

```console
$ docker pull amazoncorretto@sha256:ca05e809506b30f75a5b90f766b177e3ae996ac606b63499b4bd75b1b7890451
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.20` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:efb2d6daa75bab089221ac63cd5ec4a437567297d452fd67f9a7bd931ee74b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162659044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b0481381fe97e7f4c669654a07d5a2077766b4855ed1cc2f373657d8b2e542`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=21.0.7.6.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=21.0.7.6.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 15 Apr 2025 21:50:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0acd8a81214738af14edd8b53333d0d0bfec3b366d977b23ab350ad085a8fb`  
		Last Modified: Thu, 08 May 2025 17:05:30 GMT  
		Size: 159.0 MB (159032147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:36c9c25971fb7ad9ec6b540403b27ea24617ae02dcc76d084908f5a529658abf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.0 KB (385974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baa7ec48964d4efc160576dd93dbbbaf5608593cdb0ff79a34f1e9e3401ea0cc`

```dockerfile
```

-	Layers:
	-	`sha256:4374e63d78d691bf55a34d2c30f2361ffd5dc6b7a0f5cb57f660107546a0bd66`  
		Last Modified: Sat, 17 May 2025 16:23:38 GMT  
		Size: 376.6 KB (376560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b76f71c818d098b7b92cd20af1eec72182d864ef5cebf018cc01321c61b57f26`  
		Last Modified: Sat, 17 May 2025 16:23:39 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1a8348a8c2549d4d2c0a3670495d070d3d241ded1bf1f38a28d55690e703729f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.1 MB (161088919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae79c55fb8c188203e6c36294b7cfef7bb0b2bad7ec929c33f06c2842ad542a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=21.0.7.6.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=21.0.7.6.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 15 Apr 2025 21:50:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac99cc06360a87d5db0caba55051c50d6f5e9d504d4eb07ac9f67b831bead05c`  
		Last Modified: Thu, 08 May 2025 18:23:30 GMT  
		Size: 157.0 MB (156997754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:265319010f086baf8a039a90a2d5b06ea4fadac9fbb5b48a9e7ab232589a07a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.5 KB (385497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ce5328f636872c911199f0e9727a871c75f76674aa0c5278685cf31b10846f`

```dockerfile
```

-	Layers:
	-	`sha256:699cbcb3d82e294fd8fe36b194969c702af8ad1eba55ab3c1ba92dc353d33e1f`  
		Last Modified: Sat, 17 May 2025 16:23:41 GMT  
		Size: 376.0 KB (375979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7e4346c202f88224c95376f08076854937cd9c3fca28d702f99381863400c84`  
		Last Modified: Sat, 17 May 2025 16:23:41 GMT  
		Size: 9.5 KB (9518 bytes)  
		MIME: application/vnd.in-toto+json
