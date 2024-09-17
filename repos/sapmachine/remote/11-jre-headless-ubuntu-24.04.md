## `sapmachine:11-jre-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:f491a55619a68118b29d4da0ea4372edd208f7a8e7477cded7f13309bf17499b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:12649a1fa1b0beae862840e7dfd7712bf94501f851342ced87dd0e8435b5425b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81293672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa0aef960a182d1ca0edde220e8e7384deddaae31cba07753f69c8e5a9092db9`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9139692b751a41dd87eb250118459ddd519f3be094ee73477a4493dfa3df5966`  
		Last Modified: Tue, 17 Sep 2024 01:00:45 GMT  
		Size: 51.5 MB (51543844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e6b8337d2fb8a9bfa1f671ba88a61e13f498b5bd81940016b9dfed6ca3a6d091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2148094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ed2cdde50333481fc4f1a21b7cb80299274168129b0c271a07c9ded619ff95`

```dockerfile
```

-	Layers:
	-	`sha256:99b4a9e2002eef7907e606c3c57bf7c22c5c359f8ff9b726adc384da4d902e8e`  
		Last Modified: Tue, 17 Sep 2024 01:00:44 GMT  
		Size: 2.1 MB (2138730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:937d2692b78b3ab903cb92b8c420cc13e7852309028160cdcff93a721b6555b5`  
		Last Modified: Tue, 17 Sep 2024 01:00:43 GMT  
		Size: 9.4 KB (9364 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:4990fef7f73444ae2adc80a1b7c59eb5b7d839e1d45928c6174e1c7400ec5a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.3 MB (77324912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd636724c8caaeb8e1b2418bec26d81f240520084d7c3a2e6f5edd5349ea188`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9f23a71f1e313efedd46a7ba220354d3a6eb7196085ef28ddab1b7f266cb0666`  
		Last Modified: Thu, 01 Aug 2024 15:42:17 GMT  
		Size: 28.8 MB (28843686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2040a69b8843c5908910868a5f00703ff83b48c46adf1e3a4f765e3005403b57`  
		Last Modified: Sat, 17 Aug 2024 04:44:21 GMT  
		Size: 48.5 MB (48481226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f72c155d05d54eb6e623799118dea16d461836f3a2b9325d863783da120f1aa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2146969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f82d9c2e0ec099bef4b4b795bde5c324ac1be364fcc01d0916d8525c5e21374`

```dockerfile
```

-	Layers:
	-	`sha256:dd57435ca8b9c9d3a0251708c3775606794f464a20ff6cd762606aa0bf26b879`  
		Last Modified: Sat, 17 Aug 2024 04:44:20 GMT  
		Size: 2.1 MB (2137282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8481b7c4822e85d1a929af5408d5928513772c2bef9a699700151c1e60de64c2`  
		Last Modified: Sat, 17 Aug 2024 04:44:20 GMT  
		Size: 9.7 KB (9687 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:d34dd7643c4315e800b36783398435011d9608aae9744537c8f92afacb1c8724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.7 MB (84734850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c95b0be1bbb61fdfd3da45535aa30810688e23b24976eb9e437217b94c3424`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:c70c2393dc0404f71d25ae70ab08b5aa65e46753a6169cfd4f5554c942cc0218 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c526398e5e771684dae49961d5a74cd9606dcbcf7ddafb1fcc1433293927dca4`  
		Last Modified: Tue, 27 Aug 2024 17:08:24 GMT  
		Size: 34.4 MB (34392345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa68a90ec349ba344ec83212ceb627a402a61af3820f2aca5f8462080df966d`  
		Last Modified: Tue, 17 Sep 2024 03:03:46 GMT  
		Size: 50.3 MB (50342505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8ad8626ec830c0d9b62016344a255aa95e59e8819cfbd2771c8a405c6c2f2667
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2152036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89cf05a717868be4f64367a848175ca2b5615545f54385830ad06a36839f65ac`

```dockerfile
```

-	Layers:
	-	`sha256:ac0d66a46998e29ac3daa516b8aed2063b233d9c2827f3d02a5f5b5c724c55e9`  
		Last Modified: Tue, 17 Sep 2024 03:03:45 GMT  
		Size: 2.1 MB (2142622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:146c2fd1a7821b7c5f53f0a69cda50285f18b6cc076fa4a2690171e884ace5c3`  
		Last Modified: Tue, 17 Sep 2024 03:03:44 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.in-toto+json
