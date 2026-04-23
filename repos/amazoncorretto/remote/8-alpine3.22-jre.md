## `amazoncorretto:8-alpine3.22-jre`

```console
$ docker pull amazoncorretto@sha256:9cf3213143d433d5dca9ae4707a62a65ad5eb26583c21584aac1710c2412fe7c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.22-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2b95dd9c1eb822af63acd391817560b0879b2d3ecc67116ac43ac1805f53e08d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45558825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5657e1e93887527010d8431f706deb443b2f8b58e50c3e1450d180d0894341`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:33:07 GMT
ARG version=8.492.09.1
# Wed, 22 Apr 2026 21:33:07 GMT
# ARGS: version=8.492.09.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:33:07 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:33:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8c50f6e0cd0f913e96aa4a78121c860da36b6966c4dafa88b9e039986c5ae5`  
		Last Modified: Wed, 22 Apr 2026 21:33:18 GMT  
		Size: 41.8 MB (41750636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.22-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:98710f7ab83c900f1b16314ab75ae76db5e8da992584b7a527ff6ce66f0b790f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.1 KB (197146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f39eba5b14cdfe79dbaa4a2b6be4b039f9707a6ed1d29525bcc63c98082299a`

```dockerfile
```

-	Layers:
	-	`sha256:fc3db0a7a8e3c2b30187502ff7a6d0b38be4c2ca7112d9e8d960112c626b1ed8`  
		Last Modified: Wed, 22 Apr 2026 21:33:17 GMT  
		Size: 188.5 KB (188490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cff4fea7ceb1264bf5f29b8fc1aa990424315c97ee0996ae4b03226c24c8be4b`  
		Last Modified: Wed, 22 Apr 2026 21:33:17 GMT  
		Size: 8.7 KB (8656 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.22-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b19bbc460a746133d0edb9a3101e19c436a1e6a55f326fc09038aeec4cb37ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45608087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fdda19a72b753ba8fed9f4c6580d473c05437f78efb2841bdc840501f968a92`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:33:05 GMT
ARG version=8.492.09.1
# Wed, 22 Apr 2026 21:33:05 GMT
# ARGS: version=8.492.09.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:33:05 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:33:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346a50a080db66711e41e972bc536ba1a13f7034f8bd11d3d3ba27cc7ea2ebd9`  
		Last Modified: Wed, 22 Apr 2026 21:33:16 GMT  
		Size: 41.5 MB (41466193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.22-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7d0eeb48725b891a4beae8817d97aac6b8c25b5d610516406b656c08dc1bba3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.3 KB (197334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fa6c745d4a5ad1268b1d88f44aba33c0805cd7a5e162538d83d2f77a4d53f7c`

```dockerfile
```

-	Layers:
	-	`sha256:edf7c71e1d9da2fe5b51d575beed978db3df2c6222222b714928b24b3cb4aead`  
		Last Modified: Wed, 22 Apr 2026 21:33:15 GMT  
		Size: 188.6 KB (188598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2802af69f1cbcc64c1984443d1f79f267cf088453eef8c784eaf3277d9b9783`  
		Last Modified: Wed, 22 Apr 2026 21:33:15 GMT  
		Size: 8.7 KB (8736 bytes)  
		MIME: application/vnd.in-toto+json
