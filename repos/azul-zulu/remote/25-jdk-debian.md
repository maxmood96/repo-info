## `azul-zulu:25-jdk-debian`

```console
$ docker pull azul-zulu@sha256:20c325fb07d7fa59ba7aae9106a0b8bdd96664332777ff4d8dfcffbe70900b0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:25-jdk-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:c1053031de0193bffb1cd02d15d82cd2528f23491f7079d125e2e8dea24be9ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.9 MB (214948684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb34f65f852f2b3db44e8b972133567e8547fa9b01a54e695c6c102ac3a8d590`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:21:48 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 19 May 2026 23:21:48 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:21:48 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.3-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 19 May 2026 23:21:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Tue, 19 May 2026 23:21:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990b033f18c9c6dae9a5a5f79d9c0b342566e51b2d00859167ec615b25365efa`  
		Last Modified: Tue, 19 May 2026 23:22:06 GMT  
		Size: 185.2 MB (185168758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jdk-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:48d5b1efaee1a19613192f2b0b9c9ee0adffe2d0b5790ebfcec5f11f39049f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:867c529cae4991e6cfca1ba48cf5af32dbab960b4f8df110a94f810fab0ab902`

```dockerfile
```

-	Layers:
	-	`sha256:88629d3c8b40a6d7f140b4beb9faee7452ed4708e44f0098396ec03cfb736b32`  
		Last Modified: Tue, 19 May 2026 23:22:02 GMT  
		Size: 9.5 KB (9504 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:25-jdk-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:d1946c42e05fdf8a6152cf2f3928cdf30ca818a9c05ae32c4e314b0563c99a65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.4 MB (214448759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af3d2b814b9a5a799da6a36db4d4b862081c19a02f443030d5cc0283c711564`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:25:35 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 19 May 2026 23:25:35 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:25:35 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.3-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 19 May 2026 23:25:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Tue, 19 May 2026 23:25:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd3b0cd3830cb757e982703e41479d06e3dc4a5de851e8a9c96d9f38d364ad3`  
		Last Modified: Tue, 19 May 2026 23:25:56 GMT  
		Size: 184.3 MB (184306840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jdk-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:19077ebfe1c45205ab9a0545e6662abebaaace428e8ace6822bf1cb0b483812e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea2f2739570187b6295725ca481eaf2d801be3f4477b6c2d11786e8d3010639c`

```dockerfile
```

-	Layers:
	-	`sha256:8a05f1225fd1fbdc95276147589df4d4df4b1ee959b48e170e7b5dd963cd6c46`  
		Last Modified: Tue, 19 May 2026 23:25:51 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.in-toto+json
