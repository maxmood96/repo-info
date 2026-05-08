## `azul-zulu:17-headless-debian`

```console
$ docker pull azul-zulu@sha256:7109b30273a6d8e60dde24d4e326bc1ea38679cdafa42c421091c3dda4ddc562
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:17-headless-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:48bec15cced3f68096a110730e918cc8285af7a197d1f2e6f975ed6e0dc320a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180296906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f7598a3ff090aa0efd7179a954dca8829cb7982d944289fdc81f87fd6b696f`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:38:07 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:38:07 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:38:07 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.19-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:38:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Fri, 08 May 2026 19:38:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688d5f52d26f5700ea78542b29dd86fbfc03f0cb797f2867773643343428c6dc`  
		Last Modified: Fri, 08 May 2026 19:38:22 GMT  
		Size: 150.5 MB (150516680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:04d2adf266d2462aa1b1688d9259d3beefc87db770aaa0873a987fd44552da14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b130d98bf30f88887a1732f833999914a5d1bde8f98b0c016a133f1b04594750`

```dockerfile
```

-	Layers:
	-	`sha256:8a799ce336478be7dc08251a6973346cd4a9645cfb44bd52cb1f93e8bde3d9c5`  
		Last Modified: Fri, 08 May 2026 19:38:18 GMT  
		Size: 9.3 KB (9297 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:17-headless-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:f6a689e404b0b6fefa861912a5c01941e62ca1918cddc698440345e3009d36f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.7 MB (180701707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e1c38c15fac74ae9066428f8024e548ab79a77dcf7517a721b9a2444fe74ea3`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:40:24 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:40:24 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:40:24 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.19-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:40:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Fri, 08 May 2026 19:40:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06bf4a77fcbbba5d5c860f857de1bb24c48a0c1c8b87a5186de1f7ac7f6cfb2`  
		Last Modified: Fri, 08 May 2026 19:40:39 GMT  
		Size: 150.6 MB (150558065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:2356eea4408bc915d7cd08f8a2f1ba388c288bd1c8f6d99982343408ef1c82a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f507733556fb10e484e620f1f9e92e3e2cda1880b916ee47131b71ec8ca81b3`

```dockerfile
```

-	Layers:
	-	`sha256:e4129b0f6bafa4b80313b30abfeb25a2b30d7ce29fd1183f1328fe0697ea9053`  
		Last Modified: Fri, 08 May 2026 19:40:36 GMT  
		Size: 9.4 KB (9401 bytes)  
		MIME: application/vnd.in-toto+json
