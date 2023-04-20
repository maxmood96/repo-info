## `amazoncorretto:17-alpine3.14-jdk`

```console
$ docker pull amazoncorretto@sha256:04703b102d629df5867ee90b5824a922e136553eecd3cfeae274b7829141e51b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-alpine3.14-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4bbec99288a1d58b430b69c938be5ef9a36d852a01542f8a3a2c4b3135c10446
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.4 MB (196405982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26c2aaa06e762f35fb2d5f4f0437dea0c8a76ebb316b21b01ad2ff4f5df51db`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:37 GMT
ADD file:9663235f252e072c52b0f9e25845841e4321cce2caa7467a0d736c6003b05c00 in / 
# Wed, 29 Mar 2023 18:19:37 GMT
CMD ["/bin/sh"]
# Thu, 20 Apr 2023 18:24:52 GMT
ARG version=17.0.7.7.1
# Thu, 20 Apr 2023 18:24:57 GMT
# ARGS: version=17.0.7.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0
# Thu, 20 Apr 2023 18:24:58 GMT
ENV LANG=C.UTF-8
# Thu, 20 Apr 2023 18:24:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 20 Apr 2023 18:24:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f7dab3ab2d6ec29aa28769bec35331fb485b5837501b1e8556413d8b5a79c9c8`  
		Last Modified: Wed, 29 Mar 2023 18:20:25 GMT  
		Size: 2.8 MB (2829647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e13ba9a5bb2869d0b61549a521861dc547cdcdbc0af640a6f75d1c5922bc08`  
		Last Modified: Thu, 20 Apr 2023 18:35:57 GMT  
		Size: 193.6 MB (193576335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-alpine3.14-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f3ced7516c4ed67a4c024eb1bb31507c84c84f9a83a449bfeb9a1527c371444e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194714466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b7f5aee4f4a72bee9bfd97da1a8fb0486f0a8ae98cbef7f4e3e3cb5f6afbdc4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:25 GMT
ADD file:c3d52cc254959a9ff493e7347e6b1bc25c0ccfdcf9532dbf43173ddd182d0e4d in / 
# Wed, 29 Mar 2023 17:39:25 GMT
CMD ["/bin/sh"]
# Thu, 20 Apr 2023 17:44:05 GMT
ARG version=17.0.7.7.1
# Thu, 20 Apr 2023 17:44:10 GMT
# ARGS: version=17.0.7.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0
# Thu, 20 Apr 2023 17:44:12 GMT
ENV LANG=C.UTF-8
# Thu, 20 Apr 2023 17:44:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 20 Apr 2023 17:44:13 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:422ed46b1a92579f7c475c0c19fade6880a8d98f23a2b4ccfb77c265d4f72dfc`  
		Last Modified: Wed, 29 Mar 2023 17:40:13 GMT  
		Size: 2.7 MB (2725148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4236aee927250a9ba065fc44fd62878ae437869e4f3bd25bd4ebc869782781`  
		Last Modified: Thu, 20 Apr 2023 17:54:33 GMT  
		Size: 192.0 MB (191989318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
