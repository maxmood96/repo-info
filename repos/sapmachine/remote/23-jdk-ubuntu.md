## `sapmachine:23-jdk-ubuntu`

```console
$ docker pull sapmachine@sha256:8abcc3bfadef48cccef938f88668eea63097dbe2eaaa81da3709ab6efd4ab7d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:23-jdk-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:86021d5b27c1e11b70203021316ae89c3a2133f244b37357b752c30db705d1fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254337257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6b9c7ce05fd36a0208727e1d649f555eaf7bc5a0b04c4cd3c23d3af03546dd`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:01 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:01 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:03 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Tue, 27 Aug 2024 15:55:03 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1baf59cbb5f7fe73ad3704659822d073eb4a084f085393c77db568fae236db78`  
		Last Modified: Fri, 20 Sep 2024 16:57:48 GMT  
		Size: 224.6 MB (224587429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a2c5ff49e1290f7dffc02bf6d6ee5d716adca86190934198592187e33432b450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 KB (15925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c39d00a64d5f1c158dc13231198b8e88dc49b3d22d182a19a78919b34c24c0`

```dockerfile
```

-	Layers:
	-	`sha256:eff016a0a0933670c4f609f8f2fd62367b537d0522df516e961b405c59d600ff`  
		Last Modified: Fri, 20 Sep 2024 16:57:45 GMT  
		Size: 4.9 KB (4881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:020febb26917e043df939d75e36b4b28663ab5184f1bf7bc7b9dde390403628e`  
		Last Modified: Fri, 20 Sep 2024 16:57:45 GMT  
		Size: 11.0 KB (11044 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jdk-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:9d2da179fafea6f50a5d7cf416b59913fedf0f6065926b86d0f16eb1998720d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.3 MB (251277342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11c6c36ab26b5a55ddb7715d44564b2d8bbb343fd69aec29c2df9f316c40bb5d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 27 Aug 2024 15:55:18 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:55:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:55:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:55:18 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:55:20 GMT
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
# Tue, 27 Aug 2024 15:55:20 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e59cb05818e49ea83cbe79bd46eb80418dfe3cb3735b45570f93a23579e2cec`  
		Last Modified: Tue, 27 Aug 2024 17:08:12 GMT  
		Size: 28.9 MB (28885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28f173ff1220f93db1355508dcc09dae69d2a4f7d0285af88a7068f5f0aef42`  
		Last Modified: Fri, 20 Sep 2024 17:01:01 GMT  
		Size: 222.4 MB (222391743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9f97713af08714099709368954dcf578685d64571a99059f60a70af1bc4669b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2463450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6596178c065023a90a9d1588b2cfa728f8f5db139c6936dd8134d00ef8bc2189`

```dockerfile
```

-	Layers:
	-	`sha256:f301ff439501a19f6af9fa6705d211958db10f3a39a94109903046290c4a54fd`  
		Last Modified: Fri, 20 Sep 2024 17:00:57 GMT  
		Size: 2.5 MB (2452008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd060955ea9db7a921ac72d692da6b9d028cda32051e2084b1a04852b67c884e`  
		Last Modified: Fri, 20 Sep 2024 17:00:56 GMT  
		Size: 11.4 KB (11442 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jdk-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:479e7cbb26ca5e091b6b11e37cc846296ceabe24c8187c1230c8f87e10807b33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260304798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97919bff9ec34960f6b76bdca3de7dddbb8204ebe9ec96cfd0ca5672d2636858`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 27 Aug 2024 15:56:25 GMT
ARG RELEASE
# Tue, 27 Aug 2024 15:56:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 27 Aug 2024 15:56:25 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 27 Aug 2024 15:56:28 GMT
ADD file:c70c2393dc0404f71d25ae70ab08b5aa65e46753a6169cfd4f5554c942cc0218 in / 
# Tue, 27 Aug 2024 15:56:29 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c526398e5e771684dae49961d5a74cd9606dcbcf7ddafb1fcc1433293927dca4`  
		Last Modified: Tue, 27 Aug 2024 17:08:24 GMT  
		Size: 34.4 MB (34392345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da4fb3575ed0629644d29aff519f200e70511b807dad2326e9fc629a13825d4`  
		Last Modified: Fri, 20 Sep 2024 16:58:49 GMT  
		Size: 225.9 MB (225912453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jdk-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5dee507abcd975288b6de172b61665e38d31d077e943d49d14d3ed6a4df68d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6790ea4b0f1b31c1b58c9827613b83cb59e93d72174874b6534f72cc539b511`

```dockerfile
```

-	Layers:
	-	`sha256:5c58e0b8c55fe1b786799d48baf24ff0d80b49238511b340ce938197cdc5bcf2`  
		Last Modified: Fri, 20 Sep 2024 16:58:40 GMT  
		Size: 2.5 MB (2453493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e08aa81768be587fe7cb608185be1a61bae9182d9bd5ec54db34855f3f410b3`  
		Last Modified: Fri, 20 Sep 2024 16:58:40 GMT  
		Size: 11.1 KB (11131 bytes)  
		MIME: application/vnd.in-toto+json
