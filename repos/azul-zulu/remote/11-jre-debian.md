## `azul-zulu:11-jre-debian`

```console
$ docker pull azul-zulu@sha256:dd0846969fbec79076794bffb0fb39c2f823e5ce95d33ccb82b18459b0db958c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-jre-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:57eae6658625123ec073967f6016d546cfd97f6cfd397bed960ba6ea476c43e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96898679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ffef13d2fc7eb17905cc047e2ca60e0168729e1daff593753c93f87511215b4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:37:29 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:37:29 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:37:29 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.31-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:37:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae71f66511d431a0ea4b42309b4bb245f353cc4f67beb3a5d9495f4627c3981`  
		Last Modified: Fri, 08 May 2026 19:37:40 GMT  
		Size: 67.1 MB (67118453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:24aebb901e63b6b7646bee5fe55ef97a5e8c8acb613a5b09101c5b4d51c5057d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3df51489ef2ccaad697b820e00bddc76ee0b34eed7d51492f69ed626e29b4e00`

```dockerfile
```

-	Layers:
	-	`sha256:edf7b2c0f782c73c262b5a79459a620ef3740c5b66f40eec0537fc3c1c4c9d22`  
		Last Modified: Fri, 08 May 2026 19:37:38 GMT  
		Size: 9.2 KB (9190 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-jre-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:317fca48d012874ed5b8d84bd0cb275643f33487f77da8d5d72f2f824caa5d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97067555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8523301f665e6f49cc48c5e2c275019bab6ba7368224f94ea40977f91d34d5e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:39:34 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:39:34 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:39:34 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.31-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:39:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019d540108852388ba2833f8e30974c653b4dd577cae7f3bb3958b5f29295d7a`  
		Last Modified: Fri, 08 May 2026 19:39:45 GMT  
		Size: 66.9 MB (66923913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:7e4983dec7ff10f90cd6c845a3b22d71f04f13b8c1d464eafc208be0147b8a8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd17ce18c28e7b6881cffbc4d9a7b5716fa916ae38264e7744011ca27ce27eb1`

```dockerfile
```

-	Layers:
	-	`sha256:3e3ef8442471699c57b67014c4b243e6d8400f58feabe803892e10583fbc83c1`  
		Last Modified: Fri, 08 May 2026 19:39:43 GMT  
		Size: 9.3 KB (9294 bytes)  
		MIME: application/vnd.in-toto+json
