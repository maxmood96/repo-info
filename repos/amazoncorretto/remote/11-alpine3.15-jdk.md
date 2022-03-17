## `amazoncorretto:11-alpine3.15-jdk`

```console
$ docker pull amazoncorretto@sha256:d076873974efcd38178c0640d4bf2b6d604ccf4f342055a79091db7a6034b432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:11-alpine3.15-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4c447df5a5b023311f6c20d9a52f57deb285ba98f2a31a756ee7807e6af10049
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196276092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74266140ac047fbe80e491ed5cb8e4450498ce288dcefe71f7b58b39ad61951d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Mar 2022 04:01:58 GMT
ADD file:cf4b631a115c2bbfbd81cad2d3041bceb64a8136aac92ba8a63b6c51d60af764 in / 
# Thu, 17 Mar 2022 04:01:59 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 08:02:45 GMT
ARG version=11.0.14.9.1
# Thu, 17 Mar 2022 08:02:51 GMT
# ARGS: version=11.0.14.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Thu, 17 Mar 2022 08:02:51 GMT
ENV LANG=C.UTF-8
# Thu, 17 Mar 2022 08:02:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 17 Mar 2022 08:02:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:3d243047344378e9b7136d552d48feb7ea8b6fe14ce0990e0cc011d5e369626a`  
		Last Modified: Thu, 17 Mar 2022 04:02:41 GMT  
		Size: 2.8 MB (2812636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761b54b7438ec7c153db9477d740c32b943e1e98d7a4bc3d5e22cc138696b66c`  
		Last Modified: Thu, 17 Mar 2022 08:06:00 GMT  
		Size: 193.5 MB (193463456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
