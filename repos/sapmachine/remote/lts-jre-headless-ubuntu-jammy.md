## `sapmachine:lts-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:401d4e8a42e5e43084274e58fd4cb4ede7db24be8972bf7e72b96114327d1598
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:c182e87697a54c8de0b0e4188d69a1eb12ab149e1ac0d90d9cc82ad44e9a504c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.2 MB (86202196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b027602b12530d0f473069c96365b912bb4d1d5041ff4e73c872a5f1c6403d9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:03:49 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:03:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Apr 2026 23:03:49 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86baa2f6a7976b216b3b9501c114dd2cd4f33e2cc7193821c7fb05edec746863`  
		Last Modified: Tue, 21 Apr 2026 23:04:03 GMT  
		Size: 56.5 MB (56465698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3ff1cd9cde3dfdabfcce2fd2593760938791f5e9152b0be0af4e4de9b96a8425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e31531a019bad2f795ebfe8aee8d582c807e1db81f198dd325d1a7fd422d056`

```dockerfile
```

-	Layers:
	-	`sha256:45ec7388cfba9719017b83aa084e2958d1bb1b39c03560aea04a9f10b5abf8f4`  
		Last Modified: Tue, 21 Apr 2026 23:04:01 GMT  
		Size: 2.3 MB (2302989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:886b9216c3bd041c632db29175795d0dc2985e8eb532f9459c1107a7a75c74c1`  
		Last Modified: Tue, 21 Apr 2026 23:04:01 GMT  
		Size: 9.6 KB (9584 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:27e56aa728db3cfdb51fac04ab32bb15480511866d5512f409e381cc9ad39da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (83007988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9a99b9aed296319311a3671925f0ab949b6a7262e1fe84e8b8e922ff533b8a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:05:51 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:05:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Apr 2026 23:05:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84d3db49f2ee4a972b3958d2d4e87f7916ebabbcf51dc584d3ac8a91b3750b4`  
		Last Modified: Tue, 21 Apr 2026 23:06:04 GMT  
		Size: 55.4 MB (55401445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4eeab4212475aa100e971ac041ba0f15dfc2b5365d91071e721f86a0765ae9f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6abded0d2cd24905e03bf835e4b1171bd243d5d9a7994f11de55f98ec0ee28c`

```dockerfile
```

-	Layers:
	-	`sha256:f7a462abf84725aec8bec917aa465e7c0feac45696145fd4f39e3949b8e4439d`  
		Last Modified: Tue, 21 Apr 2026 23:06:03 GMT  
		Size: 2.3 MB (2302682 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9c613a4688622bba1fd14643eacb9a7950046a758348ffb5b2961f4b139752e`  
		Last Modified: Tue, 21 Apr 2026 23:06:03 GMT  
		Size: 9.7 KB (9712 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:a9aae917d127bc9c69fa30fb12fea745027e768acc02497162f1060fe65d740a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91481669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2165ca1d7e4f36b0fa5dc6690b3b48d02304b8f02d944f389d3e9c863d28a308`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 23:31:43 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 23:31:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 15 Apr 2026 23:31:43 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3cce524f09b16a83286ce5929bca8b300852407c6ecbd9dc182d901af2aeedb`  
		Last Modified: Wed, 15 Apr 2026 23:32:08 GMT  
		Size: 56.8 MB (56833271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e31fd4a984975e859263f4733eabf19739218d3d7a53a6c70c57017198417018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:042c6944887f6c766d3d67b683221676f22e38658b8d0b43853675fe3c4b782a`

```dockerfile
```

-	Layers:
	-	`sha256:b97c5dbcf38006c5eed2ee98d76337b3470830b5071ecdf990cc183384c5fd45`  
		Last Modified: Wed, 15 Apr 2026 23:32:06 GMT  
		Size: 2.3 MB (2301179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8f173d028c5611bab425e4ab828500761533c392ba1fce4d353403447837d77`  
		Last Modified: Wed, 15 Apr 2026 23:32:06 GMT  
		Size: 9.6 KB (9639 bytes)  
		MIME: application/vnd.in-toto+json
