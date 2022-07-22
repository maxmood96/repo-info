## `amazoncorretto:8u342-alpine`

```console
$ docker pull amazoncorretto@sha256:b4af37915fe75e3feccb4e8926f2d376eb0b41efb3555d6c8e4a8bbfd9921b08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8u342-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f1552362f193b3eb04d966a68a4afdf153d668c99e42f652f663107ee914cc2d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 MB (101612702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df1011b1378ba181c3b05fa740e237cda8fe57c5c6172bda7774c305a4352a7b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:11 GMT
ADD file:c679662d1fba5d188d8f31ab4ebeb7099221926df7630a6917aa461fc33d7ea6 in / 
# Tue, 19 Jul 2022 22:20:11 GMT
CMD ["/bin/sh"]
# Fri, 22 Jul 2022 18:20:26 GMT
ARG version=8.342.07.3
# Fri, 22 Jul 2022 18:20:30 GMT
# ARGS: version=8.342.07.3
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Fri, 22 Jul 2022 18:20:30 GMT
ENV LANG=C.UTF-8
# Fri, 22 Jul 2022 18:20:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 22 Jul 2022 18:20:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:ab6db1bc80d0a6df92d04c3fad44b9443642fbc85878023bc8c011763fe44524`  
		Last Modified: Tue, 19 Jul 2022 22:20:46 GMT  
		Size: 2.8 MB (2814645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1cd5a4f6ce47945ae64d5a04190fa46841466feaea608b4ae91bd9b8562b09b`  
		Last Modified: Fri, 22 Jul 2022 18:24:24 GMT  
		Size: 98.8 MB (98798057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
