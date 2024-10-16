## `sapmachine:11-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:f876bbcd891f232e0276abf781479692bcd68d40c76923fb757bed38d8289c05
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:1dc033a4226f1135fc147176a0e5b59d3902e9eccf74bcf99d48ac04182358f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229166246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:389eddd5f51d0fe488630ca6d4ddc0dd51a056f464d9d5ea488b689b30a26065`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963962493f851f2cb52c16cd9f1dc70baa9134c2b3c22c52c80bab7f457c2acb`  
		Last Modified: Wed, 16 Oct 2024 19:00:04 GMT  
		Size: 199.6 MB (199630558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:23ee322a904c0035e616b5d63be95c9594b56a9601842f14f74e3a687b29d763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2255887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5575c3361bc91d1777e83db59645c7ac0ae43cebff3bb4cb25d2c42ae895780`

```dockerfile
```

-	Layers:
	-	`sha256:ea86f42b162251edf652635c055a568b453118ede56c6641b404b33ca919f09e`  
		Last Modified: Wed, 16 Oct 2024 19:00:00 GMT  
		Size: 2.2 MB (2247171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bfbb34cd747e4e92ec4043db01efe9ce0e4cdeab3ff3d0c3d76c3aed2222714`  
		Last Modified: Wed, 16 Oct 2024 19:00:00 GMT  
		Size: 8.7 KB (8716 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:6e0b6eae44a16172bd96e736a6ae6fdd3e5a5a6e60b670f1b5899875184a1d5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.4 MB (225436572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84da2934cdb05c57ac5c898c470cda2677bb657c5ed8faa6931fd25e7870becb`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a916521442d3f3d95ec5a665e9e83608db154ca963672c8462a74a07c02af577`  
		Last Modified: Wed, 16 Oct 2024 19:47:59 GMT  
		Size: 198.1 MB (198078243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:98c65148eb0d7087303ef6b40774a57f48351da97837094ed9aaedec9b18113f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2256283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a0b638649904c82ee60f7456aa16c1f9b6d20317e3e5d2fab535bfa60a817a`

```dockerfile
```

-	Layers:
	-	`sha256:ac68de550f575140a20111559421b4194b6923fe187334aca89b9cbf3aaa57a7`  
		Last Modified: Wed, 16 Oct 2024 19:47:55 GMT  
		Size: 2.2 MB (2247469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:892ca2d92d3640ce7c1ff3eed62eb8d2ae961c0a548d50feb68157d7818682d6`  
		Last Modified: Wed, 16 Oct 2024 19:47:54 GMT  
		Size: 8.8 KB (8814 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:560d0962c6fcb702f6f2b627cfc467286141d30bc2f2d8afa245990843b44726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.4 MB (220441824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f341fc9c8efd1e5d759f0b89a546951c76e7dfa5027aa6f9cb56f3b85faa5e9c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e99e354ad4476324d62da56823e1992af776790a911419c7c1458020308b49`  
		Last Modified: Tue, 17 Sep 2024 03:07:53 GMT  
		Size: 186.0 MB (185993582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d9246a68d2dfa9bc03ad6667926aa54a12b4840125ec6ae2ce5a482d60b15eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2255942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d17c0089d1a5fef9a972bb5e450b326e8830a9c7d2f12ca5dda30224cf95574`

```dockerfile
```

-	Layers:
	-	`sha256:010462e3bafe013e0f4ce6c5d93c09824538122f9ac34f5933f98314d6043693`  
		Last Modified: Tue, 17 Sep 2024 03:07:47 GMT  
		Size: 2.2 MB (2247225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b038b17635da8d8aa2e93816fe17b6802b7d8b97486cd24f002442e82206acd1`  
		Last Modified: Tue, 17 Sep 2024 03:07:47 GMT  
		Size: 8.7 KB (8717 bytes)  
		MIME: application/vnd.in-toto+json
