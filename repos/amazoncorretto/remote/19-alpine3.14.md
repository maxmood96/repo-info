## `amazoncorretto:19-alpine3.14`

```console
$ docker pull amazoncorretto@sha256:407cb139fa6507e6ebb6bdf5aa4ea2c51065934e586a73823a65226dafbe9406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:19-alpine3.14` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1204ad556865d30cbb6ab5d972e2aab66a6f0ba0252ceef61de85ee3bf9c21a8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204916846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d65b848be3452cf9f6379f7dfc4e8dbb2058f602ec10a41f2b24f2aa682d1719`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:59 GMT
ADD file:a41bb436701fd0adf99a3157d19f172b3e54ea033f5c617009e2d1bdeac206d7 in / 
# Sat, 11 Feb 2023 04:46:59 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 07:01:10 GMT
ARG version=19.0.2.7.1
# Sat, 11 Feb 2023 07:01:18 GMT
# ARGS: version=19.0.2.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-19=$version-r0
# Sat, 11 Feb 2023 07:01:19 GMT
ENV LANG=C.UTF-8
# Sat, 11 Feb 2023 07:01:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Sat, 11 Feb 2023 07:01:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d261077062b2aebb9ca8dc61f2b00e7e2b4e44179d3cfbe526c4ee0c5e41b26f`  
		Last Modified: Sat, 11 Feb 2023 04:47:49 GMT  
		Size: 2.8 MB (2829633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0670e36e2902700f628e9b651a332220c1bb1dcb3ecb919f84b40c8d83a86d8a`  
		Last Modified: Sat, 11 Feb 2023 07:10:32 GMT  
		Size: 202.1 MB (202087213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
