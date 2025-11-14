## `sapmachine:17-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:9a2a5bf95d85f7a81cae9e3bfca41c8193d73bb35f812cff7e7f2dfa286762ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:385c9ddfe0cd56e0f4d79cb65e60605fed6100f863bb72bd721377a23fded2f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.3 MB (82255318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a641d395f56475f47ff592228a1c747173c809d4b077681187f101d15de004e6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:39:52 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:39:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 13 Nov 2025 23:39:52 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c2b66c2eee298a21be79ee92ad0e2fd659c2977223bb41fbfc6397140bea0f`  
		Last Modified: Thu, 13 Nov 2025 23:40:16 GMT  
		Size: 52.7 MB (52718520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:78d827f4b3544d1a5b2d937931c5ccd3604cece6f603b964a38f7480848e9b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66cd95c003d0945a7729c658e62e21297848198fbc8893f6232e6a18cd2045f5`

```dockerfile
```

-	Layers:
	-	`sha256:c43c778e2c279a315e2a5284e7098d5d58135ba362cb2010827726b32fcf17e9`  
		Last Modified: Fri, 14 Nov 2025 01:07:35 GMT  
		Size: 2.3 MB (2292859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e69af98134a9c9ff713fd7567a849101cec823a892bbffae1f4ff63b04aa14e`  
		Last Modified: Fri, 14 Nov 2025 01:07:36 GMT  
		Size: 8.9 KB (8884 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:03cab84d97e173e23d31906f346440366474dde5c7c552943a8c07777137c5a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79476707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:983cac71c24adb2a03eb139c1df2b3e255f45ae00f63a6fad2999bfef91a9fa4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:39:05 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:39:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 13 Nov 2025 23:39:05 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838fd0d43207f3fa990dda0b1d66063d10cac19901c52b6d4bd945bbfa8b0c2d`  
		Last Modified: Thu, 13 Nov 2025 23:39:37 GMT  
		Size: 52.1 MB (52092830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1209b9f17c33be2a4d48c08cef5eab034b57b51f72bdd60dce91f54d72d47fe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2301519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:677cf63554ba451fe63276c36accd541aff1f5c475641941e2298ed2e20430f6`

```dockerfile
```

-	Layers:
	-	`sha256:b06ad1645810de3a52965c74caeb03f01bb75152d855de4034a11d32a8d3906a`  
		Last Modified: Fri, 14 Nov 2025 01:07:41 GMT  
		Size: 2.3 MB (2292531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdf15b4b60ec836906c8a9c6899cef29b7dba42624aec254a59d6479d1b18513`  
		Last Modified: Fri, 14 Nov 2025 01:07:42 GMT  
		Size: 9.0 KB (8988 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:0a566c7c6353f879bef0525a9e9cc6164d84903142e6e1aa3556635a26e51247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.1 MB (88079074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e77cf395a2c00e9b707da1a6ccb1b2ac87a03070b0eb07f2e1cf4b98585ff18`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:28 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:29 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:33 GMT
ADD file:7facf0edece2a424143eac2311620688af083f73051d20a5e4ebb604f70a10e7 in / 
# Mon, 13 Oct 2025 17:25:33 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 01:56:45 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.17 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 14 Nov 2025 01:56:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Fri, 14 Nov 2025 01:56:45 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:88caf89e8ab279126b8391c59b37ac1fe7f1e90f49fae3f4861f0d045bd02806`  
		Last Modified: Thu, 13 Nov 2025 23:02:18 GMT  
		Size: 34.4 MB (34446722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b56ef927b9631d4a34c334f236c9b3631081e7a40ad7f1d49f3647c84713863`  
		Last Modified: Fri, 14 Nov 2025 01:57:31 GMT  
		Size: 53.6 MB (53632352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2ca40ad3d7ef01c99cc3ddd2528b784abb41af28afc4d64dbfd884d74a8dc68b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2299813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68c98905618092e1d296bf8120b211132b60336b027000731de87ada8a0a1f0`

```dockerfile
```

-	Layers:
	-	`sha256:c73cb44b75f83f22a63ab80fdcb9ca507806e51c4bf92cd517043c598c1486d1`  
		Last Modified: Fri, 14 Nov 2025 04:06:45 GMT  
		Size: 2.3 MB (2290884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:122c6de3a3f0af5b4e56eda20e212d446fa45d2db682ce2fd3a4007561020f67`  
		Last Modified: Fri, 14 Nov 2025 04:06:46 GMT  
		Size: 8.9 KB (8929 bytes)  
		MIME: application/vnd.in-toto+json
