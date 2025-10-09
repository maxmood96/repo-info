## `amazoncorretto:17-alpine-full`

```console
$ docker pull amazoncorretto@sha256:b4e5ae2a0de33454f70392d7dc0cf765cf07d9b5026cdc30f66195f5f3a3248c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6d4089d1a05d4018fde52d34bf6d6834c4df7e7152c85ddc1a242b3de0132723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.8 MB (149825845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d52a0ede37ea2240fdf736d241d81b797d32bf4ce7baa8b257298afae021938`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=17.0.16.8.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=17.0.16.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1d17fa9b88874d9363c49615439961f81d76b3cfd4f3c8ce8d86e9475cd3fd`  
		Last Modified: Wed, 08 Oct 2025 23:41:15 GMT  
		Size: 146.0 MB (146023393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fbf588b367b5733c3121fd29638ba25b7b743b9a1a3a881bfa6eaaa444dca831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.6 KB (392592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bed591612be5deaf1c39effb266a3b40f49ad301ae1d8eb040ab661daaff915`

```dockerfile
```

-	Layers:
	-	`sha256:98976f8ffd1cb0e9667b91e16cbe715be4ded887dd8ccee2a53b066a3daffc7f`  
		Last Modified: Thu, 09 Oct 2025 00:48:32 GMT  
		Size: 381.9 KB (381867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8fb2bf7885d4a9f24379daaff564a3a616c38dad9c82c9af8d94129f5076a9d`  
		Last Modified: Thu, 09 Oct 2025 00:48:33 GMT  
		Size: 10.7 KB (10725 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:27bc485f4a1c56571b23ec0e5d770b1deca432ad8257bd3f4a318ceddd0d80bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.5 MB (148455502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97217fbf934afe05c24a32740be68815308a6d2d93c4b9616eb8fc7d0eb8023`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=17.0.16.8.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=17.0.16.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8441cae596502c24c1df299139f12ea0010ff305b8532616eb66792872f8b7a`  
		Last Modified: Wed, 08 Oct 2025 22:59:10 GMT  
		Size: 144.3 MB (144317433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:86de97369106bbb0a92fb07b34022c20303aaa5b51f85adeb29333f6ca47c57e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.2 KB (392211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5728ee6b723a6d6db361ccddd4cea8ffdce47e7b1069afae3dab83706a68b3a4`

```dockerfile
```

-	Layers:
	-	`sha256:b68792e84aada5df2fac2f91cc1a6d3bb5f2ac1236bfdee63ec0f9262e17ff13`  
		Last Modified: Thu, 09 Oct 2025 00:48:36 GMT  
		Size: 381.3 KB (381334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d48aa2a11f1627f2fc2ecf615857dd1bb7e47d46956b907c6c25bb6d2baa001`  
		Last Modified: Thu, 09 Oct 2025 00:48:36 GMT  
		Size: 10.9 KB (10877 bytes)  
		MIME: application/vnd.in-toto+json
