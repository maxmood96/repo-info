## `amazoncorretto:19-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:75286f3b85f4ebd08c285bd9f864654efd448577704db3888e73c0cba4765ca5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:19-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:be719c180c83f2660cb0bddf5fee35c797c0c43ff76d32a6af8df25f1f62d7b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.5 MB (205461960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f60fb4cfe9555896ecec75a1e92b4191c3badc217bc265c42406152db98b5c47`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:01:42 GMT
ARG version=19.0.2.7.1
# Sat, 11 Feb 2023 07:01:48 GMT
# ARGS: version=19.0.2.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-19=$version-r0
# Sat, 11 Feb 2023 07:01:49 GMT
ENV LANG=C.UTF-8
# Sat, 11 Feb 2023 07:01:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Sat, 11 Feb 2023 07:01:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc4d8c0dcb8192dd18a96f5323ab1dd0399037754ce7d81421093b9dd151797`  
		Last Modified: Sat, 11 Feb 2023 07:12:00 GMT  
		Size: 202.1 MB (202087514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
