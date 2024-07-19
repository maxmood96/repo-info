## `sapmachine:17-jre-ubuntu-20.04`

```console
$ docker pull sapmachine@sha256:1ff4a88e773983765b3e68edd87cae22888816b08e6e637749597fe7a0e5a972
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jre-ubuntu-20.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:34363ebe6c83542ba90804e64edee66add1d4b418ea52e62df25f63c6390469b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.8 MB (80770275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547ec9213d9663bbb2d19ae1c32a11824ea072596ca6da04ec06a02631640cce`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 03 Jun 2024 17:10:41 GMT
ARG RELEASE
# Mon, 03 Jun 2024 17:10:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 17:10:41 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 03 Jun 2024 17:10:43 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Mon, 03 Jun 2024 17:10:43 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ea8908f47652b59b8055316d9c0e16b365e2b5cee15d3efcb79e2957e3e7cad`  
		Last Modified: Mon, 03 Jun 2024 17:19:42 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6908e05148638bd2a7b9f4b0ebce6e587992491f09b90cd4339ed0eda5d291c4`  
		Last Modified: Fri, 19 Jul 2024 18:00:16 GMT  
		Size: 53.3 MB (53258506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2be33eefc839fb8b834990a5d33751d2274aaea0b2cad1756016c090ea7b7358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2288208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39623cd5f36c1ac009241cf4047aa7a4574fd38d6545409a78494268c17fee42`

```dockerfile
```

-	Layers:
	-	`sha256:e8c1600ff4bb4e46a45953c0e913afec0dde38f66313bba4dfc063cd85916285`  
		Last Modified: Fri, 19 Jul 2024 18:00:15 GMT  
		Size: 2.3 MB (2279641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f0605bb8d3bb9fa3d106ffe8862044bffe6e4452a1401d5ec4f6b8ff432ce29`  
		Last Modified: Fri, 19 Jul 2024 18:00:15 GMT  
		Size: 8.6 KB (8567 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-20.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:03af048d859361370edff6851cbd93b7e8a5889b4c92ccdacbc6fd100309db8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.5 MB (78544931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c4b5635599c89044435445b258b7f279c185344e102133729db65af126116b`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:54 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 13 May 2024 10:06:54 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Mon, 13 May 2024 10:06:54 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:54 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 13 May 2024 10:06:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f02209be4ee528c246399de81af4552e52adb005a8a499815607b6b0d42746bf`  
		Last Modified: Mon, 03 Jun 2024 17:19:48 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9249bc1f05ef41f821353e5554c8b46b563c3d876b8472dd4cbd5f9e68226d`  
		Last Modified: Wed, 26 Jun 2024 00:25:51 GMT  
		Size: 52.6 MB (52570714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a0e8cf6bd1284b4b7ecf31fbb7947a6f9ffba1ccd7273b99346a000ecda8d74b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2261577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f4d47ee4899545f6cc4833700e14530fbe23d81f02868b03fd2538fd5ab7a94`

```dockerfile
```

-	Layers:
	-	`sha256:77e7311837dd83f45faf218a7206091bc705925e30beb297ef876bd8fb6990ff`  
		Last Modified: Wed, 26 Jun 2024 00:25:50 GMT  
		Size: 2.3 MB (2252691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13d01f748ae27b8500183ae1bad0db77eb982ff7208b844e12ddc2a31b97f540`  
		Last Modified: Wed, 26 Jun 2024 00:25:49 GMT  
		Size: 8.9 KB (8886 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jre-ubuntu-20.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:e2aeeb0efa62f3e8520487da6764d80743669c2688010db7fd4f0bcb051e0203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86374679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c2bc5d602a912a10446dfd5d7fe910f2c63c437dfe5dd0ddcee7cafdcac0bc`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:54 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:54 GMT
LABEL org.opencontainers.image.version=20.04
# Mon, 13 May 2024 10:06:54 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Mon, 13 May 2024 10:06:54 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:54 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.11     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Mon, 13 May 2024 10:06:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f3b175423e2add884b475baca08015a389b9791d811b3b5578a0b60aeb7e2923`  
		Last Modified: Mon, 03 Jun 2024 17:20:01 GMT  
		Size: 32.1 MB (32077140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e3d9f9417468cf4bc5fb7567b65b3248f44b34f3c2341d59c3b5ac21e8c36a`  
		Last Modified: Wed, 26 Jun 2024 01:04:37 GMT  
		Size: 54.3 MB (54297539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jre-ubuntu-20.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:695c4080a919e753490f522fa686220f6b7ce0a7a5891170e3783a7cd4bc2a65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2265443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb6a23fa45db851f872d08640b6bbb6f58b94b48c32ca286dc29c19fce70dbb2`

```dockerfile
```

-	Layers:
	-	`sha256:97e993f5f04bc77454b1856fdd8756b91f8ca65cff6dbd9e285baa2b5b1b497a`  
		Last Modified: Wed, 26 Jun 2024 01:04:35 GMT  
		Size: 2.3 MB (2256820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02b8c6185cf00a954622e25a21f63cd0fc93447e76f0ce074f295ffcb58764d8`  
		Last Modified: Wed, 26 Jun 2024 01:04:35 GMT  
		Size: 8.6 KB (8623 bytes)  
		MIME: application/vnd.in-toto+json
