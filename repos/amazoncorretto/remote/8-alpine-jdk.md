## `amazoncorretto:8-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:567af54e6223c064b9b2582ff85833c73daa1c03d3070ddca2dac15f2aa44865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3485f9ecd8d69e66934afcb1e8309f9ed32c02e710854824e02756b9e9b440dc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101777645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce0c7480c7ca8176cc27651032454e72bbb7763d8510eae34626314953046bc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 02:47:22 GMT
ARG version=8.275.01.2
# Fri, 11 Dec 2020 02:47:28 GMT
# ARGS: version=8.275.01.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Fri, 11 Dec 2020 02:47:28 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 02:47:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 11 Dec 2020 02:47:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ef433720cc605cc4903eebaf95ee8578c75d94aef68657e57ef8734cf1a7b6`  
		Last Modified: Fri, 11 Dec 2020 02:49:07 GMT  
		Size: 99.0 MB (98980700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
