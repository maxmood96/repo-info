## `amazoncorretto:8-alpine3.12-jdk`

```console
$ docker pull amazoncorretto@sha256:5f73e23d6a9e4e59a4236a6dc484e064d0f217336e7366ac827ebfe482178c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8-alpine3.12-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:089a39337aad94d6369d6533bfb973e39d345f49e8b7ce9f33d638c22710b315
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101919759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7545acc6fd12f43ebdb2094016acb78a9b3db2f1712e946423d1bd4eb8a96c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:20:08 GMT
ADD file:8f5bc5ce64ef781adadca88e4004e17affc72e6f20dbd08b9c478def12fe1dd3 in / 
# Fri, 12 Nov 2021 17:20:08 GMT
CMD ["/bin/sh"]
# Wed, 19 Jan 2022 22:02:03 GMT
ARG version=8.322.06.2
# Wed, 19 Jan 2022 22:02:07 GMT
# ARGS: version=8.322.06.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Wed, 19 Jan 2022 22:02:08 GMT
ENV LANG=C.UTF-8
# Wed, 19 Jan 2022 22:02:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 19 Jan 2022 22:02:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:8572bc8fb8a32061648dd183b2c0451c82be1bd053a4ea8fae991436b92faebb`  
		Last Modified: Fri, 12 Nov 2021 17:21:10 GMT  
		Size: 2.8 MB (2809473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9602c138189285e8bb75303e0aa2af2db6f7d24d77f0aa55faf13e485ae20ef`  
		Last Modified: Wed, 19 Jan 2022 22:07:36 GMT  
		Size: 99.1 MB (99110286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
