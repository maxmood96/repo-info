## `azul-zulu:21-jre-headless-debian13`

```console
$ docker pull azul-zulu@sha256:d26d87578e95d69931c1479b44a3cac6530cc765b548e89dd47f45937a9e516c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-jre-headless-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:a24e6950e1915358635fb9868a61fafe33f6408a0cbad6c423afaf1a78bde576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104475283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643c496a36fcb0f0a3a60b7ac44a6e07fb44c1e9680088201735c78314efa30d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:45:53 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 07 Apr 2026 01:45:53 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:45:53 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.10-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 07 Apr 2026 01:45:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89f7e901fd45cfc55a83dbd91c894f81322fc36d3d43fbe9a634a26af3098a5`  
		Last Modified: Tue, 07 Apr 2026 01:46:05 GMT  
		Size: 74.7 MB (74699643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre-headless-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:a52722565b1113338945ad6c1f0ea6494f046a4ae1ebcc21715744a2345bdb90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9059c57730fbc4fa2cdfff76020cbb61d48f35ba42e23b4e6de00844ee9b991d`

```dockerfile
```

-	Layers:
	-	`sha256:557d3b0f6e2ecb8a2301369b5a417a78cb50e4bf23f0ec399ed127234776be0f`  
		Last Modified: Tue, 07 Apr 2026 01:46:03 GMT  
		Size: 9.3 KB (9301 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-jre-headless-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:3fdb8550c7fd90fa8d49e20471e22b545fac799717ad87b9dc9b249caccde0a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104499623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:133beed23e5898ae6c9b8da85ce1ae9bf84e26c418abe6bccf3dad8478ba56b3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:48:57 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 07 Apr 2026 01:48:57 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:48:57 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.10-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 07 Apr 2026 01:48:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13152254ba333a3def7fbe8e559a88d00b3f0e8028b77ea0b2752ed54ef35a63`  
		Last Modified: Tue, 07 Apr 2026 01:49:09 GMT  
		Size: 74.4 MB (74361072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre-headless-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:fb2be43bf54d6b44988dd71c28b97b6cc519b78674f05fd96dd08248c26ce275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21245eaf046252fa2cd86766697ce8a25ccc599f90f821cfe442ead2e835c1e8`

```dockerfile
```

-	Layers:
	-	`sha256:febbdda761c04198d8165aeb9c274084fe89f9b7881027768c8f2523f4575107`  
		Last Modified: Tue, 07 Apr 2026 01:49:07 GMT  
		Size: 9.4 KB (9405 bytes)  
		MIME: application/vnd.in-toto+json
