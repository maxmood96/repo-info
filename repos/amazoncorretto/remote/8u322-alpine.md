## `amazoncorretto:8u322-alpine`

```console
$ docker pull amazoncorretto@sha256:77b2f9e1b4d3fbd13826e1fc7a36589f54b089c64e8f083471a85e32b313e0e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8u322-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b55ee85ee8ea115d95d8726d4e0280b83c8b8f94b654bcf5a3745e219f53d056
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101915823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1a955941676989fa53579deda183a3693de6c0c8374cfe57b878d60cce0600`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Mar 2022 04:01:58 GMT
ADD file:cf4b631a115c2bbfbd81cad2d3041bceb64a8136aac92ba8a63b6c51d60af764 in / 
# Thu, 17 Mar 2022 04:01:59 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 08:02:20 GMT
ARG version=8.322.06.2
# Thu, 17 Mar 2022 08:02:25 GMT
# ARGS: version=8.322.06.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Thu, 17 Mar 2022 08:02:26 GMT
ENV LANG=C.UTF-8
# Thu, 17 Mar 2022 08:02:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 17 Mar 2022 08:02:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:3d243047344378e9b7136d552d48feb7ea8b6fe14ce0990e0cc011d5e369626a`  
		Last Modified: Thu, 17 Mar 2022 04:02:41 GMT  
		Size: 2.8 MB (2812636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62726b3ae7ba1c28421d57429aecf769ab45c179601db96ebad49c8fa07dd7e5`  
		Last Modified: Thu, 17 Mar 2022 08:04:55 GMT  
		Size: 99.1 MB (99103187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
