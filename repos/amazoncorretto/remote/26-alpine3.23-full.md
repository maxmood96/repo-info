## `amazoncorretto:26-alpine3.23-full`

```console
$ docker pull amazoncorretto@sha256:e40abccb9631d250749a0e65446349e97c3b51e6e3d8f73e5d3cad6e8b0bbf17
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-alpine3.23-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2ea36c2821ffba8ea9d77b67376bd5a03d561a148f3c61229a0912bcfd76a2b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188776232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a10f492a3cc94789bf83b32574c02cfea714b6443c9820f9d1c131c0a1ddeeb7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:54:38 GMT
ARG version=26.0.1.8.1
# Mon, 22 Jun 2026 19:54:38 GMT
# ARGS: version=26.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-26=$version-r0 &&     rm -rf /usr/lib/jvm/java-26-amazon-corretto/lib/src.zip # buildkit
# Mon, 22 Jun 2026 19:54:38 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:54:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 22 Jun 2026 19:54:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbcea47f9704473ca3b9ca00d4e15e2a4ff11f52c426aa9e33981aa772fb2bb`  
		Last Modified: Mon, 22 Jun 2026 19:55:00 GMT  
		Size: 184.9 MB (184931811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-alpine3.23-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:642b065457530b8e9e81ab8eb6e83df405aa93d47f46c5a1ccf07c3bcad6464d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.7 KB (595684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7e8dce35a820d744460c3f337d25cf98ddaaa90939fd7826f67c9a2d02d9c9`

```dockerfile
```

-	Layers:
	-	`sha256:5c09245ba5e082135a5a72ed11232cb597a319a2e12f3f03e98881b2e79b4f04`  
		Last Modified: Mon, 22 Jun 2026 19:54:55 GMT  
		Size: 586.3 KB (586313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5470ad61331ca8f8947879a5b9d8629b4fc4cbefd3cb56493d82849c5fbeab6`  
		Last Modified: Mon, 22 Jun 2026 19:54:55 GMT  
		Size: 9.4 KB (9371 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:26-alpine3.23-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b42dfc43fd2a543791e736c47f900586aaddd86c3767474b547e29df45ec3452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186685923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7be0d4b4429c176a70a51eaa965f3beb8294e1374110b5a88201d7927514ed4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:56:11 GMT
ARG version=26.0.1.8.1
# Mon, 22 Jun 2026 19:56:11 GMT
# ARGS: version=26.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-26=$version-r0 &&     rm -rf /usr/lib/jvm/java-26-amazon-corretto/lib/src.zip # buildkit
# Mon, 22 Jun 2026 19:56:11 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:56:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 22 Jun 2026 19:56:11 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e61214fd6086c28ba823c9ab0c1f647315b6be9ec783415f5df8e9eeba7f2a0`  
		Last Modified: Mon, 22 Jun 2026 19:56:34 GMT  
		Size: 182.5 MB (182504063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-alpine3.23-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0cc3c3c93a50f3aff7beb0d6ac64bdb5ae6d76ffa90ee9c5a87f542dd857cf56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.6 KB (594554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f40d9c0dca1fa2f73de8d15d04a4261c42be10cd31b84fb7d6d55b4a1373aa`

```dockerfile
```

-	Layers:
	-	`sha256:16ee150838f430bf74751d9f65ab03cf1eac32b647a63c62bd9d3ce15292c28b`  
		Last Modified: Mon, 22 Jun 2026 19:56:29 GMT  
		Size: 585.1 KB (585079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f58b86fdb2b9d84814a38122a0391d052a1164918c998f5f742e0a6aad6b7be5`  
		Last Modified: Mon, 22 Jun 2026 19:56:29 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json
