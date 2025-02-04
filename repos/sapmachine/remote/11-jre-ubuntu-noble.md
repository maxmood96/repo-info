## `sapmachine:11-jre-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:385d4136fe89745dd3351400e58230afe305a3896fd9eebb45b09d35bf95f425
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
$ docker pull sapmachine@sha256:caf94cfbfcf4baeb6856058d6d8a2c521cb7dd0a1682da54c88df0525195d3d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80126110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f45e8b3c19d4df080a4b520b398f51b35798e3a7ee7c65c5431a2471bea721`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:19 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.26 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 27 Jan 2025 13:39:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528b711767b363837e6a8eb6cc2aec6be1b2b947026ab98b2a0ac8767f5ba0a3`  
		Last Modified: Tue, 04 Feb 2025 04:50:18 GMT  
		Size: 50.4 MB (50371820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:337fb208e4b3fbd3b8c0486048cd9c7c868fe0928b76a2bd3414886a8496362b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2403258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7e748c02d0d4563fd7e1f9d20c6de4ff0de510b85ac8cdf516e24b86c637637`

```dockerfile
```

-	Layers:
	-	`sha256:693525b151809e83a6b13862a9f51d6b4ee4efe937926afbc2cbdfa1c6172ca0`  
		Last Modified: Tue, 04 Feb 2025 04:50:17 GMT  
		Size: 2.4 MB (2393787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bdc10f9a13a3bb5906d9820dc280381f09ba9a64448f612da5867f51b075a48`  
		Last Modified: Tue, 04 Feb 2025 04:50:17 GMT  
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
