## `amazoncorretto:8-alpine3.13`

```console
$ docker pull amazoncorretto@sha256:76a0ce81fdef4b533c7232ec40fcd86b02bffb21f89f7f222fd76482a80de1a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8-alpine3.13` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ed3e5e549e8f3012eba4560d2c5f6f74b296ddf85cdf2d07dc2251d37abd6ab0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101932824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d1ca15650487c97752b58afc0a26ba19da2bd40c31d2c4b409ca46a497cbaf5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Wed, 19 Jan 2022 22:02:16 GMT
ARG version=8.322.06.2
# Thu, 20 Jan 2022 03:22:32 GMT
# ARGS: version=8.322.06.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Thu, 20 Jan 2022 03:22:33 GMT
ENV LANG=C.UTF-8
# Thu, 20 Jan 2022 03:22:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 20 Jan 2022 03:22:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca580d7105a4208bec2cb28b43280c2f86d87ad03e729bbb1c7103e7764b4c0`  
		Last Modified: Thu, 20 Jan 2022 03:24:52 GMT  
		Size: 99.1 MB (99110399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
