## `amazoncorretto:21-alpine`

```console
$ docker pull amazoncorretto@sha256:1564c5e6da5c2078edd89caca77ac728692552ab8aea4d026833560b96f85879
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bf3fafd81c33838a2d02f546363094a0c37cb36f74fc28f2dfeff344374812d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.7 MB (165703931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78cbc62e52d754999eeb1dc567d97302afa013231e87f0e3343e38f65291f62`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:31 GMT
ADD alpine-minirootfs-3.24.0-x86_64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:31 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:16:00 GMT
ARG version=21.0.11.10.1
# Wed, 10 Jun 2026 20:16:00 GMT
# ARGS: version=21.0.11.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 10 Jun 2026 20:16:00 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jun 2026 20:16:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 10 Jun 2026 20:16:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:9b70e313681f44d32991ec943f89228bc91d7431d4a84feafc269a76e3f96a63`  
		Last Modified: Tue, 09 Jun 2026 20:11:36 GMT  
		Size: 3.9 MB (3866755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdc9a6faa2a5c3ad02ee7fbee1ee4905d83e7a8c14a80b040c24ed551a179ea`  
		Last Modified: Wed, 10 Jun 2026 20:16:19 GMT  
		Size: 161.8 MB (161837176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:43123a566ec8c773bedf4f9bc06cb5598e167c6c53dcd6b0ac8853dea273938c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.5 KB (594471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff11464ab7829010d5797934f3d1e5d670de9ae33e1929bc8a138519016ad7b`

```dockerfile
```

-	Layers:
	-	`sha256:8523012523c4c4583a04770241ab11017db8a15dd69b32423704e2d3a8d22e3a`  
		Last Modified: Wed, 10 Jun 2026 20:16:14 GMT  
		Size: 583.8 KB (583785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f50034d5068171d3c3faa2bfc1288b35c144912e9e78d7f93cc1c3c54aa3a83c`  
		Last Modified: Wed, 10 Jun 2026 20:16:14 GMT  
		Size: 10.7 KB (10686 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1798753263def7a05ca480ad599c373696c9c6d1959924b0082ac74e0a0db565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (164044038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:798bdabb386a489e36ba2fc391f579309aaa7bb0ae0189ca6cb444eabadc61a4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:09 GMT
ADD alpine-minirootfs-3.24.0-aarch64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:09 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:15:43 GMT
ARG version=21.0.11.10.1
# Wed, 10 Jun 2026 20:15:43 GMT
# ARGS: version=21.0.11.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 10 Jun 2026 20:15:43 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jun 2026 20:15:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 10 Jun 2026 20:15:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c05efffaed614b5ff4e3b9a80136e7c0eed0b47f434802c81baf254c0defca91`  
		Last Modified: Tue, 09 Jun 2026 20:11:14 GMT  
		Size: 4.2 MB (4202330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccee2a88b4e1c8439d74b52d439b0fdd63cd2de8c80f2b4059e6c0c0eab83015`  
		Last Modified: Wed, 10 Jun 2026 20:16:02 GMT  
		Size: 159.8 MB (159841708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7257384c044e1431f9870fd776cbc934a0890e214faba49f09b7170db391b256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.4 KB (593441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e859d4fa5938ff072ddca4457bcfdb9d214de78293ae4fbe528b41e51e2c1192`

```dockerfile
```

-	Layers:
	-	`sha256:3ad1a1cbb1de82f407c9e545f896ab0923b0b8cf61347717be914720378df6ba`  
		Last Modified: Wed, 10 Jun 2026 20:15:59 GMT  
		Size: 582.6 KB (582602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd5e318243a978e10351acd1f65f6f0dfcbcef9fec2bf3ad9908732b15d1156e`  
		Last Modified: Wed, 10 Jun 2026 20:15:58 GMT  
		Size: 10.8 KB (10839 bytes)  
		MIME: application/vnd.in-toto+json
