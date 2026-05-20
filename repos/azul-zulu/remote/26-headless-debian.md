## `azul-zulu:26-headless-debian`

```console
$ docker pull azul-zulu@sha256:e63bb5b1bc198f6764b53310d4bd2ca5c0f775367781dc9be753664804cdb474
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-headless-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:7635d6b4d93b1492b2a3241579b5301c6d1fdb9169b9e084b491290d57b5de89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.0 MB (215021414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deaa7bc4fb52107f6fa464aa1e363ab0c80b9a4d665469a33520645025cfca73`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:22:42 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 19 May 2026 23:22:42 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:22:42 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26.0.1-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 19 May 2026 23:22:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Tue, 19 May 2026 23:22:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4356a5ec4b59afa3e98411f695c19729be9801b4d5d7596d1ad4b6df1bf4328`  
		Last Modified: Tue, 19 May 2026 23:23:00 GMT  
		Size: 185.2 MB (185241488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:856e5ebce8a3efa6a102ce45271933074135b35be45759803618c2a7cfab8408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80300ca664b1d4337f89403d40581a4c263c3413fbfed53d7e7a102524ef03d4`

```dockerfile
```

-	Layers:
	-	`sha256:9662aaaee6aa4267e689983f377cbb452479632a8d214e2be94699f34c0bdcf2`  
		Last Modified: Tue, 19 May 2026 23:22:56 GMT  
		Size: 9.3 KB (9295 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-headless-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:b822c99acc775d3e3ccb68e3b6a489efdf03993f4cb7bec4b7733e6115a5fe7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.1 MB (215089576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbc4b57683b088ad395acb26910edd6fd240ab77067559aeb6e1ff4913c53326`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:26:25 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 19 May 2026 23:26:25 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:26:25 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26.0.1-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 19 May 2026 23:26:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Tue, 19 May 2026 23:26:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9df71de1a19702edb4c119ab2765d36075acbb00fdb7a21600f65160ca9e68`  
		Last Modified: Tue, 19 May 2026 23:26:45 GMT  
		Size: 184.9 MB (184947657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:bb6f59aaeb8f5e3ec2074a55ce12b6a7352be19902783f957675896774b328f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02cbb40ca3aff49d49b79849c9439d0d9ab3a0802fcdf758caca89c92286882d`

```dockerfile
```

-	Layers:
	-	`sha256:8876ee81a678babf6e9f6845b1214be50c00d63827a5360d50850c88785d7e6f`  
		Last Modified: Tue, 19 May 2026 23:26:41 GMT  
		Size: 9.4 KB (9399 bytes)  
		MIME: application/vnd.in-toto+json
