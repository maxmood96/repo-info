## `sapmachine:21-jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:645270522443e6fc2d540878b2eba8eb39157e74d44ff6e13e4c0ee3a155154f
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
$ docker pull sapmachine@sha256:0b01ececb62781713e750ac1c0345beef94adf308ab795cfb0153d9edfb3d7d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.3 MB (89260010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc27a1fe07ebdff953f09e406f7eeb40edc56db34d3cdc9afe05a8aca7e958d`
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
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3649460a2692c47564aa03f0403a32b3a54f9b9a6db37fe8d6ea28565c4ed80`  
		Last Modified: Tue, 04 Feb 2025 04:49:16 GMT  
		Size: 59.7 MB (59724069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f9e5dcc6b3728323327796dad51cb39bdbe82731342b4488aee616b24b1e945f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2418730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d62aec8400437c6507d14961874840fcaad0254eae6002393388bf3c3b6dd5e`

```dockerfile
```

-	Layers:
	-	`sha256:ea5d903b1491a79d90a6d6d81ca9fd28b2542d274587f04dce4d173b55f60119`  
		Last Modified: Tue, 04 Feb 2025 04:49:15 GMT  
		Size: 2.4 MB (2409250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a874366b361cf9a735022ea3e1f0d43f4b0563059ed93153ea3495acead520c7`  
		Last Modified: Tue, 04 Feb 2025 04:49:14 GMT  
		Size: 9.5 KB (9480 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:4ba0216c75f89f634f9c95e23e89513f1718c0a8a581eedccc186cf718815041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.2 MB (86216618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce2ad72719eea327eb326631f4341516a71b7f29017d898338e776d1c46fd538`
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
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32965fbc5c6c7167bf2fd30dbcbd4cd5247fa289b1e49d9525bf0ae4d0de4397`  
		Last Modified: Tue, 28 Jan 2025 02:41:21 GMT  
		Size: 58.9 MB (58858289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:861e39452ea2a8631d431b84a6dc02ad8b0c24aab3f0e8aced29b263778df986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2418564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a601ef59081b6ab7f9c04c03945b861268fc29d4314ffdc035ceb73673ad141`

```dockerfile
```

-	Layers:
	-	`sha256:0615ae8966fe0f04641b1c0a216db502b975bc4e046cb7d14042da69fce4fb97`  
		Last Modified: Tue, 28 Jan 2025 02:41:20 GMT  
		Size: 2.4 MB (2408956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc2c832a991b000cf1dcaca26bd09dd2e0691c01678298e32a01893349d187e7`  
		Last Modified: Tue, 28 Jan 2025 02:41:19 GMT  
		Size: 9.6 KB (9608 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:fc2308957254ac4470ce2af9ed15186e4559f619709b219aa600eac5c4128dfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.7 MB (95749640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a925e76387db8b6dea5bf002915096eb58b0d33f5154cfb521750e63aa39139`
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
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02fc52c27acef058c510fab3b91792a6ff284d33fa77d569ee6dd6b6ee34dc2`  
		Last Modified: Tue, 28 Jan 2025 05:55:31 GMT  
		Size: 61.3 MB (61301398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2288b548c08d03ce66f09aa287e147deedae68c7f7942136c85d3ea50916fcb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2422779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09b02eeb800178d233654d026907fdc2c0b3e56973bd9dfc0c732b7eb7879e4`

```dockerfile
```

-	Layers:
	-	`sha256:131893deb9f9fdbdca4d0ef577eeee4789a9affa67b4965bfa314c0b202bd863`  
		Last Modified: Tue, 28 Jan 2025 05:55:29 GMT  
		Size: 2.4 MB (2413243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ba091aa64b07c65e658ed2086565ecbb7fe5e3fc9b3bcdb5313d23aea685d37`  
		Last Modified: Tue, 28 Jan 2025 05:55:29 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.in-toto+json
