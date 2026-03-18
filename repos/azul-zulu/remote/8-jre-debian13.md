## `azul-zulu:8-jre-debian13`

```console
$ docker pull azul-zulu@sha256:5394626b5cd7cefc9398e9c4060a361848e2403a1924bb36f8093538376955da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:8-jre-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:de06056ef6ad809eac6902cbba45ec23403bfdc64abecc6c299ef2b60f83742e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79585849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7d50745353025ebd516d413facba61bf8cd1aa35d6f8be47887698b910ef3a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 22:11:12 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 17 Mar 2026 22:11:12 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 22:11:12 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.482-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 17 Mar 2026 22:11:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4e012186945131dd27a3b0aea8f6e9d155bb450e358202970a2d452bfa4500`  
		Last Modified: Tue, 17 Mar 2026 22:11:24 GMT  
		Size: 49.8 MB (49810349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jre-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:34e34d16b37a700f671b7e4f0487a7663aa180f8795eff6daebc232a2b592e1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441e307fe9de6c775a0e7578949628af4c4478afd71762da1bc4fb0b1f70acfb`

```dockerfile
```

-	Layers:
	-	`sha256:dcf828dfe814aad152c96fe989bdb934434f00dbf07c813e25e0ffcc87975ce7`  
		Last Modified: Tue, 17 Mar 2026 22:11:19 GMT  
		Size: 9.2 KB (9174 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:8-jre-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:f7fb612aa3cae1bc1b33620e653e1a268a32753df2e925ae3ea6635311579f4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79248226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d16a4cb3d6a70338cd6c6551a57a59c9557cf1eacd8a244351d0fd4cc3b4053`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 22:11:22 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 17 Mar 2026 22:11:22 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 22:11:22 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.482-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 17 Mar 2026 22:11:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc9702e6990a28764f68c788d74f5342d3da4d3af011ddb76c5be8464d9f84a6`  
		Last Modified: Tue, 17 Mar 2026 22:11:30 GMT  
		Size: 49.1 MB (49109810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jre-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:7818066118b5736ee597e614e4981b9c468060cdaf4df1798dedde5444a37fef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:252cefe84dc1e2b8b5a0684fc76ac387cb082f9455d5c9a38e2f50edbd3fda41`

```dockerfile
```

-	Layers:
	-	`sha256:6169b29be028a38180ea6bafee32a8f0cb618fe50c9a9f32f3d7cc36f824c0ef`  
		Last Modified: Tue, 17 Mar 2026 22:11:29 GMT  
		Size: 9.3 KB (9277 bytes)  
		MIME: application/vnd.in-toto+json
