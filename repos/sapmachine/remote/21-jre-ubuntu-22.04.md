## `sapmachine:21-jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:f0317b938c2f84eb357b6159551112e81f552e26af9730e9ccf88aec671021b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:70786a4b6b4f4e0ea30ac107158c0be889da835ee81411db81dec7f5e1b30673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.9 MB (89882769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff88fa4f388ecd946251e74dfccb8c6aaf977df824e1efa78e5cd8bc099e84d5`
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
# Tue, 17 Mar 2026 02:24:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 17 Mar 2026 02:24:56 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da33b3a2507415b05186c68ee01844e4ab427f4cf1285fc9645ec78e1e9b020`  
		Last Modified: Tue, 17 Mar 2026 02:25:09 GMT  
		Size: 60.3 MB (60344249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b224faab1201373cc13dd58aa8e1db9c15a716eacf36994249bedd74b197d2ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2556114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c8666c03413dff230717f36d5851db22672d5a2a056eacab6f6d64a5da8072f`

```dockerfile
```

-	Layers:
	-	`sha256:793173b96fff5071917ceffb3bb6b8379949262690d63816eacf6450cfcb2f8f`  
		Last Modified: Tue, 17 Mar 2026 02:25:08 GMT  
		Size: 2.5 MB (2547317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26584f70706c60b2bc13c3f6c466300a5282a08c5aa696461b46ac99d024bee3`  
		Last Modified: Tue, 17 Mar 2026 02:25:08 GMT  
		Size: 8.8 KB (8797 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:0fd6a0c30d64938dd88197089acafc60970b72fe936cade75aacc537d9c32a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86886728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2597c5413748a9f7583b0a17546ba4e9c2bb03b2ff91a522dd79aa15f7f93f3`
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
# Tue, 17 Mar 2026 02:31:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:31:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 17 Mar 2026 02:31:11 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3bf6dab2d0cc5483783eac14083fbb9ab95f93eb35af53e83206edb07cdd008`  
		Last Modified: Tue, 17 Mar 2026 02:31:25 GMT  
		Size: 59.5 MB (59497703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d33df9d446587018e41ef19955a3da74fec9319fc4262b38853777a4bf96a682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2555901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef7fb1be04bdb380804eb0607caeda0c16fcf167fd5d9c012cc5b5578b6c99d`

```dockerfile
```

-	Layers:
	-	`sha256:60061139477455ad147f69e07006a3f08b23513ef4d89e1af9e9d155b507be0b`  
		Last Modified: Tue, 17 Mar 2026 02:31:23 GMT  
		Size: 2.5 MB (2546999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa12781ef7482bacfb2dc3a6274463d658facea1913a00f00d1cdd25aafa73cd`  
		Last Modified: Tue, 17 Mar 2026 02:31:23 GMT  
		Size: 8.9 KB (8902 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:760ca8b29948c79c6fd1f437be9cf5e2dee1c3b5ed562f7e2a52c0f28046d1b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (96024426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:314c37913831e0504b8d53f38d5c127ac1538d90c8d8b042bfd6f289a5d8869f`
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
# Tue, 17 Mar 2026 09:47:50 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 09:47:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 17 Mar 2026 09:47:50 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:31e4dc9ee1718c21d378c7cdb3929e157eabf4d70fe4bbe2e6b8ec5289e836dc`  
		Last Modified: Tue, 24 Feb 2026 08:08:05 GMT  
		Size: 34.5 MB (34453448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2fd0164cf236548ac9b04dd1b3547ddb61dea9194532f99a0f869627f311855`  
		Last Modified: Tue, 17 Mar 2026 09:48:15 GMT  
		Size: 61.6 MB (61570978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f55ed37743140ab8eee01e92ecf9bb83331bb7c46dff6906384c4e55806ff660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2555690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc8a54a6c754f32da69be113ac632364cdb056281582eda041e616f413a46f15`

```dockerfile
```

-	Layers:
	-	`sha256:8db3a5cc3c70dc1cfbf299c4aab0149903967a887780cee4f771e0df40bd83e9`  
		Last Modified: Tue, 17 Mar 2026 09:48:13 GMT  
		Size: 2.5 MB (2546849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e16d72b356023f2f9807db7d00ca18430839701dda609db9ba140547f28e8b77`  
		Last Modified: Tue, 17 Mar 2026 09:48:13 GMT  
		Size: 8.8 KB (8841 bytes)  
		MIME: application/vnd.in-toto+json
