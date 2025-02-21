## `sapmachine:17-jdk-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:ea164b7b10819cd6f152e6f5fe70ad19e9e591d7b495569c3bd9697c1d4544de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:d7315b327b85d1e02d743e789630882a4d9c72336c9a7fff0e97e6efe42fe21e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228870768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c8d6924833e01a93db45044834d96cf51eac8254ad494ec82f22bfdb13fc155`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dc4e80818ec2e45a8d557f1a0ce8e75621ec1489b73f0c286bba21d82ccd5b`  
		Last Modified: Tue, 04 Feb 2025 04:49:49 GMT  
		Size: 199.1 MB (199116478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bb757841a91e73bb24c0e59139145af8e85c7baedcede7666b303c32bfae97a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2243438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:141144a2f8dc4e096698a31c73a913b89de31680fa7bf7778a0a959633562480`

```dockerfile
```

-	Layers:
	-	`sha256:7cfab3eaff4e035bc408646d244f34f076d635b53a38157e0f8f656866271989`  
		Last Modified: Tue, 04 Feb 2025 04:49:44 GMT  
		Size: 2.2 MB (2233819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:743870a148547f5ae2aa6db083318095eff821b8087f1c0c522789b70970458e`  
		Last Modified: Tue, 04 Feb 2025 04:49:44 GMT  
		Size: 9.6 KB (9619 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:01afca54522984a5d39fc0dd6956e8ef10fe055465869a71f49a33f2d662743d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.8 MB (226761293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e28cc993cc4298a791597a70af1f8b742ea4d1b4d7330dcccfe9874b08ef6a55`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b725a493bfe78ea4cf25dade34ed3339998a213eddb7462c6022d9a6b4025e68`  
		Last Modified: Tue, 04 Feb 2025 15:35:05 GMT  
		Size: 197.9 MB (197867695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b3062aac11a14dccbfe8b9f094671575485cb630668868ac8ffb64e75b654aeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2244048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55aebd5c0ecf33ebb87efac688a039166d36f17deb06742b1c0c960a0098a495`

```dockerfile
```

-	Layers:
	-	`sha256:f154298e91c718eb52b8dcb1d5df7b559890da2db6e97fb8e222e62a0e8dbcdd`  
		Last Modified: Tue, 04 Feb 2025 15:35:01 GMT  
		Size: 2.2 MB (2234302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f516a88a005f2faef8cb0b46e3dd8c331af9f30dda0f273cd5119c571f6603e`  
		Last Modified: Tue, 04 Feb 2025 15:35:00 GMT  
		Size: 9.7 KB (9746 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:e78053027064fb9d6be8aba09ebe7ae815c9ece209e31e295828289ff75b1299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.5 MB (234507009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffb4bbbb78a7af2813ad13c514db414c570093909f9062580dfe988e6b53d0f1`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:16:03 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:16:07 GMT
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Mon, 27 Jan 2025 04:16:07 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8f72c02908d3bc8d07c12fb801bdd91e344f494f544fd989473501e0e8aea6`  
		Last Modified: Tue, 04 Feb 2025 14:51:00 GMT  
		Size: 200.1 MB (200117185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ad14c35e545d666d55116f77fdf78356a27c7ca0eb64096d98a3e7a4f143b999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2245436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc9334b787eb5169a0a8b15771a39377f7782bb0a70d2442164c0ef7f095f6f`

```dockerfile
```

-	Layers:
	-	`sha256:98c04cd06d165c87dd4e58bdc5f30b506898ec823319cfea9994770209588137`  
		Last Modified: Tue, 04 Feb 2025 14:50:55 GMT  
		Size: 2.2 MB (2235761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:960458e8e6ceca69ba38b518daacf3c401e9f0675c3f3be6af282da6af036f5e`  
		Last Modified: Tue, 04 Feb 2025 14:50:55 GMT  
		Size: 9.7 KB (9675 bytes)  
		MIME: application/vnd.in-toto+json
