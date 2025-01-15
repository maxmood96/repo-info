## `amazoncorretto:23-alpine-full`

```console
$ docker pull amazoncorretto@sha256:b5be93be529619dee0a61ce9d035788df3fbaa292693ac984d59f386dbed2022
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:84fdbe7eb505a7ad93b01e20509e070269fc7eb7757de192864df8853d80ca00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170284749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a9d3ea548bf8baa7dc8eacdee8cfdefd9ce58915ef86bf6dd16a14cb234fd7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
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
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2cd4181bb52ce426961102605623259f0d7c099af5e22cda54baa3468ebc3b6`  
		Last Modified: Wed, 08 Jan 2025 18:13:54 GMT  
		Size: 166.7 MB (166658489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3b0343e1fdf033341edf6b2f1fd06076d86c35b4f21b4399f77a6167a118b86e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.5 KB (390533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d36c34ee97067ff5b0d5d58d7c9236c064bcdb8ee1a4316e148983ce4222a3`

```dockerfile
```

-	Layers:
	-	`sha256:e7da44284f469a05ead514762cf7df886799fd8948442e859ac7234247e75e9a`  
		Last Modified: Wed, 08 Jan 2025 18:13:51 GMT  
		Size: 379.8 KB (379813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09293484245eea35eab8b3af8db1d34387dbf9a45e7c8f7e2510d25fe098e7da`  
		Last Modified: Wed, 08 Jan 2025 18:13:51 GMT  
		Size: 10.7 KB (10720 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-alpine-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:2e65482025d66b5005fc482c2f30eb1d9d626ff33683de4116c3b3ce8cbdad83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168442580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47861a120c59dfc6537ac4ee42602daf4be3441046c71da2e1e11bf2fa78f1f2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
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
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcca95e87f3664c035c01f7073ae906d0c2c8db88f18d6144eb6b18cd6a4bf4`  
		Last Modified: Tue, 14 Jan 2025 20:38:46 GMT  
		Size: 164.4 MB (164351811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:94b646f6fd6af82ed18c104fbc2cae0c3fc9b1bf794b1da88b78dfd96c5c1b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.5 KB (389512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9f8570852ccf9a7914d6a179e60ae254f8090c1ebfb97ba2780342318704af1`

```dockerfile
```

-	Layers:
	-	`sha256:d441ecb9826095f93f99730d66c2ddd98e6583c198fdf57c2a5b776a65186ea6`  
		Last Modified: Wed, 08 Jan 2025 22:22:25 GMT  
		Size: 378.6 KB (378640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4807040620c53341dad5c413b687ea8cfdbedfce4b39da5a3b1f1418baafa92`  
		Last Modified: Wed, 08 Jan 2025 22:22:25 GMT  
		Size: 10.9 KB (10872 bytes)  
		MIME: application/vnd.in-toto+json
