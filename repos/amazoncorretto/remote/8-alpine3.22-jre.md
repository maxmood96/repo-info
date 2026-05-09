## `amazoncorretto:8-alpine3.22-jre`

```console
$ docker pull amazoncorretto@sha256:2dea6ee48ac60a7f84f2f9bac260ddd64bc4c9bea9c470f5a79cb699b34056e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.22-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f0c0a7e43fed96e115cb796d5c341d4f7725fc1e5a88b99664bae85c4249fcdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45556257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed5b34b31cfdee162392b86a05adf47bf5e33e6dc220d5f98fb1867b23b3e9ca`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 22:58:24 GMT
ARG version=8.492.09.2
# Fri, 08 May 2026 22:58:24 GMT
# ARGS: version=8.492.09.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 08 May 2026 22:58:24 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 22:58:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a0fdbd1fc78c40824cd6af309385ffa81e313e7a8ec6f1e3983c5e1b9d8937`  
		Last Modified: Fri, 08 May 2026 22:58:34 GMT  
		Size: 41.7 MB (41748068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.22-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d4103d4685dfd369d8cc0605e6a22633c3c9e5c37f3dadedc9b1e88cff6fd499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.1 KB (197146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa0d320058044df1cd0d189c68e2ed7945e892bcf8204a3bb6021c8d5aebd15`

```dockerfile
```

-	Layers:
	-	`sha256:d31e7876239c8ad0bf0094cc8e8c1e890beedffc7e74e6d736d4cec3855f07e2`  
		Last Modified: Fri, 08 May 2026 22:58:33 GMT  
		Size: 188.5 KB (188490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7a250614189bf64b801e1e39da1a047c5aedace87f541bad143898eb2928b28`  
		Last Modified: Fri, 08 May 2026 22:58:33 GMT  
		Size: 8.7 KB (8656 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.22-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7116756a0909b3eaafdff3d664bee566e0ba88f7c259b4577c2ef9791a77f8cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45608674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea60e2736e17d5a62b42781795b067fa51949c976c75af190d8c25e9ea739686`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 22:48:34 GMT
ARG version=8.492.09.2
# Fri, 08 May 2026 22:48:34 GMT
# ARGS: version=8.492.09.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 08 May 2026 22:48:34 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 22:48:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8cff3925bc85c5073837dbde057868e5e710be218698f4f86531485acddbbd`  
		Last Modified: Fri, 08 May 2026 22:48:43 GMT  
		Size: 41.5 MB (41466780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.22-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:67873e3b97b183bd5d60c329a6579dc360a4ff8751052f6aba68a5446a9a2997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.3 KB (197334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8b74eccc54854b1f1c815de0f309396d7a257154b7c9c5c07e663294205844`

```dockerfile
```

-	Layers:
	-	`sha256:caaeb196817ba62ee93747c88616bc2a9b7de3b113597da56d8b5036aa212c70`  
		Last Modified: Fri, 08 May 2026 22:48:42 GMT  
		Size: 188.6 KB (188598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6962294ccf1ffd3efaac581a35113e57fe5ed43d35d7aa5c0013009fa8fee2cf`  
		Last Modified: Fri, 08 May 2026 22:48:42 GMT  
		Size: 8.7 KB (8736 bytes)  
		MIME: application/vnd.in-toto+json
