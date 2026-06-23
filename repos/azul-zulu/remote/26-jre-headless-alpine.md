## `azul-zulu:26-jre-headless-alpine`

```console
$ docker pull azul-zulu@sha256:b34bfa7ed26bc119192be270654eee42e8757c59b4b2ce3416791326958c8e5b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-jre-headless-alpine` - linux; amd64

```console
$ docker pull azul-zulu@sha256:37d30b91d3ad549f98082aac68b3f35be94f14bdf99068de5cb6090f40882c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88739380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f11894f4d1a0607e1cfb2f7d42fe2bfa9579ef484334dc28812b4e5ff5d0a13`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:56:11 GMT
ARG REPO_HOST=repos.azul.com
# Mon, 22 Jun 2026 19:56:11 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:56:11 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu26-jre-headless=26.0.1-r1;      java -version # buildkit
# Mon, 22 Jun 2026 19:56:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Mon, 22 Jun 2026 19:56:11 GMT
ENV PATH=/usr/lib/jvm/zulu26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d5567c017df2e47d8bf0900746156819167bf42aa00a9a505dd0546837e856`  
		Last Modified: Mon, 22 Jun 2026 19:56:25 GMT  
		Size: 84.9 MB (84894959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jre-headless-alpine` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:39366e9f68cd67737e10b529c6354bc25f0dcad10e3c949aaf18aafcb02d6b38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 KB (7573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4f693765c21f2f9f0e6e0c5c52d0b61357146ce3651132f5950fc983319772`

```dockerfile
```

-	Layers:
	-	`sha256:172b39e31ca832ce015866f856b2caf1e26b4db5bfeea1048c657f0546571915`  
		Last Modified: Mon, 22 Jun 2026 19:56:23 GMT  
		Size: 7.6 KB (7573 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-jre-headless-alpine` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:6b2659ac2f48d3d3ac0584b60d88ceeb26b3870acabecb8a4820b8e0bb2fa549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.9 MB (87859285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03e8c75a0f6a86cc5b69a663a1a4bfed0a598a40b3c44431cae387d68a5e302`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:57:52 GMT
ARG REPO_HOST=repos.azul.com
# Mon, 22 Jun 2026 19:57:52 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:57:52 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu26-jre-headless=26.0.1-r1;      java -version # buildkit
# Mon, 22 Jun 2026 19:57:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Mon, 22 Jun 2026 19:57:52 GMT
ENV PATH=/usr/lib/jvm/zulu26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c5bed5b2edd688305c28bc6b13ce5229e2ca09b9141d4274861c5c9a348e9e`  
		Last Modified: Mon, 22 Jun 2026 19:58:06 GMT  
		Size: 83.7 MB (83677425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jre-headless-alpine` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:1b9298b995cf1db9d3bf90888301e9f055be53525c474f043e05deda41395f70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 KB (7665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7650743f899936f31a21702b410a8a3de0041aa1ded5857d6674795b4eaa58b6`

```dockerfile
```

-	Layers:
	-	`sha256:d50de17a47ffee56f882b4f5c8e66cf7ea68bf90d0060989630d02ebe2f28455`  
		Last Modified: Mon, 22 Jun 2026 19:58:04 GMT  
		Size: 7.7 KB (7665 bytes)  
		MIME: application/vnd.in-toto+json
