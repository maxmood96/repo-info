## `sapmachine:lts-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:a16f7e866e17cd7322e24782e19a4b3453d48f3900758923071c47c3402bcdc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:8ed2e93444f7c6b9db88422de8be8731e04ff945a68b5baf90c1f8142ba3282d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.3 MB (89273611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffd870eb791e59fa97969b91d6ef145ecb278ba8c3a083261e8c9c7c979a0008`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25ab0f54148a1371ea0989f3b2728c44e02e4b6b34a42b63c9a98d1b6786d81`  
		Last Modified: Wed, 02 Jul 2025 07:33:34 GMT  
		Size: 59.7 MB (59737925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:607b075c89f853314bc6f95596c916ef334d6926b4de39e2a4018a6359abca27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2555020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f8e1c7fbd77483043eb7940fdc4cb38e4b065bd02d380d7be447bbb02b163f5`

```dockerfile
```

-	Layers:
	-	`sha256:48c3bb943c03fb7c3c1fbf1e7ff8caff7727800228e593c5ec749376b1a3e55c`  
		Last Modified: Wed, 02 Jul 2025 06:08:15 GMT  
		Size: 2.5 MB (2545541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e04ae2d5e2e4f560560587b0a4b96100c91798e63df68cde463b2370a9f523a`  
		Last Modified: Wed, 02 Jul 2025 06:08:16 GMT  
		Size: 9.5 KB (9479 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:26832bd5fd46ddc81e450d1c58dff3caa767f127c2e3908692a782a70b4b40e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.2 MB (86226171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6adab483b6d1fc270941a2d2302efd568ef349f2032ddb738c8cd82d107b06a5`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed99a447be8182e5ad2f1a1213df34d458580a2e7acdfb1a05aab357733f5c7`  
		Last Modified: Wed, 02 Jul 2025 06:43:28 GMT  
		Size: 58.9 MB (58866899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9bfd293ce05205e269120cc3c1667a4264eb3b1edfb2269a52fde6cd69d4ed3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2554855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fbdffc6973fd409ef53c1c109d7bc150ee45f3bd752d86a589cd17db0c02371`

```dockerfile
```

-	Layers:
	-	`sha256:509480a520a044483bd6be444b585ca7a9a1f52445734be5c76fb5aee1906779`  
		Last Modified: Wed, 02 Jul 2025 09:07:06 GMT  
		Size: 2.5 MB (2545247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:514fd4529045e2e82ed794d8917d55933b83f931e6334986f9ece43378ccbccf`  
		Last Modified: Wed, 02 Jul 2025 09:07:07 GMT  
		Size: 9.6 KB (9608 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:972da0e1c9682da05600b257ff4a328bf57f1c8b25b0753296aca64a69e76900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.8 MB (95754734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91d2d94ee99bb5945e477267211f7acaf0c3a82182cf3eeb85ece462e348bfee`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0f5bc7244cb201bae8faf7a4585a967c9f27beb93ea936c0e5d3d9651560c9`  
		Last Modified: Wed, 02 Jul 2025 04:56:11 GMT  
		Size: 61.3 MB (61312113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6aa079a883d6e3ae9551c11bfeec90e242ddd851d1902cdf654f7a232f768a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2559220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5751dadd61b41a68672957ced1d6c6587d2e230ef20f260ff50a002f646ed6c`

```dockerfile
```

-	Layers:
	-	`sha256:416f14c13f08f15b8c9c545e6e1969d4d3969269ea3f140b4d238df95274dc64`  
		Last Modified: Wed, 02 Jul 2025 06:08:26 GMT  
		Size: 2.5 MB (2549684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:175a65c1fc37c6b157683a3d821f9126d8c2d9cf472500c48be70dcc1bcfa6c8`  
		Last Modified: Wed, 02 Jul 2025 06:08:27 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.in-toto+json
