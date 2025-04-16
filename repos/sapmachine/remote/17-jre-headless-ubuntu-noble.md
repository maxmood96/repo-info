## `sapmachine:17-jre-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:2a25e8200465f6d04e0ef15a754279d53faa8da282ecfd31457bed85f6c0b1e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:963f41ea8ea4e9101df86dd336e6b4b4d3965b14c388b73e1b7a6531b9e19902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.7 MB (82738293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4cf3a3cb3ff179e3602df4e2207e287499c0f078342065cee15df989b3bfb49`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:43:12 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:43:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:43:12 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:43:14 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 08 Apr 2025 10:43:15 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d60afcc2273e77ba36e2f8edff2c67c65035d3ec248d0193df27bcb7c75ab2`  
		Last Modified: Wed, 16 Apr 2025 16:14:08 GMT  
		Size: 53.0 MB (53020641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:21aa117520de89801d75b315cbc2a62ba7e74f47c9d95fc329ae33de2c2df4c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2158309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add44b7e79c5fb9511dfbbe4729bd7ddb86890edb38e0cc72d862ff6ff480154`

```dockerfile
```

-	Layers:
	-	`sha256:e0d8b15b7e4388713c3160db6e9e2d13b9f462332126123df232fd309da514a3`  
		Last Modified: Wed, 16 Apr 2025 16:14:05 GMT  
		Size: 2.1 MB (2148692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4424ac5001073797c532394f8b9f84c2accda2a678510145ccd96c51e1911295`  
		Last Modified: Wed, 16 Apr 2025 16:14:05 GMT  
		Size: 9.6 KB (9617 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:40c68aba3269136da485ff6429928fb7c288f37ee95ae98c25c58b372e685695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81315310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd6d501cbc56b9677ec1454ae14168883de5e49aecca89ce27d3801aa8a168a6`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:09 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:09 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:12 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 08 Apr 2025 10:46:13 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3937fa72f62e894f3d16a557577b0df6564787963bfdf98c75e2564971f93c0f`  
		Last Modified: Wed, 16 Apr 2025 16:39:02 GMT  
		Size: 52.5 MB (52468352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1fb6ca7b8033bed953868f98e73111afdaafe86514ef0a1ddcae85a9faeafd5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2158921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:837014c2eb1a8037643f389a6109547c888cd45e143146445a9859a681f831c1`

```dockerfile
```

-	Layers:
	-	`sha256:3b26c3d8c540a5c716401bf9474cb90f11b6ae1d28d7e3f5fe192c1777acf025`  
		Last Modified: Wed, 16 Apr 2025 16:39:01 GMT  
		Size: 2.1 MB (2149175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82882013d176af3d7844d87919166f40692aad770dfda575a2c3eddd0215ed61`  
		Last Modified: Wed, 16 Apr 2025 16:39:00 GMT  
		Size: 9.7 KB (9746 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:ac7c1156527794037bc76e6948ecb249ba098303cf92c8a72129eb94b2ddafea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88785706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a96c0f4cc2f74a7d7791b7cd533f04c91814b8a13a0e70fa39ddc78e5d8639c`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 08 Apr 2025 10:46:11 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:46:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:46:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 08 Apr 2025 10:46:14 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Tue, 08 Apr 2025 10:46:15 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77884f491c3893a7636f1fbc3605e1bc71636dd399224c1c2926a95b0f2a8ee2`  
		Last Modified: Wed, 16 Apr 2025 17:07:50 GMT  
		Size: 54.4 MB (54444839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1c6a158b0d3e9c5454a16337e780cb74046e3986abdb6deecffd43caacf1d119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2162254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5468518f2d02e400b744ba08fd35939cf0e177610d07894ae32c26d85186997`

```dockerfile
```

-	Layers:
	-	`sha256:b70b6aaeb733906a62fa02d3fc1b135a839ed64838f3c91cdec26018f5f2fd3b`  
		Last Modified: Wed, 16 Apr 2025 17:07:48 GMT  
		Size: 2.2 MB (2152580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41dccf7c420664809379acb7f01454adeaf6b62c801a202c9a5dce0004ec965a`  
		Last Modified: Wed, 16 Apr 2025 17:07:48 GMT  
		Size: 9.7 KB (9674 bytes)  
		MIME: application/vnd.in-toto+json
