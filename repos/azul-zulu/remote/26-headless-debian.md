## `azul-zulu:26-headless-debian`

```console
$ docker pull azul-zulu@sha256:198b82a3fa6eb74555434e41dc8d5882c31ad0449b9efd148ee0fe5c315107bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-headless-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:4d7773aeb5077ed66982386dac2b9a0f9b2a6bca7e43b04aee45c6d9a67d3e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.0 MB (215021054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52773e453282b3e889f5b0731d5376b18e71ed0bfa9d0f39b364994ab14423bd`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:39:07 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 22 Apr 2026 01:39:07 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:39:07 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26.0.1-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 22 Apr 2026 01:39:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Wed, 22 Apr 2026 01:39:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0012a688890f6f462298e13766e735f6c46dfa8d8c500bd7d9813629da84a6`  
		Last Modified: Wed, 22 Apr 2026 01:39:25 GMT  
		Size: 185.2 MB (185240880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:ad9329b4f7af2ac124d236168fd96c575d43253881d08d6720240bf08f782eb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac4ab293cb19e11aab3262487f608981e09a46962a924704db498b8c822f4d9`

```dockerfile
```

-	Layers:
	-	`sha256:e9f849c47ac3490ba8251567d6c77f8f84c58f5fa19cb16e08dfc9db4b94a25a`  
		Last Modified: Wed, 22 Apr 2026 01:39:20 GMT  
		Size: 9.3 KB (9295 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-headless-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:8b1f719209da51a21e855717a33b621646cd45330108b41477edbf0ab2b8fb79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.1 MB (215090061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44953c94bf99f5ec11686834d831dd0ca7e7223297d955fb607973e2927c7268`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:42:53 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 22 Apr 2026 01:42:53 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:42:53 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26.0.1-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 22 Apr 2026 01:42:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Wed, 22 Apr 2026 01:42:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2346255dc148cb2a6e737935e36a14eddd564c7189e71d5f818019bb32c4cddd`  
		Last Modified: Wed, 22 Apr 2026 01:43:12 GMT  
		Size: 184.9 MB (184946455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:5953faf89250594846f2e1e6f487f50b063bee92c7daf009c79c3bafd047fbde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494bc065ffdc84e8ccc64cb3356e2a71be116f23b5374ec086114b800af1a733`

```dockerfile
```

-	Layers:
	-	`sha256:54a7b125eca9e9fad22a55af7feb2a422cdf2f73963e7414d413cf428c988da5`  
		Last Modified: Wed, 22 Apr 2026 01:43:08 GMT  
		Size: 9.4 KB (9399 bytes)  
		MIME: application/vnd.in-toto+json
