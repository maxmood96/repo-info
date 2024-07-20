## `sapmachine:22-jdk-headless-ubuntu-focal`

```console
$ docker pull sapmachine@sha256:c5c23941fedf69156aa021468a06bb62f66184d450dffe53b7f97d1d1c4afce3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:22-jdk-headless-ubuntu-focal` - linux; amd64

```console
$ docker pull sapmachine@sha256:f0f47dd21b217ac3afed4845bdb27eb7663865f5ae953ff8910b32b7848e3475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.1 MB (239074160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f840bf60bdd9acafb5fbacd388236b76ab96798d3b79ee968b26191673b7790`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a9a2a837596e17c8538352de031181825c5e68490deb474d07c3682652671f`  
		Last Modified: Fri, 19 Jul 2024 17:59:21 GMT  
		Size: 211.6 MB (211562391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a78b5d8db6d2dfc5847dd78a95995a93845bf87f6fe82c4e99cfa194dffc0e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43ca56b37d9f0bb6e5b0edc048c0636ee8d44c52f1dc2e065b44c6c11f22597`

```dockerfile
```

-	Layers:
	-	`sha256:75fe3e4b557d830b5d7b48a3a4710ae12d554bb4af1189d7a2c8449256822820`  
		Last Modified: Fri, 19 Jul 2024 17:59:18 GMT  
		Size: 2.1 MB (2129209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d6b652be7adeefefb34eb499f8790294cd98e57bc01a188021d7ff0b79e4111`  
		Last Modified: Fri, 19 Jul 2024 17:59:18 GMT  
		Size: 9.4 KB (9357 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jdk-headless-ubuntu-focal` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ff282e3f84820bb3dbe390846e94cbf42835f96de1a742327674dd3463b1e1ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.5 MB (235529789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ee8541f1c3e823de16b416bb66deffb98545f58438cc88fa160ebf57200934`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Jun 2024 16:52:57 GMT
ARG RELEASE
# Mon, 03 Jun 2024 16:52:57 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 16:52:57 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 16:52:59 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 03 Jun 2024 16:52:59 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86223dfc146a3f525bb99e86400e9e63d2ddfd4e66b04aa911053e033fc94f2`  
		Last Modified: Sat, 20 Jul 2024 00:06:16 GMT  
		Size: 209.6 MB (209555572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1dd51f38fc68b14d892c44032ae81ffea43bf29d518c45b580cc505778588f98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b14919185d77ecb30e843b35b07df8e41280d54d6ed83686aabcf243e7157c54`

```dockerfile
```

-	Layers:
	-	`sha256:1e65fc8ea7c1d2fadf3ad0674a8d35f723712d34cd6218178cc6f6aaac9df549`  
		Last Modified: Sat, 20 Jul 2024 00:06:11 GMT  
		Size: 2.1 MB (2128229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad2c8a99b08de565d3076ffa6db22673caac5a4be163a6ce1e2ae20b1063502f`  
		Last Modified: Sat, 20 Jul 2024 00:06:11 GMT  
		Size: 9.7 KB (9683 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jdk-headless-ubuntu-focal` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:04bf4f7cb59ccf183535b42b2256af9a8a47ff3509634d90d21909a14e837075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244192815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c6e0f90e2603b74e47f66021449ad8e80cc05fd8ac5f0f5b415b31254e849b1`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:42 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:42 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:45 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Mon, 03 Jun 2024 17:10:46 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4a7950ce0ddccfbc041f80700d6161caf71b672bb101dede4427ad4e908502`  
		Last Modified: Fri, 19 Jul 2024 23:06:52 GMT  
		Size: 212.1 MB (212115675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jdk-headless-ubuntu-focal` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fab387cb7352580b3df1dee32ef2e954de2eae8e5a5c4fa1f4bbe10baa024e6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2139763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf3ffbeba8ae978b113fa37c9ed1528adcd60cebc3aaf6c3790816e71a9117c5`

```dockerfile
```

-	Layers:
	-	`sha256:f5c04c21bfb9a264f434a2ac0ec30991cfd0711272c15c39d30c2138666fe731`  
		Last Modified: Fri, 19 Jul 2024 23:06:46 GMT  
		Size: 2.1 MB (2130355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a14815406b92d445ddc33aecf718e54f5f275e2af7382e8554b1a01cc96ca96b`  
		Last Modified: Fri, 19 Jul 2024 23:06:46 GMT  
		Size: 9.4 KB (9408 bytes)  
		MIME: application/vnd.in-toto+json
