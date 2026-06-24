## `azul-zulu:17-headless-debian13`

```console
$ docker pull azul-zulu@sha256:69f7f84527b51eb2c8ca811b3475698bb1f462aa9f3c35cb2e7a372f1a87892c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:17-headless-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:6ca5855e1f20ae7205b14f1c1ea3d30f1c8b77f94c0bb721aa0f54520c01a56f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180303100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebd9a5788606131ada68c42db7daa37f6cba941fe54e077ca148aabf2a759e5`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:39:15 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:39:15 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:39:15 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.19-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:39:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Wed, 24 Jun 2026 01:39:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949544c7e7681b79b5f7d6b6d2c1e7d0b2c9a20beee9283b66d96e2fca88fdd0`  
		Last Modified: Wed, 24 Jun 2026 01:39:31 GMT  
		Size: 150.5 MB (150517681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-headless-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:7358bc8b8a6acc1a36e8f14854ed9dea9c8d7d80e15c16bb64a782b13b3e5475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c60bb64c02320cf0312fdfd6187515d824e3563e642b88fe73e50f5e368506`

```dockerfile
```

-	Layers:
	-	`sha256:2ee987632ec5186ba840bdda5f99ae0a0024ff22ae325a4a0fcea54a57222266`  
		Last Modified: Wed, 24 Jun 2026 01:39:27 GMT  
		Size: 9.3 KB (9298 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:17-headless-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:223b2282baec5a3d1dbd87b56f1af65697fe9dc54aa93256564e5d7795d6f751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.7 MB (180706882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:534f9786e91f95af38de177f5c5ffd4fae14a79b92cadc765809842505b01d49`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:42:05 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:42:05 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:42:05 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.19-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:42:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Wed, 24 Jun 2026 01:42:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8238dbc927f501d36ee4d4ff24280228b751cc09bc60daacc581432078793e7c`  
		Last Modified: Wed, 24 Jun 2026 01:42:20 GMT  
		Size: 150.6 MB (150558331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-headless-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:734311502f7469c29bcf69394c29d7f96e052f72136adfc2b6d43096437287e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b8b55fe07f7899f1b281da7d4330bfd12de8e51ec5c154ae26f584bd546e69`

```dockerfile
```

-	Layers:
	-	`sha256:8138db72a9acec0b7bbce4e1ff0d7b538f87d167c2b4576f19b556be8aa48de2`  
		Last Modified: Wed, 24 Jun 2026 01:42:16 GMT  
		Size: 9.4 KB (9402 bytes)  
		MIME: application/vnd.in-toto+json
