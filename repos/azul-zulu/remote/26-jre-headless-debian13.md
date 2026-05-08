## `azul-zulu:26-jre-headless-debian13`

```console
$ docker pull azul-zulu@sha256:ea907784d9d7ee54508f1de73261c24e9a794759c7faa2d921d653abea2964b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-jre-headless-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:9c48dec9a5a2acec288b1aa4c74493521ac8974f5af754665cfa8ed0d1db9b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.9 MB (119912506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa9797ab47b3d5a3f7d766f3c6a89bb3df64d1b9b30d9a26f121655b4e08e47`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:40:17 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:40:17 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:40:17 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26.0.1-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:40:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d0552e64a7d887d0f70e165f709c95db5512250331aa24becab6cba8a7f729`  
		Last Modified: Fri, 08 May 2026 19:40:31 GMT  
		Size: 90.1 MB (90132280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jre-headless-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:8b8feeabd519fc318253772a996d9954472698c0070571ef8e481f59bbd9fae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53813fa24ed18ad8744b47e81ac06e1a4acc3e872df4ef8ecd08e28d14854a1c`

```dockerfile
```

-	Layers:
	-	`sha256:8a4b61a0575d86c9cce52569d6832e3e19a55fad72bbbdf542fa01c9da8414f8`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 9.3 KB (9298 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-jre-headless-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:96dbb67b86826492499afa8a347cd0985362a4673505f4ee534e91ffde7b4882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120202452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752a0c2c1d9037224ee07237af4bd4f7f20dc66c7afd9774d06b5af673ac0a8b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:42:27 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:42:27 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:42:27 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26.0.1-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:42:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38e3040ab5e48ae918a0d4456210927dee1ef75a96c14dd1ec8d00458ba5177`  
		Last Modified: Fri, 08 May 2026 19:42:41 GMT  
		Size: 90.1 MB (90058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jre-headless-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:2bc5f461283e0c7da4feb1be4fc0fc833f80f41fbc92eeef43aa0d1b35e4ff09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a32e1bcc1f898d15f914b012796fa260d78e3fef8b30b1dd10202f648b0426fe`

```dockerfile
```

-	Layers:
	-	`sha256:ac21c37fae9e60667af23a46584a841b4430c28b45cac13b00871bbacf8b16cb`  
		Last Modified: Fri, 08 May 2026 19:42:38 GMT  
		Size: 9.4 KB (9402 bytes)  
		MIME: application/vnd.in-toto+json
