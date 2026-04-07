## `azul-zulu:25-jdk-debian`

```console
$ docker pull azul-zulu@sha256:b74f8bd3de5e2ae22e4de824061d4eeef101f185bbfdaec6e54e8c9b7c0bb88b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:25-jdk-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:d899f30512a89ef1ff9f7e922118ad61c74550475abcd58d3e89b91c9a6e80ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.6 MB (214645969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6ed8e6036e271323ec60ffeba086d674acd5a51f3a92a279a02ab141b6c28e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:45:51 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 07 Apr 2026 01:45:51 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:45:51 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.2-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 07 Apr 2026 01:45:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Tue, 07 Apr 2026 01:45:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f12e05b40275487aa75fde4a0b48b1184dd269f20421a024adf19183ff6a85d`  
		Last Modified: Tue, 07 Apr 2026 01:46:09 GMT  
		Size: 184.9 MB (184870329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jdk-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:4e120edc677c11d5a9e784a63fc504f83a2867e56e6a4227f88c81fb8f2f7ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a259d234c05290f1468afd83b8c3b30e9c27bdb6818795fe165c0e5d3e68fa`

```dockerfile
```

-	Layers:
	-	`sha256:f378151bedcaac103968c29253a7ac71fecc124e562383fd58729396bf991034`  
		Last Modified: Tue, 07 Apr 2026 01:46:05 GMT  
		Size: 9.5 KB (9504 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:25-jdk-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:aa843115d91a50b07ce7a65b305b41fa5019c95216ef6143fb4ef20ea16497e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214137604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09db72cff9b673096c9b17148b36cf147b5b648bdd760f3dda258ffd305c1b9e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:49:04 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 07 Apr 2026 01:49:04 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:49:04 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.2-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 07 Apr 2026 01:49:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Tue, 07 Apr 2026 01:49:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62643310ed6f3c97acf60d4e47ee38ccfc6444878f95c3fbcf15be3ec223f47e`  
		Last Modified: Tue, 07 Apr 2026 01:49:24 GMT  
		Size: 184.0 MB (183999053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jdk-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:cd865971a0934d71c3c6c3b6d4c159cb16eb39c550a5df3186b264623a1ac8cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07be1a609f5eae5810474f1fceea2d45fd0a991d98c0fd26f13e53423ead9f3`

```dockerfile
```

-	Layers:
	-	`sha256:463900a5ebd2c350586fb22f4a833662d53fde0fb0092e042fd383f4feac9e09`  
		Last Modified: Tue, 07 Apr 2026 01:49:20 GMT  
		Size: 9.6 KB (9619 bytes)  
		MIME: application/vnd.in-toto+json
