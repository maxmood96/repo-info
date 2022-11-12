## `amazoncorretto:11-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:5cab8451adb8a919c6799ececf2503eca84c18b9b96df47f4549ea00dde90a65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:11-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:19243002f9ce5089604cd5207bcb8a14b948e1af1a72863f78bec29ce3d21d4d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196348843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6024c40c727e99afaee8d65a18399970ded0fc215c38f00ba4c88d428365abb0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:36:10 GMT
ARG version=11.0.17.8.1
# Sat, 12 Nov 2022 04:36:16 GMT
# ARGS: version=11.0.17.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Sat, 12 Nov 2022 04:36:17 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 04:36:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Sat, 12 Nov 2022 04:36:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2778865ff857685f8e3b22551f6e42a3a424e5d699a69417ebda32e5eb752d02`  
		Last Modified: Sat, 12 Nov 2022 04:40:17 GMT  
		Size: 193.5 MB (193542571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
