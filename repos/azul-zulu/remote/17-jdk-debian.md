## `azul-zulu:17-jdk-debian`

```console
$ docker pull azul-zulu@sha256:1ea82b04a2c834ed93e7ae5e17e663a556020e9842f6c693484b8560beeabeb1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:17-jdk-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:7c4d622e4b4eb80746909506dbed97b4f7cdc3c21a28ae51b359863d87472246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182591474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b087d8ec524f5f339aeeec92be77222193234bc3b32645bca8a449ad6eb87c97`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:39:17 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:39:17 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:39:17 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.19-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:39:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Wed, 24 Jun 2026 01:39:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f86a953c949f1056afd77b8f0050447713f68a24f182343da552bda7e53450`  
		Last Modified: Wed, 24 Jun 2026 01:39:32 GMT  
		Size: 152.8 MB (152806055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jdk-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:510771788f3f077a5c4846b1542ee2ddb0563ffce9f6bbf92904dea8e4ff966e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84ffc2635306af2b0409d7ddc080a0d2fab588d603687c6e497afc4a708f29b`

```dockerfile
```

-	Layers:
	-	`sha256:13070d62d927a380c0e4fd7583505c9ce9855a170a6178964f0cd6e7e1607a40`  
		Last Modified: Wed, 24 Jun 2026 01:39:28 GMT  
		Size: 9.5 KB (9506 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:17-jdk-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:918ffc7bb42da99930d8351a664ec4d7ce786aad7d7e46a8e9aa521826a488ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (182968177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe7e6c90b538a3220ead93443c762ec32670cbfc591b05a92cdf160ee0b651d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:41:51 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:41:51 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:41:51 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.19-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:41:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Wed, 24 Jun 2026 01:41:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1667a6538e654df382871b14cc09d6c04c1d5a80a62c7482380499e75d82ede`  
		Last Modified: Wed, 24 Jun 2026 01:42:06 GMT  
		Size: 152.8 MB (152819626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jdk-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:0806331dda08749d0947edb9985d054523dddf457c1b268cf1fd9889f98bd565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf83e5d08301bb3fafbaf4e6a4dfda5c7377db975b82914276e159e5b343c8f`

```dockerfile
```

-	Layers:
	-	`sha256:1fd9f96f1bec804daa3521d3d78a4fd68fe0c7a5e74cb0bf0fd54626057dd299`  
		Last Modified: Wed, 24 Jun 2026 01:42:03 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.in-toto+json
