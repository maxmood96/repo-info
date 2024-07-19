## `sapmachine:lts-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:dc5d07d9d3937284f6162bbe148bdebdb946e8a060d70d5c5706f0c5184f5ac7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:96ba6aba1e1e8f00901a186ceb2ad644cc12009ffddece80540bc004ff38f0ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88260512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ae7ba07ba350c257542df91290905efe16fad04b400b0bba1f0e9401f3b4d5e`
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
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc8f2b7aaa93afcf11bbffd96f29777f75b7a582aa57ef4381edd0cfa3532b9`  
		Last Modified: Fri, 19 Jul 2024 18:00:13 GMT  
		Size: 58.7 MB (58726457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f03d9598f210457bb373661d03cdd79846f10f174443150a735b05a89cb3e8dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2156888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c073eb3a097c3f19b43d4e59725e56991feec6bc00fdd1c5f2c4947d44c85f`

```dockerfile
```

-	Layers:
	-	`sha256:022e68e1c7fbdb8801ccde8eeff93c06d1c728d7a5582a62682f462789dcc2e1`  
		Last Modified: Fri, 19 Jul 2024 18:00:12 GMT  
		Size: 2.1 MB (2147515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f486cfdc3ff221e279087fafe54d39c41e9628949042ed3b7777838953319e79`  
		Last Modified: Fri, 19 Jul 2024 18:00:12 GMT  
		Size: 9.4 KB (9373 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:1091fb04e168808e7ae9751d9b0933faf38fdf92e795ebd9ea4b68e525d81cef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.1 MB (85070218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a4391fc96e5077e9115e32506ab7e5198dd3d7388fb10fe9d636ea7c696a1f9`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c584b6b1d16d5c8d19c61d53b6fc78a2e2548baa95ab81e6cedb0ab299f571`  
		Last Modified: Wed, 03 Jul 2024 00:01:31 GMT  
		Size: 57.7 MB (57710193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:db87f8af53784ca5c434e1210c5c650b8b58ee0d1fd9dab7f217bbb21de35e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2130766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a0ef35f66792e8a4a582d6e9d068b6cf4b1c2df118b7146b378ca39faf3a55b`

```dockerfile
```

-	Layers:
	-	`sha256:24f875398eece94ab43ee021c1b65b56825c5b383334c793cbb284e9ae581b32`  
		Last Modified: Wed, 03 Jul 2024 00:01:29 GMT  
		Size: 2.1 MB (2121050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40fe4a704e906afb27ccf83221eb8e651d71d4b55dcbdde0701b8fb6a83fc35c`  
		Last Modified: Wed, 03 Jul 2024 00:01:28 GMT  
		Size: 9.7 KB (9716 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:ca61316004eed007c54b350fdac12cca7665ea0fe9006acdfffffc3ff95b8ac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 MB (94503006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a2e5407cb1d38d84a8f3956b3e4d4705278a7130918238d60636fac64dcc4d0`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:52 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:52 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:52 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Mon, 13 May 2024 10:06:52 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 13 May 2024 10:06:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f8c953e60284ec09f116e3ca67dcc34b297fc93b78aeaa0fa008250b87558a`  
		Last Modified: Tue, 02 Jul 2024 21:29:41 GMT  
		Size: 60.0 MB (60041925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4fa382aa3ccfb72a409c86eb85527d501548833fe2058bf1bdaeece34f9f5ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2134718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3e422e0f37e08a2b546efb3e925d1823e41126cb85be0f8a7a80c5397e77d5`

```dockerfile
```

-	Layers:
	-	`sha256:040f0ce4e46815c793356134d132c6d6416de5f2974f44096c7b87131c2082e0`  
		Last Modified: Tue, 02 Jul 2024 21:29:39 GMT  
		Size: 2.1 MB (2125277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54ff4b7686f061b5e2c84d782af7d0b157f91135ede9991f6e5428e95062bb2d`  
		Last Modified: Tue, 02 Jul 2024 21:29:38 GMT  
		Size: 9.4 KB (9441 bytes)  
		MIME: application/vnd.in-toto+json
