## `sapmachine:17-jre-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:86b490167007a4ded1c116b4944b6d07aa7187fb32346ce4a42b65a27c24b402
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu-noble` - linux; amd64

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
		Last Modified: Wed, 17 Sep 2025 17:40:26 GMT  
		Size: 53.1 MB (53058803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-noble` - unknown; unknown

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

### `sapmachine:17-jre-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ca2b2c1651c490578ecd5f9b5ebfe5c6e4b1a6d37215a66c0655a60d208079da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81348709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc9a39370f9a979df093a8eabcc998bc3f9d1f8976e79426ac32fecdfea41bd1`
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
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
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
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38ead082516f4e79621a1c9f520747ae0765611809c7d3477cc6290a025a46c3`  
		Last Modified: Wed, 17 Sep 2025 17:42:07 GMT  
		Size: 52.5 MB (52487392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:62fe379219597c150e9209042378f0597b45e9156d74a712f07d17d0b1fe8a7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2282495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:776533a4ae329e98e5ce2cffaaa8861bed01c9fcc59ce3cfb12afe97e6eb017c`

```dockerfile
```

-	Layers:
	-	`sha256:84412df812139a20f702ced51ee47c9424ae17ef7e4d4dc31977096e51427fe0`  
		Last Modified: Wed, 17 Sep 2025 21:06:13 GMT  
		Size: 2.3 MB (2272071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3ea873293e05a3fc6e69378d85de05f4d3dbbb7043e758b4eecc85856d6f487`  
		Last Modified: Wed, 17 Sep 2025 21:06:13 GMT  
		Size: 10.4 KB (10424 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-noble` - linux; ppc64le

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

### `sapmachine:17-jre-headless-ubuntu-noble` - unknown; unknown

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
