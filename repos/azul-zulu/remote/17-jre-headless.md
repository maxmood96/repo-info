## `azul-zulu:17-jre-headless`

```console
$ docker pull azul-zulu@sha256:494564a4abb653bef6c37ea458839c4d595a1c7e5cba263b74c8cc3bd93da484
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:17-jre-headless` - linux; amd64

```console
$ docker pull azul-zulu@sha256:3abb7b801441139af76c697843d803fdeb6effbd032942dfe3c9f1637a256bce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.3 MB (99314425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5a68fc3edd97a29ebf6c3dba436d75e747627f01cb71777be23a606d9923dff`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:39:33 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:39:33 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:39:33 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.19-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:39:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8817d9905c3c1312d9d795185b7dfc3b25c4393d9cc0e1f7dd09d11e84dd85e2`  
		Last Modified: Wed, 24 Jun 2026 01:39:44 GMT  
		Size: 69.5 MB (69529006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jre-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:acc81f8e82bb908fd3cf802e5642f42c5ce6f5308f8a76041c6690b38787153e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9d8953e3493f19957982fdf60f498d18ea9119268450d39978ad79debc4595`

```dockerfile
```

-	Layers:
	-	`sha256:bc5e08c939e83a6110c78d7a28d4c9ebf402e8c45f8a39dce2343bece8d163cc`  
		Last Modified: Wed, 24 Jun 2026 01:39:42 GMT  
		Size: 9.3 KB (9301 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:17-jre-headless` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:1adfb916d2e9844cc88f2f5ee5eaad9bb9e1cb2b57d56b5f82835a411daea67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.7 MB (99733124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f3be3335d29d6258f5930e24e6edf0ea1728ea1e7fa856644db3e25888f8d8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:42:46 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:42:46 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:42:46 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.19-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:42:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9fb14dfc1ba9c30871c65a85ce069be218b30314d4220f2ba68241336fa7b8`  
		Last Modified: Wed, 24 Jun 2026 01:42:58 GMT  
		Size: 69.6 MB (69584573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jre-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:6ea3b1baeae50e316df082cec93d17aded6110a8488a24acf9f977ae33cde926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b79f17af06d0f32fe9a4def4e4fec26d22bb6e58787a1aa764672c1e69fe687`

```dockerfile
```

-	Layers:
	-	`sha256:aab7792115fed61bbe38b84883456699c0b7aedcedf91881b78d15bc01b25bbf`  
		Last Modified: Wed, 24 Jun 2026 01:42:56 GMT  
		Size: 9.4 KB (9405 bytes)  
		MIME: application/vnd.in-toto+json
