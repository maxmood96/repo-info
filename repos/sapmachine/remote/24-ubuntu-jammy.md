## `sapmachine:24-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:5edf1ec5e308f481ec9045a46db1fe7860f633bce1029d093b976a1171ab1392
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:4265ee1f0f6433df8f54bb326e2e024f987377ad4c14aa89de851f3b0ee93924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261550944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2692392480f258656eb7e9fa04ca29a5225ec3bbc045c22cb21e40e031d42d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 19 Mar 2025 14:31:37 GMT
ARG RELEASE
# Wed, 19 Mar 2025 14:31:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 19 Mar 2025 14:31:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 19 Mar 2025 14:31:37 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4dea772c810200e8eddd0c5358bc28bbe3b2bac51b27a7b053812ce7328751`  
		Last Modified: Wed, 09 Apr 2025 01:20:43 GMT  
		Size: 232.0 MB (232018579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:212a73d830ab0b92b18e8cbf84be3782f05eb71b3585cfc4972e506e89f0e1b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52ed3f02d69dfc33daecd485ebc91f49c38763e51ffbfdb0af353e52850d10cf`

```dockerfile
```

-	Layers:
	-	`sha256:5cc1ca4230ec1321146555a47b873ff336157ed260c1276614c188b9c5318986`  
		Last Modified: Wed, 09 Apr 2025 01:20:39 GMT  
		Size: 2.5 MB (2484191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60b867043e1d6c488b5c5d223e4c9ecc04d29793ca6e1adc3beb9eb6f869ada4`  
		Last Modified: Wed, 09 Apr 2025 01:20:40 GMT  
		Size: 10.1 KB (10061 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:01541a44930824dbaa7672902692efe193d257b827283804c36f1612ae9de3ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.3 MB (257259425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eefee42f866e91fe5e2db0329bb200513f49443cb9b53d34c0e2ca9ab5596f9d`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16fe07d4837160fd506363d91e9b2ce8f4baf58e81730e49e30dcc829135ea4b`  
		Last Modified: Wed, 19 Mar 2025 20:36:44 GMT  
		Size: 229.9 MB (229901243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:4b7bba02fed963ddd87d62a60a5abf0022e0342170a27caa43005f40b136b502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3683141a7a62c20fc1ca7680b60ea03d477ed8f02511403d55059b6417d2dd5b`

```dockerfile
```

-	Layers:
	-	`sha256:0e22b868b945143389ae96ed44d8ed7bfcada312177e9a3716f60de568ee0a65`  
		Last Modified: Wed, 19 Mar 2025 20:36:38 GMT  
		Size: 2.5 MB (2483796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73074ad9d08a98a93f24ff413bb296515916e2b80afcef38d7195f1e8084c4b9`  
		Last Modified: Wed, 19 Mar 2025 20:36:38 GMT  
		Size: 10.2 KB (10213 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:a3fdf4c3fc02cd6bb5d6221de308684cfe113852142b0809632ee103fc59894d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.7 MB (267689610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3eb15684fd12b769c6c260672256e9d3b36787830980a525c86e7a8a8a4a8ff`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:49 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:49 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:54 GMT
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
# Sun, 26 Jan 2025 05:31:54 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4552134261ecf305d42af8c94c32fe126da6abedd845b1b380b09e72ebfea19f`  
		Last Modified: Wed, 19 Mar 2025 20:39:24 GMT  
		Size: 233.2 MB (233241675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:bcb2f9f035a0277ac0f17b6113bb4f0219f7062503933475a11b9ca4bdf3d7ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2495638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe09f1f22fa804c9dd503246e379580edeffc3d6c4bbaf9e363065eae09f12ad`

```dockerfile
```

-	Layers:
	-	`sha256:0a37f35405e41494ab1ac634a5103c3bfe968b647bb96c8a740c148b86cb975a`  
		Last Modified: Wed, 19 Mar 2025 20:39:17 GMT  
		Size: 2.5 MB (2485510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cb5fe9a146f3272ec3bdc630517c9b275ddbe8516b15c6752b9df8139b7bb77`  
		Last Modified: Wed, 19 Mar 2025 20:39:16 GMT  
		Size: 10.1 KB (10128 bytes)  
		MIME: application/vnd.in-toto+json
