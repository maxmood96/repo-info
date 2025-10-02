## `sapmachine:17-jre-headless`

```console
$ docker pull sapmachine@sha256:586dc4a7ac8a432bc0ab7627cfc91e2d8475e81f2d7a2195f8da6844d8306fbb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless` - linux; amd64

```console
$ docker pull sapmachine@sha256:60c798a95a0308cd7fb9a8dabde1bef7f6680b05a3ac40116d3d5c0d83684f10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82782253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d70c868c9d38c45902109a4014e4b14381444cc34cd434d446ca9d11d085d7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:35 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:35 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 11 Aug 2025 06:09:35 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:35 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784ffcd4f8376992d807c3a4167d5885da4c3a143aedca78bc2551455f2dba07`  
		Last Modified: Wed, 17 Sep 2025 23:38:29 GMT  
		Size: 53.1 MB (53058803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a3eeee5f411c176b699016ccc74125b52af7f54f6c98d34aa674a776e19b25e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2281836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd96d3f3ece333a2f8b9715dd94ac5d43071e22e98b69eb2d5c603c7c953869`

```dockerfile
```

-	Layers:
	-	`sha256:40a1409ce82e0a9f357bea5bdb7d448da4395ed78c3a4e18454fdd60659a18da`  
		Last Modified: Wed, 17 Sep 2025 21:06:07 GMT  
		Size: 2.3 MB (2271564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:717a79b44661be52850db2df1b9ef6e30b48a062b7a7aaa1592198f2660b341b`  
		Last Modified: Wed, 17 Sep 2025 21:06:07 GMT  
		Size: 10.3 KB (10272 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:8a317b11d533e736ba3edbf8eafefc0448b54fe38d6b2bae8d0c776bf8210718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.6 MB (83566538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78438baf2827fd0d3590bcfe83faa8f18db4146dcadacf8285da9df43289f440`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:35 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:35 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 11 Aug 2025 06:09:35 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:35 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0689f88ab5d9732a9196a4e5474d5e5222dc4fc3200ea9ec0e4315a7774b33a`  
		Last Modified: Thu, 02 Oct 2025 01:35:05 GMT  
		Size: 54.7 MB (54704963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:dbb3f40fa768cc5588e890fa72406c0d4df158247d09f45090ff8fc5ff459c6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff9e804bf3bb7bf651945fc51af939cdc6ebff4dfda9d016684a0e450a44222`

```dockerfile
```

-	Layers:
	-	`sha256:ae830b0af0c2a7c0b827f811e9bdd987c4229eec536898c7a07ca5302f0655ec`  
		Last Modified: Thu, 02 Oct 2025 03:05:23 GMT  
		Size: 2.3 MB (2272071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65ff1cb180634bd3db2b130586f9befec9645766f9a83b4bf4fb6a28919e6384`  
		Last Modified: Thu, 02 Oct 2025 03:05:24 GMT  
		Size: 10.4 KB (10423 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:c4bf12ff77d0d6ff3d5312547971012a767497cf95611dbaba3e4cb97909468a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 MB (88368713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613864345395e949292e2b19293f52743e797a02b9d20129d887f69580339887`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:35 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:35 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 11 Aug 2025 06:09:35 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:35 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 11 Aug 2025 06:09:35 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690bac9ef7696404aa6fedbb8d6aa3ff236a287cf3cb0ee38295e0a8ba1eaea1`  
		Last Modified: Mon, 15 Sep 2025 23:51:35 GMT  
		Size: 54.1 MB (54065586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless` - unknown; unknown

```console
$ docker pull sapmachine@sha256:382552166ec5e59ab41a0356a6909ec2cb5d20a58d5ab13f24d83d3e31157bce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2279904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3be6d59de7135d37eb8f11c13bf7159dd8e4f46b617cc87a073c14d1e7b5923`

```dockerfile
```

-	Layers:
	-	`sha256:29c5521eb815e2f2204eb2e829a869efc24e61c928823c4084f7dbe660eb09e1`  
		Last Modified: Wed, 17 Sep 2025 21:06:17 GMT  
		Size: 2.3 MB (2269564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6ba258475fefd44d9296bf5f4abf9b61fcbbfeb5e9363c5df97d3f504668013`  
		Last Modified: Wed, 17 Sep 2025 21:06:18 GMT  
		Size: 10.3 KB (10340 bytes)  
		MIME: application/vnd.in-toto+json
