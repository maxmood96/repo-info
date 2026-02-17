## `sapmachine:11-jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:44139394bab856012d28c597b91b03ec1447804183ecc25412368e59dc397544
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jdk-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:ac5b224a59d030eec3e59a735020dfc0ab023ab99218ab877c487f5db640de5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229233165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b075b96fa1cf0e1fcfa76465a1d2d9315de2d1655cf9b6f17d0a0c79c543ec03`
-	Default Command: `["jshell"]`

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
# Tue, 17 Feb 2026 20:35:57 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.30 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 20:35:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 17 Feb 2026 20:35:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49057f36d3171909780b508576c7fe3f749d59d8ed6e597d739b69e5566d9a2c`  
		Last Modified: Tue, 17 Feb 2026 20:36:18 GMT  
		Size: 199.5 MB (199505554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a4f9490d78f4ce10aa100620a2b274a5c006a97f696eab06deca24a518a8bb85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd62ddc8b4ac41a04a67306c6abeeaa6fe04b9591f582bf935d58b592feb302`

```dockerfile
```

-	Layers:
	-	`sha256:5307be107258c7b7d9e4e1feb37c946365d02fe3405eb91a65dbb8f1ada18e86`  
		Last Modified: Tue, 17 Feb 2026 20:36:14 GMT  
		Size: 2.4 MB (2367224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b40b0279153a8633f084edcb75cd0051fa2651c86b2d479179ecfc76c9b6ea90`  
		Last Modified: Tue, 17 Feb 2026 20:36:14 GMT  
		Size: 10.2 KB (10233 bytes)  
		MIME: application/vnd.in-toto+json
