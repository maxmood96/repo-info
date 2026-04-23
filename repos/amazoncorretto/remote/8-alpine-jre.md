## `amazoncorretto:8-alpine-jre`

```console
$ docker pull amazoncorretto@sha256:3e3372bdb5d31f3f492e368e6e3c76eafb70cf59a92c3157291c3aeffee5aadc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d88cba1e98bc868c2833ac3df383ae377bd35aadc09fb7f2f626e8dd8c32c242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45618008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bac4bca0adfdd3329c04239dcbfe7b8cbef9df19e26e1ff0902b5306d6c7504`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:32:36 GMT
ARG version=8.492.09.1
# Wed, 22 Apr 2026 21:32:36 GMT
# ARGS: version=8.492.09.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:32:36 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:32:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb43b4978d0bc50c52025520cf671881688ada60d6242c27c58127a0f7127e57`  
		Last Modified: Wed, 22 Apr 2026 21:32:48 GMT  
		Size: 41.8 MB (41753819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3f980316e4a9a6069a374d57f14e5688edb17b2ad03a0724fb3adc2c4840b55f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.2 KB (197187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ecf62e856b0a093557f7b5ea3add167b1ff04ce783dcb3d5cf77517662cf7f3`

```dockerfile
```

-	Layers:
	-	`sha256:2388bf342165d220f8a068b2d61bd5e806cf2f5db5ac849171e9ee48463da14a`  
		Last Modified: Wed, 22 Apr 2026 21:32:45 GMT  
		Size: 187.9 KB (187871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c63d6605a7663dce13b3c709e6b1f6addb44c2d164fc870eff0b50b323bff199`  
		Last Modified: Wed, 22 Apr 2026 21:32:45 GMT  
		Size: 9.3 KB (9316 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b44528d4911bcef8f8460f087054033201683d1cba80e8c918082e28e4a05de6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45664646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8774ea453df78aa9ce63e9cf3337bbab394586ebf65ebfb4e583704f2d7397a6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:32:48 GMT
ARG version=8.492.09.1
# Wed, 22 Apr 2026 21:32:48 GMT
# ARGS: version=8.492.09.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:32:48 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:32:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16d762832e83f68f5e47570a57e3c3b0d36f3d893740760f5666d81698d80eb`  
		Last Modified: Wed, 22 Apr 2026 21:32:58 GMT  
		Size: 41.5 MB (41464776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:dae275e14245e5bf2b62ab2c261593cd367b83263fc21ac93e1eeaff16204287
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 KB (196773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee4ba74bbd00ce3c84a541cd6af199008f41a4cbba6c5ae24d1c4f5edab78998`

```dockerfile
```

-	Layers:
	-	`sha256:1c6529fd1ca958071cc212ae26985a14b9fe7872fe3c473a47acbc78ad0273ab`  
		Last Modified: Wed, 22 Apr 2026 21:32:57 GMT  
		Size: 187.4 KB (187353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00e26fca732965e71fd666b113f4474ca5244ffb6f3c66eae9ee09bbf9252ada`  
		Last Modified: Wed, 22 Apr 2026 21:32:57 GMT  
		Size: 9.4 KB (9420 bytes)  
		MIME: application/vnd.in-toto+json
