## `sapmachine:lts`

```console
$ docker pull sapmachine@sha256:74cc3f68d7bec5a6e1cdf1c35c263e1e5d6048a5698d6d87b248f3776f7de177
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts` - linux; amd64

```console
$ docker pull sapmachine@sha256:b2f67120b8822eddeb033864dc5aad78f58917eb5e485a2dba6ec4bbec36798e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.2 MB (251185154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:361c2368a7829686709a3d275d7b0065cc141d0cabe000bfe0184cbec9698cac`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:23:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:23:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Mar 2026 02:23:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03356429c9f16378949f55501f5e5cc658efdbb0428fd5185fb62ab541ca846`  
		Last Modified: Tue, 17 Mar 2026 02:23:46 GMT  
		Size: 221.5 MB (221453161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f4d4fb1c4f9761aaa14bd4dfef784f95b7028134bd67a2153868f00f2f3ae56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2618697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c898d70675813a8c2364d3387e821361b7a9d3d9531529142e807baa836e061`

```dockerfile
```

-	Layers:
	-	`sha256:541ec3092b74826dde5a9e1a4ea9307de9ef6ccebdcad1e465eaefb4fe1cbc1c`  
		Last Modified: Tue, 17 Mar 2026 02:23:41 GMT  
		Size: 2.6 MB (2601341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49beafbe953fd1d9f00ab36e6a44abe36a5d34476f7fc2b06123be245db25a1e`  
		Last Modified: Tue, 17 Mar 2026 02:23:41 GMT  
		Size: 17.4 KB (17356 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:d7dc82537ee850304c36512684150d8db14866541aeeab76302f741118a9ce6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.1 MB (248136378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8055f24b38594bfe7b5339853798f9d73e5dd5a6979e1bdf4fb506b938b7c462`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:29:50 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:29:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Mar 2026 02:29:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc13511e880c0df6cd7f945fa934e24ae2f33c796fdd717f78075a5af41e430`  
		Last Modified: Tue, 17 Mar 2026 02:30:14 GMT  
		Size: 219.3 MB (219266669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6640be9582247e1fbc9b97feef319a2c9e13b2f042015e0d67be4c85b4bc60af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2619913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d215a46610649c3c90919ceb22b4f37873c276fbc66dbd2e8134c2586ba1da53`

```dockerfile
```

-	Layers:
	-	`sha256:15aac2c498cbf6c3bc21b87f4f7357a25d774789bb60475c661f6335c386a942`  
		Last Modified: Tue, 17 Mar 2026 02:30:10 GMT  
		Size: 2.6 MB (2602130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c98cb19c2de000b38c0fc234a53917f449609b3252d64f20164622d5d9ae992d`  
		Last Modified: Tue, 17 Mar 2026 02:30:09 GMT  
		Size: 17.8 KB (17783 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:8ba7a39ab052e8e032da81dbf3b6969a2ea5efb525088135446a3d0aebf17a24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.7 MB (256661823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48b7c1da4a21d1c6e43aa3a77051183c382104c83a7dde13513556813f6a3768`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 23 Feb 2026 17:18:33 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:18:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:18:36 GMT
ADD file:2a89eb67bf550d9680999e3ff99dbaa17c251b6c343a241318e879a26da53fca in / 
# Mon, 23 Feb 2026 17:18:37 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 09:31:29 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 09:31:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Mar 2026 09:31:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f826c9b754a00ada9d9335ffdf3ffd40f6925a3223caac76cc429823b8621f9e`  
		Last Modified: Mon, 23 Feb 2026 17:51:39 GMT  
		Size: 34.3 MB (34310051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c074f0aa42d34676a7ba30ab23474ae5ac96e160c98d1c3f03f51fe79343b49b`  
		Last Modified: Tue, 17 Mar 2026 09:32:11 GMT  
		Size: 222.4 MB (222351772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8d26f6ce825b76cfb9a5051b21fc7f49f9a6cddc708c75ab6d5889eaa4b4463b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2615974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f23cdf67bf28b7c392ae44e6df944ec203ca2dd284f97fd51bcb5308f8fac9a`

```dockerfile
```

-	Layers:
	-	`sha256:446161e81272030f0b52d2ee630d27c4dbcbb8f98c23d3cdc2f5c0d9db33b23d`  
		Last Modified: Tue, 17 Mar 2026 09:32:07 GMT  
		Size: 2.6 MB (2598413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13e37960cb49606eaf61c6042b26d604270009e21880838958454a2ee51fb3a6`  
		Last Modified: Tue, 17 Mar 2026 09:32:07 GMT  
		Size: 17.6 KB (17561 bytes)  
		MIME: application/vnd.in-toto+json
