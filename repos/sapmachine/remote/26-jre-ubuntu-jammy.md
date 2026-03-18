## `sapmachine:26-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:63ad5acc6e806d8283193a4234b27af800823fb4df567b45500d0eceadbdbde8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:26-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:6aae96b97c4fa440edd88fca50ee1872867945a8989d49d37af9eea64722f59f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88144767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aaab6bbac6aa58ca9375ad4b84606d566b19a4b06cca08489dc2428503420f4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Wed, 18 Mar 2026 17:49:48 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Mar 2026 17:49:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 18 Mar 2026 17:49:48 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7b7b37c887ac570b735aff3853f2ce3ea1cc057cea9402b4bf5a68eba61c3b`  
		Last Modified: Wed, 18 Mar 2026 17:50:02 GMT  
		Size: 58.6 MB (58606247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:97a7a52ccd706a25677a124a138dbda2cb1670b0fb03da8e1ef654f1f0e9a4ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2559834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7105851b196b647d923a6baba48272ff31974f12d94a141dcf6b63b690f468c`

```dockerfile
```

-	Layers:
	-	`sha256:5ef15b509d0312f50762532c23810a21a0cca773cb35655095a5d5c0acf2261f`  
		Last Modified: Wed, 18 Mar 2026 17:50:01 GMT  
		Size: 2.6 MB (2551105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6458a506d291e4eb1b1cb4876f5a91a2f90a9269738c47de15a3f29921b0520c`  
		Last Modified: Wed, 18 Mar 2026 17:50:01 GMT  
		Size: 8.7 KB (8729 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:39d5bede5ab0fceca4a5dd91c9dace4ea77ecfbbe657731965b031e19286330c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (84957662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1cf9defed2ca27c7eac544e3d2e185525a41372b0dc285ef69fd91c92dc440`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Wed, 18 Mar 2026 17:49:46 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Mar 2026 17:49:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 18 Mar 2026 17:49:46 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da1c75427aa61728765214283163b2b8fc7df840bebd8efe18ef3f31f0fe3de`  
		Last Modified: Wed, 18 Mar 2026 17:50:00 GMT  
		Size: 57.6 MB (57568637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7d40494a7a64e8fc1d009f61b9c5b4c9cf58e64969a4b5d35acaaeac7e5a770f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2559616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ada43b3cc256433aaccce3eb9ff5776d6277ad93dc8e6d680bf364c9a426984`

```dockerfile
```

-	Layers:
	-	`sha256:e44b9a0d8b43612d5a5c302100227f4cc7f22a1e5f1a8c767854c9fec8edfca0`  
		Last Modified: Wed, 18 Mar 2026 17:49:59 GMT  
		Size: 2.6 MB (2550784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afc1830f217fc7a9a2ded8104c7143fd68178442a8b03ae3d8f1ad8dbacca36e`  
		Last Modified: Wed, 18 Mar 2026 17:49:58 GMT  
		Size: 8.8 KB (8832 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:6f9176fde2564ecfe4f7ac0260da945f2423751b614a21b1b8443300f71fa319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 MB (94127093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df8616125113a5bfe177f618a10aa6e7f24e88e804f843b3e126db6051dd14c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 24 Feb 2026 07:34:11 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:34:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:34:16 GMT
ADD file:8cdc5dcac981a23986a941c048f55a86d8ba46328e91ad30db9af43286781c61 in / 
# Tue, 24 Feb 2026 07:34:16 GMT
CMD ["/bin/bash"]
# Wed, 18 Mar 2026 17:52:54 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Mar 2026 17:52:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 18 Mar 2026 17:52:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:31e4dc9ee1718c21d378c7cdb3929e157eabf4d70fe4bbe2e6b8ec5289e836dc`  
		Last Modified: Tue, 24 Feb 2026 08:08:05 GMT  
		Size: 34.5 MB (34453448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca0e542b0ef770df5af61bb82741a61f3516d7ffce12b44ace2a4c23dc3e95e`  
		Last Modified: Wed, 18 Mar 2026 17:53:22 GMT  
		Size: 59.7 MB (59673645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0ed4fd90f79871551ce9dce92dae8e0b81a8f004419d87305e21d498727cf260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2558779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:793f2e2d1a634a4981a116f770c041b19d002e09301b884d6256c6fe6e9769b5`

```dockerfile
```

-	Layers:
	-	`sha256:80346f0c207a81651eab9b89bd8916fb0f241145a2e7e83e12580001bb08db42`  
		Last Modified: Wed, 18 Mar 2026 17:53:21 GMT  
		Size: 2.6 MB (2550007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30a9256a90a6f16adbfc6533b15abc6994dcdfadb19f669334108201008bb854`  
		Last Modified: Wed, 18 Mar 2026 17:53:20 GMT  
		Size: 8.8 KB (8772 bytes)  
		MIME: application/vnd.in-toto+json
