## `sapmachine:jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:c2b866b7a07cfc8618dd42e01c32196348f22e8c6175b0a2c132783fd3165f4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-headless-ubuntu-jammy` - linux; amd64

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

### `sapmachine:jre-headless-ubuntu-jammy` - unknown; unknown

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

### `sapmachine:jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ec4db1e57b8743f133d7e90b3c336fdccb8617c80e0b193ad919aa72c2c79333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92799288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d896ff1d4b62324bace2e7a8827d7b7415c50066954dec93a406311ec052a37`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c5ff60b17046c425158d10409d1743846f3bd1528dd7698818474942ca06ec`  
		Last Modified: Wed, 19 Mar 2025 20:39:18 GMT  
		Size: 65.4 MB (65441106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3165dee0356f44c5a0b0981aaf898e04571c38069cc717358b757b08cc920bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2181806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d7492ca105cef29feddc7283fc5ce5cd4130df2b6c39e4f0b5178c10742565`

```dockerfile
```

-	Layers:
	-	`sha256:757c6173abf4767c4f8cb84d3b7d6ff3b7255c6c9c18ac1b2236edabe0dbb033`  
		Last Modified: Wed, 19 Mar 2025 20:39:16 GMT  
		Size: 2.2 MB (2172815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f142239bc18bee4b57b5cc38ab5ff2e2418b9acf6d06b269f989a668135410c`  
		Last Modified: Wed, 19 Mar 2025 20:39:16 GMT  
		Size: 9.0 KB (8991 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-jammy` - linux; ppc64le

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

### `sapmachine:jre-headless-ubuntu-jammy` - unknown; unknown

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
