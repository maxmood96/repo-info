## `azul-zulu:8-jdk`

```console
$ docker pull azul-zulu@sha256:5ffef8f92947acddff199ac09a6ff73d76e92be1229cdcb4ffa9eb669cdb966e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:8-jdk` - linux; amd64

```console
$ docker pull azul-zulu@sha256:a9255454463a944fda75eb46bfeed55b8c6ee4196d5deecc31e9431c344d73ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91791504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196ad48874d7268bca7d2532a00776520334f2de90877105fe38fa6feb6ade71`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:43:37 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 07 Apr 2026 01:43:37 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:43:37 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.482-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 07 Apr 2026 01:43:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b29730d7203e07fcff5b4c828efcff64271d3fab0d524cfbdeec36d6481f4ab`  
		Last Modified: Tue, 07 Apr 2026 01:43:47 GMT  
		Size: 62.0 MB (62015864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jdk` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:b5eed8851ce582b095f18715b16faa6dc0e240813e74f245746e2aa2ddbc965d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b196cd4a5929ad4519ccb802d3b201929da8210e5f73a41e776fafae0362489`

```dockerfile
```

-	Layers:
	-	`sha256:067d3649695d06948830ff9cbb7424e9311632de58b7dbdbcd7f1b36784e3625`  
		Last Modified: Tue, 07 Apr 2026 01:43:45 GMT  
		Size: 9.5 KB (9468 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:8-jdk` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:f495bfcb798a4d745a1ca8f1b6cf73315ef858dd38ea4da97f77a961ff28dd38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91565383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc53d31a9e2fa52e405761d97810506f9550878df5c4f8b2feca16b9a48d4cd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:46:32 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 07 Apr 2026 01:46:32 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:46:32 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.482-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 07 Apr 2026 01:46:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b03b06a6d6d577d60cf39810bc9cbe54461520c57268a18f006448af850b591`  
		Last Modified: Tue, 07 Apr 2026 01:46:42 GMT  
		Size: 61.4 MB (61426832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jdk` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:21a593c973f59c77a95f2f1c05798b315d1988a2bfae1cbf027246dbe98ca37b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8090bd2324100834aa31e5dfeabaef298f5029a3207cf38a229bce0e671855a3`

```dockerfile
```

-	Layers:
	-	`sha256:5546c66a7b5753e954db9fd8a13513644103a81836cbaa2c3fd901816bd6a619`  
		Last Modified: Tue, 07 Apr 2026 01:46:40 GMT  
		Size: 9.6 KB (9584 bytes)  
		MIME: application/vnd.in-toto+json
