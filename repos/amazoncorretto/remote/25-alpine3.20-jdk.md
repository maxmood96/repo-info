## `amazoncorretto:25-alpine3.20-jdk`

```console
$ docker pull amazoncorretto@sha256:3e3d39c228d137a2b20847fb1b7f43c7dba622d6b750173c36e33c1753041bbc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine3.20-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:94ec0aa562680344ea157e651ca9ceff25c3b49885852f2bad62f58cf8c4962d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.2 MB (182151377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:677d06c63478d541c06196a74c9f20b39c7551a0ea56b11ce9cdf15c40206252`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
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
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20632a406affc774bf067bc277b75acccbe6b8d95ebbf5cedf37f3154c5ed3e`  
		Last Modified: Thu, 09 Oct 2025 04:30:24 GMT  
		Size: 178.5 MB (178524321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:923f929a844561d56bb6d0c8c6be2d99a7387ec3600b66c245b05df3628d6107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.5 KB (396487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b72f8a32504befd44e67a97af30658249cae36314f905042e105db7fe7a2ad4`

```dockerfile
```

-	Layers:
	-	`sha256:a530f17e43633136467f0c4fad23de524deab63e428c5b8ba5d932218f7c825e`  
		Last Modified: Thu, 09 Oct 2025 00:52:07 GMT  
		Size: 387.1 KB (387072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:633d6ca4f3edcb66335b663ee9ac1349f3a4efc6b33ea026737789c8f44f2614`  
		Last Modified: Thu, 09 Oct 2025 00:52:08 GMT  
		Size: 9.4 KB (9415 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-alpine3.20-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d685e433fe8a362b2398c9001e6a91286481d14c971d5e441e8c64fc7edbe4a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.2 MB (180161663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92b283fbbd6463eea0ebb33100d890508326ec3a0ba2b7bca88848c55e5df085`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
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
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Wed, 08 Oct 2025 12:03:09 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0dcf589dbf910f4ff0361ef88d54cc3f93808bbe326f8d291856c62b42aaf5`  
		Last Modified: Thu, 09 Oct 2025 04:30:27 GMT  
		Size: 176.1 MB (176072286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:38708bb6701fbcde2734e1a8debe36dc03fb9b837bac3931bf34af2f9c194da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.0 KB (396007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d3e425944720e0dcc30ea13a99e8f3794ad33408876c57d9893d16d165e8f73`

```dockerfile
```

-	Layers:
	-	`sha256:2ffcbe8fde19e12c4c7438506b71414d388d6d11889a598d91e37b16a1ab1fb0`  
		Last Modified: Thu, 09 Oct 2025 00:52:11 GMT  
		Size: 386.5 KB (386488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1e0cbd3376f1329ab15dea496e823595caa4a026f10ad934f8a8570acf91e8b`  
		Last Modified: Thu, 09 Oct 2025 00:52:11 GMT  
		Size: 9.5 KB (9519 bytes)  
		MIME: application/vnd.in-toto+json
