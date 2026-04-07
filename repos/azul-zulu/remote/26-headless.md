## `azul-zulu:26-headless`

```console
$ docker pull azul-zulu@sha256:5624fb14a556c57ef1c02f167b46680e8721bba5226b0bc66215a0dd1c1dca38
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-headless` - linux; amd64

```console
$ docker pull azul-zulu@sha256:3e124ee073e10ea18bec92f50678419d35da56c9ed1330f532a693874d486b24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.9 MB (214888536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ef213dae1bfa72a95f37e888cd5fbcf845ea4e8350138f806c0dd69908d196`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:46:35 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 07 Apr 2026 01:46:35 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:46:35 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 07 Apr 2026 01:46:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Tue, 07 Apr 2026 01:46:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b61968d8c9e152889963fd08929810e4a6f9f9fde96e9caec5bc2a1909e060`  
		Last Modified: Tue, 07 Apr 2026 01:46:53 GMT  
		Size: 185.1 MB (185112896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:f388337232cd7ae14e726897b4b8012d782d0bf70d3016c1aa25d806ca439a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0daa462c3eb4eacae87ae334aba0edb89a56a2955cff8bca8fb215bd680f84`

```dockerfile
```

-	Layers:
	-	`sha256:e1a342b39fe875e5a7684ddc776b73aa834b5916381408a585d332a6b889cd0b`  
		Last Modified: Tue, 07 Apr 2026 01:46:48 GMT  
		Size: 9.3 KB (9283 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-headless` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:878b5a72ba5f48ea339da086a61765eaea0c0a37e896295df0e1148ac38fc06f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.0 MB (214954511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7192c4a806d052ce7a3f4f87b574848b816e2f0207b6eff899431b60a6e065`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:49:42 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 07 Apr 2026 01:49:42 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:49:42 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 07 Apr 2026 01:49:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Tue, 07 Apr 2026 01:49:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b94357c755622ad615f086f36c7022da4a114a95376d96fd53b967d4ac4c4f1`  
		Last Modified: Tue, 07 Apr 2026 01:50:01 GMT  
		Size: 184.8 MB (184815960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:320955a49e9fa80a6e7bd132ace6b2182679174b87682a5d16f0f44cfbe83cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f085d3fb40ce7bcb55d637275f2a069dcc8c1a308a5a9f4be61bbfccb4548ed4`

```dockerfile
```

-	Layers:
	-	`sha256:bfdd2a180c967befd6ecb11d15439f72334983955db025e17b6d25423b46d39f`  
		Last Modified: Tue, 07 Apr 2026 01:49:58 GMT  
		Size: 9.4 KB (9387 bytes)  
		MIME: application/vnd.in-toto+json
