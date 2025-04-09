## `sapmachine:17-jre-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:febe83bfeb5eef621327c4ffdb06961af160e472d69bceda39318a06583733d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:4b0e61da73cfd5b4b8bd36dcdb147582beabe700e7b5d40005e84e6d3361c300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.9 MB (80870724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b46b76aa52ea0c1be3e1d4d22b02542beaa527664fe17d3cc8b80c2755acf7d`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:16 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 27 Jan 2025 13:39:16 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817caa83d63f0af3fde6fa46686a1c2b549748b2a67d9bf199321585627f986b`  
		Last Modified: Wed, 09 Apr 2025 01:21:49 GMT  
		Size: 53.4 MB (53360330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5280417f58c30bedbabc3189db4ddc0a1ac33cf2ae19c675a6200b4e8934c997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720649190cbcfdcfac3037d59b4c4c0aa4dff8a37e06af1c30feb5154fbd4f38`

```dockerfile
```

-	Layers:
	-	`sha256:a4fddc9933f168e351f80f1bcdf58e22eb1b7722157b6a0ecc8015fdb8aca2ee`  
		Last Modified: Wed, 09 Apr 2025 01:21:49 GMT  
		Size: 2.3 MB (2299303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fbd49c4957cffe877459412d9dcf764430cbe817705fb4dd0a0c76c71c39ed2`  
		Last Modified: Wed, 09 Apr 2025 01:21:49 GMT  
		Size: 8.8 KB (8821 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:cf3af657f133fcc040bac124e13b4ac609ef42ee94ffe87ad88d9b7f5e97494b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.8 MB (78771709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e211036a220194a7b9bc5551b13d4c8d84331e3122ae44205d65ac55a90fb83`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:16 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 27 Jan 2025 13:39:16 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2fe10848094f14e63e72801ea989f95108b9644b731d74aa13cdd047b93e52d`  
		Last Modified: Wed, 09 Apr 2025 09:49:33 GMT  
		Size: 52.8 MB (52794048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:57525bb1b221b3cbb46b6b7acb71d8b7bbaa18b3fc0fdf8be54f3a8dae8ad43c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2307866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5195d10c70bc34269be2f5ed8dcb878effe63c834fff2dc344a8f1136f3959f`

```dockerfile
```

-	Layers:
	-	`sha256:6d923a85549f4946e7665fdf29e2bb6d093616ba7e604f375b589561728bbb48`  
		Last Modified: Wed, 09 Apr 2025 09:49:32 GMT  
		Size: 2.3 MB (2298941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e051fda6991b44f8580856a7229a8c6f749c036010487c1ad0f5977d7f9f5df`  
		Last Modified: Wed, 09 Apr 2025 09:49:31 GMT  
		Size: 8.9 KB (8925 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:35cce1cd5f974a42f04088c71e794db57b0a8a73e41d6244a743be9d74f769f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86568866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e1a2582d4995fd45860401d83fcc111932e8da383c0ed619723e6c1835f7055`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:16 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 27 Jan 2025 13:39:16 GMT
ADD file:d85970cec61787609e3854cb76ce16d54fe420b254cf48fc9ed9ed678717ff28 in / 
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:92d54367a68b4f03400315732acb4290d88bb06f8fe1414fd823f93402bec922`  
		Last Modified: Tue, 08 Apr 2025 11:48:44 GMT  
		Size: 32.1 MB (32076946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447f9667ab1a5e764472e603d65ef06224080c91bf812ef9913f17b43059a49f`  
		Last Modified: Wed, 09 Apr 2025 07:26:54 GMT  
		Size: 54.5 MB (54491920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:490fc60192195c515455667c57b8d4cec7da6e2197c5c0ee3cf332dd52b340b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2311935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28410025674bc965bb1ec1b7056355346675ed63cf3a2f66b56863aceb39104`

```dockerfile
```

-	Layers:
	-	`sha256:4a362123ce800f80781abc7f62db1996df137e1f288ebf66d7163bd9b12d0872`  
		Last Modified: Wed, 09 Apr 2025 07:26:53 GMT  
		Size: 2.3 MB (2303070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69d6a5efda1e96fee0775a00a3193998d2446ba2be3da5e8e1786839bd8f8a1f`  
		Last Modified: Wed, 09 Apr 2025 07:26:52 GMT  
		Size: 8.9 KB (8865 bytes)  
		MIME: application/vnd.in-toto+json
