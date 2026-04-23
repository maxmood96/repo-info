## `amazoncorretto:8u492-alpine3.21-jre`

```console
$ docker pull amazoncorretto@sha256:0507fc1f3491a4788ae5f13d9bb0e234ffca349d92724762dae17d15b3a312f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u492-alpine3.21-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a385089023b9b4d3db257323ea68a9daf6ca8588351b7f483704cbfc707fff86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45404789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5652b0b4a125f25cd81455df77818f546615a14039b5f1ee218c32b8180d30ad`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:32:18 GMT
ARG version=8.492.09.1
# Wed, 22 Apr 2026 21:32:18 GMT
# ARGS: version=8.492.09.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:32:18 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:32:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e9d7714c203cea2108aca52423de90adaddf5f9b615de86ffbe4fde9070cdb`  
		Last Modified: Wed, 22 Apr 2026 21:32:29 GMT  
		Size: 41.8 MB (41757914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-alpine3.21-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a87d79fa10a417f9bc8a24911895ee52601b1ef3941705bc0b71861f8d41ad6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.4 KB (197381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c919146129312eeae72e65d75de513e7275a36bf41fe197a07d138e64fdeccf6`

```dockerfile
```

-	Layers:
	-	`sha256:dbf47cd68906507d978d6455d8341e4a2def1f95673d8c190b9990533249f540`  
		Last Modified: Wed, 22 Apr 2026 21:32:27 GMT  
		Size: 188.7 KB (188725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a57fac95560e9b4139099154269a6a10b30ff7b2b68e1bbdf089a01c404b9aab`  
		Last Modified: Wed, 22 Apr 2026 21:32:27 GMT  
		Size: 8.7 KB (8656 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u492-alpine3.21-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:bae828a7a93f236ae334626e02f1e1e98dda3f9420be842b773eee4c385dc82e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45457176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:240468c67ae36f041da08dcb4467968efb5ded42c1c9e9e1f1ca83ddd3aff29d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:13 GMT
ADD alpine-minirootfs-3.21.7-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:13 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:33:09 GMT
ARG version=8.492.09.1
# Wed, 22 Apr 2026 21:33:09 GMT
# ARGS: version=8.492.09.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:33:09 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:33:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:2dd7199cff98a7400e801cbfad6de906972a4e3dd0a749d4c1b80f5a1e3e4108`  
		Last Modified: Thu, 16 Apr 2026 05:32:50 GMT  
		Size: 4.0 MB (3994465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ce646d724e6922be21c108e9b8bc0cfca47490b54c74733336773fad45fc27`  
		Last Modified: Wed, 22 Apr 2026 21:33:19 GMT  
		Size: 41.5 MB (41462711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-alpine3.21-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fbd1f814cefcdf137e527044bd2e2a1c7183012360b67a5c5f144a4528da861a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.6 KB (197568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7c207b82699602df939946ce7443daf2eb527a712c7c5b1869b017e57970a5`

```dockerfile
```

-	Layers:
	-	`sha256:cbfaba8b1348487110c370b03b8ea3cb035d9c3fcd998d9cd6742416104d47e2`  
		Last Modified: Wed, 22 Apr 2026 21:33:18 GMT  
		Size: 188.8 KB (188833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd5a8c644a937f2d8ddbe03f700717cb656652404a98a061079886cb2f49024`  
		Last Modified: Wed, 22 Apr 2026 21:33:18 GMT  
		Size: 8.7 KB (8735 bytes)  
		MIME: application/vnd.in-toto+json
