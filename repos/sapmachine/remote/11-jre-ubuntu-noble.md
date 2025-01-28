## `sapmachine:11-jre-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:6058c18ae729dec2d33fdb70d6561fe751feeca6711f3e5a0444165e4a2c344b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:3cf1a4f4ee9f755d86d03f19b4614c011630ae793d0272467acffa8dcb17106f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80123873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438bdab3e6cf901f003f50282f04e94e5a0d862558a926ac7e397b6cda4a9d7f`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Nov 2024 17:29:23 GMT
ARG RELEASE
# Tue, 19 Nov 2024 17:29:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Nov 2024 17:29:23 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Nov 2024 17:29:25 GMT
ADD file:bcebbf0fddcba5b864d5d267b68dd23bcfb01275e6ec7bcab69bf8b56af14804 in / 
# Tue, 19 Nov 2024 17:29:25 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:19 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 27 Jan 2025 13:39:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:de44b265507ae44b212defcb50694d666f136b35c1090d9709068bc861bb2d64`  
		Last Modified: Tue, 19 Nov 2024 17:38:27 GMT  
		Size: 29.8 MB (29751968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550275249d62cbb28a031eff301c5f45fe7fcc8eff60098a4d253d41eb6f46ab`  
		Last Modified: Tue, 28 Jan 2025 01:29:05 GMT  
		Size: 50.4 MB (50371905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:65001ec31dae50a58d4d0ac1b357c0bf0f14adea094e9ef9819ebaf3981dffae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2399296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a8f49cc238caa4744d52cc709dffddf8b63dad45aeefe832b3f251a4f8815f0`

```dockerfile
```

-	Layers:
	-	`sha256:041ba93cb111a1c5f953fd781860719579225fa612f5cde2bdc2edcd6042b8b8`  
		Last Modified: Tue, 28 Jan 2025 01:29:04 GMT  
		Size: 2.4 MB (2389825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e176235e9f10f330865ba3e020ccdac25cd3bab73153e8f0319eab281140d167`  
		Last Modified: Tue, 28 Jan 2025 01:29:04 GMT  
		Size: 9.5 KB (9471 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:326c8fa3ec022fe33e2af26dd4fcb8318cf4e64c3e9374f439a045df2c1ad346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.6 MB (78604678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31e8f2e0b9d605562c41e2d5ca1e731015f9c292d7672385c6e3af0800ff6bd0`
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
ADD file:765dfd09ec2ac4870c8b3efd6ef4a994f99695c574d546d7a9a0e69bbb970b03 in / 
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
	-	`sha256:8bb55f0677778c3027fcc4253dc452bc9c22de989a696391e739fb1cdbbdb4c2`  
		Last Modified: Tue, 19 Nov 2024 17:38:33 GMT  
		Size: 28.9 MB (28892671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a23e8236ceb537640e3dc165a8bc4fac09da7e6929d6fe50f5025ca9a3e9ac`  
		Last Modified: Tue, 03 Dec 2024 10:57:02 GMT  
		Size: 49.7 MB (49712007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8b4bd67074d506b653bdc9abfb35a051135da0adea3d1f6e8871ffc7ff29af58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a635634b52505fa11e889afb27fedd0be05ba858c38027d038a522d697669e`

```dockerfile
```

-	Layers:
	-	`sha256:b04f27303dcae8eb50270da0e98f94bcdbe1cbddef9f1aa7b43efb00193c7ba0`  
		Last Modified: Tue, 03 Dec 2024 10:57:01 GMT  
		Size: 2.4 MB (2392297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2e146497dc15126013b0cc33cdb2e6f003e64dbf6665084f9027b4ed3f37bdb`  
		Last Modified: Tue, 03 Dec 2024 10:57:00 GMT  
		Size: 9.6 KB (9599 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-ubuntu-noble` - linux; ppc64le

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

### `sapmachine:11-jre-ubuntu-noble` - unknown; unknown

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
