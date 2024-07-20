## `sapmachine:17-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:db218f8c237f5f347ce17b1adb1be7533ec1af8536ac2d0263c5605f899128c7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:85e28b634360adffdb4db14990736a642dc22a91b0a02d33c3bcff9700f86e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.6 MB (229585885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d913978e83ffe39f3d71a1dd24b052401ed7e0df0e19e4f113c0ab2fee6991f6`
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
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd67323e43a3b07f99cb66c5d9c780b874214bd022db16076e8b70b343a87e1`  
		Last Modified: Fri, 19 Jul 2024 18:00:46 GMT  
		Size: 200.1 MB (200051830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:cd3ce5e629644707248105439fee3a3e1b5082af204d0a60dbe6f5214cdf353f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2481100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30da6affb3f60d2e30329e04f6c529049cb065c6700984d6cd3b000123be795e`

```dockerfile
```

-	Layers:
	-	`sha256:746e57e60d9f12a8fa187957223da71dc26ca15960b3e36dbd2590735c0fe1fd`  
		Last Modified: Fri, 19 Jul 2024 18:00:42 GMT  
		Size: 2.5 MB (2471217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab6a71808061110e57ea6195e0c4700c6970fcf66a87a2e0aa3001880509921b`  
		Last Modified: Fri, 19 Jul 2024 18:00:42 GMT  
		Size: 9.9 KB (9883 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:7da2b3dee5b7fb258276b97faf5ce6e1b2429771e6a55ca51a0cdb4bb6eff236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.0 MB (226000950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16397fd07a9d5a6dfb1fbca6fd8ffe96a62d138f1929c4a895c5b2e859d919bf`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jun 2024 19:23:22 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:23:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:23:22 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:26 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 19:23:26 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8082bf6d92ee7bd9e95b1ff3720b9e9de032f5a2f457c01bcb4af5e7dc44970`  
		Last Modified: Sat, 20 Jul 2024 00:26:05 GMT  
		Size: 198.6 MB (198640925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:dec342097e97f204abae6a48ede48bd6789f7d2a534206da4d77c87481e20ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2481178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c9a2a5a53380617c5e1d191d0990e45587c60d122691ee8cc5b7509fe0bc03`

```dockerfile
```

-	Layers:
	-	`sha256:62715d4ddfbb26d972ee58d6db3cf0c2576fe30923a6f64171b88eda3e864a45`  
		Last Modified: Sat, 20 Jul 2024 00:26:01 GMT  
		Size: 2.5 MB (2470945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c681d6f84745367579723a29bb16b03fcaaed49744fff218dc69fb336ad1b5a6`  
		Last Modified: Sat, 20 Jul 2024 00:26:01 GMT  
		Size: 10.2 KB (10233 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:26e3f086eb1ca745b9730b84a9762c5c35c2bc02c20cdf721f5f830bc130470d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.6 MB (235585896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7381e23491f58fd823d2866d29c96cbdf981dbb746ec5a8cbf8a5af3ec8396a`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jun 2024 19:22:59 GMT
ARG RELEASE
# Thu, 27 Jun 2024 19:22:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 19:22:59 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 19:23:03 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb517a7c7c313be345205e877de4674ca539ce2d472c8a066fca7406641d1d3`  
		Last Modified: Fri, 19 Jul 2024 23:37:29 GMT  
		Size: 201.1 MB (201124815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:799d0a9c3580c1ecb5ca3d2d683d401c71c178c6a87d6b606dc36a538edb00b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2483217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf77e4e98933c3200bcd804a8540eb2bfc4c9a874a85a71f5aabaccc8cc266a`

```dockerfile
```

-	Layers:
	-	`sha256:6382036b3aac0107f0f23059502f3ebd3262954edac4fc9bbb6cf4ca21df3452`  
		Last Modified: Fri, 19 Jul 2024 23:37:23 GMT  
		Size: 2.5 MB (2473271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4010aba3dc6287f0bc1a7a7c9c1dacbaf1875e916875f6a60aecc46af07ea0c`  
		Last Modified: Fri, 19 Jul 2024 23:37:23 GMT  
		Size: 9.9 KB (9946 bytes)  
		MIME: application/vnd.in-toto+json
