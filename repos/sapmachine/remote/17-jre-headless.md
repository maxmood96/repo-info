## `sapmachine:17-jre-headless`

```console
$ docker pull sapmachine@sha256:5305503af5e697b3c0b0f2309e4808bb35c85a54e246f0b315220566bb46869a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless` - linux; amd64

```console
$ docker pull sapmachine@sha256:7414fe7a80ade869967f3352f38c17dfed572617842368bfe6368ed25486096f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82781836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b1585c5d6a07eac4785707df151a748455561a478d5130fa48f7219fce2e79`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a68dd9bb022929c75c899423254d70bfb2fd984f35bfbe4ac5d9ad2735ccab`  
		Last Modified: Tue, 02 Sep 2025 03:13:18 GMT  
		Size: 53.1 MB (53058772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3a0e843008dc66219de86652f133fed431e5cd878c51e01c3dbf575d6a1a0d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2281836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4e5bdb0c721eb0dc7ed54fa5f2454e19499da71ef74da9feefbe3197fe8e4d2`

```dockerfile
```

-	Layers:
	-	`sha256:718ba3f6586e0688604bac82b1edfb960860058f2900c0bac7482c25f8c40f3d`  
		Last Modified: Tue, 02 Sep 2025 03:05:56 GMT  
		Size: 2.3 MB (2271560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dd8a555ce660969100a36c1ddfe8fb08ad447a3e3eaf36e86cc5a46ed6a9282`  
		Last Modified: Tue, 02 Sep 2025 03:05:57 GMT  
		Size: 10.3 KB (10276 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ab8cc91c927a630976bdac5e78b1cdbcdc3668e42141050e973eddea490dd8e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81347436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bddb1c2bb7017e0f733b6a4e2f3289887a8ad83139c50b176e731b3dd73d27d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236c5c0c495c4a10353d9b00113faf09c0f3979d092e03dc4c9d2bfc8a40b91b`  
		Last Modified: Tue, 02 Sep 2025 03:14:45 GMT  
		Size: 52.5 MB (52487196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3a4b8faa952c3929651cf6c526ccf6617c50f6eada50a3a8f03d18de0cecaf48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6cee657b46af0b85a7bdfe9e0007dcea535d717ad07840fd82caf65e19db415`

```dockerfile
```

-	Layers:
	-	`sha256:e5b59d4e14e440adbd597c79e5df087cd66c3324664472888e4a83a7e59904e5`  
		Last Modified: Tue, 02 Sep 2025 06:05:12 GMT  
		Size: 2.3 MB (2272067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cbe465ead904ea3308e165560f5141067846f2803cf761b0a4e57927ff2bb39`  
		Last Modified: Tue, 02 Sep 2025 06:05:13 GMT  
		Size: 10.4 KB (10427 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:07d75c1b4b515351dbe0daaae9cb24c0eeda7143b96279ef3ad4ade39cfe08c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 MB (88395125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0874abd740f44b91516f8b336c512d6427726a879a9a44640c96cf398d8a65a9`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:e2ae399c3aa36bf07b7d3562a21b9ad89f66ae6e03733ed0edcdcda5bd391c60 in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:403b01240f845337685ead3abfb0228bb1d1b78b076d609aa20f4733d260f58f`  
		Last Modified: Wed, 30 Jul 2025 11:30:48 GMT  
		Size: 34.3 MB (34329650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91fa73b53ab856dd65ecbfa46745606c6b58494bed9897c1a71376196b089e6`  
		Last Modified: Tue, 12 Aug 2025 22:56:48 GMT  
		Size: 54.1 MB (54065475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1fd950906c89e9bf02a355a127f71ed33fa4dc4fc3ce799dfb96ac13c8ba4aa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e23c7c49943a98eb60c0aa3bb8f276febce4422787c4ba76865a511dd81907b`

```dockerfile
```

-	Layers:
	-	`sha256:cc4a4b4818f0d79973332f19625d2310dd83cdf42bd2befce5114b8cf67dabfb`  
		Last Modified: Wed, 13 Aug 2025 00:05:32 GMT  
		Size: 2.3 MB (2269560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9af937bfab73ea5fe76265f76a6e7a974e4e3127f2147d3cd9e9b909b57e310d`  
		Last Modified: Wed, 13 Aug 2025 00:05:32 GMT  
		Size: 10.3 KB (10344 bytes)  
		MIME: application/vnd.in-toto+json
