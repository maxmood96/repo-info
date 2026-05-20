## `azul-zulu:26-jre-debian13`

```console
$ docker pull azul-zulu@sha256:7425185ca0eeee8831500ea8954aa43bc03da987de65ae2f308a3a905ae3ac44
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-jre-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:4dd5af2e0b36bd68c8a9ab81f28615ff8666c00419062a7f86428e3f6d261198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121914741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:393fa48df910617a5a086087ee713a0453fecf0691d0c5e8c34e124f662ea04a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:22:46 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 19 May 2026 23:22:46 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:22:46 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26.0.1-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 19 May 2026 23:22:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a4c2d70899b4bb33884a9717ee05ed43ee8a6a4a32e6b0974a8c7428e919c6`  
		Last Modified: Tue, 19 May 2026 23:23:00 GMT  
		Size: 92.1 MB (92134815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jre-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:02de4a84bf9c6c8765396b768626b84d9d31c13e0160dda7bd39f7c7e566d0be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81be97380a518f54d91e1fabe556c3be0687a9cf50dd7a8b13e1fb13100a38b0`

```dockerfile
```

-	Layers:
	-	`sha256:0b5052b8e1822928fcb31afe8ba8d3f0ab0632b2b808ab98ffc10ce8c5d29879`  
		Last Modified: Tue, 19 May 2026 23:22:58 GMT  
		Size: 9.2 KB (9187 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-jre-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:dc5721f0768eb936346ef957d80c2c390d2b12662deb0ec70b51c3bec723387c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122182306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47d9f38ac7db56cc5b4bc03a5a3593bc7ce8d77c04aab19b3702b101a81aadc9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:26:29 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 19 May 2026 23:26:29 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:26:29 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26.0.1-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 19 May 2026 23:26:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c16177c1176fe774d763480114704149cc74a83ef8b43fcbf7deac015210a5d`  
		Last Modified: Tue, 19 May 2026 23:26:43 GMT  
		Size: 92.0 MB (92040387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jre-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:f1f620be911aad39c4af0c63afeb1b5ac5c38943d0f5e437e3a9eaa5e17de80d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be5e128b752ce4bf6e1e150cabdcfd06b80b2b7ccb80a1970667525c9507c230`

```dockerfile
```

-	Layers:
	-	`sha256:aec521d9a90f8ae5bf5de54266535cca8625e74a303772bd84028d019af69656`  
		Last Modified: Tue, 19 May 2026 23:26:41 GMT  
		Size: 9.3 KB (9291 bytes)  
		MIME: application/vnd.in-toto+json
