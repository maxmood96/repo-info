## `sapmachine:26-jdk`

```console
$ docker pull sapmachine@sha256:4973ac701de58c90e5be140c96dd4ac021babc08ad922288ae8c089099626bb1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:26-jdk` - linux; amd64

```console
$ docker pull sapmachine@sha256:426d30654c3a2e049440d62defa2047df5f9ae1ab467add5a72016f0e997ef84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.1 MB (256090314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a88592ec05bdb62866ab3cc7ea85a8f1586ea21bfdcd649eae9e04521ddcd23`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Wed, 18 Mar 2026 17:49:49 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Mar 2026 17:49:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 18 Mar 2026 17:49:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1545a05810439b60afd98dbebc8ca1f0088a067cd30da0424d1a924fe43923f`  
		Last Modified: Wed, 18 Mar 2026 17:50:11 GMT  
		Size: 226.4 MB (226358321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jdk` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d011f1daa5867d6ca20238664f0d10b583ff701691d92f7c2d8a1341d53cdcab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2607038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c699611e1bb16a729262b681e72ac7fd79de773e02df52bb7114cf8252d82e`

```dockerfile
```

-	Layers:
	-	`sha256:c9ec028d92a0b8f5ef477e168be05bb95ab6b204bebdd95b6f0cd6e87796119b`  
		Last Modified: Wed, 18 Mar 2026 17:50:07 GMT  
		Size: 2.6 MB (2594558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0848a4ee22053bc679aaccda9319900e4c884d96905394dc0429a6d2fccba5c1`  
		Last Modified: Wed, 18 Mar 2026 17:50:07 GMT  
		Size: 12.5 KB (12480 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jdk` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:90de619cde3dc51d0ffce996ccb49a3492d3ecc0146eed6286fc91ceda169486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.1 MB (253104979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:015fd0a681f5e2ba7528e28c25a47cb840dafb36d49f3755f5cdee1fa85a4f53`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Wed, 18 Mar 2026 17:49:36 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Mar 2026 17:49:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 18 Mar 2026 17:49:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8db15a6ff7912550a105e0456d072642f0cbf20b8f056ed2774526378f23ad0`  
		Last Modified: Wed, 18 Mar 2026 17:50:00 GMT  
		Size: 224.2 MB (224235270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jdk` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d8a8d9fc76fb7e437104daee6fd52ff669371c1c7644f1cd4f92f9535122641b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2607895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf5bfae834e717ef7a723fecb5319d87cf8cc718924dc575346757c50c0136b`

```dockerfile
```

-	Layers:
	-	`sha256:c97aff8536cac67af12b689c4dc45d8301d034c32fa2935fdb10e2521df1ae10`  
		Last Modified: Wed, 18 Mar 2026 17:49:55 GMT  
		Size: 2.6 MB (2595167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:752b8778a8d0c0aac5fa8b90c5765d0262d6501f8ed63b389119ecda4596fb94`  
		Last Modified: Wed, 18 Mar 2026 17:49:55 GMT  
		Size: 12.7 KB (12728 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:26-jdk` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:23d67d6829fbb78dc894b34ef117a52803f79bcea92c23deaf082c58d30df66d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.9 MB (261926539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be085f4e3eaac862a35014b395e3030239898458f8b07462e54f76b052b6a352`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 17:18:33 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:18:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:18:36 GMT
ADD file:2a89eb67bf550d9680999e3ff99dbaa17c251b6c343a241318e879a26da53fca in / 
# Mon, 23 Feb 2026 17:18:37 GMT
CMD ["/bin/bash"]
# Wed, 18 Mar 2026 17:47:02 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jdk=26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Mar 2026 17:47:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Wed, 18 Mar 2026 17:47:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f826c9b754a00ada9d9335ffdf3ffd40f6925a3223caac76cc429823b8621f9e`  
		Last Modified: Mon, 23 Feb 2026 17:51:39 GMT  
		Size: 34.3 MB (34310051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb9b13cee3dcaafe363388b692c2a4202efd5b6c82460bdaf204157a13d2a10`  
		Last Modified: Wed, 18 Mar 2026 17:47:43 GMT  
		Size: 227.6 MB (227616488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:26-jdk` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cae90b5e7a7287e79dc791645cfb4758559b3969f963e816f02ebced8424a23a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2604136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8b8433c4d545cc51fe5a4c740734818f312ab034646fcb9c841a28f8300e18f`

```dockerfile
```

-	Layers:
	-	`sha256:85dc0c6cfff8101db69e1769f0518ab53a0e9c47ef1df17a6cc1aa8eba3415d5`  
		Last Modified: Wed, 18 Mar 2026 17:47:39 GMT  
		Size: 2.6 MB (2591540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f3b0c4c3d8affc3d25a9b082b789cee6818024fe802e3c296e5238aafb58dff`  
		Last Modified: Wed, 18 Mar 2026 17:47:38 GMT  
		Size: 12.6 KB (12596 bytes)  
		MIME: application/vnd.in-toto+json
