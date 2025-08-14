## `sapmachine:24-jre`

```console
$ docker pull sapmachine@sha256:8a68df62ca2f679cd0bd8434d2baf3d43aa8083497ec0a73cab8a9d53694e978
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-jre` - linux; amd64

```console
$ docker pull sapmachine@sha256:62bc070e34603a2a596c3697efee159d3e49e48ca54c3a22d3041a1fe4f5fa39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.8 MB (97815316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f269ed4d5543f878f790af76d502b55b24edc1d5f219383a07c27ba916122b7`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:20 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:20 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d2d611ec06690a9d84c3ea022f14f94d0728667fe73e1b23f3ec6aa95505c7`  
		Last Modified: Tue, 12 Aug 2025 18:04:59 GMT  
		Size: 68.1 MB (68092101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre` - unknown; unknown

```console
$ docker pull sapmachine@sha256:99f0f86cd912eabb1722879a5c2db667d7395052c79cbd7d811c20924a81c67d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2538291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8e176e29443d710cf97b64c072240a58d563d5569c237c97bf5b39763da8fcc`

```dockerfile
```

-	Layers:
	-	`sha256:7e60eb4a05adc5322d07cdca2a82d58caf54cc1755321e10a11d9408b0905bbc`  
		Last Modified: Tue, 12 Aug 2025 18:08:05 GMT  
		Size: 2.5 MB (2526946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8810873394456632046e2009dad6752ba05eee8156d39acaefcf104ee4afda9`  
		Last Modified: Tue, 12 Aug 2025 18:08:06 GMT  
		Size: 11.3 KB (11345 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jre` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:31b9dc939b0ecc0e20dd163d01bf7a946aca2a6892186825152915e3eb755919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95994254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ffa950a8f63a9bf304a7a30275f0d31aeb49b4d52b134024267a5a3459b1e9`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:20 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:20 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d545ab2e17ca906a8755577701c99448d01bc0df95e6d6a61b6fa5e66bf6d043`  
		Last Modified: Tue, 12 Aug 2025 21:14:04 GMT  
		Size: 67.1 MB (67133877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre` - unknown; unknown

```console
$ docker pull sapmachine@sha256:adb515dd959e45dad4ff5dedf0853aee5d76d30ea588e4d0093eddeb5816fbda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2539053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b609ae1472b465c388f7723979d62fe0a6a25fd3f229798001d5d39fa9706616`

```dockerfile
```

-	Layers:
	-	`sha256:77920c88463580e9877eb93f39869e971b68c03dfed7d122d41c8dab68c16736`  
		Last Modified: Wed, 13 Aug 2025 00:09:26 GMT  
		Size: 2.5 MB (2527507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2e73e08a4b36b183d4362be678cc9f108f60a92d0be65a09a339ffc3e5fc052`  
		Last Modified: Wed, 13 Aug 2025 00:09:27 GMT  
		Size: 11.5 KB (11546 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jre` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:9f98191f57aebebc2a019a7fef66347d35053ad48aebe7f7ea01517d4af604b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.3 MB (103345372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95c14dd7a4a8f249364d669ef91cabdbe3ea2a7d7febe667b581d2c97877ab55`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:20 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:20 GMT
ADD file:e2ae399c3aa36bf07b7d3562a21b9ad89f66ae6e03733ed0edcdcda5bd391c60 in / 
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:403b01240f845337685ead3abfb0228bb1d1b78b076d609aa20f4733d260f58f`  
		Last Modified: Wed, 30 Jul 2025 11:30:48 GMT  
		Size: 34.3 MB (34329650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596b018efe98522c768bb0a99f3eedcdb66504e75ce239015c4f40da677311e4`  
		Last Modified: Tue, 12 Aug 2025 22:26:21 GMT  
		Size: 69.0 MB (69015722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fd40f7f148676b426d4547129c6ab0381b8d4696af077c26f94bcf7a2fa66925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2535859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85eeefb74d734a992dc2cbc357f2aecff2a6e3cb5bf74ee5a9ad683e24f49dbc`

```dockerfile
```

-	Layers:
	-	`sha256:ae9c6fdea9dc95c0ea334e2dfb0b4f9939bab5777e64603b82954c854b9f8580`  
		Last Modified: Wed, 13 Aug 2025 00:09:32 GMT  
		Size: 2.5 MB (2524421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f116b7c4b4ebb924449d812e8f0e05535c89895f33d8835b0872bfefceed460e`  
		Last Modified: Wed, 13 Aug 2025 00:09:32 GMT  
		Size: 11.4 KB (11438 bytes)  
		MIME: application/vnd.in-toto+json
