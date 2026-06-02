## `sapmachine:21-jre-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:01090b28346c13cf92e63a82c47f1c842310058d8e9a5d61fb680574448f8e01
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:7b0b4518fe92363a30535cff64572aa4f72c7b48b158acbc404e2d84cabc7567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.4 MB (89386277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c36d1a8a229fd2dd61930b48a1a30d9ed496fef3a5d9e3c0cfb3ddfccbcc2570`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:19 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:19 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:21 GMT
ADD file:46ac5b8ee4c64ad9ebe840abd5619f571a617ac19483764d47d0eeba7907934f in / 
# Wed, 20 May 2026 01:37:22 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:24:42 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.11 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:24:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 02 Jun 2026 08:24:42 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:cb259a83ac3dd9fea0b394df41df2b298adf0df938fef5999475af18a751c257`  
		Last Modified: Wed, 20 May 2026 02:15:22 GMT  
		Size: 29.7 MB (29732805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301aef322eee7c1aed281e799234d0dd408e3c77334527ec8bce9a6ba88ccf85`  
		Last Modified: Tue, 02 Jun 2026 08:24:55 GMT  
		Size: 59.7 MB (59653472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b39b3af13dca959ea2b038ccf73849af6b5d0e41c6f254e72e1a1b02f46a0424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b47a05644937a9c790f1e83be51935b1f7b28f6886a2793daf95dc4e1d4fab`

```dockerfile
```

-	Layers:
	-	`sha256:1b09c2dcf4df2647bd3237be6fa2799cbf2c247f6518b618e660081ebeace83d`  
		Last Modified: Tue, 02 Jun 2026 08:24:53 GMT  
		Size: 2.3 MB (2275890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a4d533ada6152c44f9f75e93362fedc942075bd6eca7847083fff68e04e33c8`  
		Last Modified: Tue, 02 Jun 2026 08:24:53 GMT  
		Size: 10.2 KB (10229 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:6d5126f5b55433a43d235c009f03b86088e83904c01af420e7af3275a7028ac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87722710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4ef58d3211a1bca3b323e3ab4059cfebd2696277726d6944e644d185a89002`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:31 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:31 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:34 GMT
ADD file:08e1f650999ca51d9b63c782d658d9485c64263966d69dc423a3b64a16449f00 in / 
# Wed, 20 May 2026 01:37:34 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:25:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.11 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:25:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 02 Jun 2026 08:25:16 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:fff3795b437199a0b714aadba6fb2c251d7da853c3e257d3fed1d2c8d0f05158`  
		Last Modified: Wed, 20 May 2026 02:15:29 GMT  
		Size: 28.9 MB (28876406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e158542578167eef8fc916be925e2e778a95ef91bcf7bee3eb79bcf5059bd0`  
		Last Modified: Tue, 02 Jun 2026 08:25:29 GMT  
		Size: 58.8 MB (58846304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bc5a9a8ceb3cacad44512c0fc7ce62f63654866bba090202796b05fde35a8bdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2286778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2b62d710c6d3b0478bd9f7e8032d784df1d03fdb0635f48dcba8354a4d20e3d`

```dockerfile
```

-	Layers:
	-	`sha256:a42568847713dce401ed73ccc329056b2da603989841f573d25a20dc12d6e33d`  
		Last Modified: Tue, 02 Jun 2026 08:25:27 GMT  
		Size: 2.3 MB (2276397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:811cb7b776c0ea0bcfe6621d87dbcaa9af96cc0e23aa48791c9a48032216ad2e`  
		Last Modified: Tue, 02 Jun 2026 08:25:27 GMT  
		Size: 10.4 KB (10381 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:7a2e86a925e553f645653242d5c020d3f7c836f0b8f42f76791afab9e3062ae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.1 MB (95096038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb028bb362bb298ae35bc000c0abe78a4b81175ee97f88b9695aed3fb2e5b45`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 May 2026 01:37:26 GMT
ARG RELEASE
# Wed, 20 May 2026 01:37:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 20 May 2026 01:37:26 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 20 May 2026 01:37:29 GMT
ADD file:25dad72762cb0d82bbf57f17b8713b1ca4d35e813d99be37e61090f10acd5d92 in / 
# Wed, 20 May 2026 01:37:30 GMT
CMD ["/bin/bash"]
# Tue, 02 Jun 2026 08:59:45 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.11 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 08:59:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 02 Jun 2026 08:59:45 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:e091f822489caa06bb3d2fde38646b1d65be890bc1155c44ed55dc18ce539afc`  
		Last Modified: Wed, 20 May 2026 02:15:44 GMT  
		Size: 34.3 MB (34314099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cdaa5f7baa3ad6d0cbe3e6e1ef251ec5e1bc7b9e6d5dcd2a048c50ca17ab456`  
		Last Modified: Tue, 02 Jun 2026 09:00:15 GMT  
		Size: 60.8 MB (60781939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:78e0b9fa90dc6d75e6da0c904d2235fd71e910e94deb6a8ea92e40bb7cea1f70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06652750c695ab45cd861b6bbb914f1337165dcfeddc533c219fb6a0d896f3ed`

```dockerfile
```

-	Layers:
	-	`sha256:cdfabff936a670bfe18d2f98cf5d9f18e12637efa9adec6bbeceb85949f08746`  
		Last Modified: Tue, 02 Jun 2026 09:00:13 GMT  
		Size: 2.3 MB (2275307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01336798cc2bf8ef257b8216dd4d83af2d3fbd85bf3b3c37d2765d63530083e9`  
		Last Modified: Tue, 02 Jun 2026 09:00:14 GMT  
		Size: 10.3 KB (10297 bytes)  
		MIME: application/vnd.in-toto+json
