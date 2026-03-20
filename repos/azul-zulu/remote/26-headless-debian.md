## `azul-zulu:26-headless-debian`

```console
$ docker pull azul-zulu@sha256:26f5f6b227a32b6ead07345f0327c32777f3f188a7607d8caed4b14ecbdc4347
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-headless-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:b552a9cf07bb250462f4c000968b38162b5fe39bc1459b53f3077943025bbf89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.9 MB (214887628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4bf06cd476dd567f42c9ba4c9554f9313f378d5de78d245207cf15405e18196`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Fri, 20 Mar 2026 17:25:40 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 20 Mar 2026 17:25:40 GMT
ENV LANG=C.UTF-8
# Fri, 20 Mar 2026 17:25:40 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 20 Mar 2026 17:25:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Fri, 20 Mar 2026 17:25:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe32dc966b2073de319819bfdf9dfc6e6c0c776f6f866edae3e9efe089744bcc`  
		Last Modified: Fri, 20 Mar 2026 17:26:05 GMT  
		Size: 185.1 MB (185112128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:1590e5ff159522b556e431e0184f8e8004fcc263015b41ae7fdb3d0691a0e596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b62b6e41238849f5b1ac3e76126fc6eb2b10998acee466ba64e2947331c7d5`

```dockerfile
```

-	Layers:
	-	`sha256:8613c41ad9041df3553fededc4cbc3616bad9ed18b4b5d64dd7400178c8df6c4`  
		Last Modified: Fri, 20 Mar 2026 17:25:54 GMT  
		Size: 9.3 KB (9283 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-headless-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:025df5ec0f0998b2e4cf4b0535fe32faee6fba08aa95b957aab3e29493344980
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.0 MB (214954930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0960111a666083068aedd98baba6a87a52101dc5a8401fc5d5770d334bc11c92`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Fri, 20 Mar 2026 17:25:36 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 20 Mar 2026 17:25:36 GMT
ENV LANG=C.UTF-8
# Fri, 20 Mar 2026 17:25:36 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Fri, 20 Mar 2026 17:25:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Fri, 20 Mar 2026 17:25:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258975993917a1bd4875071791ab46a321aeb30a694cbcba2e6667f2bf086b1a`  
		Last Modified: Fri, 20 Mar 2026 17:25:56 GMT  
		Size: 184.8 MB (184816514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:d403ad9f328aa779e3d73a6536babfa1bb96933b8747c1b21486b59da009add1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eab6ac02eea0ed3805a4d5597f9c63afd68333629ccc9aad6ff21f6763fe274`

```dockerfile
```

-	Layers:
	-	`sha256:86590bdf5d1e28e6c9addb6b2d16c2cfdf709947a10a3d6b6d18a73dc7ae02be`  
		Last Modified: Fri, 20 Mar 2026 17:25:52 GMT  
		Size: 9.4 KB (9387 bytes)  
		MIME: application/vnd.in-toto+json
