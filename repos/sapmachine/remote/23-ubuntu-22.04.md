## `sapmachine:23-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:543c7fd573d1301caafa4ebbfdae049059f0446eeddf2030bebef7f13ad8bb70
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:23-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:28336e18d53b839e4545e596de3ee24bd5e77e307a7ecf45ce01407b5fa63bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.8 MB (251800027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed051ffd900ff4c93ca429612cdd9b6e33c920003b220c4825cc6320d82f6cb`
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
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jdk=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5d674a1b591c4d0c2e9dbe59224f41a31de1124bac807b8db0b6bbd41d0bfb`  
		Last Modified: Tue, 04 Feb 2025 04:48:47 GMT  
		Size: 222.3 MB (222264086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ba41802dc37e648078810e139a9e76f0a421942aeb4cddd1e57cce54b1a7c54a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2508054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ea1a4b6dd661b9d8c2fd0a970e8929d3c37ce009ff6c1897a2aef07e5ea5d3`

```dockerfile
```

-	Layers:
	-	`sha256:338997e617d33ac4c7bcc643674f1765c53cf8181497ce61a6141072a67167f5`  
		Last Modified: Tue, 04 Feb 2025 04:48:42 GMT  
		Size: 2.5 MB (2496641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d47d53b84b96dd44b58127fe6ed47ae6d3316f13532645a1db3531d54cb0b8b3`  
		Last Modified: Tue, 04 Feb 2025 04:48:43 GMT  
		Size: 11.4 KB (11413 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:5541e693f5a7569598d027ea0764aea9eed8c8f7087cbe571f4d8498d1c3092b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.6 MB (247582764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc72b4042929c48b0bcbd64acbe312371e18af896e28fd5b961690d0849a4d41`
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
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jdk=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d0cd5da64a94b6b147d041c70244d21fb9c75856a123199dd09206f5d48c16`  
		Last Modified: Tue, 28 Jan 2025 02:24:58 GMT  
		Size: 220.2 MB (220224435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9ecbae176c81256662d6a7ca6721f64e707a65c2ba7ec581248b12bf8e91a285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2507402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e5c5bc9248c0d3c404b6e7b9fb68d290c55cba1e2839e721a196b05517520e`

```dockerfile
```

-	Layers:
	-	`sha256:f10c5de220ba7d90b95ea39879195a0ac35c2b3c683429390b75c6f3e146a5b5`  
		Last Modified: Tue, 28 Jan 2025 02:24:52 GMT  
		Size: 2.5 MB (2495789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d00bee5960c006c1124bed3a429efb8bf28aec423eb4cba8c4a5cec15475c4f2`  
		Last Modified: Tue, 28 Jan 2025 02:24:52 GMT  
		Size: 11.6 KB (11613 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:d688e08e2322624481f85fa38cf2a835f38dff0a87fd4630c3ae60f275631563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257741587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:437af9d12c78558a3fe1c4f67d986c24adc0468ae27e8c1a6be2c7c2a656b942`
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
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jdk=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deebca553f118bbfd64f15798b7a34a5dff7dfa767e21433b90e33224935b70f`  
		Last Modified: Tue, 28 Jan 2025 02:26:41 GMT  
		Size: 223.3 MB (223293345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b83e1ed17fd0db8d357dcdaa8407e3bc8408c28518733518a5143bef8fa3e38a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2509611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:105b1bf242e41023fcabea424b9036d6e67dfac0c1641f37090c72605cc1ade0`

```dockerfile
```

-	Layers:
	-	`sha256:115f7be74dd6a63748f1744e8e39928494816d0dd131b7defd6a35d18c60395f`  
		Last Modified: Tue, 28 Jan 2025 02:26:34 GMT  
		Size: 2.5 MB (2498106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3d3ffd42af2c89bce86b1786f3367e91688302f8483d20206668d692555fd87`  
		Last Modified: Tue, 28 Jan 2025 02:26:33 GMT  
		Size: 11.5 KB (11505 bytes)  
		MIME: application/vnd.in-toto+json
