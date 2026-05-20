## `azul-zulu:11-jre-headless-debian`

```console
$ docker pull azul-zulu@sha256:a0cea7fe636e6ee3af158cb5743401bb08d47efd268f64e977168c5031e26158
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-jre-headless-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:e2985a2e7dbd267226d2cebc0cde5564defdc219c67f1907560135272ca9c31d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94824541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8642d88b38c11e1f53d609abb90919c14f3979d722c01e8836a904882a0b9b2a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:20:06 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 19 May 2026 23:20:06 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:20:06 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.31-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 19 May 2026 23:20:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc1626a54c69919fa19474addb9d72c43febe2eccbb781177cd5c527147b773`  
		Last Modified: Tue, 19 May 2026 23:20:17 GMT  
		Size: 65.0 MB (65044615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:2f4be39eb4adc2d314a683988f0f29aee3992bdda9c4f0aa51f86828754f4f96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5054337fda95f7bfbf4ccafc2ad048fc25bd911b64ed3152585f06c247842814`

```dockerfile
```

-	Layers:
	-	`sha256:dc137c1fd16c577d880c00da782c1cfc42fd01e6c50b62e9ae338b58728779a5`  
		Last Modified: Tue, 19 May 2026 23:20:15 GMT  
		Size: 9.3 KB (9301 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-jre-headless-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:b1d921a67a2c00a8036c8bdad652984c9fdea0d0ea3d1b210996f97d5c77d903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95026135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ee4e80713be19a4505bdaa51e348d38511a47f190f7ffef32b187ca3e99efa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:23:57 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 19 May 2026 23:23:57 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:23:57 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.31-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 19 May 2026 23:23:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b529e2133fa5d1a16d2dd2509c51ee87dbfb130b63a7f2f93f82484671de39f9`  
		Last Modified: Tue, 19 May 2026 23:24:08 GMT  
		Size: 64.9 MB (64884216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:bfac7e2bf730a5db12f1419c7f87df569de2a51e62c114f24d98bb4f5075f3d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ca26fb15995bf41cca905676db8ab7843d37cc2f924953e9c137131b84d626`

```dockerfile
```

-	Layers:
	-	`sha256:579c40156057141893f103b9201a868d65c05567285b4b7b84472ded64745d36`  
		Last Modified: Tue, 19 May 2026 23:24:06 GMT  
		Size: 9.4 KB (9404 bytes)  
		MIME: application/vnd.in-toto+json
