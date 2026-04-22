## `azul-zulu:8-jre-headless`

```console
$ docker pull azul-zulu@sha256:499a7effa153b705bac155b1c70ad52fdab5c16c11e44e19ab129ee601ad3f77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:8-jre-headless` - linux; amd64

```console
$ docker pull azul-zulu@sha256:b0f923c7da5e034535b8747be044f82656785aeef30251916cb0d371e97955c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77507074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67fe692a093e2605e851dc05b3d6cef01cfe501b34ada3ffd4db8369c7736f34`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:36:01 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 22 Apr 2026 01:36:01 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:36:01 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.492-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 22 Apr 2026 01:36:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4683c72f8773c91709b13f55855894365e29c2fd777ca84bbd85e799e0b04d64`  
		Last Modified: Wed, 22 Apr 2026 01:36:10 GMT  
		Size: 47.7 MB (47726900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jre-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:c93144f208cf9c2b738b55d808439c62f7c01b4fe3f5cca7a0f3780fb8673854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f5906dedf6a572e8a64653c06f517138071e37bf2aa0ffadb582c271ed026d5`

```dockerfile
```

-	Layers:
	-	`sha256:4f7585462eb4b067335d304741630cde2783f46635b5d4819f18836ad6939590`  
		Last Modified: Wed, 22 Apr 2026 01:36:08 GMT  
		Size: 9.3 KB (9285 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:8-jre-headless` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:68c04a5cb4c03d18b025af5761c6be626b214b23dd90fbe00dad815e01049b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78094814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78bb4216018a00b83ac3102cf72277250bcf62288e789c0331cf12af720830e9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:39:50 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 22 Apr 2026 01:39:50 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:39:50 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu8-*\nPin: version 8.0.492-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu8-jre-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 22 Apr 2026 01:39:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0854312621a5c9e4afc97f1bc5ef113980fd43789da802f0a72454696bcdee0e`  
		Last Modified: Wed, 22 Apr 2026 01:39:58 GMT  
		Size: 48.0 MB (47951208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-jre-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:f80b69a0e7a0d1002c83a9b504937cb6768a60fe3df4fd0f4d00f4daac9152df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:481383b030d56310acd7aac1aa7e05e2c836ca244d7db193a41556282ec8779f`

```dockerfile
```

-	Layers:
	-	`sha256:2396900646b9e84a053278145926a82ddb79572c50b9347dd697291acacd280f`  
		Last Modified: Wed, 22 Apr 2026 01:39:56 GMT  
		Size: 9.4 KB (9389 bytes)  
		MIME: application/vnd.in-toto+json
