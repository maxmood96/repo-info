## `azul-zulu:26-jdk-debian13`

```console
$ docker pull azul-zulu@sha256:86a5fb3f5fff34655f1ff70ccd9a30bb49758b4a90518f2a560b08dc46e28928
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-jdk-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:2d5d20db0be30a154bad4f2af92a907d9cc6895cb85ba9041c01ff58f4981686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 MB (217226223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ba00b1e9e93abe5e883822f194672475e2a0de05b3d695ee238f6ff5e14faf`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:38:43 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 22 Apr 2026 01:38:43 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:38:43 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26.0.1-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 22 Apr 2026 01:38:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Wed, 22 Apr 2026 01:38:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed4523d06752d349730dd3cdbbe350648fc94421e15eff843c04479e663edf67`  
		Last Modified: Wed, 22 Apr 2026 01:39:00 GMT  
		Size: 187.4 MB (187446049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jdk-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:3126a32951631868cb9e631fce37e4e3e18bae0d7337f092c9bd41cc5af77cbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1081ed7a27221f56abcaba6a9af0727893b5ff566003244b5cdbd9291bfa279`

```dockerfile
```

-	Layers:
	-	`sha256:bfc68184aa8eb37060d7049984a2df98256aca8cfb04f63276e4af8ba98fba27`  
		Last Modified: Wed, 22 Apr 2026 01:38:56 GMT  
		Size: 9.5 KB (9504 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-jdk-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:0149160e9474627d5d69d727131f201c905dd754676d78c3159b1bc2d87a9e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217271156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f91728b0bad620c60391e4f35bf0827644e39ef5fcf1a103bcfea5f3a360e36`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:42:49 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 22 Apr 2026 01:42:49 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:42:49 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26.0.1-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 22 Apr 2026 01:42:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Wed, 22 Apr 2026 01:42:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41352d892a8a93f957d7a1e331a1a16f5a2d03efa20781977cd506f49f20e6c0`  
		Last Modified: Wed, 22 Apr 2026 01:43:09 GMT  
		Size: 187.1 MB (187127550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jdk-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:c4f3fa9f3634eee6705b22898b99d1ab71aa9799b041bbf31b2346810296a69d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7e09ddfb4caeba92fbc65537d972a0f7c0dd4cf534b74649516aef38655319`

```dockerfile
```

-	Layers:
	-	`sha256:1d2c1efd12c3ddb2cf09ba7b7936bb3ecb74ab5dd7cce389c16acb9192eff5a7`  
		Last Modified: Wed, 22 Apr 2026 01:43:04 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.in-toto+json
