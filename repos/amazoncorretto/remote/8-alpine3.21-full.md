## `amazoncorretto:8-alpine3.21-full`

```console
$ docker pull amazoncorretto@sha256:775d9a2a56eead2f329711f0d6411a4a45035ba1093aa5bf24c971776b281f96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.21-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bb309f29cb6ad1455bafd6a87ec715bb584a2a801679d9bdcac09752a4b18df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104418594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b1297a4da125809ae643feb3dcc496b97248127ab8f1725fb3120db85735b7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 18:58:33 GMT
ARG version=8.482.08.1
# Wed, 21 Jan 2026 18:58:33 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 18:58:33 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:58:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 18:58:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Sun, 07 Dec 2025 13:55:07 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e9c9a984760ccb18b0ae51ba3361d277e98594640470ca92549b5e4e182d26`  
		Last Modified: Wed, 21 Jan 2026 18:59:07 GMT  
		Size: 100.8 MB (100776025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.21-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8deb0d0527f880409b99575a3ffe9dd6270a898ec43fee43968f550fbd604084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 KB (260283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35984db494a8938b6c34048ddc40d2129a0fce92feb26cb91fa78d5bf791c482`

```dockerfile
```

-	Layers:
	-	`sha256:78c147c4430fe7732f8587eb812362a162a4d52126ec815fd2a042b4b1c97c85`  
		Last Modified: Wed, 21 Jan 2026 18:58:44 GMT  
		Size: 250.9 KB (250929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92a561a039c9176912048f82d25e39a5e5254637f50c7171fb90bd507e430534`  
		Last Modified: Wed, 21 Jan 2026 18:58:44 GMT  
		Size: 9.4 KB (9354 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.21-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:61594956d29ff1b2408e813797c2fd16db98b79e0a6a3b7a021e38b59553a9a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104554480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61403ac3e297e4ed37cce4bba47bc5d7dc1a70cb17f9fb621e9b171778ccdd45`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 18:59:36 GMT
ARG version=8.482.08.1
# Wed, 21 Jan 2026 18:59:36 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 18:59:36 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 18:59:36 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Sun, 07 Dec 2025 17:54:48 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8287577c4a7194af2c0ef35b314ff44a5bfa82311ee4623c6fd7dac830aa458`  
		Last Modified: Wed, 21 Jan 2026 18:59:50 GMT  
		Size: 100.6 MB (100562127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.21-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f6aae130d36b03e9dd1a928ac602ecf15bd32270e224bab3b9612be1fa051b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.5 KB (260518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88fa678cbbed7a7153f51fae0a9efd19f9d7905e4227d800def3a5480b0faee8`

```dockerfile
```

-	Layers:
	-	`sha256:5715c95ddae41e62357cc1559a8f24000d60de7bfc6909d324074e91f0c04865`  
		Last Modified: Wed, 21 Jan 2026 18:59:48 GMT  
		Size: 251.1 KB (251061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88fb883443ce73680ba3e237ae8dbc5d8fe070b89618125702d62ad184fcb657`  
		Last Modified: Wed, 21 Jan 2026 19:55:59 GMT  
		Size: 9.5 KB (9457 bytes)  
		MIME: application/vnd.in-toto+json
