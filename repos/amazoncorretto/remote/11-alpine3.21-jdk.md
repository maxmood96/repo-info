## `amazoncorretto:11-alpine3.21-jdk`

```console
$ docker pull amazoncorretto@sha256:46cb7d2700c15a303c669cbe5ea6ab1d20bc60982d31382ec09103f4996a395b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.21-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:accfb9f5140c53d563443ae678782aa58a204da9f0c938648068df50374b670e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.6 MB (145588358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d8a18eb9890cdfa7b963c3613ebd25384cb72880fb9f6158b2c122220865933`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=11.0.27.6.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=11.0.27.6.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 15 Apr 2025 21:50:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae27bccbfd4794c783369d03d2e4db1320694d457c213c0a6fe8dbe04f5b0d93`  
		Last Modified: Thu, 08 May 2025 17:09:24 GMT  
		Size: 141.9 MB (141946111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.21-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e4ee1deb8424129cc21a3f9cbfac5e6a46a5d197f73d6960ff88863a65a31807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.2 KB (401222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:717f2bba06dd3347b73ab75b778eb13a2638018546e07318081b08513c31d6d2`

```dockerfile
```

-	Layers:
	-	`sha256:b6d5c289e4d38b36b37419bfaeae65eca0b186875efffa820d2da5dea88b9fc0`  
		Last Modified: Tue, 15 Apr 2025 23:55:33 GMT  
		Size: 390.5 KB (390497 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d021e3c75e0dec6dfd96e5f28e27128cba6a9f027cbf995a02f45cc2876c3ddb`  
		Last Modified: Tue, 15 Apr 2025 23:55:33 GMT  
		Size: 10.7 KB (10725 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.21-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:cd3d2dc75dd9b8cf65e1e6983367f0988e6755621bee629acb050d645fc1d2a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144060553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c409cbd767610cfc12dba5081b09b6b49397a77f13263c6d047a7ea664db3d03`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=11.0.27.6.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=11.0.27.6.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 15 Apr 2025 21:50:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa05e5c4cbe4c1e67eb5b40b9e63db18ad771eeed2437e6109f659d91bfedc6`  
		Last Modified: Thu, 08 May 2025 20:01:35 GMT  
		Size: 140.1 MB (140067524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.21-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:928bde9262250d9902da4a9cc3e57e60f2ec9b3a85a83665826f8238aaca3644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.5 KB (401477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce8cb13019d123da724f839f473412a24571120688b9eb13ac3c4b38168acf8a`

```dockerfile
```

-	Layers:
	-	`sha256:35a79b98d26bd0921f6d55ca89120de52ece708cb783f0587d2bd1fdd589c69d`  
		Last Modified: Wed, 16 Apr 2025 00:07:21 GMT  
		Size: 390.6 KB (390601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fa138c809dd5dc71660216a701400caf22417519258ec51662b5dd75740b22d`  
		Last Modified: Wed, 16 Apr 2025 00:07:20 GMT  
		Size: 10.9 KB (10876 bytes)  
		MIME: application/vnd.in-toto+json
