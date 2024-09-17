## `sapmachine:11-jdk-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:2d7073851e0f72beb308c3ea6e7c9acec98b7af3248e435b57fe688e82e6170e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jdk-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:cf88797915dbc4832aa5818ce5b46fc1315ecfaaa190dd43a730ab6732d34e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230270901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbb221bb1c6123239ab03777916195ef313aee77f9f6a1575750721f6a2542de`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af43ed6fb4deb7b0800847382a4cdae401a2d36d8a96726445207b37e46df74e`  
		Last Modified: Tue, 17 Sep 2024 01:01:19 GMT  
		Size: 200.7 MB (200735213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1be80ea3b944b3a861897b6759e2fce55ba55a203344af3f10b26c8595298d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2499036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62efadf00985fe08876e5988dcf098719551f6f40feed9512d7a397226d598ac`

```dockerfile
```

-	Layers:
	-	`sha256:02183fe0b9944731047c8d46cbbd7a833665a1e0179c47e8377e56be52c51a5a`  
		Last Modified: Tue, 17 Sep 2024 01:01:14 GMT  
		Size: 2.5 MB (2489152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4038074caab7b56cb60b8771df04e6d1ae11aebd356cd3ea44d4c89e5adffff`  
		Last Modified: Tue, 17 Sep 2024 01:01:14 GMT  
		Size: 9.9 KB (9884 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:db831ea86d25791dee8ed8f20f5265d6e7cb9bf82cbc524fa6614b9def2e042a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.6 MB (226551159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ada204e22c2373abc06ece784c1d7ee4e63db424b4165218051b8df803d67d`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755c6b5fc9ded1562eda8353fe656ada8b14215502678ef93de1d56c8ee7aa64`  
		Last Modified: Sat, 17 Aug 2024 04:45:34 GMT  
		Size: 199.2 MB (199192476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:6a142d099aa0aff7f7fe0117ac14da52c26a60d8e40e601013d8cd04e70cb9dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2499740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fde960efd270fb8f6fd5376cc707e1069aa47238f43a14a768232cf0df684a0`

```dockerfile
```

-	Layers:
	-	`sha256:71af787178068853af8f1a3971c25dd19320180ba58975b0fe4bfe63a9f13923`  
		Last Modified: Sat, 17 Aug 2024 04:45:30 GMT  
		Size: 2.5 MB (2489508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9926fba49eb7a38332c5e77997fde16ce0861e9d822a46d760c25831c9cd7981`  
		Last Modified: Sat, 17 Aug 2024 04:45:30 GMT  
		Size: 10.2 KB (10232 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:8f3fe75d839f792bc3e543f0f69bcef108c0eaa190bfab5a7a5a1050ec8101d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.8 MB (221846236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf4a48fde87f3b4c4be607d2c7c753e5055e352bb4a60e4c01f227ab635eba7f`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:19 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:19 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e0aacbb6089cf147697d708102cfc52fb7689ce2464b5a29689fad50d8722a`  
		Last Modified: Sat, 17 Aug 2024 03:33:50 GMT  
		Size: 187.4 MB (187382058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:86e9e1fc90e991175e5ade6e14dbe8eb930d8723c14b081c82e66db1a90ed102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2500527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff5a1495b0071397233a5b2f44ffc185ac67b9633d53af57159fc3eec47ae3f1`

```dockerfile
```

-	Layers:
	-	`sha256:7b3240db715bd6e32b54660503f2195037a0c65928768709862ea3c6c77c1751`  
		Last Modified: Sat, 17 Aug 2024 03:33:45 GMT  
		Size: 2.5 MB (2490581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:155a57259b8ee4c41dc84e3a66c503d7b54800c33e7a23175b6a1d6e867238d5`  
		Last Modified: Sat, 17 Aug 2024 03:33:45 GMT  
		Size: 9.9 KB (9946 bytes)  
		MIME: application/vnd.in-toto+json
