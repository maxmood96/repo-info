## `sapmachine:lts-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:5efad546bea8484152187170887d80b44b75552351a20b171e899b9f00dafdc3
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
$ docker pull sapmachine@sha256:5eb36c894d4d1a5f4f09c1b3769ba123134512aa802ceae0dec12351acc7e87b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.3 MB (89259170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:012120a22b08cf0831a9dc7516316890e7b29ffa9a1cb15ad2e6d07b9fc12b16`
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
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808d9508bebede5128f7f0273b9443c1a8572c7146c2c49bb5f305d3013cce98`  
		Last Modified: Tue, 28 Jan 2025 01:29:54 GMT  
		Size: 59.7 MB (59723482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:920e262be6450ad28342245f2a9e5f5f532c16094f005910d2e38687713b0aba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2418730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d1ce4b623bb11d5053736d521cb6c66c6adb448e9d18d2e4402ce3b4b13a7c`

```dockerfile
```

-	Layers:
	-	`sha256:2adb3f0e168dc3f61bfb76ac8095e959388f4ceec154e84320a61a3321089aba`  
		Last Modified: Tue, 28 Jan 2025 01:29:52 GMT  
		Size: 2.4 MB (2409250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d39d02e567d898d1c33f0333c7b9ea238ca962a6acf1603d70328c24c7bbd8ca`  
		Last Modified: Tue, 28 Jan 2025 01:29:52 GMT  
		Size: 9.5 KB (9480 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:4ba0216c75f89f634f9c95e23e89513f1718c0a8a581eedccc186cf718815041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.2 MB (86216618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce2ad72719eea327eb326631f4341516a71b7f29017d898338e776d1c46fd538`
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
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Last Modified: Wed, 11 Sep 2024 17:24:47 GMT  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32965fbc5c6c7167bf2fd30dbcbd4cd5247fa289b1e49d9525bf0ae4d0de4397`  
		Last Modified: Tue, 28 Jan 2025 02:41:21 GMT  
		Size: 58.9 MB (58858289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:861e39452ea2a8631d431b84a6dc02ad8b0c24aab3f0e8aced29b263778df986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2418564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a601ef59081b6ab7f9c04c03945b861268fc29d4314ffdc035ceb73673ad141`

```dockerfile
```

-	Layers:
	-	`sha256:0615ae8966fe0f04641b1c0a216db502b975bc4e046cb7d14042da69fce4fb97`  
		Last Modified: Tue, 28 Jan 2025 02:41:20 GMT  
		Size: 2.4 MB (2408956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc2c832a991b000cf1dcaca26bd09dd2e0691c01678298e32a01893349d187e7`  
		Last Modified: Tue, 28 Jan 2025 02:41:19 GMT  
		Size: 9.6 KB (9608 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:fc2308957254ac4470ce2af9ed15186e4559f619709b219aa600eac5c4128dfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.7 MB (95749640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a925e76387db8b6dea5bf002915096eb58b0d33f5154cfb521750e63aa39139`
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
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02fc52c27acef058c510fab3b91792a6ff284d33fa77d569ee6dd6b6ee34dc2`  
		Last Modified: Tue, 28 Jan 2025 05:55:31 GMT  
		Size: 61.3 MB (61301398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2288b548c08d03ce66f09aa287e147deedae68c7f7942136c85d3ea50916fcb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2422779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09b02eeb800178d233654d026907fdc2c0b3e56973bd9dfc0c732b7eb7879e4`

```dockerfile
```

-	Layers:
	-	`sha256:131893deb9f9fdbdca4d0ef577eeee4789a9affa67b4965bfa314c0b202bd863`  
		Last Modified: Tue, 28 Jan 2025 05:55:29 GMT  
		Size: 2.4 MB (2413243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ba091aa64b07c65e658ed2086565ecbb7fe5e3fc9b3bcdb5313d23aea685d37`  
		Last Modified: Tue, 28 Jan 2025 05:55:29 GMT  
		Size: 9.5 KB (9536 bytes)  
		MIME: application/vnd.in-toto+json
