## `sapmachine:jdk-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:ea10226d3331c69f9c73f64ca45ef6da329a1c76514c8719cb8b0a74694cf129
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:3bc23951358e8c4690ae3ed461b944623c42b41a476e281ce8596cb0b0ba9868
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.6 MB (250603732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff5fe1dc2c6259918278da241e394102cf3b152f690f165cff2db0acff6366d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:24:15 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:24:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Mar 2026 02:24:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80a47d6bea13c725ce18db32da8584c0cdd63276b86c70e443f050c49c3a058`  
		Last Modified: Tue, 17 Mar 2026 02:24:40 GMT  
		Size: 221.1 MB (221065212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:efdb76ebdedfc8cd1daa843d0ac23bf32e476a8747bba6a923add4728c1aa635
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2636862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a62f9657e84129a45893616c46fdd785d3d3abc72dbc15643786c3bf37e9df7`

```dockerfile
```

-	Layers:
	-	`sha256:c561687d3ddf8e3185eeb03c1b28c3d1cf991c28ee7e0b456563201aa765da7a`  
		Last Modified: Tue, 17 Mar 2026 02:24:35 GMT  
		Size: 2.6 MB (2624172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d03489a6d33aba60a23e2993fe06af87b8014a15524e45a858526fbfdb5892a`  
		Last Modified: Tue, 17 Mar 2026 02:24:35 GMT  
		Size: 12.7 KB (12690 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:f1a80b361035be97c5600623831697b0c458fb9cedb0cdaeaf6b7bf81c3b0e68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.2 MB (246220046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:169061f8a95a82d3e279de6dfbaa22338a4c6a23295f57df6eda05f71b26fcfe`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:48 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:48 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:50 GMT
ADD file:c702451b25bb6668fb3c759f7610e3f9399be20edb133c5855fd072ab2065456 in / 
# Tue, 24 Feb 2026 07:33:51 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:29:59 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:29:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Mar 2026 02:29:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e5060c94aa7453be0f9f82bbbe15bf13087740760371266cca7f76bac1ac9d`  
		Last Modified: Tue, 17 Mar 2026 02:30:23 GMT  
		Size: 218.8 MB (218831021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0d2b303d5b44baf1878cfef45c39d796a474f926d23bfd826fcaee9bf4e5e9bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2636933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f4df9585bb17803e4c7f22067207948cb88dd680fcaaaf0d12923e2755b77a4`

```dockerfile
```

-	Layers:
	-	`sha256:b186908c4a598e3deb5af21c7f71595dcb1e94f51fd3596fbfdb2048985e13f6`  
		Last Modified: Tue, 17 Mar 2026 02:30:18 GMT  
		Size: 2.6 MB (2623995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14cd6184a40bddfaf6ebf95d1d85a5e8a23d8e9ae23c8d11cd66b62d60a3f578`  
		Last Modified: Tue, 17 Mar 2026 02:30:18 GMT  
		Size: 12.9 KB (12938 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:bc7b5ef4257376fb7192d61a63723e54de07a438f755b20d7c45c8f277a17373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.3 MB (256318150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e87467c18dde75cc32d024d957b7d8cd1be20d319a02a836fe24d375da84716c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Feb 2026 17:41:33 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:41:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:41:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:41:33 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:41:39 GMT
ADD file:0418bf4995f9b54380cc1e509e3f7d65bb07aed9a367528d0b1084f0a34f3bf3 in / 
# Tue, 10 Feb 2026 17:41:39 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 21:22:36 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:22:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Feb 2026 21:22:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:95401e425d899946469007a0ce4b02622cf84a67cdd684aa25d61d472fffc38f`  
		Last Modified: Tue, 10 Feb 2026 18:13:52 GMT  
		Size: 34.4 MB (34446102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cb297e17ef9d98c6a02128ad93a4c1bbe833dff6e8d286b795f21d6183be5d`  
		Last Modified: Tue, 17 Feb 2026 21:23:26 GMT  
		Size: 221.9 MB (221872048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:097e92eafb43994e48e3b431705608df11f1647cd6f162676b9060ab3b0ba1eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2634018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e55ca63e9c17152d1766e8467daeb1156096846d612e08f9c58cb872bdff26c`

```dockerfile
```

-	Layers:
	-	`sha256:2b900d8b2ce4a988d8891fd30b559a8fa3acdf62fde90c1ff07c6e6a5cf0510f`  
		Last Modified: Tue, 17 Feb 2026 21:23:21 GMT  
		Size: 2.6 MB (2621212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca1fbdebeddb28af845374c0b01f0fa0343e62a3592c7a658a3aaf1a4f1ed1b5`  
		Last Modified: Tue, 17 Feb 2026 21:23:20 GMT  
		Size: 12.8 KB (12806 bytes)  
		MIME: application/vnd.in-toto+json
