## `amazoncorretto:8u492-alpine3.21`

```console
$ docker pull amazoncorretto@sha256:8642333a3c24c7117848011c959a74714b019cff0b30d731acfc0512c944c725
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u492-alpine3.21` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a773147e7a327449c35490ba4ea94b5dc0cd8e2b9da18cad6c0b523d254cf5c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104397900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad631a8891f0b7686886bfa216c17e6e9bc77ee713707332ceac54e0b78da577`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 22:57:24 GMT
ARG version=8.492.09.2
# Fri, 08 May 2026 22:57:24 GMT
# ARGS: version=8.492.09.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 08 May 2026 22:57:24 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 22:57:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 08 May 2026 22:57:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7880e97bce3e349b698c7d17bdb3295e168e0292765bf1ac8c63c5cec91094`  
		Last Modified: Fri, 08 May 2026 22:57:37 GMT  
		Size: 100.8 MB (100751025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-alpine3.21` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fe7458ddc5c6a450ab6552346e67404766cebf0e8f5e2e10b567f894b65f4376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 KB (260288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb5dd3860100b6451527d814153e7ae2fd95dbd098bb5b5ad8f97f83eaf27bc8`

```dockerfile
```

-	Layers:
	-	`sha256:2b265707fb4520ce0da04f6e45d885b67844108c36667396b872fc3c99fd1e50`  
		Last Modified: Fri, 08 May 2026 22:57:35 GMT  
		Size: 250.9 KB (250933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fda383de4a7c0348386d26405f573773b27ac9f1183b8509b20ed2795021bdab`  
		Last Modified: Fri, 08 May 2026 22:57:35 GMT  
		Size: 9.4 KB (9355 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u492-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4c4750651bf20daf8c7eaa45a86ff93da594efb0541cce5773b0b249c2fbd86e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104538767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a60a106112f7c54c07f8ca5a61f18e35b34ad8f2ebc02346797928489bf594`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:13 GMT
ADD alpine-minirootfs-3.21.7-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:13 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 22:48:23 GMT
ARG version=8.492.09.2
# Fri, 08 May 2026 22:48:23 GMT
# ARGS: version=8.492.09.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 08 May 2026 22:48:23 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 22:48:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 08 May 2026 22:48:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:2dd7199cff98a7400e801cbfad6de906972a4e3dd0a749d4c1b80f5a1e3e4108`  
		Last Modified: Thu, 16 Apr 2026 05:32:50 GMT  
		Size: 4.0 MB (3994465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987a2b3117eb079a7019a2b0705f094365b2c4d456bea4353fce13102c9b09b3`  
		Last Modified: Fri, 08 May 2026 22:48:38 GMT  
		Size: 100.5 MB (100544302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-alpine3.21` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fba1ef92f4767c98ff0dce64d07699d3eb5593dc9d1d4c7d36d9a27af9bee89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.5 KB (260524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e9d0af0cef6f8356a81bdf22c97754572a3dde59f415107348e84218c61352`

```dockerfile
```

-	Layers:
	-	`sha256:3c2cd574cec526a403e87393cdbbaed2c243e6609675b7d09fb1a5309d87996a`  
		Last Modified: Fri, 08 May 2026 22:48:35 GMT  
		Size: 251.1 KB (251065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23c1167ac2284f33ad63d0223c52b519e7cc688f4b658ea37eccee55d5fc6a39`  
		Last Modified: Fri, 08 May 2026 22:48:35 GMT  
		Size: 9.5 KB (9459 bytes)  
		MIME: application/vnd.in-toto+json
