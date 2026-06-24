## `azul-zulu:11-jdk-debian13`

```console
$ docker pull azul-zulu@sha256:edc949d082d660da036c0dcb24855892e8a8b003194527e0d6aa57d88db5c5d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-jdk-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:46fcbb40af0203413b84f4cd4aa79f36886bacca2a13a624f1f1496e170013bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.4 MB (178390992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f94e99815af27c08d68d1992da04579255b6fd599e714d92149d93db023b8127`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:38:32 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:38:32 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:38:32 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.31-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:38:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Wed, 24 Jun 2026 01:38:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e0a769f15cad24135f1aeb5d46613a58b0800ffee118b41b33345cdb46734c`  
		Last Modified: Wed, 24 Jun 2026 01:38:48 GMT  
		Size: 148.6 MB (148605573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jdk-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:dbe3f0b5c37b393767410f5aa9085eaf7fb70ae6fde42c403cab8d3473b02fa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d6af74ef3cd9799382c3fc55115adff5a4f85b44150215db6ffb83398e2e196`

```dockerfile
```

-	Layers:
	-	`sha256:a14b7e10aac25066d045572ba00be4b33c4d8b01b3e128bd79c1699756d8b1d8`  
		Last Modified: Wed, 24 Jun 2026 01:38:44 GMT  
		Size: 9.5 KB (9507 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-jdk-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:bbb375d668c5837076eb55846bc2f9bd7cd6bdb7d424524c2b8f091b44a559d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.4 MB (178431389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42f63e4da846593d3d971180e3b2c215c0ef25e72fd92a22bab49077fefe76a4`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:40:26 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:40:26 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:40:26 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.31-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:40:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Wed, 24 Jun 2026 01:40:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774306264af74e9b0fe2709776fd1c8933cb5013e7db9bb89b6396eb5bc87934`  
		Last Modified: Wed, 24 Jun 2026 01:40:43 GMT  
		Size: 148.3 MB (148282838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jdk-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:9286453d80d4e845a6e8eea87b9349db02c9a5138457e06ed4bced329a761678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:701d03c59c45b0f6d78efa497f8fbc4d1213fd21b28b32a7c6c32edd5d21d93a`

```dockerfile
```

-	Layers:
	-	`sha256:127aba186dd01f562861c9865753cc5b0750311474123f4a79aeee3bc2be8446`  
		Last Modified: Wed, 24 Jun 2026 01:40:39 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.in-toto+json
