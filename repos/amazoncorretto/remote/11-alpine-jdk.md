## `amazoncorretto:11-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:e023facd0fecabe49ce9ce2ac57c51cdca7ddaf24e7ecf09342bb781fc281ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:11-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:04fd2eb740baf12c3cc07d2826016b1da3695ca3e2567c5d59628153d9ec1e3d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194418801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5704a31cbe1a69c5cdca36f036d56034c2b67c75232f85b75d9cadca3bfa2bee`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Wed, 26 Aug 2020 18:20:09 GMT
ARG version=11.0.8.10.1
# Wed, 26 Aug 2020 18:20:16 GMT
# ARGS: version=11.0.8.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar xvzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Wed, 26 Aug 2020 18:20:16 GMT
ENV LANG=C.UTF-8
# Wed, 26 Aug 2020 18:20:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 26 Aug 2020 18:20:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aee8c7ecf2e507ad103df153fa6dc6c60ea3682d246372b827b48335854d42f`  
		Last Modified: Wed, 26 Aug 2020 18:21:13 GMT  
		Size: 191.6 MB (191621260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
