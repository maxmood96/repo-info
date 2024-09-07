## `amazoncorretto:8-alpine3.19-jre`

```console
$ docker pull amazoncorretto@sha256:63fe7ac9ed4fe6f70c09cd8221357a27b8d9d9c938bfce89c5c1f71a9fcf05c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.19-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:97cb328fefb0e5a87ef02b064fe1470bbd3f61aeb7026ac838352ec4d5d9d3db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45019092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ffb8d96e75287f56484eb204e3987e8d6d1320ab434dcbde79c5978bdea57f4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
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
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42ac38a39ce917c8fa653be82c1869e9fd3c51eaf89abd93076dfc5e6538eee`  
		Last Modified: Fri, 06 Sep 2024 23:16:50 GMT  
		Size: 41.6 MB (41599386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ad5b25cecb835c71bd4323e3c63197c5e8890c8a88031f4c86c45fa70ac67d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 KB (193840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbe85682a7f3382274f30ace367ab551889c981a1a7c445c9e82fafd02091d2`

```dockerfile
```

-	Layers:
	-	`sha256:98f5b36e6565af6b28204415b7be16fca6497baa75d7e9b27a1b9d285b838965`  
		Last Modified: Fri, 06 Sep 2024 23:16:50 GMT  
		Size: 185.4 KB (185386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:796aca45c93ee7845b005b9970f2b67200281a600baebde25b650c261c58996c`  
		Last Modified: Fri, 06 Sep 2024 23:16:50 GMT  
		Size: 8.5 KB (8454 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.19-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:66f2773f2d316807702166711b4a57d2415fd52cb8ae4423fe03a5307a42d661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44665448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb282b815f39418164e00e5d97c02198bd7bc0abcef4d3aaa27bea103f61cef8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
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
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebc49b43677af50a569c440d249156eaa1fb24c87c0c8721bbfb02c442ec05b`  
		Last Modified: Sat, 07 Sep 2024 12:07:20 GMT  
		Size: 41.3 MB (41306345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:cb165457ad68858e8e4a7e332353a5f2943e805b251bcdbec9ec2996ca72d497
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.2 KB (194224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8b227a37ace051eff57c676c4f89bee9dfda2697dbbfee743607a3aa4a65127`

```dockerfile
```

-	Layers:
	-	`sha256:d9ea1b90540300829384eda8748607e6dcc08165ac7a6827d5f9ad5a0fb3eee5`  
		Last Modified: Sat, 07 Sep 2024 12:07:18 GMT  
		Size: 185.5 KB (185494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5528650ae4197b3d0f4fb51740c2c6e405a1646d1edc6a40186637b5a0eda7aa`  
		Last Modified: Sat, 07 Sep 2024 12:07:18 GMT  
		Size: 8.7 KB (8730 bytes)  
		MIME: application/vnd.in-toto+json
