## `amazoncorretto:8-alpine3.12-jre`

```console
$ docker pull amazoncorretto@sha256:cdb3060114c4419062a32de2b1c128240e9615c4f8dcf4d1fa17ba2a527b1da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8-alpine3.12-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:107f3983032e2706941e884979ca611b4685e83cb0ae3f50540c9d1e68218b57
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43177908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0603bb43e29879167210f59a707d5f5f7ce1eb663bc40f581606baef3f969ffe`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:45 GMT
ADD file:cdff961a4dd899295df5fd92711f8ee8fd8e682208d52bcfcfa3fcffd295821f in / 
# Thu, 17 Mar 2022 15:19:45 GMT
CMD ["/bin/sh"]
# Sat, 19 Mar 2022 00:34:16 GMT
ARG version=8.322.06.2
# Sat, 19 Mar 2022 00:34:35 GMT
# ARGS: version=8.322.06.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0
# Sat, 19 Mar 2022 00:34:36 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 00:34:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:c7f02851fb7d4b5eb2cdd31353ecdcfc954d48241f12bbe91b831f73abe2d29c`  
		Last Modified: Thu, 17 Mar 2022 15:20:34 GMT  
		Size: 2.8 MB (2806202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd60c6160e64041cfde257d813bd8cb20d815a8edf26c6db6e67458e3a768d4`  
		Last Modified: Sat, 19 Mar 2022 00:41:10 GMT  
		Size: 40.4 MB (40371706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
