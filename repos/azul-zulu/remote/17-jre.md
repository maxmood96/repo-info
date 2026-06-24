## `azul-zulu:17-jre`

```console
$ docker pull azul-zulu@sha256:38a645954002ec0581a0b29bca11d4c7428eaba8c9155aabee0908d0a688c354
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:17-jre` - linux; amd64

```console
$ docker pull azul-zulu@sha256:a2629e88d1dfcd8b1d35252c12e4e0c62111514c22074491e43ea4d86f735b74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101409969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:758a9346e577e217f40acd6c6bc5ebd5ca0731aa4ace0baf05713ea3621500af`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:39:16 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:39:16 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:39:16 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.19-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9cc7f76a766212a1e415e3c358fbb0b956dbc8fd8cb190b9c01367acaf02dd`  
		Last Modified: Wed, 24 Jun 2026 01:39:29 GMT  
		Size: 71.6 MB (71624550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jre` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:5327ead791d71d848a7e9093aef42bad17fb169952d3880b1a880899b47445ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adcc6786b1fc338c40d99d882305b1b68778c4eca0bab172270c8f06296e78f3`

```dockerfile
```

-	Layers:
	-	`sha256:ff8251e94370736a1f367012e83c7990379dfb0c7e20ec637e8e75d17ccaa8fc`  
		Last Modified: Wed, 24 Jun 2026 01:39:26 GMT  
		Size: 9.2 KB (9189 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:17-jre` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:5b13051728c10bdf812de38c3215fe01b59c329d62beea15fb139c00bd8b6886
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101805764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2454dc146c93dadb123b8760a666ce29bc68603430b1156e934140ae496b2b21`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:42:33 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:42:33 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:42:33 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.19-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:42:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8362560b8f8fb55927ff20f8edbab471d4c24bee0de85d2c8c91e9fac3d95b`  
		Last Modified: Wed, 24 Jun 2026 01:42:45 GMT  
		Size: 71.7 MB (71657213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jre` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:a6e65114473acaf61bc40292e38726e4b1f57c9db64b2907edd661de18d612e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c182122835f4515c0c10c61df00e1fe5996953cfba1a367e493e15cb83d7b28`

```dockerfile
```

-	Layers:
	-	`sha256:83cf3b5b8ca3bc4f1e91efaaa7a5b72c1761c5a93d62969bccdc7b78332065b0`  
		Last Modified: Wed, 24 Jun 2026 01:42:43 GMT  
		Size: 9.3 KB (9294 bytes)  
		MIME: application/vnd.in-toto+json
