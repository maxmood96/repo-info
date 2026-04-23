## `amazoncorretto:8u492-alpine3.20-jre`

```console
$ docker pull amazoncorretto@sha256:1f6603290dc0be7163a85bbda5bc67a79cf2bf4f90b087035603658c5a8f7987
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u492-alpine3.20-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7bb2bac50312367703c744492bf0728f8a5f6d749b982bafb96aae47edb24121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45386177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3971adf273dba51440aaa0abb3697ad3f1a8a8e54cfc671ded29a6db3f9356df`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:26 GMT
ADD alpine-minirootfs-3.20.10-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:26 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:32:44 GMT
ARG version=8.492.09.1
# Wed, 22 Apr 2026 21:32:44 GMT
# ARGS: version=8.492.09.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:32:44 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:32:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:25f1d6b1951ac8eb3740558fe94cb83d377bdadf95fd9f98b50d2e1b96130471`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.6 MB (3630321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c41ffe19f3a543aa0df2dd6ecfd48801c046fda47d98d809986fbf13e4e8bf`  
		Last Modified: Wed, 22 Apr 2026 21:32:54 GMT  
		Size: 41.8 MB (41755856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-alpine3.20-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8b5ba8d6d85d59d061b098cf74ffcdc9b0887596aaea3c774987cb99ba09b6cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 KB (191473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1609cea2858d6639977c78cb6e15be2c19ce541ee01eed98f61cfaea565f8ad5`

```dockerfile
```

-	Layers:
	-	`sha256:b1f3b2c2a66dbeb2f88aa8018de29f27395acba56857e980c46256de7b0b3918`  
		Last Modified: Wed, 22 Apr 2026 21:32:53 GMT  
		Size: 182.8 KB (182818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a58f9650ea6c9fb8a8f7059026cc6ce0fda90252ea934d62787c7ec6b6825b5`  
		Last Modified: Wed, 22 Apr 2026 21:32:53 GMT  
		Size: 8.7 KB (8655 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u492-alpine3.20-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:efb527c426896e5e7c27a53f382fd0af23fbb949d4cf210ea9929990547a1dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45554419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e70bbec55aa9b511df25f546531a85de47ab2b14e2bc7e3e00d8a5ee570966`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:24 GMT
ADD alpine-minirootfs-3.20.10-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:24 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:32:50 GMT
ARG version=8.492.09.1
# Wed, 22 Apr 2026 21:32:50 GMT
# ARGS: version=8.492.09.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:32:50 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:32:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:3f26bc2dec0b515f1c2818f6e13a8f1da1f88179a008445d4e587233386bff78`  
		Last Modified: Thu, 16 Apr 2026 23:53:29 GMT  
		Size: 4.1 MB (4092319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4186f21fa771df683edfdfaec425adc7c8bc3edc969830171fdbfcefd997f1d4`  
		Last Modified: Wed, 22 Apr 2026 21:33:00 GMT  
		Size: 41.5 MB (41462100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-alpine3.20-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ced5bceceb41d94c0a1f9ebb6296c32a53df4066849b3fafc49d58d92891b836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 KB (191662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cfe0cc20c00d35f8c2cfe265b116f2266fac0ad9ecca46d25f149655c86ea88`

```dockerfile
```

-	Layers:
	-	`sha256:f086ed194a0d1287dcfd4bf163e2064c18d1b1d03392988db9d04edecab9d653`  
		Last Modified: Wed, 22 Apr 2026 21:32:59 GMT  
		Size: 182.9 KB (182926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58b10b824b339b0f84220ad56da3b74efb2bfc4038d859ad7b9c62f1ccd5c2e2`  
		Last Modified: Wed, 22 Apr 2026 21:32:59 GMT  
		Size: 8.7 KB (8736 bytes)  
		MIME: application/vnd.in-toto+json
