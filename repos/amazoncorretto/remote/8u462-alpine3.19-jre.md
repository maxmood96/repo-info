## `amazoncorretto:8u462-alpine3.19-jre`

```console
$ docker pull amazoncorretto@sha256:56db2581993b5b5141473eb114157e850b1585dfc177ada4c1390b66f5d9ba21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u462-alpine3.19-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:73d4c3a0b6724b4fd1ad260a98f633759191b20e400ee1dd99851baced4185a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45147115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21406310a090b22cc0706e6ba5a0cc8b8645ee395f86f79e8052e49f696b6c1b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:32:09 GMT
ADD alpine-minirootfs-3.19.8-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:32:09 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 19:33:24 GMT
ARG version=8.462.08.1
# Wed, 16 Jul 2025 19:33:24 GMT
# ARGS: version=8.462.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Jul 2025 19:33:24 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 19:33:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:1747dece94917ce1b0256ecd60138ce4deaea1bd35dcb6b2e8afe697dd2f5b71`  
		Last Modified: Tue, 15 Jul 2025 18:59:51 GMT  
		Size: 3.4 MB (3415528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c0d37503733cd4425e4d77e12813f331073e870a4749d48e7b0833e207cbff5`  
		Last Modified: Wed, 16 Jul 2025 20:24:52 GMT  
		Size: 41.7 MB (41731587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u462-alpine3.19-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2a4fabb749c49a19deefc7c992eb7cd9cb24511fafb839477b7fea2293573177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.8 KB (195800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a58bce359287cbe3fc7ba1be86c2045af668ecd6205197b0ee409ba05f3d2f`

```dockerfile
```

-	Layers:
	-	`sha256:663a196561c53ad138fa383e15dec569b29675987b8ba3c570a03b995cf5de64`  
		Last Modified: Wed, 16 Jul 2025 21:51:36 GMT  
		Size: 187.1 KB (187101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43a476bd61fe9beec6ee8c4ae10165cdaa9cc54a0ae659f359609ebcf1a8f440`  
		Last Modified: Wed, 16 Jul 2025 21:51:36 GMT  
		Size: 8.7 KB (8699 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u462-alpine3.19-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:2237db9d64e389ad77708f0add70f0818cd09cc72f34b5fcfb47f0fdc8e02bd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44790046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f409b7119eb2a3cad1725de51555611520ee4a58162f002e0849da0aa650b57`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:32:09 GMT
ADD alpine-minirootfs-3.19.8-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:32:09 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 19:33:24 GMT
ARG version=8.462.08.1
# Wed, 16 Jul 2025 19:33:24 GMT
# ARGS: version=8.462.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Jul 2025 19:33:24 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 19:33:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:07e9a47f0c334cceba1b05e86ef0150c84564a9b9e9d4ae9dc9a5ebc85ef2b7c`  
		Last Modified: Tue, 15 Jul 2025 19:00:19 GMT  
		Size: 3.4 MB (3353103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeff64e42dd2af72bbfd1a56991933ade45d0e9b786193ce1ca123b31fc398fb`  
		Last Modified: Thu, 17 Jul 2025 01:47:09 GMT  
		Size: 41.4 MB (41436943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u462-alpine3.19-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:bba3c005b9481972a5a49e4340a70920a4f9c55c5aea9c68a8213eae12c08022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.0 KB (195987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e8b018b056803c508a5ffefddc5b0b1f6e1544bec165ee4b635127d77765d5b`

```dockerfile
```

-	Layers:
	-	`sha256:6c6a9adb4a7c3e9709b57219a46ab7629ac3c15b17fe9d768abc3a92e9b3f9cb`  
		Last Modified: Thu, 17 Jul 2025 03:51:29 GMT  
		Size: 187.2 KB (187209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a848d35fc85c146667783f84be2975337d3a99b5ac6162bb804c702aed729a67`  
		Last Modified: Thu, 17 Jul 2025 03:51:29 GMT  
		Size: 8.8 KB (8778 bytes)  
		MIME: application/vnd.in-toto+json
