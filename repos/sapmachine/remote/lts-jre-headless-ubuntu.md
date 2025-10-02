## `sapmachine:lts-jre-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:c4a4601bd4320e4f1bd4e5e6198f74dba80102c0adf3a1055af62085a517d073
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:4b06b079e58c617ed5433316cd3e4bb8113c0be5401257251efe629f83c5993e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97506382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02e1b6c4f6f7834d2185a7566149731cfb5bd4494af384b41f4aedbf99a82a2f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Sep 2025 05:42:32 GMT
ARG RELEASE
# Wed, 10 Sep 2025 05:42:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 10 Sep 2025 05:42:32 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 10 Sep 2025 05:42:34 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Wed, 10 Sep 2025 05:42:34 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc244670a19828abd2fe5012ee1c8a3e4842093a67681374431201f82962414b`  
		Last Modified: Wed, 17 Sep 2025 17:34:57 GMT  
		Size: 67.8 MB (67782932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:04339a3c1730ed6136ea247aa7efd466f01a6f1504d98f7e1eae1264d18e0538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2292097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa697eda2d3b0a83b5a48d55950194873618f8f89d6ea9fbe736606fa8e910aa`

```dockerfile
```

-	Layers:
	-	`sha256:b36d3a2d5b52645b6b37456734921ecb53c6423bfcb239b001d860d1982b120e`  
		Last Modified: Wed, 17 Sep 2025 21:11:45 GMT  
		Size: 2.3 MB (2280858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd7ef1ca608c6f651b15b935e7a8bec1f426797a0c58587a5bfa9d3c6ebc65df`  
		Last Modified: Wed, 17 Sep 2025 21:11:46 GMT  
		Size: 11.2 KB (11239 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:51e786b687654104822a458921c3e7c1a100ee3285234e6e0fde500880f79c02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.8 MB (97841888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0e2700b5f471d752904c747023006d479dae07daf589783d0b66c9683c79b1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Sep 2025 04:28:56 GMT
ARG RELEASE
# Wed, 17 Sep 2025 04:28:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 17 Sep 2025 04:28:56 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
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
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f2f8c82281656f7849c9b8aff7b56f945d45e6d65fa839dba2eeec6c47a47e`  
		Last Modified: Thu, 02 Oct 2025 01:33:19 GMT  
		Size: 69.0 MB (68980313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6437c2fe62c042b02db750113979bfb0d70ecb7cda3a40f4d868128a72da77a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2292825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e50ba34efde147105eedef852aae2512f575d93b9495b79600e5642fab4376c6`

```dockerfile
```

-	Layers:
	-	`sha256:d8593086caf5e9723df0cc6af6c94ea6a1e3040af7a0178e911de1ce7bdca55b`  
		Last Modified: Thu, 02 Oct 2025 03:10:53 GMT  
		Size: 2.3 MB (2281398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c91eda1f620a7133619fd7b95ff7ba823df9161962481089d6956cf77e186c80`  
		Last Modified: Thu, 02 Oct 2025 03:10:54 GMT  
		Size: 11.4 KB (11427 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:3914db22114a04b79c0bb9c59e0a5055a2be7dd68458f859a71b3379fe2c0185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.5 MB (105456371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17d495226670a023f322ad7febc33aca62e3e812904822bb55562a6b64fc170c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Sep 2025 04:28:56 GMT
ARG RELEASE
# Wed, 17 Sep 2025 04:28:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 17 Sep 2025 04:28:56 GMT
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
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
	-	`sha256:15a6b79c4fd2f3417787ba4c0a8161183cf898454880102c719eb0c91671c218`  
		Last Modified: Tue, 30 Sep 2025 17:28:16 GMT  
		Size: 34.3 MB (34303547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44886fa4184870a4f6ce3cf735a319428a666bb6fb13c64e88d54e236c1d90b0`  
		Last Modified: Thu, 02 Oct 2025 04:17:17 GMT  
		Size: 71.2 MB (71152824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:545af48b5828d0627529742c0a7fed84199bc2078518f3c4b8a0da6bd8150b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2289571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9cb902eb7618310dec9b5829590bb2b21c89d3be1b68a813f8155d815bb489d`

```dockerfile
```

-	Layers:
	-	`sha256:a5507f5a21a4cab235faaa89818178bf0b3ef2f0dcba0f9fea498d1f521491b9`  
		Last Modified: Thu, 02 Oct 2025 06:11:14 GMT  
		Size: 2.3 MB (2278246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75de0ab95ce72b7bdbb911a9720dcf805d0db9a82afd0f229369227f82892cb4`  
		Last Modified: Thu, 02 Oct 2025 06:11:15 GMT  
		Size: 11.3 KB (11325 bytes)  
		MIME: application/vnd.in-toto+json
