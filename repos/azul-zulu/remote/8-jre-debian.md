## `azul-zulu:8-jre-debian`

```console
$ docker pull azul-zulu@sha256:1fee99e98112171759402996ed1e034acee0915046f085313c47f89aa3182466
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:8-jre-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:1ab452191ebed5054b528ea5c01a843a064c80d339584b3d66a2a1ff134cb935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79617915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e8a1256b659f114e2d6b5f9e0667db09dfe7a432f1fea69928f3d3e8cd2f4d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:37:51 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:37:51 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:37:51 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.492-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:37:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a8d0770171fdf17b5e16171608e7b5fb87a46035d1a7ebbad9d9ed532bb039`  
		Last Modified: Wed, 24 Jun 2026 01:38:00 GMT  
		Size: 49.8 MB (49832496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jre-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:974aa4e6cbfbdc63c6e2788acd3452cd8e86bbaa78f26524ba5d7917a32ed46d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9939a84114a876ebb850ab79b655c9acfedcbbb77d1a819ff7cfb0016ed0d7`

```dockerfile
```

-	Layers:
	-	`sha256:36088b852afcc8dc5f6e87679c58838d6bf5202e08dcd46191c06dc276ef0f5f`  
		Last Modified: Wed, 24 Jun 2026 01:37:58 GMT  
		Size: 9.2 KB (9173 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:8-jre-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:07b5e606989f79166c4664bae6f20b43867233ea87f8def3224593319a843edc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.2 MB (80203834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1be7df5d31f8879e2d6f5e75e313c79ccf54287c3e0dea35be3acd1d6f2b037`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:39:46 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:39:46 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:39:46 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.492-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:39:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23ef721f851ce113eeaa4d65cfba186362fb03827963512f961a80c6c447a22`  
		Last Modified: Wed, 24 Jun 2026 01:39:55 GMT  
		Size: 50.1 MB (50055283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jre-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:9b42208dd1e17296a7b181d05e1ef7486b77bd6f82b5abd1bd71599d42429736
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4573bb66bc71662f8166bb715a732c54ae8c842d49b6dbd65be45d15fd2fb7da`

```dockerfile
```

-	Layers:
	-	`sha256:4091c9b412d1a2bfcf64f8ae487f1beb364e69408cc7fa20321b933feb693144`  
		Last Modified: Wed, 24 Jun 2026 01:39:53 GMT  
		Size: 9.3 KB (9277 bytes)  
		MIME: application/vnd.in-toto+json
