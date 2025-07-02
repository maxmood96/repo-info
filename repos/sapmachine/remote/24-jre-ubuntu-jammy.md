## `sapmachine:24-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:a99dd288930ea258233587bc0e467995dae4d4ac4e153e9b62397e8a3ea8313c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:c787029c2f9094d00fb33232d6b015be29aa4a42ddad7e41de31ccca8b8a4097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97215709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5eeb0c3c44fec6294162b215e840191c1906fd0d5e6fdd1fbda14f18ebec96`
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
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebf34cec58cfa98f7441a9346994b2765732ea91915c140bf14a46150dcb876`  
		Last Modified: Wed, 02 Jul 2025 21:10:02 GMT  
		Size: 67.7 MB (67680023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:682d32ad42508bfc150d616a573b73ae4b3a675f654884706f5d41f9a7f25f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2562041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d2cd9a4ce737be0dc7a7921e5cf8b404b54a9bf2fce4f2dcb3259811479532d`

```dockerfile
```

-	Layers:
	-	`sha256:72d4f6501469eb2cd6444469ca14156f56f767f73c38713c956a41092273d5c7`  
		Last Modified: Wed, 02 Jul 2025 06:10:10 GMT  
		Size: 2.6 MB (2552577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3413aba095611c0f0ba527c0d95fc8d42961696a7cb34eee342ea2a0ff5e6030`  
		Last Modified: Wed, 02 Jul 2025 06:10:10 GMT  
		Size: 9.5 KB (9464 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:de7e42924999d19502fb2b740ae832593e0febf3c6bb171771635fd45c1ceae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94034441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:454e56bdbd0d18d8bf20ad99d160d968c844e110b1de94c0358379fbc5eed91c`
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
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b53a174b6471ec89e7306a6255a1744ee22a6fa9f2d19726aa43ba521d9a8ad`  
		Last Modified: Wed, 02 Jul 2025 06:37:01 GMT  
		Size: 66.7 MB (66675169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a1addc7388b739977ee1e517e99b13ebc3eb5098da0ccf4ca3c38da7a7a4b82f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2561871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838b1d56028c774a8caac39079caf61f51ab6b840649a3d224f6664e98907fd2`

```dockerfile
```

-	Layers:
	-	`sha256:713412aba17b362a234f4908adffd22264a21646327267b58cacf2a0f5eb8f0a`  
		Last Modified: Wed, 02 Jul 2025 09:08:45 GMT  
		Size: 2.6 MB (2552280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d565586100e02e0efb155e296ad52bad50140a0877344d360f1160350f93d1eb`  
		Last Modified: Wed, 02 Jul 2025 09:08:46 GMT  
		Size: 9.6 KB (9591 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:b3d8c934855d4715be31388e37eba93e8908ba0adaacbb6b0807173ebdef07c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.4 MB (103392537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63bb1870c82a837cba1cbcb6b96fc30904fef9d160f07a63cf1d55458826e887`
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
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa07063648c11bb38fc383a08c8693723cae48f6508607d3f4237c6e5ee72b51`  
		Last Modified: Wed, 02 Jul 2025 04:44:49 GMT  
		Size: 68.9 MB (68949916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:71509e19ba53487b3947ba3493c5bef8873b0a71dc85070b3bba21b968fdc4d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2565610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e83c313e9b27222540c6313a93550dd7f202ac2401582cc8e67491185400617`

```dockerfile
```

-	Layers:
	-	`sha256:efe83fe53c3aafb969ecbb711ec8a89f83e20f02883bc07c7b2ecff2f5401f92`  
		Last Modified: Wed, 02 Jul 2025 06:10:20 GMT  
		Size: 2.6 MB (2556090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b18d2f62bce81e2afce9dc1a9c8e29738f10ef3395a28374a6d12e224122719f`  
		Last Modified: Wed, 02 Jul 2025 06:10:21 GMT  
		Size: 9.5 KB (9520 bytes)  
		MIME: application/vnd.in-toto+json
