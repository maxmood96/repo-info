## `sapmachine:21-jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:aed5cfa5f4dd48a9533074d77e31c0ece091c6c7d2027d69b80a0f8c11a8b2ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:675895a0ed85e27aa2736129e4d84cf004bd7f0f08e09fbe34d7f3012ed7578a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89384709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d961393fcaf024514e7b6e1d165a5bc74f7b916ce56719bf9d577e71742a423e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:39:03 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:39:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 13 Nov 2025 23:39:03 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7e1c1d22357188e696f2105c0d752f28a6e1ae4bb19558a77ef18aa3d8632f`  
		Last Modified: Thu, 13 Nov 2025 23:39:30 GMT  
		Size: 59.8 MB (59847911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:487c2ebab0f985a4601fc4ae0436dea1016e9dba68dbc5e2d076235956ebad55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74af9e1871b71eb2ffe7dd4da0430220cac49a3f00230ad405cca68f329ed1fe`

```dockerfile
```

-	Layers:
	-	`sha256:9fcefc4eefc707b020a07f4d203a1122eb9f7702088d79b2c62e3846bd715cab`  
		Last Modified: Fri, 14 Nov 2025 01:10:49 GMT  
		Size: 2.5 MB (2544889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd70bdb5ddab7f4be53178babb93b347a621c301eff4ad87529e72c6414274ae`  
		Last Modified: Fri, 14 Nov 2025 01:10:50 GMT  
		Size: 8.8 KB (8769 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ad1b10c3f189daca8ed17596220c602ee1fb55d8abd1f4bab91130666663c792
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86368982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212d0cdeb6d5c42e97693fd54c2c60b1948222cce02842a8467ec3d1479c38dd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:38:15 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:38:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 13 Nov 2025 23:38:15 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03edf874b3661c7dc8f8121ccb1b8b64bc80a988721353377c953a60f4750d34`  
		Last Modified: Thu, 13 Nov 2025 23:38:39 GMT  
		Size: 59.0 MB (58985105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4ca515aefea7623e3f531f662e3ee1f9e817cd3aff6a8d83f74502941cf2cf1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e54fd64d98c0e86ba4993c33d4c78929746719f23bdbb0b52de3dda680c974`

```dockerfile
```

-	Layers:
	-	`sha256:c24d3367252450a80662a4fdc549ea0a55b37d856a9c4f31884103817f1d73e1`  
		Last Modified: Fri, 14 Nov 2025 01:10:54 GMT  
		Size: 2.5 MB (2544571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:432cbb85198ccf68cf3f8aab471031ad8b255852a17397da3d92aa79ae779235`  
		Last Modified: Fri, 14 Nov 2025 01:10:55 GMT  
		Size: 8.9 KB (8873 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:a9087852770d3100b12236ead697673de678a43ed72158841f2091dc80d07c41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95408857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1fa77f02e439552acb6b530d02c480ebdf64f0eeea39029d58390f7258b8d3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 01:38:34 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.9 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:38:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Fri, 14 Nov 2025 01:38:34 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Thu, 13 Nov 2025 23:02:18 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f8d172ff24ac7319f637eee09ff5983fe493578a87ba8c04446e31b3afc5fe`  
		Last Modified: Fri, 14 Nov 2025 01:39:33 GMT  
		Size: 61.0 MB (60962135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:72d395b8a2b0c3ce3b31946f423ffaff9d1a07ddc1251b2a5332695df0979d06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2551817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ea828d4be63d42d177e9507f0b8e08af5d86d8f7cd5296de7956d9073f6629`

```dockerfile
```

-	Layers:
	-	`sha256:0b85264e6a2111c6d85b7c8e3b915e98975cd3e1d8e08ab4d53280a03f984282`  
		Last Modified: Fri, 14 Nov 2025 04:08:28 GMT  
		Size: 2.5 MB (2543004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd1eff92657f74b429c5985743974d6bfd8b02eb750bb670929498d863c03ac3`  
		Last Modified: Fri, 14 Nov 2025 04:08:29 GMT  
		Size: 8.8 KB (8813 bytes)  
		MIME: application/vnd.in-toto+json
