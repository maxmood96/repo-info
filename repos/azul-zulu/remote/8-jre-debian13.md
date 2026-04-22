## `azul-zulu:8-jre-debian13`

```console
$ docker pull azul-zulu@sha256:9123b199509cfd8e49ec0d0ea35474df6a66993d681adc22063d2016c1ada5c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:8-jre-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:1076f3d0e2f18eb308a3bd67373fad9927b93736f2524e3837a542a21488b461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79612342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f860bdff448191b12f7a23bd9dde84d1ecc108f788aced2ac7e75fa041fa96d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:36:08 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 22 Apr 2026 01:36:08 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:36:08 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.492-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 22 Apr 2026 01:36:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297aacd14b46a916796a77419f11dd57ace3201feb0ef49e8b1172113beb0d79`  
		Last Modified: Wed, 22 Apr 2026 01:36:17 GMT  
		Size: 49.8 MB (49832168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jre-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:f5438d036a8f9474654022995a3f2bd92ebc6c880e98ca4dde95e2fbf4828c7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7630d0eaae58c1a8904b0aae4ac251b81a5ef8b395f77056bc236dbdda8adff1`

```dockerfile
```

-	Layers:
	-	`sha256:5f0c67cc4f320d080ed05872fb777fc2ccb3b89e5d30120189ec9fd5d070a1a4`  
		Last Modified: Wed, 22 Apr 2026 01:36:15 GMT  
		Size: 9.2 KB (9174 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:8-jre-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:d81fdf5c36c113f2ac23c9db16efbff6c6ea9ca1d680bcf7c56b73f9eea47ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.2 MB (80197474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f08fa513e06d4b087b4b29da52d2c8607749583b7f4066bfee386501777b527c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:48:21 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 22 Apr 2026 02:48:21 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 02:48:21 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.492-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 22 Apr 2026 02:48:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae65d155e562b7402bb8b7f88adbf2ef8188b0ea6a8dc84ad07d3e45bbfcbaba`  
		Last Modified: Wed, 22 Apr 2026 02:48:30 GMT  
		Size: 50.1 MB (50053868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jre-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:1ecdc3e8ef742a9711126647947e90c5d030402f249451a44b9af6aa9f43c1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2d343e142754919260a7ce4722ab960c1800bf69caf0c6c9f1630118806317`

```dockerfile
```

-	Layers:
	-	`sha256:bc2f4796e7578f1f70eb6ecee51b2000b32b6e0e1d1c6200bb9aacadf57bfdce`  
		Last Modified: Wed, 22 Apr 2026 02:48:28 GMT  
		Size: 9.3 KB (9278 bytes)  
		MIME: application/vnd.in-toto+json
