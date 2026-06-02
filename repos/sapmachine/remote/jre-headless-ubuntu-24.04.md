## `sapmachine:jre-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:cd672ea307f652bd475cf888b76d5e51db651677545106a1c6057dac2d1c5eec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:2bb44a3ababc9936830b4485eac1f00e79825073b2be7fd70596c2da98e2fbd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 MB (87557936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0c6057e1187912dcd8e3b248ad345af8886e41b45036c504df5b247f0eb8a59`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:23:30 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre-headless=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:23:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 02 Jun 2026 08:23:30 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28c84942487c8f2261f835acae694401dcc5efebe169f5688861d2d555f5728`  
		Last Modified: Tue, 02 Jun 2026 08:23:43 GMT  
		Size: 57.8 MB (57825131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5a3a24fc42abf9a735b265649118070590fc7bd6011f71a9be8a4902424cb66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2292030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:017a60a8684f6e7c052e18d363be3c0dbd895240ae6824149ecb9b0f1402e725`

```dockerfile
```

-	Layers:
	-	`sha256:141c826f5dae818037503d9bf4c80f501a03c2ff3a720058394ff535df187844`  
		Last Modified: Tue, 02 Jun 2026 08:23:42 GMT  
		Size: 2.3 MB (2280472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9267d2b5faaae1ddce1391c888b9dac44561c62a32cc0bff6be6971eb8330b60`  
		Last Modified: Tue, 02 Jun 2026 08:23:41 GMT  
		Size: 11.6 KB (11558 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:339623351681efa4742dae5c71a4993fd4ddbb229a19c6b4545d58c576fd681f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.7 MB (85707543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64955abf67211f97f45c25133bf966811063a51b28187cae1d23969564995fb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:23:35 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre-headless=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:23:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 02 Jun 2026 08:23:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2026153a61b26a1bfa4dd6ae8edc01da2da639bd13ee2bd1e5f6b98d190f85`  
		Last Modified: Tue, 02 Jun 2026 08:23:48 GMT  
		Size: 56.8 MB (56831137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e640a7cd71ce764ba3bf9b05d91f3ab39b0ade11b313b3245b631305203c0bca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2292782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4181408daefba9b05fd7bbaf27c1f2baacd155ac9580672254fce073d9b92a46`

```dockerfile
```

-	Layers:
	-	`sha256:4cb38518a660404989380a409bd4cb2d0bdc366e509048835b121f8e8f65e163`  
		Last Modified: Tue, 02 Jun 2026 08:23:46 GMT  
		Size: 2.3 MB (2281024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc3ef93c5664f1c43340637c18b4ce1f75a9a7b1f634185c166989a046c2aacd`  
		Last Modified: Tue, 02 Jun 2026 08:23:46 GMT  
		Size: 11.8 KB (11758 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:3aa29fad7121645e922d228cd990b852d3d249c48063cd846b8fdddad02cfc10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93105642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c6f062a522f4dea65867b9e53a7427997a6e3773569de086f2a57d08ba5677`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:52:36 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre-headless=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:52:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 02 Jun 2026 08:52:36 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c64ac1f9733e348c60a907a4e50edfb1b0203434ce5e2e513fdab8828e4cb100`  
		Last Modified: Tue, 02 Jun 2026 08:53:06 GMT  
		Size: 58.8 MB (58791543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:94311eeb9718e98b76c873681175edce9dab7c86c43e29caab6327569873f642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2290933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b696dd5e6f12db27b283864858b2d31e0708ae4bdd06aa2bf11052be7e405b73`

```dockerfile
```

-	Layers:
	-	`sha256:492c01e5a7043b7de33ee1fc121c41bc6d4243257191232f0d559bfb477e3778`  
		Last Modified: Tue, 02 Jun 2026 08:53:03 GMT  
		Size: 2.3 MB (2279283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf4354d33c7788a3cdecad23258b3fd06e562f575ca0f89eee06f7b5a77d5dc7`  
		Last Modified: Tue, 02 Jun 2026 08:53:03 GMT  
		Size: 11.7 KB (11650 bytes)  
		MIME: application/vnd.in-toto+json
