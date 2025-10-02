## `sapmachine:21-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:2487c48d2a586f20acd65afe8f644028656793b487707b1b4eb4ca36641e9415
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:6db619d1235dd13df9c1198e7b55cc1b247d7483562a7273356e9075ade31c1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89361271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8b5b07a2eded43d6e28fe4724c9f15369864ddd34e8e899b3c93f5de7424826`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:32 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 11 Aug 2025 06:09:32 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:32 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea0da80cc5ef4058645b7fddcde70c2bf170b3f4fe06c5aaef2252af218b5ff`  
		Last Modified: Wed, 17 Sep 2025 17:38:58 GMT  
		Size: 59.8 MB (59824336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d577c0c4833928c0efce633daae700ad6bb705f826c9c82e00d1a7c96567f9b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8baa8baeba41689bbabc996d63256bdd0a046160e702e9952b89ae253e1d9b4d`

```dockerfile
```

-	Layers:
	-	`sha256:d21b632acf1b698493c1e77486a421fe88b28a6dd4a5b7327b724bd166685002`  
		Last Modified: Wed, 17 Sep 2025 21:09:01 GMT  
		Size: 2.5 MB (2544889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8583ba4ebcae44ff056e7700da9aef6d8cee9f95a264ac45cf86758e35bdfa80`  
		Last Modified: Wed, 17 Sep 2025 21:09:02 GMT  
		Size: 8.8 KB (8812 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:1608ce911b207e32b5fa6c716a59cf23fc29ea92ceef363728ed90ad4fc78eab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86328282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f825a544aa574d5100aab8df6ede3ca82c378cfc941917a41e9ba5c118d1d44d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:32 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 11 Aug 2025 06:09:32 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:32 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0755320e29e15c62cc3345748a364d1fc6ee278e19fdf09d617155edabaffca9`  
		Last Modified: Thu, 02 Oct 2025 01:34:58 GMT  
		Size: 58.9 MB (58945175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fee89f24e395ded477041e39050b4ec5f4394696eb9dd3fbcca0e8ad91d3d4a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc6e3d06de601262366e1bd9787d12d2697a29cba43959968063b1eeaee96412`

```dockerfile
```

-	Layers:
	-	`sha256:63033859cae409705e1ab0b4eea6f882081b6a809d940ddf49d8fc61b33e3e14`  
		Last Modified: Thu, 02 Oct 2025 03:08:32 GMT  
		Size: 2.5 MB (2544571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9079a6949edaa8874c4288be5f7c33cc81785ac7dd7e5017e242ae3f33342fca`  
		Last Modified: Thu, 02 Oct 2025 03:08:33 GMT  
		Size: 8.9 KB (8916 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:ec8f56bedd54069439c7d44a19daf7ef437aae9a98691aa10b49c06f35a58f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.4 MB (95384802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a3d3696e80ab596a7e48eb0e8468c6d7540e900be967ff46816daa9521c3c4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:32 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 11 Aug 2025 06:09:32 GMT
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:32 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d08625dd5b89b9ecbe59e8a61dd90b183b6486f5fc278fdd193a50eaf5ede52`  
		Last Modified: Wed, 17 Sep 2025 17:53:08 GMT  
		Size: 60.9 MB (60941578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4a1694ac0e55eeab416c7f16f6a5dbd803e3dd10c64e6bc5cf6bdb4895c121e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2551860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7022555984102887842025bbb4edc2e4f452cd2389d60c98f84b8c51104cd046`

```dockerfile
```

-	Layers:
	-	`sha256:e0c313a1a360ccc540d49589792042f121d43c4a4263b45f026b9bc2d66670ea`  
		Last Modified: Wed, 17 Sep 2025 21:09:10 GMT  
		Size: 2.5 MB (2543004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1af943839a7312a9c01ea293332ed7335b0e2a56bc066e511e152d1e733de344`  
		Last Modified: Wed, 17 Sep 2025 21:09:12 GMT  
		Size: 8.9 KB (8856 bytes)  
		MIME: application/vnd.in-toto+json
