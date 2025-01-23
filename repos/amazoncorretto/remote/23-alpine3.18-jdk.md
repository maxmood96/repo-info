## `amazoncorretto:23-alpine3.18-jdk`

```console
$ docker pull amazoncorretto@sha256:29415cfe7dceef4b9d2bcf82eff756e433fad7c0b463b5453df5095cd68962d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-alpine3.18-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6a4b95efadb78f4f8147981be54af7d4208c584ccc20347630b0aea6cee78a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170076541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0e2854087c78edc067d53740401feb7f130a94aceaa2b43ba37c975f9dde0c0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.18.11-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=23.0.1.8.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=23.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:2c2422ed9175222718605f3aefdd9ce6490003e6786ccbf4d5e38befddedf56c`  
		Last Modified: Wed, 08 Jan 2025 18:13:42 GMT  
		Size: 166.7 MB (166658567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.18-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d88b4a1f883fb8e5c464736b99f73c48d2c0b3c5fddb5d0cbb1708dc46a44710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.5 KB (391491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d72a066588ae458784488716c166a9706fd45f42b2829b685088c5f231dd5a4`

```dockerfile
```

-	Layers:
	-	`sha256:f51702e161ad31500add866a0f8f3d7db05397341e17a836d373678971c9e443`  
		Last Modified: Wed, 08 Jan 2025 18:13:40 GMT  
		Size: 382.1 KB (382078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12873c77dd9138b6e6c38831a1490cf550a23b8e50ba9f867a49d0035070b291`  
		Last Modified: Wed, 08 Jan 2025 18:13:40 GMT  
		Size: 9.4 KB (9413 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-alpine3.18-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:88838d570ca5935d68cc0a3612595a0a3d60162ef02b30e83eb401e754df812f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167750697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d3dbe9637def7f24bfca9e2eb723563090024ff885be40fb4b5b8f63e22feb5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:05:14 GMT
ADD alpine-minirootfs-3.18.11-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:05:14 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=23.0.2.7.1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=23.0.2.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:1f667f42a5367d609333da21f1ce59f892b560125d6b7b1a7adcd3b0c4e1165e`  
		Last Modified: Thu, 23 Jan 2025 18:57:00 GMT  
		Size: 164.4 MB (164408836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.18-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:38810bde38843647f90d9ae78b3e94e5ba9bedceeeab8f774429abe06bdd9373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.4 KB (390375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d2b2019d9d05f0d58eaedcb05cc3f284a11b47771a1d36ebdd05e88fd36a186`

```dockerfile
```

-	Layers:
	-	`sha256:eada28e2e9c91007467c479351e047f5df4a9bf5aa256d0bf3488960d9179584`  
		Last Modified: Thu, 23 Jan 2025 18:56:56 GMT  
		Size: 380.9 KB (380857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa5ffaa3ade52568a84b6f2e1a5e4689f77eaf5bddc5b2dcd019e62a49b4de17`  
		Last Modified: Thu, 23 Jan 2025 18:56:56 GMT  
		Size: 9.5 KB (9518 bytes)  
		MIME: application/vnd.in-toto+json
