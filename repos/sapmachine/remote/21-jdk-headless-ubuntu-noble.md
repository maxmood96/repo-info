## `sapmachine:21-jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:d1152cdf5a1906e7773ba3543792377f4f2c0e059bcf6236f6563ec3ed102bd0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:9142a7508e663449e846972116073639b13f5eadbb44276e780150214c6cf533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.0 MB (245042074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49751fe35073c56254cccef8c968869d90eda4a001fd8554010f2b3fa878b825`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:33:08 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:33:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 07 Apr 2026 02:33:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b59fede2e74b3fa5e00e601889ec18d06a16fff170434a4d00f192e03f4e7b1`  
		Last Modified: Tue, 07 Apr 2026 02:33:32 GMT  
		Size: 215.3 MB (215308615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:05deb80509a96b54ae4c8d78f1eae1138a693e51d33d6aeb441d01e4d8b06503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2369081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a400280ea528935f150d1568365c4f75276016677c0fe599f3c53efb36381dd9`

```dockerfile
```

-	Layers:
	-	`sha256:a24d616cf408495632b8517e2dcab3513871d9f3477567fb6cd9e5963584c998`  
		Last Modified: Tue, 07 Apr 2026 02:33:27 GMT  
		Size: 2.4 MB (2358807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:895d989b18d7df15d96cc0bc062bcda6d9282ef6a9b690eff1a593ba4a0390b9`  
		Last Modified: Tue, 07 Apr 2026 02:33:27 GMT  
		Size: 10.3 KB (10274 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:848692e22534e0530f305f64db41506e07df400f1129cd4db5a53e11d539725c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242434761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ca5d5c709e67c85956fc952b12927d58bfbbcaa73dfc30c9f5f3413ff6df09`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:39:26 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:39:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 07 Apr 2026 02:39:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70eeb54f055229804030ac8dfdb6ce0704417b7da28fcfaabf63791985cf24c2`  
		Last Modified: Tue, 07 Apr 2026 02:39:50 GMT  
		Size: 213.6 MB (213560686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3a767503d27ad8acfe20cc174c560253d6a36c69091159b3911a7b89b2c03a5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2369740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:873a5f339fcfd13b7fba202caf98f989bb1f7b13be6d359e049e2485b6ec3f8f`

```dockerfile
```

-	Layers:
	-	`sha256:476a0e845fb9647379ca7a8c8c868d087bfc49fe0fe970d4fd5d7981d03dc9e1`  
		Last Modified: Tue, 07 Apr 2026 02:39:45 GMT  
		Size: 2.4 MB (2359314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3771212914984cd471387095f269e9d27e7594b1c4b67f07e0bd17c42df6505a`  
		Last Modified: Tue, 07 Apr 2026 02:39:45 GMT  
		Size: 10.4 KB (10426 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:a55f4eaa516164319a09a8f5c5cc59095d8c54fae03086b6d709d342166d29b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.5 MB (250481072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e8c6a1f3c9c4c7de81939de28e69201c221e7d84db15bdb0f2e5a569a21bf82`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:25 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:26 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:29 GMT
ADD file:ede7e3b047d459e8abfd20afae677192c0eab70c709496e87b2110289bfb5f3c in / 
# Fri, 03 Apr 2026 15:15:29 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 09:07:46 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 09:07:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 07 Apr 2026 09:07:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb318618821b175586e236bb7761b198b58de5561f4bebafbdb987dadf5d6a64`  
		Last Modified: Tue, 07 Apr 2026 09:08:32 GMT  
		Size: 216.2 MB (216167738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ec4547725c26b7ecdfab097fcd64a000e6af7b110b7a7e571166fd74fefd2ff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc385552f18e1dfea53c09e72e7a014cd2a900cc67e2bfe597bf5b49f2a2c0f`

```dockerfile
```

-	Layers:
	-	`sha256:4621c07bebc814849811d339b5ef3c8be7b8f2ca50074ed0e96e3210a60e5533`  
		Last Modified: Tue, 07 Apr 2026 09:08:27 GMT  
		Size: 2.4 MB (2356278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4059760e71423c3ef9bc10fd5b5322dc031104c94b31dec6adbb470b7dd92de3`  
		Last Modified: Tue, 07 Apr 2026 09:08:27 GMT  
		Size: 10.3 KB (10342 bytes)  
		MIME: application/vnd.in-toto+json
