## `azul-zulu:21-jre-headless`

```console
$ docker pull azul-zulu@sha256:abbbefbf182c56df64d8aacce9825c62f30f5834c7a4b669ee666987c1df5efe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-jre-headless` - linux; amd64

```console
$ docker pull azul-zulu@sha256:f25bbc35da7bdf3a4c881929f7905452fb1e9345de9dcdd17acc4e89da2fc373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104610627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1323ff91812fbcdc85f9228f3718ff80676650822cd4b1ab5bf989f1701c309`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:40:09 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:40:09 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:40:09 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.11-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:40:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4fddb2468f056bf339df277ce6a4fd11257adfc2544ca7d835bdac52fd7610b`  
		Last Modified: Wed, 24 Jun 2026 01:40:21 GMT  
		Size: 74.8 MB (74825208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:6328ad6025f7858fb505d3de86369187a85488a9a20396d3a2979497325bd338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b34c0d49177e485bd4e217b07152c208cab1ab93e0ad56fd063dc8da0dd6409`

```dockerfile
```

-	Layers:
	-	`sha256:b94cf4069f9495f72e04beab6aca99d6ba16c83baff171fb828beb76f2c3dd86`  
		Last Modified: Wed, 24 Jun 2026 01:40:19 GMT  
		Size: 9.3 KB (9301 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-jre-headless` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:b2592e62191e3de481666daebd3fd53afe433afd6a190ee9ca1015db86071c0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104640545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3f9f276dcb03bbd2377489668daa98f542ab17a035f1618de37883abaed92e6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:43:24 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:43:24 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:43:24 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.11-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:43:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4634c5bce112fe2199ae8f48bcbe7f958ab76dc18183051d10f1363ceafb8d`  
		Last Modified: Wed, 24 Jun 2026 01:43:37 GMT  
		Size: 74.5 MB (74491994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:129398231d75cf1587ec6e9027ae7006d923d8bdc2f02d3f73954957ba163e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7a8a141ecab90c156d3e49d1bc6f033a3ce9ae34f358fbb29bb9ff2679c9bb3`

```dockerfile
```

-	Layers:
	-	`sha256:4a44740a7f5270ef282d4aaff8a249a754e48847b9b7b772b3a488e3ded19ac8`  
		Last Modified: Wed, 24 Jun 2026 01:43:34 GMT  
		Size: 9.4 KB (9405 bytes)  
		MIME: application/vnd.in-toto+json
