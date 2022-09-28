## `amazoncorretto:11-alpine-full`

```console
$ docker pull amazoncorretto@sha256:72caf67123f80e86c759c408f08aa5c0a60745650a6faba2b1ae7de86628f1ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:11-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7b4e3f58835d9bbbdef6cefacb2c573d6b238575d7b2e994bdbf0c7a2e919ac8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.0 MB (196015456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704ee5dd2be52aa7775032246244b14fdfcd005ebb27a2529548091e25cb8497`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Wed, 28 Sep 2022 21:20:09 GMT
ARG version=11.0.16.9.1
# Wed, 28 Sep 2022 21:20:15 GMT
# ARGS: version=11.0.16.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Wed, 28 Sep 2022 21:20:15 GMT
ENV LANG=C.UTF-8
# Wed, 28 Sep 2022 21:20:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Sep 2022 21:20:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079fc43f6f5bd2828ac482a984f769069359b0186bd2293bd08ce4fcf52a7140`  
		Last Modified: Wed, 28 Sep 2022 21:24:38 GMT  
		Size: 193.2 MB (193209402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
