## `azul-zulu:25-jre-headless`

```console
$ docker pull azul-zulu@sha256:44658225d543b3bcb7e61b655c68c81a2b335ead25bfd180e62c7d6d7bd8a461
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:25-jre-headless` - linux; amd64

```console
$ docker pull azul-zulu@sha256:d65650c6003aded8d04a74bf7f3bb0b571857680012be49aad40f75b196ed73d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.8 MB (118774572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2a38560597c0eafe0e702e86b7be99b98dcae036fe52afad481ae4f970affaa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:40:49 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:40:49 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:40:49 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.3-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:40:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a482ca1b85ca74c1e7f1b2702f79fa947707417f4548c5fca84993eefa776c8f`  
		Last Modified: Wed, 24 Jun 2026 01:41:03 GMT  
		Size: 89.0 MB (88989153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jre-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:bd0f178f481718b8fe7631ac61c7be7c85799d4fef86a548926ae217b29fa925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec6c5eca30fd351b3046d2a64c4afef5a3a4b79d1788a56510e0907c20cb4f7`

```dockerfile
```

-	Layers:
	-	`sha256:0475e77270303741ff44280d35405f89b2440f9d2887ad300331eb48159e0028`  
		Last Modified: Wed, 24 Jun 2026 01:41:01 GMT  
		Size: 9.3 KB (9298 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:25-jre-headless` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:328e2ad8ad9de51e3d5f14e550965a0fe7a1d7819bd46e274241a626edbe8451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.7 MB (118745787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b855610e744aaf92a5b313ba9b4e0a80acb784779c7eeeca622e673956801f3b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:44:03 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:44:03 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:44:03 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu25-*\nPin: version 25.0.3-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu25-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:44:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu25
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07bcad1ea10ab628d5d145e09eb64b85a6ef93754ca1400e62f7cffe2d66733`  
		Last Modified: Wed, 24 Jun 2026 01:44:18 GMT  
		Size: 88.6 MB (88597236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:25-jre-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:b8d4712c053d9b959112239f187d828e63ffce030192f88fd0f5938d49e7f766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ce0881fd7e2e25bdb811bac730e102ee9e40b65793890028376346b403137a9`

```dockerfile
```

-	Layers:
	-	`sha256:b68e53c63353912305982b9e2ecfbc6d173c26101fd08e7e5363b0cedd5b0c02`  
		Last Modified: Wed, 24 Jun 2026 01:44:15 GMT  
		Size: 9.4 KB (9401 bytes)  
		MIME: application/vnd.in-toto+json
