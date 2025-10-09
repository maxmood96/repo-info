## `amazoncorretto:25-alpine3.22`

```console
$ docker pull amazoncorretto@sha256:e779e964a15d62c8c39dd3faa17ed2aa921795b642d4437c6c8a3ad8d581cf36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine3.22` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f0c118ffa37b7b3d7f1f1916ea6875d7f8d5d78c525b709f98356a61c5537c47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.3 MB (182323546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2158c2c28bd6d5cb0b74c85c220523506a88e15536b7dbe52df45d55e0f7f64`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=25.0.0.36.2
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=25.0.0.36.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:af6c1fe4088fbbb049c51655abeadbf9a8ffa173bf595c0ec46c4f3813dafcb7`  
		Last Modified: Wed, 08 Oct 2025 23:50:54 GMT  
		Size: 178.5 MB (178521094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.22` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1cb80e5690aff51af015b2000248c1a95951bdbbd51b0cbe6b3dbf4905e34b14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.6 KB (401579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd22c1e0655b06173702d601041ace8647ac33c2107346686faf2620e891b7ac`

```dockerfile
```

-	Layers:
	-	`sha256:08526330c9f21bbc561b1a177974b50993643104538485a4dfd69c7e4bd1ef59`  
		Last Modified: Thu, 09 Oct 2025 00:51:46 GMT  
		Size: 390.9 KB (390858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29c40dbb3e683c54af62e29f044a4e345637469091ffa8256135b20c9b7b79c4`  
		Last Modified: Thu, 09 Oct 2025 00:51:46 GMT  
		Size: 10.7 KB (10721 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c8c90655e8c52b232f2cf8583970991c95b4217f4a568496bbc0d53964bc8dab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.2 MB (180208789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb2235c55e6add621899e63383fad26bb8ad90193f46d27cd020e23f89db36c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=25.0.0.36.2
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=25.0.0.36.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:5bebaba7c9073910ccc58702f77f884b8d201987fef89ce731ab6e34711fcfb4`  
		Last Modified: Wed, 08 Oct 2025 23:18:02 GMT  
		Size: 176.1 MB (176070720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.22` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6d4278e451de05ceafa3b6dca4dd1d84b1ffe2d5f968b599441637f7cecee9ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.2 KB (401195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b724dd05816089478a3892f553076015b0dd54995d2dbf9b3df23262c70bdb7d`

```dockerfile
```

-	Layers:
	-	`sha256:51d60624ee2e8c00d735e0e10c0420fe3eec6e32fd94863aeb1409ec45153f3d`  
		Last Modified: Thu, 09 Oct 2025 00:51:50 GMT  
		Size: 390.3 KB (390322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc181b12d5e755423e8932eddf02a0e9e29e8a0960d55e94d56618838b20c6f1`  
		Last Modified: Thu, 09 Oct 2025 00:51:51 GMT  
		Size: 10.9 KB (10873 bytes)  
		MIME: application/vnd.in-toto+json
