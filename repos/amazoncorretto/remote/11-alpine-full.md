## `amazoncorretto:11-alpine-full`

```console
$ docker pull amazoncorretto@sha256:35e8797e008eac2e05264c8a3894767b8cd4661ddca0837db1df7795d142ed1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:11-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4201449d2c1ccd174ed6dd41ec90d21a88e5d12ef00e30ba29a1d642b7bc3a0b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.0 MB (196029750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a895b16a7e33d9d36955302d1cd0844f09db71db7afac4b94263a3d347419c3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Tue, 20 Apr 2021 23:20:30 GMT
ARG version=11.0.11.9.1
# Tue, 20 Apr 2021 23:20:37 GMT
# ARGS: version=11.0.11.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Tue, 20 Apr 2021 23:20:37 GMT
ENV LANG=C.UTF-8
# Tue, 20 Apr 2021 23:20:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 20 Apr 2021 23:20:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2531042875644865f91c5f2fa487ccced5f1edb710eb483a2f11059a879156`  
		Last Modified: Tue, 20 Apr 2021 23:23:14 GMT  
		Size: 193.2 MB (193229183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
