## `amazoncorretto:21-alpine3.18-full`

```console
$ docker pull amazoncorretto@sha256:0d44eb66e366f1913db16cca0ac803f473710a98e019d266c795c5583cca0c94
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.18-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:44538846737b47d1ea67a72c7eaa96f8774901c96d0fc455a620d687173942cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.3 MB (163288092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23bf68e30b6d8b62339964b3b916bba89f4f979d2ae8b9873f99b6587987ca16`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
ADD file:aa183dc07d0f6a47c02f7f1388fa0ce4639ad328111172149be7c7c65d634ded in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=21.0.3.9.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=21.0.3.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Apr 2024 21:21:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:73baa7ef167e70f1c0233fe09e741780d780ea16e78b3c1b6f4216e2afbbd03e`  
		Last Modified: Thu, 20 Jun 2024 20:17:53 GMT  
		Size: 3.4 MB (3413894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fc1fce04315a520e80ab9b0493cca987508f0ebae6a76cc75c6baba66c5a5a`  
		Last Modified: Fri, 05 Jul 2024 19:56:31 GMT  
		Size: 159.9 MB (159874198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.18-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4f9f1428455aca5c7fab770815b265a487b0388ec396f8a38f9fdab53dfbdca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.8 KB (385799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:466f09464d9bcd4c54f949628aee67775425c38b2281cdc4ec153b862df79a83`

```dockerfile
```

-	Layers:
	-	`sha256:b34c7dfea8312e192b36d3848e86863f0ca257ec0db9b7fbc697a1ab956c2784`  
		Last Modified: Fri, 05 Jul 2024 19:56:28 GMT  
		Size: 376.6 KB (376630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db1c523a0b9c27fecc6887ec4df569a91ad6dc8fd647d2e3f3d44b45c9890d11`  
		Last Modified: Fri, 05 Jul 2024 19:56:28 GMT  
		Size: 9.2 KB (9169 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.18-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:40e40c225547a346831f3544acd9d9c2a8957e1066b03bc1a96d70d36b54a644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160724546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b40be60aaf83b5a6dfc5a863b7b1ac9951718f9a810edc2c81d817793068f3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
ADD file:4f760ede9d48d6073317cae6d632deaab101f337e09c56a7f9b8847ed99de3e8 in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=21.0.3.9.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=21.0.3.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Apr 2024 21:21:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5c905c7ebe2fecec0b1115f145c0ea74b3233aa25d8239903194f6b4424044ce`  
		Last Modified: Thu, 20 Jun 2024 17:41:31 GMT  
		Size: 3.3 MB (3337949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9625ec5c3ca1ad3b3d2cd69c2e530fc6ab0a7f2bf45f48de5b3863bd601fca`  
		Last Modified: Fri, 05 Jul 2024 20:26:19 GMT  
		Size: 157.4 MB (157386597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.18-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:98045a95dc3ef4ae8860b2b188d8388d6c210776e6bcf7fcaf9875b04876cd73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.5 KB (385516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b1af969dd194737cc7cc0ef9e4e15df35592d0853128ff210c79b5536c06c9`

```dockerfile
```

-	Layers:
	-	`sha256:f0ca24e9b75af2246f4c89db66f596208634a51f61e9e9ff343de5456d6d8aae`  
		Last Modified: Fri, 05 Jul 2024 20:26:15 GMT  
		Size: 376.0 KB (376048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13a0b2b1d83c020790d9a320be2b804eb634b02fd955e2a755ada21fd93da5f2`  
		Last Modified: Fri, 05 Jul 2024 20:26:15 GMT  
		Size: 9.5 KB (9468 bytes)  
		MIME: application/vnd.in-toto+json
