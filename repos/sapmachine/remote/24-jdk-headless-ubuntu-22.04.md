## `sapmachine:24-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:23a6d2c67ec6f8fd8752e483656548b27d0aa7e54e95e1045051c8543807fd95
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:d85d1ff483c43a5a10f3e9198a2cdc9d4c86af0d34963e553058ed0d144424e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.4 MB (260369678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4208dada1551b58157753779fad831496a2d32fbff8e92631ce10ec9a7e541c3`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caec4d2a3f17d428e234dc662c84b592dbb2c2295fa9235a84965af6fea6c7d9`  
		Last Modified: Mon, 05 May 2025 16:37:03 GMT  
		Size: 230.8 MB (230837064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4deb05ff56f756c704e899978a543df1664009cf13f9b89bf6fd794d983ffc45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2250773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f533192b89ecfa9c54e09b8360290e164f3922b9f8a032ad21708fe92e92504`

```dockerfile
```

-	Layers:
	-	`sha256:0455e367d2966414fdbb9f807080c090bc3370aef258bc16b04758af2974161e`  
		Last Modified: Mon, 05 May 2025 16:36:59 GMT  
		Size: 2.2 MB (2241161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aef1409cb5051de2f80a0085ee50432549ac7b9990a7a538782e5f79595d61f`  
		Last Modified: Mon, 05 May 2025 16:36:59 GMT  
		Size: 9.6 KB (9612 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

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

### `sapmachine:24-jdk-headless-ubuntu-22.04` - unknown; unknown

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

### `sapmachine:24-jdk-headless-ubuntu-22.04` - linux; ppc64le

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

### `sapmachine:24-jdk-headless-ubuntu-22.04` - unknown; unknown

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
