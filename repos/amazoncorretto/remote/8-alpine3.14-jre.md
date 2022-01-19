## `amazoncorretto:8-alpine3.14-jre`

```console
$ docker pull amazoncorretto@sha256:511d592ac5f65c0414296be08807e6c13adc60c4bce0bb6442eac196470205c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8-alpine3.14-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:dccd2db5f7caec34df34a2ff8ba39886f20fba09f0a1e88401d7f391ecb1bb69
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43203966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06323fd9c5948e7dbf8147dd9c8c7217e2041061b7faa764df4d98c31c2dde82`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 19 Jan 2022 22:02:37 GMT
ARG version=8.322.06.2
# Wed, 19 Jan 2022 22:02:48 GMT
# ARGS: version=8.322.06.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0
# Wed, 19 Jan 2022 22:02:48 GMT
ENV LANG=C.UTF-8
# Wed, 19 Jan 2022 22:02:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5df95c000527dc5bcd851e31e04fedaf2bb84540177e9dc6f36b7552f4d0daea`  
		Last Modified: Wed, 19 Jan 2022 22:09:02 GMT  
		Size: 40.4 MB (40380985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
