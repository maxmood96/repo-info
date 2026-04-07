## `azul-zulu:8-jre-headless-debian`

```console
$ docker pull azul-zulu@sha256:66e3f93b19b65b100ab0d326a55708e3f4596714120cdad92c130a670599c68c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:8-jre-headless-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:615f7ca89f04d93cbb0b766446017be4c3974a8a14ed2a3f0f69cee75aee10de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77472326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7617e375cdc98aa5f50d648cf3dd9317eda0acae1d435a6f1ab8b74b769b54aa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:43:55 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 07 Apr 2026 01:43:55 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:43:55 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.482-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 07 Apr 2026 01:43:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c16db5f1f580f5a74848aaf163c2c6f4ffcef252209a7a5e95be00e42f0205`  
		Last Modified: Tue, 07 Apr 2026 01:44:03 GMT  
		Size: 47.7 MB (47696686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jre-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:56db32efaca20d60e520a1a6b07d1e4c3ee94b6e222764057b2f107d9450a89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:465dc7df71e8c72a08b9014411965924b4003b92551922052e31afafcafbf021`

```dockerfile
```

-	Layers:
	-	`sha256:6f970e9f0ef891cd3b42029afba1b5ee1965165896a28aa479b6eb778f616210`  
		Last Modified: Tue, 07 Apr 2026 01:44:02 GMT  
		Size: 9.3 KB (9284 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:8-jre-headless-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:c5bbea53e085c79ff9284d28cb9636df4d374f544144c5222291dcec47a82b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77161450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7932be3e384b8a707c26e4d6f90b591cf1cbbb2542c08d3933c9706823f28f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:47:06 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 07 Apr 2026 01:47:06 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:47:06 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.482-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 07 Apr 2026 01:47:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83150db931c6ee1e63773dd5c0a952363a51c97cd0d4bad20b20f51b92060696`  
		Last Modified: Tue, 07 Apr 2026 01:47:14 GMT  
		Size: 47.0 MB (47022899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jre-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:088a9b35697138cd99c79e6972b4090b44b7c93b2fa45b1e49b3ba51d85395a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd4f18f2c221a03dc586cdd3f695d5173ef4e52e66ef8db63cfc49de6b43b0b4`

```dockerfile
```

-	Layers:
	-	`sha256:a0a72f6b98c2994118eb8932013327a84a938d93a67cdfc56bdf5e9a9520348a`  
		Last Modified: Tue, 07 Apr 2026 01:47:13 GMT  
		Size: 9.4 KB (9389 bytes)  
		MIME: application/vnd.in-toto+json
