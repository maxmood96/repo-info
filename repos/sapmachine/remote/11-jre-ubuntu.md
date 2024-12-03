## `sapmachine:11-jre-ubuntu`

```console
$ docker pull sapmachine@sha256:ff17deb975255469a48c759703b9951c1caea4c5a494af69a9eced5c9c265c09
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:00bec4974d1516517a594a7b2211ec45fa6cec8513df9f88fcf771f31ec373da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80127881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06e1efe993676fdbc18f73e3c7e5fa238a52626b624b8298ae580a88e4d0b1a7`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 12:49:16 GMT
ARG RELEASE
# Wed, 16 Oct 2024 12:49:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 12:49:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 12:49:16 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 12:49:16 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878137653d942ba70c4bd2a0cf1777ab57fd3aab588ce3621b53fed65698901f`  
		Last Modified: Tue, 03 Dec 2024 02:37:05 GMT  
		Size: 50.4 MB (50375913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a71426999459058bfe586b552f6383b907411863f1b1f3ec8b7f7c73cfb3346e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2400649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67e05d25beb6ff08f888ab2370ea26d7e56f67c125fba135e0b4ca165dcb3bdf`

```dockerfile
```

-	Layers:
	-	`sha256:5a793c34cbc55f2e59849b575f926c96ca978f1842552000e21e4f114d26d556`  
		Last Modified: Tue, 03 Dec 2024 02:37:05 GMT  
		Size: 2.4 MB (2391178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2507c5dce0f372e01bed11c0471e6d6c9b3c290f60c2700b9521770024c7a5d6`  
		Last Modified: Tue, 03 Dec 2024 02:37:04 GMT  
		Size: 9.5 KB (9471 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:7f6831b2744b2b62b98e61f05e7b59820a3586cbac9f2dad330c2bf9384a117c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78604232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c796a63b02a57d381d843968c6c7b784c2d3437027f18cbe64b12b283dfc128`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:38 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:40 GMT
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Wed, 16 Oct 2024 09:25:40 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6570c261f32a8aa5b265f247b49a39bc626dae54938714126be361dbd3c01cfb`  
		Last Modified: Sat, 16 Nov 2024 03:56:18 GMT  
		Size: 49.7 MB (49711807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:861a1232bd76f926b594c4bcb0933d7b82769ff24436539399ed13a8174b7511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:022e55bb5bc8ac602d1c393add9d263ae9e8a4060d1d2e84adb717d0be4b3d7b`

```dockerfile
```

-	Layers:
	-	`sha256:c1bad22387ef665839e88cb4a2f2f9223a2bcfef3c88c54c1303700ddd2b502a`  
		Last Modified: Sat, 16 Nov 2024 03:56:16 GMT  
		Size: 2.4 MB (2392277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce055840b336ba2d2ee7ee2fb8b0d015d79ff2bc3c9e4e60a6d3503baf312afe`  
		Last Modified: Sat, 16 Nov 2024 03:56:16 GMT  
		Size: 9.6 KB (9599 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:0aed8811da68c4cd6da4ae0f766ce59692e45a68952928747f20b61529d2107a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83533277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46dc65e3d431572301b58cf0bd369fb8c68872452006ed288e3c77216eff93e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 12:49:16 GMT
ARG RELEASE
# Wed, 16 Oct 2024 12:49:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 12:49:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 12:49:16 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 12:49:16 GMT
ADD file:43ada82586e21a3bec38211b678fc6eb9b5e39f96a2d31fced4653d2b54a553f in / 
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.25     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Oct 2024 12:49:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4e112885c8061d52bcd0f8d99851b65be887b95c74de235a16946b3562526bbb`  
		Last Modified: Tue, 19 Nov 2024 17:38:45 GMT  
		Size: 34.4 MB (34388820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fb0732a26c54f9575b2479f53b0d76310f160c2eb96d80a5f4eacc8963d7e7`  
		Last Modified: Tue, 03 Dec 2024 08:48:50 GMT  
		Size: 49.1 MB (49144457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:d22b4194e1cc5d673392eb83c92b15c567076f869be8629587cdc113875f811f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2404660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41dbf2464e3cfab214951931b0fd085380a7d06421cb858e09079ec80a0170f2`

```dockerfile
```

-	Layers:
	-	`sha256:2c15bf6319537f3ef23761d7cdb6eddd1e67a9caa91ce54363656c43b4a05d5b`  
		Last Modified: Tue, 03 Dec 2024 08:48:48 GMT  
		Size: 2.4 MB (2395133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8487efcdd4670c2d7d4be83236c595b530f2f824e3308b25add28b8aaa1fba32`  
		Last Modified: Tue, 03 Dec 2024 08:48:48 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.in-toto+json
