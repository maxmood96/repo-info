## `azul-zulu:26-headless-debian`

```console
$ docker pull azul-zulu@sha256:880435745d6497eb10e801305266a20df6489cf8e65916f80d8b81b0fc94fab9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-headless-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:26a2d8f9acae749b7ba9bd5c5eb1a2bb298b8b1dab61ee3eaa537bf2011c11be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.0 MB (215026936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2afd1291321fa8ef48bb90b788cd75e3c6c68776ed35ac78f8f66de0e82a4344`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:40:51 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:40:51 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:40:51 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26.0.1-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:40:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Wed, 24 Jun 2026 01:40:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda5be457ec26626499b64ca1a9e8501f6f876a20671dfa53f01575a4acc491a`  
		Last Modified: Wed, 24 Jun 2026 01:41:08 GMT  
		Size: 185.2 MB (185241517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:269789017e34d800c51369e897e7ec19569a4446b4aa54883473179b35f56791
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bf1b8939059784256c9cc61de6044588b610d2c3e23606e6015259fb0543824`

```dockerfile
```

-	Layers:
	-	`sha256:a1a8ac5277d44a06abda372020ddf960e1ae039af785ac35a486a138a99c4e4f`  
		Last Modified: Wed, 24 Jun 2026 01:41:05 GMT  
		Size: 9.3 KB (9295 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-headless-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:f9604dfc0e31058fcc0118ea8ffb809c3d25975a0e507d15afabf5e9c8e27cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.1 MB (215096193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:403b7c506be9d0820f48520a0ab331f6713168d379db2c0a7456bd0f2a9063ba`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:44:46 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:44:46 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:44:46 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26.0.1-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:44:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Wed, 24 Jun 2026 01:44:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df4ce4b2d46ac182dc6947b0c07d620b195a6e345384a8da2e76d9cc3124526`  
		Last Modified: Wed, 24 Jun 2026 01:45:06 GMT  
		Size: 184.9 MB (184947642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:3136451c0d3fd045fb2e690313147c0079aa4c2f9a6519089c837fd2419b9ca3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecbc79b52c94b403f0199322758f5f0ff944911a2b524d625452e68e1532417a`

```dockerfile
```

-	Layers:
	-	`sha256:9be02a564299b9e16fba1aae7bcbac8b5e7e73932494d00a69240868442e68c7`  
		Last Modified: Wed, 24 Jun 2026 01:45:02 GMT  
		Size: 9.4 KB (9399 bytes)  
		MIME: application/vnd.in-toto+json
