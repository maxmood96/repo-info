## `amazoncorretto:21-alpine3.19`

```console
$ docker pull amazoncorretto@sha256:ec774b927da7cf72c74c6a54af3f2ccf6993eb6b02ad5e4eabc74b6d2d637300
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.19` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8f0d5bce9864bdd82b4c28eaf1c3bfc420c7f7473cb9140e2621d8437227c3c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.3 MB (163291764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f544e33c1c835ccc7c0cdd95d2565de68cadea0875a56f7dc98206497b3a36be`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
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
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568fc69116028005d998ef943e435ebe61e4b1a0aa289198870d4fee548f5cf8`  
		Last Modified: Fri, 05 Jul 2024 19:56:32 GMT  
		Size: 159.9 MB (159874432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:61c9fe5e0620ad93886895a75f9c1f14bcc29634d992a0b1ff086ecbf867a589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.1 KB (389071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:953cad085126535b2592d450b526d54e5c88343686b653f19bde4655cec7f2be`

```dockerfile
```

-	Layers:
	-	`sha256:72d630ac6deefe3232103c5168cbcb8d465b5b263947594e6573583af0e2c5e7`  
		Last Modified: Fri, 05 Jul 2024 19:56:28 GMT  
		Size: 378.6 KB (378596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:079a492cdd035667341b2c008c9186ad526f85a7fa69f84c1c773666f41a7ab0`  
		Last Modified: Fri, 05 Jul 2024 19:56:28 GMT  
		Size: 10.5 KB (10475 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0604b6d1579917290c41a43caa659d6209b4e6c8ff7951c2254e6eb6812f4f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160744706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf2fc7cd4e4f9fbd6d81a5c3c081aa7f06526a46bde4e7b709168393139447e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
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
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b51be52e2561313980c806e5ef648b55139c5b5a90931f0008d2837cd64f62`  
		Last Modified: Fri, 05 Jul 2024 20:26:56 GMT  
		Size: 157.4 MB (157387504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:93158d9233d8f4b68a4eda0f2eac03c09c369034febc8ff6092a8973334ccba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.9 KB (388885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10f46493eb428c25c518ef1ccf9fd1c2d86dd4ec3e4eb6a6522c3ae54076dcfa`

```dockerfile
```

-	Layers:
	-	`sha256:4b733c4626763cce91d65919297bd02efe8fe99efb301320613fbbae240b4cfc`  
		Last Modified: Fri, 05 Jul 2024 20:26:53 GMT  
		Size: 378.1 KB (378062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd10aba51554cf4abcd17c7c8ac26618c84d38694e32a1669b52e102180be3ae`  
		Last Modified: Fri, 05 Jul 2024 20:26:53 GMT  
		Size: 10.8 KB (10823 bytes)  
		MIME: application/vnd.in-toto+json
