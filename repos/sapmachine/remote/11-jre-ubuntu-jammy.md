## `sapmachine:11-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:acb15cf13405a2ccb027ce32a618a0462c5b8948dd8c15bd6ca2c98fba2f4948
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:3f56f3a8503c6adb5045403cfd2d2a20f7727f95ab5090683a6a9bc9fe4f6e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79519663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3521f66c305d3c08ebffe401f8998d89551200919948cbff4844b6238f0ac8ae`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:19 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 27 Jan 2025 13:39:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916c264df9fe26f99f69c15daf5999f6a280c6e61cfff3d83cef854a38fac964`  
		Last Modified: Tue, 04 Feb 2025 04:50:23 GMT  
		Size: 50.0 MB (49983722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5cc9ea9425d3111d39844e2e06c36501510c4b82606631e78daed57be09604df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2422175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a638d28d151d8bc6dd324f5eed92a6540f4a76205c02c9b26e9739c6c06a00a2`

```dockerfile
```

-	Layers:
	-	`sha256:007a31e80d6fede033f73b342185337686fed52e2f140a671bc25e16e8a5b8df`  
		Last Modified: Tue, 04 Feb 2025 04:50:22 GMT  
		Size: 2.4 MB (2413354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b507b6bc0458213fe3e0777b0f4eb72982ccf0ad42327dbff572ccab035c40e`  
		Last Modified: Tue, 04 Feb 2025 04:50:22 GMT  
		Size: 8.8 KB (8821 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:1285c90858d95adf7b3c5e9ec1d26dd78b596e41ffdbb4addffbaa7f4b47895f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76631169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18fa609eeacaf738e1cb9fcd0eb640fb8d256fdee8c71c267726f4c0198773a4`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:fee4a09d4d28cee43da3fd4e73788702a289288266433684e3b888210585845d`  
		Last Modified: Wed, 16 Oct 2024 19:48:52 GMT  
		Size: 49.3 MB (49272840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7270967663217ca47a4507cf70ef03b685f7538c986003296c6ad4119d214209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2408586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a79fdb05ee89733027fbe473c68ffeeccdbfd7244d89fc5e6cb8b339457c2ff`

```dockerfile
```

-	Layers:
	-	`sha256:04514e14dd439194c41852ef9080a30b8c2144059faae4aef8c10823975227a0`  
		Last Modified: Wed, 16 Oct 2024 19:48:50 GMT  
		Size: 2.4 MB (2399883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43a7446c95a7409a7186b1047d3608f440a753031615c5f63aaa23ab9a5d796c`  
		Last Modified: Wed, 16 Oct 2024 19:48:50 GMT  
		Size: 8.7 KB (8703 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:95a687d84d8c0bddb25b6c740db70053211bdaff6986760753efc79d8ddc847c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83073384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a056cb468dc343e11082fe5ce67ed2a5539d69be9489291180ffdb7e9de870bd`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:b09e7672e573cb87deb788ce9c604a40e17e00fb8483c5017b321bfadced6360`  
		Last Modified: Wed, 16 Oct 2024 20:24:58 GMT  
		Size: 48.6 MB (48625142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ce7f7807ede1e69e71c480038226c954995d4987018d46fd73bd763b4577a3b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2412203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00804117b41769d36f35491d9b618a8db9f4d6118126fef9cccbccff6cff381a`

```dockerfile
```

-	Layers:
	-	`sha256:3a16aa52083d589f35dbec7a27bf55023239cbb2a8a88cac09076a3d672ca28c`  
		Last Modified: Wed, 16 Oct 2024 20:24:57 GMT  
		Size: 2.4 MB (2403560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82691aa17144d8bf4713c9b95206ceb8341b8f9db911503dc1773d08f791ac9b`  
		Last Modified: Wed, 16 Oct 2024 20:24:57 GMT  
		Size: 8.6 KB (8643 bytes)  
		MIME: application/vnd.in-toto+json
