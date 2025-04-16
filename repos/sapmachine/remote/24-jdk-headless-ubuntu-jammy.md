## `sapmachine:24-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:883138897e19eac642414c857a55f1afaa062b66c41a58c5f7317d1009619bee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:df51855ca91295b8126ae4a97a384e6c9d429a16eafa2925314449d1e73ce42c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.4 MB (260369158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac5b951d068d13c28e7144d5e1f2ddcae273d5d53fee0d5a65991910ffe1b2fd`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 07 Apr 2025 07:24:14 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:24:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:24:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:24:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:24:17 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Mon, 07 Apr 2025 07:24:18 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1bb174906e51b2d5d32d255495a435c9dd0cbe42754f0fcc7becac3c8b08f2`  
		Last Modified: Wed, 16 Apr 2025 16:14:17 GMT  
		Size: 230.8 MB (230836793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:412f269ce90cec52a242c0f8d94d431530291bd22a2e945588d4de4638259cac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2250773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:699934ce3aa193ec6668bca1856cfd28299e2114382f9126e92f9e09b4cdd423`

```dockerfile
```

-	Layers:
	-	`sha256:97ee2a29ed9cfe34d0cda7e399c1cfb3c8a4b3640149069864a6ed705e14ae27`  
		Last Modified: Wed, 16 Apr 2025 16:14:12 GMT  
		Size: 2.2 MB (2241161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fba5f2271ec83d8e1099665ba16f72d40b632d2d23c03da4f64763a3e46c990`  
		Last Modified: Wed, 16 Apr 2025 16:14:12 GMT  
		Size: 9.6 KB (9612 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:761b708bd3db358216b04b1770ea7ed47cb4368bafa37f24f6d92fb65359881c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256063515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9910f6d991b11bbbda5de73e75834db26e03c07e3cd414465efd3277f1bc7534`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 07 Apr 2025 07:27:02 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:27:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:27:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:27:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:27:04 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Mon, 07 Apr 2025 07:27:05 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ac8b47e9b639aa1d57bded188ecf735181cab61b4998e7b9c2127e75480b94`  
		Last Modified: Wed, 16 Apr 2025 16:19:07 GMT  
		Size: 228.7 MB (228709284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4399a6ba43212e8f395c8cd4454af63d28a2f494b0d582bb3af4742260a90046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2250594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c3e88533229d17a6e1af4aca9fa6dff0d5f3688429cb5b1da69af4e2baf927`

```dockerfile
```

-	Layers:
	-	`sha256:b8d2c0072fd1b4a4c9e097632438274f9154b547c3743520bd77d94799a2ca8f`  
		Last Modified: Wed, 16 Apr 2025 16:19:03 GMT  
		Size: 2.2 MB (2240854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f60e2ac6f8281e5738ad37f70186fb0e85c1a26bfd58f5eaa7e7df660b704f86`  
		Last Modified: Wed, 16 Apr 2025 16:19:02 GMT  
		Size: 9.7 KB (9740 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c78b58aa3d037ffcadf00c2290e54e30ab48971513b0bf5b214343a97cb86cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266305410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f3daa34433cdb50f3932917292e23edb5cb58f3747e7e413901fbb7b0436662`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 07 Apr 2025 07:25:40 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:25:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:25:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:25:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:25:44 GMT
ADD file:b1634c9c9ee669b835ef39787fc71f78267fab0678a8e8c5547ba2339762e075 in / 
# Mon, 07 Apr 2025 07:25:45 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:220e8fedb927c1ecfafdf1e8cd0a85977de62e4afd95df2c5a27a70d3bdf34b0`  
		Last Modified: Mon, 07 Apr 2025 08:26:45 GMT  
		Size: 34.4 MB (34442696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0650944c196d4e4888efee0da857435d66e9ddfa41bbb8a1e139e4d1ee1f07df`  
		Last Modified: Wed, 16 Apr 2025 16:25:54 GMT  
		Size: 231.9 MB (231862714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:66ceaf6678ea877a18d90be6624b4ecccdd25d5470a98c676c4dae73bf9f7992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2252188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a9afb2877200677f3846d39d610ab486881978dc7ccd9330ff1cd7ebe37990`

```dockerfile
```

-	Layers:
	-	`sha256:8b9e9f8f5cceb48ccb5c6124dbdfc88bb2a6048e65fde1a66de5973d74ab227c`  
		Last Modified: Wed, 16 Apr 2025 16:25:41 GMT  
		Size: 2.2 MB (2242520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc5acd86855d79a33da7c77b8dc0792b087fcda27d5b88c24485169bfc069eed`  
		Last Modified: Wed, 16 Apr 2025 16:25:40 GMT  
		Size: 9.7 KB (9668 bytes)  
		MIME: application/vnd.in-toto+json
