## `azul-zulu:21-headless-debian`

```console
$ docker pull azul-zulu@sha256:713366d42d34e12c46ddb4310e35cf15bae155375200ae597736fde4b67e281d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-headless-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:6242548e1c30043ba1e7d49b551452d0f9d0ffadd49ac34b3340fac93c78b1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193616321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf83d433dc37aae9aa90a1e281ca1f50f2c84bdc72f57292f60eca219d078c6`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:21:21 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 19 May 2026 23:21:21 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:21:21 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.11-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 19 May 2026 23:21:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Tue, 19 May 2026 23:21:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81bb4c92bdb7da7266674ba987ae9e159f648c627f035509a7d688e9ce2daf7`  
		Last Modified: Tue, 19 May 2026 23:21:37 GMT  
		Size: 163.8 MB (163836395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:85dcb923efa87615163a2295fe7759aab5ced8059e27b8e91cba4e01841e76ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6bf29d11b8e91f10193f8fcd50b75a5ef97c09d7aff74386cadc4ae0d589d4c`

```dockerfile
```

-	Layers:
	-	`sha256:95c6763b2f58cd529668cccadcf99817248b0c6deb32b9fb7dd76b6b59985ce2`  
		Last Modified: Tue, 19 May 2026 23:21:33 GMT  
		Size: 9.3 KB (9298 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-headless-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:6e8622cec78d53baacfa8474813213d39b8371a2d28abcaedc394dfff22060c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.3 MB (193290580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23727305d37b48107ff52d680a08e2f1d26c4fcbe7ebec93bad557be32b51501`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:25:06 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 19 May 2026 23:25:06 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:25:06 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu21-*\nPin: version 21.0.11-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu21-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 19 May 2026 23:25:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Tue, 19 May 2026 23:25:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d95b3408c5ea029ad20ac49f54c01849d7ef710c2fc06e376f7b4809cc77361`  
		Last Modified: Tue, 19 May 2026 23:25:24 GMT  
		Size: 163.1 MB (163148661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-headless-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:8b787ce1d89abadcdb74f7f1f71d3d0549422cceec6b7dd3fbbe74bbec86ecfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bfbdec5a0b8325ed6a9538c26fe0b27e21d320b322bcffcf46980b135984370`

```dockerfile
```

-	Layers:
	-	`sha256:e18f412a641069286884c7943c06ae1aefa22c38a70f94260df6be5a730eab99`  
		Last Modified: Tue, 19 May 2026 23:25:20 GMT  
		Size: 9.4 KB (9402 bytes)  
		MIME: application/vnd.in-toto+json
