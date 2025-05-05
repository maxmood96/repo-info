## `sapmachine:21-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:3055ffeeb759f092ad8f8f38111ec4e78e44a344dee4c857b339831119861f8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:b0d77181180c6ed6334d867cc87351ce1d378d368acefdb5496ca8b915c78fb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.0 MB (88045667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cae2b6fc560d71d28f73ad6cd30805e367733086e414b0cc20f0f08f41a5f7d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5cd6e96b90d06405dd77a6dea3f4e3080f0f0b22fa18313842aa6b20069da4`  
		Last Modified: Mon, 05 May 2025 16:36:58 GMT  
		Size: 58.5 MB (58513053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:74e1dd89e0ad92e15880b5399a9e9bc39fb833beb01d277c6fe5b23657a1158a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2ffff5799ea30bf8fdbb6f70e6adc19cea3192bfb015e0e940d136069649e5`

```dockerfile
```

-	Layers:
	-	`sha256:91b6ced9b0acd46486aa174bf377b3133b1a2b3b7c9cdb4866e670825911350c`  
		Last Modified: Mon, 05 May 2025 16:36:57 GMT  
		Size: 2.2 MB (2166930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcdb1334970b8f5f9df09e87896fbf2e79053ebcb34dd0142a3d430105777351`  
		Last Modified: Mon, 05 May 2025 16:36:57 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:5ca0085d70108efa52c5cc77f2a239de883798b81336744b10632a5593e24cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85010632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd715c6581016d7b10cce549cd2b74085fa27635aebf3816e0d1bd00b874d900`
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
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c533153d8d349041299ddd694eb393677af0c4d3f7459b0a36689396daafdd`  
		Last Modified: Wed, 16 Apr 2025 16:32:03 GMT  
		Size: 57.7 MB (57656401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:983ba5ff0d816dd3650273f5a3c764488d82d4685e0911895d46532d134cc13a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2176381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e3912068543cc82837a1eeb4bdb9fc01ce4316e5ffbb973e8e6e71996293e30`

```dockerfile
```

-	Layers:
	-	`sha256:10597e7c314aa5fc3a98ee7019ce94f8a52e3cfa25489cc55692bffb130d768e`  
		Last Modified: Wed, 16 Apr 2025 16:32:01 GMT  
		Size: 2.2 MB (2166626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10c983516d9a4def2a3582314f997a44127986fff67370a584edef74833295b9`  
		Last Modified: Wed, 16 Apr 2025 16:32:01 GMT  
		Size: 9.8 KB (9755 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:54758853f2b05ddf33c06cb7b4fe1551b954e298d3ba728d082041f551094257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94353078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:115fe7077a5b6634e8d1f284d4ffd32e6b7a3313b3dae65cae59386475ff1bb0`
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
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:220e8fedb927c1ecfafdf1e8cd0a85977de62e4afd95df2c5a27a70d3bdf34b0`  
		Last Modified: Mon, 07 Apr 2025 08:26:45 GMT  
		Size: 34.4 MB (34442696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755d3498bee22bbeb0003201dee7bf5f306adba624ecad10001f80098bb2f5c6`  
		Last Modified: Wed, 16 Apr 2025 16:52:56 GMT  
		Size: 59.9 MB (59910382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a054cc45a9d4223896eff8361bb58318f808fb25e293f4a83bc9297b1a6670eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2180536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28bc8124385ea269c7ce08284e96bb76a5d1d0eafecf416383cc4699282189c9`

```dockerfile
```

-	Layers:
	-	`sha256:3f5da81ac468e7d4de64b442a800f6e4013c2e5e56991093b593d1ced2df8d23`  
		Last Modified: Wed, 16 Apr 2025 16:52:54 GMT  
		Size: 2.2 MB (2170853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:008323e59630dda21044fc45a8436f8732cfc60ce1a39178828ba6b5131cd679`  
		Last Modified: Wed, 16 Apr 2025 16:52:54 GMT  
		Size: 9.7 KB (9683 bytes)  
		MIME: application/vnd.in-toto+json
