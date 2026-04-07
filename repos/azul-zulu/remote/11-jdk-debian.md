## `azul-zulu:11-jdk-debian`

```console
$ docker pull azul-zulu@sha256:908a367283170e54ddb7723a7688d0ccc22f945f0cc09fd6f6dd4253b3eb66b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-jdk-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:fdf1a56976d9059c5d75844abea4c5d00bdf65d0b7e130d1b39e129faeb30f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.3 MB (178267267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b37c26fd27272b0159d18f41b7133059b8963dca56d7e4890ed06f9371854472`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:44:15 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 07 Apr 2026 01:44:15 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:44:15 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.30-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 07 Apr 2026 01:44:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Tue, 07 Apr 2026 01:44:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94f36dcb7defacc693ce3b9e65b8bad27fb3a0103a285a2830566fba43d5d05`  
		Last Modified: Tue, 07 Apr 2026 01:44:29 GMT  
		Size: 148.5 MB (148491627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jdk-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:8681d7a639cde45c626c081f8a81d9428d1b6ae3037cbfe4eb909d5ee3c092a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5661120b6de48fe9b214cf5f72e6d633becd2672d655aa54ed62c12465273a42`

```dockerfile
```

-	Layers:
	-	`sha256:e28dff09cd29912ff807dd18e93ab1395384ce38f9d45a7d2dc255c54e9e2bbf`  
		Last Modified: Tue, 07 Apr 2026 01:44:26 GMT  
		Size: 9.5 KB (9507 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-jdk-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:a8d93f305bdec4d483d6a4c8fd5ee09b8ada40a32f33067eb48ee5ab3e906c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.2 MB (178233132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3937d063275c3069ae8ef3c745d8c3227f40f9db24ac0f1dbc84a7aec74030f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:47:25 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 07 Apr 2026 01:47:25 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:47:25 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.30-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 07 Apr 2026 01:47:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Tue, 07 Apr 2026 01:47:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8909b9ee467936e330309964a0e3a65472733a53e2a0a0434f3d65e5f823619`  
		Last Modified: Tue, 07 Apr 2026 01:47:40 GMT  
		Size: 148.1 MB (148094581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jdk-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:9990b9e0768d165c5022dfa89c9f3106d4e4437dd4b4906f92038762d249e831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74eb2fce3cef28489d1bee0c14ea03de3822e13f9faf203ae5c311b041d7db1`

```dockerfile
```

-	Layers:
	-	`sha256:f12cb07e5cfe23312958eeccf7080069fb3b35fdd25fd2f7781539f9fb11c65e`  
		Last Modified: Tue, 07 Apr 2026 01:47:36 GMT  
		Size: 9.6 KB (9623 bytes)  
		MIME: application/vnd.in-toto+json
