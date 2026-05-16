## `sapmachine:lts-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:29b5e42b9476e8126582a60bd724a3cd8db95bb12068dede22090783b10cfc62
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:3ae42e16fb94667484446d557e36ae259db846e7164f7103d5b62838bc56ee01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.5 MB (251534681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2632dd6fd23f5419906d9bdcaeb726a77977b40e9a9efae1a71f6c522c1e39fa`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:21:05 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Fri, 15 May 2026 21:21:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9543e1af33f4cdf2dd209313f5526829586035d3a39828889a339e946cb7a3`  
		Last Modified: Fri, 15 May 2026 21:21:28 GMT  
		Size: 221.8 MB (221797997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cbaca3a0ac3bb1c14f446aa3da5091953e0435322916b26c2bda99e6ebec3c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2634924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb4f3172f0ee894dd81f08c27f7019a855ff0b5cd4c0e4378f3241f08d3d19a`

```dockerfile
```

-	Layers:
	-	`sha256:d32c9a30cbfc7f24eb6458da375626dff6b648489b822f196901384d425e14fc`  
		Last Modified: Fri, 15 May 2026 21:21:24 GMT  
		Size: 2.6 MB (2623522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45d14eb6b99619895cd5a852463c0bf8f984096d56be561a3ae36e935b27c0fe`  
		Last Modified: Fri, 15 May 2026 21:21:23 GMT  
		Size: 11.4 KB (11402 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:339d56ee1490067a773b61899e98a827545268ca0879b85c0578cfc567452410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247158906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e22e58a2de956bf92aff23cae6695e95818dc413ae6e80fca0874dfb291e31`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:21:15 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:21:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Fri, 15 May 2026 21:21:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd65aa1ef0dfe24c4d27ebd4e365e52ffd90b7e82a7e281cd68ec3ab35b924da`  
		Last Modified: Fri, 15 May 2026 21:21:40 GMT  
		Size: 219.6 MB (219552283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:37fbfdb452c97ccafe3fd8980bcb42eb87da274fa768469796ed6320ca0ef106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2634899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1519c5455fa458fd3beed6935dff78d96abaafb7230e799ea2406896c3a3013`

```dockerfile
```

-	Layers:
	-	`sha256:055e1d047fb83d1937a2a3194cd5d0d72205fdb5b979575fcd3016b9bf1e5e86`  
		Last Modified: Fri, 15 May 2026 21:21:34 GMT  
		Size: 2.6 MB (2623297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cce5422fab1e06841cc9eb3ab3074b6bd8e7b1895166cffd9017c1b1590dade`  
		Last Modified: Fri, 15 May 2026 21:21:33 GMT  
		Size: 11.6 KB (11602 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:a283aced5f1045a4e5af17f08168440b5d2fb835bf82c8b97f97172d32e731f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257071386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0276fe2ee801a508a7f8a4c063a51b250b3a413e6e00bf8b59948c53d3f64e`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 09 May 2026 04:51:05 GMT
ARG RELEASE
# Sat, 09 May 2026 04:51:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:51:05 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:51:11 GMT
ADD file:bd6823713e9d7c2f4ea7ca1d6d549e2bed56e8ce1fc6f98e14f6eb3a3371ebfa in / 
# Sat, 09 May 2026 04:51:12 GMT
CMD ["/bin/bash"]
# Fri, 15 May 2026 21:36:10 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.3 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Fri, 15 May 2026 21:36:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Fri, 15 May 2026 21:36:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6970bf2b5ef1698cb51975b1a652f6511f8fd9f88ae7b247e3ee32591d975e63`  
		Last Modified: Sat, 09 May 2026 05:25:11 GMT  
		Size: 34.6 MB (34646720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d6bf36c9563b68a0efdf78f4c30b2205b3016e2d4a24e041f2545bcff82a60`  
		Last Modified: Fri, 15 May 2026 21:37:00 GMT  
		Size: 222.4 MB (222424666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1d4c4cd20eda52bc6185ebf70430623b20c40093254caf31b4247dc5b4e1a7a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2632032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a070b14086257dbbb0331dea7ddeb0f12673876b2c20bb9612a36567e9391b47`

```dockerfile
```

-	Layers:
	-	`sha256:7349e4c96762431b84b20724c3481fe95696daf07ae7b27311c2c94535d91c6c`  
		Last Modified: Fri, 15 May 2026 21:36:55 GMT  
		Size: 2.6 MB (2620538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:271d7c959d6d833110301c45043079db2327be06a3478e7e5aee74523f2858ca`  
		Last Modified: Fri, 15 May 2026 21:36:55 GMT  
		Size: 11.5 KB (11494 bytes)  
		MIME: application/vnd.in-toto+json
