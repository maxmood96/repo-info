## `sapmachine:jre-headless`

```console
$ docker pull sapmachine@sha256:133b4232ba6a6d0c89b91e3ce57aefbbc70f66ce3656e922fee4c07c4face4ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-headless` - linux; amd64

```console
$ docker pull sapmachine@sha256:20b7c1f5862f199847b5baf2311f982cf0a527b28bf8a951df9c5441a1080e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.9 MB (99907964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c5fc0f3860dc9d0e34af748d27d9bb1cd93983ecd5a9c726c518b325237bf54`
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
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
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
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6b65a358cb09ae67e07a2f0c4aaedd297610ed7bab852d072bbbd855a714b0`  
		Last Modified: Thu, 02 Oct 2025 05:18:25 GMT  
		Size: 70.2 MB (70184953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:32cb831421e9215d7508034124398606a56747c6fe9751e9fe53764a3ab8573c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2292097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1e64c2aa9fc6deaa602f74635b71a10b2c4ef7801a983f84afc05a510035450`

```dockerfile
```

-	Layers:
	-	`sha256:68144bf27b137a26fdfb2416d856d9978c5ae9ca06f2949c8b00d8024f018d4f`  
		Last Modified: Thu, 02 Oct 2025 09:12:52 GMT  
		Size: 2.3 MB (2280858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ce3bc7643fbd31af7d638e20a49ebf4ebd1ef569c98c6a2a6a58a225a673885`  
		Last Modified: Thu, 02 Oct 2025 09:12:53 GMT  
		Size: 11.2 KB (11239 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless` - linux; arm64 variant v8

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

### `sapmachine:jre-headless` - unknown; unknown

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

### `sapmachine:jre-headless` - linux; ppc64le

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

### `sapmachine:jre-headless` - unknown; unknown

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
