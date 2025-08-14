## `amazoncorretto:21-alpine3.20`

```console
$ docker pull amazoncorretto@sha256:ad7f284ec19a083199401013cd122cf005f824df86d63fe8b54bff71dbe676d0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.20` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4c098cd005cab58a9327bb83f180a1b15abcefdc8bed8b0df10b64e8550ee571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (163002294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75eebc956e02f425b58ba6dc5c2e318db84c82f479a82e9dd7e917aad1c5d1b6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 19:33:24 GMT
ARG version=21.0.8.9.1
# Wed, 16 Jul 2025 19:33:24 GMT
# ARGS: version=21.0.8.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:6617cdef4ba672b1291127d22f2b5f3bd481697673485448cefc14f8e0eff70f`  
		Last Modified: Wed, 16 Jul 2025 22:06:22 GMT  
		Size: 159.4 MB (159381817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a97e5e69da3fcc872982733696e03b93bb623f7416ba4582b6b33fc96bbad03d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.4 KB (387389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af12b56e0b13597de6fbd5b0ccaa6127fd45f6c918c7e31290f3bafc9b513880`

```dockerfile
```

-	Layers:
	-	`sha256:da1cc7b203411c8a5d91a17f0fc0b04ef48303e0173c9802572bc293c59261ed`  
		Last Modified: Wed, 16 Jul 2025 21:49:55 GMT  
		Size: 378.0 KB (377976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31f4d197f896edf2dfb9447623dc70ada6e65cfe6470784f9d3daea77a610eb6`  
		Last Modified: Wed, 16 Jul 2025 21:49:56 GMT  
		Size: 9.4 KB (9413 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:2bf040a46440eb0ce2d3e1be01f75e0dffcee9c25ee159758ee59ceb0730085e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.4 MB (161430236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9382282144c63a46c2ddd69da71c47187e4b864b96171e6fedba8188077d00`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 19:33:24 GMT
ARG version=21.0.8.9.1
# Wed, 16 Jul 2025 19:33:24 GMT
# ARGS: version=21.0.8.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:f474e04a3efa50bcd8d373921b1e760dc212b4c409dbf60f152e8f0ac17e07fc`  
		Last Modified: Thu, 17 Jul 2025 04:37:06 GMT  
		Size: 157.3 MB (157341868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:efab8cbb73c299d7774a5894660f43554034adf51f14539b1c229f40c1c3412c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.9 KB (386913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64632a5419b32d0089af94bfc854de8f31bad195d52053d319441f50bf8a8dd8`

```dockerfile
```

-	Layers:
	-	`sha256:042d4651dfe751fd3d711e09e130e29a8c29faa2722f519baf6ec4e9be426e88`  
		Last Modified: Thu, 17 Jul 2025 03:49:50 GMT  
		Size: 377.4 KB (377395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:680fbce40337e84d3a357959999dda64fd800e411d383524f7489ea3c0d0674b`  
		Last Modified: Thu, 17 Jul 2025 03:49:50 GMT  
		Size: 9.5 KB (9518 bytes)  
		MIME: application/vnd.in-toto+json
