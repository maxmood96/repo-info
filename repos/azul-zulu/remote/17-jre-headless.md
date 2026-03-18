## `azul-zulu:17-jre-headless`

```console
$ docker pull azul-zulu@sha256:da8d481408399ed9cf54a40b3544c47f7572f30fa62335905e0f295260076d76
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:17-jre-headless` - linux; amd64

```console
$ docker pull azul-zulu@sha256:929dd1da70f7c15c40eba200c331a84be56d9d6060babe2cb203c6214abefa6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99169207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3040e056688c8cee3dd12adf0e0211f6041e3dba9bef7e91341e2aa9cc7f55d8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 22:12:20 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 17 Mar 2026 22:12:20 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 22:12:20 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.18-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 17 Mar 2026 22:12:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:501921c462afb95466ebf753cc92e7f08e99956883e27e6227e7ea45f89f65dc`  
		Last Modified: Tue, 17 Mar 2026 22:12:31 GMT  
		Size: 69.4 MB (69393707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jre-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:51810e56aebad2e687cad3a83a90f055ef780713f36a91bfd19c95bac4368b3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acefe45b182aecdc1b8fe47f0c9f4fb486c4f04309e33c4c66b61ce06e0d4d5f`

```dockerfile
```

-	Layers:
	-	`sha256:6b46fed73b85d745b16135df13c209e7ac938ce7aaf07a9c283a912089bbdd96`  
		Last Modified: Tue, 17 Mar 2026 22:12:29 GMT  
		Size: 9.3 KB (9301 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:17-jre-headless` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:3faddcc087314304eed424a171ecab5cec101041b338e782ddd3d2659db734f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.6 MB (99569563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf162d0ecec8c5e0119e290ff6a19d212a26ba7890b366d9d8792c347c726950`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 22:11:23 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 17 Mar 2026 22:11:23 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 22:11:23 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.18-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 17 Mar 2026 22:11:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5d618b885531955ecc3fc7cfe99c50fdf92fb9f8074008695b052384f9abc7`  
		Last Modified: Tue, 17 Mar 2026 22:11:36 GMT  
		Size: 69.4 MB (69431147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jre-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:cefb98c93678303c091c7c605bef809f08497ecc00ec2666f8175d4eb1b2ff14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e68aaeeb6905a349433791eb9ee753be4e1c23bb79284af48e4c4757a3fad8`

```dockerfile
```

-	Layers:
	-	`sha256:c3b7a5a84ace6ebed49a86dd985ff88bd586821a800bd56369a59597b0e62ecc`  
		Last Modified: Tue, 17 Mar 2026 22:11:33 GMT  
		Size: 9.4 KB (9405 bytes)  
		MIME: application/vnd.in-toto+json
