## `sapmachine:jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:2ce48d17767d3e79ce94c6da1e9bc5fdfcfe2a003fc7d69f6db73b6b1363c4de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:ada266046f6d38c5a9ebf63ad8fccc8b969eb5ce4b35dea4df38cdbe0b52cb5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.2 MB (85209401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a42c0260641623351ad7a1d8d037c27855d6bddea443388706609f4da4a9cef`
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
# Thu, 13 Nov 2025 23:38:07 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:38:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 13 Nov 2025 23:38:07 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3d51bfa88546228a9900a5d72616b886a15a1b2b53cf76c39b939225230143`  
		Last Modified: Thu, 13 Nov 2025 23:38:35 GMT  
		Size: 55.7 MB (55672603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:38f2b18b76ab4ad05187b801115aaf238a3661a4845992fd65441b5c248b8544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d19f34ae8b9eb164d5d4c65ccbc48f19f0e708ffb70731279c54b0ce434658e`

```dockerfile
```

-	Layers:
	-	`sha256:42ef326e9647839373bfa87be8d4fc9170d0e1d01266725769775e79db6e290d`  
		Last Modified: Fri, 14 Nov 2025 01:13:28 GMT  
		Size: 2.3 MB (2300655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35778c990725bd0fe62786cbe531b64784826c4513f90ae8061620360f24c983`  
		Last Modified: Fri, 14 Nov 2025 01:13:31 GMT  
		Size: 10.3 KB (10272 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:cc7b68a6c0f023ed5cbe424d641573f968c0335d17181c131a570a21b4a3cf23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81945156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e30dddc9bd499bf6a9f308108e3f0289fcf38e2475f4848dd327efada6ad8eb`
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
# Thu, 13 Nov 2025 23:37:23 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 13 Nov 2025 23:37:23 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8159e1ba8c4a0d34c1dfca7922e2270186b490879387989860e41cab308a76e`  
		Last Modified: Thu, 13 Nov 2025 23:37:45 GMT  
		Size: 54.6 MB (54561279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:58c55b06c8323cff10bbac1a5252e9d37868a17584ae92247b6afa9d1769413e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2310796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c1c85b70ef80cf2fa704dacaba11e3d07888efb62a6535c440d7e37fa852107`

```dockerfile
```

-	Layers:
	-	`sha256:6b442566aae8fc0577949a46d47f7e24cfd4e7f2f928411cf125dc17dd7d1d6a`  
		Last Modified: Fri, 14 Nov 2025 01:13:35 GMT  
		Size: 2.3 MB (2300372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:603940e8efc84852cf0eb770e9e98d01e4db65ec00631465708e46eed0f279d4`  
		Last Modified: Fri, 14 Nov 2025 01:13:35 GMT  
		Size: 10.4 KB (10424 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:0ce2b7ee59a4330f67941c6ac42415e5c249fbb5b11d0424009b6d042f1cf9f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.7 MB (90736753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59047c7e68e72f4ae6a16d973d9ab61ab4c9e3addc70d822a926ee421e88868a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Oct 2025 07:06:37 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:06:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:06:42 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Wed, 01 Oct 2025 07:06:43 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:17 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Oct 2025 21:30:17 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d841a0a60144b98f709a389854575d04c5a229584626add443f4c4b2c6c248db`  
		Last Modified: Wed, 22 Oct 2025 11:45:22 GMT  
		Size: 56.3 MB (56289964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:be5e72d2de5f5429f5b9ecff03c0a7c3d36ba2aa994c1eea8149699dca6662ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa776f13fd821b5b8521cbc04d1c835743ec7691118fd30ffb6a7423598df3e5`

```dockerfile
```

-	Layers:
	-	`sha256:78d8756e8e22174c3f39762afd0d3d2a98400aa78ffcecde9b957eca464bbf50`  
		Last Modified: Wed, 22 Oct 2025 15:10:51 GMT  
		Size: 2.3 MB (2298074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fee79ba69f9132c07d054838dfc2d7e7e468e974be0a576c419dd5bb4596aa41`  
		Last Modified: Wed, 22 Oct 2025 15:10:52 GMT  
		Size: 10.4 KB (10383 bytes)  
		MIME: application/vnd.in-toto+json
