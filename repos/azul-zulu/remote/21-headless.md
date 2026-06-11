## `azul-zulu:21-headless`

```console
$ docker pull azul-zulu@sha256:e7b19a2e0f90d94314e4c397e34f5a25d46bc07d0edf9750b297c23738c8b759
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-headless` - linux; amd64

```console
$ docker pull azul-zulu@sha256:cfb81ae723fac33c03edd32c252b4cc179d6c16fa21e12f2d31acb70ac07998a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193621982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa452fbb633a023aa8100cda8df7b35faa4d3953cc734213a4fa31d1a25aa707`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:40:34 GMT
ARG REPO_HOST=repos.azul.com
# Thu, 11 Jun 2026 00:40:34 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:40:34 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.11-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Thu, 11 Jun 2026 00:40:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Thu, 11 Jun 2026 00:40:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97d60ee3d9863a7926049438c156e8d7dcc1cf21bc270f8b52c370ecdd64f92`  
		Last Modified: Thu, 11 Jun 2026 00:40:51 GMT  
		Size: 163.8 MB (163836567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:21b9b474aeb4338ee551863e6d970f4cadb5d8db38bff2f699b896a0db27b895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed90279975fe43684261a038bb5b52d0d43e73adfd9e1ba8217005b3e7e378a7`

```dockerfile
```

-	Layers:
	-	`sha256:01a5bc525d39fe84ca6e9226e8f3b4e7e92ed25285e1614ed81a5866967da338`  
		Last Modified: Thu, 11 Jun 2026 00:40:47 GMT  
		Size: 9.3 KB (9298 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-headless` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:9f92468bcf303493be375c4b2265fe4987d00753710aa70b485451b50430c65b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193297340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:084db9f431cf4b01ddcb794f60b91481452f50cef29c38011b5c71d2b6d61f36`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:42:18 GMT
ARG REPO_HOST=repos.azul.com
# Thu, 11 Jun 2026 00:42:18 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:42:18 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.11-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Thu, 11 Jun 2026 00:42:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Thu, 11 Jun 2026 00:42:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc792f92e7eacabdca19f65d67a4287e63944fac69e82330b45bd778bc48581d`  
		Last Modified: Thu, 11 Jun 2026 00:42:34 GMT  
		Size: 163.1 MB (163148810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:fed220292f58f2a430b68c1a0e3790dc2f69f5e55d2e12f9d1e826dc01170f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec591999ec38d3bb11315eea37547d1dda53316049ba090ca950944802fe69d`

```dockerfile
```

-	Layers:
	-	`sha256:026b24f37479d170c22dc008142a22b296a44babdf03807ad9e2ee7e4dad014b`  
		Last Modified: Thu, 11 Jun 2026 00:42:31 GMT  
		Size: 9.4 KB (9402 bytes)  
		MIME: application/vnd.in-toto+json
