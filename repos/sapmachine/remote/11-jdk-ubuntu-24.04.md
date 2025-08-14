## `sapmachine:11-jdk-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:88e01ec0d6795c6824c25772287ebdd400704af2a76142a780fe6aff47e9e96b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jdk-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:ed69fccb05fbdfcea467fc81f2d3cae10c99cfa78c597b1e8d04a12849a7844e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231028930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc2a4077e2bf6c8b5b7864b453c937b56a6f1a126a5b1adfd48b26703f3b0f8`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:16 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:16 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:16 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Tue, 15 Jul 2025 19:58:16 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.28 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 15 Jul 2025 19:58:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9d4c2bd50f1daea5d3d01306a57a79439d93c0a80ba400e3390c9dc09bcd3b`  
		Last Modified: Tue, 12 Aug 2025 18:10:56 GMT  
		Size: 201.3 MB (201305715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1d59fbe400ef0a6b20e27d430978e16fdafc4846cfc853c81dd1148f1367572d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0fad27b530b1f43c7c6c63f3651a28472749094986e939a3682e89e831bfa5`

```dockerfile
```

-	Layers:
	-	`sha256:23d5b276a1f682493ea1ee5e66cb9bc6afca304772dd8197584339cffaebc31d`  
		Last Modified: Tue, 12 Aug 2025 21:04:17 GMT  
		Size: 2.6 MB (2615586 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:accc84ff48ec1f96396efba8d0af6dd8e78547c8ccc0bc2550919d8b0d3966d2`  
		Last Modified: Tue, 12 Aug 2025 21:04:18 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json
