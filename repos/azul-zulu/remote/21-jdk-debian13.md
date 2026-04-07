## `azul-zulu:21-jdk-debian13`

```console
$ docker pull azul-zulu@sha256:8ca6a8108bbc4b02e308ad84376c3fc2b8958f5bfd7c44672e2f84f425eb6374
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-jdk-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:afb55b6e5d8a9b83a5edf7e298b19dc3974d26d322ffcafb64ca08eae40893f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.6 MB (195622076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ac1f478cfd2cb6e62686e271ef97df55529ca242624aee170f19f4d7a6ac89`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:45:40 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 07 Apr 2026 01:45:40 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:45:40 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.10-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 07 Apr 2026 01:45:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Tue, 07 Apr 2026 01:45:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6493144720e6b2158dc2d507934066678b6a47d01c241cf6a95b4504048260`  
		Last Modified: Tue, 07 Apr 2026 01:45:55 GMT  
		Size: 165.8 MB (165846436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jdk-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:0b21f8ca5b38a7b91927967ef4d53a9870d10bd01a57739878e134b68940353b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e6323135841def14c70d88fbf1d3563519881283dcac66fa06b6d65711423db`

```dockerfile
```

-	Layers:
	-	`sha256:193ebc7ff0e0b38b4c13456a0441301addf320478a8ec54c68677f1275e7bd03`  
		Last Modified: Tue, 07 Apr 2026 01:45:51 GMT  
		Size: 9.5 KB (9507 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-jdk-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:f3942fddb6c6246a530c5da5fc1b8e63a346bd64ccd5676969dc09c08fec1a77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.3 MB (195266872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3d543ff4876a6f49ce0ea95872a0473fa4473b5ed38fded24a044cfc41d12b5`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:48:54 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 07 Apr 2026 01:48:54 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:48:54 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.10-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 07 Apr 2026 01:48:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Tue, 07 Apr 2026 01:48:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f909caf14b3e160a30d5558c2fb915c699f15bc5f3478c607087504b672a2a94`  
		Last Modified: Tue, 07 Apr 2026 01:49:10 GMT  
		Size: 165.1 MB (165128321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jdk-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:3150e90119eb8555ca7fc5870b3d407f71720f14f5c2eeb5d72636a595ea83a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f74064840fd41b722eae637c3347b06d8517e9ac778a081b3e2ee7af78f9835`

```dockerfile
```

-	Layers:
	-	`sha256:8a8356213f18111d3365b3c56565e50711abb18414e4f6d3beef32364e376a7c`  
		Last Modified: Tue, 07 Apr 2026 01:49:07 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.in-toto+json
