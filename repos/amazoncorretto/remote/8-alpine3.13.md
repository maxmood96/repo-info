## `amazoncorretto:8-alpine3.13`

```console
$ docker pull amazoncorretto@sha256:3f4792f7859ffebf3b1c6291d7150db896f999580b4e3844a245a75652bc082d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8-alpine3.13` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:fc93fe212267a4f2f0dbe6b8e6934d8c86512bb23de5feb0537a682da0f04b52
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 MB (101610978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26279e7e7a00fd12eb29037eaf5d432c1fbf4fce3f9cdbf91f7742da230fe2bf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 19 Jul 2022 22:20:26 GMT
ADD file:e15461ac94648d9599df6304a53587fc8bfceaf6e111ee5917860e95ed9e751c in / 
# Tue, 19 Jul 2022 22:20:26 GMT
CMD ["/bin/sh"]
# Fri, 22 Jul 2022 18:19:58 GMT
ARG version=8.342.07.3
# Fri, 22 Jul 2022 18:20:03 GMT
# ARGS: version=8.342.07.3
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Fri, 22 Jul 2022 18:20:03 GMT
ENV LANG=C.UTF-8
# Fri, 22 Jul 2022 18:20:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 22 Jul 2022 18:20:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:627fad6f28f79c3907ad18a4399be4d810c0e1bb503fe3712217145c555b9d2f`  
		Last Modified: Tue, 19 Jul 2022 22:21:04 GMT  
		Size: 2.8 MB (2819330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe3764ae396caae9b9163ce8ae97deafb6e1a83528ade99f759f4e0f51b32e6d`  
		Last Modified: Fri, 22 Jul 2022 18:23:11 GMT  
		Size: 98.8 MB (98791648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
