## `azul-zulu:26-jre-debian13`

```console
$ docker pull azul-zulu@sha256:af988940d23fb69559cd4fb8401422b7c81cf0983403dd0944701ba7698016e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-jre-debian13` - linux; amd64

```console
$ docker pull azul-zulu@sha256:37231250d4299e9678a271cd85656e52565bec3f54504c83c3e48a17bdc875c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.9 MB (121920207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e58d4beaaf16345cbc0e36d5f69cc6cdcad53e36f8ce46a055e95338244d063`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:41:24 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:41:24 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:41:24 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26.0.1-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:41:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfd736b9893258df3e05a1f3e5947165bddd11f2c1b48d15358c282e399626a`  
		Last Modified: Wed, 24 Jun 2026 01:41:38 GMT  
		Size: 92.1 MB (92134788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jre-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:96bd1a9ead5b237ee486bd8088d1b483b6a534c6fed13c04c32e2cabb864c80a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4388df5e01fe42646d1d933cf471eaaab6b61e3d6362f7eacb3d77f20ec180b0`

```dockerfile
```

-	Layers:
	-	`sha256:d18cf2650f9535ced43fb0f252b7b6b0b0d3143d84392419a6c975bc7d46a70a`  
		Last Modified: Wed, 24 Jun 2026 01:41:35 GMT  
		Size: 9.2 KB (9186 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-jre-debian13` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:62953b8e0239e86190ddc641e645049660ce0d59a8e8f58b413894231c2e5bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122188949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97afa649457408505df80482c5b89e2a53f5713b34b4ec1d39c1dbef1a0656ba`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:44:42 GMT
ARG REPO_HOST=repos.azul.com
# Wed, 24 Jun 2026 01:44:42 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:44:42 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26.0.1-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jre &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Wed, 24 Jun 2026 01:44:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802c52af4f6117d539ee1fda1a479ddf63990452966328f8da0b316a0de5081e`  
		Last Modified: Wed, 24 Jun 2026 01:44:56 GMT  
		Size: 92.0 MB (92040398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jre-debian13` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:1bd405e7cb7a1af02990b5cf1b6e5bbfdd569336019ad990c0f49a1d45cc8857
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555f03d7c177a22cb30f337f5cac0f8ffd0c7f886bb7154c6034fda1ce3178e9`

```dockerfile
```

-	Layers:
	-	`sha256:8725b36eca4f138c1881ea5179de7f021115e69ea6e20d6aadabcb8af7f0955c`  
		Last Modified: Wed, 24 Jun 2026 01:44:54 GMT  
		Size: 9.3 KB (9291 bytes)  
		MIME: application/vnd.in-toto+json
