## `sapmachine:23-jdk-headless-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:03b26cb3176f9bfc0a8e5866f38ae474df1a9b00bf1020fe1295ed87ff3ab460
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:23-jdk-headless-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:fa92fd4e2af24a0d5e6cef1714e1078fb4408c5a8fed9629754e586af5475e16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 MB (247654482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d57d917047bc26bc1bf2defe415300182229199b46a255e2894d29b164eb25e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:32 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:32 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:34 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
# Wed, 18 Sep 2024 04:18:34 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9aaf467bcfc75a57f93fb0e8dcaa93d38813459587c25616d682be9baa40bb`  
		Last Modified: Wed, 02 Oct 2024 02:00:14 GMT  
		Size: 220.1 MB (220143430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0ce73457554cbfcb1a28081814e5c424dee729eddf03d56393362cba4c472ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3786a21a4ff2eb2491658fb6ba638eec2289d6238438b5e3614503b4ce84e72c`

```dockerfile
```

-	Layers:
	-	`sha256:1dabed6218d855666cdb6b26cf8975cb4204c0f38e8f48bb17c42397962e9e13`  
		Last Modified: Wed, 02 Oct 2024 02:00:10 GMT  
		Size: 2.1 MB (2129812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06965fc8a2926d6e497baf527fa73747c8ba0463f695464aaf9869ddeb1e2c54`  
		Last Modified: Wed, 02 Oct 2024 02:00:10 GMT  
		Size: 8.6 KB (8639 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jdk-headless-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:444db08dc731a3f96159b8a6dedf0ed54de8f54a1334d6db18c59c8d55bd0f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244090651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:505feea516de89c6adfa0a7ac1a13ba940dff014085620b0faba6bc80a104d25`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 18 Sep 2024 04:18:13 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:18:13 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:18:15 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
# Wed, 18 Sep 2024 04:18:15 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7087ec3f63a82386ce40d74d075d761ece5bfaefdc30b9ef62f73ecfb2e41fe`  
		Last Modified: Wed, 18 Sep 2024 05:32:46 GMT  
		Size: 26.0 MB (25973592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df2ed96065aa1e3420182e4cf9decb8d7ff123754b143ebcba62cd1897a2fc6`  
		Last Modified: Wed, 02 Oct 2024 03:47:01 GMT  
		Size: 218.1 MB (218117059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:55d476b3783ac895c185eb6e47aa51ac6d6da86a5ebbc1115af9ad6d1688adcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e10a2d943f840a1da8a47f56a47000f3ea4f3719914a5219f7ea943c498129`

```dockerfile
```

-	Layers:
	-	`sha256:f8279576ce75d4dbe1f226003099664b9a37b732d67d66d49c2358ae88e38000`  
		Last Modified: Wed, 02 Oct 2024 03:46:55 GMT  
		Size: 2.1 MB (2128808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5d081251c7b82a35572027fedfabff571e0efc1bee09073c6e617f7f893a4a9`  
		Last Modified: Wed, 02 Oct 2024 03:46:55 GMT  
		Size: 8.7 KB (8737 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jdk-headless-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:9496bb1036d37e6905f92117df649e50fc5803b3794c5c09ee757507789aa74f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252658040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2def67c62af9448e56a9ef8c302807211e9c26041542aedee5f818aa160ac57`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 18 Sep 2024 04:19:24 GMT
ARG RELEASE
# Wed, 18 Sep 2024 04:19:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 18 Sep 2024 04:19:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 18 Sep 2024 04:19:24 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 18 Sep 2024 04:19:28 GMT
ADD file:c6515e5ea6494efa348e1177d50c0c28bb8236a5d2b518388f13b7d5a528d4fd in / 
# Wed, 18 Sep 2024 04:19:28 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cafd57629abc05d597016161b87b83b544a17d39d1016cfb289a60295fc7d492`  
		Last Modified: Wed, 18 Sep 2024 05:32:58 GMT  
		Size: 32.1 MB (32076334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0746849aee8e72a5def034502ddd7ed9f7b17968a52bd28cfb88ed5690cc216`  
		Last Modified: Wed, 02 Oct 2024 02:53:27 GMT  
		Size: 220.6 MB (220581706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jdk-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:21b82e95d14c8091efff1317dea74869cd224730005acb94bfbeee01f026232d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df464b1bf668720567bc69e3038fb558091d9212e2ea1e8bcba9f4c6fe85c9d`

```dockerfile
```

-	Layers:
	-	`sha256:95aac5353f0693d20319a121caac53b3b0a20e85b2e357dfb69d28b1a1600bde`  
		Last Modified: Wed, 02 Oct 2024 02:53:21 GMT  
		Size: 2.1 MB (2130946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8d8390a51c9a28a3317b36f7e80b944ad8f4234ccf26efa1d6ab8839f2d4018`  
		Last Modified: Wed, 02 Oct 2024 02:53:21 GMT  
		Size: 8.7 KB (8677 bytes)  
		MIME: application/vnd.in-toto+json
