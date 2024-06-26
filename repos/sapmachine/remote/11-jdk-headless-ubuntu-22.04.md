## `sapmachine:11-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:f238173dbbebab5e6a671b515e9d9c90c68207918ee04ee67a1df6b5dace7c3e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:079f9e1f99d4be26c721b3ebb01e1b19ccb6074ca8f6dabdbf0b19acd56a798e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228998819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766dca8795a7739267f2179df2d4a010ee37fcb5f9fabce565320d4f0a21b3cd`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d655c55ef3325f04d27d3500545b8a0209ada6b80f2686f670ebf11e75bb1a9`  
		Last Modified: Tue, 25 Jun 2024 22:59:12 GMT  
		Size: 199.5 MB (199465065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2cb45fade3e251fe516fae77dc32c9d5eb40def20e5fd3b229478c2c56768740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2229696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fcf2debd4d2bfd493d26325eb83718b8bd2fa77d51cd7354cb32e5c8b807084`

```dockerfile
```

-	Layers:
	-	`sha256:4966abbb5b7a8dd371d8a25d6bf52175fffb09b4707423a44c59a0733f62a91f`  
		Last Modified: Tue, 25 Jun 2024 22:59:09 GMT  
		Size: 2.2 MB (2220999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a36728258e6c1b011d4a7639803308ec2b33dea0badd8373c78817b1278fdfa`  
		Last Modified: Tue, 25 Jun 2024 22:59:09 GMT  
		Size: 8.7 KB (8697 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ad8fabd515e1e4e247adddcecba7cae1d9c2cfa320848ab940800e34626cfb57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.3 MB (225307961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca19d54ca6f5050c3ac5a7408640a002101b4b6843bd0e1ea65d30f58f19bd0a`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae4f99c8601d6b3497a48d959988a64e5c1b84409cdbdc5ac5bb18cd3022cd2`  
		Last Modified: Wed, 26 Jun 2024 00:33:04 GMT  
		Size: 197.9 MB (197946179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:627737a50727beec459e6cafd5d685cbce7c8067265ec20d4810bc253ba04f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2230295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d7a31902cb6d02e46c6c57e38f9b0e190156faba5785a9efc055d4b0620063`

```dockerfile
```

-	Layers:
	-	`sha256:5733c98d35eb89d7ae9b03b3bef46423248cd2ee7339ba3a274374be1d48ebb6`  
		Last Modified: Wed, 26 Jun 2024 00:33:00 GMT  
		Size: 2.2 MB (2221297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:991979bd156e75954f53dfb77eee064d2b8b940d76762ebd87296fee1c41f882`  
		Last Modified: Wed, 26 Jun 2024 00:33:00 GMT  
		Size: 9.0 KB (8998 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jdk-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:fe9429658520d8ac80381a2ea6268d6c7db32fb29ac59ba912913ba17363efc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.4 MB (220416281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42bef8a654c305f43aa7f435b7bde5e07328c53b25150ecf52a717c161a9a7ed`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk-headless=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4185260f5a85604ba58ea9ba6d2a0cf271737a154627900de12264dd5be581e1`  
		Last Modified: Wed, 26 Jun 2024 01:16:02 GMT  
		Size: 186.0 MB (185955588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fb78c8effd89c79ad5936105cf4c73d9a41e93280ff281d578a8f692f19e8bf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2231069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a73ce2613e92db56617c54b0977ab81d8254b5225ae567dbf90883b93623a72`

```dockerfile
```

-	Layers:
	-	`sha256:37b710a755c1bd2aa43c8849068f419df7f9d479654286cd8deb9bb6de46fc3a`  
		Last Modified: Wed, 26 Jun 2024 01:15:57 GMT  
		Size: 2.2 MB (2222334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:602ee5f1bfcfa23e5b113a9e41b14cd275669f476afb171458ea85a2acb53f85`  
		Last Modified: Wed, 26 Jun 2024 01:15:57 GMT  
		Size: 8.7 KB (8735 bytes)  
		MIME: application/vnd.in-toto+json
