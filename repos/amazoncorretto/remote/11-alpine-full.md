## `amazoncorretto:11-alpine-full`

```console
$ docker pull amazoncorretto@sha256:e964fa3536e3253a8cb6c3b9ba28e891acad3a46682fcfa566e2ae06c1e02d41
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5f33bca4c0be4e8502f28f69aaa04c17871bb3ed9e0a9fc131171204063a0163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.3 MB (147322012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cdaeff01d65785150285812e061368253bf448bebba25389a2c0fed375394ac`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=11.0.29.7.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=11.0.29.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94eb835f12b8d685474782e26aa1a629a8487ee3c358a3349d709d8a9c303bd5`  
		Last Modified: Tue, 21 Oct 2025 23:26:56 GMT  
		Size: 143.5 MB (143519560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:be501a97a8f73fc94ad1098cfff3eb035c95a6f07f03f9f4ca18fb5174b7c4de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.0 KB (600961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6eb29a8d4c07fa0efd382b7732eba2b17764d266dd8ecfc1f3b2c9d6eb91fb`

```dockerfile
```

-	Layers:
	-	`sha256:220b562e917465365702d3cb7cc90b152b0f057daec8fe63307864066ee30716`  
		Last Modified: Tue, 21 Oct 2025 23:26:53 GMT  
		Size: 590.2 KB (590236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aebebd8eb00a65b76e3b20501a245cf9c381ce3892368945f52e5ca926c0834e`  
		Last Modified: Mon, 22 Dec 2025 09:26:24 GMT  
		Size: 10.7 KB (10725 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:067927b7739991124d6be685f5ccbbdbdca57193e5eb48f968d00f2024fad2d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.9 MB (145924931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1b15750e3978e25963cd6949ad9fb6b98cf8cae4cc69cb8c3b69a423ce0e164`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=11.0.29.7.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=11.0.29.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019f117255af6f7914c8f78afb38eb2889f1e9e16fbdbf37cb83ebf7cbaa4a83`  
		Last Modified: Sun, 21 Dec 2025 00:10:39 GMT  
		Size: 141.8 MB (141786862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1ced7283f4d082aa5841abfa472b5f36de0be7e9d837d930617f48b3c2f2a27a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.2 KB (601217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a3cd5d8eb31b87454493eb146568c032a61bdcce1978217c02b36bda8acad7`

```dockerfile
```

-	Layers:
	-	`sha256:a905edf09ad6a99b1fec9489c6b089b4624bef7f04e6d85c903e7bb7a987973b`  
		Last Modified: Mon, 22 Dec 2025 09:26:25 GMT  
		Size: 590.3 KB (590340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:189dd2710065cac4a7758f9ff5db7b6b8d00b326368116a764ec239f9faf89f4`  
		Last Modified: Mon, 22 Dec 2025 09:26:24 GMT  
		Size: 10.9 KB (10877 bytes)  
		MIME: application/vnd.in-toto+json
