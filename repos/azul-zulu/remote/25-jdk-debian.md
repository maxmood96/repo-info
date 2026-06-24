## `azul-zulu:25-jdk-debian`

```console
$ docker pull azul-zulu@sha256:672ad51f98a1559d1c6dc6ce86f5f34b87a71d2767838b1ac987584e62eb82fc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:25-jdk-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:008c887e622b6e3eea8e2942a86a5082c1ac2b44d59207386ff22bd3d933d002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.0 MB (214954143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:145877aa512bb88faed2f11efbaa8377ece1c6765880e4b2828814a3f5d482f5`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:40:45 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:40:45 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:40:45 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.3-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:40:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Wed, 24 Jun 2026 01:40:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ceb4c98e5808403a25b8024a370450924b84642afe87f9aefef290dc9901d08`  
		Last Modified: Wed, 24 Jun 2026 01:41:04 GMT  
		Size: 185.2 MB (185168724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jdk-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:bcf31bdf13f60de06cadd8d4a555767469f4b8311ab4110fe14f25e417f88fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfef9e4bc5b4c6f05f79beb9cd5d54dd1e19945d3952310df4d9fdbb63518516`

```dockerfile
```

-	Layers:
	-	`sha256:d30e4a74a0136275f0650398c99dd5e0d243d891a8f45d91b76d3a2844fc701a`  
		Last Modified: Wed, 24 Jun 2026 01:40:59 GMT  
		Size: 9.5 KB (9503 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:25-jdk-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:e1da3dda90fd309dce04447a5abf4c9cda3b3559d37dbd489ba6b37635e8551b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214455310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01a91c8ab1ba845e50d4c01b1921a890ad2dcf40ca4f29f1ee23e23b9f1c1fb5`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:43:57 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:43:57 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:43:57 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.3-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:43:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
# Wed, 24 Jun 2026 01:43:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42699189caa0d1acf52f70477f32607327e6ca65dac476c0847abf893876b5e`  
		Last Modified: Wed, 24 Jun 2026 01:44:15 GMT  
		Size: 184.3 MB (184306759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jdk-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:89fe5ae9213452ba14e45e78319513280254c4265f237d6919e060a1b7dd7fe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ff77ebc5f257ff4d50b580a2bd74f09fa452a3038febe0fbc3b4d606df4d48`

```dockerfile
```

-	Layers:
	-	`sha256:ebf7b7af3df236a0e74ae8687de01616c95ff1971b56bd14473e9110d69089fb`  
		Last Modified: Wed, 24 Jun 2026 01:44:11 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.in-toto+json
