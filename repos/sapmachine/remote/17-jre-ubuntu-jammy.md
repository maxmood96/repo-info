## `sapmachine:17-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:27d12a8ea3cd5b324a7c3c3ba223044a48244efc3252789c437ae2cfbfecee31
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:22ef4e238c26bf099ef1f77c2597a786176b38bc98ae66eb492c38c28ee2ae42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.4 MB (83355314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d172c7b7c4afe10ae5949fb750a5768bee59a412ec74b6bd8cc2fd31af342572`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 07 Apr 2025 07:24:14 GMT
ARG RELEASE
# Mon, 07 Apr 2025 07:24:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 07 Apr 2025 07:24:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 07 Apr 2025 07:24:14 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 07 Apr 2025 07:24:17 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
# Mon, 07 Apr 2025 07:24:18 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b71438a59140a3a8f1c6893aa8b0a2e62663f09be50768b8f810bb0995bdecb`  
		Last Modified: Wed, 16 Apr 2025 16:14:04 GMT  
		Size: 53.8 MB (53822949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:526944a07c981ef971c7a26d26d33d0f70b39948c5da5fe6d2ff5b77370296be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2416275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da96e3c2076743715753ca39a02bf522562e063ea33ebbd59eced5ac845cb0b`

```dockerfile
```

-	Layers:
	-	`sha256:3205169095f20677af5fc1fd16c19d87229c6105cd2c65e4bc6929e6d192a6da`  
		Last Modified: Wed, 16 Apr 2025 16:14:04 GMT  
		Size: 2.4 MB (2407454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a39dec536b9136b5caed5c7029e3abe31947e758139aace8afbfd88ace31ffa`  
		Last Modified: Wed, 16 Apr 2025 16:14:04 GMT  
		Size: 8.8 KB (8821 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-jammy` - linux; arm64 variant v8

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

### `sapmachine:17-jre-ubuntu-jammy` - unknown; unknown

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

### `sapmachine:17-jre-ubuntu-jammy` - linux; ppc64le

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

### `sapmachine:17-jre-ubuntu-jammy` - unknown; unknown

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
