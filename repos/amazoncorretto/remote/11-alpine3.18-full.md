## `amazoncorretto:11-alpine3.18-full`

```console
$ docker pull amazoncorretto@sha256:2a52157c28d9ab3a47e07543e21053ba2552bbf53aa171667d9af2471a926d68
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.18-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:76ef4e07dec749f012178079ea8bef43a462722f27e106021ead6812b634cb92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.2 MB (145226480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8333dc7701c079b9bda3e6cb80f747cac7ed6d636034d651e84f3b1ea75bc48`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:5851aef23205a072ef361dd412a73a39a1ada75e19a207a392bb7ec9b8556e11 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:930bdd4d222e2e63c22bd9e88d29b3c5ddd3d8a9d8fb93cf8324f4e7b9577cfb`  
		Last Modified: Mon, 22 Jul 2024 22:27:34 GMT  
		Size: 3.4 MB (3415640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8073783742b7cc9cfa995b021731c8a42394b5c40758699841c6e74cfac10d4c`  
		Last Modified: Mon, 22 Jul 2024 23:04:45 GMT  
		Size: 141.8 MB (141810840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.18-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:40ab46929723659997048386349360751b7f29daa455477d0279fb08470904de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.7 KB (396736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b92a4cd8ea45c6777a04ce03ff8cb8666baca4f3ad4c3f5b211d799a07feaf48`

```dockerfile
```

-	Layers:
	-	`sha256:4bfbaca200a6f247bfbea001a0092cf3e6b1acc8cfb0e3a36f1f4a8ef5544092`  
		Last Modified: Mon, 22 Jul 2024 23:04:42 GMT  
		Size: 387.6 KB (387564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a5cc3236f42eddb59a11dc744c66ee72424bebf6fd5cf2a8077ae2c98a005d1`  
		Last Modified: Mon, 22 Jul 2024 23:04:41 GMT  
		Size: 9.2 KB (9172 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.18-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5f231f4a90cdbe102e9bbb73af29172e53b394d8e3eb0f7d907b98f68421d131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143298197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:573a34fce16cdc241f905bfa9b6ee5c690999de04e41cf53dfd855402dc62516`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:4a10978248445fe045fc2859ce867988ab71bd2281ad7d88b62597252642a56b in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:4983c3fe2029a430985943e6d87b35248366efd28cee655acc3ebff5daf703fa`  
		Last Modified: Mon, 22 Jul 2024 21:44:57 GMT  
		Size: 3.3 MB (3339494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf8d832fc9d2540cbd2c6c5a54767b6e68751ebbeb496568ce2c6873e3074e4`  
		Last Modified: Wed, 24 Jul 2024 10:40:40 GMT  
		Size: 140.0 MB (139958703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.18-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2477c100b0e24fbf81ffbf8f5f1f78a1c2c477b816f610de4ad79e418c438405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.1 KB (397092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46a9512affd0e23ebff3031af6f09281660203a48d07bb17e5f0f9767f6004a`

```dockerfile
```

-	Layers:
	-	`sha256:88be6db0f176119ccc4643cfd014939f4753a52c1a359ccd9c4568b977913e86`  
		Last Modified: Wed, 24 Jul 2024 10:40:37 GMT  
		Size: 387.6 KB (387620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:681e1230e4182d98e21ae6cc70cff48792024f5dd5a09cbd783561e9ed673a5f`  
		Last Modified: Wed, 24 Jul 2024 10:40:36 GMT  
		Size: 9.5 KB (9472 bytes)  
		MIME: application/vnd.in-toto+json
