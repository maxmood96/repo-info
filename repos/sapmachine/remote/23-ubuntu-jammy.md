## `sapmachine:23-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:c62d21a10bf3db261eafe4494a93ae19c2d40e0365c01f581d909ee904558cdb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:23-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:bd5c0957c499f6f8e3e51339fc7d04b43f3f6f7250aa2ed639f315da8da00064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.8 MB (251799622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:130a52d9b9c7f6251e8ead80e2fe3b1fb7b2c822e1a487e2692d56c54ed34696`
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
# Mon, 27 Jan 2025 13:39:22 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-23-jdk=23.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Mon, 27 Jan 2025 13:39:22 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbaea44bd7216e63d105bf302198ad667f6558440e2c759aae0abe3e7432f23f`  
		Last Modified: Tue, 28 Jan 2025 01:30:01 GMT  
		Size: 222.3 MB (222263934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:08d8682d1535860b0a48fcbf0f632903239c1929da805d650824dba9a3e66bf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2508054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a39d3fbfce80f0d53c4476fb93ee584d04df35d165d9221d2022c7ad94a1c7e`

```dockerfile
```

-	Layers:
	-	`sha256:04bd8cef81710f6db84edb5dc2973fbd46eea63327b2df1e721ff89ae57ac38f`  
		Last Modified: Tue, 28 Jan 2025 01:29:58 GMT  
		Size: 2.5 MB (2496641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4877b86eccc6ec1807e4700a941550c0cc7511553447f18ea6c9bc0252617e7`  
		Last Modified: Tue, 28 Jan 2025 01:29:58 GMT  
		Size: 11.4 KB (11413 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-ubuntu-jammy` - linux; arm64 variant v8

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

### `sapmachine:23-ubuntu-jammy` - unknown; unknown

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

### `sapmachine:23-ubuntu-jammy` - linux; ppc64le

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

### `sapmachine:23-ubuntu-jammy` - unknown; unknown

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
