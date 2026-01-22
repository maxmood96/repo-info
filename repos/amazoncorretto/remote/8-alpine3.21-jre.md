## `amazoncorretto:8-alpine3.21-jre`

```console
$ docker pull amazoncorretto@sha256:9fa914dc49a6ea45162458f5e80cbc7c12e81ba1041886b900db21e083100c76
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.21-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bdc92987819de53f517527d315d3cbea0c4a926d1e2d9fe8ae49fe9677fef157
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45386469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:610da2ca1ce6adec0cb3d652737b33ff5e1196d6301791fabbed055b42f95856`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 18:59:30 GMT
ARG version=8.482.08.1
# Wed, 21 Jan 2026 18:59:30 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 18:59:30 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:04:22 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1cd6f9882a7aab608bf97d63ed0aa38a3c8f727c0ddcaf1703fd33d755dffd8`  
		Last Modified: Wed, 21 Jan 2026 18:59:53 GMT  
		Size: 41.7 MB (41743900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.21-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:df8e1574503839725f4a4011ab6307cdd55c72b17faa77ccd6356afff250f71e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.4 KB (197377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66d8e511014fde1c285480661e81c470bc58c361ec06d0ad130b3fb965d8582`

```dockerfile
```

-	Layers:
	-	`sha256:7c0cef571f948e33c6fb80b72a99b3cf472140f5462e7292d45466e673f36de6`  
		Last Modified: Wed, 21 Jan 2026 18:59:38 GMT  
		Size: 188.7 KB (188721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62784f42594ba4cc190cc73d266bb63bd8c8c6cd630e0ff1d298ea5595a7604a`  
		Last Modified: Wed, 21 Jan 2026 19:56:04 GMT  
		Size: 8.7 KB (8656 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.21-jre` - linux; arm64 variant v8

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

### `amazoncorretto:8-alpine3.21-jre` - unknown; unknown

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
		Last Modified: Wed, 21 Jan 2026 19:56:12 GMT  
		Size: 8.7 KB (8736 bytes)  
		MIME: application/vnd.in-toto+json
