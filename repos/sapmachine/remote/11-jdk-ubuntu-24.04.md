## `sapmachine:11-jdk-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:3b2e74ee2526931cbc0fc6d9c2fefaa2215de315f8d7912c84b265aab8967962
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jdk-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:8d26685ab31104401b40021e29c7c0e8cf6b43a76767e62f2905197f6760d8a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (230974703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0989a90ffb5a0008c0d96013941e2fefbdaf2c3d0080e7920a677027879f271b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:44 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:44 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:44 GMT
ADD file:0ebb3dd98809cffc1b5ade76d8ccac01def087e7d7a84a84a33db4aa9090ac67 in / 
# Wed, 16 Apr 2025 10:34:44 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:44 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.27 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Apr 2025 10:34:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b08e2ff4391ef70ca747960a731d1f21a75febbd86edc403cd1514a099615808`  
		Last Modified: Fri, 20 Jun 2025 02:35:35 GMT  
		Size: 29.7 MB (29718366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92874c2a9dd3aa9804bb85eeb1f898b8907aed2017454e8ea7f9d767a386182`  
		Last Modified: Wed, 02 Jul 2025 05:12:51 GMT  
		Size: 201.3 MB (201256337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1c77bb83f7725c6c1ce358cd2724fd9a00d5aa484608efbb3f3fccfc054a263e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2625714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6115c3f4fa050040f5e6e8a66afe31bd1e2ae266557813d1c36f14b2553ac171`

```dockerfile
```

-	Layers:
	-	`sha256:81460e435d48940b0d4478899068870b772a65a2fa911423a526d4821c058104`  
		Last Modified: Wed, 02 Jul 2025 06:04:16 GMT  
		Size: 2.6 MB (2614320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad7eb0a58758b3300d47936631ffc38cbae7beae3d26a029b851111aa913d4c0`  
		Last Modified: Wed, 02 Jul 2025 06:04:16 GMT  
		Size: 11.4 KB (11394 bytes)  
		MIME: application/vnd.in-toto+json
