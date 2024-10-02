## `sapmachine:17-jdk-headless-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:8223a0abaf1f21e75444730b8b1bdf749b4a7d496f52c0e898cd2351ab296e4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:bb4e046cafab21d7377b706c9835af8f46a2a6363880cea443b161d9e1bf6373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.9 MB (225899613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46be7ad038de7ccd6342d950a46f889f6895b5f4c401001001e639d6603481ae`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:6a209aa51ba684c0a39769619c42058ca99311b87563c7b079319a8bb91bec1f in / 
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
	-	`sha256:3823320faa42774534fd7eee0bd245af8cec6a720ad722144d40efa229291d8f`  
		Last Modified: Wed, 18 Sep 2024 05:32:37 GMT  
		Size: 27.5 MB (27511052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a40e064d1c7a20235948e75e6c10da31af5dd3215c3d09370b32009c5e89f0`  
		Last Modified: Wed, 02 Oct 2024 02:00:22 GMT  
		Size: 198.4 MB (198388561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ee2f5c7c2ab346f2e70ee72f0e7db02900aa465149ba0b27654c42f87e7a0e61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86b45f0f22243d4a07cedbf971ef8c454b4826844cb07e42aa171d454440be18`

```dockerfile
```

-	Layers:
	-	`sha256:63f2e7b1cdb4719dcbdf0e4f025eee5616f7f8b8db9c736fa1c562a41014119f`  
		Last Modified: Wed, 02 Oct 2024 02:00:17 GMT  
		Size: 2.1 MB (2125406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abe534042db21c0ae20a0d9cabeb3fe4134b5c94671b721b23f8fc04de36f1da`  
		Last Modified: Wed, 02 Oct 2024 02:00:17 GMT  
		Size: 8.7 KB (8684 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:5764bd2037daff5e3d5202d15a3ff68a90a2454d7674e5b88f3b7b64a8814393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (222996033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff9c19702e5eda5966c9568e5991e9c7323a4e34af2196cb7f3de73f063eb69`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:193e44687e108da6ce3970dd4e85b4ab975e008873500871bb89e452afe82d52 in / 
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
	-	`sha256:f7087ec3f63a82386ce40d74d075d761ece5bfaefdc30b9ef62f73ecfb2e41fe`  
		Last Modified: Wed, 18 Sep 2024 05:32:46 GMT  
		Size: 26.0 MB (25973592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47075c66a968a15a95251a6fe73836ce1c160af67d8809e3852539c81f693bff`  
		Last Modified: Wed, 02 Oct 2024 04:02:01 GMT  
		Size: 197.0 MB (197022441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0c09cc7357fcf0164058a62c913d06e2445d5079374a32527d06b82cc13dcad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2133815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:187ce22ba46a277bfa9c1fecb664f8dbedcddabe1a92944603b54cb61448d471`

```dockerfile
```

-	Layers:
	-	`sha256:e2715899f31283833282c5daf78d37c46754cc73f169e22e4ef401f703f28044`  
		Last Modified: Wed, 02 Oct 2024 04:01:56 GMT  
		Size: 2.1 MB (2125033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ae2787a654dfa736150404c03de82cb6b1e5f45dff5e66474284992d64d9bff`  
		Last Modified: Wed, 02 Oct 2024 04:01:56 GMT  
		Size: 8.8 KB (8782 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:ec66fb33b1b34d6ac40c720b69f54615bf8477a218944d22e37783d3de23000f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231006494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d44172a9095a2fb87f4d9c5f30e105d2da848303abe5a18efeb9f0218e186731`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=20.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:c6515e5ea6494efa348e1177d50c0c28bb8236a5d2b518388f13b7d5a528d4fd in / 
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
	-	`sha256:cafd57629abc05d597016161b87b83b544a17d39d1016cfb289a60295fc7d492`  
		Last Modified: Wed, 18 Sep 2024 05:32:58 GMT  
		Size: 32.1 MB (32076334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2983a5755b166dbc6afa57cbe5c86c43c4eab88fa471ba80093df7d107d23ee0`  
		Last Modified: Wed, 02 Oct 2024 03:17:14 GMT  
		Size: 198.9 MB (198930160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:30f167d06788840125ecc205dca3b0f8b28be34b4a522d7a450a16992a94ba62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2135881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd8105ae15d33d0a2a3e845a73c9cbb6c7ca21117a67a8b4067279ae57a4fcc5`

```dockerfile
```

-	Layers:
	-	`sha256:8b6944461c850dfba92be0cd2f753880480104a821e20ce9c58a4d719faf3a6b`  
		Last Modified: Wed, 02 Oct 2024 03:17:09 GMT  
		Size: 2.1 MB (2127159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8e09fc29e7641935aa27ba8a294ff2a98d6e2b5a34f6af69cf5664541eab1c4`  
		Last Modified: Wed, 02 Oct 2024 03:17:08 GMT  
		Size: 8.7 KB (8722 bytes)  
		MIME: application/vnd.in-toto+json
