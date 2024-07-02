## `sapmachine:17-jdk-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:79963d1604ad56ae28e438009088ea470e03e76f48c9488ba800fdac68fcc8eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:2244482570be573c80c1bd751f0e95492300c133ea7dc86bef27996b2c0d82cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.4 MB (229449777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51122a33c41ade034a17712d659caa8eeab641f5f058c488a1e94d807f3aa0f`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:54 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:54 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Mon, 13 May 2024 10:06:54 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:54 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 13 May 2024 10:06:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c677d91854cc723daf2713a7a79324dfacb8dc25e332336f2151a0db2a7b8054`  
		Last Modified: Tue, 02 Jul 2024 03:32:02 GMT  
		Size: 199.9 MB (199915722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:25c55ec482760b77fde14f17e809dac3f9c01d5325c44f2a04f35a1f0a8e8e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2450405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b09c4aa13b13b1576995bb79b4e7d2a7d701211a7ee517375fe3f1ef79da2b6b`

```dockerfile
```

-	Layers:
	-	`sha256:83016ab2391256d95a54de05e3e24911f0aac626d4bac4f04a5676ef3b836232`  
		Last Modified: Tue, 02 Jul 2024 03:31:58 GMT  
		Size: 2.4 MB (2440503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2ef0cb9f293ea835a0e6d48a1ade220d5f3e91b36c9b1d52172fb63550ae62a`  
		Last Modified: Tue, 02 Jul 2024 03:31:58 GMT  
		Size: 9.9 KB (9902 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:6723c487b37fc7182945fe3107eccbceb93fa7dc5825d91c201b4f808736d291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.9 MB (225861878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8057b24691f8fea274a7c9550aa8ebafa035552cd2b14acb4561cbde7ff88f6`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:54 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:54 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 13 May 2024 10:06:54 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:54 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 13 May 2024 10:06:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec91001f4708fe55dd15636bf5ead6bd7d63b987b6372ad93116f5d1e41e73e`  
		Last Modified: Wed, 26 Jun 2024 00:18:50 GMT  
		Size: 198.5 MB (198500096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3f9343bef17b302889901cf8f8be52c959aa34ddc140d1ac486e9f7732223bd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2450482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33265d6d7a09dbd21e95bf3874db130a860973f2e141b082af26208e3927e177`

```dockerfile
```

-	Layers:
	-	`sha256:bb840263fbd5642ae140e716cd8a2ea33bea94a7a3b5339cd795f88582322a45`  
		Last Modified: Wed, 26 Jun 2024 00:18:46 GMT  
		Size: 2.4 MB (2440231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:498aa46b7e22328df5328498ff2d0b1c5fb7895390d52a79c3c0b747adc0d370`  
		Last Modified: Wed, 26 Jun 2024 00:18:45 GMT  
		Size: 10.3 KB (10251 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:0ee6b346b38aab94b39cf8c6576a7c7d526e9da14bde86762c1e5c1ff4b959a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235427639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d0245abc21793a01b773427758c64e79a9ad13c14a9fec912b297d118396604`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:54 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:54 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 13 May 2024 10:06:54 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:54 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 13 May 2024 10:06:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66d4e0701e5f4f8e02dd2dcc16f67f66f1d87067ec40a2c7e3e421f1e3ca751`  
		Last Modified: Wed, 26 Jun 2024 00:53:42 GMT  
		Size: 201.0 MB (200966946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4b42db80f2cd980948f1ffbdb34ad8d20de4584fc1655528e032821b1d5a452b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2452521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ba00db5213393deae5028b7eb3b40fb88dc65fffa476b9bca86adf1b7aab7a`

```dockerfile
```

-	Layers:
	-	`sha256:3e536b542cb1c7d36862a003bef04afc963ec9a169f0845f3ff17e83b41d73b6`  
		Last Modified: Wed, 26 Jun 2024 00:53:37 GMT  
		Size: 2.4 MB (2442557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82a8c43e8260837ff24bdbe54dd1c3974ae59df8fac81e88ebc5702ba01aa74d`  
		Last Modified: Wed, 26 Jun 2024 00:53:36 GMT  
		Size: 10.0 KB (9964 bytes)  
		MIME: application/vnd.in-toto+json
