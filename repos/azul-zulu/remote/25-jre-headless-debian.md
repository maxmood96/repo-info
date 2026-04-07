## `azul-zulu:25-jre-headless-debian`

```console
$ docker pull azul-zulu@sha256:acec09e084feb26ddd31caf8d9399323f74acac3643363a542a84a5df20d1d2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:25-jre-headless-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:23815f5130e57a6f686870e6120e5809375492a8a17f269e736c94267086b332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.6 MB (118606193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:661a97b875dd5d4a96e5d81922b05505c437713312943b9eab170de111fdb963`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:46:26 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 07 Apr 2026 01:46:26 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:46:26 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.2-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 07 Apr 2026 01:46:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e878558b61e9d9a05ab749987f7f6e6fd261842c27c70ffcddd5f6de3625d4bc`  
		Last Modified: Tue, 07 Apr 2026 01:46:40 GMT  
		Size: 88.8 MB (88830553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jre-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:9340e4d23f10bbc09d4b29754d95ad1a380ef15ddd179a081a74f36eb203330f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e123fcaa276bb43386a4ff073e1dad3ad5d06206bd8a72ed971c0d4acd6574c1`

```dockerfile
```

-	Layers:
	-	`sha256:e79696a2e313ce859abb0070bee126b6d6c6eccc3a8d01d4d84729290790d192`  
		Last Modified: Tue, 07 Apr 2026 01:46:38 GMT  
		Size: 9.3 KB (9298 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:25-jre-headless-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:092575507b2611e488726b491fabfc395af2b3b6a352ad8fbcaa65e2c3314ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.6 MB (118585924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118bfa2d107b1f6a954595319a70e8711f6560209f85b4aff96ad3e86d12af1c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:49:36 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 07 Apr 2026 01:49:36 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:49:36 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.2-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 07 Apr 2026 01:49:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7f29ede1396f582e996d367ca415d02ce93dc665d186148457edbb85f1ff8a`  
		Last Modified: Tue, 07 Apr 2026 01:49:50 GMT  
		Size: 88.4 MB (88447373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jre-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:19670413e78e28ce85662f69a0917ce21ebc7c2688285597847456c534ebc94f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:561506e7cab96aeeb2c3092544802df6c1e8ae230c1d5c2304706c8ebadba331`

```dockerfile
```

-	Layers:
	-	`sha256:6617769c66de0f9ff84e3d1d08010ca0cd6ad5e7ebc220bffbdf7f812db072a1`  
		Last Modified: Tue, 07 Apr 2026 01:49:48 GMT  
		Size: 9.4 KB (9402 bytes)  
		MIME: application/vnd.in-toto+json
