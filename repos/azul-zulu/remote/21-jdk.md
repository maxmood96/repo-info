## `azul-zulu:21-jdk`

```console
$ docker pull azul-zulu@sha256:c4fe63bb96ca08d6785a59e56f465e5d01121e63f3f4e0fb56df9bde6c3f6809
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-jdk` - linux; amd64

```console
$ docker pull azul-zulu@sha256:22c38594ed386d9b555ef6349abaacab2cc4271535274ec73b3ec12f3bc941d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.9 MB (195880919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d5effc7d7f0f089d6ced9bac02eab2fed8f8d5d597dff008a2b225aebd8262`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:39:58 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:39:58 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:39:58 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.11-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:39:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Wed, 24 Jun 2026 01:39:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4837a83174bfb515a2d236127f6198fec8c3ae562a2c8fc771621713bcf947`  
		Last Modified: Wed, 24 Jun 2026 01:40:15 GMT  
		Size: 166.1 MB (166095500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jdk` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:a2b5d2ed75fa8a0af953954a47d6455525263c52e7eefdb1caa6e3c93a8d73d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1780bfc5c271b159070928b80d8c33c6f98d81cf1dfe74dddb9535f06c319887`

```dockerfile
```

-	Layers:
	-	`sha256:fd5038a06fa3a0415ffcc307cecdf91da10c26851ea4a9d846402f4c03ce6282`  
		Last Modified: Wed, 24 Jun 2026 01:40:11 GMT  
		Size: 9.5 KB (9507 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-jdk` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:8f57b69bc912497d71ccb5c93ee3ebc9bd6d435979d54691c3fb38a74e94db35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.5 MB (195548714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66d7cceb7723c446b46a9ec2f6601e40e02b6e2833552af939803e722f3b5fca`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:43:15 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:43:15 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:43:15 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.11-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:43:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Wed, 24 Jun 2026 01:43:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc288f14005074db27a32cd38b2d9f0e0aeec01f8f9d8253a3b1591fd0daede5`  
		Last Modified: Wed, 24 Jun 2026 01:43:32 GMT  
		Size: 165.4 MB (165400163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jdk` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:578301f72937827f34007ab5e24515b43fdbb967ab1a51d8c740eceb19a0e8df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab164abcc50c25d537a642c3297efa001e166049fd4d6a561fbbff821f2296be`

```dockerfile
```

-	Layers:
	-	`sha256:a746bead8330a7ced840859cac1fe61e25a14dfc93ed3884dab0b515c4a283a1`  
		Last Modified: Wed, 24 Jun 2026 01:43:29 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.in-toto+json
