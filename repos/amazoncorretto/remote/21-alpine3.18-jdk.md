## `amazoncorretto:21-alpine3.18-jdk`

```console
$ docker pull amazoncorretto@sha256:0ca9008c3ff4483084180006427f499fe7645ab2ea78bd3e06c18ad1cb786095
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.18-jdk` - linux; amd64

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

### `amazoncorretto:21-alpine3.18-jdk` - unknown; unknown

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

### `amazoncorretto:21-alpine3.18-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f7ab96d610fcc7fc8b314f08c4276a1bf36e265fcf25096561fd253554bbd4ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160216323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e056b0c62ddac2246511e20c6c2418f89c94ec42a028e884a069e6f1397feaa1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.18.10-aarch64.tar.gz / # buildkit
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
	-	`sha256:fb3f1f9d2d6533828602bbf29a9a8cc07ae4a2a3e88846100e68ce43a16d2932`  
		Last Modified: Tue, 07 Jan 2025 03:03:28 GMT  
		Size: 3.3 MB (3337435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a6b223bf05ae80c03812ebf00d018c211db6c03f593f27319fea53abf60563`  
		Last Modified: Tue, 07 Jan 2025 15:43:47 GMT  
		Size: 156.9 MB (156878888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.18-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:055833327c82655e465370a690609e653113037096cc8e0bf4d49226784121a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.1 KB (389071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150179515f417d548461b44a3030ffb6a31c0796dfc4c6ffad78cdbafcaa5ed2`

```dockerfile
```

-	Layers:
	-	`sha256:13e5d36bf51ec0aa3c069f6b6801e6624261ff43e797dd15b4f4d24bfb15cfb0`  
		Last Modified: Tue, 07 Jan 2025 15:43:42 GMT  
		Size: 379.6 KB (379552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da661b245bcb810e294b8ce2972fee4909f9b2693a4e8dcf7ebd0768d332ad7c`  
		Last Modified: Tue, 07 Jan 2025 15:43:42 GMT  
		Size: 9.5 KB (9519 bytes)  
		MIME: application/vnd.in-toto+json
