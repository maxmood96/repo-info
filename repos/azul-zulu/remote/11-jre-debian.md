## `azul-zulu:11-jre-debian`

```console
$ docker pull azul-zulu@sha256:6e5bfe88c5e68eb5f307e801787be5288c29e761f023dc10ddfea2c74c481106
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-jre-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:c7cab625ddf48b4266e1e4e367fe756841d28195a788fca8added2231fcdf450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96898572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25985c8e841f7ea09646598e79ee85662b71e6d6e3d5ed29a3ce402cd6b4465`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:20:01 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 19 May 2026 23:20:01 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:20:01 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.31-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 19 May 2026 23:20:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85bceac7fc7f680bb7d06920a337f105e16bb8325eee5cfc540b1694a9bf743`  
		Last Modified: Tue, 19 May 2026 23:20:12 GMT  
		Size: 67.1 MB (67118646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:f9fbc562626b4e7d68f147d9dce174c1549a14367772dc60355404303051a222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f95b4e25b2830155caa86ca79cd1d7c4fa49ea44608b8451962bd6b11ea17ed`

```dockerfile
```

-	Layers:
	-	`sha256:ee60cc3950607fe34ba12bee5349ca04ca40a57b60e3dfb5b4d74d9cb5064eb2`  
		Last Modified: Tue, 19 May 2026 23:20:10 GMT  
		Size: 9.2 KB (9190 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-jre-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:7b07e29499ca116d03149dc957994b81ce2abe2589fe372dd8ec55c13be6aeeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97066551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254884e5b57d5339c900a19510f115130ff182a0deb5a19570c1a2281629ae4a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:23:43 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 19 May 2026 23:23:43 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:23:43 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.31-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 19 May 2026 23:23:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a236e205bb3fb636864e2202dbe88e1780115a464f538bddaccd4b6ea13460e`  
		Last Modified: Tue, 19 May 2026 23:23:55 GMT  
		Size: 66.9 MB (66924632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:053b911bcd66a75251db5f8c97ac3b0c1c7319ba5c8a42f3d1fd9202927b5a12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:879713117a57d06a6f5231c0371b1a91fdd2eda502376de0c5767f028fdeb819`

```dockerfile
```

-	Layers:
	-	`sha256:0ecb9244d7c7ce7362fff4596644df67b5d318fcbfff2b7d18b445d383aaca87`  
		Last Modified: Tue, 19 May 2026 23:23:53 GMT  
		Size: 9.3 KB (9294 bytes)  
		MIME: application/vnd.in-toto+json
