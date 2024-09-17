## `sapmachine:17-jdk-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:dea97597fce47f905293a8b92479de5d3430f37841197d7a7660baac93765b64
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:2837f575a4da95065d14e73e962ade3fcaf9b5fac06bfa7f86f8383dfd0f0db4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.4 MB (231401049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d65171b553cb361bcb28727e5d32f834d419c05b02f7bbc82452e778a5a1bc73`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316d46459239a0890ac904e6461aa9f71b86e16bdc554a6bcbd68acb350b2938`  
		Last Modified: Tue, 17 Sep 2024 01:00:50 GMT  
		Size: 201.7 MB (201651221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6c38be1e97d287e1019911d512a8a4a689f9ccaa6f3e7abca8a1276dc226cb90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2219068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6018f7cc99763616073078b2153f551bc4acbba8a3080dedc3503e1f74a78159`

```dockerfile
```

-	Layers:
	-	`sha256:7a5d48d531a940a91cb8153297442457c70376d952ea8dfa996ffd3ca8acb95a`  
		Last Modified: Tue, 17 Sep 2024 01:00:47 GMT  
		Size: 2.2 MB (2209703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da8f76407050be8699ca050fce5645ef22b885f7a8d95f3740ebcdb0478b74d5`  
		Last Modified: Tue, 17 Sep 2024 01:00:47 GMT  
		Size: 9.4 KB (9365 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:51f8e7727ba03de1edd39947ac8b3834e915e01dda3838ece2f80b0125bb742c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228984090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27bdd70660d0e140b48b6fdf3c9c9225d90b4cb7794b78b3b9fa6d4c9008abe3`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e59cb05818e49ea83cbe79bd46eb80418dfe3cb3735b45570f93a23579e2cec`  
		Last Modified: Tue, 27 Aug 2024 17:08:12 GMT  
		Size: 28.9 MB (28885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eababa2f443d6992be622dbe7440e9b6c1fed0bbd2d77220d846e44946e26f85`  
		Last Modified: Tue, 17 Sep 2024 03:27:50 GMT  
		Size: 200.1 MB (200098491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e30db73b9684e481eb8d37a4f8f05c933a0b3c655f8d30199ef00d1bc82935bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2219875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff5bd8431162be591dc150224b45dc69afdc799b108c6e5c1a9fe8662d62a63`

```dockerfile
```

-	Layers:
	-	`sha256:0058da6054a3a4f6d6530dddfac66af3ccfbaec1bff8df9c3e7f372f5c9a30ea`  
		Last Modified: Tue, 17 Sep 2024 03:27:46 GMT  
		Size: 2.2 MB (2210185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac9e27baabbd4b06932c8d699aabf6b641a3c1f76d75b5291e6ca725ac6f094a`  
		Last Modified: Tue, 17 Sep 2024 03:27:46 GMT  
		Size: 9.7 KB (9690 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:af953808e84923e626c6d567ec0a1403411beb878c7e861e3364877b74c549c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.3 MB (237268789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8aaf3a385518b94d44a3d554cd33a95b49e54100f87ffe96afe04623d53e353`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:c70c2393dc0404f71d25ae70ab08b5aa65e46753a6169cfd4f5554c942cc0218 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c526398e5e771684dae49961d5a74cd9606dcbcf7ddafb1fcc1433293927dca4`  
		Last Modified: Tue, 27 Aug 2024 17:08:24 GMT  
		Size: 34.4 MB (34392345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa3bb3fa67fd9429f1d4aacf99d6bc05a9b39f326f3b03e360d8c08272defda`  
		Last Modified: Tue, 17 Sep 2024 02:46:24 GMT  
		Size: 202.9 MB (202876444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cd3f25734eedd82c78cf787104b5c97423a7da9b8a07e22a9701884aec2d0abb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2221055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57de92c38de8b896da729c454cb62395920843c7bde91103f01975bba6b7620b`

```dockerfile
```

-	Layers:
	-	`sha256:f33ad39ed669816f83d7d9975d2d31ad1b96d0e42b9e442503409c9c0dd0dff6`  
		Last Modified: Tue, 17 Sep 2024 02:46:19 GMT  
		Size: 2.2 MB (2211640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fefc028d27932e7dbaec7cfa2cd4bf72866330113009320b99ef8d659b6f00f`  
		Last Modified: Tue, 17 Sep 2024 02:46:19 GMT  
		Size: 9.4 KB (9415 bytes)  
		MIME: application/vnd.in-toto+json
