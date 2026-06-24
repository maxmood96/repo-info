## `azul-zulu:11-headless`

```console
$ docker pull azul-zulu@sha256:c362cb7786d7a1d92b1d9f92242010f30964f7c521365a1c3e2bc8455f8f6d8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-headless` - linux; amd64

```console
$ docker pull azul-zulu@sha256:33982374a856d9d6865ea8e32e2160bb98430070ee89b29fb1ce59e1fa55322b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.0 MB (175986104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dacda0074ad8322d593586368a76a15afa2b893f66a9a7a9f8358b0e45c391e8`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:38:32 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:38:32 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:38:32 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.31-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:38:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Wed, 24 Jun 2026 01:38:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a69e01ddc26aaa5b75435ef747819e4c14e75e70e39bb179e44c58ce253a4b`  
		Last Modified: Wed, 24 Jun 2026 01:38:47 GMT  
		Size: 146.2 MB (146200685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:cc38bbd5bb801f3dd8f6c8dd8b1fb5bbfc66b4889d77a1fc3326769489020041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80191170b718316a9b0ec6ffc87be65c357ef7ba35e6b0fed1fdea018bfbc92`

```dockerfile
```

-	Layers:
	-	`sha256:eaaca747507d86b14ca524288c19895af95579004b181079de73cd2fa8e7d43b`  
		Last Modified: Wed, 24 Jun 2026 01:38:43 GMT  
		Size: 9.3 KB (9298 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-headless` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:51cf94941bd9331e1e5867c2701a94c6d83cd60e2eed67656217999627d07f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176059534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8786abea60109769ff0890be3403a5fbf96ab3ada0957dd6782c0edf86fa03e`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:40:45 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:40:45 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:40:45 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.31-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:40:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Wed, 24 Jun 2026 01:40:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a77ece3dfa0f1d2750e53170b9d00820a36e2196c37d255063feb45b440da72`  
		Last Modified: Wed, 24 Jun 2026 01:41:00 GMT  
		Size: 145.9 MB (145910983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:be6cace8ba412e2bc479f5e395f07f098a8062b6567da94ea4501668218dbb3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84e70aceacfc02681f31b5e78ea97e6a1f5657b9fbaec11e6bc1d90fd022a1a7`

```dockerfile
```

-	Layers:
	-	`sha256:65b7a5b760feb5ccb6f036da11ab73753a33b25a30bf098412915c5ce758c4b4`  
		Last Modified: Wed, 24 Jun 2026 01:40:57 GMT  
		Size: 9.4 KB (9402 bytes)  
		MIME: application/vnd.in-toto+json
