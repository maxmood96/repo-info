## `amazoncorretto:8-alpine3.17-jre`

```console
$ docker pull amazoncorretto@sha256:244feb5d28f7c5a0a746da56cd1113b872374cd42b25e06b62647f0db2451d6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.17-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bbac661707743546844df332a3996a3671edcb36534e04fddd7a7715cacb0308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44991365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233da5cd4232f5553619e24e5f37339109b6b5d71b5b92fd90283ba67ec7fd79`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:ec892b6986dac395477ae6947272ea0913b711cda60bbd7d575b374ecfc4cee2 in / 
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
	-	`sha256:b99da37831f37d3f77de0ac7a864f9b69f1dbb4461e5ddfe5a3c2b7e2a3586c5`  
		Last Modified: Mon, 22 Jul 2024 22:27:42 GMT  
		Size: 3.4 MB (3391983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ec8924afc6ffd5fdc2c2074136d72927592514dab5c0d02b9cd2ea10b75ca0`  
		Last Modified: Mon, 22 Jul 2024 23:04:23 GMT  
		Size: 41.6 MB (41599382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.17-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a3cf7d60e568bcc07285d83bb6dd3907588dbd4418f57e7e9d73ae1f0f1ae6df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.6 KB (192578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe098e9a4b6274a4289a520624bdea69ebbb8bc6a14a8623f5733d8d9e328951`

```dockerfile
```

-	Layers:
	-	`sha256:b2c1a3279bc1cb71a9f0fef4155033284ffb5250a4f641b5289fee8b07f83387`  
		Last Modified: Mon, 22 Jul 2024 23:04:23 GMT  
		Size: 184.1 KB (184124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4f1f02b9ad3e2bab6f3bd0cf73803968137e2862ce055481c507d52b5999fa5`  
		Last Modified: Mon, 22 Jul 2024 23:04:23 GMT  
		Size: 8.5 KB (8454 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.17-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:80cebc22bbc7bd425b8531bff1f5826ec785a6ff66b31369d7d49ff2316f4a53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44578628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d9aa593f860a52caf4d819709428149a8649d06305d4ad7a34d0d39edbe9c5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:45 GMT
ADD file:deb5b1c3cd4e7a5be179620c767b9d7bfac29f2544596a65b760460e7a645c51 in / 
# Thu, 20 Jun 2024 17:40:45 GMT
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
	-	`sha256:e45a60384f0269bd8514e16cf71591639353996e62a144763c5e519b386ac31c`  
		Last Modified: Thu, 20 Jun 2024 17:41:39 GMT  
		Size: 3.3 MB (3272586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd4551a81efcf753b7f1ec21bd1a0251b16dfec0a64c9232b1343c9238c733f`  
		Last Modified: Thu, 18 Jul 2024 02:13:57 GMT  
		Size: 41.3 MB (41306042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.17-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:466321fec4d73ab197924e553ef19d40a017ef2c740008f9618b14ff54bc7830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 KB (192962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b5a685482a23cf397d02c63a92a95b09b3f623a6ea59b53bb315177a6aebfb2`

```dockerfile
```

-	Layers:
	-	`sha256:0e6896ca98a08c1ca8ada4b5200a0e6c4ac445c020b900a13e4c1442f6b1f412`  
		Last Modified: Thu, 18 Jul 2024 02:13:56 GMT  
		Size: 184.2 KB (184232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e490b596a970d07d34401636e06f77b3fb1840b9f5905556fe154f7b09165caf`  
		Last Modified: Thu, 18 Jul 2024 02:13:56 GMT  
		Size: 8.7 KB (8730 bytes)  
		MIME: application/vnd.in-toto+json
