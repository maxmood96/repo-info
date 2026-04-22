## `azul-zulu:11-headless`

```console
$ docker pull azul-zulu@sha256:67c9639970c04229c4266a986c7bcbc6b2b94cb87e5a7b72061ed2f2875cc79c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-headless` - linux; amd64

```console
$ docker pull azul-zulu@sha256:b57b00ee8b812c8fcc49e93fdc0dec695f6de10e1cdf08a110ec3407a8e53f03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.0 MB (175979699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13df2d27e170bb1fa666e006967f65071251e1d8bcfce8678e0453863bfb6b0`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:36:40 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 22 Apr 2026 01:36:40 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:36:40 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.31-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 22 Apr 2026 01:36:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Wed, 22 Apr 2026 01:36:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8921d9a7870d2cf131e0c0330a23ed782f0585db4127871e9188895de0597ef`  
		Last Modified: Wed, 22 Apr 2026 01:36:59 GMT  
		Size: 146.2 MB (146199525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:7d297b53cb47ddbda9309b8d40f017a311b83d7a6b9c7296161efc473f17b298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29d2ebeba38f3a0260afe93db65e395b9c3dc3fe5abe4c576030e57e2f848e96`

```dockerfile
```

-	Layers:
	-	`sha256:d979c51d85d71b40b8a4f79dab55a3a64a543d7ac10960d32ef0b4c7ebb08cae`  
		Last Modified: Wed, 22 Apr 2026 01:36:51 GMT  
		Size: 9.3 KB (9298 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-headless` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:6dc44694fb6e588e1e25d3d435c7430ac7cfc0532b77e159b0a51b4628c1801d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176053124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7831723247671151637d0e84789408381262971dbca3fdfc95fdeab5f3c6a607`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:40:26 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 22 Apr 2026 01:40:26 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:40:26 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu11-*\nPin: version 11.0.31-3\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu11-jdk-headless &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 22 Apr 2026 01:40:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Wed, 22 Apr 2026 01:40:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdc84377185a356b5bac3768f26d8a5aa302e0bd008cf00b0747cf2e7dcffdb`  
		Last Modified: Wed, 22 Apr 2026 01:40:41 GMT  
		Size: 145.9 MB (145909518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-headless` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:d51078c5122e9f0ad7c64f9d2b6262c8275da570a43fd586c21edad6b98a2fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff66e5f0995cf26952865a02ade7cb974faa4f29476857e27e358b41a485021`

```dockerfile
```

-	Layers:
	-	`sha256:c37376932f7cc11d48c672f0f3562f019b73b1199b3ac137bcf3a261b974340a`  
		Last Modified: Wed, 22 Apr 2026 01:40:37 GMT  
		Size: 9.4 KB (9401 bytes)  
		MIME: application/vnd.in-toto+json
