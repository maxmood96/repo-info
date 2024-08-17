## `sapmachine:11-jdk-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:ea1dac1685dfe004e780493668c17d243692c387d65b5b8264703199e89bdf5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jdk-ubuntu-22.04` - linux; amd64

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

### `sapmachine:11-jdk-ubuntu-22.04` - unknown; unknown

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

### `sapmachine:11-jdk-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:db831ea86d25791dee8ed8f20f5265d6e7cb9bf82cbc524fa6614b9def2e042a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226551159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ada204e22c2373abc06ece784c1d7ee4e63db424b4165218051b8df803d67d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755c6b5fc9ded1562eda8353fe656ada8b14215502678ef93de1d56c8ee7aa64`  
		Last Modified: Sat, 17 Aug 2024 04:45:34 GMT  
		Size: 199.2 MB (199192476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6a142d099aa0aff7f7fe0117ac14da52c26a60d8e40e601013d8cd04e70cb9dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2499740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fde960efd270fb8f6fd5376cc707e1069aa47238f43a14a768232cf0df684a0`

```dockerfile
```

-	Layers:
	-	`sha256:71af787178068853af8f1a3971c25dd19320180ba58975b0fe4bfe63a9f13923`  
		Last Modified: Sat, 17 Aug 2024 04:45:30 GMT  
		Size: 2.5 MB (2489508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9926fba49eb7a38332c5e77997fde16ce0861e9d822a46d760c25831c9cd7981`  
		Last Modified: Sat, 17 Aug 2024 04:45:30 GMT  
		Size: 10.2 KB (10232 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:8f3fe75d839f792bc3e543f0f69bcef108c0eaa190bfab5a7a5a1050ec8101d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221846236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf4a48fde87f3b4c4be607d2c7c753e5055e352bb4a60e4c01f227ab635eba7f`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e0aacbb6089cf147697d708102cfc52fb7689ce2464b5a29689fad50d8722a`  
		Last Modified: Sat, 17 Aug 2024 03:33:50 GMT  
		Size: 187.4 MB (187382058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:86e9e1fc90e991175e5ade6e14dbe8eb930d8723c14b081c82e66db1a90ed102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2500527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff5a1495b0071397233a5b2f44ffc185ac67b9633d53af57159fc3eec47ae3f1`

```dockerfile
```

-	Layers:
	-	`sha256:7b3240db715bd6e32b54660503f2195037a0c65928768709862ea3c6c77c1751`  
		Last Modified: Sat, 17 Aug 2024 03:33:45 GMT  
		Size: 2.5 MB (2490581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:155a57259b8ee4c41dc84e3a66c503d7b54800c33e7a23175b6a1d6e867238d5`  
		Last Modified: Sat, 17 Aug 2024 03:33:45 GMT  
		Size: 9.9 KB (9946 bytes)  
		MIME: application/vnd.in-toto+json
