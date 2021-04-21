## `amazoncorretto:8u282-alpine-jre`

```console
$ docker pull amazoncorretto@sha256:9b512161b10206d94138a47759ca3e1a503f01d6b97169f99bd9fc52f76fb7b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8u282-alpine-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:efdb98e9a99c921602eed17fb06c2f0661abfdff42a9490589d523a55afad5b1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43136777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a944531e0b8aaf3cecdd7a3e65440030e6e4cfca9c15b10481a1ef41aa52d423`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Tue, 20 Apr 2021 23:20:11 GMT
ARG version=8.292.10.1
# Tue, 20 Apr 2021 23:20:26 GMT
# ARGS: version=8.292.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0
# Tue, 20 Apr 2021 23:20:27 GMT
ENV LANG=C.UTF-8
# Tue, 20 Apr 2021 23:20:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4daa33c191f16afa306f7b3db9d2d8b3d1acf292d71a9414a041e146d4ba97a`  
		Last Modified: Tue, 20 Apr 2021 23:22:49 GMT  
		Size: 40.3 MB (40336210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
