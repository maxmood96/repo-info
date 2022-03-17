## `amazoncorretto:8u322-alpine3.15-jre`

```console
$ docker pull amazoncorretto@sha256:e43e751051a8fbc77531578237c80328383f25a71d72a70d93fd531510a7c1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8u322-alpine3.15-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e209348ae8c8994f85ecc099e5bea7f93673c897d85adf6d219564ebfd314684
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43193731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f0d2ae0178a80c3551bc28060afe99d31c7dd1382f906750a2cec5b085e9521`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Mar 2022 04:01:58 GMT
ADD file:cf4b631a115c2bbfbd81cad2d3041bceb64a8136aac92ba8a63b6c51d60af764 in / 
# Thu, 17 Mar 2022 04:01:59 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 08:02:20 GMT
ARG version=8.322.06.2
# Thu, 17 Mar 2022 08:02:33 GMT
# ARGS: version=8.322.06.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0
# Thu, 17 Mar 2022 08:02:33 GMT
ENV LANG=C.UTF-8
# Thu, 17 Mar 2022 08:02:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:3d243047344378e9b7136d552d48feb7ea8b6fe14ce0990e0cc011d5e369626a`  
		Last Modified: Thu, 17 Mar 2022 04:02:41 GMT  
		Size: 2.8 MB (2812636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1b13689d4839c875f86eb7f16ce9433b04f438eba705b88bff6ec3c1805d82`  
		Last Modified: Thu, 17 Mar 2022 08:05:24 GMT  
		Size: 40.4 MB (40381095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
