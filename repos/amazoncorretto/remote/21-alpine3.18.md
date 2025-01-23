## `amazoncorretto:21-alpine3.18`

```console
$ docker pull amazoncorretto@sha256:31436be79c9d31afaa805d4aa6cf2706d2dbe9d0f407d3505b50bd508090941e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.18` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e918c92749f92308944df81ff43ff17bfcbf15c940d2a001e1f041b1dfc7d5f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162348004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f37393715a805dbac8bc74079657313d2004c581809176ffb3fea7abb756a0d6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.18.11-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=21.0.5.11.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=21.0.5.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f54a5150a7602eaef3169b83e73d5927b20aef2fcaefcba18b532bd63b328fff`  
		Last Modified: Wed, 08 Jan 2025 17:23:37 GMT  
		Size: 3.4 MB (3417974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d598ea955da2f810f84f5476eb0a3b9ccdae9d122c999ed7d7a376445069248`  
		Last Modified: Wed, 08 Jan 2025 18:13:42 GMT  
		Size: 158.9 MB (158930030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c3000f9fa619f6beb704a2f15525c65a47c971722dc3bc3f90ea5c841e3638ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.5 KB (389548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:943db3974e5f10bbc7966443777c05088de780be82f928a813e6586ecd325aa5`

```dockerfile
```

-	Layers:
	-	`sha256:45e23c39bc0be5da6f69166d95c9c909d472bd6fb09f28f16175c16ece0eddac`  
		Last Modified: Wed, 08 Jan 2025 18:13:38 GMT  
		Size: 380.1 KB (380133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e027b277b255be095d6abc40669022b643d1a2a4d1015db927d1e2370dc4f871`  
		Last Modified: Wed, 08 Jan 2025 18:13:38 GMT  
		Size: 9.4 KB (9415 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:bfd01184f1d495f1b6666e6fb739ba09a57a822737cd22f0c6e672b8e5427b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160277144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f26f2554ea5b2b49c606dd2996843d2e1151d7ffa4e5548872ed7102012c17`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:05:14 GMT
ADD alpine-minirootfs-3.18.11-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:05:14 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=21.0.6.7.1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=21.0.6.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 23 Jan 2025 01:09:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f6b431426dd566e612639f03cd46e521b3133a043bb6b60edeeeef80d513e870`  
		Last Modified: Wed, 08 Jan 2025 17:24:31 GMT  
		Size: 3.3 MB (3341861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16149fb98927747995aacea4de7cc623298ba445fe9c41ca25d72eaff889d58e`  
		Last Modified: Thu, 23 Jan 2025 18:53:04 GMT  
		Size: 156.9 MB (156935283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e0b2403cb739c8426b88d88e764e16634722f6d53d70887283f5e3c18e159de0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.1 KB (389067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8189d369244ba9427d28270ee993e4cca2e330d7041809427dd4e637b78a2fb2`

```dockerfile
```

-	Layers:
	-	`sha256:8d333ca0a91ab8635e5adae36be46448e983bfeced40219e7dcde0ae7fdaf933`  
		Last Modified: Thu, 23 Jan 2025 18:53:00 GMT  
		Size: 379.6 KB (379550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e76d190fe28bda82e2ce45df3b7dbe2fdce2e111b1bf9f7e5cc06e125e251740`  
		Last Modified: Thu, 23 Jan 2025 18:53:00 GMT  
		Size: 9.5 KB (9517 bytes)  
		MIME: application/vnd.in-toto+json
