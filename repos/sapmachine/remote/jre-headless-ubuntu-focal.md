## `sapmachine:jre-headless-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:9f69c08fc4a90a6f5ffa3f8af49b47e56eccc8b9e2b11e55829212e960abf224
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-headless-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:3bb069819c0033592fcb37b65bd5a26e837fae6b91b40e0025dafe16897ccef6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93523740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f132926e54232f85aa955886fcab3d26d74804498319b62a01466f0d68ff9007`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c51ad1db47418ab4e7b04471b002ec7dad9c021f972536af2900cc91a32c6b4`  
		Last Modified: Wed, 09 Apr 2025 01:20:36 GMT  
		Size: 66.0 MB (66013346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:09094a96da20181b6d1ba2b502610c2282c62940750f30322855b35c510e8ee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2078571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fdcd5e484abb9f3b6a8c358d15b114caa8b969970ca9d3fd905e3f3dff6f53`

```dockerfile
```

-	Layers:
	-	`sha256:a2a3cbcb6aeecf1c50c8e9f02e682e7449de161e0872716265f7645b08541c7e`  
		Last Modified: Wed, 09 Apr 2025 01:20:34 GMT  
		Size: 2.1 MB (2069684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d1ab85127b2ca43c11e9329ab2849e1b91abb8b7bf45c113a92bfa9cf246214`  
		Last Modified: Wed, 09 Apr 2025 01:20:34 GMT  
		Size: 8.9 KB (8887 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:c0d2158d73c5bf2cd2a771676ea559688f7ed562597aa61216dfa30bb1d341a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (91018412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2009ffeb9c5a1eb1cd0ec9fc15a6597d4a3d154e20661ba6d646299b9b27c6`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7439aa58e1ed565c21987021c26c9f2be27b9e892c0fb013300b3c86f08d6627`  
		Last Modified: Wed, 09 Apr 2025 09:28:07 GMT  
		Size: 65.0 MB (65040751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f4e56672af0b7c83dc8e424e9469f2ded4258a5514c2172345c68a8e4eb00758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2078301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36a3c1f8b7647c0d4b728e43192ea5fdde75b27bd84e9a6698f3e6639bb7417`

```dockerfile
```

-	Layers:
	-	`sha256:244da58d20e90471b02dae4ec0a293c3999fe20fd7dcf646fb57cdfbb03dbcaa`  
		Last Modified: Wed, 09 Apr 2025 09:28:06 GMT  
		Size: 2.1 MB (2069310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d98127658cd4e0eabde5ed0cc0000115e58895242b7cc34fa6b815f382985e9`  
		Last Modified: Wed, 09 Apr 2025 09:28:05 GMT  
		Size: 9.0 KB (8991 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:905cda5d4afb430c02552143b5b5f391895b95e07c204ecbb552eb7149fd2a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.8 MB (98816098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45723e4de087f8a888b98c266a212f143c8ef138608bcbed56628313d048351`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:d85970cec61787609e3854cb76ce16d54fe420b254cf48fc9ed9ed678717ff28 in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:92d54367a68b4f03400315732acb4290d88bb06f8fe1414fd823f93402bec922`  
		Last Modified: Tue, 08 Apr 2025 11:48:44 GMT  
		Size: 32.1 MB (32076946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aadda2d2711e11915c22acb7d4e12d608ce4428932805f7c76a076f4e7ec0ce`  
		Last Modified: Wed, 09 Apr 2025 06:50:01 GMT  
		Size: 66.7 MB (66739152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:47e5f56c18bb615d5589ad3be22d5283a9a4dc65bc8c9cbe05ea44a8f3011763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2081689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7093e082f3e2cab0380c274ce724b0e4010f4e8e6c63b1396815d728079e7931`

```dockerfile
```

-	Layers:
	-	`sha256:ef46c0966dae747668bfa94ea707bca0916f28267ca227c3322fbbc0437f3de6`  
		Last Modified: Wed, 09 Apr 2025 06:49:59 GMT  
		Size: 2.1 MB (2072758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6559b23777c2a1eb017053fac988bb4aadd8e7dfbb9afe372762da7d7bdab303`  
		Last Modified: Wed, 09 Apr 2025 06:49:59 GMT  
		Size: 8.9 KB (8931 bytes)  
		MIME: application/vnd.in-toto+json
