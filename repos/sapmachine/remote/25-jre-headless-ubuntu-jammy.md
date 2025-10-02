## `sapmachine:25-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:405582cc9a40628ccd8ea2cae7bffacf9d9aa321072ece17e23bce84b3cba35c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:25-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:835c096ea13ceda1cc96160c905ba78aecd2246189ae05669f30860316cb3f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96904991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e189ba812ed064c314acce93dbc3e6892d7a74e144738da9da6427e64d59abf0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Sep 2025 04:28:56 GMT
ARG RELEASE
# Wed, 17 Sep 2025 04:28:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Sep 2025 04:28:56 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c10fdf662c1cf43a0227d398de10afa49c1508c7eae61fbe76ea0bca32ea341`  
		Last Modified: Thu, 02 Oct 2025 05:19:03 GMT  
		Size: 67.4 MB (67368173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4c1f9146c9b5986877250181bb5496bc8b942a16c7ec5c2037d03984225c6b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a23119c7beae0a2743e24339a204468bda3a080aad319831ffe0d53299aeb5`

```dockerfile
```

-	Layers:
	-	`sha256:9e31723b433dcd8b8c266f07ff26c82146f205cb6c2b1733c902905c2ea7c7d8`  
		Last Modified: Thu, 02 Oct 2025 09:13:01 GMT  
		Size: 2.3 MB (2301845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db878b5b5e071a741df500c70ab65b0b718f49ee97b4d32e017da43b943de1d4`  
		Last Modified: Thu, 02 Oct 2025 09:13:01 GMT  
		Size: 9.6 KB (9586 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:9ca2791185ccbd8f5b90e429425b136181475275000cbfa2e812b930994289a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93690791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6dc9b9b4717524704ce091eff68b8aa4d67ecbc84e173cbc64c6fec8f4d7e73`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Sep 2025 04:28:56 GMT
ARG RELEASE
# Wed, 17 Sep 2025 04:28:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Sep 2025 04:28:56 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac5d256bf47c87053d6576a135fbf98ff0db6866564ba7031f546c9f4d31b7c`  
		Last Modified: Thu, 02 Oct 2025 01:34:04 GMT  
		Size: 66.3 MB (66307684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d8203cd365fce30ed255a244e2e0963f67b6dddcd2a38ab2ae9b37ab8ca44f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfae456b2a9a5b272c786f2d0f83c7939f558075e46f16eaaf7875ea5776da06`

```dockerfile
```

-	Layers:
	-	`sha256:df2979427e2479674aabd384c7c2aadefc79360efcb55bd4bbd1e823a0cc7c52`  
		Last Modified: Thu, 02 Oct 2025 03:11:00 GMT  
		Size: 2.3 MB (2301538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf2ea04023fb1a777204564fc1f428f46e97baceedae46f652bb2c8f322b2bdc`  
		Last Modified: Thu, 02 Oct 2025 03:11:01 GMT  
		Size: 9.7 KB (9715 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:bd60e78ba8b0d47fdf2566f9e0dbf80935b67bd9aa7530ecc64a90e34430f0db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102469075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17fc1ecf06d89dd96eb2467888aa4a2a535ac0d00653ef612b930787f49a5f9d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Sep 2025 04:28:56 GMT
ARG RELEASE
# Wed, 17 Sep 2025 04:28:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Sep 2025 04:28:56 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee8407a41aa5e576f2f686e849207b50098655013dcb40547a334ecb1e71e8b`  
		Last Modified: Thu, 02 Oct 2025 04:25:20 GMT  
		Size: 68.0 MB (68022286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cc8707bdc44e69fa3473bc7138031f25b6aba596ff2a94fd9cf2e925e3e78d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e558a866a123040de9775c30eccc4d78abe4aa90f79acebf9c29eb1811fe8f`

```dockerfile
```

-	Layers:
	-	`sha256:efdff3cc2d4cee7a1b70cf3de92d769992a9a364c82621c1933f46b62f4fb2ed`  
		Last Modified: Thu, 02 Oct 2025 06:11:23 GMT  
		Size: 2.3 MB (2299252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:897e6448f887b0d323a2ae61e0cdc586a0c1ca37a376105363eca37bca78e2f1`  
		Last Modified: Thu, 02 Oct 2025 06:11:24 GMT  
		Size: 9.6 KB (9643 bytes)  
		MIME: application/vnd.in-toto+json
