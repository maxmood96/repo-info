## `sapmachine:24-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:cf5738e5733d6af80d88e6c10b33ced31c37e1df76cfc21a3bc448d840014cb3
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
$ docker pull sapmachine@sha256:1a7443e23838e1640fe2ea4e2fd061945d1c4dc489c588b46bdab71034132d12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261581971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb9a34625109cf5b9045e3b8882db28473d8351572ac3c96d29ca72ef39eafb`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eaa6ccb3ac83f0c0cfe0505f4e5180b521d8ab32cefa342ef2228aac280c02f`  
		Last Modified: Mon, 05 May 2025 16:37:05 GMT  
		Size: 232.0 MB (232049357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:34021467e76d52a92cc70197a6248256a8b25414f7ec845ef71fc722cafbf156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2496964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b21e12f9ba0160333bba2f25bfe5ceba8e9b24981e809aefa9a7d8a1da6699a2`

```dockerfile
```

-	Layers:
	-	`sha256:0e0f260e40fc0d8d8bde0ce61575985a27b91e4b5dbd1069ab60faac7e0d9b1d`  
		Last Modified: Mon, 05 May 2025 16:37:01 GMT  
		Size: 2.5 MB (2485551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de7c1f88d95231cafa80469a404b90e7d338401c0cc312d02b5ec10f302faf00`  
		Last Modified: Mon, 05 May 2025 16:37:01 GMT  
		Size: 11.4 KB (11413 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:f2df2b7c723bb227a0d065b61f5d24bd4be93e239ebf8529e377c9dc334c8fa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.3 MB (257268130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea63524b6f235ee6c206e11dfb34c909c09947d3bb956448f1f091f4ba16b2d`
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
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7b76bc00f23a24375cf6b51079ebcf72fb02d56fa741b31e5f979672fc65c576`  
		Last Modified: Mon, 07 Apr 2025 08:26:32 GMT  
		Size: 27.4 MB (27354231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae4077107b3b126d79b9a66fbc3b7899e89705f6fd381671db934d611c11e0c`  
		Last Modified: Wed, 16 Apr 2025 16:17:58 GMT  
		Size: 229.9 MB (229913899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6dfe3b554df76156a3a14bf89c586b4734148c47381821ffc302a0f47cccc452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2496939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6fae0adf6c11993b0e64a027106332f8654ed903dedef03a8b8d41f0b60357`

```dockerfile
```

-	Layers:
	-	`sha256:c908c2ea4bf2727bce55f6659750f655a1c356ba9cbdac67ce306c8a35e059fd`  
		Last Modified: Wed, 16 Apr 2025 16:17:48 GMT  
		Size: 2.5 MB (2485326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1e7986da7aaa3c62c35db4e0a7c7bf5a2145e277e9e93716b5aef6fdafd18c2`  
		Last Modified: Wed, 16 Apr 2025 16:17:47 GMT  
		Size: 11.6 KB (11613 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:83ebfa69e370738d06f7857a19b59974c517533b35831998514817cb9eb355a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.7 MB (267694377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec7a691e1d86c1188e7c06a939069c1ed3b0d5fc6e82e802e2c5817a3207469`
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
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jdk=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:220e8fedb927c1ecfafdf1e8cd0a85977de62e4afd95df2c5a27a70d3bdf34b0`  
		Last Modified: Mon, 07 Apr 2025 08:26:45 GMT  
		Size: 34.4 MB (34442696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce45a2bf4f9c789f7568e463bdd20c72b4807e0525e7fa64bcae724aa8bc44e`  
		Last Modified: Wed, 16 Apr 2025 16:23:30 GMT  
		Size: 233.3 MB (233251681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:90f42ac365b277e28c28540dd07c854f68f118309fc8df7e7b82eed1ab63511d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2498521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43b89ebd5ce5811561cfe2fc566d15867a1abeeebf6fd98e5dbda67578568c6`

```dockerfile
```

-	Layers:
	-	`sha256:1026b4840c82dd174ddeb9adee79e012f6845fe9046aad74e3e9c7ddd5ac01aa`  
		Last Modified: Wed, 16 Apr 2025 16:23:22 GMT  
		Size: 2.5 MB (2487016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:665b8819fcd315c4461e1220c4b05b67819c7bd10a7988bee2aa835edfbd91c0`  
		Last Modified: Wed, 16 Apr 2025 16:23:21 GMT  
		Size: 11.5 KB (11505 bytes)  
		MIME: application/vnd.in-toto+json
