## `sapmachine:25-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:a25761cc6f6d3831a491cbd2a082479b9898da34b6493fe3ddb6eed0528a4a05
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:25-jre-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:5cb470eb89bfb7084e6433498de0537c37801689b850775e16c3b050529aa784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96905155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49a411544b951ed55eab853ecfd3d80ef03cbf94e49f2af22869221dffbd9b0e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0599fd5d837fadec6b7009a25dd381746c11631789e41544f9de194e174bd183`  
		Last Modified: Wed, 17 Sep 2025 17:36:49 GMT  
		Size: 67.4 MB (67368220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5dc3f3ffa38d7c0f1c3eb0c3a41fa015377f7bc59612052f88ba87dbc1b9572a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3c975c71f63608c96f8b8012c2b40da4b9c9a2cf1e1bb525af1590f2e01bec`

```dockerfile
```

-	Layers:
	-	`sha256:5c4ceeec28ae8d13dc5f2ba1afe393d1ba47e9b4d23afde7e0bdde9a120fbd22`  
		Last Modified: Wed, 17 Sep 2025 21:11:56 GMT  
		Size: 2.3 MB (2301845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6a35d480a8b1282ac0c4aade789e5eaad16a670f65922e07daee95e2d053c3b`  
		Last Modified: Wed, 17 Sep 2025 21:11:56 GMT  
		Size: 9.6 KB (9587 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jre-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:30265a62df034b1c1d2285ae6711297db6470bf7f4dcce52f3afc80f202b0098
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93669200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc201c8455bb6fab14c63c48c659efca9896f00fe0139687bee0505e5e1520f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfacc7ec871629fb863d5e0e9d6f845af01f8a331982fa2d132063b637f4683`  
		Last Modified: Wed, 17 Sep 2025 17:40:55 GMT  
		Size: 66.3 MB (66307731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ff2aad6a24850d29a00cc30a0e4864f4c6f9f7db72692a67acbfeddc7d29d1a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a47a7d704a153a24f41cf9e5c8995cbfa225e296efe0b17dc23fced978a8ab`

```dockerfile
```

-	Layers:
	-	`sha256:a3fd2f04ff276eb03a9aa775ad9e5dd2be33b97391a931b97cc85f8f359d1336`  
		Last Modified: Wed, 17 Sep 2025 21:12:01 GMT  
		Size: 2.3 MB (2301538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b77a20ad234108d029b5be767c895f780e5dd00e55e50db20ea186bd6b3ed84`  
		Last Modified: Wed, 17 Sep 2025 21:12:02 GMT  
		Size: 9.7 KB (9715 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jre-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:7934f8b3c1461da40b2d38fab68127b1a779a759c83e7bce395073acd5d932fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102465568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeda0962f06dbdd08b610ed21af873b9d6eb772dcb6713e151af6506f68578f7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:45 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:46 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:49 GMT
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
# Tue, 19 Aug 2025 17:21:50 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23c3bdc5f6e265fcc27cc2a0b8db3828ff898c37cbc8ae6c7c12c674e99cf76`  
		Last Modified: Wed, 17 Sep 2025 17:50:39 GMT  
		Size: 68.0 MB (68022344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:618cd8735ede6a50e4743fd523ac3a53d3d2e8dd6ec41123c5cd01ccaf0549c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4612f759afcfacde569831f3b860bf0996a8ec3601c00dbe2a8646e8a3f500d`

```dockerfile
```

-	Layers:
	-	`sha256:1a8bde4853fa88b4974aeedf88bf5efed60d5edcfb33be2e8a072886dbc95a55`  
		Last Modified: Wed, 17 Sep 2025 21:12:05 GMT  
		Size: 2.3 MB (2299252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae3b72367d9eb4476a9f9e9a196d13c96902dcfd03cb8d3fac42fb5c6f0d45cf`  
		Last Modified: Wed, 17 Sep 2025 21:12:07 GMT  
		Size: 9.6 KB (9643 bytes)  
		MIME: application/vnd.in-toto+json
