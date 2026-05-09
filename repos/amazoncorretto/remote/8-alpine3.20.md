## `amazoncorretto:8-alpine3.20`

```console
$ docker pull amazoncorretto@sha256:76067bd7734e505d7d9d83b2d1069d099cb8791eaf74367c0965a4c312f297bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.20` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:cbc08a8c9c871a1f2dc200470e057e9be04da403f34d832b4cb5536236bdd997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104382263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7efd0cf541296e155b306ea5fdb4f211f82972c9422d6b69798f72e393976b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:26 GMT
ADD alpine-minirootfs-3.20.10-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:26 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 22:56:44 GMT
ARG version=8.492.09.2
# Fri, 08 May 2026 22:56:44 GMT
# ARGS: version=8.492.09.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 08 May 2026 22:56:44 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 22:56:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 08 May 2026 22:56:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:25f1d6b1951ac8eb3740558fe94cb83d377bdadf95fd9f98b50d2e1b96130471`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.6 MB (3630321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b3d6df29e85cfecf6284a65bae13f7c1f3c9a1f093396f8244bf2a13eb814b`  
		Last Modified: Fri, 08 May 2026 22:56:57 GMT  
		Size: 100.8 MB (100751942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:54dcd0518b452b2eae6f8ee5b1b53e3b59b8be9538586f1eacdd5d7794342680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.4 KB (254381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fbea2125be18e0493b9674d1006ee416875cd34a4b75474a51c73ba9efc9898`

```dockerfile
```

-	Layers:
	-	`sha256:7667461a8022cbbf36a0889a6fbdcb9623d93e639b05128d721f217efbb6217e`  
		Last Modified: Fri, 08 May 2026 22:56:55 GMT  
		Size: 245.0 KB (245026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cafd77469a73df12d9665186324196f316cb1e1821f56656127193e44f270ba`  
		Last Modified: Fri, 08 May 2026 22:56:55 GMT  
		Size: 9.4 KB (9355 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:aefe2c10d9826973eb862d151066725a07e8c5f3c4d503090e52811254246456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104637131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47371c11c6a69c0f056f55f3f48a207210d86ac3e38bb50ee8e65e612a1ee62`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:24 GMT
ADD alpine-minirootfs-3.20.10-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:24 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 22:48:14 GMT
ARG version=8.492.09.2
# Fri, 08 May 2026 22:48:14 GMT
# ARGS: version=8.492.09.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 08 May 2026 22:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 22:48:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 08 May 2026 22:48:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:3f26bc2dec0b515f1c2818f6e13a8f1da1f88179a008445d4e587233386bff78`  
		Last Modified: Thu, 16 Apr 2026 23:53:29 GMT  
		Size: 4.1 MB (4092319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c156372baf8d2d7c81fb71cd742e879e11573dfd86fa99b124cd686af520752`  
		Last Modified: Fri, 08 May 2026 22:48:28 GMT  
		Size: 100.5 MB (100544812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c61a42056620074cd423110f412b609b4bd8c0811b012021e61a304d579e95b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.6 KB (254617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2a9f126955691396f50dd11d1aebd3f96b74dd7cf2e6a67f415363a9235cff8`

```dockerfile
```

-	Layers:
	-	`sha256:a1b775e06ca146e234ec80975ef9d4000c2a93a3931999b1b64c464f8ddde8be`  
		Last Modified: Fri, 08 May 2026 22:48:25 GMT  
		Size: 245.2 KB (245158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d769a32d846dc2946333f2ddf2bad89fd2310ce222483cbb31958ed1110ed169`  
		Last Modified: Fri, 08 May 2026 22:48:25 GMT  
		Size: 9.5 KB (9459 bytes)  
		MIME: application/vnd.in-toto+json
