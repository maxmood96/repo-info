## `sapmachine:jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:215c611557b11cba5825e7365fe7ffb42cdc78859595590cbd469fe11f2327f1
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
$ docker pull sapmachine@sha256:3dfb4b15c87dea7d101b886756142855e99d30b00ae9ec00bd1eef1e3fa68e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.5 MB (87450718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7182bcf9c0495bf3fc289bfb0b78d9a6ab363007bcad8018b0cf246815f4f192`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1933ea20e815622b28c36ea300483dcac41fb829e80a37ce420bd514d3c1a3`  
		Last Modified: Tue, 17 Sep 2024 01:00:56 GMT  
		Size: 57.9 MB (57915030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4d338f9d1e221fd9dbd359d22e8190f0192856ea1dcdbb175cbaca23727e59f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2157486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af0ac041de5e60d367735d18426d301d783c66983e59a0271e496fde73c68f1`

```dockerfile
```

-	Layers:
	-	`sha256:16df2a5982a7328805721613987f637bb0e4896cd6dcd7faf4829e475b0b30b8`  
		Last Modified: Tue, 17 Sep 2024 01:00:54 GMT  
		Size: 2.1 MB (2148130 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d501ae11059b2ca39aa90df6388d74d9e66cd15f06aec71520fab6391b19fc95`  
		Last Modified: Tue, 17 Sep 2024 01:00:54 GMT  
		Size: 9.4 KB (9356 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:0bb8ca6b1400880d20c1d16b5468c9882b70aa328d512408c0074d3182a26ee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84271557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c80ae7226fe6feb5c1da65f4bf8a29d624f49c32ac2f57da05efee30e6d8ed65`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd83b2b8568bc22411fa5ac71e1bd8f00765f12980811bc71e0e10dd37135406`  
		Last Modified: Tue, 17 Sep 2024 03:16:06 GMT  
		Size: 56.9 MB (56913228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6ef5f39c987af04d49ac019e8042c4eff39754fb904112931a812a29d6d9385d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2156875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031b2c62ee2524cba79b3fdc070b6ee581d2edaa040def6b7e562e6a3f673e6a`

```dockerfile
```

-	Layers:
	-	`sha256:149c16fe0df890664f2a3f58ea09fb853eb555d086276daae2cb60db78776637`  
		Last Modified: Tue, 17 Sep 2024 03:16:05 GMT  
		Size: 2.1 MB (2147193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b30a546bc9db2a26a174115acaa811ffa454a6e082c2234f19cd99cc34f72e0f`  
		Last Modified: Tue, 17 Sep 2024 03:16:04 GMT  
		Size: 9.7 KB (9682 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:3ae3d2353d919ca73d2111b460210a2dc04c2ff3aa4f4a551f8deae1a7c2f748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93621256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e8957a2b4de51c87d262b80cefc441d0d897272a47df0618ff0f33f9f84728`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre-headless=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88e3c555b09f04065954f379eef94f7a5c91f0ea767100afdf0658aa213de31`  
		Last Modified: Tue, 17 Sep 2024 02:28:30 GMT  
		Size: 59.2 MB (59173014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a661ca8ee4d9f4a111b75ee677e7fc326d9179328d93aba246a182da809df6d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2160827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b03e328f023b27af054a1268d2f646a2f9db615fb885301e2df6909da04dcf`

```dockerfile
```

-	Layers:
	-	`sha256:cbb63a28760731d26b0cf103f5725b24ec57f7f905ec6f0654b6d7ae3d3c920e`  
		Last Modified: Tue, 17 Sep 2024 02:28:29 GMT  
		Size: 2.2 MB (2151420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b69c3d6bf10490584c368de3fc52a030aefccdfb0e2c00e12ac69929faa232ed`  
		Last Modified: Tue, 17 Sep 2024 02:28:28 GMT  
		Size: 9.4 KB (9407 bytes)  
		MIME: application/vnd.in-toto+json
