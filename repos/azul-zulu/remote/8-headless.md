## `azul-zulu:8-headless`

```console
$ docker pull azul-zulu@sha256:e103b97c2749227e8f0fe42a810a51ebd7d5b810f821fc25b9fabcd3d5df2084
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:8-headless` - linux; amd64

```console
$ docker pull azul-zulu@sha256:ab6ae6c4ae61e5e21e2cf7a56fff55bcab175431b75d653996ee64d304c944ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.9 MB (88933997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3788997628e004cee6a30d65829af7e4842cf8100f14d807740885c3e60eb8b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:37:17 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:37:17 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:37:17 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.492-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:37:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791ae61826287e619ce79f2734bcebb49343a9bc446ac78bd2997862e83c338e`  
		Last Modified: Wed, 24 Jun 2026 01:37:27 GMT  
		Size: 59.1 MB (59148578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:b489786dbdbce85930442d3f3498bfccde2ad02b5c31ee8d4cd409ed4b64fc19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb95db4bd0a3ea418d35726e09d87d12f5428fabe9bb9a8afbf093c71d3e6fae`

```dockerfile
```

-	Layers:
	-	`sha256:dc6ed0c010fea2bf4182ea03ca7afa854cc8942bc5b26888edb64288173971e5`  
		Last Modified: Wed, 24 Jun 2026 01:37:25 GMT  
		Size: 9.3 KB (9261 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:8-headless` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:e0b7ed1e2c5c150996bd6c325a3da090de5dd2aaa2081822619e2c8e15f00d5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89626895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b997fe155509ce9489977443290f3cef066bfa595bcd5077fa54a0e5b4f85b4c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:39:33 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:39:33 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:39:33 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.492-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:39:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd340ed3c3a4a5bca38cd7fa385fe5770fb88d902583932b84811ea2e888c2b`  
		Last Modified: Wed, 24 Jun 2026 01:39:42 GMT  
		Size: 59.5 MB (59478344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:8ec0f73ecf9258ed9b25a7cba0eae11fc584c0a0c424a5aaaae25b2b2f76d66f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:677bbbe8d35db9424c4a4cc52872f7b587e9929bc2ea5fa693fd8cd77dddc27e`

```dockerfile
```

-	Layers:
	-	`sha256:c1c45e766d1989783bf5e7b81f855239fbbd48b22db85261e1549e67155e399d`  
		Last Modified: Wed, 24 Jun 2026 01:39:40 GMT  
		Size: 9.4 KB (9364 bytes)  
		MIME: application/vnd.in-toto+json
