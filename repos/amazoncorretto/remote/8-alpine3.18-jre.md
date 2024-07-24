## `amazoncorretto:8-alpine3.18-jre`

```console
$ docker pull amazoncorretto@sha256:9f59fe25d955343bfb647fca952f3b590b3a9f29155c289d3fe5128aaa2e4765
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.18-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0f0f199c9dd8f6bacc57870d343d9c6c0136304d75a90cce1e8e16208e58a87b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45015069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d0089093244d2ee8fd71b310b57e814c9749acd90f912dd3d095cf7b390df2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:5851aef23205a072ef361dd412a73a39a1ada75e19a207a392bb7ec9b8556e11 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:930bdd4d222e2e63c22bd9e88d29b3c5ddd3d8a9d8fb93cf8324f4e7b9577cfb`  
		Last Modified: Mon, 22 Jul 2024 22:27:34 GMT  
		Size: 3.4 MB (3415640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15e0a08f51f3863317437492601beb5a28033cbd34e892020cb0a82af369df6`  
		Last Modified: Mon, 22 Jul 2024 23:04:23 GMT  
		Size: 41.6 MB (41599429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.18-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:71746ea8e58982a0a428400b0f0d305b2e125c1ebe51ed1c1c98a1c772bb57e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.2 KB (193180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3785e4d029d984b1e8d4109dbde76225e2af4bf2ade936740535982453c60d9`

```dockerfile
```

-	Layers:
	-	`sha256:8456978bfdab809cb151778e114a7eab297cc314c33ced320d138f5951178e80`  
		Last Modified: Mon, 22 Jul 2024 23:04:22 GMT  
		Size: 184.7 KB (184726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:015b118db3485fd38c30514b9bbff06ce0d00c920d751210f718452cae7381fb`  
		Last Modified: Mon, 22 Jul 2024 23:04:22 GMT  
		Size: 8.5 KB (8454 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.18-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d149d906102a9cb0cc2e7cff5c1448779065ec05ecc75138480b94f5c21d4624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44645974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f16a6218b5d15cd0816e543880077a4cc6202ee9f015e7e7a9c6dee16e37e0f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:4a10978248445fe045fc2859ce867988ab71bd2281ad7d88b62597252642a56b in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:4983c3fe2029a430985943e6d87b35248366efd28cee655acc3ebff5daf703fa`  
		Last Modified: Mon, 22 Jul 2024 21:44:57 GMT  
		Size: 3.3 MB (3339494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3879fc1f7aaa8334f9a89f30e42d88048e377e5abd153683d682129aab974d2e`  
		Last Modified: Wed, 24 Jul 2024 10:38:10 GMT  
		Size: 41.3 MB (41306480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.18-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:27ebeed300303ef8f542a25b5cb3fd455589a7893f71cd6999955e4e457fc3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 KB (193563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e3ad2d78c6ed8ac73a88795758a7427383a4a660d9c05ebca1a149ba9813bd2`

```dockerfile
```

-	Layers:
	-	`sha256:a315dc740d6d088fc6a30460105b18b22bc481f74a5da85d1cae02a5c63aa46a`  
		Last Modified: Wed, 24 Jul 2024 10:38:09 GMT  
		Size: 184.8 KB (184834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbdea74ffe3639d13fdb8fb9f6c8158964509d59dc2a92b43abe93d880f7f99a`  
		Last Modified: Wed, 24 Jul 2024 10:38:09 GMT  
		Size: 8.7 KB (8729 bytes)  
		MIME: application/vnd.in-toto+json
