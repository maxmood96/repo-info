## `amazoncorretto:23-alpine3.20-full`

```console
$ docker pull amazoncorretto@sha256:a815d3a8fd609c32da83e8d2f60a92d5782eb4da7817ddf67c8695fae20cc83d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-alpine3.20-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a438ff308b5a8927400c2500456061e1a07fe47270d7880853089163298885b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170314208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f4fadc327e6dec7abbadd5bd19180092a7da4ea45d6be5c4c597713fa2ff4dc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=23.0.2.7.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=23.0.2.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ec8f4dd8de24537b687316308c1818251765c8e8ae2abeb35ae913501ac134`  
		Last Modified: Fri, 14 Feb 2025 23:39:42 GMT  
		Size: 166.7 MB (166687311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:15e75d641478804fa22dc32f8ecf99bff8c4cddf7440968e5db8e14e2a871d1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.9 KB (387921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de28860a8e0efbf7cd1f4185b92f2404a98731ebc47279120c8b0d7853d19925`

```dockerfile
```

-	Layers:
	-	`sha256:c1f983838e7c7fdcc853380c4042fb6b2a5669265c32cb220a7c914b874f752b`  
		Last Modified: Fri, 14 Feb 2025 22:49:22 GMT  
		Size: 378.5 KB (378507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0869a5b1778e3986101552a88ff9e9440f083c0205999bf95c25639472fcd0bb`  
		Last Modified: Fri, 14 Feb 2025 22:49:22 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-alpine3.20-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f7cecdbe7afd06a602939ce5f752c98d410b5275af01a63e995da45a3ed7fc58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168499098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad217f369e068d1d1b0cb1624b4e88727cae6ee84a0d55d736121d4fb1985bde`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
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
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8a1b77d8fb2973a5165487ae4f9ba602b01b62aa495d03847f6a44857d4e29`  
		Last Modified: Wed, 05 Feb 2025 21:10:56 GMT  
		Size: 164.4 MB (164408329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9f497379153d4b2d17d23733d71efab3acc457311085a6f5f703d16cbded59a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.5 KB (389512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d504997fc7f392da24efb1858731e42546dc2a3edb27b77ef0dc353b7095e4`

```dockerfile
```

-	Layers:
	-	`sha256:83bd24864454e5d987103d23111264bddb1153b7426aa74e461152eaa6db612a`  
		Last Modified: Fri, 14 Feb 2025 22:49:23 GMT  
		Size: 378.6 KB (378640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0629dc887c1bf7f9da378b1f7ef9d1e15a4d010d304cd6ae1cba8adee5707e41`  
		Last Modified: Fri, 14 Feb 2025 22:49:24 GMT  
		Size: 10.9 KB (10872 bytes)  
		MIME: application/vnd.in-toto+json
