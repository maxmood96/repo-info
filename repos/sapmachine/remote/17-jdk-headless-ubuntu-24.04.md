## `sapmachine:17-jdk-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:7321dc97e62cf8ddcb9ecd5a1aed2f79823ae159f48ec1b1cc746ce08cc2b932
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:12c3af6631433dc5bc6d1a43d6e51214219d63e671361aa7053d66a43c999d3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228837270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:defba9171e8960014e986c7087ec06fb6572bd8c28cefb9cd48be0386980a1fd`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:16 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 13:39:16 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d800178ccd826e5ce636aa6e3064544e2fc623a805f02b9a1cc12a4876e75046`  
		Last Modified: Wed, 09 Apr 2025 01:21:47 GMT  
		Size: 199.1 MB (199119618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5ac6f6b5aee33ea932d5ec59fa917d4aee061cf818f7bc466d0380febc0d5c91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2241219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4024b2639501ef8dc93d56687bc3b74c6eb11df9bdcac15ebfb13bf52cd39259`

```dockerfile
```

-	Layers:
	-	`sha256:f51d7213756dc7a9734f2fc48726047ccb5b6ee4fde8b61c4b325ba7cea5fdf2`  
		Last Modified: Wed, 09 Apr 2025 01:21:44 GMT  
		Size: 2.2 MB (2231600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc72b0818b77f29671bdf3b4350f98cca9912756931955d43fda7918f72857df`  
		Last Modified: Wed, 09 Apr 2025 01:21:44 GMT  
		Size: 9.6 KB (9619 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:01afca54522984a5d39fc0dd6956e8ef10fe055465869a71f49a33f2d662743d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.8 MB (226761293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e28cc993cc4298a791597a70af1f8b742ea4d1b4d7330dcccfe9874b08ef6a55`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b725a493bfe78ea4cf25dade34ed3339998a213eddb7462c6022d9a6b4025e68`  
		Last Modified: Tue, 04 Feb 2025 15:35:05 GMT  
		Size: 197.9 MB (197867695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b3062aac11a14dccbfe8b9f094671575485cb630668868ac8ffb64e75b654aeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2244048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55aebd5c0ecf33ebb87efac688a039166d36f17deb06742b1c0c960a0098a495`

```dockerfile
```

-	Layers:
	-	`sha256:f154298e91c718eb52b8dcb1d5df7b559890da2db6e97fb8e222e62a0e8dbcdd`  
		Last Modified: Tue, 04 Feb 2025 15:35:01 GMT  
		Size: 2.2 MB (2234302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f516a88a005f2faef8cb0b46e3dd8c331af9f30dda0f273cd5119c571f6603e`  
		Last Modified: Tue, 04 Feb 2025 15:35:00 GMT  
		Size: 9.7 KB (9746 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:674f31913ed2603610a875bd4c20d6943d9bb140265bb4531d620a7e628db617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.5 MB (234458406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:930ddfa17deb505bef15f6d1387293973d440b666bab2afa0fcb0214b1c569f6`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 13:39:16 GMT
ARG RELEASE
# Mon, 27 Jan 2025 13:39:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 13:39:16 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 13:39:16 GMT
ADD file:d7a12d3d510b1bacf894dbb7d42f36de9391b0766c28643a60d20d3c37a12762 in / 
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:16 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.14 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 27 Jan 2025 13:39:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7be894b3e11d60e6c310a10016f7c569f1a313b370ab3964114b1c135b1ce53c`  
		Last Modified: Tue, 08 Apr 2025 11:53:59 GMT  
		Size: 34.3 MB (34340867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1dd65da063702df6f4d89aa473281481350f0f28210a9652f69bd76ad9fa55`  
		Last Modified: Wed, 09 Apr 2025 07:11:50 GMT  
		Size: 200.1 MB (200117539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ae689b2f135244313c2a1951d18e4bea6171e6922d3b6e31a52ecaab57528696
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2243217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cac0897edb64aea470d1723e283bb8b8783f598cc8c9246b7f4ecd01eaf2a3a`

```dockerfile
```

-	Layers:
	-	`sha256:26322c206493ddb0735e7d15bfa3a6678b04ee01c222dc6feade5baa41ef68e4`  
		Last Modified: Wed, 09 Apr 2025 07:11:44 GMT  
		Size: 2.2 MB (2233542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65e2ae51a9a33f11b2d7b0eb2a1a0029ed20a192d2254195f73eb6499a736abe`  
		Last Modified: Wed, 09 Apr 2025 07:11:44 GMT  
		Size: 9.7 KB (9675 bytes)  
		MIME: application/vnd.in-toto+json
