## `sapmachine:21-jre-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:c6b0731bff6f81962227dace31b80f4112876d067e695fad733a824869a49dd9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:a2e5b0336460565801230541d1dbdeb487772942191a22d3d8e90be8cd0ebe97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.0 MB (88048591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b570d112dcdd0210b90572a8a79ca9d276b16b522508214d4c98f2863717b2`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef7ae22bbab8ed7fa09aa6bf98c84de16c5ce81ec3a84222611aa4a2462e905`  
		Last Modified: Wed, 02 Jul 2025 03:13:00 GMT  
		Size: 58.5 MB (58512905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8b7408b0c5fb3d22c341de8a438e85705ba9a4f99b9d5fe4b6c59be04a700b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2304423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b49e35b10548a19210eaf3c1c75b3172a3d4b2e6b3c40d93abc0ef17770e9b1b`

```dockerfile
```

-	Layers:
	-	`sha256:51b051dd5eab30e41deb7e7bdc8ce2292d9f011d41be4e32e6b4e6a37c06d71c`  
		Last Modified: Wed, 02 Jul 2025 06:07:59 GMT  
		Size: 2.3 MB (2294797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94bf444ad8e2c8943d961c9e88fc72cd0aff71665060dcb921eeab3ebf7d2a6b`  
		Last Modified: Wed, 02 Jul 2025 06:08:00 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:fa99ae9f876f63f0acb11b70d31f96208e5173e152c32e2937a33eb5248b36e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.0 MB (85011789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14d09a2a1d95564b7b74955986754f43ecd02925b7ec8f3adbc2ce6a5db3d10f`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08346ab44796d01445fef33aa694c19d8ac1e4a3e2fc3b8a8d210fa5ca94ce5c`  
		Last Modified: Sat, 07 Jun 2025 16:11:53 GMT  
		Size: 57.7 MB (57656208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:958385b0a44e2b0fdd3e5917c38eb757531e8da2df897c14000b4d0f96d31bb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2199461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f1bb6f04d377eeba9c7d3ebbef76f4a76a7815a73065415ee09aaa71fa8fa0`

```dockerfile
```

-	Layers:
	-	`sha256:30825a98748b63802b6d34ab2edd1a8614c1a25813153b9877ba234f97803075`  
		Last Modified: Tue, 24 Jun 2025 17:44:57 GMT  
		Size: 2.2 MB (2189706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89b25c177483246c780cf424c08afb7ddaf1611f4dc0ba886854b2a3a7790c6e`  
		Last Modified: Tue, 24 Jun 2025 17:44:56 GMT  
		Size: 9.8 KB (9755 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:41ba376a92e5a3545fba1d6591be7eeab479f1ce2706efaa00ceae64079fbf19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94353537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25ac3dc79e0d082d58ce4fd7fd1288b24d4e2a113b1a199d39c9242c13117d2d`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db06309b0f2974b8e3b7ba4bb536e50542c976d9d9d76ddb1ce95e38f4284ef1`  
		Last Modified: Wed, 02 Jul 2025 04:57:03 GMT  
		Size: 59.9 MB (59910916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9c46d11f0f96fa7bfd892f3e4e039ffd886553504c87411202aedc4eb519e699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dad678d0a2ca67d46ee092ae15c0208d595a7e794613b14749dae41c4525100`

```dockerfile
```

-	Layers:
	-	`sha256:b74367805050a1acac96c057d50166b6e4354f8a73875cca5540565071639906`  
		Last Modified: Wed, 02 Jul 2025 06:08:08 GMT  
		Size: 2.3 MB (2298850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57d4fc719612e4b631dcc20da3a73c429db5e5b1199ffad313e558dba49c1179`  
		Last Modified: Wed, 02 Jul 2025 06:08:09 GMT  
		Size: 9.7 KB (9683 bytes)  
		MIME: application/vnd.in-toto+json
