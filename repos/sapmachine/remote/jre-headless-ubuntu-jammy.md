## `sapmachine:jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:0090d3660eede9fc4f5e84f6bf8794a105458e46159b1535d11274f449e59b4f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:426c69bdf8add3eb23f741fbf93f0e9c81b6d7648a4d6e94162cdb91477cb10a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (96015159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd373d764cff633678bedf2efda75314531e52c234002254063181b0655ea9e2`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:20 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:20 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f1829b3a30d683dfc3c675b2c99df8d8762c8c3ef5565298b97b6643bf5dfd`  
		Last Modified: Tue, 02 Sep 2025 00:28:46 GMT  
		Size: 66.5 MB (66478224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6bc0ae8e5c4e52a209e72e7399f6903953700d515f1f283425ee72017d437145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e27d69f8241d45057d386c25368c4ce2508a959bff91ded87805a0f4912a7e0`

```dockerfile
```

-	Layers:
	-	`sha256:3ca8a6b3e81a2777090f990842263ee9a71cd7753f8b88455fa6dec99ac0444d`  
		Last Modified: Tue, 02 Sep 2025 03:09:49 GMT  
		Size: 2.3 MB (2301849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd0c8c912cb426f5288525ff93ccbeb282c34874dae5b883cad8a0ef9fc883a8`  
		Last Modified: Tue, 02 Sep 2025 03:09:50 GMT  
		Size: 9.6 KB (9610 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:37476c92c0382908389688aaed7b0cc03d2d1b9308788dee9cd05f1f67f0e482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92843452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf4a551be4be33b7c48b10fa4fd37f184388e23f4f6f9be424e8423b2864e28`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:20 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:20 GMT
ADD file:b045ee8ca1dc1b3294d6328d500a5ec30fb4bcdea1a91177f0280497c391ce2b in / 
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:12988d4e65587a5bf2d724b19602de581247805c1ae6298b95f29cef57aabbed`  
		Last Modified: Wed, 30 Jul 2025 09:58:44 GMT  
		Size: 27.4 MB (27359247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f88270af846dcdfca23b39a7b9809661d7217efed005663d327e03d793998d0`  
		Last Modified: Tue, 12 Aug 2025 21:19:11 GMT  
		Size: 65.5 MB (65484205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f9afc55269bb927415b9eb253743860c18f0ce6a84dd25096aad43f68f8f4dde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c06104dd9644c276bb6e0ad144f13a782c496364cd15ad829aa468bad31e05e`

```dockerfile
```

-	Layers:
	-	`sha256:c43564985607b99abd4556f1889db53f7f0df131308455a4a79c336ade544583`  
		Last Modified: Wed, 13 Aug 2025 00:09:40 GMT  
		Size: 2.3 MB (2301526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62e87e3903e337b1aa5bbfa0b93cbdc6efffcd26a0de68b2b50df5cd870f1961`  
		Last Modified: Wed, 13 Aug 2025 00:09:41 GMT  
		Size: 9.7 KB (9739 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:135a35a6dd21226cd8acc18953e9527e67c20b1c142cb3dca7af7b34ec7876a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 MB (101566467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c773c7c41157ea59d8ab06839566f068e7dfe80cc38abe256fc18d643472a5ce`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:20 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 15 Jul 2025 19:58:20 GMT
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df698a9655394a84212f405d13d378c9a4dccd44722c1924425056e255bf665c`  
		Last Modified: Tue, 02 Sep 2025 01:59:51 GMT  
		Size: 67.1 MB (67123243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8f54ab37c14fb9b84251c1d2a602cedcbd671dc1ad9f28a1aa8ff31c7c2d8b0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c805ae654150aec02a0a6ea990c9ba0dac39b221eef505e27772ffbe42011b97`

```dockerfile
```

-	Layers:
	-	`sha256:2dd07a442025d3987e51cc010e0da2c44418d5aaf03b80b37e29b74c5028ecb5`  
		Last Modified: Tue, 02 Sep 2025 03:09:58 GMT  
		Size: 2.3 MB (2299256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6dadf7997623bef50ff1ebb95b3fc4b359a2fe91a9b941871250daf440a99e6`  
		Last Modified: Tue, 02 Sep 2025 03:09:58 GMT  
		Size: 9.7 KB (9667 bytes)  
		MIME: application/vnd.in-toto+json
