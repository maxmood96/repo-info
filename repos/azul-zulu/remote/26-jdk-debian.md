## `azul-zulu:26-jdk-debian`

```console
$ docker pull azul-zulu@sha256:1865f595e03b98cc3024ba9dcd5e39aba892dbddcf0e951a5e32f89e43e54f8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-jdk-debian` - linux; amd64

```console
$ docker pull azul-zulu@sha256:d4d6f21e272d18aa76fe5de44d6719e3a0d95b99e58ac505d410a631100e1dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.2 MB (217226421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9acb478486071abc9abbab8ad265fa38bde5148a288ff6e0202d2bef0896aa1`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:22:37 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 19 May 2026 23:22:37 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:22:37 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26.0.1-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 19 May 2026 23:22:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Tue, 19 May 2026 23:22:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228d65897f2755b62e0721bb8dd28543a73e8e9c94d445ebdc061a5408df8f95`  
		Last Modified: Tue, 19 May 2026 23:22:55 GMT  
		Size: 187.4 MB (187446495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jdk-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:07d3984c9b4c3371ec9f139bb6d6d75343e5e2b0bf1fd72ea550ed5add393c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c84eb529463360cacdc212dd9358c445b5b3e421f76da11d41fbdd432cd3899`

```dockerfile
```

-	Layers:
	-	`sha256:538749a6a34cb14bfedc822a3a533218ddba971013972a072cadb5834fd47646`  
		Last Modified: Tue, 19 May 2026 23:22:51 GMT  
		Size: 9.5 KB (9504 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-jdk-debian` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:42371b73f824d95c9b0ddaef04227c18aaeef90aed4ac2b15fc83bd2397beaa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.3 MB (217269329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b56dd6adc4c6cd7b7e633f595a6006b61c8ca48f2af610877a64e48ed4d175`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:26:06 GMT
ARG REPO_HOST=repos.azul.com
# Tue, 19 May 2026 23:26:06 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:26:06 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux &&     apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates curl &&     GNUPGHOME="$(mktemp -d)" &&     export GNUPGHOME &&     curl -fsSL https://repos.azul.com/azul-repo.key | gpg --batch --import &&     gpg --batch --export --armor '27BC 0C8C B3D8 1623 F59B  DADC B199 8361 219B D9C9' > /usr/share/keyrings/azul.pgp.asc &&     gpgconf --kill all &&     rm -rf "$GNUPGHOME" &&     echo "deb [signed-by=/usr/share/keyrings/azul.pgp.asc] https://$REPO_HOST/zulu/deb stable main" | tee /etc/apt/sources.list.d/zulu.list &&     printf 'Package: zulu26-*\nPin: version 26.0.1-1\nPin-Priority: 1001\n' > /etc/apt/preferences &&     apt-get update &&     apt-get -y --no-install-recommends install zulu26-jdk &&     apt-get -y purge --auto-remove gnupg curl &&     apt-get dist-clean &&     java -version # buildkit
# Tue, 19 May 2026 23:26:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Tue, 19 May 2026 23:26:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839a833bf5486842cb4843d6bca81ada7e5fd1032c73b942d406431e63ff5ffb`  
		Last Modified: Tue, 19 May 2026 23:26:27 GMT  
		Size: 187.1 MB (187127410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-jdk-debian` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:f96dec107e9c9a1e0c77b883d69570b6c37e270b70b67bd82e6d6a7ee95444e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.6 KB (9619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf1bee5ceec0018f783c97d38367d1c98b6d7e75b2c0bd8b0b379de943a78b5`

```dockerfile
```

-	Layers:
	-	`sha256:482e09e4a8b8ef460c7bea72d3eb404e81e4aa8ebe86ed6d8e9dd17b209a69f0`  
		Last Modified: Tue, 19 May 2026 23:26:22 GMT  
		Size: 9.6 KB (9619 bytes)  
		MIME: application/vnd.in-toto+json
