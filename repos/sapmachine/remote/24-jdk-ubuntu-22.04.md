## `sapmachine:24-jdk-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:fb2b5dc985b0c22f976773210a4f2e268910bd6b97003a2e4dfc33c332066930
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-jdk-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:9699979872f3c723eadf6ee7bf6ff70b376ea774db86fd030cacea7646b3731d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261553180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d2621b5e3ec107b18f9053a68a511843c87eba7a0e88440854f6bc465478df5`
-	Default Command: `["jshell"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
CMD ["/bin/bash"]
# Wed, 19 Mar 2025 14:31:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 14:31:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 19 Mar 2025 14:31:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Sun, 26 Jan 2025 07:02:02 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4658adade80c6fef4ff8a94c4015c1a4f7236d1c156fb701132ea6f52e14fe9c`  
		Last Modified: Wed, 19 Mar 2025 20:46:38 GMT  
		Size: 232.0 MB (232017239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:dcb3ef0d5ed9807036addcb757a23d30ae87e33024c0059a7f4b188eba0dcb58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2494129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c9ddda213cd0bc7dde23ff7e4a2899deed6246a1cbf38343b5bd5dca3dd763`

```dockerfile
```

-	Layers:
	-	`sha256:94a42a3b599653b8b45c6e01c5b6e1a4e3e34966bca9b437e067a357b99c1f19`  
		Last Modified: Wed, 19 Mar 2025 20:46:35 GMT  
		Size: 2.5 MB (2484069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab4a4030b1df2879cf67109c5fd0c86e8c09b33e37dc1540118b740359768dd7`  
		Last Modified: Wed, 19 Mar 2025 20:46:34 GMT  
		Size: 10.1 KB (10060 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jdk-ubuntu-22.04` - linux; arm64 variant v8

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

### `sapmachine:24-jdk-ubuntu-22.04` - unknown; unknown

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

### `sapmachine:24-jdk-ubuntu-22.04` - linux; ppc64le

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

### `sapmachine:24-jdk-ubuntu-22.04` - unknown; unknown

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
