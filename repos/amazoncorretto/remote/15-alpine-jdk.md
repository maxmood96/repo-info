## `amazoncorretto:15-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:91d7a26a3f2a4d3b8dd2ad7fcf08e9cfa6d9aa35a54edd6d3f7b1a5f48d3cfc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:15-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2edee727b1c760a96dd0d5267dbbd382e797199806ec701708637d73ef908400
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207722795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c34d404df62de60345bc5826297c3c55e10e2aced6060569dea0b200c74041`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Fri, 22 Jan 2021 23:20:26 GMT
ARG version=15.0.2.7.1
# Fri, 22 Jan 2021 23:20:33 GMT
# ARGS: version=15.0.2.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-15=$version-r0
# Fri, 22 Jan 2021 23:20:34 GMT
ENV LANG=C.UTF-8
# Fri, 22 Jan 2021 23:20:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 22 Jan 2021 23:20:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283c15272aa4724dc3ab01a3af98281a0c0c7696cd21929df1cd2f7951c411b6`  
		Last Modified: Fri, 22 Jan 2021 23:21:50 GMT  
		Size: 204.9 MB (204923729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
