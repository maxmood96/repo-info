## `sapmachine:17-jre-headless-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:f6a84166b3aafa18d8babe8904ea3aa16a7031ec176f2a25c1beb8b415bec990
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:f00fdcddacbf590653926b03b3e4c6d8182097c6b44ce29dadc5f3f068f2a20b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79557762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284618f11a9701c7ab98135cfec6f3a455dfb496443a337c1b8ac8931ccbf214`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e55ab9e58107cf4a48c5322de63d98b28ee2998fd086222dd9e83cebf8c3d6`  
		Last Modified: Wed, 02 Oct 2024 01:59:48 GMT  
		Size: 52.0 MB (52046710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:18363132df24a4d58bbe5e90ab76b87cafc05f6b9cbe528d1ab86a686301949c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2051050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a5c4f180a3909410f7675c680202604c6806db0b3ea8f13eb4d22805e3a01d`

```dockerfile
```

-	Layers:
	-	`sha256:ae36f7490d1a37f66cf75b4fba2f3c9c0429b16c7ddcb94ce76a2a06a587ac85`  
		Last Modified: Wed, 02 Oct 2024 01:59:48 GMT  
		Size: 2.0 MB (2042367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952a7f8d739b8f3442857193fae05769050317d55ebe4a51d3c81dff13b67cbe`  
		Last Modified: Wed, 02 Oct 2024 01:59:48 GMT  
		Size: 8.7 KB (8683 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:d4a856cb0988205f2050bede9933a5353b075a92e17d95f98f2b3f03750c680f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77399202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276f1ef5188b8a6d12e2b67db378cc94410f6ebb7676ec7ce9f720d7a82f6e8e`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7087ec3f63a82386ce40d74d075d761ece5bfaefdc30b9ef62f73ecfb2e41fe`  
		Last Modified: Wed, 18 Sep 2024 05:32:46 GMT  
		Size: 26.0 MB (25973592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42bef9abdc1e5b65d0c2d10f9c8c5eff0578ed379b15f35299715884a0acbe5`  
		Last Modified: Wed, 02 Oct 2024 04:03:35 GMT  
		Size: 51.4 MB (51425610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:368da3b4a834d40835cc1c6ff4055cc34c61ea91aae7567fc27491248638874c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2050775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3789e3caa0dc148317e14c12691f8a3e811d91984009dc248ee2573d88a08ee7`

```dockerfile
```

-	Layers:
	-	`sha256:8c7cff973cbf0fe19997a4cc3790dc5f8aa511e671e884f047ccf1f73601d8c0`  
		Last Modified: Wed, 02 Oct 2024 04:03:33 GMT  
		Size: 2.0 MB (2041994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52f0483d19b1fc502427d4ebf852aeff05f6f1094c413246ec6a4d8fa15b2d24`  
		Last Modified: Wed, 02 Oct 2024 04:03:33 GMT  
		Size: 8.8 KB (8781 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:ca0ee9e1cbfc6fe43ec728ee0e0436f1cebd47a2378959c8bad776aa73057b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.1 MB (85074611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb06f1c3984390e31fc5c22a2e82c55157dc5a59603f9d392ae309b5dd36c51`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:c6515e5ea6494efa348e1177d50c0c28bb8236a5d2b518388f13b7d5a528d4fd in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cafd57629abc05d597016161b87b83b544a17d39d1016cfb289a60295fc7d492`  
		Last Modified: Wed, 18 Sep 2024 05:32:58 GMT  
		Size: 32.1 MB (32076334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d429e8afef6b147e8701e128183278262c9d71b6415860b8ed5fcd772bb809e2`  
		Last Modified: Wed, 02 Oct 2024 03:19:37 GMT  
		Size: 53.0 MB (52998277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:972841fe30817be9a08572fd79536270115cc6b116d26e3b9d33f1e70a40949c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2054790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57d670665da28d8961bbf7e757b8ce529c1e88d85b570251400d49121b93c663`

```dockerfile
```

-	Layers:
	-	`sha256:9bfd6be8a18b647bccd75a909944dbfdc979217fef85021b6e020fda96e0539d`  
		Last Modified: Wed, 02 Oct 2024 03:19:36 GMT  
		Size: 2.0 MB (2046069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:581a7431e277955ced9b83bc36ff9baae9a1c58f10b2956ba3f908712d098c28`  
		Last Modified: Wed, 02 Oct 2024 03:19:35 GMT  
		Size: 8.7 KB (8721 bytes)  
		MIME: application/vnd.in-toto+json
