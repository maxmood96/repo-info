## `amazoncorretto:11-alpine3.12-jdk`

```console
$ docker pull amazoncorretto@sha256:c5f2664511aa2adc621347084ec0d3457b588cbc4c8099920fb0434cc07b027e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:11-alpine3.12-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c97261a5a149a29949d5949665d03e25c76359660aacc0427f6736fb58ffaf49
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196271111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:109f955a483ad8c209db56129995b03c842381cc8e93d7fd35c33514ce99c726`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:20:08 GMT
ADD file:8f5bc5ce64ef781adadca88e4004e17affc72e6f20dbd08b9c478def12fe1dd3 in / 
# Fri, 12 Nov 2021 17:20:08 GMT
CMD ["/bin/sh"]
# Wed, 19 Jan 2022 22:03:33 GMT
ARG version=11.0.14.9.1
# Wed, 19 Jan 2022 22:03:39 GMT
# ARGS: version=11.0.14.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Wed, 19 Jan 2022 22:03:40 GMT
ENV LANG=C.UTF-8
# Wed, 19 Jan 2022 22:03:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 19 Jan 2022 22:03:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:8572bc8fb8a32061648dd183b2c0451c82be1bd053a4ea8fae991436b92faebb`  
		Last Modified: Fri, 12 Nov 2021 17:21:10 GMT  
		Size: 2.8 MB (2809473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b5ef1d2b2fa09080142f92672fb45a7fcba20765ee3bdc712f34a7c9984667`  
		Last Modified: Wed, 19 Jan 2022 22:11:25 GMT  
		Size: 193.5 MB (193461638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
