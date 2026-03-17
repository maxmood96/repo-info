## `sapmachine:jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:066ab1ae74c1ed8783a25d1861f1343dbba16eea8fa5229259d03cce71c4d6d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:6f7a15995cab8c4f89e317b7dd390a43b87d20dfe33aeb05a635bf014b064c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.4 MB (249393276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c323ab923367cdd4be21eb82d9267f0d21da6bb777c04730feeadc803c8380d6`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:24:04 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Mar 2026 02:24:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acf84db329ab71b788ed2491c892ed785a06e77f54a72e20249d964bb270398`  
		Last Modified: Tue, 17 Mar 2026 02:24:28 GMT  
		Size: 219.9 MB (219854756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:01e79aa04793aa67804a75e8419a66e209b18d63f8538846d2344561a1f3511d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d76fea9b0934d3ea99b98bacbca0717a22564618e03128e9fc790850b2d276df`

```dockerfile
```

-	Layers:
	-	`sha256:73f7385e941a629d7cf7181bf47e0ec4871d10885dbd81b5ffa89b5e3a7b1074`  
		Last Modified: Tue, 17 Mar 2026 02:24:23 GMT  
		Size: 2.4 MB (2370882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fd3e13a7a1a8df2b7b6874aa440bc025cd44962a3c09fb4f3b0a774bce19456`  
		Last Modified: Tue, 17 Mar 2026 02:24:23 GMT  
		Size: 10.3 KB (10273 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:c04514fc65734f5f36d4de27657412b477b787eb78b1cf6e9b0821d2e32aac2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.0 MB (245007544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43977105f90b9c3f50debce053aaf4dfbf20115af522e3217d05834439de5590`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:30:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:30:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Mar 2026 02:30:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74926855e6e0cf33de9683d614621f121f945599d14e2d118ed0a1a8a0e5dbf5`  
		Last Modified: Tue, 17 Mar 2026 02:30:39 GMT  
		Size: 217.6 MB (217618519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4585f817a390a4948ca1e2394660d3dc25a93581d332b3c03323759d871b3af7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2381024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a95dffc75996dc98c56bc39bc62ec898fc6f84c5fa809eb64043976fea6daa91`

```dockerfile
```

-	Layers:
	-	`sha256:8ed22817cb80afa13412eab722031e743f3067a1e5151a440a585782642a7b85`  
		Last Modified: Tue, 17 Mar 2026 02:30:32 GMT  
		Size: 2.4 MB (2370599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87f2211732f36a1bd0bab5f3ef065300c450351cf98607938775a6cb6e50abfb`  
		Last Modified: Tue, 17 Mar 2026 02:30:32 GMT  
		Size: 10.4 KB (10425 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:02d4b08635eb6a5b7ce7bcc6ce78e7a1d11353fb4f93db32c2a6ee1313a2e1c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.9 MB (254928925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6ac92ec1f2d4aceffa7c9d0391fa3d232dc854dd638256a91ef938da2650299`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 24 Feb 2026 07:34:11 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:34:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:34:16 GMT
ADD file:8cdc5dcac981a23986a941c048f55a86d8ba46328e91ad30db9af43286781c61 in / 
# Tue, 24 Feb 2026 07:34:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 09:38:00 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 09:38:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Mar 2026 09:38:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:31e4dc9ee1718c21d378c7cdb3929e157eabf4d70fe4bbe2e6b8ec5289e836dc`  
		Last Modified: Tue, 24 Feb 2026 08:08:05 GMT  
		Size: 34.5 MB (34453448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd1dcfd795d3656d20afc574582f26f1b24631253f57c53ef3b0efdca0060c3`  
		Last Modified: Tue, 17 Mar 2026 09:38:49 GMT  
		Size: 220.5 MB (220475477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5d735940329f4497cd01b5afa65db37808b07dea9eb75bfe90f44aad77d9f788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2378125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2155224afce9c3559a515c9374b569ae23f67c7c67e42d5fcd1b1853d4c9e6`

```dockerfile
```

-	Layers:
	-	`sha256:110360f13d03036c507c884d253ca2053cf6cd91e5ec04002ece0804a7b3c33f`  
		Last Modified: Tue, 17 Mar 2026 09:38:45 GMT  
		Size: 2.4 MB (2367784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e41ed2e37e6a3bc9a5478fe87772f295b6926ab212951e4670409c229379e6e9`  
		Last Modified: Tue, 17 Mar 2026 09:38:44 GMT  
		Size: 10.3 KB (10341 bytes)  
		MIME: application/vnd.in-toto+json
