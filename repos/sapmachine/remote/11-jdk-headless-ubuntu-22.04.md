## `sapmachine:11-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:776070515f0acb93d0c5a663b803f93a62e9f83425cda41ce287e2705587b56b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:df4a68de34e46da893830322aee8a77ddc1c9280d77ec46f5d1fe044f2784783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229158075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:751a95439596fabe36698706b49356cda9dc89f321e48725e0ef29693a90e5d8`
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
# Mon, 27 Jan 2025 13:39:19 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 27 Jan 2025 13:39:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2489ee44779fd31d9b7bfd44c173979a7c80def9f989c6ac7719b5c7aeae4fa4`  
		Last Modified: Tue, 28 Jan 2025 01:29:39 GMT  
		Size: 199.6 MB (199622387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a5f92cafd4fad462d7433f0e3db5948fc6d822b1bc1869e2b287f56363946df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2269244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001146998a0254e5cbb7ea7f48c008a2c99171035204ae333ad65996adc53927`

```dockerfile
```

-	Layers:
	-	`sha256:c89a9c57ab15212c7a84cf69356bf2a7d9d65bad591eb6ae6f1803e8b6cbc8bb`  
		Last Modified: Tue, 28 Jan 2025 01:29:35 GMT  
		Size: 2.3 MB (2260311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dceb559b09a5d3cdd37f1975d1b8f786e3a7068f2a8892ec1155d4e546cc700c`  
		Last Modified: Tue, 28 Jan 2025 01:29:35 GMT  
		Size: 8.9 KB (8933 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

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

### `sapmachine:11-jdk-headless-ubuntu-22.04` - unknown; unknown

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

### `sapmachine:11-jdk-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:64805ff556209e5377f6255529688bea1edd53980985d155b323b2b4e4e7d7d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 MB (220571297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5937a952010e81f4d0d16b8c44288fb36395c9169962ada81183fdb21f8c31e3`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c992d5f536128ea85e3d8f23733eae56643d68504b770f65ca9eaf01ee9639`  
		Last Modified: Wed, 16 Oct 2024 20:23:12 GMT  
		Size: 186.1 MB (186123055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:69a588e816e828d7384e468dfd61112f203a7e4c5dca9daca9d9da55f782db98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2257261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a830aaf0f941b88ad3d02b12510643c447df87303fc46a44bbce00635909854`

```dockerfile
```

-	Layers:
	-	`sha256:f911bc0dd3335fff8e6e1b19e5ef2e19e5ba7f6f8c6416405223101fe5c05b94`  
		Last Modified: Wed, 16 Oct 2024 20:23:07 GMT  
		Size: 2.2 MB (2248506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8f05d532b158b42372388e79c5f616808e18484191aff27978652f81ac7a6c8`  
		Last Modified: Wed, 16 Oct 2024 20:23:07 GMT  
		Size: 8.8 KB (8755 bytes)  
		MIME: application/vnd.in-toto+json
