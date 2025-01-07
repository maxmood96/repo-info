## `amazoncorretto:21-alpine3.19`

```console
$ docker pull amazoncorretto@sha256:89c8beee3a0b14d72a73852cbcb37fc9760fa5e7919f40be10c88dad3c688025
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.19` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a9dea616fe1cf3531b77448afd1cbd881cfee13cc2153b794bd1d8a22c122774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162349307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c91d7f1acf7fab3445aa8cbf2300600340e931e0327ffd87e8b27b7a5d9c453`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=21.0.5.11.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=21.0.5.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804857584fdbe6d661d5b64a7e35b163ecf8ddc058f11401f59d165e7ba8a2c5`  
		Last Modified: Tue, 12 Nov 2024 02:12:42 GMT  
		Size: 158.9 MB (158929579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:40b09d070938d8be613696437bbb60085294365a0a1c4b87cc6da41a3302bdc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.8 KB (390836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b843946cccc02f089b21daaa9ce28c4ec6a444e8b7f3ca81490a129e4f7ef142`

```dockerfile
```

-	Layers:
	-	`sha256:0017daa3d99837412ae4477d597966f6a08cb0277858c06ed8c7f99b45e49bb4`  
		Last Modified: Tue, 12 Nov 2024 02:12:40 GMT  
		Size: 381.4 KB (381421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c405903ba729aaa884947c4802813df7f6d20b186a706f4098234a6eeacf7da`  
		Last Modified: Tue, 12 Nov 2024 02:12:40 GMT  
		Size: 9.4 KB (9415 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5a28a15a5febc0a34954a4e96d908871a6d4eb0204eebbbf50c33f1c86348837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160237651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dae95b1299101108704821499c2988d4ea9dcff972efe967f67181ec265f39f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=21.0.5.11.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=21.0.5.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e70d98938925701e2d23b6c7267efc15fe083e0beee80b84caf5d635b0b6f2`  
		Last Modified: Tue, 12 Nov 2024 11:12:10 GMT  
		Size: 156.9 MB (156878405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4120eb2ecee8e1aa0f9b4cddbb097202faf06a24d89354c55d55a4bc0f9cc3eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.4 KB (390358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e47d3a0abaccc69ab6687d96db609134431d104517fcac4696c169a45024fb45`

```dockerfile
```

-	Layers:
	-	`sha256:91e0369367be4d34ba472f0796b6c74b74ff2bc098d759cd026d17a5f113d1f0`  
		Last Modified: Tue, 12 Nov 2024 11:12:06 GMT  
		Size: 380.8 KB (380839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28b2a251e53094e6b2c5c27d5bfa9a2c74f81e16fe6db4e4ef4f8f056366feba`  
		Last Modified: Tue, 12 Nov 2024 11:12:06 GMT  
		Size: 9.5 KB (9519 bytes)  
		MIME: application/vnd.in-toto+json
