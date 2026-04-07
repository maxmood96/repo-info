## `sapmachine:26-jre-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:0a14437fb0797faeba1cfe038801c46d932e11da0af6b9c8d179172e8feeff5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:26-jre-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:36d39aebd80d1420fbc3f52faf5c3a6711fdbf193a7e76ca6f3e2cc96557fd1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87538118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a40bcdc3d89c9b769340458ae7300081d37b965ae1484e5422f9f4609b060477`
-	Default Command: `["bash"]`

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
# Tue, 07 Apr 2026 02:32:23 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:32:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 07 Apr 2026 02:32:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284f91cb4c359d4da29f0fb77e36bf937ee6bbea78064ead7d30b9376bff445e`  
		Last Modified: Tue, 07 Apr 2026 02:32:36 GMT  
		Size: 57.8 MB (57804659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c418528841f83380b53cbd0c7d59680a2029456d8f9066f5980be111802c55cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2289195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a079094de4bba21160be3e7d8490d4b615acb8b8f70116f31825f4957f679b`

```dockerfile
```

-	Layers:
	-	`sha256:f5d1975e3ba5396b3da15d9fd74d36911944982ee8156b41bf03b1a53281da08`  
		Last Modified: Tue, 07 Apr 2026 02:32:35 GMT  
		Size: 2.3 MB (2279044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a3a4bdf5b8b018a21ab69a25195da241dfb67843cf9b54e9331c774db560351`  
		Last Modified: Tue, 07 Apr 2026 02:32:35 GMT  
		Size: 10.2 KB (10151 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jre-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:110a4bc5afb28304852d483585ff09d8242ad61d040d3b6455c63d7478f4568e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85683570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f3377d3993445654ecd4032da269762f3aad595a512ebef9f5599b5160a721`
-	Default Command: `["bash"]`

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
# Tue, 07 Apr 2026 02:38:38 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:38:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 07 Apr 2026 02:38:38 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640205fd12edc6c6ff37d10ae7278b01d7835db933782cc4a5223fc82f5ed39a`  
		Last Modified: Tue, 07 Apr 2026 02:38:52 GMT  
		Size: 56.8 MB (56809495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:db02abd92c7b82baf64567837ff49b5df091bee2f7c7e56779d6d989b0573be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2289852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc767114c14c3094780e128f59d17a91053d74992b21013d840df1a0036138b`

```dockerfile
```

-	Layers:
	-	`sha256:a8a7dd808649c33322be4547149971e8c9479d2f19443be8d8e40f65429942f5`  
		Last Modified: Tue, 07 Apr 2026 02:38:51 GMT  
		Size: 2.3 MB (2279548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e51d2b69520e0522d54b6a29e14ecff3c367fceb9e79a703e9f5d877af31c2a`  
		Last Modified: Tue, 07 Apr 2026 02:38:51 GMT  
		Size: 10.3 KB (10304 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jre-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:14b35e502103397cc2207fb5eac4b2751262ce16e03a30982e5bfced186e431c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93092786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c13dffed96b26d26a080333c34bde65edaf0b2e1c745c05c47b4c1ed259807b`
-	Default Command: `["bash"]`

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
# Tue, 07 Apr 2026 09:02:38 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 09:02:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 07 Apr 2026 09:02:38 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f98154d322f56db364a8050c7a741355a27a4a4cadbc8c09ec238f7b379000`  
		Last Modified: Tue, 07 Apr 2026 09:03:09 GMT  
		Size: 58.8 MB (58779452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bfdae44850fee740ae21e8c982ced17110c5daee2e043cfe068bc8a4fdbef49b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2288051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53ceaa1e80e071c36978459260fbdf8ff090110f787a6f948ace5f2e2df9b565`

```dockerfile
```

-	Layers:
	-	`sha256:54ad142db09a3e98da44c6c82e37439700f64fa7422a9c4c7e1aec48fcead88b`  
		Last Modified: Tue, 07 Apr 2026 09:03:08 GMT  
		Size: 2.3 MB (2277831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bca651b7e644494398e5308d8a080337f987d24c6682b2dbf86583f3cf833a2`  
		Last Modified: Tue, 07 Apr 2026 09:03:07 GMT  
		Size: 10.2 KB (10220 bytes)  
		MIME: application/vnd.in-toto+json
