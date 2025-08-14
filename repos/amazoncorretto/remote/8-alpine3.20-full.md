## `amazoncorretto:8-alpine3.20-full`

```console
$ docker pull amazoncorretto@sha256:a3809fecf9f73d1e582c4c08ff310f02f5e30f264891c82f8b1f8999e8d3c98e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.20-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d499925893537d27c92f568a6f70023d37979667d0a6742619aaee05005f1040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103917033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:317d4e133feb3f72fede61a29025757410d9f0a9ef478bcefc5bfed75dfde642`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 19:33:24 GMT
ARG version=8.462.08.1
# Wed, 16 Jul 2025 19:33:24 GMT
# ARGS: version=8.462.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Jul 2025 19:33:24 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 19:33:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Jul 2025 19:33:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0704a4f2982f92db8ed11e88f91ff6c800678bb1a4f00e2de18c12bc68f994`  
		Last Modified: Wed, 16 Jul 2025 20:25:01 GMT  
		Size: 100.3 MB (100296556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:45230372de6dc1b0851155561048a6b0a64d9502454a7809c14c975b4c0db180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.4 KB (252393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f4f82eaad26828c969c2148ac153490d06c805de36c4774fa2a71716b3b467`

```dockerfile
```

-	Layers:
	-	`sha256:9d5593c7a224cd74ec5fcebfa7d37bb199f9b52abea2d3de893f7665c2743bb2`  
		Last Modified: Wed, 16 Jul 2025 21:51:41 GMT  
		Size: 243.0 KB (242995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f519b6495feeb3d9912b532a11f752e251e054b6c3a29a0c4f53045b244b12e2`  
		Last Modified: Wed, 16 Jul 2025 21:51:42 GMT  
		Size: 9.4 KB (9398 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.20-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3f61ecdc7844c1475e607fcbf192a8ac9cf2039acc618835e3a4c2f69d04ccd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104177982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51c0de3632d76407daba122a8778405571cd8237e94420bffcf5c4d990021e97`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 19:33:24 GMT
ARG version=8.462.08.1
# Wed, 16 Jul 2025 19:33:24 GMT
# ARGS: version=8.462.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Jul 2025 19:33:24 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 19:33:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Jul 2025 19:33:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:13e713f825654e9e4f57146ec84918d478434f708d4d3d9d18d0e7ba2be56801`  
		Last Modified: Tue, 15 Jul 2025 19:00:10 GMT  
		Size: 4.1 MB (4088368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a97209fe4e031b8b02a736a11b8e2822a16d3029743669ecaa9e2b2e9801c91d`  
		Last Modified: Thu, 17 Jul 2025 01:47:33 GMT  
		Size: 100.1 MB (100089614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:827f4327b3daf3c478d8fafa7b22aeeeae705dc3f02bd1d6227a16d100e02207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.6 KB (252629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77fd24c8b19dc57522cf77cebf30bef38994c09ddd9c8b4da8fc10d37d7bde4`

```dockerfile
```

-	Layers:
	-	`sha256:eb031cf3793fbaf77dcc65a64432a44bfdbaae9eba59f590087279560a1b78dd`  
		Last Modified: Thu, 17 Jul 2025 03:51:31 GMT  
		Size: 243.1 KB (243127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:380060103d6dac056817200d0d9a0c59d89c819d6e808edea7d13fce5f0a18ea`  
		Last Modified: Thu, 17 Jul 2025 03:51:32 GMT  
		Size: 9.5 KB (9502 bytes)  
		MIME: application/vnd.in-toto+json
