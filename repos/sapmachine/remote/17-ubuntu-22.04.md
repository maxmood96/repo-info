## `sapmachine:17-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:df55ab6d9ad68b56cf33d05e30ac19bfb6c69275d556c44e56e818a8da3fbf46
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:09b4dbfe829bdc40bc8fb2bc0d1d0010d82d747e3b16d7d1622f553ba0a1f633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229549472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f0fa12ce71a38a49c2256dddbf8b6640012b59f3a53a5ff151f406748671d34`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:41 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:41 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Fri, 30 May 2025 23:34:45 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba438839f0182274472764d120f1c4c13ce4b8a64657c0a2a2d137bb516e3773`  
		Last Modified: Tue, 03 Jun 2025 04:18:16 GMT  
		Size: 200.0 MB (200016469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d3072ebf45d5c24a2c5646fa51715f3a635ba57b6e7e205d3d550d83d503aaa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2528150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2baa16e31e5e0005ab71fee7556d4e848d9109f125b5d069eefbe5f550d9b0`

```dockerfile
```

-	Layers:
	-	`sha256:6d99692fa1bd821051514686fb86ba66105c8f45d7883be5a63f394f3b3c0a8f`  
		Last Modified: Tue, 03 Jun 2025 04:18:13 GMT  
		Size: 2.5 MB (2518012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6dca4c121ceb1640d4ff70b92bbf117d3d57272dc90a7fec7e5b7d688deef39`  
		Last Modified: Tue, 03 Jun 2025 04:18:13 GMT  
		Size: 10.1 KB (10138 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:17a1aaeded69a2873de830bd1d38c3f78b7b4f3303350ba5ebb23c84e209d40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226068212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c46b5152859ae379d82d4cdcd1bdbe328dddc56b84bf026d5cac5e829374ad7f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:41 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:41 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179f6dd11fa1543c0ee2582dad777bf6a45fe8a8251ee06633f67118871d573f`  
		Last Modified: Mon, 05 May 2025 18:41:36 GMT  
		Size: 198.7 MB (198714001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a3bc699449704039fff03590d6a3483ba54435703981b42a4cc235fd7af6edcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2501698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719228bffbba833c5d961c14af9612201f92429243fc9a5938906a5faa507579`

```dockerfile
```

-	Layers:
	-	`sha256:386c39de8ede2309f573e6ac30353fdeae75236abd8fd385d24c033362395828`  
		Last Modified: Mon, 05 May 2025 18:41:32 GMT  
		Size: 2.5 MB (2491408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc4b8ff33d36aba062a6c17acef1ea2b828fda6bbeec3a0c931ac90d90a0aa26`  
		Last Modified: Mon, 05 May 2025 18:41:31 GMT  
		Size: 10.3 KB (10290 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b5b35e1536a8d09db45d8ff062890ce8a646cc5792f497c728140d71a505ba8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.5 MB (235531744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07cc53c19eca45ee54696d26eeaea29c07631bed7ab5d30dd2bac6ca2cb83422`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:41 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:41 GMT
ADD file:f6d72fdda03fb8754d82331b1f726d49b6b7d2d850ad2d1dfc2de6e1b365251b in / 
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:95ba4619a43d3f4f7f5ee2c8fbe313d19bb9c0e9ca5fa9efeb7b93f942dcf377`  
		Last Modified: Mon, 28 Apr 2025 10:44:03 GMT  
		Size: 34.4 MB (34443215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e4f901ef81742cdb23b180946d09a0592336361d02d19bd275a3241c5c2a39`  
		Last Modified: Mon, 05 May 2025 18:39:29 GMT  
		Size: 201.1 MB (201088529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:616c849dc20bf56b4a4eae8cb94d495da4e289ef76abae7e88c1e3eafb3fe760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2503943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87cdbaf658a11dcb1289b3c6c7408f408060ca2fe5a91600275f7a5c7e004c93`

```dockerfile
```

-	Layers:
	-	`sha256:aba54e4be709af00987b90a2f868c9ca9166d3f600e2949b97fb9dcd1502aa4c`  
		Last Modified: Mon, 05 May 2025 18:39:21 GMT  
		Size: 2.5 MB (2493737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91f1b2afbf06235221bf41d5afe204d57b73490d73a4b3a6fadae4615d9e23d1`  
		Last Modified: Mon, 05 May 2025 18:39:21 GMT  
		Size: 10.2 KB (10206 bytes)  
		MIME: application/vnd.in-toto+json
