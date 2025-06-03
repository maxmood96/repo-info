## `amazoncorretto:8-alpine3.20-jre`

```console
$ docker pull amazoncorretto@sha256:efb9e47f58c27eec5060bc2cbd31351ab9b142dbd968ba72161dfa39d0cf30ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.20-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:efa7ead2992ddb88afe1fa16669a33c7e0c85191cc861a98f55615a59eeedd9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45288524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba2a0e3bf8aa17fab674def0646c90b2a6f48591146ff469d4bbda35d1fffb8b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=8.452.09.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=8.452.09.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882b04dae120132fdf7b03175da6c1441b67a84dbad132956bf9b31692935f36`  
		Last Modified: Thu, 08 May 2025 17:17:34 GMT  
		Size: 41.7 MB (41661627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1ee3d1145219d7de7039b145e774c6372bbc16d8fcca7110a42d0c0a499cec12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.8 KB (189800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ddc79f3aa910136280ae446c7cd673c4f33f6c5299ecda8d30af1d00f87836`

```dockerfile
```

-	Layers:
	-	`sha256:3f6a5303fc267b52b63bdf367e83d6c6b485a352f7411d130a454868fea484c8`  
		Last Modified: Tue, 03 Jun 2025 19:45:16 GMT  
		Size: 181.1 KB (181101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f188745c4b6a83cd122b56342c19243b72706f26202416e161bc84d91971abe3`  
		Last Modified: Tue, 03 Jun 2025 19:45:17 GMT  
		Size: 8.7 KB (8699 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.20-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b0f36a8802a1a1bd2fa62c51f40186aba7868553fafb37bc7eeac468f4dc7e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45456786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2479786e14912e2b252469302fe47568698b5b377ff3fe5cc3a67d4c74783c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=8.452.09.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=8.452.09.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3efa5f59a1a57b1c44db54c7bad55d2767d414a863c64871d64586023db79100`  
		Last Modified: Thu, 08 May 2025 17:18:05 GMT  
		Size: 41.4 MB (41365621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9975b8e35daeb09fa9c491f124374a264316a80243f38ec954c02a1dfcb3a42a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 KB (189988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c97678ed7b931ab9f645c266d3804b0db072a139a2eaa69d91c09c4f9f6ee4ee`

```dockerfile
```

-	Layers:
	-	`sha256:02ad389e45a3da28ff5a641ee0d0fcd02e71ecd5cea32da8457eff8fcffc4fd6`  
		Last Modified: Tue, 15 Apr 2025 23:59:41 GMT  
		Size: 181.2 KB (181209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c471cdd0ed9942abcce5eaecc989e99c4df6c28427a00ff2cc1eedb2a858ec1`  
		Last Modified: Tue, 15 Apr 2025 23:59:41 GMT  
		Size: 8.8 KB (8779 bytes)  
		MIME: application/vnd.in-toto+json
