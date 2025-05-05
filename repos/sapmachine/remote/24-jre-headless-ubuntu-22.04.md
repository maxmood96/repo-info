## `sapmachine:24-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:e1ca1493c678d76fd6dc768149a7cb1122481c3df6a8bbcef9aa449fb1f6125f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-jre-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:c04feca7d88c43b0ada97162bb051791babef18e0385ba8446cbdde2e39a7ba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (96000678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74291cddb034ac29f1957224cc828a895819b5f4c895ec44c1e2800dd6cd7dfe`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:85cf0825f365ad7bca0f2e5054febdf5ff35af93bc58221548eeb09d4e75d526`  
		Last Modified: Mon, 05 May 2025 16:36:47 GMT  
		Size: 66.5 MB (66468064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:870200250355c074109ef4c480f043f91c84e3a76a18d0b708cf538a51356f6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2183576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f5e050789f6f06cfcf76ba21f2a3de9acdc24a660ede750c831e8497e26caed`

```dockerfile
```

-	Layers:
	-	`sha256:24acea9594ea57e8250cb660dd394eb30bcdeff6e4ab4a82ba14330b9131f822`  
		Last Modified: Mon, 05 May 2025 16:36:46 GMT  
		Size: 2.2 MB (2173966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:145df2639e47e560590e6cdaf44c71633af22a2b6b86b5f3b95c5519777a3fd3`  
		Last Modified: Mon, 05 May 2025 16:36:46 GMT  
		Size: 9.6 KB (9610 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jre-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:6c530fb3d053e29ad2d22b1e1bedcaf156051337ef5dbd9b1f10a284998bd966
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92810280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075cc1b7e460675961f16c96108c5ecc758cc332f950dbb8bfedc7dbae8d1844`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:da3e216a5631938b3c5a3db2b5b226064646ee7e9e98ec72e6861117401f2e6b`  
		Last Modified: Wed, 16 Apr 2025 16:20:40 GMT  
		Size: 65.5 MB (65456049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fe107852bc7f1f13e56dc6bf4fc1053ab27c4a1986a2b7cceed39d9de3630c29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2183398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f01da504b83035b802ca3b69805c7c1e336557e954ab4f2cbbff104c52147f`

```dockerfile
```

-	Layers:
	-	`sha256:ff30126568f5e7bb13493d0207b507a97005f1e4f68ad7e4e5171a93aa72a16d`  
		Last Modified: Wed, 16 Apr 2025 16:20:36 GMT  
		Size: 2.2 MB (2173659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d778108d59da115f94c8e7066a183f112033ce0c09641dbb7b07d71de245831`  
		Last Modified: Wed, 16 Apr 2025 16:20:35 GMT  
		Size: 9.7 KB (9739 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jre-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:1606dd3213b3356e23d4199f9a3dd1178e68c4d5837183298e0110a5406dcda5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101998133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a679eb51efa31bc8b244eb3bda1c9ee668d05af9eff3850023dc59aaaa1744`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:2251f741ca14e4ec33afbc6b5fad77f20dd215b352c4b95be8e645e388d2a535`  
		Last Modified: Wed, 16 Apr 2025 16:29:32 GMT  
		Size: 67.6 MB (67555437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3ed1caeaae0c8b60386f68dd9bab4ea6bc1a90752375d49f29164ffb62161c30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace9191dbf05786db7aad8ff0b3ad88e19f0b2b80b5466ebe9cf9b29d84a0dba`

```dockerfile
```

-	Layers:
	-	`sha256:2e2df6a39c31a2960c87a757bff959a7b3e09e6dff5b5243aedaebe74811823f`  
		Last Modified: Wed, 16 Apr 2025 16:29:29 GMT  
		Size: 2.2 MB (2177259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8355133c7c6eb1ad835989b2c6f8f73654e3d6a0718afa1a396d047a25074d72`  
		Last Modified: Wed, 16 Apr 2025 16:29:29 GMT  
		Size: 9.7 KB (9667 bytes)  
		MIME: application/vnd.in-toto+json
