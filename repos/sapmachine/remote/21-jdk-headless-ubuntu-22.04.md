## `sapmachine:21-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:7ad9fd10c22cc4797b2086c39506a53f539bcaf4bd2f08bf1c3ee86ce04fcf97
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:02e81e339fa17a630b01395006f33bedf688579ec8eaaf3fa1d6d192cc2cc97f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.4 MB (244425085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:798b458dcafa64842760c55ae00f06ce08e3d8a287afb31c715a317e3d42d826`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Wed, 18 Feb 2026 19:23:33 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Feb 2026 19:23:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 18 Feb 2026 19:23:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5f43ff5e5f7b40d8f72c78da1a60aaeb3a9998b67c985be762ce6b15b3f3b2`  
		Last Modified: Wed, 18 Feb 2026 19:23:57 GMT  
		Size: 214.9 MB (214887719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:aa51804c55b141b8ba7f2384614abc8ef72a1ca356c045334269bf9d05e3e628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2388971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b640f3e5a7d0b748156474c6c483dc0631378d4f5c65bff06c5860f2ac4791a3`

```dockerfile
```

-	Layers:
	-	`sha256:4159aeb3adaf47779727f94327da67f38f6cc5ffa3fe05525b8345f2de5a6490`  
		Last Modified: Wed, 18 Feb 2026 19:23:51 GMT  
		Size: 2.4 MB (2380058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5209fd9f4ae2138c7eaf224ab579b489f22b8d190bd942f90ed6ad77e5f716e3`  
		Last Modified: Wed, 18 Feb 2026 19:23:51 GMT  
		Size: 8.9 KB (8913 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:6ee3cfb2e5718b8bb1d3d27f96f1f5a24938d769157daeb05262c0faa583a6d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.5 MB (240486028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b85b08b824fc603c500a9369dae07ce3080e4950e552679bd0d9853b261d8a47`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Wed, 18 Feb 2026 19:22:08 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Feb 2026 19:22:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 18 Feb 2026 19:22:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65cdfe2335ee79ba10038cfd0db42edadd207fafa3baeaec13decf1bd4e25451`  
		Last Modified: Wed, 18 Feb 2026 19:22:31 GMT  
		Size: 213.1 MB (213101084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a24d0f66ed7b7077e992bfe0035170ca9a8c5838e32efbbc6c1953a3aab37554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2388748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00483bcf727ef776446802222d95a181bdd06c765f9423bfeb3dccc3927bb989`

```dockerfile
```

-	Layers:
	-	`sha256:53de9c1471a26c3489cf709562d521ca11e0726165bd1b2e8a443c00843a3abf`  
		Last Modified: Wed, 18 Feb 2026 19:22:27 GMT  
		Size: 2.4 MB (2379730 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac067ab62f68fd7ba6706349e550e1bbe3984cb3898462819f8f5fafced7b731`  
		Last Modified: Wed, 18 Feb 2026 19:22:27 GMT  
		Size: 9.0 KB (9018 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:87635681a10637eaf64cd30574e34325638500da4a42f2c3723f23e49274e023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250122235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67a51702e558cd4cce35e2face6280fcdf8e81f93f32e883748096d46177bb1`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 10 Feb 2026 17:41:33 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:41:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:41:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:41:33 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:41:39 GMT
ADD file:0418bf4995f9b54380cc1e509e3f7d65bb07aed9a367528d0b1084f0a34f3bf3 in / 
# Tue, 10 Feb 2026 17:41:39 GMT
CMD ["/bin/bash"]
# Wed, 18 Feb 2026 19:18:27 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.10.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 18 Feb 2026 19:18:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 18 Feb 2026 19:18:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:95401e425d899946469007a0ce4b02622cf84a67cdd684aa25d61d472fffc38f`  
		Last Modified: Tue, 10 Feb 2026 18:13:52 GMT  
		Size: 34.4 MB (34446102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d8fb1f39b3c120abfcf98b51c32153f1cd4a57fbbd4d2a96cf6b948c871452`  
		Last Modified: Wed, 18 Feb 2026 19:19:22 GMT  
		Size: 215.7 MB (215676133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2cec6f1ab9c9872a02e78b87db22f5cb0194a8b6a65f70652ed93cd420fa5d05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10ea66c2fc6eb5532d3b0076f0003bf9f059e448f9e1fbd69eb970ed5b16d7fe`

```dockerfile
```

-	Layers:
	-	`sha256:8b77101fc0e61221d5e190443bedb3dddb39c5193e91acd6ce127e8113500f47`  
		Last Modified: Wed, 18 Feb 2026 19:19:16 GMT  
		Size: 2.4 MB (2377554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4930c8b54c9b55888ef402f95830ea426d7131570a738b6426d94b5daee040fa`  
		Last Modified: Wed, 18 Feb 2026 19:19:16 GMT  
		Size: 9.0 KB (8958 bytes)  
		MIME: application/vnd.in-toto+json
