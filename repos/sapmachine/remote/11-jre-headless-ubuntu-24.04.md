## `sapmachine:11-jre-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:a08178f818774c10337085f2880e22e26e45ec59c52c269d89fb9b197663a11f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:8c5f8109f5db057b194f5d3d29ad1c9157752e7b8aa2d0cd52dffbea544dd685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78916718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b94cb6d13c43e9d905968bc36613a474d4d28af48ffbdcc10e128c4925ba23d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:44 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:44 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:44 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Wed, 16 Apr 2025 10:34:44 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:44 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.27 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Apr 2025 10:34:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe191a211eb65d9be65d8267bf9769b8a6ab5dbe580ebda585efa75d7d25b0e0`  
		Last Modified: Wed, 02 Jul 2025 21:25:41 GMT  
		Size: 49.2 MB (49198352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:99ca8761df49b46a96139db5e0aa1aebfb7d8cfc6724c39802b44e12dc54f8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f573df427d48f990a13d07370f6f229ff0300fc61fd972fd6564a86716d5b6bd`

```dockerfile
```

-	Layers:
	-	`sha256:de3116a86a2b3a684e1a7a485fe00a6324a8570d5d96cd8b77d0978846e8b299`  
		Last Modified: Wed, 02 Jul 2025 06:04:34 GMT  
		Size: 2.3 MB (2277139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6210a35565e59f75edc209da7160b5f3ef49873369783e54cb394ff520e3a375`  
		Last Modified: Wed, 02 Jul 2025 06:04:34 GMT  
		Size: 9.6 KB (9618 bytes)  
		MIME: application/vnd.in-toto+json
