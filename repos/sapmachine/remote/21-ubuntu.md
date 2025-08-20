## `sapmachine:21-ubuntu`

```console
$ docker pull sapmachine@sha256:e3540c4bd95fa0a80ad62e29ccd79ff28b4aef2d169c1c4fbcf8061810ecaf6a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:c4cf09ae5cc578421b2edfb80c3c6a5b1bf260358c4357fba29ecaa089e85067
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.0 MB (245033315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afbac6d6e124a0290a0a3a90fde90be1b12404a2d757ca4fee82be6e57e6ef19`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7788dfcfcee8ce7fb5d57f3b777ca4770fa86d992b0815b3d0e4316d0baee2`  
		Last Modified: Tue, 12 Aug 2025 18:10:45 GMT  
		Size: 215.3 MB (215310100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4ca89481496289a7f0a2e6c67544485eaeb298ae07390d4a77c35143d33e3f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2621838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8cf5eb0182dbf5b5f1e9aaee362d8e7d92b7324a3f9e5603d5a82310b41ebb`

```dockerfile
```

-	Layers:
	-	`sha256:52df347fadbfb6979629e25f26e3455fc7c181b255ed76cff4dc6b7b275fc32d`  
		Last Modified: Tue, 12 Aug 2025 18:06:12 GMT  
		Size: 2.6 MB (2606953 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43f264dd8e760261e68816a536c5c28e3fec86a1cae256a11ed14119e8c5b084`  
		Last Modified: Tue, 12 Aug 2025 18:06:13 GMT  
		Size: 14.9 KB (14885 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:97bab0232cdbbd8cd4afc931552d5850bd3dad8f0aed1263f27e2d1c732682de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242406828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac4c487dd0f2fd450dadeb261f0ca659966d7211122298ecc004be9cada7279`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7da4bbe26e5ed1f4185e18fa9980133a0e7ddd43e7a60b609e4088c3ffe4e8f`  
		Last Modified: Wed, 13 Aug 2025 07:32:50 GMT  
		Size: 213.5 MB (213546451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5c26b92710e9fee09fe74951d8ed7dc1bfb86f783f28850c29c191e705513b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2622866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6faa5a386e6bd3e0da52586c740228964d4fef66648ab046a5fcce13a38ff6fe`

```dockerfile
```

-	Layers:
	-	`sha256:cc60144d4b14d3f052a894051e2dc933d4c4e4b8f50ed03c2c69df48cc248617`  
		Last Modified: Wed, 13 Aug 2025 00:06:44 GMT  
		Size: 2.6 MB (2607649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31c5a997fa52ea0b77d556febc8dcfc090b59ffc78aa2452c0650db34d1ed609`  
		Last Modified: Wed, 13 Aug 2025 00:06:45 GMT  
		Size: 15.2 KB (15217 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:6471e511034cccd22847f036a84b2c898bd0dbefac32cf5c8bae3af9e3c3778a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.6 MB (250593398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:337a10bbcafb28dba6546c8f24ad25769eb912f5b04596e82a54db5695d95210`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:e2ae399c3aa36bf07b7d3562a21b9ad89f66ae6e03733ed0edcdcda5bd391c60 in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:403b01240f845337685ead3abfb0228bb1d1b78b076d609aa20f4733d260f58f`  
		Last Modified: Wed, 30 Jul 2025 11:30:48 GMT  
		Size: 34.3 MB (34329650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa9184002b3235173621a5c951f560287637d9edd247442d5d0b5d7c5fb91c8`  
		Last Modified: Wed, 20 Aug 2025 18:41:45 GMT  
		Size: 216.3 MB (216263748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bbc318ee3b760be87fc882391928ceec152f8c40fdabd152df2feb2325e101ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2618221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f3dcdb237365b20700794497736fabf3e7ecdac4ee6f54748e005a8916beff`

```dockerfile
```

-	Layers:
	-	`sha256:8a15f459c3737f6e2972a0f473c21445295b8441652597128049ff9e4d8fb3cc`  
		Last Modified: Wed, 13 Aug 2025 00:06:49 GMT  
		Size: 2.6 MB (2603178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f77efc3e3580ec02ee872a1da278b36afb81f9a896603971433d9200a091ddd4`  
		Last Modified: Wed, 13 Aug 2025 00:06:50 GMT  
		Size: 15.0 KB (15043 bytes)  
		MIME: application/vnd.in-toto+json
