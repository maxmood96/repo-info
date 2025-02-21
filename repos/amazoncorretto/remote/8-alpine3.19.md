## `amazoncorretto:8-alpine3.19`

```console
$ docker pull amazoncorretto@sha256:16814eaf9b1869dc0f39fcd68ac40756f9422df83ca6461b01007fcebb136ff5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.19` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e7a235d294de2c6124f1972c5dbb72b8e9382b31a051421304363cd375d9f6f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103645170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47f0b2317569656dbd5177b14e54f6b51cd822e65beaee44c65bd71bc9e051ad`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.19.7-x86_64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=8.442.06.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=8.442.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:83abf496f1b833f01c8f72695520b8975cc8b730d14a8ac270d6201bd0f1877e`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3420868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7af82793b829c59d710dbaef296fc7d79009cc1a54a4545ea4b28100e90302a`  
		Last Modified: Fri, 14 Feb 2025 19:12:09 GMT  
		Size: 100.2 MB (100224302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:40d3ab1dfab74ad1fa393fd26add9a9099db0219baf06b230b9c099d29f87a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 KB (255030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a49eb78d48949feec7eb2aca67e470eb976e2fced89eaebc9cf0fb149a9352b`

```dockerfile
```

-	Layers:
	-	`sha256:3136e859cfc18a7e194b6d305291324f4651665737fd4163f538988632fcd8e5`  
		Last Modified: Fri, 14 Feb 2025 19:12:07 GMT  
		Size: 245.6 KB (245632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca19a28e0b017de1c4b1049f37b84a9b4d69505d3df830fa584375ab50737912`  
		Last Modified: Fri, 14 Feb 2025 19:12:06 GMT  
		Size: 9.4 KB (9398 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9c8dd04ceecd4f512b06fd59e8f983504945b56e7861e82b39601c0e33be714e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.4 MB (103370892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:021133c12543431d73ec3258e9e5cbb0eb3a28b79c9bc426a5ea57d271bf20b0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.19.7-aarch64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=8.442.06.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=8.442.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d13a3fff434d56c3504596695435266be8d07061a80359aa09366eea2e094aa0`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3361424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067f83542dd7f92ff66cc947bc5218abc87e08c81c99d196b5b14f2600288f67`  
		Last Modified: Fri, 14 Feb 2025 22:32:08 GMT  
		Size: 100.0 MB (100009468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6c50b374be69ece6f044ac0f334c6a7712747c9febdd7ee985812f93ad532d14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 KB (255266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a31d4443e4e68f29829e37c4ab4c486aff344c1671705e980ef56b2d9abe265`

```dockerfile
```

-	Layers:
	-	`sha256:5c52f03c66b859f4effc6aca8f9b80a42d6faf548bde052f0eb4e2ceb218ddf4`  
		Last Modified: Fri, 14 Feb 2025 22:32:05 GMT  
		Size: 245.8 KB (245764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d94400e282eb6dd99d95b79cad1aed9141f5422613a9c25b195a3800b84b280e`  
		Last Modified: Fri, 14 Feb 2025 22:32:05 GMT  
		Size: 9.5 KB (9502 bytes)  
		MIME: application/vnd.in-toto+json
