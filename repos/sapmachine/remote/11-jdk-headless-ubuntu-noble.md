## `sapmachine:11-jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:f46bbc8b4fef0536a1036369ad4001cbb52a01f2ec73f15e96457222f0d1cb1c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jdk-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:906afc20993e845a42894049009db5d68f954e7509e98964e5840ef6627f1bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229794810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c76137db9fe9cb9bfbdcccb7e1e6dcca954b97fe28b1a00610214e35f66c871`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:54 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:55 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:57 GMT
ADD file:a3272496fda5a8d021b94dccaa6baa685ded51e9d23edb05f0b30978a83c9fc2 in / 
# Wed, 16 Oct 2024 09:25:57 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0577f3c8fa24c375287e44f7df2fde5893debbd5dfbd17bdaca199ccc7a4a97`  
		Last Modified: Sat, 16 Nov 2024 02:57:21 GMT  
		Size: 200.0 MB (200043026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6854091dc4671530b4186d998e63272c0e7c8638c9e98b6a420e3d70fefdc215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2252952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e40de265634ab067ef4be5000209a4fa7eebbbbcc5326a5399d0271bccb556dc`

```dockerfile
```

-	Layers:
	-	`sha256:51aa5c9cc75216b5296d756bcb977fa75895c7b108aecbfd4b23b31d292a858d`  
		Last Modified: Sat, 16 Nov 2024 02:57:19 GMT  
		Size: 2.2 MB (2243333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37a9bf5ecdf8eb7d56767459f01e3aab3a81e25b07f439cda5b8692b2e73ffaa`  
		Last Modified: Sat, 16 Nov 2024 02:57:18 GMT  
		Size: 9.6 KB (9619 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:3b93ea78cdc3379f088e1a379c8448893b10f618d92339862b1342d69b340075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.4 MB (227433825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c54ac15f8c975d09615a7109cc8c17a8092e5318170aa6c51849f2a0c0c3d42`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:38 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:40 GMT
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Wed, 16 Oct 2024 09:25:40 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65356c87b02ea834375ade8aee58f870a53469e0ea8058c2896757084d85b2c6`  
		Last Modified: Sat, 16 Nov 2024 03:55:35 GMT  
		Size: 198.5 MB (198541400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:178c708bdf61f5ff1d36e953e9a5242d457628fb3e9637b6c9eb77bab23c680e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7e2c0cfa4db43fa5aa2d2f8928d9365c34ace21a0e0f8c833dbc93c5a07d56`

```dockerfile
```

-	Layers:
	-	`sha256:9a4cb47852b0e5ad997fd25886657d693d5f2e7b75ebfa68dda22186b3e8ff0a`  
		Last Modified: Sat, 16 Nov 2024 03:55:31 GMT  
		Size: 2.2 MB (2244443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dee005718af8b44d3f3f55fd9896c2141af11662fd61291a09dd237b2adc329a`  
		Last Modified: Sat, 16 Nov 2024 03:55:31 GMT  
		Size: 9.7 KB (9747 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:a81b606fdb8f20cd0195a7966bef1abe7b8242895ee5f171081f36c7f2b3ea9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 MB (221037690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0a46a93e9f01b1d3f2a3daca3421b159b25b26e655959acac1341ef7bcb540e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 09:26:09 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:26:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:26:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:26:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:26:12 GMT
ADD file:8427b57c40c05cd946f6695dbd1754b0a521a98decd2cdc16eeb114c7128804a in / 
# Wed, 16 Oct 2024 09:26:12 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:991986948126e836a79c1084e3bee33549a43b83cabfe16234aef5b4b30d86f9`  
		Last Modified: Wed, 16 Oct 2024 12:48:24 GMT  
		Size: 34.4 MB (34388822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0bc9171757f7cf4632f617744ad0626de20a72564f9bc7ba8709ea0e574998`  
		Last Modified: Sat, 16 Nov 2024 03:59:08 GMT  
		Size: 186.6 MB (186648868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ea47439d8020f65baaa54b10de55546e339c14339bafb6ed279dd65142ac111d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebe6166e6599227780126b0a49b3f495757013295cdfa08a68dd52d89bd49a2`

```dockerfile
```

-	Layers:
	-	`sha256:dde5ce1d24bcb45ea3e50a10257caba33826e2b3695f353ac4ceb4866b7cc8d0`  
		Last Modified: Sat, 16 Nov 2024 03:59:04 GMT  
		Size: 2.2 MB (2244645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30c85236c5ff714899e8150af8e2d37347698bae7e1b3ffb15736596ceca2a36`  
		Last Modified: Sat, 16 Nov 2024 03:59:03 GMT  
		Size: 9.7 KB (9675 bytes)  
		MIME: application/vnd.in-toto+json
