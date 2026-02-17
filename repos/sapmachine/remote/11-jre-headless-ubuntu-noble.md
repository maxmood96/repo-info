## `sapmachine:11-jre-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:04871bed7762048bc9d91c331d384d560bb90bd065ac704242b57bb20dea570d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:430e036fc9dcdf6e2f69fd7c194cfe698fcbe1395c892999aa0263ab56987704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78631058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ddd2bbb52bfaaa295645182807363c380e3be863bf6f729ca2f7936ef087725`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:36:07 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.30 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:36:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 17 Feb 2026 20:36:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013ec98490afa31b420a2bd9c0be5abcdda65d31be29ba5e4ca35a4ca746b745`  
		Last Modified: Tue, 17 Feb 2026 20:36:21 GMT  
		Size: 48.9 MB (48903447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:56ed031c28c73c44f3d8b0fab245a0f48773c265335af6ee2bae97efc5973955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2288051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5fbcee94e05370c8073bb2d0d4bb41819282b7d64d4057ab3518dac9d2755e4`

```dockerfile
```

-	Layers:
	-	`sha256:9524f7d9dfee9a3ab36c6b91d1dde9fe61c7bad3be0644d7c47cd3b2bd84a4ac`  
		Last Modified: Tue, 17 Feb 2026 20:36:19 GMT  
		Size: 2.3 MB (2277823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e384f3250fbed99518b08211c9b5fcbcc0c7ee757c632466b44e471cd18dab6d`  
		Last Modified: Tue, 17 Feb 2026 20:36:19 GMT  
		Size: 10.2 KB (10228 bytes)  
		MIME: application/vnd.in-toto+json
