## `sapmachine:11-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:c92f59178f53c0f5883a5f87bbd20ef934ec325129e68a2c32f2e2b05c401a10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:031039a0a0e374fab95dad797a2282e2056c29c9c1ff2fd618f8bc30b4e62c69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (229040852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942a5b9be92227ff0dd3a8902b5ec46353339ff16590a016ee181b177c68b706`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc14af9015edba9efb5d3c5bb74b55696d49d57dffcda5f56be5496bba4ed495`  
		Last Modified: Fri, 19 Jul 2024 18:00:57 GMT  
		Size: 199.5 MB (199506797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cf43d7f2a6ce86c28d42952e934510231a7e99e4a4d9b5424f360ca09afb4c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2254568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef022c2249ba535adc679d13e3b7a0b07827e81ee2f937be24049977d1ec8d5f`

```dockerfile
```

-	Layers:
	-	`sha256:a0f75ad98717e9c71d0e2795a68050a2d9455f68db7b7b31cb6ff9b484c521b0`  
		Last Modified: Fri, 19 Jul 2024 18:00:53 GMT  
		Size: 2.2 MB (2245890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ded857992ca1011449b8af4be11e10d1f8094f6bb5ac6bb317f3b18d473612ad`  
		Last Modified: Fri, 19 Jul 2024 18:00:52 GMT  
		Size: 8.7 KB (8678 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:54a483d4fdec7da5815cc35616c1ddb29d21c3b6659f01ad2ecdc7663c956952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.3 MB (225338863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e9fd37d1e20666d586637e055a4dc58fbde50205ad9bde65ada96786b20504c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a41e1e616613e031faf15bdb0cd5c497f67fa2d449cd9e4ea7d58a2c4463a47`  
		Last Modified: Sat, 17 Aug 2024 04:46:46 GMT  
		Size: 198.0 MB (197980180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e1e52d2e8d287ba0d0aaa18d34ed7c4f2f11bd1dd0d2ee89af3705168e13f8ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2255168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4bf5f964a62691f5c61c9e662b406bc74cc1b9c99c7519773e0e8851befe9c`

```dockerfile
```

-	Layers:
	-	`sha256:6dccb02fba1493103c739d69b215322b912bba80af0c71c0ce0c990a6dd73341`  
		Last Modified: Sat, 17 Aug 2024 04:46:41 GMT  
		Size: 2.2 MB (2246188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf162bfe661b167ad23fce866243fc31592de3058e4ea77d7279d17db48c8d30`  
		Last Modified: Sat, 17 Aug 2024 04:46:41 GMT  
		Size: 9.0 KB (8980 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:2a554a77c8d51588b0a35be1ef9373d4cdbbc120295e0b528d4759a4c59d873c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.5 MB (220458030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3baabdde5dd5cf80e3da21a9288dfe9b048881a51f5ca0407b916befd76ef713`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c6814968a642c96d09537613dce9cb2644f97bc533c75c35c746b01a3de638`  
		Last Modified: Sat, 17 Aug 2024 03:35:38 GMT  
		Size: 186.0 MB (185993852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c63ba4ec38e606a5b9005d440dc0f191eb0facbcd9d5f701a7da6f8162d21601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2255942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b51c4f12f6fcd75d672bb6c987f2aa91d9668662243d3b08c4e3702c574076ed`

```dockerfile
```

-	Layers:
	-	`sha256:3cd9410812dbd5a4a3379128eceb9ad8892fef97ed29117ca082fa872579b168`  
		Last Modified: Sat, 17 Aug 2024 03:35:31 GMT  
		Size: 2.2 MB (2247225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44639be3ed9e55755bbe77d3d077e058f1682902527ba2a6f8a8a5781c0b3790`  
		Last Modified: Sat, 17 Aug 2024 03:35:30 GMT  
		Size: 8.7 KB (8717 bytes)  
		MIME: application/vnd.in-toto+json
