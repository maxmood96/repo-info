## `amazoncorretto:8-alpine`

```console
$ docker pull amazoncorretto@sha256:e32ced29f597a2f21860b40bef5da718dc4912ee759e6ceb4439740178858699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6aa7629bab21432d34e820e734d234f083b591ff3c922fb7739034194521c0fa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 MB (101603335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ddf9e5717b5b8c6d6f9b0b5b897ed164bbe85b08bd41af59631aa8db359f56a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Wed, 28 Sep 2022 21:19:45 GMT
ARG version=8.342.07.4
# Wed, 28 Sep 2022 21:19:49 GMT
# ARGS: version=8.342.07.4
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Wed, 28 Sep 2022 21:19:49 GMT
ENV LANG=C.UTF-8
# Wed, 28 Sep 2022 21:19:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Sep 2022 21:19:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba4271b59c29ca4de170c1067570f65b6ae879bee597f0765c707b27901ae778`  
		Last Modified: Wed, 28 Sep 2022 21:23:35 GMT  
		Size: 98.8 MB (98797281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
