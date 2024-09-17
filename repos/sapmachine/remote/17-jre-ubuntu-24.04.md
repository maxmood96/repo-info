## `sapmachine:17-jre-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:c118d5ccfee2d68de6b433669e07371833d78d16fb619ca5a12a144b09b53f7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:3bb18331884c61efa299deea244f542e047d10b728c19d2eef2d01c92a324a08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.2 MB (86249798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b371ffccf6feed23159ed2f45e32be617348a4488fc6256002b05fcffa7c8b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:aaeb92d3288093ff43a69d19f9133475372ca003b6de902066a2d4641eec2456 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6`  
		Last Modified: Tue, 27 Aug 2024 17:08:05 GMT  
		Size: 29.7 MB (29749828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f0116c53a60883aeefddf009826aee10b61e1f404f7961dca44eb8ff117da0`  
		Last Modified: Tue, 17 Sep 2024 01:00:45 GMT  
		Size: 56.5 MB (56499970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8c6a9f172c54fb696f3fb76220158d4c53cd610e4a9fcb0c370e979842e59091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2371976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69aedff1cb72aecb5ad152e910277e1125d96651ce98be525ecab5109dc26a4`

```dockerfile
```

-	Layers:
	-	`sha256:275f425129e9adfb524f877f5413e521f1961b3082a995f39e3638dd54f37f6f`  
		Last Modified: Tue, 17 Sep 2024 01:00:44 GMT  
		Size: 2.4 MB (2362759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07f36c21e7d561a5ec959d075c746830dfc865b962b6d93f7090abc3667f0488`  
		Last Modified: Tue, 17 Sep 2024 01:00:44 GMT  
		Size: 9.2 KB (9217 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:f271af950536f22616936089edc1058574a4f5f0e8a55dd5a4e1f499ee5bb578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84583011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:573a3ec712f84432cc34f0488b2a2bd054d9afeddce44f52f361ef335988b64d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:326f7645aedaef39f6ed8d915cfab4d497b0b35ba156d1d1449a5a2eea30f71c in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e59cb05818e49ea83cbe79bd46eb80418dfe3cb3735b45570f93a23579e2cec`  
		Last Modified: Tue, 27 Aug 2024 17:08:12 GMT  
		Size: 28.9 MB (28885599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6548878113041f0a5a8437a7c6bb529eef5cdb9e15dc3620cefdf1ea3289fcb4`  
		Last Modified: Tue, 17 Sep 2024 03:28:43 GMT  
		Size: 55.7 MB (55697412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9f957222bb1e08d68349c6d5a2bc474e6645c810438cfcab32446a3e836a40b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2372792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb46c0249c3c482943cb8c3d20608bffebfdaf9ca38fb56a119352f763c9fd66`

```dockerfile
```

-	Layers:
	-	`sha256:e403a62f215f20fa3fe539d24c95860233e8caafe716cc33cab9c445ae2ca48d`  
		Last Modified: Tue, 17 Sep 2024 03:28:42 GMT  
		Size: 2.4 MB (2363250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41dfb87a5073d309390dfd1195115a8f6287fd74999fc51cf99cfd230bbe096e`  
		Last Modified: Tue, 17 Sep 2024 03:28:41 GMT  
		Size: 9.5 KB (9542 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:9dc75c6973879f16b6a61f3a4417c741a217b17e55d8f1fa4ea74dfeb2f1cb47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.7 MB (92727779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ede715b6efe99174e412bb7367790a4559e6ada3b9ccf49460215080823551b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:21 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:21 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 18 Jul 2024 15:16:21 GMT
ADD file:c70c2393dc0404f71d25ae70ab08b5aa65e46753a6169cfd4f5554c942cc0218 in / 
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c526398e5e771684dae49961d5a74cd9606dcbcf7ddafb1fcc1433293927dca4`  
		Last Modified: Tue, 27 Aug 2024 17:08:24 GMT  
		Size: 34.4 MB (34392345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7182ef23112c2106bdbd8995b5b93ad0f4bc33e8015ba3942836924c98674820`  
		Last Modified: Tue, 17 Sep 2024 02:47:47 GMT  
		Size: 58.3 MB (58335434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a128ce331eb6ab30e81711d079a1e65a4d28336ecc547e4011171953c87fa2d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2375975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103cda2624b3ddedca1d8287566997d2925694af1ccbe0954b1f78a775ca81d7`

```dockerfile
```

-	Layers:
	-	`sha256:67cb69617f31df3ebafbce10d0bad529d147a0b678020911a52ee06a627a1393`  
		Last Modified: Tue, 17 Sep 2024 02:47:46 GMT  
		Size: 2.4 MB (2366708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53fd0118b8b1763f425909d9c7bbaa4a7eab3fdb13841766fa7ce789dfb38c03`  
		Last Modified: Tue, 17 Sep 2024 02:47:45 GMT  
		Size: 9.3 KB (9267 bytes)  
		MIME: application/vnd.in-toto+json
