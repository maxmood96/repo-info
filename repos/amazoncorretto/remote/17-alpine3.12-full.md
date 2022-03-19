## `amazoncorretto:17-alpine3.12-full`

```console
$ docker pull amazoncorretto@sha256:c851e55c646fb25f5896bd027ef62622ac0ea13d72167ad76bdae132d2eaa4d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:17-alpine3.12-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:60ca629dddc01b584de0942b48a37dcb4a3c60d3c3e063f3f70a4bc5faefda32
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194615750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8b6620e77bb8cb4a1de2bdf682e77d6f185a04e8d131778153b151ea871e5c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:45 GMT
ADD file:cdff961a4dd899295df5fd92711f8ee8fd8e682208d52bcfcfa3fcffd295821f in / 
# Thu, 17 Mar 2022 15:19:45 GMT
CMD ["/bin/sh"]
# Sat, 19 Mar 2022 00:37:36 GMT
ARG version=17.0.2.8.1
# Sat, 19 Mar 2022 00:37:47 GMT
# ARGS: version=17.0.2.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0
# Sat, 19 Mar 2022 00:37:48 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 00:37:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Sat, 19 Mar 2022 00:37:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c7f02851fb7d4b5eb2cdd31353ecdcfc954d48241f12bbe91b831f73abe2d29c`  
		Last Modified: Thu, 17 Mar 2022 15:20:34 GMT  
		Size: 2.8 MB (2806202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba32a3cca62d7b5f3732970d09abef6bcba0613606ff3a82cde7cc73ba1b1fd`  
		Last Modified: Sat, 19 Mar 2022 00:46:15 GMT  
		Size: 191.8 MB (191809548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
