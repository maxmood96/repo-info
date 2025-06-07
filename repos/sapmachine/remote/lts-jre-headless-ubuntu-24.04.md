## `sapmachine:lts-jre-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:2b0817edc16d420cc526130e1dcf3b0ce56ec23694c708bd25f898b7255b8b74
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:13cbe86177d26240eb3fb1e0c9ccdbc812203e4296c7a9f04bb71ede598de009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88648702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ac9207f3c57f23a647df9bcc410d7194b4b7ab26d02fe30a5479ca4be0268a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
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
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c0e548c1069442f05f321f03b191edcdfd790df2394ef9d65b155361182018`  
		Last Modified: Tue, 03 Jun 2025 14:45:56 GMT  
		Size: 58.9 MB (58933365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f8db465ee4313a4b01518bfa2f1ec412c652260a27cac45bcf96ddc58b98474e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2182883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fffeceab40bb054d348312a5fbbbb230e5cd187e36e3140601da5627da8ee2b9`

```dockerfile
```

-	Layers:
	-	`sha256:83a487056ca1636681dfa06fb4ef849db3db9531535102ced83eaf6afbcd04b8`  
		Last Modified: Tue, 03 Jun 2025 04:17:35 GMT  
		Size: 2.2 MB (2172232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30f938e0229f9ccee59a64287b354cb1ec65074e24e2c6cb05279dfa993d28ff`  
		Last Modified: Tue, 03 Jun 2025 04:17:35 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:2377058a1c82c3ca887189d0ad2f56e7f12f69cdf53b3656f9cc4481b3b41787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86968244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e702096391a31d56cb4c8f6005ba56ef81600d06ddfd50434cf8ecadef51923`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
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
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Tue, 03 Jun 2025 13:30:25 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b33e9bf4f386ecdfebfc3db4a7dd1176d41cab2c99ebc5d0393a494e9c1494`  
		Last Modified: Sat, 07 Jun 2025 16:10:58 GMT  
		Size: 58.1 MB (58116345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a9959808b6c1cb4a2f5a61b529c05f4c14e8a5f66d4e7a11b0e5cdf5aa380804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2183566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb069b4b856a8f8554830dd18b1c8ebb45d19ccaa3a4e12dd00bbd9ea4c6672`

```dockerfile
```

-	Layers:
	-	`sha256:846801ccfa885b2401e26233f775b19681f1a404620b7bca2ffe366820c9f16b`  
		Last Modified: Tue, 03 Jun 2025 06:02:33 GMT  
		Size: 2.2 MB (2172751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:019e1f6b2dd4e45b21ab1276f36afc67420bc8c5c0d6c0d4767e83ea50251265`  
		Last Modified: Tue, 03 Jun 2025 06:02:33 GMT  
		Size: 10.8 KB (10815 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b637c09be1a7cbe5dd60e20f75fc2de4cffdc07151d2297585bb808ef60f405a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94747454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88aab0c7c095748b3fbef6c89fdac5a4cd2ec401abf2971da3c6fd236ad27df0`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:5b5c63079c35f826dfba60892de9b0b4108ed6547a12101193a481b991b1add9 in / 
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
	-	`sha256:9f6c4197b204ad8fd01f03e4a049c781a2075478303fbfa660f581b019365dab`  
		Last Modified: Tue, 03 Jun 2025 13:31:13 GMT  
		Size: 34.3 MB (34325210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344166601ed12b6d14bb29c8b2f9a3b585119d025bc6ebc7c040aa33ced9580a`  
		Last Modified: Tue, 03 Jun 2025 06:03:48 GMT  
		Size: 60.4 MB (60422244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f097bc89e80caa2bebf36e82cd413240e6dbb98bb4efd28228f01fd6c13831b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c64a6d4da034a620b4d363db98de7febb0e0209c9f579630428f7298386630a2`

```dockerfile
```

-	Layers:
	-	`sha256:3c65614ee0a8799c2dce246c795757fb96a314e3ce770a109b8b7c1ca4a2b867`  
		Last Modified: Tue, 03 Jun 2025 06:03:46 GMT  
		Size: 2.2 MB (2176254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f2d6f7a6e274df15814ff90312d23b4b029747116188c30c0df366959f0afcc`  
		Last Modified: Tue, 03 Jun 2025 06:03:45 GMT  
		Size: 10.7 KB (10725 bytes)  
		MIME: application/vnd.in-toto+json
