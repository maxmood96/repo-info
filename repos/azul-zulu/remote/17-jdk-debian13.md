## `azul-zulu:17-jdk-debian13`

```console
$ docker pull azul-zulu@sha256:247acaa0de956284251d058ba2e1ad96877fba6ede6c7ef6f57afb67e02a254f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:17-jdk-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:ffe351b7460d746d28fe33f890ba6ac8f7ac8c303d5e4a1c249f913df550603f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182586087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4707d13524e66725ab8945c4a2596f195befe5b8a172bc4cf58dd146fca59ad6`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:20:17 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 19 May 2026 23:20:17 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:20:17 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.19-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 19 May 2026 23:20:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Tue, 19 May 2026 23:20:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47123de37082c6717132b85073ba31a991d4d65edf87e4f9e7e7def94a69e5d`  
		Last Modified: Tue, 19 May 2026 23:20:32 GMT  
		Size: 152.8 MB (152806161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jdk-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:3d1e84bd7a3f978e4cb6578d85d7b8e4a823f5cfaeef8e98f7d301ad9bb59047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62eac696e4b89583024794f638d7fdbc4fdedf93f44c7ceb86b63f054db1a278`

```dockerfile
```

-	Layers:
	-	`sha256:2b3941694fd02dc914755b4dd1037498f5ec8e3b8f6f2984f314e853f35bb2fd`  
		Last Modified: Tue, 19 May 2026 23:20:29 GMT  
		Size: 9.5 KB (9506 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:17-jdk-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:51048c22eb2be54340d88abb6988efd29e347bf5eb8d8a67cf56a01a90b89a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (182961488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b2686d2706bd61a2ffa9726b7ddb975d7d3e25eb79a94bb4594e878764d17a`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:24:24 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 19 May 2026 23:24:24 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:24:24 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.19-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 19 May 2026 23:24:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Tue, 19 May 2026 23:24:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b3cd68874fe1587f578d3e409519cf081739c7e13ba8871a3874f638469b44`  
		Last Modified: Tue, 19 May 2026 23:24:46 GMT  
		Size: 152.8 MB (152819569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jdk-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:ff8fdd5fc22833d845bb0799545c7e096d70b242b8cc11e43006bfefbbbac982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b0411b7319846fc3de078725f729db31a2e8a72a5faec380ae659327a68e1d`

```dockerfile
```

-	Layers:
	-	`sha256:f9063a2f5dc7e7c1449df919c3a50ebf13695d806db447e6170c9614272e6af2`  
		Last Modified: Tue, 19 May 2026 23:24:37 GMT  
		Size: 9.6 KB (9622 bytes)  
		MIME: application/vnd.in-toto+json
