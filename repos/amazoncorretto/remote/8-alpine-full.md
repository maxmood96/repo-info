## `amazoncorretto:8-alpine-full`

```console
$ docker pull amazoncorretto@sha256:e4e9f603133fe29849d6ff7ad30345fa09b8934d0015040026c8c716d715eb3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e57fb787af51e9c1bb2f3eba07672d58bd4df98efaf6343dceead3d64999bbbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.8 MB (103821398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9e6c32e6272d4a8111438beb1359f365c0d973838e7befeb6bb7e1058bc430`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=8.432.06.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a15a91bb85d85949856ba1d3ccade006b10de18ccdc8675614554939053055`  
		Last Modified: Wed, 08 Jan 2025 18:09:49 GMT  
		Size: 100.2 MB (100195138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2c3c5bcc5dc0b0902525f46744dafd0514c313857699fd1f4a186a35a8e0c499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 KB (253396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afb0a4fa8b6b6d54bdf84d0fc17b071453750044dc0d4e32e49c03fb537e2051`

```dockerfile
```

-	Layers:
	-	`sha256:f155b48d7d890d1d748e8452ba823b19c45015ad6f536568e904eedca58ce274`  
		Last Modified: Wed, 08 Jan 2025 18:09:48 GMT  
		Size: 242.7 KB (242700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b202bdf0f589e05101c8b41bda428265fa09b14a592c0fe47cf79cbb13d70907`  
		Last Modified: Wed, 15 Jan 2025 08:32:32 GMT  
		Size: 10.7 KB (10696 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ea8a7c7be2a469d7b8b095885010a4c506f4dda4f79bc5913d93c2d89f58b1e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104069504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:167f85a6613ed7e758334cc8655336b2ffbb4fc58e085aaf9bf70f4be529076a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=8.432.06.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:d676acef0262114b575dbe155e1594d5a6f3b4a62c043566b36b1d8e6a050b5c`  
		Last Modified: Wed, 15 Jan 2025 00:04:46 GMT  
		Size: 100.0 MB (99978735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b20298f5e2709bfdd7792e0e6baf86e33b0732251be2404dde5e4c13dd97163d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 KB (253727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74c7260d27c485a5b218c39023adfb2d11d53d4fa5210de6d1bd8e2c796fa76d`

```dockerfile
```

-	Layers:
	-	`sha256:f1bdba6ca64e7196c25a5d3a42c613a6e37ff28097cfb5926762b3a5f79e1d87`  
		Last Modified: Wed, 15 Jan 2025 08:32:33 GMT  
		Size: 242.9 KB (242880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d974a1a34688bd31585fa55a3aeb9f98e360a9febd91d787751c8ddd1df0d661`  
		Last Modified: Wed, 08 Jan 2025 22:17:24 GMT  
		Size: 10.8 KB (10847 bytes)  
		MIME: application/vnd.in-toto+json
