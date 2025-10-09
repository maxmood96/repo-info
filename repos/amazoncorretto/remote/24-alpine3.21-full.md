## `amazoncorretto:24-alpine3.21-full`

```console
$ docker pull amazoncorretto@sha256:79a172166e3ddd7019f60c2b197808ec36a05e63e479d1ce8f499e865377d7f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-alpine3.21-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4ef5a173fc5064f7b220baeed08c8f0f4c2fe5c337b6b3dd123f7e39a24ac7f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.4 MB (180413141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47019acd1ab8e83360719069f2661a77345f1860b2738c002af2a18d29553e36`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=24.0.2.12.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=24.0.2.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-24=$version-r0 &&     rm -rf /usr/lib/jvm/java-24-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b061855b6fa56dbf8ee611acfb76015149db3105569ed51735b27f8d81f5006`  
		Last Modified: Wed, 08 Oct 2025 23:00:43 GMT  
		Size: 176.8 MB (176770572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-alpine3.21-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6f92301ba2e9f4c5fc56001ef185a2a5d5e2db1b3194dfabe3bc4f960cbba5b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.4 KB (402388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:277722b4c58e78c5c82270c49aa8e70ddfae81b9f3ceec7e042391e2f7e77d51`

```dockerfile
```

-	Layers:
	-	`sha256:b80f3f9c2192ae9df9e5e7bbeb6b3b397377d2ac9630c09e4189803403b1116c`  
		Last Modified: Thu, 09 Oct 2025 00:51:13 GMT  
		Size: 393.0 KB (392973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f476f074d622282650f5737ab6d3e5bf88da7f2538f72acbf23dc5f9a38ad63`  
		Last Modified: Thu, 09 Oct 2025 00:51:14 GMT  
		Size: 9.4 KB (9415 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-alpine3.21-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f71c90287d1c546c9453ffd1deec51475b70725b06a50817a5b6b8971962e57d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178509696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50de8b9a203be1548023e8486c692af7bb5d36bfa359fc4bc4ecd38a488cb3ab`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=24.0.2.12.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=24.0.2.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-24=$version-r0 &&     rm -rf /usr/lib/jvm/java-24-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ae72cd4c3976c9885e9d878d32fe8a100880d41d7969e2fec73f7f4c23bdb5`  
		Last Modified: Wed, 08 Oct 2025 21:47:53 GMT  
		Size: 174.5 MB (174517343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-alpine3.21-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:66c73d044e07358e97ee620772eac34b11a60a5a64e6715261ae20c342796a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.9 KB (401908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50fefe3d2ad5a5b42943a6259f8d698cd1cd0908bc3374bd73cee9949525ecf2`

```dockerfile
```

-	Layers:
	-	`sha256:4f93a15cb801f6c278eb282ee1916cc09314bca4570eaeb759534aa85776678c`  
		Last Modified: Thu, 09 Oct 2025 00:51:17 GMT  
		Size: 392.4 KB (392389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2ec5532596f16fb0852a2b8e15074306273b145c27533a3c73f1ae90cf2f07c`  
		Last Modified: Thu, 09 Oct 2025 00:51:18 GMT  
		Size: 9.5 KB (9519 bytes)  
		MIME: application/vnd.in-toto+json
