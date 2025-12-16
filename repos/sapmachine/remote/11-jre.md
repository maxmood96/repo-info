## `sapmachine:11-jre`

```console
$ docker pull sapmachine@sha256:3cb1c9fd820a0f77293eaf39ecbaa0f0c475ccb721cc2fed738408e45ca3f7d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre` - linux; amd64

```console
$ docker pull sapmachine@sha256:c8b01d99415d740d89ff860cb96abb51acc7c03805110e5d6251bd4623899e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.8 MB (79797887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa6dd2e220302de1d86a022e2947072a58cf7555408dd8c3dbca2cad4575b41`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:39:53 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.29 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:39:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 13 Nov 2025 23:39:53 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe9fcc70fde3f883de4ea5f7294cb2d815ca415bea92f1d8d2022915aea3f0e`  
		Last Modified: Thu, 13 Nov 2025 23:40:17 GMT  
		Size: 50.1 MB (50073199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a829f7a38342369a557202f6eeea57aed08b1d020a824533e8264dd110105d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2533678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ffe97f26ab323ef8a1c9e0aa07eeac93531947fb105dfbb873f5200d4556d8`

```dockerfile
```

-	Layers:
	-	`sha256:38c902f74dedcd8eeb1cc20169e6bd9a5e5c2b1175302102c635b8e5d5a96ce5`  
		Last Modified: Fri, 14 Nov 2025 01:04:52 GMT  
		Size: 2.5 MB (2523633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f852d65b65672553ae6337ae6b5703702134cad4555145a92a90ef52be4cbbd`  
		Last Modified: Fri, 14 Nov 2025 01:04:53 GMT  
		Size: 10.0 KB (10045 bytes)  
		MIME: application/vnd.in-toto+json
