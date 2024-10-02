## `sapmachine:jdk-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:df85bc5096d91e974ab7705bef63081db416f46ddfc4a2c1e6434bbd70f814b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jdk-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:65ac80cfe8a5a4b87f00c7076b5c9462774a4d33fdd390b10a488e61a6ec48db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.9 MB (248857810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6001f2d3c3ec320285aa6b921083bcb1d77d2a51e0cd8da45bb7fbe9c20da587`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:50246322460b061c017415db05408d43b5861488e205744cb27f12daa6afe420`  
		Last Modified: Wed, 02 Oct 2024 02:00:10 GMT  
		Size: 221.3 MB (221346758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:38e8ff5917db418ea96013ff1850d6c838995f494853f8f78963474f8e4b6bad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2378195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c666f5a81eb8fbbc4496d0c74af01b5a8a01583776aaa066d34800225d469f6f`

```dockerfile
```

-	Layers:
	-	`sha256:b6b5557b9c4b5fa0379061708c82f242bec98dac27e7e4514bbbd90790db2452`  
		Last Modified: Wed, 02 Oct 2024 02:00:06 GMT  
		Size: 2.4 MB (2368383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04a84241737141e4e095b75ff218e3ead7df490af94bbeae8a04823d80dfafad`  
		Last Modified: Wed, 02 Oct 2024 02:00:06 GMT  
		Size: 9.8 KB (9812 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:54cc8bda2806bc8d69c43735d8747ebca331e8edf69fa8a816fdfe0ba5f919df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 MB (245283760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b58b8e80977f4c2fc46a737b05c3d809906c06df3fea5ff9c91a4ce00879f3bc`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:578770371938bb4e6554c30bd30463648bc924bc0c9ecfdd0e0d6c6e582e517f`  
		Last Modified: Wed, 02 Oct 2024 03:45:50 GMT  
		Size: 219.3 MB (219310168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9282c94a5a91b1d18f273fe7afdea95764c2662daba4e0f915f2081c48df51a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb7c2f5360b2105f05eb0bb7fa1482b2445300437e0e7fd1a40c9a6e48f72f3`

```dockerfile
```

-	Layers:
	-	`sha256:86078539f22e7e5beae6e386c436c86bc239b8daa8b93aec4c498beb76690834`  
		Last Modified: Wed, 02 Oct 2024 03:45:46 GMT  
		Size: 2.4 MB (2367436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd3d9083e2bd7d27f68c053b589fad99f50a2f76cddc3026afd637e7aa6a7511`  
		Last Modified: Wed, 02 Oct 2024 03:45:45 GMT  
		Size: 10.0 KB (9957 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jdk-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:d727cd547c8c2cae647109ee919bb0e522dab4502db96ed492262503a5dc3585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.0 MB (254014084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9833e665c89564ccbff929f48a1e741b37fec671eb6e5fa419245acaa261e2cd`
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
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
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
	-	`sha256:08e62fef5cc0224de34d234b1d76f98f8089d2a2105a2df0cec59be7e3178d97`  
		Last Modified: Wed, 02 Oct 2024 02:51:36 GMT  
		Size: 221.9 MB (221937750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jdk-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1ba8ea1fe79b316a9eb5458401c1ec9232cfd8a3b665debe596dc834e6dced9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b1b91d7b120284e5ef0e422c0e8ded80272635ee2bd8b6d56f861119b306d55`

```dockerfile
```

-	Layers:
	-	`sha256:bb2b0e14b3ccb6ec213159d9970167d929508eac80eda7425a201e5bb8271d87`  
		Last Modified: Wed, 02 Oct 2024 02:51:31 GMT  
		Size: 2.4 MB (2369604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bfd5dba92d9b1c084fceff3670fbe769baf08d956c3c9ed5a4c64197ee00cb5`  
		Last Modified: Wed, 02 Oct 2024 02:51:30 GMT  
		Size: 9.9 KB (9874 bytes)  
		MIME: application/vnd.in-toto+json
