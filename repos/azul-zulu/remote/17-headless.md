## `azul-zulu:17-headless`

```console
$ docker pull azul-zulu@sha256:054058ace5d6cc7bc033b5e3fb224ac341b56d55aa5cf1951c06d1a578da6539
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:17-headless` - linux; amd64

```console
$ docker pull azul-zulu@sha256:3418be8a79b00f375be39e9baef72b3003c97e62783f14ce201f13b9ba7fffea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180297486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d2a93c877801dd9fc015dbcd0bc567bf5fbf3bb3ceb6b00d707818c6433339`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:20:39 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 19 May 2026 23:20:39 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:20:39 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.19-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 19 May 2026 23:20:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Tue, 19 May 2026 23:20:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c9b24ed3e5c82ecbd92b5c2ac7df08783f733a495bb6576301fdc2d6c28ecd`  
		Last Modified: Tue, 19 May 2026 23:20:55 GMT  
		Size: 150.5 MB (150517560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:501086229f29b302da347d8167357c8c4271a9033630dbbc8369b3e0bdd1b277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:220f50d577623d27f74d2baca4c8a7faa3e998948732bfe04c8ba55d25737fe7`

```dockerfile
```

-	Layers:
	-	`sha256:711b885f37da47c2656ea3019d26253f6d7aa2a3144a7899b951d302a343136d`  
		Last Modified: Tue, 19 May 2026 23:20:51 GMT  
		Size: 9.3 KB (9297 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:17-headless` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:7871a40ebba2883a134698e7ceaeeb0beb3cb69ff42841e82d13226bf2d27a82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.7 MB (180700171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56cec3387bdc12e3a1d0a03a27ebd046724f1d9513280b6737c47d72e23960b1`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:24:25 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 19 May 2026 23:24:25 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:24:25 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.19-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 19 May 2026 23:24:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Tue, 19 May 2026 23:24:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b1407860dedd8394b54adb471c63f477cfa4fab886f2e5dfa876deb90e27ac5`  
		Last Modified: Tue, 19 May 2026 23:24:42 GMT  
		Size: 150.6 MB (150558252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:5732a162c35a2f346ef839d818367f4b7b1dedcd2ed2d9968d7e5d43bcf73a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adf6615cf16312c8318d2d1005865dfd4732b53f1e2221b0cd06904684886934`

```dockerfile
```

-	Layers:
	-	`sha256:2199f7c982783cc8bbcdf83239b9f94bd375c1c10aa0e5bb4f9d06893a99310f`  
		Last Modified: Tue, 19 May 2026 23:24:38 GMT  
		Size: 9.4 KB (9402 bytes)  
		MIME: application/vnd.in-toto+json
