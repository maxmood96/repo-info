## `sapmachine:17-ubuntu`

```console
$ docker pull sapmachine@sha256:5ee85059078baae173b64ceb5107b68af1702670b6d6d74a72f95a8f19dbf1e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:1ab57334db25cd49151a51d7348e38cce029924a4cd65d1ed30901a696fb0570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.6 MB (232620891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a164a5ad347242233d3729dd4e14695a861ab6722b34f40b88f63d5aeb45ecc`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad4848a53762a348bdab8bf667414ca770a012f5c22aab2052bc81e81b9e25b`  
		Last Modified: Thu, 02 Oct 2025 09:09:20 GMT  
		Size: 202.9 MB (202897880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:13a76cce800bd6842543fe2f23d001ad2afac218f362ec4e6b2981cf831651bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2615500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913d2c3bbc23dc448f36920f717a393d525802773cf93b076865b9d4fa882a97`

```dockerfile
```

-	Layers:
	-	`sha256:e64e6d3152d74d206fbe778b9aecd094b80d0178b91728d6508bc232ab0de8e3`  
		Last Modified: Thu, 02 Oct 2025 09:06:19 GMT  
		Size: 2.6 MB (2602850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45968006e31a1332dfa1afbec5a0e3b83805de5ad3ff0cb2678353404cd989b1`  
		Last Modified: Thu, 02 Oct 2025 09:06:20 GMT  
		Size: 12.7 KB (12650 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:df0aff8c8792bbd01342cf01cfc2867ec15297d87b6b3172b81a10f6cfec11da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230283299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0c226bb7552e35c23b2d9d5f9973b5b5d2456faf46ec09cd0cc0917141fa928`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45598e3658cf1449335e772b429ea71b0bcaad8250818237d5f83764d92d54d8`  
		Last Modified: Thu, 02 Oct 2025 03:07:26 GMT  
		Size: 201.4 MB (201421724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0b8f98777b3fb3f72d662b26e06fe81db071b71192f51603875240a3a65c51ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2616359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f42bb480d105477173957b52bf5fb73e4701cd2c505f58798d2efcba4dc0b0c5`

```dockerfile
```

-	Layers:
	-	`sha256:622b4b61be5e8557369924c1064da88524c92e237ab7976b810701b6af8ab47f`  
		Last Modified: Thu, 02 Oct 2025 03:04:36 GMT  
		Size: 2.6 MB (2603462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89c1a8dedcd37ae8e82024a7cf4c29029025cd4f838611089828c560caa04dd9`  
		Last Modified: Thu, 02 Oct 2025 03:04:36 GMT  
		Size: 12.9 KB (12897 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b3e7f026eb57fb6066a3ca89cbbf1b1813a79f80f7459f954960a16c4aeec29b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.2 MB (238196439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ada26b0925ab7862c12c10ebe3e3398ad2f86d985826aad189a377a9992b9fd`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:11 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:11 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:11 GMT
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:11 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.16 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 15 Jul 2025 19:58:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:15a6b79c4fd2f3417787ba4c0a8161183cf898454880102c719eb0c91671c218`  
		Last Modified: Tue, 30 Sep 2025 17:28:16 GMT  
		Size: 34.3 MB (34303547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c54e70067e13d55d84ac5d49b254266a7289ed0966a498afc1ae95ff2565b324`  
		Last Modified: Thu, 02 Oct 2025 06:05:56 GMT  
		Size: 203.9 MB (203892892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:df1fb05037efd4d288851874a755de0130229972e38431399644fcd716bc35db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2611799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e7816540c8abe3f197d4407cdab22c5588ac1744deb58dd54880136018ecbe`

```dockerfile
```

-	Layers:
	-	`sha256:f41db953ccd2529457a76f8c72b9bad88093567800c7b3bf34d6b4e4c9b79cf3`  
		Last Modified: Thu, 02 Oct 2025 06:04:42 GMT  
		Size: 2.6 MB (2599033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13555087771aca1f2a2ed7abc4136f1b18cde8a3883d151c2307d40ffcb5894a`  
		Last Modified: Thu, 02 Oct 2025 06:04:42 GMT  
		Size: 12.8 KB (12766 bytes)  
		MIME: application/vnd.in-toto+json
