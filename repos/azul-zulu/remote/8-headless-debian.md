## `azul-zulu:8-headless-debian`

```console
$ docker pull azul-zulu@sha256:060265f2a5dd8fb9ffa40d3a0c608f65d79f71c55c9e9351b28ff725d8ca68fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:8-headless-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:71b9f750c19397b8af16fc09d4fe39f200493bbcd94131ca52a932463c25e5c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.9 MB (88907381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e40284ee13bb14a834f72df3df86f36fa932a8d48e7fbfa0506a201df8b547c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 22:10:56 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 17 Mar 2026 22:10:56 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 22:10:56 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.482-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 17 Mar 2026 22:10:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8cb67e1f224af3b5172f2d16574c74de4f63f2b6270fffb9b75db0a9dd2c49c`  
		Last Modified: Tue, 17 Mar 2026 22:11:05 GMT  
		Size: 59.1 MB (59131881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:269a929098cea38fad94493c5c31a583d49b685870272f0c94888a226269f6f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b575a5361768f667b335d40559eb241987659273217f271962ded9fb4137ee6`

```dockerfile
```

-	Layers:
	-	`sha256:de2aef5d9c6bac7e509b39c37a652bf5b20b0ba0ac7cd8550ad5607e5ae0a58c`  
		Last Modified: Tue, 17 Mar 2026 22:11:03 GMT  
		Size: 9.3 KB (9261 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:8-headless-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:3cf6c103a38979082b7ab8641531bdb287b870b285dbd82c73e3729b7716652c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88692393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f808d8314aa88108f3e136554336dc5fcdbecca6e3a4e5a0dd7d2997cd0cce8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 22:10:49 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 17 Mar 2026 22:10:49 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 22:10:49 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.482-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 17 Mar 2026 22:10:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed74cb8b624c0f0bbc3021d3278f3a9d3be042d9ead6b698c4ef67453f51ead`  
		Last Modified: Tue, 17 Mar 2026 22:10:59 GMT  
		Size: 58.6 MB (58553977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:95ecced3dc755503a2fa0570ccabe3d43ad5b4afc3f32deab6fa345cfc2453cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:343ee50b8673df18b5fddb44fbbab12c4f6d0e56570cc0b70014b5554c9f84af`

```dockerfile
```

-	Layers:
	-	`sha256:74827993b542771cfa0e0448890c71e3567026297070cdda1c1f71aa57100832`  
		Last Modified: Tue, 17 Mar 2026 22:10:57 GMT  
		Size: 9.4 KB (9364 bytes)  
		MIME: application/vnd.in-toto+json
