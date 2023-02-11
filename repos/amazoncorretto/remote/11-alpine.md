## `amazoncorretto:11-alpine`

```console
$ docker pull amazoncorretto@sha256:1e7217fe3d7a072ea33960f0046708a11f239b453022b5972bf4f30d155d2731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:11-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5fee6a54cbb301301f16d8cc893eaf5f8d9aacf3bd40be4aae5fee3fb2d30c89
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.5 MB (198507911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a1f51d239499c59c16bb9683b823c3af8119525042b1737ea64af78683b076`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:00:06 GMT
ARG version=11.0.18.10.1
# Sat, 11 Feb 2023 07:00:12 GMT
# ARGS: version=11.0.18.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Sat, 11 Feb 2023 07:00:13 GMT
ENV LANG=C.UTF-8
# Sat, 11 Feb 2023 07:00:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Sat, 11 Feb 2023 07:00:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d5c2d90c1480c910408149bf19c4bce729d0fe14e6113b00c29ad8724bfb42`  
		Last Modified: Sat, 11 Feb 2023 07:07:54 GMT  
		Size: 195.1 MB (195133465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
