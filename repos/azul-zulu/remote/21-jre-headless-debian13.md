## `azul-zulu:21-jre-headless-debian13`

```console
$ docker pull azul-zulu@sha256:9d2510c05e415c9eaee093da55b48eef8fb39680a1e471a319bac108fdb86454
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-jre-headless-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:501dfc39bb0f68a69db495df3a5df7152da4236e63bd72ac0d51a3eb8bf4ada7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104610610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85cf864120c30814875f9130fbc3b95e9d0b8b1d780fd86f80983606af3d3d31`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:40:37 GMT
ARG REPO_HOST=repos.azul.com
# Thu, 11 Jun 2026 00:40:37 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:40:37 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.11-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Thu, 11 Jun 2026 00:40:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ae076e1646c204597ee6bd05dbe5db99b8de022e369b08261b931ba494606a`  
		Last Modified: Thu, 11 Jun 2026 00:40:50 GMT  
		Size: 74.8 MB (74825195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre-headless-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:e27443f33baefe3ea88016f3c1241fb88d40f7329ba0eda78f949406070c8f41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d1500110b5064de515e92c0aa18e1bfbb9cf15ebd951540b6e2c342329f3116`

```dockerfile
```

-	Layers:
	-	`sha256:d2c1abbb9456ba765fdd7dc09d9e7058ef1fd645529552a10e5e34a2ea5b5bf7`  
		Last Modified: Thu, 11 Jun 2026 00:40:47 GMT  
		Size: 9.3 KB (9301 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-jre-headless-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:e877f95902e1feff207f90204c5fc81b889168cb418bacc61d6006f79f627eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104640590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a42b689deee024a77437c01e96ede8eb938312de5781ea3834cbdc31c8f0b53`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:42:33 GMT
ARG REPO_HOST=repos.azul.com
# Thu, 11 Jun 2026 00:42:33 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:42:33 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.11-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Thu, 11 Jun 2026 00:42:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493b0df00efe6eb42513642ab01dd4729433632f7fefda0b4c762639ddf29a88`  
		Last Modified: Thu, 11 Jun 2026 00:42:45 GMT  
		Size: 74.5 MB (74492060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-jre-headless-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:20c7eeefbb256ca2bbde778898f494e9e5b8d81f0ae7f988f0b9844553c28a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b1459a24069d05bf508571bf5154825be15c5d5cb74ab5f889f564be0390f7`

```dockerfile
```

-	Layers:
	-	`sha256:a3e48384e1ba32ae8159ef3b16a0ca8478ca522e20edb5128c9dc757c1e298f7`  
		Last Modified: Thu, 11 Jun 2026 00:42:43 GMT  
		Size: 9.4 KB (9405 bytes)  
		MIME: application/vnd.in-toto+json
