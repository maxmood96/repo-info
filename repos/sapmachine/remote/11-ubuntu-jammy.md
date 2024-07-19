## `sapmachine:11-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:b730c59ef9024de1c12c92e912c134134ee3f4e8ddb24379d33c302d88a9c0ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:7230399053bb921f8c8bd881c3f8bc771e00342b3a5d59e10b58b944e62b1be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230269437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd23147f24c708307f5aafc0fd46a0dafa03aa76f91ee00dae9ce86744d49a3`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea5ad96924f28f4f65cd42514a7513066037496eb93130e07b74fcfbc786d4b`  
		Last Modified: Fri, 19 Jul 2024 18:00:47 GMT  
		Size: 200.7 MB (200735382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:40ea5fd807fc87a58b232fffbf04fcb2e53ac8f54ece9eeb8153e344004d4238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2499036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b7682f40726341ee3fafc59e47a9cc9bb2e8eedf43a5e6f38c569d415c871b`

```dockerfile
```

-	Layers:
	-	`sha256:de4ba91620afdd2185d433a94b0dd04259efd36f497ac3342eeb9e8b31323eba`  
		Last Modified: Fri, 19 Jul 2024 18:00:43 GMT  
		Size: 2.5 MB (2489152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a532e7156af8bfcedc14108a3722fd7fb489766b52289dcfd18c43038a28f8a6`  
		Last Modified: Fri, 19 Jul 2024 18:00:42 GMT  
		Size: 9.9 KB (9884 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ab3388f8535b39f13bb80f159f88d0af3d7a7a6340f042f2aa2cc129057746ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.5 MB (226524240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ab90879ceb1c081e67fde94c5027e47e1d660dc13d7c2ad92b723692135ad4`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb9362e292770e7d4cd6eacbec7e5c3ffe061afa903dc3dcc05bcd686dc9c34`  
		Last Modified: Wed, 03 Jul 2024 00:06:18 GMT  
		Size: 199.2 MB (199164215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5cbf3b2ca9cda6b250bd6fa5a2d354eba19a241db7c2377ac7802d35faa4a771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2471578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:990f32fd4f1310419fdc7de25e34523ffa2b442a7221d4c0327d9dcb4f726077`

```dockerfile
```

-	Layers:
	-	`sha256:00512bdb7c9e9c8c60112940a07a880a74f877286b7bbc702b253425cbd404e4`  
		Last Modified: Wed, 03 Jul 2024 00:06:12 GMT  
		Size: 2.5 MB (2461328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1b29c4e753a46e5c1acb28145a5f2c68452899d48a4ba43600ec7a11565e7fd`  
		Last Modified: Wed, 03 Jul 2024 00:06:12 GMT  
		Size: 10.2 KB (10250 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:3ca214468f593025c239611b7ed6891ad4968085b78ee8627ef0d177077c2793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221816030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5d91a30c185556123b1ef9015d8caf4913311b18308cb39a6f535a4e2627ed1`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa55cb64602e6ad1399ea6f7e95fbdb85c3209872636bca85ecf464d94f86144`  
		Last Modified: Tue, 02 Jul 2024 21:37:31 GMT  
		Size: 187.4 MB (187354949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d760f884afff9f00adba3020bb2329c140aa7a92427abc9abdf54a2ff1c5a45a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2472365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c70f6ec3616e7a67f793b0801cb3210c454d7c9d6285b07d0a784c573f809d5`

```dockerfile
```

-	Layers:
	-	`sha256:6471fda1ffea73051edb8fadfe3b3ba091b60e786a0b4a403272c6c8c5a6dec6`  
		Last Modified: Tue, 02 Jul 2024 21:37:24 GMT  
		Size: 2.5 MB (2462401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31b6a2935caa057bcd7be7a3694f2f9573cf7a7cba85580ad62bd987d851f8f6`  
		Last Modified: Tue, 02 Jul 2024 21:37:24 GMT  
		Size: 10.0 KB (9964 bytes)  
		MIME: application/vnd.in-toto+json
