## `sapmachine:17-jre-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:09e66c363237c500d3ad0ade2ad60c40ea900463fcc221d112bb3bd112cb5b65
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:718fd5a7e2be802ea646e0a3a7b555266473ba499cd7842d4f5219228aed137e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.8 MB (80769640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c4e7f7dc9d836468aa821edd913d2b4f4f6db33f7f4ebe676ebf6d8f36c557`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:09a7c452651dfe578fa06e78da0224ca8fadcaaa84ce672d3821c89d6f24286f`  
		Last Modified: Wed, 02 Oct 2024 01:59:50 GMT  
		Size: 53.3 MB (53258588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:46d32c3f38a593998ef6caf48cdd871784a2711f6009c850551ee0c719a1fa04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2288226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3cd631695df0ac1c56c7779a244af5e25c8f79aa345f4115424b197d674425b`

```dockerfile
```

-	Layers:
	-	`sha256:b3303b189aea2a4ba6735adaedba67815390d9a55c1017199f08f0771fbfe645`  
		Last Modified: Wed, 02 Oct 2024 01:59:50 GMT  
		Size: 2.3 MB (2279654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60ff43b52c2961bcfdf76b286325ebcc63acf453a119f826a11c15ebdac3eb0a`  
		Last Modified: Wed, 02 Oct 2024 01:59:50 GMT  
		Size: 8.6 KB (8572 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:b76632f1f364863619e7d3a2fd2f89f8413fc282235cad1857479aee85ddc920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78599443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551341d40194d566406106981b186f5fbf07725fe7171ea923a0bcf14b723f9d`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:08b9d3b02149d3925ecb9d2a240a8e624489dbffe910243fa0b41b4e50e41abb`  
		Last Modified: Wed, 02 Oct 2024 04:02:50 GMT  
		Size: 52.6 MB (52625851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1cda3fd42ffaa04c4976063ddd2b24f259eb2c8ae46340aaf2713308eaa346c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2287960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:063e563fff6d2d0e18a767e1d75c8552105b3307c363dbc9e79633a97eeb3ccf`

```dockerfile
```

-	Layers:
	-	`sha256:fc54503682fe37920c7348ee3d01af4b71f3ad86903ae1ca616aa38a1c65dd79`  
		Last Modified: Wed, 02 Oct 2024 04:02:48 GMT  
		Size: 2.3 MB (2279290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caf939f7b8c63628558f4d39a4857a65da516498191c1b10e3bbf0c4cc0b1d8c`  
		Last Modified: Wed, 02 Oct 2024 04:02:48 GMT  
		Size: 8.7 KB (8670 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:44b494a1332e3f5c570d1eebf4f076ad36dbea859da766c0e54fd4db867c10a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86438650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25157189f0f9d6304502862845bcf56b649dad4daa01f282d426aadafdcf1239`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:a0120d36ab9c6097f03d569c7e8c33b8176ecb0531d46ca5de7924da53b286cd`  
		Last Modified: Wed, 02 Oct 2024 03:18:26 GMT  
		Size: 54.4 MB (54362316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:79015987bdfc9080ea4fdc793fbb1824ff3b878743a400e863a58a6df7108a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2292029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60ea8ee8190a63704d9818602a5542553eb220de2873f7ebfd9188d6444bf6ea`

```dockerfile
```

-	Layers:
	-	`sha256:c1ec5ea0a41988fcfb8b8139ba87f3f36942c5f798423f2d9e9a5f03e90ce29d`  
		Last Modified: Wed, 02 Oct 2024 03:18:25 GMT  
		Size: 2.3 MB (2283419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7033934f1f36e6aaef556adb7630713e9a54e07f06a009eae43c3c63c8ea1d7a`  
		Last Modified: Wed, 02 Oct 2024 03:18:24 GMT  
		Size: 8.6 KB (8610 bytes)  
		MIME: application/vnd.in-toto+json
