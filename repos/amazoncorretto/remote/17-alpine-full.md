## `amazoncorretto:17-alpine-full`

```console
$ docker pull amazoncorretto@sha256:55910135e17f0cbde36944c00fa327dc350cdc3f71bc3b150bb0950a116990c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:17-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d998c1ed83f30560f22eb8063fd75bc8848ae52f1b3fdd2367438b5287310e0d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194740962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40665b97c2b589f3dfc5d89624684d410af2911b107db2ef0777d879d5e729f9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:36:36 GMT
ARG version=17.0.5.8.1
# Sat, 12 Nov 2022 04:36:42 GMT
# ARGS: version=17.0.5.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0
# Sat, 12 Nov 2022 04:36:42 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 04:36:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Sat, 12 Nov 2022 04:36:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345c203382bf9a9870d2c450d2d4c9184f0145cf1f5061603bcd88294e6215a6`  
		Last Modified: Sat, 12 Nov 2022 04:41:04 GMT  
		Size: 191.9 MB (191934690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
