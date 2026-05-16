## `sapmachine:jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:95b3766992d95164d7b5c9e05c6459e263c6a4a6c9c2cc2ad8cb45bbfa303220
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:1397f475e03cec2630135766893fb1942344216938aadf7c31720017d04e4da2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87135102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a21a1eb62b6582bd7271af2766a3198726c78603d23cd98339b82d144d3120`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:20:59 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre-headless=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:20:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Fri, 15 May 2026 21:20:59 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098ca09bfb572754329f05e5b12a95e45cd0ac42fd4b751971fcc2957f9e0879`  
		Last Modified: Fri, 15 May 2026 21:21:11 GMT  
		Size: 57.4 MB (57398418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e018fc3feefd0acf72fdac32719ed613935b179fc3ef41c3a1679e263128767b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da3f6322fda2530440d49f08ee94aea7dfe44e9bbc0bdd62b3b91ad5d5d9fb9`

```dockerfile
```

-	Layers:
	-	`sha256:e6c9f5fae338e98a15a36b2bd6947687491d868850fdb2ac1aa42d36cc9f4c24`  
		Last Modified: Fri, 15 May 2026 21:21:10 GMT  
		Size: 2.3 MB (2301079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad0363e3122ce1a3b43c1d71f7caf52981de8ab7293b6a3b779461dfee011408`  
		Last Modified: Fri, 15 May 2026 21:21:09 GMT  
		Size: 9.6 KB (9568 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:3dc3558bf8b05468d0e474cefe30d4f1e57da8cee4b1eb5efc5d2282613d2090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.0 MB (83970393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee7e9225387a3022df29bb9f4a405864e27e2b3a19b8b9d8f7c826101726805`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:21:08 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre-headless=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Fri, 15 May 2026 21:21:08 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a0994b18326c972deaeaa165a333f274a6d712e74c55cc24138997cbda4268`  
		Last Modified: Fri, 15 May 2026 21:21:22 GMT  
		Size: 56.4 MB (56363770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a770cbcba6d5f00634c8887c9d46b6b68d295effec0524934ce41b2d7759f65a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77ba9094fbca7d3aad33ef9032599706b2a18318cd8a92e734349ecfb198240`

```dockerfile
```

-	Layers:
	-	`sha256:dad5dc97fd9ffd902afc53a8acec1ce9587a43d8a666365d477de996f899ce5d`  
		Last Modified: Fri, 15 May 2026 21:21:20 GMT  
		Size: 2.3 MB (2300772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b3afb1d0de2fc36566057c47a3170d172943bf5e58b20b228c2b137a9bbe9ec`  
		Last Modified: Fri, 15 May 2026 21:21:20 GMT  
		Size: 9.7 KB (9694 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b0ba4a51b71f344f1a8e986c8d1950c8e0b6d4def13181fd03ce7262529c86c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92940932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c088f5d659f00d32e791bd3dee36d90910bce3b5b526749b08931419ce6c52`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 09 May 2026 04:51:05 GMT
ARG RELEASE
# Sat, 09 May 2026 04:51:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:51:05 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:51:11 GMT
ADD file:bd6823713e9d7c2f4ea7ca1d6d549e2bed56e8ce1fc6f98e14f6eb3a3371ebfa in / 
# Sat, 09 May 2026 04:51:12 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:34:51 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre-headless=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:34:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Fri, 15 May 2026 21:34:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6970bf2b5ef1698cb51975b1a652f6511f8fd9f88ae7b247e3ee32591d975e63`  
		Last Modified: Sat, 09 May 2026 05:25:11 GMT  
		Size: 34.6 MB (34646720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a37457ebc89299f2b9547bb1d5347acce21d0c4a643d45dd945a80814b96b3f`  
		Last Modified: Fri, 15 May 2026 21:35:16 GMT  
		Size: 58.3 MB (58294212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:555525ef6e2af6f5ae6e7ecc3b44cc74358a457b8eed012286eb20e09ecb1990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2309527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5766e1834cd8103e2ad5bb56ceabdd64ffeeddd067088b49abcf3a160b342c1c`

```dockerfile
```

-	Layers:
	-	`sha256:68d061341343583df8927f4510cb2a397ed0c24c5df1dfdb44965bf408a9e94f`  
		Last Modified: Fri, 15 May 2026 21:35:14 GMT  
		Size: 2.3 MB (2299903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:452d422a0d5b536fc994dbb83494e9ba5be81aa7ab3f52012dd5714317529eca`  
		Last Modified: Fri, 15 May 2026 21:35:14 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.in-toto+json
