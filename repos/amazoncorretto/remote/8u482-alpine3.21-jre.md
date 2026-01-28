## `amazoncorretto:8u482-alpine3.21-jre`

```console
$ docker pull amazoncorretto@sha256:996b23c27942b0b67b9169e9d2903d3439cf5c3a372a7e9064f8c2bc30035503
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u482-alpine3.21-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:91be468fa22a70c7f6d80b26c99adad349693aa16d40a3d14d9738f77ba4c2b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45387712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ec19c3f3c6eaef43f6ac844032a689c8e7712738af28c11c032d95beae1e9b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:41:36 GMT
ARG version=8.482.08.1
# Wed, 28 Jan 2026 02:41:36 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:41:36 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:41:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9423c2e63b810fcde874737d818a4ef23f7253921aa23ad8c0b0099673b24b7a`  
		Last Modified: Wed, 28 Jan 2026 02:41:46 GMT  
		Size: 41.7 MB (41743970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u482-alpine3.21-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:73d6712020ede3444a4538bf8a1e683b41f3df5ba8da9f23017ea835147bac3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.4 KB (197376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43eebb37691422ffb082896377ab718998b65679d94a5fe540bb91898912e03d`

```dockerfile
```

-	Layers:
	-	`sha256:573a9a36b5e268b5b47457a87868f03d599a26c73e0f91ea54cd845ca7f2b786`  
		Last Modified: Wed, 28 Jan 2026 02:41:45 GMT  
		Size: 188.7 KB (188721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2896af1729d537bd2e69cee0d398517d1b19ed800ba50646ed1dea46f755cde`  
		Last Modified: Wed, 28 Jan 2026 02:41:45 GMT  
		Size: 8.7 KB (8655 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u482-alpine3.21-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ba1b7500b5ff4c36536954159f8ec4b3284fb2098a68f852dc94b794c9032587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45448796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3d00b2d280c23992248f78aa1e6aa324d369499e81a2eed1df16db1a15df42`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 18:58:39 GMT
ARG version=8.482.08.1
# Wed, 21 Jan 2026 18:58:39 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 18:58:39 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:58:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 12:04:23 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4d8e0dc972f3dd95ea0bf783568c920358e0022918ba16a26a504c41b73e67e`  
		Last Modified: Wed, 21 Jan 2026 18:58:50 GMT  
		Size: 41.5 MB (41456443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u482-alpine3.21-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b89c636f2e286f7f33f24ee78a559d8b12b50a26056f5cbdc31c3303179db240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.6 KB (197565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1961f90066c769d2a59c0ad95de78a4abdcedbb60e1e368f828e40b05360463c`

```dockerfile
```

-	Layers:
	-	`sha256:978785032383c3bd203249436ed980965f82478a942155387667f8210f1a84fc`  
		Last Modified: Wed, 21 Jan 2026 18:58:49 GMT  
		Size: 188.8 KB (188829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75929976891216ab61444665628933ade8ac7262c355788b4ccce7cd4ba18bf7`  
		Last Modified: Wed, 21 Jan 2026 18:58:49 GMT  
		Size: 8.7 KB (8736 bytes)  
		MIME: application/vnd.in-toto+json
