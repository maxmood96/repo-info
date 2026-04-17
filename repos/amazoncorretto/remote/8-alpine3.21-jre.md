## `amazoncorretto:8-alpine3.21-jre`

```console
$ docker pull amazoncorretto@sha256:144c868b95db8cc62a64a6735f29f97e90e2f0c630a47efcc12af30852bf9e74
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.21-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:dfce394dd51524602ae3ea4efdee002e47ae997b22998b53ad00b25c7034b1ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45390796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68f98c02e9118e9fdd142fcae08e64f4be9aa0c0bf7f3e9ffbfbfdb81c6c1f8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:22:13 GMT
ARG version=8.482.08.1
# Fri, 17 Apr 2026 00:22:13 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 17 Apr 2026 00:22:13 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:22:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5331b294b95e4a9964bcfff0cb7df450dcf5428c975b7ca86ba9735a908c6356`  
		Last Modified: Fri, 17 Apr 2026 00:22:23 GMT  
		Size: 41.7 MB (41743921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.21-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:581fa4f24f1fe77f567af8c10496cb851456ff28f0e20e6f40581fd1660c4c10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.4 KB (197381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799f47502a9304b8245e819fcf237256e93b9d75891b56d7898a75403410e89c`

```dockerfile
```

-	Layers:
	-	`sha256:2f1446afd18a51b9034f371671a2e80bd47c2289f4de14dec70d8232aa570e72`  
		Last Modified: Fri, 17 Apr 2026 00:22:21 GMT  
		Size: 188.7 KB (188725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f30e770f204f8f0f9e6d898ce109d0af82dcd81aa04026871aa134065e692374`  
		Last Modified: Fri, 17 Apr 2026 00:22:21 GMT  
		Size: 8.7 KB (8656 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.21-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b78a69235d2efe807d74abf76a491eeffa57bd8515bbb93cea76b12b637c8658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45450950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff6ab8bde3cc9b0a240aebaafa2c9bd446e2e5f686879afcd417d37749114b1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:13 GMT
ADD alpine-minirootfs-3.21.7-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:13 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:24:09 GMT
ARG version=8.482.08.1
# Fri, 17 Apr 2026 00:24:09 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 17 Apr 2026 00:24:09 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:24:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:2dd7199cff98a7400e801cbfad6de906972a4e3dd0a749d4c1b80f5a1e3e4108`  
		Last Modified: Thu, 16 Apr 2026 05:32:50 GMT  
		Size: 4.0 MB (3994465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a75edc6e0a13e6b8f0f212a6e7d0f6fc2f2c3a43721edce64116b5ec6621c3ba`  
		Last Modified: Fri, 17 Apr 2026 00:24:19 GMT  
		Size: 41.5 MB (41456485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.21-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:45470b684fd62339344f961df4a86dc07c37025dde072c611ddafa6da919ea79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.6 KB (197569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08969460844059c5b8598b902ca12e66fa5a10a6a81a48e6763b543b9335b78f`

```dockerfile
```

-	Layers:
	-	`sha256:47b299d7b52de8859de34d57e727fd727524d0c23fb45543702b0ec04883aa73`  
		Last Modified: Fri, 17 Apr 2026 00:24:18 GMT  
		Size: 188.8 KB (188833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db5b174233b2529640b5b4028cd7b4db59df01d45f220c1bff0483a977c8f5c1`  
		Last Modified: Fri, 17 Apr 2026 00:24:18 GMT  
		Size: 8.7 KB (8736 bytes)  
		MIME: application/vnd.in-toto+json
