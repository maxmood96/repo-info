## `sapmachine:24-jre-ubuntu`

```console
$ docker pull sapmachine@sha256:aa301794045595c0e848ad6675203451528b61ea015e0eca93b4aa6d196db9f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-jre-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:741b9f357c7215278df489e9df2e97fd2595f025c133ee6fc5b18252547daa0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.8 MB (97815562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a87a8df90ec77583953b44a8018d4b9b834bf03f905c24671324319380c98e6f`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:20 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:20 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3683986f82fdb785ce9c83d7b846c9f852ab42ea0e64e17b52f2cafc062ce9ee`  
		Last Modified: Mon, 15 Sep 2025 22:26:47 GMT  
		Size: 68.1 MB (68092112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0c8893f6b658bb69eda859a84433125ee84822111e0c0a5b7b3f430d8f050db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2538296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c1bde173bc9ec1bddca3ba2142ba1c525c97c1672defa43019c59890841e78`

```dockerfile
```

-	Layers:
	-	`sha256:65b758d0a3ecd7de5407a8fce8fa7f848c07905da3aa49685928d60eac5b5057`  
		Last Modified: Tue, 16 Sep 2025 00:10:32 GMT  
		Size: 2.5 MB (2526950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5b6ba17eb47e761a040f6a1757cb31cd8373094ae3cd82db24918da09c0dfc7`  
		Last Modified: Tue, 16 Sep 2025 00:10:32 GMT  
		Size: 11.3 KB (11346 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jre-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:50fdc27cdcda5c2e2e490a1cc0468de2574bd37be87f1f11a3d7e5e0b3b4e53f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95995589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6246c3edc1f34a18a0afe63056b37d061165d6769611ae4df509c84f634be95c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:20 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:20 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6e65450babdeea723d3fc3fc96838a771f8450c62bb8f26a0adca6a0029917`  
		Last Modified: Mon, 15 Sep 2025 22:25:41 GMT  
		Size: 67.1 MB (67134272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2671a946a236ba24028fb3d53f496d0189444a67dd949839cad6dcc448b3778d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2539057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:654a916be766653ee975e3561f4fecd64417224c5a9bdcc2f244c748beba0dd9`

```dockerfile
```

-	Layers:
	-	`sha256:3846f5aaeccebdd7a35fe050f5cb8ca43d434e5e809cd93ca02ccd4b4e5e60dd`  
		Last Modified: Tue, 16 Sep 2025 00:10:37 GMT  
		Size: 2.5 MB (2527511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:262cf5bc1af72bd82f1c752ccdba54a7e1c19c56da8b7fffb5d876bb9742c4e1`  
		Last Modified: Tue, 16 Sep 2025 00:10:38 GMT  
		Size: 11.5 KB (11546 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jre-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:e00fb6f620e3692a4f65dc54e16169c5c362be8d81bf191d9a7badb874a43f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.3 MB (103318830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8635c997aed8bcccf2cd5367ed7a23184266dfff06524f93b1966857bf73d97`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:20 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:20 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:20 GMT
ADD file:e9d760118b96af8e8cac849fade94b73f63176864a676545ce75488d38f30dff in / 
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Tue, 15 Jul 2025 19:58:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a6b4a89244b131752ebf5cc65f8db49bc0ff54baddc21f51045db73ecaae806f`  
		Last Modified: Wed, 10 Sep 2025 16:24:52 GMT  
		Size: 34.3 MB (34303127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09723c63664d96d579b7f87b4938bf67ad332fd90a321c7e7487c51f49097f46`  
		Last Modified: Mon, 15 Sep 2025 23:38:45 GMT  
		Size: 69.0 MB (69015703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4625334a4d0c4c194f6e8871fa6d02b20a8105792485ec058bc4dacae276338c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2535862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf38d3f76674cffde81ef6b24460cffe1a86927d16686f5eb899195dea0a5f5b`

```dockerfile
```

-	Layers:
	-	`sha256:f7b1b3f2f352a65334ca33194e9a485ee7bbfe3ceabbf86813ad864c32552220`  
		Last Modified: Tue, 16 Sep 2025 00:12:59 GMT  
		Size: 2.5 MB (2524425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6c49c0a932aff34799be275e21b86ed8133aa3ed1e79021c063e828406c1d1`  
		Last Modified: Tue, 16 Sep 2025 00:13:00 GMT  
		Size: 11.4 KB (11437 bytes)  
		MIME: application/vnd.in-toto+json
