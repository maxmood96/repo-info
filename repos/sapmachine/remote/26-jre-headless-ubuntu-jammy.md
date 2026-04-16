## `sapmachine:26-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:a305b4c872fcce0bd58060c7e0c4f0fb9e936f50a8b3a1d924ca196e7bf45a87
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:26-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:b5344b05aa0fd521eb6b7999c3f4e7282a30c16098cac1642a49e7285b41ce57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87130048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9af3c6a4fbadcffa5cd789b825dc7b2bc4714d0afc9f67e52b073a0bc725d9dc`
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
# Wed, 15 Apr 2026 20:57:34 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 20:57:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 15 Apr 2026 20:57:34 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d125a6cfae5f5061a762adbf62071323a95bf35d19742bdd6a4bcf7c40f604bc`  
		Last Modified: Wed, 15 Apr 2026 20:57:49 GMT  
		Size: 57.4 MB (57393550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:41a8883d66f79f66b23349489e171117194414aa1cb4af80c4a90fbb00dbe8a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2309183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c990faacfbe4abbc688a436a89c7eeee004c2e11df4cc5f54229e65bed4d058e`

```dockerfile
```

-	Layers:
	-	`sha256:7f2fd9e9650def530b248b238833d5574be123af63b939497dd11873928c23bc`  
		Last Modified: Wed, 15 Apr 2026 20:57:47 GMT  
		Size: 2.3 MB (2300343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3bc9011f1658efe492635398aabc7cc98249650c8f78ac8fa4287274d8eca9b`  
		Last Modified: Wed, 15 Apr 2026 20:57:47 GMT  
		Size: 8.8 KB (8840 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:39ba5f9b042d769c771994e2405c045eae2430356eb4a438ea8b2484dbd2fc6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.0 MB (83973345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ef7aa66e767713979af331a75f97648fcdca08b7cdcb83dfe274abbacbec3cf`
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
# Wed, 15 Apr 2026 21:07:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:07:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 15 Apr 2026 21:07:06 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8205e5b21d162bac5d15862f6c67ab17113711b3835049f6abf84099003ab25b`  
		Last Modified: Wed, 15 Apr 2026 21:07:20 GMT  
		Size: 56.4 MB (56366802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:dd35493b44a697effc727e6ad4129dcd397d9a865eaf6a8698ba3aa9be18aeeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8869f936ae0fc823cb2a867dd63830756c34209b8da44fd9f8798aa58c70fddc`

```dockerfile
```

-	Layers:
	-	`sha256:203c10e8e6c584621ba9228d40e3b84bac2ff38e3d84ad31b95c334299ca9c6e`  
		Last Modified: Wed, 15 Apr 2026 21:07:18 GMT  
		Size: 2.3 MB (2300012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdce6078d6ba485f3cd4e4231435cc6146f40f9bf5246400fe5f0adb36796558`  
		Last Modified: Wed, 15 Apr 2026 21:07:18 GMT  
		Size: 8.9 KB (8944 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:0497c973be166375a7faef4f7ceff34f53f06a6369c7ea1238ab5588157e9d6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.9 MB (92938321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bca5ba6bd3aba837f2774cee02a3947dfed74a61af43b07a53252c098505e58`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 23:25:34 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre-headless=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 23:25:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 15 Apr 2026 23:25:34 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab18b7aaea8a13162975c3329615ff5d9e70f2f0fd13a8e0251b247a9e882c43`  
		Last Modified: Wed, 15 Apr 2026 23:26:03 GMT  
		Size: 58.3 MB (58289923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1c477aeacf0c9739492b22537e1aae97c23b87408b04461c1f8216bf982a0773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36710fd588d108c0b265e0454791902d9df8ad1704116a085b9239399cfd3f15`

```dockerfile
```

-	Layers:
	-	`sha256:fe879b652b0f2fedd78cb1034a9c0e92cd748829090b0f539c5b83908e0a2efa`  
		Last Modified: Wed, 15 Apr 2026 23:26:01 GMT  
		Size: 2.3 MB (2299155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a9f4e3205449bfb09ec001c7b5753213ec2699337d23b593ed12d8ec4102679`  
		Last Modified: Wed, 15 Apr 2026 23:26:01 GMT  
		Size: 8.9 KB (8884 bytes)  
		MIME: application/vnd.in-toto+json
