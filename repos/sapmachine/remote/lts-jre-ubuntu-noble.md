## `sapmachine:lts-jre-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:ae32be2a26a07bf97e879e0c844bcdf20a00020878bb236c1dd6d3ec4fa566b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:438c830fda21a786921af7612a716d03dd960db4f5ae044337c85ab895dbe2ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89796411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13357a36c6a13d60ba48d33a09110118641a74790b183808ba2289ff4061bd84`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 12:49:09 GMT
ARG RELEASE
# Wed, 16 Oct 2024 12:49:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 12:49:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 12:49:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 12:49:09 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b153c70e46ec6385a0b6ab52c0cf640127bef6d23324d0f8a4c895447144821c`  
		Last Modified: Tue, 03 Dec 2024 02:36:04 GMT  
		Size: 60.0 MB (60044443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4d6a134e2380884946c808753e6d1b840d2666f17911dd461b4739a39710ef36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2397814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f65fe77eafc78391ad56ffe78a8300365b3bf71d8895e3c16b9014c3659d816`

```dockerfile
```

-	Layers:
	-	`sha256:26b050c352d0eb4489d7983ed47fcad2186238e297534858796bad4d0250ddde`  
		Last Modified: Tue, 03 Dec 2024 02:36:04 GMT  
		Size: 2.4 MB (2387364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b724682d6c52063611e66ffb5c5511cc4e5b5415dd1828e8ad3d5978476370b7`  
		Last Modified: Tue, 03 Dec 2024 02:36:04 GMT  
		Size: 10.4 KB (10450 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:e79a3e9d1a704c0be7e0894ef5c1ca738d0c47e92ddde699b195841595f3cd5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88100936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7febe457c20440b879c7b1731bad38644897ab56c3798de9dfad75a23616471f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 12:49:09 GMT
ARG RELEASE
# Wed, 16 Oct 2024 12:49:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 12:49:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 12:49:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 12:49:09 GMT
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f366b00e3b80ba43697595417a53184031b052ebe48de530118999c4fe25f28`  
		Size: 59.2 MB (59208265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:76730b79e4b5fce2eaf9ee3ec63b4d286b0a423a3e1c5cd1f85d1910c030eb8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a1f178cfeeca14e13b40fe07da94a53539b5ca9b71d12fa13e49abd4eb78e80`

```dockerfile
```

-	Layers:
	-	`sha256:790bc50120afb34361ca4d136c1b2031770b356bc8ec24d722fa48dd3185b8c7`  
		Last Modified: Tue, 03 Dec 2024 10:50:32 GMT  
		Size: 2.4 MB (2387891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa79e26ec69af92f352b47493919bcc5deb0bb439b37491b0344d8967d3f263e`  
		Size: 10.6 KB (10614 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:0fc6e6d56900ecb3ff4089e024294602df54ea03d5d1ba87540c5ba0a9856c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96140029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5534c7ff8f73efa8298c7dfc72e973da35209426b8a25766e2799d926e970e7`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 12:49:09 GMT
ARG RELEASE
# Wed, 16 Oct 2024 12:49:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 12:49:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 12:49:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 12:49:09 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8417540d3457377d4600d25949f5658e9cb01c4baaa9d1169d42f0f2e07c5260`  
		Last Modified: Tue, 03 Dec 2024 08:35:39 GMT  
		Size: 61.8 MB (61751209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cccd1147985223a7ac9674e88f2bd0ef69e0f8d5ace6c8cb72495c185d213e1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27a257e8f0a0c377dd67de2a9cd1e6fa5c3b297e68f21a49ab336bd69f737e53`

```dockerfile
```

-	Layers:
	-	`sha256:24ba6508be0ceb8cd3b84d93173f7685f5c9298ac0fb048fcf710c5e14928cad`  
		Last Modified: Tue, 03 Dec 2024 08:35:37 GMT  
		Size: 2.4 MB (2391331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3727c819e7fde16b2060ec5e28b50b5b3b21fb5c609c79db5750e9b70619f0e1`  
		Last Modified: Tue, 03 Dec 2024 08:35:36 GMT  
		Size: 10.5 KB (10524 bytes)  
		MIME: application/vnd.in-toto+json
