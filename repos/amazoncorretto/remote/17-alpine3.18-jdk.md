## `amazoncorretto:17-alpine3.18-jdk`

```console
$ docker pull amazoncorretto@sha256:8eadff326545683861f0c96c067aea6cb60660386d84d20556ce1ffaf4bbc9cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.18-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f2eec1bdfee2374f2ed4e6992311c9109e6a0a4fcf321c7469dd1b07bc910d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149431668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062f267627dd555dc86d59eb9b7185e23f7cfd058ddb8189b3d6eb7d53531a7c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:10 GMT
ADD file:aa183dc07d0f6a47c02f7f1388fa0ce4639ad328111172149be7c7c65d634ded in / 
# Thu, 20 Jun 2024 20:17:10 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:73baa7ef167e70f1c0233fe09e741780d780ea16e78b3c1b6f4216e2afbbd03e`  
		Last Modified: Thu, 20 Jun 2024 20:17:53 GMT  
		Size: 3.4 MB (3413894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86877c9432a5dfa60ed4a55790d901a2e434707756fecc8734a88a860f372998`  
		Last Modified: Thu, 18 Jul 2024 01:51:18 GMT  
		Size: 146.0 MB (146017774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.18-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:72d74bf116a865665d3d33218ce9376b6fd5c034553900169606b1d9c5926b00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.3 KB (389275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04fd86b51a68f3a0bbae621b103f55c9b74c9b14da87fce29f8c8c0eb8b1f8d`

```dockerfile
```

-	Layers:
	-	`sha256:1d709cf655780146262a43e509217f337e6ef0d4f80621f15e8679ecd2a1294d`  
		Last Modified: Thu, 18 Jul 2024 01:51:16 GMT  
		Size: 380.1 KB (380103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bb931a092eb25f1a9d6b1343def993b38ffc1a5ba041c998c28a32217c4e5b5`  
		Last Modified: Thu, 18 Jul 2024 01:51:16 GMT  
		Size: 9.2 KB (9172 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.18-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c42a0b9a62f3a81ea2b0efa023b8c68dfe1796e874f83740171114700759dca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147688590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e741326161628e0da27c557a0346f30ac8aac30babe79b70320bb886a72429`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:41 GMT
ADD file:4f760ede9d48d6073317cae6d632deaab101f337e09c56a7f9b8847ed99de3e8 in / 
# Thu, 20 Jun 2024 17:40:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5c905c7ebe2fecec0b1115f145c0ea74b3233aa25d8239903194f6b4424044ce`  
		Last Modified: Thu, 20 Jun 2024 17:41:31 GMT  
		Size: 3.3 MB (3337949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ad20501618025cbc0fb2d405c801152d1983ede65054d1a12ef82019207e5c`  
		Last Modified: Thu, 18 Jul 2024 01:16:57 GMT  
		Size: 144.4 MB (144350641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.18-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6421fa81dbd9ca72329c56aabc14a6f0d7d9182ba4516a7008b94725b28d34f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.0 KB (388993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92bef00ea000919645f2db95ea32ea6b4d375d689a741707faf15047775460b2`

```dockerfile
```

-	Layers:
	-	`sha256:f1be24c1074fc8908667e1c47a04bfb582cf077074a712f7bdc0e94047afa15d`  
		Last Modified: Thu, 18 Jul 2024 01:16:53 GMT  
		Size: 379.5 KB (379521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbf7dd75d9c9188540cd6a9a5fa05c834e39022801b6b6b63101d5e4d49e5150`  
		Last Modified: Thu, 18 Jul 2024 01:16:52 GMT  
		Size: 9.5 KB (9472 bytes)  
		MIME: application/vnd.in-toto+json
