## `sapmachine:jre`

```console
$ docker pull sapmachine@sha256:d4b31e9f2e736b3df9b267583c77e7bb48b088d9628eae6be76126ef9b4be413
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre` - linux; amd64

```console
$ docker pull sapmachine@sha256:8f22ee91a3db6745eab3b35f924911c1c9bb5c8903177d881723b3975cc5cc6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86999847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de067f4f14a4212459abbeb28303c55d14234ed5890dde3507e20bbb5db3610b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:37:21 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 13 Nov 2025 23:37:21 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf25bf564cd2f219b1cae805d9fa9825ca39c0d6fef355f352ee07c565936da`  
		Last Modified: Thu, 13 Nov 2025 23:37:44 GMT  
		Size: 57.3 MB (57275159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bb95ad8d4cda83e92b044f2cb5c456bdc2960367e972397f834a716af3822a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2538317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ef883d724be415461f8d6d29082607bebc24db6e9c432c737dfb3fc52d125a1`

```dockerfile
```

-	Layers:
	-	`sha256:c3c790b826c4b9eb4cf0e973bbb8db563f877c88e3379173e63070b3ece5372f`  
		Last Modified: Fri, 14 Nov 2025 01:13:11 GMT  
		Size: 2.5 MB (2526024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b34dd8db711e94399b992e9085583f506adfabd2b29620b41701eb8450bc9c9b`  
		Last Modified: Fri, 14 Nov 2025 01:13:12 GMT  
		Size: 12.3 KB (12293 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:58b76a66815531e89a76d33cd91571d21f2d55408c3a1b3581ff61a3a5365b08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.1 MB (85079591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae8aba91e36976e31968a4d627f13e9d2b0255470da6c53e691f72c9a76395cf`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:36 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 13 Nov 2025 23:36:36 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5573a585510ded13aad9c2ea9670c858064c4ac891271e3e41babc8d5fa0f26`  
		Last Modified: Thu, 13 Nov 2025 23:37:07 GMT  
		Size: 56.2 MB (56217634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3765aea39242dc17105b77e186398629a7a123df9f72a5d67e9c12d82d09714a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2539150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af6aa26553908501b2b5f3d36eb6864fe72fadf2cec3e0eebb601063a803800a`

```dockerfile
```

-	Layers:
	-	`sha256:2b8292e3da933df5c831048f078992365093c1bbec79f195343fb107f13e2b5c`  
		Last Modified: Fri, 14 Nov 2025 01:13:16 GMT  
		Size: 2.5 MB (2526621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f364f137b44d88f0fc3d5f8241c0c201738890e2cc8fea9beafaee06c96897d`  
		Last Modified: Fri, 14 Nov 2025 01:13:17 GMT  
		Size: 12.5 KB (12529 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c83c3228eb6ffc5e867f21fbd417a916455151b1a7cca470a8d3319b98a2cbe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92487049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccaf4e657d3eb9b001b8da8e8605481283215e0ae883823a2b47ccaac069a278`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:25:20 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:25:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:25:20 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:25:23 GMT
ADD file:33eacf94519a8a8195b8465116ad15d91df7bc9e43d9609157043b3b8b8f7588 in / 
# Thu, 16 Oct 2025 19:25:24 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 01:13:54 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:13:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Fri, 14 Nov 2025 01:13:54 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:d63f81c8011c079a4b917f15cc5c547103c6dee1be455ff6ecd1f2c1f5af0055`  
		Last Modified: Thu, 16 Oct 2025 22:53:24 GMT  
		Size: 34.3 MB (34304424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7217b1909e78a6727acba0c771047bd0927bcaa4d8966f998a8be7f3d259eb7d`  
		Last Modified: Fri, 14 Nov 2025 01:14:35 GMT  
		Size: 58.2 MB (58182625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f6e6437d53bfb681d9373fe9b8d045e9d68748aff8249fccb90c278b7da1ed8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2535920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5faf0cb0cb95a044597a37ebe31b62804182b907af39056e4acc05b19f0facf5`

```dockerfile
```

-	Layers:
	-	`sha256:d87e6b24132f1e1986fe0508331ae2923614a5d0e9a1bcdc1c8b70c330bba2f7`  
		Last Modified: Fri, 14 Nov 2025 04:10:55 GMT  
		Size: 2.5 MB (2523517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6b31a82146e496d0fa264a118d0027a959f8f8caad09fe46e5453f08362d522`  
		Last Modified: Fri, 14 Nov 2025 04:10:56 GMT  
		Size: 12.4 KB (12403 bytes)  
		MIME: application/vnd.in-toto+json
