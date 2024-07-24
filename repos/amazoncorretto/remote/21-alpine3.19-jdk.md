## `amazoncorretto:21-alpine3.19-jdk`

```console
$ docker pull amazoncorretto@sha256:c815b95bbbe1eb4f14f9db14884edd1e2c061cb2d3192017476a0d94d611d23d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.19-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bfc998fefa75d3c92b0dd1c2cf5a393b11d188a45208d91b88f4db8ffa260939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163144997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd949cdcebd5106dd03562a46fde86fd86158d0dcf67c10bd7cb2b6bc28ca14`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=21.0.4.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=21.0.4.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123f128cbd4e3b0ba308fa776cf8ded7feb7d83c33ffd1ae5410a9fbc493bcc2`  
		Last Modified: Mon, 22 Jul 2024 23:05:00 GMT  
		Size: 159.7 MB (159725957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b34c63dc915d5d733d9455c74c4ab725b161b2945e5b88e2c8ee8733937d53ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.5 KB (390482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38bd0134c8ce4eeb0063ac52b2da27506ba2503e90f5be90859df3ca38026056`

```dockerfile
```

-	Layers:
	-	`sha256:c37027bf46ab8fdf42e8bcdc13ead9571fffee98c39388b41a115d82fa617923`  
		Last Modified: Mon, 22 Jul 2024 23:04:58 GMT  
		Size: 381.3 KB (381313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3064f03baca3495e91d7709e0297308ee052b6ba49d10303130313a833eb21be`  
		Last Modified: Mon, 22 Jul 2024 23:04:58 GMT  
		Size: 9.2 KB (9169 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.19-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:212d0dc65ec85884b62cc086f2914a18bc5336d03a3b7243ff24bd8d3132e8e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160839862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad1f427852b562cb9d3626f752ae588cb0cb9fbe7b5265b5ddf8c17e734c521`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=21.0.4.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=21.0.4.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2ff134aac824399135305ce77bb44258563cd5ef5fa3afec41036025a0969e`  
		Last Modified: Wed, 24 Jul 2024 10:45:43 GMT  
		Size: 157.5 MB (157481404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b91732bbda9de212801be55f00fd8f745be25b8c231690b35633d571910a874c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.2 KB (390200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5159dc43a959b27405e5442558525e533f569932d4d0e79a7f4f215dab2c2f25`

```dockerfile
```

-	Layers:
	-	`sha256:fd35b2b68450bc1cc7e75760d95bb3ad892b517a6e3ad453b6d23472d5cc7a57`  
		Last Modified: Wed, 24 Jul 2024 10:45:39 GMT  
		Size: 380.7 KB (380731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e3732b42d0fd5c8db34d462b0f3baebf7954a2652e79b14c6445d033a9ea533`  
		Last Modified: Wed, 24 Jul 2024 10:45:39 GMT  
		Size: 9.5 KB (9469 bytes)  
		MIME: application/vnd.in-toto+json
