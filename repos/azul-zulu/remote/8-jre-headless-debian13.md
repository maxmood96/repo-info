## `azul-zulu:8-jre-headless-debian13`

```console
$ docker pull azul-zulu@sha256:6db4f84b54033eb92b5650e74f3b660c68070df34b16ed9ed270a8c592e71a8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:8-jre-headless-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:d65f425e0b64d83cc9292fea2ea6abd263e7fecf1114512c2a3be0136beadf42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77512895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6afb4be805e756b4be455cb8b2822d22ad002ec99f1e73fab1be3a22cf14c137`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:38:24 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:38:24 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:38:24 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.492-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:38:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de3640de4d664370210e92d99682adb8b675d9d0595bca547e17a990a022f55`  
		Last Modified: Wed, 24 Jun 2026 01:38:32 GMT  
		Size: 47.7 MB (47727476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jre-headless-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:20cea2a59463e7d797edd0f0af611d940ac9c493b0b3c11307ad55d786fed6c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980332221a5166ca3556be98271fb316c01ca6a3a098b5b5bed744d722ad7a39`

```dockerfile
```

-	Layers:
	-	`sha256:7220cf5c0efdb07ef6602919dcc502412dd7aa489257eafcde289312a1a82211`  
		Last Modified: Wed, 24 Jun 2026 01:38:30 GMT  
		Size: 9.3 KB (9285 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:8-jre-headless-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:7622946dad279a18021b7e95dfce3386d04ba20b305aa308a28dc8facd2959d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78100289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe2f158f7d1355bc9577141c59510d5b3ecb85951e28f7dde59a97e49df8f05`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:40:07 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:40:07 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:40:07 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.492-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:40:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677c8d7c71e714fae64ab50fb517b1ae46d6db35fb859a6e75c9631b27bb2b5b`  
		Last Modified: Wed, 24 Jun 2026 01:40:15 GMT  
		Size: 48.0 MB (47951738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jre-headless-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:833f202b4c46c90138968e4a3992bb89bee73aa5bb1b42e7d458ac2d6190eb10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81bfbbf2d078fb198502fcc9e8b53c0b57876feae8502bf3c6020e9a9d9a5c88`

```dockerfile
```

-	Layers:
	-	`sha256:993c85eef9978b310e53a547998b667c147dac10a3d994a9471b41d9f7b47207`  
		Last Modified: Wed, 24 Jun 2026 01:40:14 GMT  
		Size: 9.4 KB (9389 bytes)  
		MIME: application/vnd.in-toto+json
