## `amazoncorretto:8u322-alpine3.12-jre`

```console
$ docker pull amazoncorretto@sha256:3f76db1272905e19ac1a773398dc066a212f043c5c18c8eb89670a6b9d827b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8u322-alpine3.12-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f2ac8caafedb71ddc9e894eef6a2e471ac7571e1b28ffbb1bd3a212f2a8a3e25
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43181209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104ade62e8ab76648b02fb7f7edca71948e42ea48056bdb3c67cc1718fe88768`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:20:08 GMT
ADD file:8f5bc5ce64ef781adadca88e4004e17affc72e6f20dbd08b9c478def12fe1dd3 in / 
# Fri, 12 Nov 2021 17:20:08 GMT
CMD ["/bin/sh"]
# Wed, 19 Jan 2022 22:02:03 GMT
ARG version=8.322.06.2
# Wed, 19 Jan 2022 22:02:13 GMT
# ARGS: version=8.322.06.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0
# Wed, 19 Jan 2022 22:02:14 GMT
ENV LANG=C.UTF-8
# Wed, 19 Jan 2022 22:02:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:8572bc8fb8a32061648dd183b2c0451c82be1bd053a4ea8fae991436b92faebb`  
		Last Modified: Fri, 12 Nov 2021 17:21:10 GMT  
		Size: 2.8 MB (2809473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8aff4d65720cd5af417f2af1c634f2ba9630c2d3369b101f2e05e83eda37e8`  
		Last Modified: Wed, 19 Jan 2022 22:07:57 GMT  
		Size: 40.4 MB (40371736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
