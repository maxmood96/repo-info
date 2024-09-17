## `sapmachine:lts-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:d2910d5261fdbc9d669f1942df952e7fafe6b34e5cfb91137ed7156547602f01
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
$ docker pull sapmachine@sha256:317e77022d762f46c8186ef31180dfd0a748638b2e14f864ffca7799f83f1bc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89475423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da2d541fead42b1b91ae02cb02f3965660214bc4548e2ddba9509b21539e093`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9cbd0cc432f50b0f4c446d550c42aff41443bea5034eb1941a79d2069767e3b`  
		Last Modified: Tue, 17 Sep 2024 01:00:48 GMT  
		Size: 59.9 MB (59939735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:52ab93bdadedb0a0e6b16c51ffe4843228f4e9f25553175bd57d73e2a046ec8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ddff7ae827656cd4535b75dd0ffb3ad37825aa6918d5fc4341e2a420c1a7d27`

```dockerfile
```

-	Layers:
	-	`sha256:adb3b9db98dc45c0b8a5717525d6f896c91759e1107973a7d7c8d1d0501b1c04`  
		Last Modified: Tue, 17 Sep 2024 01:00:47 GMT  
		Size: 2.4 MB (2389425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e58d577b0bab4c083a76566418f4234175c799609dbdc50f9ae71be6eaac68b`  
		Last Modified: Tue, 17 Sep 2024 01:00:47 GMT  
		Size: 9.2 KB (9226 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:adf49a1e4343d480b596b28584c226b95bc40d97cb2e69224ae5a7f3ec793ead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86356009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e35aa4e009270c18f718980ddd7d18fda7e96438f4c27f018af9100fd70ec8c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c954a2e37a3febe379ba5d63e5b5945fe45200c62c945013df132472e785c51`  
		Last Modified: Sat, 17 Aug 2024 04:22:25 GMT  
		Size: 59.0 MB (58997326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7e22dfb514e539b443f5ed63d1f0a7fe54ad9809f4ab052884d121da452a803a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e187232f001e3af298f05773b341e5bb8a49da3d19bd97b030c91cac869c2547`

```dockerfile
```

-	Layers:
	-	`sha256:153073c0493fca4b006efb4f69fa5d285c5d34639ada867340e7c229d3b2b376`  
		Last Modified: Sat, 17 Aug 2024 04:22:24 GMT  
		Size: 2.4 MB (2389129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f2767e2b7e505d0a8cb27c06728e8aa4596dd7469da4586df6d85afcfa61d16`  
		Last Modified: Sat, 17 Aug 2024 04:22:23 GMT  
		Size: 9.6 KB (9551 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:eccfb1c099b4208a86f4065c2705299078a49909bc4d898d7de716a5c2cc2118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95951325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff8be612e9187bd70b5f7da63ca5c5b4b54afb68627b741dc83f22970b72aa7`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:16 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:16 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:16 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b7465ce1889fbdcb82ecba7a5c9155c3123041241a3195e70e3aad79717c2c`  
		Last Modified: Tue, 17 Sep 2024 02:41:01 GMT  
		Size: 61.5 MB (61503083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:710124747c377835fce6f1f6b5ac95da6aa35080a07b4f5ea0c2be41c59fcf20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2402691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b99ea69840cd1370e80bd4cb07fb9735d8a9eee6b0aeea4fbcbeca8e994a1283`

```dockerfile
```

-	Layers:
	-	`sha256:b93e0096fe2385d6c65e492d20602ed1c757ded07d2175299638f58dfd1abf1e`  
		Last Modified: Tue, 17 Sep 2024 02:40:59 GMT  
		Size: 2.4 MB (2393416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db237fc8027ad99463716fb5b580ca4ef12d0b21403a18fbe42c39b47d782899`  
		Last Modified: Tue, 17 Sep 2024 02:40:58 GMT  
		Size: 9.3 KB (9275 bytes)  
		MIME: application/vnd.in-toto+json
