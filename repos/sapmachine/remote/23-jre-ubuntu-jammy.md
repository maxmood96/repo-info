## `sapmachine:23-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:c8800879a4d1220b5a066ac4e6bc2f5318a1c3691afbbcbbf6864d8e02cd804e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:23-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:e6eb390aff3a3501862703579cb9f231511ec59220118e4a7e48a8b00a0b4b76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.2 MB (89229696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844a81d1db289c9492432a95b66aeca9e7682c51995134e409ef97af21ba7e14`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre=23.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Wed, 16 Oct 2024 12:49:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3e3b2c3deb90d899fa3d4c49519a9843eaeec7f91a053c5d9b0e32a94aa39f`  
		Last Modified: Wed, 16 Oct 2024 18:58:30 GMT  
		Size: 59.7 MB (59694008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c433475e53f33b9c9779dc20eff25d95a39350fa7aef12e92b296a9fc5096537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2405953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edfa31e675cddf9be1ca350d0caff38715172fc4f4bc3256e0f928aa5dc0690c`

```dockerfile
```

-	Layers:
	-	`sha256:fd03e528db18296284300321bfd3436a89ac6c6e2a3bc669229c14d66570d48f`  
		Last Modified: Wed, 16 Oct 2024 18:58:29 GMT  
		Size: 2.4 MB (2396705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6320fd8e5e2b20cb76403226266541190536bdee4b75abeeb304774ef0a0484`  
		Size: 9.2 KB (9248 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:508b71966a1370ac112e5231bb05330128aa8d3ac05668d43c39407aa646ec71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86062960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55807b432231965506c695e383ab3aad7ae9022fce83b45922020f5149d2697a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:26:04 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:26:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:26:04 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:26:06 GMT
ADD file:53ce73ebbd6d87a234a33414686f12909aaaf28b7238593f746a327c7d004ce7 in / 
# Wed, 11 Sep 2024 16:26:06 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre=23.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Wed, 16 Oct 2024 12:49:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a186900671ab62e1dea364788f4e84c156e1825939914cfb5a6770be2b58b4da`  
		Size: 27.4 MB (27358329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f84c321bf8f6047ba1bd7eb283e73b1ecfbf4faa54e075c884121ad1040074`  
		Last Modified: Wed, 16 Oct 2024 19:06:24 GMT  
		Size: 58.7 MB (58704631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8790bc5737314aef71a3f4b223bc081bc04d5e7bad944fad961b1514295ef7c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2405147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be707d64dbab0ed7b11fb6b978f15ea3c678d015bdc11158968adfcd1d89465`

```dockerfile
```

-	Layers:
	-	`sha256:07cfe12141acbf2bc4561da19cb6ca6ae8735cc02a75c047c79c11a402e9ab46`  
		Last Modified: Wed, 16 Oct 2024 19:06:23 GMT  
		Size: 2.4 MB (2395778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28fb433af6210877e47809b83a09cfee24383a5ef9016c7263a2286108f63b9d`  
		Last Modified: Wed, 16 Oct 2024 19:06:22 GMT  
		Size: 9.4 KB (9369 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:23-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:bcb63b32cbc257fffe2e2dbe583dd86182841fffb2d36d1700889e446ed9205b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95585724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d556f11b10962b084ed57a11636a9b0c3a58a798ecff60302297796ad4250b25`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:52 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:53 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:57 GMT
ADD file:8b71bf5e48ac3a761ff94511892207fd277c013e3c67b735b87f7338e62bb1f3 in / 
# Wed, 11 Sep 2024 16:25:57 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-23-jre=23.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-23
# Wed, 16 Oct 2024 12:49:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd389594e541fc722f244791a495e1a62a526cb95daeea3d2304d9be4e2f0e2a`  
		Last Modified: Wed, 11 Sep 2024 17:24:59 GMT  
		Size: 34.4 MB (34448242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212bc7a92769920761adc4707e1d201ef02e4a8638c29b46aa29ce148d2d1662`  
		Last Modified: Wed, 16 Oct 2024 19:11:54 GMT  
		Size: 61.1 MB (61137482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:23-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:490994a894b9209a8a9bcf7859c9c0275b9b5bb97321cf40cdcdc30d6fe88f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2409363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d164446ab8b3f3d85e75adfc6b24e3506c810da047a728a5dd21dc25df8c4045`

```dockerfile
```

-	Layers:
	-	`sha256:9508209aca21d8338ad14155b3226f4f16f828cebe63da5dde4ff1b06a483a38`  
		Last Modified: Wed, 16 Oct 2024 19:11:53 GMT  
		Size: 2.4 MB (2400065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:329c8eaed497398fae41f0018e0192c7666b6a89687151e58aeab13d1125fa82`  
		Last Modified: Wed, 16 Oct 2024 19:11:52 GMT  
		Size: 9.3 KB (9298 bytes)  
		MIME: application/vnd.in-toto+json
