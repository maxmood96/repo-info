## `azul-zulu:25-headless-debian13`

```console
$ docker pull azul-zulu@sha256:e7de6508d4ea8c0ef7f84d28a4efe289e01fdeb7e885c8d11aa0921c5e3866fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:25-headless-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:55871475bee67d68cd14cd969a5ea4e53b10b8ebb0e59dae261901e4f5e2576a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.7 MB (212683770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3fbfec7d6d9035ed11d06e4bc1dd22882a178df0e189962a8b07c467d97a0d5`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:46:29 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:46:29 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:46:29 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.3-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:46:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Fri, 08 May 2026 19:46:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb12d5a333d3a962ff0b4f487599bc2b3b10b366b21d56c6e97115376e748d9`  
		Last Modified: Fri, 08 May 2026 19:46:48 GMT  
		Size: 182.9 MB (182903544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-headless-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:24d18a704ba627a98b89cf1543d9b3be008373aba78c528e48316bacca9aa62c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f55012711a32c97eec32b38b3ab1585e9b17536f137adcc8f6880ede07f2348`

```dockerfile
```

-	Layers:
	-	`sha256:215362276a0fc87b81e09bfef42a1887f0311d98d725a30e657f17b0f4eecdda`  
		Last Modified: Fri, 08 May 2026 19:46:43 GMT  
		Size: 9.3 KB (9295 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:25-headless-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:ed6dcc3124f76fac2f729f72d1e93dcc0c4a888d0e36a5375d2bd3539019ffb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212197338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7967a3b6d34b0e7dacf076455a43d4052184908d0e84db080828e3d89237f7d5`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:41:47 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:41:47 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:41:47 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.3-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:41:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Fri, 08 May 2026 19:41:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d7b0dc8200d0a75ecee80a1f0006109259384db880f88d9c8532142643ff55`  
		Last Modified: Fri, 08 May 2026 19:42:06 GMT  
		Size: 182.1 MB (182053696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-headless-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:07e15a63795d9c1c41cb6d13e517299a28580ffc41dfb234b7010b73e1139714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b698bf3bc26286528fc7af485b8e0b49f1ec64f8775ad5bb6180bac3fd5e32a`

```dockerfile
```

-	Layers:
	-	`sha256:13918e88b5a63352d13285cedd8b3998a790dfaa585bc2d5fb9f0a0c578bc6ca`  
		Last Modified: Fri, 08 May 2026 19:42:02 GMT  
		Size: 9.4 KB (9399 bytes)  
		MIME: application/vnd.in-toto+json
