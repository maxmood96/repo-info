## `sapmachine:24-jre-headless-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:00ebde9ed351ecc8702e3eba15075525b464fedfff449f1085f98c5b75897104
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-jre-headless-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:7a3bea7224ff7d26561ac96f2de49ca834d6d8df04b12cc8716fe76e5204f2e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93538871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628f71aef8b256a4fe3d85c3ca4a1ea64b4b117a9956e94318a7d468ea597d07`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3090478be6817190b59df8dd2d3fdc7708e06894e08a8183a645e876f9a043d8`  
		Last Modified: Wed, 16 Apr 2025 16:13:47 GMT  
		Size: 66.0 MB (66028477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:162c3b7cda4ea8c6227e27c673cd4dc5791f5f6ec3c29f171ea7f67f6d46da99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2080027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5bfe95e735d1f6b75a38467db6b3c399925b15f6a7fb946c3cebafbff9ea165`

```dockerfile
```

-	Layers:
	-	`sha256:9cd6778ebc5d7193ef525a14de9f494ab02db1c83eeeb917d3ea78ab1afed654`  
		Last Modified: Wed, 16 Apr 2025 16:13:46 GMT  
		Size: 2.1 MB (2070416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89342babf15e43b0441e59b98aaac2c0a0837e50385c74b04e7fea186ab2363a`  
		Last Modified: Wed, 16 Apr 2025 16:13:46 GMT  
		Size: 9.6 KB (9611 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jre-headless-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:6af3836b117e514b2b8c32761fba09511fb82cdcc8cf2902cb8df8ab1657bd31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.0 MB (91036192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a63c3aeaef35a8e9bcc076553e7d392cbaaa3f7ac7ec830a792ea4f0f1685c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:43 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:43 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:43 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:46:45 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 08 Apr 2025 10:46:45 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c67333bc136e86b3dacb95dece91fe0c090b24b361b56601fe94ae8c9d3391e`  
		Last Modified: Wed, 16 Apr 2025 16:24:59 GMT  
		Size: 65.1 MB (65058531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:52f083c6f51385778abd59feebc03700c5d9dc979194f41ab09b81c034e759a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2079805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:105860c20532056892fd86b7347431a959133402d2a3ccf9159967b305f10b25`

```dockerfile
```

-	Layers:
	-	`sha256:22cae3940bd0482f2149a619b3913d82c69ed98f608061efda4ccedcb72ca47f`  
		Last Modified: Wed, 16 Apr 2025 16:24:58 GMT  
		Size: 2.1 MB (2070066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be0e88f84ebbb70f58807a2114bf72bcf8c7f4429d0b4e9be1bb2f233e200f50`  
		Last Modified: Wed, 16 Apr 2025 16:24:57 GMT  
		Size: 9.7 KB (9739 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jre-headless-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:0aef1b4789d80c39caf42cb89735489e2950902c70e33cb0dd4eac44981fa451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.8 MB (98835152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f6959562e8fb4cbad6b31f85f25d60e52d7403a95465aebfb298bc3bd9d3723`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:47:01 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:47:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:47:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:47:01 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:47:04 GMT
ADD file:d85970cec61787609e3854cb76ce16d54fe420b254cf48fc9ed9ed678717ff28 in / 
# Tue, 08 Apr 2025 10:47:05 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:92d54367a68b4f03400315732acb4290d88bb06f8fe1414fd823f93402bec922`  
		Last Modified: Thu, 08 May 2025 21:39:31 GMT  
		Size: 32.1 MB (32076946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02b3c6215c91feda5773d3423cdbcba3dfdd06f8588901d85911b5c0724343f1`  
		Last Modified: Wed, 16 Apr 2025 16:38:23 GMT  
		Size: 66.8 MB (66758206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-headless-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a6450ec54980f9b9e0663e54ccea6859b425faaea8e50a4ca79a3c7317c71b63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2083169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6618172a097c1918025dedd41a4bd8ba5eeb9064028799d913eeb4383fcd36a`

```dockerfile
```

-	Layers:
	-	`sha256:5a76b653516b645dbf969282f8c7578f0d410aea521829b704522c22b4894d61`  
		Last Modified: Wed, 16 Apr 2025 16:38:20 GMT  
		Size: 2.1 MB (2073502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e42bdafb9fe5686aa769f981a87aca9716e15a5dc9ac38a59f6b1973f4f54fcc`  
		Last Modified: Wed, 16 Apr 2025 16:38:20 GMT  
		Size: 9.7 KB (9667 bytes)  
		MIME: application/vnd.in-toto+json
