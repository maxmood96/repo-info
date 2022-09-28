## `amazoncorretto:17-alpine3.16`

```console
$ docker pull amazoncorretto@sha256:3496e4603fb7c1fcc1b32daded1eeab543aa7d9b7c58be84a21e491e644e4a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:17-alpine3.16` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:afb0ab7d50848bfcbf17004c465b993b7557c93dad5990a675e8d7d54bd801a0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.5 MB (194468121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c8d0dff7dc1e742611366719cf4f7039eebc393727f1f38f8ce2955ebac3be1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Wed, 28 Sep 2022 21:20:29 GMT
ARG version=17.0.4.9.1
# Wed, 28 Sep 2022 21:20:35 GMT
# ARGS: version=17.0.4.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0
# Wed, 28 Sep 2022 21:20:35 GMT
ENV LANG=C.UTF-8
# Wed, 28 Sep 2022 21:20:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Sep 2022 21:20:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3656ea9ea5cc0bfa4e5d309614a54292c2033a05e231292937d871753dd2dc`  
		Last Modified: Wed, 28 Sep 2022 21:25:23 GMT  
		Size: 191.7 MB (191662067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
