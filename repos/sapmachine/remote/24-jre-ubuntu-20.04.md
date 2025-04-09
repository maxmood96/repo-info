## `sapmachine:24-jre-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:eab0b2453890c614be4f26d75e361a3e77ef9c087bc85fb785b3aa31749da812
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-jre-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:e74622bd4152bb6967c8966fe6ea61af2577f90c6df154e57e8d5662d36d0f98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94720120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1783ecc35432fced9e888dc99ea8f67dff7fcf3c880021ced46cfcdd3ad33c55`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f469347b3520ed621aa82537dcdfd65319bbcc73f92a8f0e4ae6db5facd6c9`  
		Last Modified: Wed, 09 Apr 2025 01:20:39 GMT  
		Size: 67.2 MB (67209726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5795d49ddec341a764a73c076ad24bc8ff7dab95557d54cbba4f3c8c84339026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2316337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9149baebf67a014994d7786d51f5803a1c1536df246265450b8d4e3aab1b1b`

```dockerfile
```

-	Layers:
	-	`sha256:e0022836507902f4af89d8075410e8a8d5631105dcd45050636efb7e6d1b08ec`  
		Last Modified: Wed, 09 Apr 2025 01:20:38 GMT  
		Size: 2.3 MB (2307561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9afe0e7393d99553165a6586631700bc8900454755ae8932053a3c4dba318bac`  
		Last Modified: Wed, 09 Apr 2025 01:20:38 GMT  
		Size: 8.8 KB (8776 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jre-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:cc4b5a2e6263fa447f012b51cb8479fba0913392b08f18252d3dcf2b5f1cc2cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 MB (92219869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d241671605742999121cbdfdbd80948c4b7fe1dd2a8c0fe5b126086abea77faf`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338c1abbd0a316b8f745ce6d34886ef69dad9b854660d25865af593887344fe2`  
		Last Modified: Wed, 09 Apr 2025 09:27:26 GMT  
		Size: 66.2 MB (66242208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5a7e750990ef0372bfcf6a172ee854a1997ba8b7aa3ec7b68918792a96eafdc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2316076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46aacd496bd6bdb8199075a69c7b0b8e396c08bfa86e360cb5547b611f546eda`

```dockerfile
```

-	Layers:
	-	`sha256:39b15b6d2f22315e807c0ba470e80d906ee4cb8cc705cd9f9ecb64cf4ddc6859`  
		Last Modified: Wed, 09 Apr 2025 09:27:24 GMT  
		Size: 2.3 MB (2307196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9641bba306e096f819eb8d5605df8b1b737dd7e1d6697c59fc54d7aade77e855`  
		Last Modified: Wed, 09 Apr 2025 09:27:24 GMT  
		Size: 8.9 KB (8880 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jre-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:32c4f9a1e7755e4be7ae78db78b61816fad9358b66d23c1ccb0a3600c634ade6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.2 MB (100183520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90310c443fdfab672935c7ee34b7f8474c4ff08efcc77171dba3562ad0f92d10`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:d85970cec61787609e3854cb76ce16d54fe420b254cf48fc9ed9ed678717ff28 in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:92d54367a68b4f03400315732acb4290d88bb06f8fe1414fd823f93402bec922`  
		Last Modified: Tue, 08 Apr 2025 11:48:44 GMT  
		Size: 32.1 MB (32076946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3411a6bd7f4c5f582abf412eb2f1bd379d1529b1ba0ae0aee427a92432838915`  
		Last Modified: Wed, 09 Apr 2025 06:48:42 GMT  
		Size: 68.1 MB (68106574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2092e4d8e14683f33e6a2e30ae7326bf68f670f2faa67bf7ec5035bd43ee7909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2319518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9efdfe0fde0b0899d86f0369a290c76b52c0a36488abbb8228078e77218e141`

```dockerfile
```

-	Layers:
	-	`sha256:105f97a87f3eb0644cef03ab9ab2604edae17967a744179d2a4221914c97d194`  
		Last Modified: Wed, 09 Apr 2025 06:48:39 GMT  
		Size: 2.3 MB (2310698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8420afef0c0dac741d4796a06a8b73d31a18d67b9b7523d13cf986466505036e`  
		Last Modified: Wed, 09 Apr 2025 06:48:39 GMT  
		Size: 8.8 KB (8820 bytes)  
		MIME: application/vnd.in-toto+json
