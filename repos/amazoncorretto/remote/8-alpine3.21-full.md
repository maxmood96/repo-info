## `amazoncorretto:8-alpine3.21-full`

```console
$ docker pull amazoncorretto@sha256:f0c515ecf23aa0e419a4765fa2bd37a070a5ae1bcf4d12398c8f2077ce8dbd4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.21-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8edbc8db43b21f99fa4f5a61476ff6057780177b610a9571b417c2c4c700821e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104419834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8dc831f4bb6b9cd97cc5de6b4cdc3e1ed5144630b8a5424d1d46895516ab9e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:43 GMT
ADD alpine-minirootfs-3.21.6-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:43 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:40:58 GMT
ARG version=8.482.08.1
# Wed, 28 Jan 2026 02:40:58 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:40:58 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:40:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:40:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:bc1da058f299723f8258c5a82dd007d1dd72e275087b726d5e1be5ef6198f286`  
		Last Modified: Wed, 28 Jan 2026 01:18:49 GMT  
		Size: 3.6 MB (3643742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad04cce4ac51c398476b4cf4bf77aa6a5a031730dba4e828e1ef8d9cf034194`  
		Last Modified: Wed, 28 Jan 2026 02:41:12 GMT  
		Size: 100.8 MB (100776092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.21-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:958f5e428666fe2a843a3c43d208c3aa1f39e80053f9ca47f6f0a09c9e023b48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 KB (260284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a8583f185eb8024c014ca8a7263cc33fc5cbb33e36fe30cb2b605b454a8885`

```dockerfile
```

-	Layers:
	-	`sha256:d57ac12f16182b5508155d5ba36b8be4e307a1d4dbc4b6d150d2f31d0c19cab2`  
		Last Modified: Wed, 28 Jan 2026 02:41:10 GMT  
		Size: 250.9 KB (250929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9a50a84409bd1e438abbea2bf0c0fadbdf030b9329b8d4f64a6210aeb95b1e9`  
		Last Modified: Wed, 28 Jan 2026 02:41:10 GMT  
		Size: 9.4 KB (9355 bytes)  
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
		Last Modified: Wed, 08 Oct 2025 12:04:23 GMT  
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
		Last Modified: Wed, 21 Jan 2026 18:59:48 GMT  
		Size: 9.5 KB (9457 bytes)  
		MIME: application/vnd.in-toto+json
