## `azul-zulu:21-jdk-debian13`

```console
$ docker pull azul-zulu@sha256:5302e7127e85a0cf99c7752de559363f767f51ccaadb8228f808553cbbca47b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-jdk-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:c08ea598efb738ed4c67c81f1b2c33e52996ac083f0640730d598415e88116be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.9 MB (195875310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3bf1c8b37b1c406e0b8feb28eab0a589d416de9a9cb96b319bed010541f6ba7`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:21:01 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 19 May 2026 23:21:01 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:21:01 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.11-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 19 May 2026 23:21:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Tue, 19 May 2026 23:21:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a4a3eb7e8ea07bb854bd0dcfac004e581ed0de6a6cbf732e9d8ba13b24d8d6`  
		Last Modified: Tue, 19 May 2026 23:21:18 GMT  
		Size: 166.1 MB (166095384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jdk-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:d9e525578ae2daea30388e0b586ee0aa1dea602eadce725d04b6a6ba08027ff1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a879958eae9a4e45da59042381616f7600dc72d2cb282ba17b395d0bd8a2048`

```dockerfile
```

-	Layers:
	-	`sha256:d11966d302fbd6e9daebc2b9c5ba87e108612dcc4b690badd7743d607cd1ab44`  
		Last Modified: Tue, 19 May 2026 23:21:14 GMT  
		Size: 9.5 KB (9507 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-jdk-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:8d6e78ad448217cad457f737438e626f6a523b3a62cd9a1e652eaf7f2680e045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195541996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3183d08a8016d06e5ed6352772cdce869bbd094c2546dae2ad62abda8eb00e19`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:24:39 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 19 May 2026 23:24:39 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:24:39 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.11-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 19 May 2026 23:24:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Tue, 19 May 2026 23:24:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ef66a1c1e346bf2978f5dc24cbc981cbe9444f7e0ac52c8c67c78415d1f649`  
		Last Modified: Tue, 19 May 2026 23:25:00 GMT  
		Size: 165.4 MB (165400077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jdk-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:1413cead6cf2fdb03104616284b4dbd119c2b9777e54e842e442bb9eaec9da38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095939036cbc7f1d28521304049ad0b15dca5fa6b142037d44d317e21b8cc92c`

```dockerfile
```

-	Layers:
	-	`sha256:9938336e8e87069fc023a73beb4466f94420a57b9c335e1c380b9ab1f003ed48`  
		Last Modified: Tue, 19 May 2026 23:24:53 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.in-toto+json
