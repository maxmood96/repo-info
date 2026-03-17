## `sapmachine:17-jre-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:e81ed8ef28524d98221307e8bad4bfd150ba7df22b18c90b93d44668c9fc09b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:2fe1857b3e2e4993873b948dda29cdf8208191f2c2b9d4d2525483e4896e1355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84502494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c2a7b03474ab17725dbde571ba2d4fceb6320b7f171feb04739e9a690bfb822`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:25:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:25:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Mar 2026 02:25:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c21c0cf590f041bf2ca26df90977180a74748688735fb165af7b54839ac78e5`  
		Last Modified: Tue, 17 Mar 2026 02:25:24 GMT  
		Size: 54.8 MB (54770501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:393c4236a74e916f173559cb8ce7638b27b5bfc40fa68dd2bbe76dc9dae09f0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2529847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec91b5c4dbea440f9aedcde890a99abe33e8afa1b6dc47ff5c1e17f52880597b`

```dockerfile
```

-	Layers:
	-	`sha256:c2e4e04444f66185cb8d6a2ea06851e6f47fe4e9e968af7bda201a4c931c0cf8`  
		Last Modified: Tue, 17 Mar 2026 02:25:23 GMT  
		Size: 2.5 MB (2519802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dbf8df6cdcf4d685032e51f3578281a860694fc0ec001a7a82e21fce3e72cad`  
		Last Modified: Tue, 17 Mar 2026 02:25:23 GMT  
		Size: 10.0 KB (10045 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:516aa5adbeee37d99fe8fc7486ceb7e04f66328bb55a078e6f0f86dacae2ff2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83072015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b1c5dcb1f130fd5749dfc77e9e36dc94c4a867bd8341b4d03fbc74e38e6d775`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:31:23 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:31:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Mar 2026 02:31:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988b97690056879b2e9819f7ec1dd9cf66fe3a117d4e471ec3829f4e70da1587`  
		Last Modified: Tue, 17 Mar 2026 02:31:37 GMT  
		Size: 54.2 MB (54202306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a4566e0f510f6f8082ebc88deac21a85e5b83f953591663750d5341ea9b8d181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2530516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7327743f6418c643067954bcad5efd8d88c8ee6b8c5cc3f7bd6d689867b6df1e`

```dockerfile
```

-	Layers:
	-	`sha256:7f06730668dfa27c58dbfb2b80d8c1463e44bbe72b3bfbac27b012df6cc0ceae`  
		Last Modified: Tue, 17 Mar 2026 02:31:35 GMT  
		Size: 2.5 MB (2520318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:627415e3074905c3aec886388d7224b47aeef8269d9b1008c02994922e0b76b0`  
		Last Modified: Tue, 17 Mar 2026 02:31:35 GMT  
		Size: 10.2 KB (10198 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:5d30747f02737ceb53e517ed21ed31b2214b3e3a38b1238ec064f45166cfbaaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.4 MB (90379288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd277193684a641ab6706366143458fa10d1cc04e928d0663793a0cd0b8f9887`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:50:31 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:50:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:50:31 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:50:35 GMT
ADD file:993db8d05f03953198d71fcb66f9a9dca68dcfd7ca7b3e4a866954aa297b35ce in / 
# Tue, 10 Feb 2026 16:50:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 21:36:07 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:36:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 17 Feb 2026 21:36:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:de86bbb8cdc5c52dc9167f3fab22b2f39424ccbfd06ab6c7b34bb3456cf0ad43`  
		Last Modified: Tue, 10 Feb 2026 17:41:57 GMT  
		Size: 34.3 MB (34306906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bd219eca1947f6ae5437f10567d75741584d4c0bae306d0f6249c27b36a5b2`  
		Last Modified: Tue, 17 Feb 2026 21:36:40 GMT  
		Size: 56.1 MB (56072382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d01648edcb9e0bdfc30f6f106644e420c24a1a514bd16fc2c550665ee480a372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2529374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ece7b44d693c2f94f8c2305f02bf0749a20f56438b03079c51f143c0c5ca6ae`

```dockerfile
```

-	Layers:
	-	`sha256:39c9ef8c95964897bae577be04f1a462eca5bcb4c63222b36f13524edcae8ab2`  
		Last Modified: Tue, 17 Feb 2026 21:36:38 GMT  
		Size: 2.5 MB (2519260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08b38ba7f47b6218981520a2fff43f3438960310ff6638155bdf583a4e7add8d`  
		Last Modified: Tue, 17 Feb 2026 21:36:37 GMT  
		Size: 10.1 KB (10114 bytes)  
		MIME: application/vnd.in-toto+json
