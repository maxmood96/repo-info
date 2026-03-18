## `azul-zulu:25-jre-headless-debian`

```console
$ docker pull azul-zulu@sha256:6e2c0c50e97bc110bfb835d66f7fb207efe2da9958044b5bffea904e4537aba0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:25-jre-headless-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:6871e2859ce50b61c4c109886a70f1bd16e170b0f11cc9f6f86aa9bf8333c948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.6 MB (118605428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0106f90775329e1f9dcc6ffbd5053187a726581e0cf88bbc46fe50fb5b8ed707`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 22:12:33 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 17 Mar 2026 22:12:33 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 22:12:33 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.2-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 17 Mar 2026 22:12:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6e13755640134e1ae41f471fa607de238efdb7e6ea82b3de41057352ccd53a`  
		Last Modified: Tue, 17 Mar 2026 22:12:47 GMT  
		Size: 88.8 MB (88829928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jre-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:8945082b4a5b02d1422098cdb4eeaef5f69af907ab0644b6c2823c8b40a12ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b22df58c7bffd63e71eea86805233e4ef13c19ecbbda96a47160c7c0da4fab7`

```dockerfile
```

-	Layers:
	-	`sha256:55f347a9166c8678cf23b90be76057d2cfabeb9c757183fa9974e1215aaeee73`  
		Last Modified: Tue, 17 Mar 2026 22:12:45 GMT  
		Size: 9.3 KB (9298 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:25-jre-headless-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:91a398bcf9186065c70c4bf73d1477a1e53cdb5b1e8da37ddaab4ade0b879af2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.6 MB (118585130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b65d177e70f07704148cbdcab5bc3379f716cc905963da007aabaf3ea816f983`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 22:12:22 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 17 Mar 2026 22:12:22 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 22:12:22 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.2-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 17 Mar 2026 22:12:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6c22c620e308cab1854310587fc9cf49cac449d381aeb7d049e44d02f79f8c`  
		Last Modified: Tue, 17 Mar 2026 22:12:36 GMT  
		Size: 88.4 MB (88446714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jre-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:af8946643971a2fa05278c7e59bb805fd24d3e3680050bfd38a94f4f430df3e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dc397f826a98a57980da8c933ffe894cc76e85eb04dfcb45f62d4313b19d201`

```dockerfile
```

-	Layers:
	-	`sha256:f4e66402a6030d7e13695ad16f0b183181d9ee1b1d9814544d4adb83edf400ef`  
		Last Modified: Tue, 17 Mar 2026 22:12:33 GMT  
		Size: 9.4 KB (9402 bytes)  
		MIME: application/vnd.in-toto+json
