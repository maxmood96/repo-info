## `azul-zulu:11-jre`

```console
$ docker pull azul-zulu@sha256:41781dd88776030646e87e06b09bcda5f47753a7f881048e3ebee7265dc2f6bf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-jre` - linux; amd64

```console
$ docker pull azul-zulu@sha256:c8cf10a80c8c2aa62bac05b9410ea929df0229597af7e83659014f92caab9041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96903845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574474132cfb43bb4433c43abb296d3cf5a37ee6c4241ca308f74bd8d2c835d8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:38:40 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:38:40 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:38:40 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.31-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:38:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f03dfc9957f9024bd4af53f115ad07e95107cbaf46e6cb8efc848b89bb86896`  
		Last Modified: Wed, 24 Jun 2026 01:38:51 GMT  
		Size: 67.1 MB (67118426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:e8499dfa6ed6426254bc49710979f1805f019043f2843d2e920ec65ff2fa32f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2346515bdabc83c277de28f5384515319ad214f86eddf417bbf9a1d16e8cd616`

```dockerfile
```

-	Layers:
	-	`sha256:40a31d372749f22e47a30d6048f81d73c2986a92659d0bec680078b5036aee07`  
		Last Modified: Wed, 24 Jun 2026 01:38:49 GMT  
		Size: 9.2 KB (9190 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-jre` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:77bf68c9030ea69acfb3b089b26987a79ab7baf16a8e8b269f4f73a5773c108f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97073263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:928a5714a7f389672776785ab216449b9fd5b208fa59f86625ff2ea6ddca3773`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:41:08 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:41:08 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:41:08 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.31-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:41:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a866b7d07413a997580717b632c1a2e797a9c8b539046e097207a575762ef611`  
		Last Modified: Wed, 24 Jun 2026 01:41:20 GMT  
		Size: 66.9 MB (66924712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:61dc3db9e1fdb6746e77fdc805c0573911d5b14fdafd3f0701ff35cff63c8ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5379572d65934b77a710fba9e487169b07baac1e90411399eb1975e0475dd961`

```dockerfile
```

-	Layers:
	-	`sha256:443a8697a1f4be84ce1c946ed2189ef2de17be7d8c61ed72d7fc46fa5b77fd89`  
		Last Modified: Wed, 24 Jun 2026 01:41:18 GMT  
		Size: 9.3 KB (9293 bytes)  
		MIME: application/vnd.in-toto+json
