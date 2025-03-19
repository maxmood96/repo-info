## `sapmachine:jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:d0a9fc08afa64e02384bc7336905278d5bef80e2a9f955e9aeca9068abf974e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:b5a3d57ab82d9d3af14bf3701638b4ccc0e859ed16ed703fb11450b72a61a40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97195369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31adc6bbfa37e2713397d3bd9ca0ceadd2d2867306c88457578268c614b5c2d7`
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
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63aa0de9f56ab98718f5a03d741c02fc0004b360866a783ec33de2d442b28de`  
		Last Modified: Wed, 19 Mar 2025 20:32:55 GMT  
		Size: 67.7 MB (67659428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3a2c2c25bc70908a3a8a7c5d5d84da186fa7e2c290a465c08e99fe6b6d9356d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2424366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec44b9e743aeef691d91472e90837f34d46aec96bef24e042b5394838ced89b6`

```dockerfile
```

-	Layers:
	-	`sha256:22b5d5f11f5f46597690c9ebdfb9c5ee7165cc996ae9db00d0a19a2c94dd1580`  
		Last Modified: Wed, 19 Mar 2025 20:32:53 GMT  
		Size: 2.4 MB (2415590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:715ad50fbb6ee3b78f6f650f22a21638334c304c4f5fb16965b38d50adfdaca5`  
		Last Modified: Wed, 19 Mar 2025 20:32:53 GMT  
		Size: 8.8 KB (8776 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:65b1f6ce600c5aee75cb661c3c746145c5f0af031c02381ac826893523ccf9cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94025601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af21db30fae4da56ade64f830f42425a3a2bc68b3e0694d5009c2599eab8b2d`
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
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:8493f821c8fdba445b33d07c091a4264a2684d16ec118ab034e9472d9baea288`  
		Last Modified: Wed, 19 Mar 2025 20:38:36 GMT  
		Size: 66.7 MB (66667419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c1c2c1302fde91765cfbc43e885575eec895559e2174b391074c70b0abbdd1a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2424149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2611506095dcfa5d4696f9d746cbef1434a8457cae8bf938ebeed09499feb165`

```dockerfile
```

-	Layers:
	-	`sha256:0eca796af91d2217ff9836b0f40eb7e9a8c4a9231bb491bfa3b833beef9bdd9a`  
		Last Modified: Wed, 19 Mar 2025 20:38:33 GMT  
		Size: 2.4 MB (2415269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30a88e18a325c3ce60bba7a724d772b85a0dd84955ae8e4bb6ed808dbfc9f234`  
		Last Modified: Wed, 19 Mar 2025 20:38:33 GMT  
		Size: 8.9 KB (8880 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c102f8316f783615b6489bb9f8fcae71a5daf333fb66d5d0653f10c98c4b4bde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.4 MB (103385127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4748dde25c0d66525dede94f1b1f0f4a298b9705a04876d80eade5f70079ddf`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:49 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:54 GMT
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
# Sun, 26 Jan 2025 05:31:54 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f89a8a9c984eed9b1edb40775528fe6ee08965088928c8a53ffb43fb752bf1`  
		Last Modified: Wed, 19 Mar 2025 20:42:24 GMT  
		Size: 68.9 MB (68937192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ff4a25cf24a561731d70bbe134b3bda3ec8f823369df4997d1e3b80625cf2dde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2427761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acd3f694187ffead8822ca2501c9a6bef4dd8340056c187b655b2a6e68f41cfb`

```dockerfile
```

-	Layers:
	-	`sha256:910df76f718d58bcdbdc6450fe14ceedc9fbb0749214faf6b9886e810703539d`  
		Last Modified: Wed, 19 Mar 2025 20:42:22 GMT  
		Size: 2.4 MB (2418941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7c42d1bc658ddab7063d3ea05641f0f1ec8ec697d683449cac82a8de9249904`  
		Last Modified: Wed, 19 Mar 2025 20:42:21 GMT  
		Size: 8.8 KB (8820 bytes)  
		MIME: application/vnd.in-toto+json
