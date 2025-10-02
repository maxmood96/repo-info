## `sapmachine:25-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:e401100809a631bf19590c65a845659ecf0ce5678482dde3f5a496141395c02d
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
$ docker pull sapmachine@sha256:9ca2791185ccbd8f5b90e429425b136181475275000cbfa2e812b930994289a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93690791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6dc9b9b4717524704ce091eff68b8aa4d67ecbc84e173cbc64c6fec8f4d7e73`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Sep 2025 04:28:56 GMT
ARG RELEASE
# Wed, 17 Sep 2025 04:28:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Sep 2025 04:28:56 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac5d256bf47c87053d6576a135fbf98ff0db6866564ba7031f546c9f4d31b7c`  
		Last Modified: Thu, 02 Oct 2025 01:34:04 GMT  
		Size: 66.3 MB (66307684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d8203cd365fce30ed255a244e2e0963f67b6dddcd2a38ab2ae9b37ab8ca44f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfae456b2a9a5b272c786f2d0f83c7939f558075e46f16eaaf7875ea5776da06`

```dockerfile
```

-	Layers:
	-	`sha256:df2979427e2479674aabd384c7c2aadefc79360efcb55bd4bbd1e823a0cc7c52`  
		Last Modified: Thu, 02 Oct 2025 03:11:00 GMT  
		Size: 2.3 MB (2301538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf2ea04023fb1a777204564fc1f428f46e97baceedae46f652bb2c8f322b2bdc`  
		Last Modified: Thu, 02 Oct 2025 03:11:01 GMT  
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
