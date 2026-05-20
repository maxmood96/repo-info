## `azul-zulu:11-headless`

```console
$ docker pull azul-zulu@sha256:c86f22f328705a65e2c67806f8419d9f4507b81de2323c30596dad4c5cb8c2ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-headless` - linux; amd64

```console
$ docker pull azul-zulu@sha256:c927d3eba8895234b51a7d50a60f2a24db1afeba4ca1d2a0deead788391b5825
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.0 MB (175980420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087f9f3c9e9797f16ff50d9a92029e5bacabd2ac5b7d56a1d5901c2e0ba04cdf`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:20:00 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 19 May 2026 23:20:00 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:20:00 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.31-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 19 May 2026 23:20:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Tue, 19 May 2026 23:20:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce7b744801022733ccb9a1a58618180c584c0d68a1b187a0756b9eb5537bab7`  
		Last Modified: Tue, 19 May 2026 23:20:14 GMT  
		Size: 146.2 MB (146200494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:c85bf2eed927c343c4800a05f67cd7bea0a2340f7077a3c6b508f217d932d917
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959569d3fc655fc01debda916eeff7c1b3e79385842f80edd27d3f941b93e844`

```dockerfile
```

-	Layers:
	-	`sha256:ad4d237accf9789490f78091f491b7d90690016e04641d8033439fea01969e0b`  
		Last Modified: Tue, 19 May 2026 23:20:11 GMT  
		Size: 9.3 KB (9298 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-headless` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:c9a3c96676fb4dfa2c3d86387a40125cd2140e2e443e6127aac1fc5f78f66586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176052953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20fa67441a75922c4a4c3681204d673aa69cda2b06fc288c6c7c18b2fd7f1314`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:23:41 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 19 May 2026 23:23:41 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:23:41 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.31-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 19 May 2026 23:23:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Tue, 19 May 2026 23:23:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a16ab33b48b117a1a598ae1f2b649f686aa543e265b754a6135c15b2b3227c7`  
		Last Modified: Tue, 19 May 2026 23:23:56 GMT  
		Size: 145.9 MB (145911034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:2b691d4e3cb337b017c534e1d08fb90517ed8fa316577a029212eb61a86aa810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f008e9a207b3e9addb8e00074d95c6a872efaa75661936fcf933452b8b4f0e2e`

```dockerfile
```

-	Layers:
	-	`sha256:4deba88ff6e255164c17576441472250cf621e8cd9fb01d8f7aaa07239ac3ee9`  
		Last Modified: Tue, 19 May 2026 23:23:52 GMT  
		Size: 9.4 KB (9402 bytes)  
		MIME: application/vnd.in-toto+json
