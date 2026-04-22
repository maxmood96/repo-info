## `azul-zulu:26-jre-debian13`

```console
$ docker pull azul-zulu@sha256:6431199449dae925fb68fc55b0bbb32fb284dd0387a6cde43dfee51086d61ae8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-jre-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:62db72d264f6cc9eb12ef60cde8b5b8859ba3894fe99e599baad426bf24c7805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121914277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155b9c5072d2b3d652abd0d3395f042dbaf433a41290c5f99c78e0ca2d250794`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:39:44 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 22 Apr 2026 01:39:44 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:39:44 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26.0.1-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 22 Apr 2026 01:39:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd8d8d132da79faffeb4362c7aa2c294617cbe7cfb911972a047f18c010c8a1`  
		Last Modified: Wed, 22 Apr 2026 01:39:58 GMT  
		Size: 92.1 MB (92134103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jre-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:f1acb12fbbefac50a7084889bb7407d1d949811b30507b65e9d042761f2d7d15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58be1b09cf5a02ef7fbd93208d1a8a13ae87fb8da13c51bde9c9e753f3a9e707`

```dockerfile
```

-	Layers:
	-	`sha256:6a9b54801495d112637d05af603ef4c27dff435d43501c031a2642e3f751b0b1`  
		Last Modified: Wed, 22 Apr 2026 01:39:56 GMT  
		Size: 9.2 KB (9187 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-jre-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:2609f49c6ff34c4886bb87a51b653c5806d2df018b8025a117b7373771f5c72d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122183206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ca02ac6b3c6fa1e88c4839026e0414cd00375cf9d148f77d49958d26664a80`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:42:58 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 22 Apr 2026 01:42:58 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:42:58 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26.0.1-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 22 Apr 2026 01:42:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:445f85807227808429497264a6281aeae4f422f1e17acd64caf68bd2e336e706`  
		Last Modified: Wed, 22 Apr 2026 01:43:14 GMT  
		Size: 92.0 MB (92039600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jre-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:05056d7b20ba327750df8c367d044fbf82ece4385cd86cba1dcbf15f9e604a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52eac3d3ac388d345e25d7835a806aa0246e855c14a13a71c2abb6928e51bc68`

```dockerfile
```

-	Layers:
	-	`sha256:4a8c691a94fe2c7f7f56d91c69040ecf91874b5cf78104ae0a0ef24a42a00b54`  
		Last Modified: Wed, 22 Apr 2026 01:43:11 GMT  
		Size: 9.3 KB (9291 bytes)  
		MIME: application/vnd.in-toto+json
