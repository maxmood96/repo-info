## `sapmachine:21-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:32b9aa0504b793fb98bfc3f6e983776c4fbd7a382e4d93270dfb0be0b3c13f29
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
$ docker pull sapmachine@sha256:d21960c76c4bb68fa5625d8bf820fe37ced66d7f84dd13ac53f572cb6cbb632a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90080868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb4f5f851749b94c37556510b76b9f09c27a740fdeb26ca1b7e30b2602fb49e`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:16:44 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:16:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 01 Apr 2026 20:16:44 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb7e9da8c6584eb6f22b7639972d6c013ffd011765647a7933a298817edaea7`  
		Last Modified: Wed, 01 Apr 2026 20:16:57 GMT  
		Size: 60.3 MB (60344455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ac7badb03bcfca3458af44360d188ce985d12f37e8ad3f8151a7b37d561d33b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2556115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af560dda46d6cd6207ae66747c43a48e1a8d74042a69c4f63015cc84c1639f28`

```dockerfile
```

-	Layers:
	-	`sha256:11739b80a34fdc7a8ead7c994836036806ecfbdef2dd87b964c11703b9c08b2e`  
		Last Modified: Wed, 01 Apr 2026 20:16:56 GMT  
		Size: 2.5 MB (2547317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96dfa7acf3e80a49dc9f360de9d5fe633f5dce68b4688d5515e2f58ea5466b00`  
		Last Modified: Wed, 01 Apr 2026 20:16:56 GMT  
		Size: 8.8 KB (8798 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:4ac3fae7a92a9fd41ca8e8841315e20d1cb695a632677c65af9cb700ef79f32c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87104693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2be213f9328c287fe7dc6b1308cdbd836cf5d8460d2e35f91332c2723393e41`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:16:18 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:16:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 01 Apr 2026 20:16:18 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f059d539975a90fd3d02104b763c6a6795a2a54daaefef020514efbe4e052fd`  
		Last Modified: Wed, 01 Apr 2026 20:16:32 GMT  
		Size: 59.5 MB (59497750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:17cf2686a13a845fea3705c635d440822a01dfa9f98eff80381312365babc690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2555901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ab6e40b7b75d0231c7674c14b2f4ec29f092ff875baebf5894ddd1cb22ba768`

```dockerfile
```

-	Layers:
	-	`sha256:1e81eb198daabcd129c808af819660ba38aa6418b7b2cec199b63c11bbee67d0`  
		Last Modified: Wed, 01 Apr 2026 20:16:30 GMT  
		Size: 2.5 MB (2546999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fea7d630f6d46c01787d33c838d85a1dde9fb19a31b29db3167a208485625f9`  
		Last Modified: Wed, 01 Apr 2026 20:16:30 GMT  
		Size: 8.9 KB (8902 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:13918d483bb61145ad0b77094feed44cb4135218f1eb6f29e64721963aa3d5f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96220915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1598712952c7efe8fb2f5ddfb1c5d4d2080d6a1ad657bce30698f63a5f82103`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:11:34 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:11:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:11:34 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:11:37 GMT
ADD file:268be611d24f69c3d8e480314cd587652e4c89a6032236737057c8b64f2379da in / 
# Sun, 22 Mar 2026 18:11:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:49:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:49:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 01 Apr 2026 20:49:13 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b42f0db0a1bf72bf3e885b9a10438f55d6a5339b4a048022d05e845d4a76ef`  
		Last Modified: Wed, 01 Apr 2026 20:49:40 GMT  
		Size: 61.6 MB (61571255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9c0056f2301219e123b12fbaaf3cd5dfcaab2ef14e0e08cbcdd7b398c9f9469e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2555690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6071d96ce6a991b7c50571e999dc09cb5a0f3a1609db4b2eb02b9c866739fb6`

```dockerfile
```

-	Layers:
	-	`sha256:9c3073586a2aab7c343655810141097596222c768634d07441e0c9db3913d2bb`  
		Last Modified: Wed, 01 Apr 2026 20:49:37 GMT  
		Size: 2.5 MB (2546849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:470b94923bd3c8b094bfb8f49ee4cca12f63eb7e735ccb0a6757ab5387c1290e`  
		Last Modified: Wed, 01 Apr 2026 20:49:37 GMT  
		Size: 8.8 KB (8841 bytes)  
		MIME: application/vnd.in-toto+json
