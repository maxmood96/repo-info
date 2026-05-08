## `azul-zulu:17-jdk`

```console
$ docker pull azul-zulu@sha256:ca18d5fef72c03c6bd63bd6a9ca3dfac55612a6743981c5ef9fc5d7e5f53199e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:17-jdk` - linux; amd64

```console
$ docker pull azul-zulu@sha256:faaa4184a5465cf4f29aa9b52c22561c8f858944a9858c00ba7dd1c85836c31c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182585713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2ca31c98217481b43c7f063791d526b400823f318d58f0ea790084fa8320549`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:38:03 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:38:03 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:38:03 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.19-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:38:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Fri, 08 May 2026 19:38:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed35589859e2b268e2b1131ffc26fd13ae775f917546653a5255381590bf4a99`  
		Last Modified: Fri, 08 May 2026 19:38:19 GMT  
		Size: 152.8 MB (152805487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jdk` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:a33de50aa8ae3147704c59e55dfde92ef66a3d3f1c36ed6793cb707769326700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6168029d5b18b5929263ca6690e1ba76c30ed531f1e48c06b8fa039f3300d05`

```dockerfile
```

-	Layers:
	-	`sha256:3501308910b8136f4ebadab12f53a274644d5dda42bda547ec22c80a3325f6b4`  
		Last Modified: Fri, 08 May 2026 19:38:15 GMT  
		Size: 9.5 KB (9507 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:17-jdk` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:fa7fa34ad35fac816ed8f00ae3ad1f038b6c02c59ffc2d0e078f0fd3a369ec61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (182961422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e2eac5170b3ed0dbeb7172f36f8dfecec8946dc676a1dae8c09809ecbaa7764`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:40:16 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 08 May 2026 19:40:16 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 19:40:16 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.19-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 08 May 2026 19:40:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Fri, 08 May 2026 19:40:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbaa422f8961c87c3437453c7855f42923c3db3dab25d7fdad767a28c79593a1`  
		Last Modified: Fri, 08 May 2026 19:40:32 GMT  
		Size: 152.8 MB (152817780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jdk` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:325245359b536c30bfa068a679e389c356ccae961639389cfc3b02efca2a1a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6754bef743cd93b3aa70e03ec92d9762caca721e141729a1d60906216cf24dd`

```dockerfile
```

-	Layers:
	-	`sha256:9a95c637ef4e7f2a4a5295f30db9dd4ab6bac4566eba321718cbddd2d0b714e4`  
		Last Modified: Fri, 08 May 2026 19:40:28 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.in-toto+json
