## `sapmachine:17-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:775c01c38882737f7147711a3eef0d2dcb84cc0937849ff38ebe6582dfb2c902
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:33905c5d80aa3ae2baeabc6db4663ce50536ace5d20216fcbc9387de48651b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.5 MB (229456670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a74274b4ba62a0030f45c2013f9b4e50b9b7015f9619f1deb805c14168386774`
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
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86a891226481e9ae5d3b6e7856f19098167ad854fb2cfd86137743eb9acb52e`  
		Last Modified: Tue, 04 Feb 2025 04:49:57 GMT  
		Size: 199.9 MB (199920729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:277f18357c85ae74e7abe1234afe58783f17878006ce75353dc105d3236938fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2501694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42e0b965083d20d28291f2c124d4632283d5cf832cfa0cc7aa1e73f09b496c55`

```dockerfile
```

-	Layers:
	-	`sha256:76cac1af6e5157e274d4f589bd55f4a3653ecaa39fd0cc3bc0e4a120469fffb0`  
		Last Modified: Tue, 04 Feb 2025 04:49:54 GMT  
		Size: 2.5 MB (2491556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c9cffe8d15dce236dbc277893730f3c1e3117be69a8897e7bea0c098a35ed8b`  
		Last Modified: Tue, 04 Feb 2025 04:49:54 GMT  
		Size: 10.1 KB (10138 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:3152312f6bc8de83a53552cf606f2e4dfc5f48bb45e69c6f57aaec5fa056aaf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.0 MB (225984589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7898e1a1088f5d17de8c9f7f5f471cfa2d2d0846873ced5fb8e7315e315cc650`
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
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1620994d69c25f02383f497d23c2a1da495a94dc4fbffd1117d6de9350bd55a3`  
		Last Modified: Tue, 28 Jan 2025 02:52:13 GMT  
		Size: 198.6 MB (198626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:10415c0058e170f5e2646a533fb722996f64c22b833b3831efdb7e11c0972db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2501575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6756b8e6c55a09fed4505f1b10c96b859c069a952fa8bd5828fa957f4f6ca8ae`

```dockerfile
```

-	Layers:
	-	`sha256:124840eb95211dd2403226a1baf133d0ee57407eebcb735432427ac5b28dc68b`  
		Last Modified: Tue, 28 Jan 2025 02:52:08 GMT  
		Size: 2.5 MB (2491286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50cf061bb01e136d3f0234fb8ffb58060488eeb15d8a6ea745b7aaac84835fb3`  
		Last Modified: Tue, 28 Jan 2025 02:52:08 GMT  
		Size: 10.3 KB (10289 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:5055b78001662be5c7f536f6df5c3338c0c80a4ba273ef7e5ee6de1e63b5040d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.5 MB (235451663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0f4b2ec555a641c6fcd03d68635c7df364e2b4709bd412342f8d1d2d226114b`
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
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589ab061e8f9d7b45a2d2eca01201e5f525b4b99c63e071766fbd4da78026a4d`  
		Last Modified: Tue, 28 Jan 2025 06:17:28 GMT  
		Size: 201.0 MB (201003421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:02e46e17f8f5cdabc5b4e965ab2af971153476c4186ea186235b8bbe093a4066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2503821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:002f2ba9fdd943c0b98cbd42beca00d6b3ea1c95e9d5bae8f4bc353f4970cb95`

```dockerfile
```

-	Layers:
	-	`sha256:cec3c22db4cb85e946d136ef8412800768f3e601d0399ebc02d47f2b53eca358`  
		Last Modified: Tue, 28 Jan 2025 06:17:21 GMT  
		Size: 2.5 MB (2493615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1913bc8e70ff2937f16d537875b4cfa26e290872edbebb9cbbda5caddcbdd3d9`  
		Last Modified: Tue, 28 Jan 2025 06:17:20 GMT  
		Size: 10.2 KB (10206 bytes)  
		MIME: application/vnd.in-toto+json
