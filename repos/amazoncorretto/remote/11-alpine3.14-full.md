## `amazoncorretto:11-alpine3.14-full`

```console
$ docker pull amazoncorretto@sha256:e1d5af02e71a12650443afd92fcdd4a68688c4da803649badbc984c2aacc0b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-alpine3.14-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3e8c543de7f2793a958b026632f044d259444d1eebde209ea3e47ed5ba2889a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.0 MB (198012069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6966d5f40d5943844d1f0ea5be5cb9db1daae599eaf677bf3d59f7aaa34e1033`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:37 GMT
ADD file:9663235f252e072c52b0f9e25845841e4321cce2caa7467a0d736c6003b05c00 in / 
# Wed, 29 Mar 2023 18:19:37 GMT
CMD ["/bin/sh"]
# Thu, 20 Apr 2023 18:22:53 GMT
ARG version=11.0.19.7.1
# Thu, 20 Apr 2023 18:22:58 GMT
# ARGS: version=11.0.19.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Thu, 20 Apr 2023 18:22:59 GMT
ENV LANG=C.UTF-8
# Thu, 20 Apr 2023 18:22:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 20 Apr 2023 18:22:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f7dab3ab2d6ec29aa28769bec35331fb485b5837501b1e8556413d8b5a79c9c8`  
		Last Modified: Wed, 29 Mar 2023 18:20:25 GMT  
		Size: 2.8 MB (2829647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b99133d400bc723cacf5074f04a9c7a120cc6c45fb59babab415b3f1dd2608`  
		Last Modified: Thu, 20 Apr 2023 18:32:44 GMT  
		Size: 195.2 MB (195182422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-alpine3.14-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:edb77897d7a385d971b50ea9f83fdf5ab7aa78d44c2bb3956350d5e45dda0dac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196193964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b8745399177715eaedf9b575aac177d4a06d86433eda0c11fe593580f3abce4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:25 GMT
ADD file:c3d52cc254959a9ff493e7347e6b1bc25c0ccfdcf9532dbf43173ddd182d0e4d in / 
# Wed, 29 Mar 2023 17:39:25 GMT
CMD ["/bin/sh"]
# Thu, 20 Apr 2023 17:42:08 GMT
ARG version=11.0.19.7.1
# Thu, 20 Apr 2023 17:42:13 GMT
# ARGS: version=11.0.19.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Thu, 20 Apr 2023 17:42:15 GMT
ENV LANG=C.UTF-8
# Thu, 20 Apr 2023 17:42:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 20 Apr 2023 17:42:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:422ed46b1a92579f7c475c0c19fade6880a8d98f23a2b4ccfb77c265d4f72dfc`  
		Last Modified: Wed, 29 Mar 2023 17:40:13 GMT  
		Size: 2.7 MB (2725148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a420344064c8d1ba1004841ccd73768db44fc587864acfabc662a5d44435eb82`  
		Last Modified: Thu, 20 Apr 2023 17:51:28 GMT  
		Size: 193.5 MB (193468816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
