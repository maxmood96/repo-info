## `amazoncorretto:8-alpine3.14-full`

```console
$ docker pull amazoncorretto@sha256:9e1d1d44a275b8ff90f4b472b534909dab6b817c1ca8f5711eac4d85168206ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8-alpine3.14-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:14168cc565ce7859c4dd70e2f117481fd0dcfa437ec5d7d8e703f18e27d92551
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101919676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:511112a827e73f7fbc0a6707100248d0326e87ec42d99c7d8aa247c6bd57837b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Sat, 19 Mar 2022 00:35:01 GMT
ARG version=8.322.06.2
# Sat, 19 Mar 2022 00:35:08 GMT
# ARGS: version=8.322.06.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Sat, 19 Mar 2022 00:35:08 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 00:35:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Sat, 19 Mar 2022 00:35:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687db627c6d0aaf946aa3ac57c9029a1040aa6c1fcac1c4133f2feb62ae46100`  
		Last Modified: Sat, 19 Mar 2022 00:42:14 GMT  
		Size: 99.1 MB (99103507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
