## `amazoncorretto:8u262-alpine`

```console
$ docker pull amazoncorretto@sha256:338740eba6f584e41d9377e5d08422d4c1cca56ddfee7fffa24200485d0be597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8u262-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:05e25d0ff71de61969216676ebaaa44489e604cb39c6dbdc8c820d797cde2137
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.8 MB (100774800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72eb4df6544bee28d5ab4ae5fe858f18d5bf90c15ba190a00012668acfa3e6b5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 02:51:34 GMT
ARG version=8.265.01.2
# Thu, 22 Oct 2020 02:51:42 GMT
# ARGS: version=8.265.01.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Thu, 22 Oct 2020 02:51:43 GMT
ENV LANG=C.UTF-8
# Thu, 22 Oct 2020 02:51:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 22 Oct 2020 02:51:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2ea2e70b7ba8722f7d6ede0096e3838b0d225fe238f784a4cdbf9dfef24623`  
		Last Modified: Thu, 22 Oct 2020 02:53:19 GMT  
		Size: 98.0 MB (97977940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
