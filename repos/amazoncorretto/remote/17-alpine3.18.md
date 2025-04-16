## `amazoncorretto:17-alpine3.18`

```console
$ docker pull amazoncorretto@sha256:ac8f23c3909e94c073bc16315ab471e6ee992cb6f2023cdb63d278ab6e94d847
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.18` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5798339b981df70e033ed151b0301d63d72f341015cfa86bbdd6a28c1b308199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149170770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6215839a01e7eb38e023f3d99cf2f59ee8008eb432fc384a55551e288c3179d5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:03:06 GMT
ADD alpine-minirootfs-3.18.12-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:03:06 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=17.0.15.6.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=17.0.15.6.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 15 Apr 2025 21:50:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:44cf07d57ee4424189f012074a59110ee2065adfdde9c7d9826bebdffce0a885`  
		Last Modified: Fri, 14 Feb 2025 12:05:05 GMT  
		Size: 3.4 MB (3418409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7605f0f0556f49f8e8892c4a88bac761763e2122eb68c13d2148e9e1c5de914a`  
		Last Modified: Tue, 15 Apr 2025 23:55:41 GMT  
		Size: 145.8 MB (145752361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3d24e03c09aef825a5bd606cbd89828f0f381cdef3cd8cd3a6142a4f1bfe4438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.7 KB (389651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd813d8a3a3871b3756ddcab685556275b0959b0d4a528ccb003658059635e0f`

```dockerfile
```

-	Layers:
	-	`sha256:567b44b9443e2de9d9481c2875be9c9ddb11c3fd395c8f8d99f38a821316a6ab`  
		Last Modified: Tue, 15 Apr 2025 23:55:38 GMT  
		Size: 380.2 KB (380234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f456282ad450d0e14d85afa892970e17f9c5520ab491d2dff5247f6bc0e6e225`  
		Last Modified: Tue, 15 Apr 2025 23:55:38 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5a9aaa33501518c8cc45ca57bca6cc8d544a67eca568acadc707e7e0ebc075ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147364395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:052f03a942327a3467b346bbe0f1ccb3aede6d9572bb26634cb5fed2d9769bcc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.18.12-aarch64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=17.0.14.7.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=17.0.14.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:95459497489f07b9d71d294c852a09f9bbf1af51bb35db752a31f6f48935e293`  
		Last Modified: Fri, 14 Feb 2025 12:05:04 GMT  
		Size: 3.3 MB (3342657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66991c9dda9302218c2cbbbdbc324ea14868d009ecdd595f9f398feec1998cdf`  
		Last Modified: Fri, 14 Feb 2025 22:36:09 GMT  
		Size: 144.0 MB (144021738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:06e58a98bdc29424dfcc028d78f45a00e261f6359fb91f4d38d8d666ec975b0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.2 KB (389174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce639a75bf33b2505aac5d3d7dc9fee640e298e8ecd25d87c3b3622e44fd3ce`

```dockerfile
```

-	Layers:
	-	`sha256:c94ed8d7b9b00e9afee02f1a2570a94f73cab3dbadd584fc60bc0eee04246fdd`  
		Last Modified: Fri, 14 Feb 2025 22:36:06 GMT  
		Size: 379.7 KB (379653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ff1437c25202e0393a960bbba0040086acb504d5d5a9ced35e8e74c70072c32`  
		Last Modified: Fri, 14 Feb 2025 22:36:05 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.in-toto+json
