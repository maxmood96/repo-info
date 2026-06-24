## `azul-zulu:26-jdk`

```console
$ docker pull azul-zulu@sha256:7d0d62494b6e9d1e42d1ae1b2b0785d6d7afd296fce12f24b10194622b30c4a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-jdk` - linux; amd64

```console
$ docker pull azul-zulu@sha256:b56d1f1ace0f8b57d29e06b8c2318dc8b3fa2c6b9e63faab876a7ceb90496d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 MB (217231859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7521928f1a06b21e01761bfc7bf1e7d99e3baf3032769498e2fa01720eec5529`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:40:53 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:40:53 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:40:53 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26.0.1-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:40:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Wed, 24 Jun 2026 01:40:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f225ce653b1f312ec4b124ce74e1f20264700f38e02d08ead8172ee80fb65d`  
		Last Modified: Wed, 24 Jun 2026 01:41:12 GMT  
		Size: 187.4 MB (187446440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jdk` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:fdc2e38182ecba1e77fb8a7518388737794f46d965bc6b8122443cecd88f11b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9886b7d14f9b53e96e3ef00022d7386148f5c2777a25b68f262cdd78813798f2`

```dockerfile
```

-	Layers:
	-	`sha256:8a9a339cc517034db33a24b78d6ebeb99fcda857e0831fd1a35045e2fc20b220`  
		Last Modified: Wed, 24 Jun 2026 01:41:07 GMT  
		Size: 9.5 KB (9503 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-jdk` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:9f871e3d70017ee2a7696ff68861afae5abfeb0254803c477da98641e26240c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217276041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1ba74776e38d477923edd74babfe117a136080d5602eb1c206a93a2fed6a33b`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:44:30 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:44:30 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:44:30 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26.0.1-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:44:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Wed, 24 Jun 2026 01:44:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980262e8d5c11101c16230a89797c1841ae83ebf8d93e8541b97e82a30639a5c`  
		Last Modified: Wed, 24 Jun 2026 01:44:50 GMT  
		Size: 187.1 MB (187127490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jdk` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:60a81697a950f164e61cf7516658f922fc05ad215f9e6aa6ae15cb861e92a9bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550bc3eccf186fdd3c3dc59b4b4017bd2ab61dc101a3792251247de700428f58`

```dockerfile
```

-	Layers:
	-	`sha256:c158973ed23ec939f6dbe3cb21d0c8d326bee6e55dd31a875c24b09188b7282e`  
		Last Modified: Wed, 24 Jun 2026 01:44:45 GMT  
		Size: 9.6 KB (9620 bytes)  
		MIME: application/vnd.in-toto+json
