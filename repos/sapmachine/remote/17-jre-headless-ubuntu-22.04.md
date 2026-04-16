## `sapmachine:17-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:88515ad4f9a2fa5245bee77c0f9500bba22f236ce77ed95b7b2d84267e220c9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:b3df6a0b2bc529b80c1fc42a879c5a8804b81ca8695c8102a9b1f0ce996c3daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82894880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db11474cf4b0b5bbf719fcaa93fac067ac4ed08fccd4a6c8d7653f12f93e5cad`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:00:34 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:00:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 15 Apr 2026 21:00:34 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf5a8f81b0cb4f998ba7b761c9306f852267ab508097c4c420eb0cfb2bb88dd`  
		Last Modified: Wed, 15 Apr 2026 21:01:00 GMT  
		Size: 53.2 MB (53158382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b9866001d64b62e6c9d712535fc7122dba8387255f4dd890ad1a8342839e941d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37845c2b0ac53a1860a83f0e29c0346a90e9c8aab332128778e892ea679bfa15`

```dockerfile
```

-	Layers:
	-	`sha256:58d58f8d91e0ae44d92e1cc0cdab17e4541c5e871624d179a646ad22ea8a18b4`  
		Last Modified: Wed, 15 Apr 2026 21:00:46 GMT  
		Size: 2.3 MB (2295247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84a918f8d28d0e5c0965ed3efe3dff597627c49d14895a0d9211c3575ccb2145`  
		Last Modified: Wed, 15 Apr 2026 21:00:46 GMT  
		Size: 8.9 KB (8885 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:17bd9440de36aa3129f56f319ef9d08b5bdb983454e5bea56296e3fcbc2cd468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.2 MB (80166623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:338ddf3cda02c1d813e901dd7e6361e21cb015b6d2f84b572a95cd6e9f73cc8f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:11:18 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:11:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 15 Apr 2026 21:11:18 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64f7a49e00f717038b5f3b548fac4eeedfb79082bee0bdca3728f3c64f0d65a`  
		Last Modified: Wed, 15 Apr 2026 21:11:32 GMT  
		Size: 52.6 MB (52560080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:648ebe7f49217c7f6e681bc18a58c0dede8836fc94d364ec5b8ffb3ac45ad3e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06e952579c7bcf14337f215ae1e985ff82c0ea95ba216006701cc8ff5ccaf777`

```dockerfile
```

-	Layers:
	-	`sha256:5ac58bd316e23f8a13725b45d9f45d18c0f93177ca8f9d663d18ad803ec300c5`  
		Last Modified: Wed, 15 Apr 2026 21:11:30 GMT  
		Size: 2.3 MB (2294919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:407ece272633a1acef41672e0dbabbbf47ea7e3ac8fa4ac0c69718b71da7df09`  
		Last Modified: Wed, 15 Apr 2026 21:11:30 GMT  
		Size: 9.0 KB (8989 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b382691f947092601e6e3824d9822ca5800fafe84fbac2be1c97541a6d3a3307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88816013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a41c78986ec3533d5cd319eff6a7a9dc7ae5cca14aea8e7ec0de77b164880b19`
-	Default Command: `["bash"]`

```dockerfile
# Sun, 22 Mar 2026 18:11:34 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:11:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:11:34 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:11:37 GMT
ADD file:268be611d24f69c3d8e480314cd587652e4c89a6032236737057c8b64f2379da in / 
# Sun, 22 Mar 2026 18:11:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:53:21 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.18 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 01 Apr 2026 20:53:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 01 Apr 2026 20:53:21 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6fb1b04a0a70d070de8a04181c7b855a46b1ea4f771660ae7f0783acd4569be2`  
		Last Modified: Sun, 22 Mar 2026 18:43:46 GMT  
		Size: 34.6 MB (34649660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0b85fa7a91b6ac1d1efd2129eabb94576e5b975618183f35ae209f4dc126c7`  
		Last Modified: Wed, 01 Apr 2026 20:53:45 GMT  
		Size: 54.2 MB (54166353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2d45862fcfe84401a9d738bd591fd255c2cbc449bc2a33af153142a24e1a6894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2303618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51fe7838d65841fd9312d80d8ee3357661a2c1f6a51141f84d3e3b3fd00799a9`

```dockerfile
```

-	Layers:
	-	`sha256:4420365ed81524cf8541e23acf306d52662fc6b7c5fd87a0eee23e0ccf9d6afb`  
		Last Modified: Wed, 01 Apr 2026 20:53:44 GMT  
		Size: 2.3 MB (2294689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dac05863383a18059638361412428f2c4f3d3adc7004d670f68290736667194`  
		Last Modified: Wed, 01 Apr 2026 20:53:43 GMT  
		Size: 8.9 KB (8929 bytes)  
		MIME: application/vnd.in-toto+json
