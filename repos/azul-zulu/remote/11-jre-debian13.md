## `azul-zulu:11-jre-debian13`

```console
$ docker pull azul-zulu@sha256:6d5e6cd71ba2278cd051fb48e362c8ce3c9c55fac2eaef72c1cb5fcebe01a5d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-jre-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:879cdeb9c667331814c17d8409b0c023937bef50cb8248edf8fbd98e289b9c7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.8 MB (96832895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c6d758b443bd9325c272059fbba8fee44df5bc1c7dd237866f25b89db0d7537`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 22:11:27 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 17 Mar 2026 22:11:27 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 22:11:27 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.30-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 17 Mar 2026 22:11:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfa13ffb6570d94271210ab37460871525db788eb674e5152b7a9e1df33d9ff`  
		Last Modified: Tue, 17 Mar 2026 22:11:38 GMT  
		Size: 67.1 MB (67057395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:102384bfa544151711ab3113d8b80cf54c8ae34b7062838a1c9387f8710426f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36fa0c17a60f84aaa4674a8019e2aeb89d5f76cb4d1817c349858b31a1dbc510`

```dockerfile
```

-	Layers:
	-	`sha256:64084d95b064623c5291f7bcd0c904913ec214138722995ea91161d80984ca53`  
		Last Modified: Tue, 17 Mar 2026 22:11:37 GMT  
		Size: 9.2 KB (9188 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-jre-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:c129675af317abd5392211558d0f12e2b921d4c97b56f0b8b5cdbd5feda8659b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.0 MB (96966458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faabcc5d9a7e9e8244421bfdefd3a4eb4a5f764c69f61e0684106084daf404c8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 22:11:25 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 17 Mar 2026 22:11:25 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 22:11:25 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.30-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 17 Mar 2026 22:11:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0679adc3c2c5cd7920fd8ffb75843d16f8e4a36f9a6025207d1421eff5156d92`  
		Last Modified: Tue, 17 Mar 2026 22:11:36 GMT  
		Size: 66.8 MB (66828042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:22a6a352ba11537cbeeb3784336de419e545adad21481866a9d2617097406d18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16fc907d068d5e2716d577a709d3a5a01d0d6a427c699322039c8b33db1cb55d`

```dockerfile
```

-	Layers:
	-	`sha256:e25d5c27eed5ba89428f3675f647fc6931cf711151c4b268c5001ac3388f70f2`  
		Last Modified: Tue, 17 Mar 2026 22:11:34 GMT  
		Size: 9.3 KB (9294 bytes)  
		MIME: application/vnd.in-toto+json
