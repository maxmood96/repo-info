## `sapmachine:17-jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:c3a5d118ba829e030118c50d6f85107cfb1d067a327b8f7e2621b3df908c41db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:89e3cbd801ddad4e5d0b6a6a49bc0bc9e6fd7849539077e924e6aeb069e4ecad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83355731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d0bb8ff23c5402bd9fb8ae19f069699b9116fe19084881530afac74e50ea4a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:41 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:41 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9daf5b053c0b7abb3ce5cc0c7764281f0115959d97fef80b64d1ffd91b90954f`  
		Last Modified: Mon, 05 May 2025 16:36:54 GMT  
		Size: 53.8 MB (53823117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:12672963d816f53c61c26aa44b6e0d474ca0be54619187e2b27c83217e3232b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485c5e0b0116be1d00e90476bcd4aa4b24b177acc0e8a2fdf49e07aabb402456`

```dockerfile
```

-	Layers:
	-	`sha256:8beedaf74f4e93c34fa3ff2e9b92f7a7f473ce5aa7ff7ccaf693d0e79cf945ad`  
		Last Modified: Mon, 05 May 2025 16:36:53 GMT  
		Size: 2.4 MB (2407454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a29b39d8d2b02e92d5996f7887f8d432c09048e2711427deae1a8ec60ef0297`  
		Last Modified: Mon, 05 May 2025 16:36:53 GMT  
		Size: 8.8 KB (8821 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:6274b6e59d0e180320d50e15df9a9bc11a0644de77e016052373dea199fafdb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.6 MB (80573287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8191ff664700219bf4ff1da1542fb557f0f6f2d35675d557eed29ad75cc3ed8`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 07 Apr 2025 07:27:02 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:27:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:27:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:27:02 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:27:04 GMT
ADD file:f7fa9c3fec404bf0500211305250f795384645b6032774d9641b0dae7d5fac61 in / 
# Mon, 07 Apr 2025 07:27:05 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e356bfcd458954b8b9f2ba0ca28358cd7699ce994be6a584303006a1506b72b`  
		Last Modified: Wed, 16 Apr 2025 16:42:02 GMT  
		Size: 53.2 MB (53219056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8a4934a62dcb8edff6e6d205571a610ffdfa40b415c9bd5e6da942b56e1c050b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d669dded86d1e290f2b7bc434fd7b2f56c37bbd92864c6c3a8de2a867cd74363`

```dockerfile
```

-	Layers:
	-	`sha256:f14074aff9bc52ae7a71951f974442bda46fa4c5baea16f9a68da834c80db1da`  
		Last Modified: Wed, 16 Apr 2025 16:42:00 GMT  
		Size: 2.4 MB (2407136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82b1fae00032d11c7e28f9a57018c3bda2f6c6aa6d85f7bac9f580c38a5f109f`  
		Last Modified: Wed, 16 Apr 2025 16:42:00 GMT  
		Size: 8.9 KB (8925 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:d9b35e5e09f0f3e01098136ffc63e8428eea394c02f08158ab2a3eafbe030e8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89772332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34cd694a13db131bb3a2ef43da437351df1096bb3d6a81405947d1d1fe6ba378`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 07 Apr 2025 07:25:40 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:25:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:25:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:25:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:25:44 GMT
ADD file:b1634c9c9ee669b835ef39787fc71f78267fab0678a8e8c5547ba2339762e075 in / 
# Mon, 07 Apr 2025 07:25:45 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:220e8fedb927c1ecfafdf1e8cd0a85977de62e4afd95df2c5a27a70d3bdf34b0`  
		Last Modified: Mon, 07 Apr 2025 08:26:45 GMT  
		Size: 34.4 MB (34442696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0600631e6ea2ea6e1b514e84d8342a0a25b58893a576cca251ba090aaae476`  
		Last Modified: Wed, 16 Apr 2025 17:13:50 GMT  
		Size: 55.3 MB (55329636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2884c57e3ed2562799ff5fa591d9196cabea589e561d27ca7fb2e114d54f8206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2420300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a2430a8c8c3416ede2bdd01d0068f6f8841bb79ddbf30b847b45fc41f7f88f`

```dockerfile
```

-	Layers:
	-	`sha256:9615c17220ff2805bbc8b05e2cc00aaf1762440918e5afbfadebf29181365ec4`  
		Last Modified: Wed, 16 Apr 2025 17:13:48 GMT  
		Size: 2.4 MB (2411435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25a1aab4bbe90d3f4a9f0b95ef3daaffecf3406ef471899b8cb48c74a8a49d12`  
		Last Modified: Wed, 16 Apr 2025 17:13:47 GMT  
		Size: 8.9 KB (8865 bytes)  
		MIME: application/vnd.in-toto+json
