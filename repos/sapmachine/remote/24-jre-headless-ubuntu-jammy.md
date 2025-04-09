## `sapmachine:24-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:889ef9c4ad8af643123c046cb7cc9ab4c40a7d16036d1da8644bcebfd4e56c98
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:1b5dcafd37d068dcb7bf03c4d3aad409dc2b32e8663bc8709c1de66c1d412d8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95986648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e111d5a675a38597437f241adbcf07bc8efaed9937e181ddd756676e00da75d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1881947dcd715c904066cade40ef849a60845c5fd26bbf381368762052019f3d`  
		Last Modified: Wed, 09 Apr 2025 01:20:59 GMT  
		Size: 66.5 MB (66454283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ae982b61b381a34c6e20593e93ce9a3eb79109b362a38f760cc3b235620398f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2182121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b64a7c1c660756c62f2ac0df47ea3e79a933f9671c0756232ee502a6c752bf`

```dockerfile
```

-	Layers:
	-	`sha256:e69a3ce7e94abac5afb2e9daf6f5ac3b756936f4c87a231aaf424a22e900259a`  
		Last Modified: Wed, 09 Apr 2025 01:20:39 GMT  
		Size: 2.2 MB (2173234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd66e74e5de34b279ecb621b359f30e5bb8563ab1655317aa308bcec3e052194`  
		Last Modified: Wed, 09 Apr 2025 01:20:38 GMT  
		Size: 8.9 KB (8887 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:d30967fe1dbb23592ab8bf40ad0c86433a613485f43bcf30ef9bfe5603ef880d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92801747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82091b146c437bc86a64f5b3c75e89acfc25fad99672cb47dff05fa6f3429723`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6a57736925ce6e9aa0e18c9257eaa37a3e3180158ae96ae049a5964aa6c60a`  
		Last Modified: Wed, 09 Apr 2025 09:24:09 GMT  
		Size: 65.4 MB (65447516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2017b961946122e9fac27de2befc15078b9cc7652c987a27bcbc4bdfd3f0dc9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2181894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:030515843a0f5a2e60a55bc5b9c71b8fb21da800fbf8e1d46a0b961930a6d551`

```dockerfile
```

-	Layers:
	-	`sha256:c1c377c3c28efa681329cd7f60e8227482c45bc0065707c7b9c4542a53b3616c`  
		Last Modified: Wed, 09 Apr 2025 09:24:08 GMT  
		Size: 2.2 MB (2172903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d6df6107f37ba43814831e0eb6c131514e9f2bd1e0ecbd7c9dd483c55277338`  
		Last Modified: Wed, 09 Apr 2025 09:24:07 GMT  
		Size: 9.0 KB (8991 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:85b6ec0790c0200b4ac97341cf1c5b979115bceafe0671d2d0dcbabdf39122d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (101981868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643178871acbf1b34e23b928607548e1a4c78efec72e1d3be8bc775fd1f988dc`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:b1634c9c9ee669b835ef39787fc71f78267fab0678a8e8c5547ba2339762e075 in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:220e8fedb927c1ecfafdf1e8cd0a85977de62e4afd95df2c5a27a70d3bdf34b0`  
		Last Modified: Mon, 07 Apr 2025 08:26:45 GMT  
		Size: 34.4 MB (34442696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54809987596ef59941c8bebc0b2a554f75da3ccf83e1b5bc1bfaba5397df7a5`  
		Last Modified: Wed, 09 Apr 2025 06:43:08 GMT  
		Size: 67.5 MB (67539172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:275118df1c76b528ef766ac7b43ede58911139f7d31e16f120c4d458dcc737f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2185446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac5f1a09940c3b9e344f46684a68cd230938f9c901855f7f49d2883af34c97ac`

```dockerfile
```

-	Layers:
	-	`sha256:072f672bbce7c69a6b6ff4adc003684135db7cddfc0d36bb555cc0a0b510570e`  
		Last Modified: Wed, 09 Apr 2025 06:43:05 GMT  
		Size: 2.2 MB (2176515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2af14f9e69bfc789f9ce53fcf8310bfa81a61cc1f0df159070b66e008a6ac30`  
		Last Modified: Wed, 09 Apr 2025 06:43:05 GMT  
		Size: 8.9 KB (8931 bytes)  
		MIME: application/vnd.in-toto+json
