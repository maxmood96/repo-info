## `sapmachine:jre-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:edac846f6650da6c75f439bbc5afa383ff7f16cc8a3135c9ad3e93f204bbbd96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:e74622bd4152bb6967c8966fe6ea61af2577f90c6df154e57e8d5662d36d0f98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94720120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1783ecc35432fced9e888dc99ea8f67dff7fcf3c880021ced46cfcdd3ad33c55`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:66f469347b3520ed621aa82537dcdfd65319bbcc73f92a8f0e4ae6db5facd6c9`  
		Last Modified: Wed, 09 Apr 2025 01:20:39 GMT  
		Size: 67.2 MB (67209726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5795d49ddec341a764a73c076ad24bc8ff7dab95557d54cbba4f3c8c84339026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2316337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9149baebf67a014994d7786d51f5803a1c1536df246265450b8d4e3aab1b1b`

```dockerfile
```

-	Layers:
	-	`sha256:e0022836507902f4af89d8075410e8a8d5631105dcd45050636efb7e6d1b08ec`  
		Last Modified: Wed, 09 Apr 2025 01:20:38 GMT  
		Size: 2.3 MB (2307561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9afe0e7393d99553165a6586631700bc8900454755ae8932053a3c4dba318bac`  
		Last Modified: Wed, 09 Apr 2025 01:20:38 GMT  
		Size: 8.8 KB (8776 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:a830d04ef8433b50228b39ecc878fb6134ac82fae468aa3abdfc5ab11db41e23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 MB (92215643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86da4735508ed839cfd609a7e2f36843d48a3efe7e80daeaf369ee75ca10772e`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3e2a474b6acb3ff7a851f91fbd74331e7960b607d8a6803dd0b1df5970521c`  
		Last Modified: Wed, 19 Mar 2025 20:42:31 GMT  
		Size: 66.2 MB (66241815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7bd62b9354f4321bb774adff757b9508d78fd33025e634ff267a44898dc54062
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2315976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8ee2f2e1d177cdc841b76792a7f55f658c72bf5d85922c42c34ae6ec555795e`

```dockerfile
```

-	Layers:
	-	`sha256:2f813df4d067eec6e808eb120154e9f339ac109d2ef99047dd8600c221065d48`  
		Last Modified: Wed, 19 Mar 2025 20:42:30 GMT  
		Size: 2.3 MB (2307096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da10658d3596a07cdebdf5979fc098062c07f9ee28e825436cd2f3a69ec1fed6`  
		Last Modified: Wed, 19 Mar 2025 20:42:29 GMT  
		Size: 8.9 KB (8880 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:651805e89b72cf922a4c9a1dd3459c317ca8342a2aeb0844d650b66fa5e23b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.2 MB (100182895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c0e28ddf8792b0f6f212b5df2903df6a79ad3f7d0f8afc06ae7883b4278f5f0`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:35 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:35 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:38 GMT
ADD file:869a92a1e06a4985a0281417502ee0c0d8ba6cc4e0b72062dd8e4eb87833bae7 in / 
# Fri, 11 Oct 2024 03:38:39 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cd720328ce8da41e08a7dd5922261b0c1980c2565df21b810488c55260400f68`  
		Last Modified: Fri, 11 Oct 2024 04:41:42 GMT  
		Size: 32.1 MB (32076506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12dcb9c8cbd7226c516e02d2c212a6282f78463d24412c2989b64d4a0eba797b`  
		Last Modified: Wed, 19 Mar 2025 20:47:26 GMT  
		Size: 68.1 MB (68106389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5e724ce999f427c2baccbac3813198a4a5bbbf9b8c73bf6757a520fd2aa1fcef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2319416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159022d29808e1607a6f5801cb8fee83de800f08fd0493b9a796a49698f50955`

```dockerfile
```

-	Layers:
	-	`sha256:8e224d8b69e5c1f14faf923df4756173e6b51bc3ba8ba63b611e26e813a0d314`  
		Last Modified: Wed, 19 Mar 2025 20:47:23 GMT  
		Size: 2.3 MB (2310598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57784e4f7870b4e2f333fc99bce8d90138998c9ea212819faa69d9d97706f24e`  
		Last Modified: Wed, 19 Mar 2025 20:47:23 GMT  
		Size: 8.8 KB (8818 bytes)  
		MIME: application/vnd.in-toto+json
