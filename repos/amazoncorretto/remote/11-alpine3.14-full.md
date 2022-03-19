## `amazoncorretto:11-alpine3.14-full`

```console
$ docker pull amazoncorretto@sha256:49c63925604dc5edaafb6f39d38018e8f9b4a62d40418876ebe63e1eb9e2c1d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:11-alpine3.14-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9e1e0ad1683a61dea18ff8e5adb345a3b00c27505135192e4a7dab29a43cb9b6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196279578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa0c3f14de637fc70c2f36eeae0d799381d923283bc0aaff04ea6169e6c99e4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:26 GMT
ADD file:8ec3735d4b1b4b070607b94e3bd360117b07dc26e1baf5dd485b49b3413e8fff in / 
# Thu, 17 Mar 2022 15:19:26 GMT
CMD ["/bin/sh"]
# Sat, 19 Mar 2022 00:36:37 GMT
ARG version=11.0.14.9.1
# Sat, 19 Mar 2022 00:36:44 GMT
# ARGS: version=11.0.14.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Sat, 19 Mar 2022 00:36:45 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 00:36:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Sat, 19 Mar 2022 00:36:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:36ccefbf3d8a9a1b18baaa9cbf0f3ad50e8a7b751656c74df359900a318cbffc`  
		Last Modified: Thu, 17 Mar 2022 15:20:13 GMT  
		Size: 2.8 MB (2816169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:924dd72b8055076502ca3fffe5367ee3389fe8b54135b4a3a463b8f7fa5e0968`  
		Last Modified: Sat, 19 Mar 2022 00:44:55 GMT  
		Size: 193.5 MB (193463409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
