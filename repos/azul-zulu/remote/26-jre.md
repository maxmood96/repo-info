## `azul-zulu:26-jre`

```console
$ docker pull azul-zulu@sha256:ba83408152ed41f8450ac643aac80fd06118ca4c7d03577921a8f7d42fc81bd3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-jre` - linux; amd64

```console
$ docker pull azul-zulu@sha256:2564bcad9d1d7b8c561e389a5b3f1de4650655bddc8ecb95c2ebebe5aa1bd09c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121920179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d421539fbac215028aee81b3ed80675fe409d31e8a02dbd11bd473c13c61c2d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:42:03 GMT
ARG REPO_HOST=repos.azul.com
# Thu, 11 Jun 2026 00:42:03 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:42:03 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26.0.1-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Thu, 11 Jun 2026 00:42:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8ebf9a8255fe941af42c48e9f1a8f231ca4fc0db6299c6e2c9f0d2b0d23fbe`  
		Last Modified: Thu, 11 Jun 2026 00:42:18 GMT  
		Size: 92.1 MB (92134764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jre` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:84070382c56a36e9aa264437c9a4bf352b53d12101c032bcdc81e1cf5fdd99ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d976bc6b11bdcc4c13d66da77e8b847df0973abd30ecf92a559ce7749d053671`

```dockerfile
```

-	Layers:
	-	`sha256:db48b49e222ede533e7f3f98255c61e1680640b6a02bd39622016789fad55a4d`  
		Last Modified: Thu, 11 Jun 2026 00:42:15 GMT  
		Size: 9.2 KB (9187 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-jre` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:5db7cba0aa6269e40f5f09ff6ed67945346edf49b9302a4a0a31873713f04d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122189025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a82cf579bbe0b4f7ee112bb5260b86e656bf8a253ce0927fe0ebafb3a4d6599`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:43:53 GMT
ARG REPO_HOST=repos.azul.com
# Thu, 11 Jun 2026 00:43:53 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:43:53 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26.0.1-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Thu, 11 Jun 2026 00:43:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67b0d2eddd8b3832ec0592aad754b5e4b29f9ac80df54e92bb25bf64b201326`  
		Last Modified: Thu, 11 Jun 2026 00:44:08 GMT  
		Size: 92.0 MB (92040495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jre` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:ca235d718d6e22340094dc8b8b03d5b1fb2210f6028ed4a487829501cb9d6a23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fa76b8d661e8c562330cc5d067569cfc26b4279ada8044a19cfb3416e7ae9ef`

```dockerfile
```

-	Layers:
	-	`sha256:477a0320b4d01bfbab070198e93f5d2a16cbb45b79bed3539b4645afebe5059d`  
		Last Modified: Thu, 11 Jun 2026 00:44:05 GMT  
		Size: 9.3 KB (9291 bytes)  
		MIME: application/vnd.in-toto+json
