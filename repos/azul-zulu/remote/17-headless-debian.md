## `azul-zulu:17-headless-debian`

```console
$ docker pull azul-zulu@sha256:44ce737a8091f1498e57e1a9fadad6ba434fda29c3a838b97c6ddad7794995f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:17-headless-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:3f1eeef762065e52cea0185060d5172ddc4b7565fb0193ec2b7bcd598cadfd3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180296730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a714595751dc43008afcb1874c0fec39fce34db9b47d6018455b76a214dac84a`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:37:15 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 22 Apr 2026 01:37:15 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:37:15 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.19-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 22 Apr 2026 01:37:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Wed, 22 Apr 2026 01:37:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347405e74a9fd997c576b0789f3f886f04c2a4f6985ae33a1973450b670ed4a4`  
		Last Modified: Wed, 22 Apr 2026 01:37:30 GMT  
		Size: 150.5 MB (150516556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:3be037e806bc40d551d487ae98b0c9a010f8af00ebb1554623169e75a3e7cd87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe1f796d74ea2d0196d0ec0bc3809a78c5b37d42171a6799e0d9225506dc1fd`

```dockerfile
```

-	Layers:
	-	`sha256:19fb6bf6e7b0a8f7627c2eaefcc1578273e6f23f8c6b3a2d841cd8d2346739b2`  
		Last Modified: Wed, 22 Apr 2026 01:37:25 GMT  
		Size: 9.3 KB (9298 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:17-headless-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:6a9a9bb3a3dd3abc31de6c2dd5c8e6bc7613b47b27b2b6d184d0e9b0c09069a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.7 MB (180701666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd3820fc3abc7a7894fc8ca83febcb96bb66a153580870e7e86876217b538f36`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:41:22 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 22 Apr 2026 01:41:22 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:41:22 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.19-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 22 Apr 2026 01:41:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Wed, 22 Apr 2026 01:41:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19dfb41ff3783793d55f40679f7e2bf26a7a8cee0c3d6124f05a929cd9836144`  
		Last Modified: Wed, 22 Apr 2026 01:41:39 GMT  
		Size: 150.6 MB (150558060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:a83f0a3cf341252ce3c796eafea99fbdd8e37d938bca747204d90dfb8a645a4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72ca2cbf17400c5c4c16bb9bea13f5c7d6c91cda1b7563d353db5a58a4caaeed`

```dockerfile
```

-	Layers:
	-	`sha256:ae3e9686be2b840746de4d564e1d334b890cd59bfeec4343ffc7845ceacf57a5`  
		Last Modified: Wed, 22 Apr 2026 01:41:36 GMT  
		Size: 9.4 KB (9402 bytes)  
		MIME: application/vnd.in-toto+json
