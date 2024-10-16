## `sapmachine:11-jre-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:e013a38f64bfa5d23362bd0e5584a2f04d69dc5d8d9f2664bbeb38ad3dd2c643
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:a87a1572af78437736fa9a1ce64cbaeb9617c5235b5ac5a529dce17195b2fb03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78895677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71bcbaf0698261de900e3c9fa6e059c354f09a00f570e80e65b66a64864bd7d9`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:34dc4f3ab7a694ecde47ff7a610be18591834c45f1d7251813267798412604e5 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ff65ddf9395be21bfe1f320b7705e539ee44c1053034f801b1a3cbbf2d0f4056`  
		Last Modified: Fri, 11 Oct 2024 05:07:18 GMT  
		Size: 29.8 MB (29750363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508d119ca3496fc49a9e442e8bbe398e9eddb5dddc47e67023d695889f147012`  
		Last Modified: Wed, 16 Oct 2024 16:18:14 GMT  
		Size: 49.1 MB (49145314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1647bf272959d269b990c11089380d2a339a47dba01b909d2652aa8444639560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2148783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8016ad8d30913c8353a4353c61287873ca490b3991e67f2fdc35e0a26432b3a`

```dockerfile
```

-	Layers:
	-	`sha256:cbe10158aabc0134e02bc90d1e0e6304f164e1106add6d3b95739d0fd45b0687`  
		Last Modified: Wed, 16 Oct 2024 16:18:13 GMT  
		Size: 2.1 MB (2139382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edf5a3a81c56c7815af52b6b17ca0e871c3383d3417a95119b1a0118b0565401`  
		Last Modified: Wed, 16 Oct 2024 16:18:12 GMT  
		Size: 9.4 KB (9401 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:c9935fa76fd22ee977b99691cd24b31f2f11672039ced84db1c8bb2e5da0c169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77368371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:268c306d66fcc9a448908a8a4ba069b31f1ceb9aeb8dced9830d06ed2234170e`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:b14427a5ec8028ba993a0ff27f9e398456229f9113c9c39f3cc7a0f96c15943b in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1f630473117188fe348ebdcf0da5e93138275af14007f15baf79967a365e647a`  
		Last Modified: Fri, 11 Oct 2024 05:07:24 GMT  
		Size: 28.9 MB (28885845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8fafb54fd7080a222d23cb42e9811fd8535c96a9418420d7a128c9ec15b4909`  
		Last Modified: Wed, 16 Oct 2024 04:50:03 GMT  
		Size: 48.5 MB (48482526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fc4f93f22d1c153d309cfe88f8e11615473d8fa2d88fdc91a5f7bb16a51db523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2150014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da170455ed4b54d6865a26a14fdb736b9df565c7eb510582e288cd8d43f0162c`

```dockerfile
```

-	Layers:
	-	`sha256:5830f77eec6a408fe09537f382249782b137a64e7168c1c8390c798ac09e383a`  
		Last Modified: Wed, 16 Oct 2024 04:50:01 GMT  
		Size: 2.1 MB (2140492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:707279a76f91c4fb0b6b0f1bd93ae0990b2e51e8aea68c1d6ed8dc0d58c850df`  
		Last Modified: Wed, 16 Oct 2024 04:50:01 GMT  
		Size: 9.5 KB (9522 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:057ffcda753361af6071cd275059a3eecf58d5617252a1cf4b07e8f3352794e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.1 MB (82108183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad2f4e2442d644fdffb4d2c60fec0205884d038d76296ab94e415689ce3e78a4`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:536f7d2a284525103973196c539c45f59251ee1d6bbd34f1d92ff9d6187da127 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5f3161c1c329da2d67fc0650c9fd31e151f03956f8a0cb901012dc9bf6029cbc`  
		Last Modified: Fri, 11 Oct 2024 05:07:35 GMT  
		Size: 34.4 MB (34388969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be80ee7bf0872676f625c06a94222712431dc9ebe655627a35406bde59352d5b`  
		Last Modified: Wed, 16 Oct 2024 06:14:05 GMT  
		Size: 47.7 MB (47719214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7ab57943bfafe11db1dfaea3b34364697c1c835ddba0eb7810d504fe7e347aa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2152726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d762ca560850f7a0ba9f37cb6a55533d2381ac1673146a797b55b8b458a9ae`

```dockerfile
```

-	Layers:
	-	`sha256:ca29ec825a154d2cb038855c97ab01fe586d6aa71bfdbe1e3b21ff2cf9a73e0c`  
		Last Modified: Wed, 16 Oct 2024 06:14:01 GMT  
		Size: 2.1 MB (2143274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:389d12c99793e46866610345b2595ee2ea77085b727960b7c0d2560c34649a79`  
		Last Modified: Wed, 16 Oct 2024 06:14:01 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.in-toto+json
