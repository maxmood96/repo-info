## `sapmachine:25-jre-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:0e84b70faf81aa4ec4687973e07f69b9783f16110ff4144fa177d537b3c13ce1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:25-jre-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:7d38db5064439a0730fb88011964b3b86348b423c9594e7a707dc76f6a959960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.3 MB (86286897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c4bfa30109e0d2fd69af093987a96ce2f08a86a845f6c737a5a9d31ba80124`
-	Default Command: `["bash"]`

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
# Tue, 17 Mar 2026 02:23:59 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:23:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Mar 2026 02:23:59 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911c5776f1573801d6e042784a7d0dedcc18d631b3cfffc52353e3b6c6b79257`  
		Last Modified: Tue, 17 Mar 2026 02:24:11 GMT  
		Size: 56.6 MB (56554904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:90e41bbf5b47e8c9ece41054164b9e0f5d9b1d5daecbabb0fd38dd6c8eb2d4a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2295364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1ddb9fe86b73c93e278639a886cf3bce6b17ebc403e6536cc374b5928b0796`

```dockerfile
```

-	Layers:
	-	`sha256:b10bcf4a332e37a1a8aa7d4bdd85d266e126235a7a0c253f54c64a66cb7fba96`  
		Last Modified: Tue, 17 Mar 2026 02:24:10 GMT  
		Size: 2.3 MB (2282762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dd527c141f26df598c75ffe6a174e2e156efb4f5ce3c4e25425c78829e4cb95`  
		Last Modified: Tue, 17 Mar 2026 02:24:10 GMT  
		Size: 12.6 KB (12602 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jre-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:643f97737d37190e4f70f413aed6c029194799cc513670c058b713c3fbb9c049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.4 MB (84373630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba88d793e3c4176295bc74bbd545f6c4c704be2d131befa5eae63d39f2190a43`
-	Default Command: `["bash"]`

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
# Tue, 17 Mar 2026 02:29:48 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:29:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Mar 2026 02:29:48 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2466c14893823cbf4902b37da53440236db3b0d005864e19bdf788ee7208bd39`  
		Last Modified: Tue, 17 Mar 2026 02:30:02 GMT  
		Size: 55.5 MB (55503921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ce6cfbf7605719d19a9db88f8d2539df4bdb4b686b3984d750c7dea62efe609c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2296188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b901697dc6e217a492f8c5d15d9e38eb6870d83d900c04baecf662f1d7aeb7d`

```dockerfile
```

-	Layers:
	-	`sha256:4d41eca7411d8ff32987468a5cdf46f7d57cd54c627a3beffeefd43029f24023`  
		Last Modified: Tue, 17 Mar 2026 02:30:00 GMT  
		Size: 2.3 MB (2283350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53c9d2bafc9fc2f2969d6d9335a467449d77c4b7436fd67b6c762c67c270806d`  
		Last Modified: Tue, 17 Mar 2026 02:30:00 GMT  
		Size: 12.8 KB (12838 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jre-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:770f6676fd5772a9de37540f210f26d9f09a30d7418420c2c41c7c08ca05a5fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91637700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e742749d9370c18b8c10442586dcce4e745950701ae19ef6a921c53c6c39d6e`
-	Default Command: `["bash"]`

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
# Tue, 17 Mar 2026 09:36:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jre-headless=25.0.2 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 09:36:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 17 Mar 2026 09:36:20 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f826c9b754a00ada9d9335ffdf3ffd40f6925a3223caac76cc429823b8621f9e`  
		Last Modified: Mon, 23 Feb 2026 17:51:39 GMT  
		Size: 34.3 MB (34310051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187273fa160d40d9d0f2fdd859e525a9652347d3e4b82daf3734709001746217`  
		Last Modified: Tue, 17 Mar 2026 09:36:43 GMT  
		Size: 57.3 MB (57327649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1334022c63303883acf8aa1d261a67a6398b69efac87b3112e7bc499f3a4d64a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2294303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e6bb1e0d07c7f5d14d25d27fae5c051611a175a9762a133bbfb93edb2161d5`

```dockerfile
```

-	Layers:
	-	`sha256:64fd63dd01b102ff44fe655f2377e4febd4e9ee9b2637e5a6703baf86a2b2757`  
		Last Modified: Tue, 17 Mar 2026 09:36:42 GMT  
		Size: 2.3 MB (2281591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9125b383d31c14028b41344a3904379b9dffd75c732a783daa4e958b735194d`  
		Last Modified: Tue, 17 Mar 2026 09:36:42 GMT  
		Size: 12.7 KB (12712 bytes)  
		MIME: application/vnd.in-toto+json
