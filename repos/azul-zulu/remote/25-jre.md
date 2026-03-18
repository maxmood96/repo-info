## `azul-zulu:25-jre`

```console
$ docker pull azul-zulu@sha256:64440b8e621a666370e38acb547943f5faf64c53baae002d45cbdc97933f9f98
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:25-jre` - linux; amd64

```console
$ docker pull azul-zulu@sha256:2d44facafc8311530cecae998360a7d33640d64fb8eb8da3a5758207e37d32e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120678465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2e0e140672a36b3f61d153cc3cbfaf5d4cf58bbe2d6be5a22cbc5e16098e13`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 22:12:30 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 17 Mar 2026 22:12:30 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 22:12:30 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.2-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 17 Mar 2026 22:12:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5776d7b9b8c3045a70de75a1a689c1f06d034e7961867a21cf172fe82d0e3f96`  
		Last Modified: Tue, 17 Mar 2026 22:12:44 GMT  
		Size: 90.9 MB (90902965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jre` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:9cbffac56d8654a7945491539fc1c08d47894f7f0d7799f1578092a8381e1185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8be59e3fcf7351add4f6b9980466f7dfa2f08bcebfa93f544adca89a966f036`

```dockerfile
```

-	Layers:
	-	`sha256:ccd4d219433ae2995d6b1ee6a81023e76e7bbd1dbe619534b0aecbb7a963f574`  
		Last Modified: Tue, 17 Mar 2026 22:12:42 GMT  
		Size: 9.2 KB (9187 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:25-jre` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:9bbed7da5d86746ac4952515dc16612a9c5add0c951eb54918f185679a463d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.6 MB (120618188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2313dacb992da83a543c10f14feeb2b3bd3a12529cc24f6f01155360f36ab1c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 22:12:10 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 17 Mar 2026 22:12:10 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 22:12:10 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.2-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 17 Mar 2026 22:12:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f73b797ab56ff3dd86d4837e1f99a42d5dbcb6b6b6a527833f6219c809a0b4`  
		Last Modified: Tue, 17 Mar 2026 22:12:25 GMT  
		Size: 90.5 MB (90479772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jre` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:0509af89f14f3f622658e247b5295ed7458dd95c4c2fff6f8dc72ac711c7449c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc84bab31f2fc0e8bc5cd36399b349474b9be6048924566b5f33222cf41961b`

```dockerfile
```

-	Layers:
	-	`sha256:caa64309b9e60939260e20ebef2eae68cdeca74c88414f5422cc5ed36e8b7a3d`  
		Last Modified: Tue, 17 Mar 2026 22:12:22 GMT  
		Size: 9.3 KB (9291 bytes)  
		MIME: application/vnd.in-toto+json
