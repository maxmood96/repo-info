## `amazoncorretto:17-alpine3.12-full`

```console
$ docker pull amazoncorretto@sha256:a4b113856c1a0326f73a17873af73e69f7eceef75ab99203830078d954559447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:17-alpine3.12-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3b5fc1d401dc9c288349878b51a927f21764d9ae06efb32650f305cb24e6bba8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194619174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e16502fca0f83a36af02b60d5780efb96fd76b069669cdb9cc837ead5910af`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:20:08 GMT
ADD file:8f5bc5ce64ef781adadca88e4004e17affc72e6f20dbd08b9c478def12fe1dd3 in / 
# Fri, 12 Nov 2021 17:20:08 GMT
CMD ["/bin/sh"]
# Wed, 19 Jan 2022 22:04:49 GMT
ARG version=17.0.2.8.1
# Wed, 19 Jan 2022 22:04:59 GMT
# ARGS: version=17.0.2.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0
# Wed, 19 Jan 2022 22:05:00 GMT
ENV LANG=C.UTF-8
# Wed, 19 Jan 2022 22:05:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 19 Jan 2022 22:05:00 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:8572bc8fb8a32061648dd183b2c0451c82be1bd053a4ea8fae991436b92faebb`  
		Last Modified: Fri, 12 Nov 2021 17:21:10 GMT  
		Size: 2.8 MB (2809473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b225b834f4fbbae275317056b1ce450d0d3d3cb47ef9b22a6c5f3fafd9ddd0`  
		Last Modified: Wed, 19 Jan 2022 22:15:46 GMT  
		Size: 191.8 MB (191809701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
