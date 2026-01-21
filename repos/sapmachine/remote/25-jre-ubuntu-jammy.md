## `sapmachine:25-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:29e251fc0c631785ecfe392b969a6f762f33a83e43fe4fa4946e4769f6c36d50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:25-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:28e2b5aa7f2e50f22610b1da5497aef71226eed7130bbf64c7ba3580792e64ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86429421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e0736e119ff20834c0e6c6bf2075ad0c8526d35f6013a9f15800333255fb44`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:42:36 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:42:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 15 Jan 2026 22:42:36 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 09:47:12 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d9883c4b7155e79e24b84cac723e27a3aea2a5ca873b188218a88daffefd68`  
		Last Modified: Thu, 15 Jan 2026 22:43:01 GMT  
		Size: 56.9 MB (56892754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9b010f4499b7bd30b0256186e44ca98c009100ed7f55e3e4e7bfcc067c12e8c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2561446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ec994cb5157aae79c2bb01df9c2f077b45cf46394b877de38e01e226d7685a`

```dockerfile
```

-	Layers:
	-	`sha256:03b2f74351503a2c15fdf6c7e61a428292f0a0e6854073ae5301c503a3ee90c8`  
		Last Modified: Fri, 16 Jan 2026 01:16:16 GMT  
		Size: 2.6 MB (2551357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae3ce76c934285bd630c791e23135a97a70e1078116756482f81bd2ca27d3091`  
		Last Modified: Fri, 16 Jan 2026 01:16:17 GMT  
		Size: 10.1 KB (10089 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:c960e16a0d7bd3be66c6c79ca32d04d91f33550a2cd68cbf95dff0cdac42f63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83162506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068ae71992a9229242a0cde7dfac9cb1e8cf06d297c0acea55d0f303ddc9f5f8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:45:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 22:45:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 15 Jan 2026 22:45:41 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 11:16:52 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd17fddbdb49045edab9aff0d9a45bb61f8d4c6fb70a98df6a1e5a29c3c2ce4a`  
		Last Modified: Thu, 15 Jan 2026 22:46:13 GMT  
		Size: 55.8 MB (55779009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:062e13fed8725e39cc7636e80c14e88923789fc7738975c3560fccc99940f602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2561325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85522e01572eed0b7225dd58e2db09a41449ab7b1538e3e314f7e265e972e076`

```dockerfile
```

-	Layers:
	-	`sha256:ab8f2ada2e01e32bdaa07750ae7529f393f4e08b3950b6151b7450c064b31cc1`  
		Last Modified: Fri, 16 Jan 2026 01:16:21 GMT  
		Size: 2.6 MB (2551084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afcbe7813ce24a5d7e941ffb627a50872b62b623179943d920ff0b4ea3ba4a4d`  
		Last Modified: Fri, 16 Jan 2026 01:16:22 GMT  
		Size: 10.2 KB (10241 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c512c64d1e43ff5c565bbf7f121dcaad64b5d4d1ee1e4e7e4d6f0efc1fa5549c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.1 MB (92134552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee5baee1a50b864391c53a7d3253f24c5654314a752268bf7814febbb1245a1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:04 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:04 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:08 GMT
ADD file:db1efb6f83d2e5fbbebd44054afcb57c6ffff071d50a2434a5322064fe97af59 in / 
# Fri, 09 Jan 2026 07:03:08 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 23:30:59 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 15 Jan 2026 23:30:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 15 Jan 2026 23:30:59 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2490923be26ec970f7d805c10bc7c9c56e219061e875cf31dad74e227e0bbdc4`  
		Last Modified: Fri, 09 Jan 2026 07:36:16 GMT  
		Size: 34.4 MB (34446962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df41e1236aa702c94ef0d4dfc2f9accf86500f6e6794d88050c33fdb82bc4a39`  
		Last Modified: Thu, 15 Jan 2026 23:31:43 GMT  
		Size: 57.7 MB (57687590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d1226fa253e55aefbb07efbf6d51b68c4e0e40b81dd2de8f52ad26bc16f9fae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2559023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b669c1092680f1b671ea28c7dc913564310616dd76ef1a0ee8aa500a0c2d47`

```dockerfile
```

-	Layers:
	-	`sha256:eb7467ebd5703164a643522f76085ed44c4ec8521c25872894568df34f2ad165`  
		Last Modified: Fri, 16 Jan 2026 01:16:27 GMT  
		Size: 2.5 MB (2548866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85cc7a85a5a88ed0af249a9e7c0c8c5b80b826b11d9620c4764b396e6608ec50`  
		Last Modified: Fri, 16 Jan 2026 01:16:28 GMT  
		Size: 10.2 KB (10157 bytes)  
		MIME: application/vnd.in-toto+json
