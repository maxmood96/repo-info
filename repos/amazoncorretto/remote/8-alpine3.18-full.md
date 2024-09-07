## `amazoncorretto:8-alpine3.18-full`

```console
$ docker pull amazoncorretto@sha256:691b9a169978ef6ee4d56ea27af1a135bac55100e4142cc68330a7e72b4275e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.18-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e4fa17110d82dfc95e4a5bc8c49a5ca37efda6af79de6c46c974cdcadaa1595e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103540094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c614a9aa4c39e645e33c4ea59bace64eb02c5c8f4f57319b5522cf4da9afe6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:5dd525c57625a3a84d57d435b3c255f417ad1722250faaf006c66b9090207f66 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:1cc3d825d8b2468ef662a8b631220516f492e24232477209fe863836d2d2ed44`  
		Last Modified: Fri, 06 Sep 2024 22:20:59 GMT  
		Size: 3.4 MB (3416313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57eebac4290f3e8e977d83a9f3378054fb74142f1209a9bbca0a46098b203ab2`  
		Last Modified: Fri, 06 Sep 2024 23:25:53 GMT  
		Size: 100.1 MB (100123781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.18-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:284b9cbe487d0b209cceba02aa5a25d4aab86a7171f8a04fb2c9ae324bcf1d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.2 KB (254228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9da3a59ac3db71ee343b51d2337159411adfe9420e5ddca6d699955da41b65a1`

```dockerfile
```

-	Layers:
	-	`sha256:a99874cd4067727db40873e5ec5b581abe408c437600e93cea80cd9b9a187813`  
		Last Modified: Fri, 06 Sep 2024 23:25:52 GMT  
		Size: 245.1 KB (245075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80a704684a60befe1d5133933ee3a942cb49aa7884b488c7e66df4fb58b3e430`  
		Last Modified: Fri, 06 Sep 2024 23:25:51 GMT  
		Size: 9.2 KB (9153 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.18-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:42c5a9e76b39430e760513a27bd58a51365cdfea78746da76c1a3848356bbaac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.2 MB (103175425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b82c04d1a356d80a6f5261deee66c6d70edf8da49466694ca3872c74597cca9b`
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
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:439e6a3a58b098e98be3c67c1056b1ad0f5c908e17ca369d0ccdea4d2f6b1d3a`  
		Last Modified: Wed, 24 Jul 2024 10:37:46 GMT  
		Size: 99.8 MB (99835931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.18-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3e3c475f7031c92307ba752878258ee8671b7f3dcc42ebb505b29b5f1638abdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 KB (254659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdff50760433a0d3ab5d8c987f065992d86532c6b47ee803f89c79dd1ba8b392`

```dockerfile
```

-	Layers:
	-	`sha256:81ed5cd809be495b1f697b374e52b976365a45d6e29822a7576b82dd240d1056`  
		Last Modified: Wed, 24 Jul 2024 10:37:44 GMT  
		Size: 245.2 KB (245207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7010a7ddb8977ea2560d39fe16105b8afcb4bbbd59333061e326b1bdd9f728d3`  
		Last Modified: Wed, 24 Jul 2024 10:37:43 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.in-toto+json
