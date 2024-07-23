## `amazoncorretto:11-alpine3.19`

```console
$ docker pull amazoncorretto@sha256:7a97c9f5d8db4384bda227da0eb2c33b22216eee16c1015161ae00cc32276fdb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.19` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:08bf91b7df471cea14d7d09963b216758cca9bde9fdb8130229ea520756d76e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.2 MB (145229947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c08895a49c9e53c084cad37fd0c56f8dff7383e2cb0369e902fde210a98e290`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
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
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4890a54334c429cb5445dfca2599b331eaeb0208998fee9605bfcdf0eff2cb98`  
		Last Modified: Mon, 22 Jul 2024 23:04:38 GMT  
		Size: 141.8 MB (141810907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b987429f9fa9d474910cd73d271efcab49af6273b18dc627cbc37088b769b6e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.4 KB (397396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73a747578960080136b801c0cfa437c03bf7124c6008ba00ddb33e28921dea8`

```dockerfile
```

-	Layers:
	-	`sha256:647c3dcc43b3877c4b62c15611d9c566008da08594e815e6b017381371733c60`  
		Last Modified: Mon, 22 Jul 2024 23:04:35 GMT  
		Size: 388.2 KB (388224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b914dd1372be3715cd0b8a4dd0dcef536bebfc8ffd94d34cec09344353f77b9`  
		Last Modified: Mon, 22 Jul 2024 23:04:35 GMT  
		Size: 9.2 KB (9172 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:836df20a3d4e0c21379ba768d307aae54437dc8972fb94d569f0a448e573944e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143316042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:522ab9fda7f97cb9b06a5124a5328ee1897c99552a7d0c54682600a105ba29a8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
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
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcca778f984f2205a165ed9e8e5933b21a4917e7454e01f38acbaf40035817a6`  
		Last Modified: Thu, 18 Jul 2024 01:09:06 GMT  
		Size: 140.0 MB (139958840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:785a38fdb0890db52766ae01e662351417f6d5fb2ac1e7502ca31e2dc8d35890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.8 KB (397752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c99188f3e4ea42a92501fbc59dd9c102f53a83f40ea2a769807cef4346ef3a1c`

```dockerfile
```

-	Layers:
	-	`sha256:2a41a49e2dd0cdeb0affe68f7cfe97c3f0479bcf25783718319803f82f647f74`  
		Last Modified: Thu, 18 Jul 2024 01:09:02 GMT  
		Size: 388.3 KB (388280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e5bf4c3b697a6a2ce381ea2e79691522c7c088899770d7190c440fb2df3827b`  
		Last Modified: Thu, 18 Jul 2024 01:09:02 GMT  
		Size: 9.5 KB (9472 bytes)  
		MIME: application/vnd.in-toto+json
