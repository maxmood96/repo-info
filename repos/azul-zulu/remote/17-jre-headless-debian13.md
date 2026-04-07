## `azul-zulu:17-jre-headless-debian13`

```console
$ docker pull azul-zulu@sha256:52d2bb24dd239a7d3a99c936dbb607560712e515a1de5678527a3d162eb37657
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:17-jre-headless-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:b5e1145ad915ad635d2082f200a362ec56229850ed8a1195a198a35b907a9163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99169559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762b9bbea70685d288fe5f58b61b819388cdcc308125fc46d591fc1e2e6344ab`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:45:07 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 07 Apr 2026 01:45:07 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:45:07 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.18-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 07 Apr 2026 01:45:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1420520145c43b8449f4e0789543785f13508b70a692694fc2d8b31311df0c2`  
		Last Modified: Tue, 07 Apr 2026 01:45:19 GMT  
		Size: 69.4 MB (69393919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jre-headless-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:21f2ac05745ea73b42bbb3ae8cf7525636da37a66d1f25bd5d375677e9ff2195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c657f9591ae7492a4b39088bf9fbe03a39a1ff63a3360216225aefdd50203f`

```dockerfile
```

-	Layers:
	-	`sha256:bfbde5e4a1f51f9b102751057dec103831edd95275758987298b217e0ced93c7`  
		Last Modified: Tue, 07 Apr 2026 01:45:17 GMT  
		Size: 9.3 KB (9301 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:17-jre-headless-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:d14ce84e316ed281e066db940074734db5e4d272c68b15ff9fd7106adab05f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.6 MB (99570022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dcf2fe5ad0a49ed0f7d5b79844212c5383105cc55e6fe41ec19937db8dfe6a8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:48:16 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 07 Apr 2026 01:48:16 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:48:16 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu17-*\nPin: version 17.0.18-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu17-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 07 Apr 2026 01:48:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7361872426ee0f259a66706a7a4fefc4ea9c4d49f71d96461b9a369a59b23fff`  
		Last Modified: Tue, 07 Apr 2026 01:48:28 GMT  
		Size: 69.4 MB (69431471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jre-headless-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:82dd4ce2b845f0141e5ebdfb3ca524a9ebcd01873a2de9a197e7c9261885120e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843bf7e93084d96f89fdf0647e802b3dbc2d0702e22848f0f76d396007c0f4e9`

```dockerfile
```

-	Layers:
	-	`sha256:55cb76680fe06f69cf3627b3b0863bc4681d83187eafbcc22787143553830e90`  
		Last Modified: Tue, 07 Apr 2026 01:48:26 GMT  
		Size: 9.4 KB (9404 bytes)  
		MIME: application/vnd.in-toto+json
