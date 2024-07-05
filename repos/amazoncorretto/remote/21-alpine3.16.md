## `amazoncorretto:21-alpine3.16`

```console
$ docker pull amazoncorretto@sha256:27d1927f8df1353f91913bcd474f5bcd371cce906103292fbacef9929aa4ae94
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.16` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:953fc37cc6f856d79bbcb17dbabf27e55a45e5f3d7e3efefc8701535772c1efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162682114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c63026f9e12107c9058c2f60a02b83546c2932d90b6eead62f3329ef9f490b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=21.0.3.9.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=21.0.3.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Apr 2024 21:21:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403b22376bc7613f3279be8174122f126e53f4f96b08ab240a48a6cf2d21e66f`  
		Last Modified: Fri, 05 Jul 2024 19:56:25 GMT  
		Size: 159.9 MB (159874277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.16` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1475563c60bc4f005c235588489190aaf1a175bdb838d769a41e23e87d1f2815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.1 KB (383111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d5a386d7b3d86ebd29bc452d6628baa7122e5fc5fda4de28baec97d8959a2dc`

```dockerfile
```

-	Layers:
	-	`sha256:58ce30635ded54b8623675e0be233e0a3a79ab17cb0b38e1fcec8d0f6d823ca7`  
		Last Modified: Fri, 05 Jul 2024 19:56:23 GMT  
		Size: 373.9 KB (373942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28b36d462408e190f726ed88f4596ac05065aff62dc90afc9ea0086821a9f8b3`  
		Last Modified: Fri, 05 Jul 2024 19:56:23 GMT  
		Size: 9.2 KB (9169 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7e5e806c6526c7e771add8c73d2491acc99a1b5fa71a5654bbface242fd65d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.1 MB (160094293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecae24c5adbce090d018082dbcd6f85ccc8d2df4835afed428e18f7dac89554f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:05 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Fri, 26 Jan 2024 23:45:05 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=21.0.3.9.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=21.0.3.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Apr 2024 21:21:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2605612170bad692ba27150edede3ce7d7041fc00c4397de3c60760f2eaca7f5`  
		Last Modified: Fri, 05 Jul 2024 20:24:09 GMT  
		Size: 157.4 MB (157386010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.16` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f6ee56e51170f2d3ad2cead644e21b06812c8c2fbdcd5fefb1e131f4635814e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.8 KB (382829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e18a5d4f21f75bfcabae024293a555a4f95ff09b61df9541f6d539095669faf`

```dockerfile
```

-	Layers:
	-	`sha256:d8fb339ed610215396a85b6e4a45709c654ec6f84887fe5be2ad53a6d92943a9`  
		Last Modified: Fri, 05 Jul 2024 20:24:05 GMT  
		Size: 373.4 KB (373360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a42911aacbd24ee32ef70fcdf33f1bc53a32424b43588c79e55c0b8e06aacc5b`  
		Last Modified: Fri, 05 Jul 2024 20:24:05 GMT  
		Size: 9.5 KB (9469 bytes)  
		MIME: application/vnd.in-toto+json
