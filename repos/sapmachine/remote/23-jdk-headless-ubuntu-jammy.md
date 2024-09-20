## `sapmachine:23-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:eee5e48c7fd97acfddbf81572245f923ee85921f4181f799faab75c9e5e7ab90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:23-jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:08c5e442affa9c4fe7f8329fd1386a8632ed99145d129e0d178da9e1091f9180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250117700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f52c8470caa1382bdc8fd6133150b007c695b992e4a86519582c1a2d47ee469d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c09f4f6cb1733b37889d6f3f1106df49d455d3644b0f87da770d6bd18663d83`  
		Last Modified: Fri, 20 Sep 2024 16:57:56 GMT  
		Size: 220.6 MB (220582012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c482419bf35744cbd0294cbc30d7b4066741821ef386549e5d6cfccfdf3c1c26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 KB (11065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f6afefb7d5e5274f075e2696e64be16a72c423dc3ff1dc0f628fc73750c50d`

```dockerfile
```

-	Layers:
	-	`sha256:d4ecc7bf128f8751ab32128c45930567762ee9ecadc31b51bfafe4b76549ed99`  
		Last Modified: Fri, 20 Sep 2024 16:57:53 GMT  
		Size: 2.4 KB (2431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1abd049af8e274fb4d1178d7fe2e946f5453e4b986383ca9644b1b521aa01e30`  
		Last Modified: Fri, 20 Sep 2024 16:57:53 GMT  
		Size: 8.6 KB (8634 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:7fadb65355c4a910799df12ee1f824063a4c247dc110bd700ec0c6e7a217ca8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 MB (245870317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad0b56c87d16b905561dac0167c81a736724ccc3df302dd07a66ccd74701eb2`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ebfb7fac5c083c5f8362a043ad4a3e46c217da8d449f8b5ca3345213f072d1`  
		Last Modified: Fri, 20 Sep 2024 17:07:28 GMT  
		Size: 218.5 MB (218511988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:eafb658bfe484f3b2c7c93c3e75c9701ff322f0861ace9bd80be1c44e14f24ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2240334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d623a082eff19326994d3f24fb3cec63d082766ffa26a37e4ec54c472f3bc879`

```dockerfile
```

-	Layers:
	-	`sha256:389465f5e359aafe85318e3cfa5a489ed73e86eba0852e93f59130737ca597ea`  
		Last Modified: Fri, 20 Sep 2024 17:07:24 GMT  
		Size: 2.2 MB (2231400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05ee08c27392b8cf29c7edb8edb7a518849e31ba3b112b8d0e0d49dded17d462`  
		Last Modified: Fri, 20 Sep 2024 17:07:23 GMT  
		Size: 8.9 KB (8934 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:707d2382fe41c02e7cb106a5c0fea489a16e1e00f2ff6c4682403693527396eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.8 MB (255834297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13fe281321cd1130823428fc63379132db012f3979f9ea5cf0a53d289570eb0f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 13:42:45 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jdk-headless=23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 19 Sep 2024 13:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Thu, 19 Sep 2024 13:42:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a95fb03619fbb727d6f59990d188acf938ee5a6e11398b4e208f0f59f5cc21`  
		Last Modified: Fri, 20 Sep 2024 17:09:33 GMT  
		Size: 221.4 MB (221386055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ddee92b4e9571630cb00b2b8cc3631f23a90879fa4077652753cb7c729d5d074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2242374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5bc9144f99d51da454cd3363581131489fbb89b95155ca896c891d2330a6784`

```dockerfile
```

-	Layers:
	-	`sha256:a337b8a699e41ffa69528870e09028b53814cb78fffdf010f061fe09d5f899f2`  
		Last Modified: Fri, 20 Sep 2024 17:09:28 GMT  
		Size: 2.2 MB (2233702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1571ffbf0a3a15ec99534e441a56e3f3c1dbe12172b4bfc7013a2f5d128016e`  
		Last Modified: Fri, 20 Sep 2024 17:09:27 GMT  
		Size: 8.7 KB (8672 bytes)  
		MIME: application/vnd.in-toto+json
