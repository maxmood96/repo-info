## `sapmachine:17-jre`

```console
$ docker pull sapmachine@sha256:aa437a2ecf7528d8afd5bd0c5577e496a5d85231349476f6e635fd15f381f430
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre` - linux; amd64

```console
$ docker pull sapmachine@sha256:4f6d7b17686a5366d4ec94212f9d17400bf49645676cbde8072fe76fd46aade8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84503513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9fc2505c2023625ff04a7ff3c0ecc7a293a43bc2b7ce67b2d9af96cd29098a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:59:51 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:59:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 15 Apr 2026 20:59:51 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294cce58cee18fcc78243bf580a4ba26e1cbaa6f2fde65d8edfc3783c20ce0ac`  
		Last Modified: Wed, 15 Apr 2026 21:00:09 GMT  
		Size: 54.8 MB (54770535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a54782abe63bd3bb598863af45844f5e9b54b5efce381b7a1ad13f223477c058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2529848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:484e6d79a8bebd63527d85d165a948c331cf002938a6bbc1cb7679191fa6c116`

```dockerfile
```

-	Layers:
	-	`sha256:80a3d330a5dffeb0326b67e23afe3a9fa93860c217dd77f5c057b793e56f5fef`  
		Last Modified: Wed, 15 Apr 2026 21:00:08 GMT  
		Size: 2.5 MB (2519802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bcd9135507e329762affc2a3c79b7e96a132157fd4ea232778c266c3a38d5cf`  
		Last Modified: Wed, 15 Apr 2026 21:00:08 GMT  
		Size: 10.0 KB (10046 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:0976e561f0cb27a209d9e984ad8d78e80f2238df3f22b6736fa263b74e69748c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83078207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09ab229b9bf79fe0eab66f9e9781c088435318bfe41a74c356b5814711a22734`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:10:26 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:10:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 15 Apr 2026 21:10:26 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9312d826f565547118266e45065d7ba2cb2461418bee6dd3756cb0dffd2d2a7`  
		Last Modified: Wed, 15 Apr 2026 21:10:40 GMT  
		Size: 54.2 MB (54202422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre` - unknown; unknown

```console
$ docker pull sapmachine@sha256:684480d9c625a3a21c7f750f52e5c6e51de2fc1f6f95df273641c896e80f16bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2530516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7753d504634745b8c7ed61c0707bf83fc70816d69712dd2d6d1c3795e1546d32`

```dockerfile
```

-	Layers:
	-	`sha256:fd93030fea5afa11e41cbb0e606605a76a7dbb471bc808de01d8e7b023e52210`  
		Last Modified: Wed, 15 Apr 2026 21:10:38 GMT  
		Size: 2.5 MB (2520318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3376c85c1984436a96f8b68f0aa2632ab60427c13f15c0aeaf5148a584f5962b`  
		Last Modified: Wed, 15 Apr 2026 21:10:38 GMT  
		Size: 10.2 KB (10198 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:e71d0d3d76d86bd0269eda6185466e27f0d7029ef92b74c03fa8bac1e0073e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.4 MB (90356393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5407fe128fc92c2679936bdafe627c0355628a294a061077153f2aad400cb83`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:25 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:26 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:29 GMT
ADD file:ede7e3b047d459e8abfd20afae677192c0eab70c709496e87b2110289bfb5f3c in / 
# Fri, 03 Apr 2026 15:15:29 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 09:11:30 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 09:11:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 07 Apr 2026 09:11:30 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2206a81f65df3147f8c62d4c01c47495515dae16f93ce6845cd7cdacdd206f1e`  
		Last Modified: Fri, 03 Apr 2026 15:56:51 GMT  
		Size: 34.3 MB (34313334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37c39d59f5a5635c5765b7026763eb8f2645bcee117321f66fddd228aeb0fc5`  
		Last Modified: Tue, 07 Apr 2026 09:12:05 GMT  
		Size: 56.0 MB (56043059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e6028c749b2ad3a463705f8463fda460e84e48209101e515c21b92568c17bbb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2529414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6115c9d9bd5260b788f7759256a0b91dd1981a0dc7a4f1ee2f4808450297d92a`

```dockerfile
```

-	Layers:
	-	`sha256:480954c9d26bbd1817dd16b8271ec28a97aca56089c3ecf107f7e71740ec13b0`  
		Last Modified: Tue, 07 Apr 2026 09:12:04 GMT  
		Size: 2.5 MB (2519300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b20c335b0057239b1eb597d79645d26eb95dc6af85bea5bb6786444ea16cc6b`  
		Last Modified: Tue, 07 Apr 2026 09:12:03 GMT  
		Size: 10.1 KB (10114 bytes)  
		MIME: application/vnd.in-toto+json
