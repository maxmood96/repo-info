## `amazoncorretto:20-alpine3.15-jdk`

```console
$ docker pull amazoncorretto@sha256:da16c5d255f774e05ec6643ee2b6eb29586723d6cc08486be0d57335c9cfca40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:20-alpine3.15-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:79be40cde99a1d4723585776d607674e9b269e1110eaa52a20c09620cc4f09fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.6 MB (206554553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8569481d79cf932a43d8095c0d89c81b3a1f85fbc39fe70be2cf3b207d18dcc2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:33 GMT
ADD file:08ad6c1c886a26e30ae4ab103ff377ee6cfbc1be2437fa227ec28a335c63d78a in / 
# Wed, 29 Mar 2023 18:19:33 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:20:00 GMT
ARG version=20.0.0.36.1
# Wed, 29 Mar 2023 19:20:05 GMT
# ARGS: version=20.0.0.36.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-20=$version-r0
# Wed, 29 Mar 2023 19:20:06 GMT
ENV LANG=C.UTF-8
# Wed, 29 Mar 2023 19:20:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 29 Mar 2023 19:20:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:0ce1dd7918a48990ab749aab2e805c26f691a3a8103495530e7ea5a1d168af4a`  
		Last Modified: Wed, 29 Mar 2023 18:20:17 GMT  
		Size: 2.8 MB (2826596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6011ecefc9ad2a8be3cc5b1f968cf3a448ffa74fd2ec7fcf2bbf485c800d4d25`  
		Last Modified: Wed, 29 Mar 2023 19:30:10 GMT  
		Size: 203.7 MB (203727957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
