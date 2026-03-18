## `sapmachine:jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:3d8467be755c02a3023f2e92e83df1c4d0bbba4a02f478b3628bce60896ffb61
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:5b5788d98e8ec7ca85c203dc7c371c15bd869dd2e169ed1646ce01703511c330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86931803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f5f25ee84fcaf6b38075a9d9011b6f3941e9c800973df19a5b19620d4a89ebd`
-	Default Command: `["bash"]`

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
# Wed, 18 Mar 2026 17:49:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Mar 2026 17:49:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 18 Mar 2026 17:49:29 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5282d4323a443e637fd4503c2b245ee460eb03ee558d21f8389d9ba223b90dd3`  
		Last Modified: Wed, 18 Mar 2026 17:49:42 GMT  
		Size: 57.4 MB (57393283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7e2a31967e61d050512790fb7c88680fc82a3697d5609b3e13fc152de4cf521e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2309183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2f68b33cec9f2fffbe69bd80e3130dd8ea8ceccad66826ae243eb991792849`

```dockerfile
```

-	Layers:
	-	`sha256:5e731380338a48ac36d8dea0ccf4cffee4a5b4703311db8ff2ba208011d8653a`  
		Last Modified: Wed, 18 Mar 2026 17:49:41 GMT  
		Size: 2.3 MB (2300343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:192dfcf7b36931ac4fe63942caf2b06e323e662e53d9a12538200f2f27a4a1ef`  
		Last Modified: Wed, 18 Mar 2026 17:49:41 GMT  
		Size: 8.8 KB (8840 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:63096a8403be9022bf610760efaffbb74541e445e1f833cc778b9f0fac91461c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.8 MB (83755393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a26a27c8ea26969f5a6907d051a1f8a58a98c668ba2613c5e4b042c121e4177`
-	Default Command: `["bash"]`

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
# Wed, 18 Mar 2026 17:49:26 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Mar 2026 17:49:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 18 Mar 2026 17:49:26 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e477b212833763b39fa21b482602c3eb92a5b985c313b94570e2e55c03132c77`  
		Last Modified: Wed, 18 Mar 2026 17:49:40 GMT  
		Size: 56.4 MB (56366368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:09b944cd776a9c4b6be5436688f9e96c1aec6e1ae9fb205bff292ab2e41acd5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1329f9303a6fba5d66c411f8a15a828f08f8ad01d0d968507267b5f5e2bfc26`

```dockerfile
```

-	Layers:
	-	`sha256:fbc12254701a5c09d7c9c9280dad330bef9d25839f08de8cb390be1e17b917b0`  
		Last Modified: Wed, 18 Mar 2026 17:49:39 GMT  
		Size: 2.3 MB (2300012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:accdc1d2932d006b5410de39f242ae146ec95847bfb2183381ec0acc09065fe6`  
		Last Modified: Wed, 18 Mar 2026 17:49:39 GMT  
		Size: 8.9 KB (8944 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:ced0d5fd04699e4d789c1b0fe6108e5cca9802377414bbfffab3a325e74277a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92743163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:663cee2056f7bb3dd10445712fed79b606cb0818824186e0dc64cbad50bc2477`
-	Default Command: `["bash"]`

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
# Wed, 18 Mar 2026 17:52:55 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Mar 2026 17:52:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 18 Mar 2026 17:52:55 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:31e4dc9ee1718c21d378c7cdb3929e157eabf4d70fe4bbe2e6b8ec5289e836dc`  
		Last Modified: Tue, 24 Feb 2026 08:08:05 GMT  
		Size: 34.5 MB (34453448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfff8ad08abb81b37e26361bfb60c40b7c02e17f19dc1d5ab5c961389db9c6ab`  
		Last Modified: Wed, 18 Mar 2026 17:53:23 GMT  
		Size: 58.3 MB (58289715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e1d9acafb81ac49dcfb70c037dcfa28c2e7a01ecea902f5309f9e8eb95b38499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a0804770bed57408156603a94eabff612989a7abeb6c7660ab1593f93b65da`

```dockerfile
```

-	Layers:
	-	`sha256:1496b81a540948e664e29abbbd8956d80fc1a0a66344c5399c8f14b28b2712ec`  
		Last Modified: Wed, 18 Mar 2026 17:53:22 GMT  
		Size: 2.3 MB (2299155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:358e537cb09473054315816fe269ad0b9e49cc58c17ba00726ebaea4e8dcae31`  
		Last Modified: Wed, 18 Mar 2026 17:53:21 GMT  
		Size: 8.9 KB (8884 bytes)  
		MIME: application/vnd.in-toto+json
