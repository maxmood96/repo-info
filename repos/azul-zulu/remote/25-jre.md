## `azul-zulu:25-jre`

```console
$ docker pull azul-zulu@sha256:3223cd32b62cccc2d4542c64f72d74ff800b7f03d3c7cd70e2d5094ced03b742
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:25-jre` - linux; amd64

```console
$ docker pull azul-zulu@sha256:88d95cc62b9c3aa981723d135abbbfc5a63a57ff01db9317e04aba59e3737d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.7 MB (120679049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f464d42198a2b298be34d035c8cf2059eb18caf95c9ff71af797c593e053e6ef`
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
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.2-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 07 Apr 2026 01:46:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d623d9e038cdd35c3b199233f0cb200cf579f6d926c7af17c112f254c3c7c46d`  
		Last Modified: Tue, 07 Apr 2026 01:46:39 GMT  
		Size: 90.9 MB (90903409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jre` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:63f245dbb7cbc353bcadb2523b5e717514fba6bc7ac3b23b53ff7dcd4ba229c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fff85daccaa1e3e3ef611e3d244e26e57fa942b9e2f05b5b06985134fa8aac0`

```dockerfile
```

-	Layers:
	-	`sha256:ae6d60ab007c60714a144b0ba810ce46548dc47ee55c9573f2878692502f2887`  
		Last Modified: Tue, 07 Apr 2026 01:46:37 GMT  
		Size: 9.2 KB (9187 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:25-jre` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:edd4cb78d2f83323a02e037dbba333d62c31dcbea2e8ae0ce85c1d1adcba599e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.6 MB (120617617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae34096e5ee1664c095d8ca62c2ed1627053d6507d976635a7b2adcfc784245`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:49:41 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 07 Apr 2026 01:49:41 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:49:41 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.2-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 07 Apr 2026 01:49:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53398a3b8fa1578cecb2266d25cdf0a532a1bd9e078d86e2c79a5db2be2dadab`  
		Last Modified: Tue, 07 Apr 2026 01:49:57 GMT  
		Size: 90.5 MB (90479066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jre` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:4dbdde2a97a7e8e39527c5660242995f2e8deea8e126d99ff7f42beefa09ec68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63c8c1050b002168be7469dea40d923f28586ed50ee9bb30c8e201dbb2abd38`

```dockerfile
```

-	Layers:
	-	`sha256:cba0f850e8dae41a5206a06bbbdf238ee33767ad7601acfed695a0c8b453b988`  
		Last Modified: Tue, 07 Apr 2026 01:49:53 GMT  
		Size: 9.3 KB (9290 bytes)  
		MIME: application/vnd.in-toto+json
