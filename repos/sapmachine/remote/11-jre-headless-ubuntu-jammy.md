## `sapmachine:11-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:ba9b323cbc01eb5d0037d2c5ed7ce3b5b02be80de32046c333447cb46a5eebe2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:9d8da464e69cee39a2d8357af926228c107aea01c9837c7ad7f0155cea05311c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78319025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fc20b1d2bd9999936c707f2cd80a72ec483a8b1e04dbe83bd3c8a3ec0531b81`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:44 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:44 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:44 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Wed, 16 Apr 2025 10:34:44 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:44 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.27 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Apr 2025 10:34:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31dafe19c08a62ad993d8e861857c76ab9f6f26def1250e5432f043f2bce971`  
		Last Modified: Thu, 03 Jul 2025 16:59:52 GMT  
		Size: 48.8 MB (48783339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c7d4875ee8ae7099e98cbc1c44cdbf0618911f7faa9f37ec2387d18d6dfadfa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c08c8d1114f95d36da03567439faeb0bb9dabcd5088a7a44c3e6b6be180f5d54`

```dockerfile
```

-	Layers:
	-	`sha256:4cfd78aeeb9af1e77ca05af902e82ac6bb44209002b013f8f2a6e176c6a70063`  
		Last Modified: Wed, 02 Jul 2025 06:04:38 GMT  
		Size: 2.3 MB (2299090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2f2725e8294fe7cd80376f795accee7c0b4787e6610680c55e50a2a27222013`  
		Last Modified: Wed, 02 Jul 2025 06:04:39 GMT  
		Size: 8.9 KB (8932 bytes)  
		MIME: application/vnd.in-toto+json
