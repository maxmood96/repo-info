## `amazoncorretto:16-alpine-full`

```console
$ docker pull amazoncorretto@sha256:5bbc495064db815b1e9ae3b4f4414bfd1a88312ccb7c70ed757bb95947080c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:16-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4389c14487b6352cc1791fa3da9fbdb83cfee28d8efcf571b9628236520db39c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212453390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86a522aee821c91c6ba3e976a752c4c901bd68c983a5fcfabf96e97e86f0e7c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Mon, 26 Jul 2021 18:20:07 GMT
ARG version=16.0.2.7.1
# Mon, 26 Jul 2021 18:20:33 GMT
# ARGS: version=16.0.2.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-16=$version-r0
# Mon, 26 Jul 2021 18:20:34 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jul 2021 18:20:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 26 Jul 2021 18:20:35 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b237e8ec8f6af5a00c2c0ae1aa93844d981ab4cdd90eccb27fb63a64d7b2adaa`  
		Last Modified: Mon, 26 Jul 2021 18:22:19 GMT  
		Size: 209.7 MB (209652823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
