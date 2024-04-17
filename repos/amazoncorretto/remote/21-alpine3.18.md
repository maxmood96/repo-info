## `amazoncorretto:21-alpine3.18`

```console
$ docker pull amazoncorretto@sha256:631d0014996da80a261a204680245a78d850ba626ddcf995be490c92e27ae81c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:21-alpine3.18` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c7c2a3a99b35911132a8fa17d0e4078a79266cf03d948522294adb1e2af272df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.3 MB (163276772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5086216c8f9e94b3952b63e6661fbe5c441a038cc83c99c3b7b7004b81751442`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Wed, 17 Apr 2024 00:06:20 GMT
ARG version=21.0.3.9.1
# Wed, 17 Apr 2024 00:06:27 GMT
# ARGS: version=21.0.3.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip
# Wed, 17 Apr 2024 00:06:27 GMT
ENV LANG=C.UTF-8
# Wed, 17 Apr 2024 00:06:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Apr 2024 00:06:27 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c0ea1758d54f1fae1219fc02c2c4a41f1323a9077dc878dbd84c68ee9a55d55`  
		Last Modified: Wed, 17 Apr 2024 00:26:09 GMT  
		Size: 159.9 MB (159874230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:21-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b1f1a0971099d24cfdc957f27270ad26a8234f7be0a57b1966f5d97c21213371
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160719739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08e32c1a0d0af30f403373a082867c332cbce89654ea5743eff66fbda508f7d6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Wed, 17 Apr 2024 00:15:19 GMT
ARG version=21.0.3.9.1
# Wed, 17 Apr 2024 00:15:24 GMT
# ARGS: version=21.0.3.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip
# Wed, 17 Apr 2024 00:15:26 GMT
ENV LANG=C.UTF-8
# Wed, 17 Apr 2024 00:15:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Apr 2024 00:15:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52da3795450e397a35c13cd17e765f904604bd9a4302ca29a43a54037e3dc7b2`  
		Last Modified: Wed, 17 Apr 2024 00:35:10 GMT  
		Size: 157.4 MB (157386378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
