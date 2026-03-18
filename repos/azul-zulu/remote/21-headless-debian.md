## `azul-zulu:21-headless-debian`

```console
$ docker pull azul-zulu@sha256:8aa1ae51d9c42ef0eb435ccc86a6d677f4817e0855ee173ffdf19abc371a10a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-headless-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:741a18b299fffb5bf9e3a4d8ebf40bb766d1c132662a4aad1fb5ebcb00abb8e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193346387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:587179eb15053586692db199fe32ca401f0d101b3e10df56244c78079afae4c9`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 22:11:58 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 17 Mar 2026 22:11:58 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 22:11:58 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.10-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 17 Mar 2026 22:11:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Tue, 17 Mar 2026 22:11:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82344434136836674cf14335869ce0853b73e011eba86cc5c1da6d7ad90d2921`  
		Last Modified: Tue, 17 Mar 2026 22:12:14 GMT  
		Size: 163.6 MB (163570887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:2581bb18db7e3e85f3afa814cefc1c5946c635ceceafb0c333523f954a35094c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccd9d411d7eb4cf19aff88b45fd7c41e88d40bb2c316e8a895bc9e16941c973a`

```dockerfile
```

-	Layers:
	-	`sha256:8a85f9415f7bf29276c4c78185c6d9a67cc73eab8ab047941fe74587dfdc4f69`  
		Last Modified: Tue, 17 Mar 2026 22:12:11 GMT  
		Size: 9.3 KB (9297 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-headless-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:595f097e75f4b8d5b8b2a1d04ee07865842dbaa9089c76d7ad2f3e18dd4467f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (193014638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e3e312265450bd02d40ac26bb5657f55f2ed5df7b2abde7643f87037943cf7`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 22:12:00 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 17 Mar 2026 22:12:00 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 22:12:00 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.10-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 17 Mar 2026 22:12:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Tue, 17 Mar 2026 22:12:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952c9227794302c39accfb4621064aa1608328d13ab227084e0fcfbec98722c9`  
		Last Modified: Tue, 17 Mar 2026 22:12:17 GMT  
		Size: 162.9 MB (162876222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:73c28009b33168ada856d6efd486442d246145ac30dae2c046ccfc8bbbf5d504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:190209dd40694f25910daf9054d4e9ba941eaefb793df76a8801732ab050fcd9`

```dockerfile
```

-	Layers:
	-	`sha256:03f8d59fcb8ac10f6c6509475fddeb411e3af089becccc8cfc8f1fc1d705f32a`  
		Last Modified: Tue, 17 Mar 2026 22:12:13 GMT  
		Size: 9.4 KB (9402 bytes)  
		MIME: application/vnd.in-toto+json
