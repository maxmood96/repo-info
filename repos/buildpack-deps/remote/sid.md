## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:b1f6c14bc86bdca834d62f654f5dd4a85a490d301635f6cd0201417c338e4c71
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:sid` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2cb9d1e21230a34d2756ed3bc7e7c2974c7e2719d68bd4b91d0d3a508f51570c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.6 MB (334556179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942834980133fa8c3d0d1ce767c50b59f2a19154fd308bf3047b03ca6d066eed`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6b1598688dd5948f64dc955f58b0dcf5627fc6bbc5754f5ea08612c6d3bace8b`  
		Last Modified: Tue, 10 Jun 2025 23:26:12 GMT  
		Size: 49.3 MB (49263317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05cec2bdcd950987565d27e6bef170159a9fdde6f46531b0889933354046db48`  
		Last Modified: Wed, 11 Jun 2025 00:01:47 GMT  
		Size: 25.6 MB (25603931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbea8bacad06666c3210aff4437aaea1773f797c5f0e58c28f9f9d0f3ca5ec62`  
		Last Modified: Wed, 11 Jun 2025 00:02:53 GMT  
		Size: 68.0 MB (68042724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b1a15ead1fdc2b27741cd129b839bf3c769c50fda44e4c60084fb500a01680`  
		Last Modified: Wed, 11 Jun 2025 06:50:39 GMT  
		Size: 191.6 MB (191646207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:225762f5db004be7e702dac553662d84fb88cd9c5d2caa3675385decb5738c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16321843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37317bb4186b26931fe654152af2e331d5d8de08f8d682d3d870cb7a835daace`

```dockerfile
```

-	Layers:
	-	`sha256:077164af1f646145cfcf31f5a72df654e06d6b326a74a375ac45f4e6c70cc8a1`  
		Last Modified: Wed, 11 Jun 2025 04:20:45 GMT  
		Size: 16.3 MB (16311667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ff00ebd206d719e4d5ab0b8f80e69a328f5d8e3a9b4e7ea48aef6145fb1bc00`  
		Last Modified: Wed, 11 Jun 2025 04:20:46 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:7f1c8fa4d15ce5a71703cdb0924ede66bde31c60fb1c354bca651e0e3bb61030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299719569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39e2b8b561df5a7771e37fc228d404544208d42aac4cfad0f8d0b811964c9385`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8344b2028cc05a08f8b0b577cc9430fd30421d98f7302a20cc79a7392635ca51`  
		Last Modified: Tue, 10 Jun 2025 22:47:59 GMT  
		Size: 47.4 MB (47435203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e8ec6927bc0cb7d56e990391b853ec23d7d3eb74a5f1f9500df8d5cf23ea4d`  
		Last Modified: Wed, 11 Jun 2025 03:13:46 GMT  
		Size: 24.3 MB (24328621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2085f136199cc5a804201375aeae18b933264b5486014fd2d2c46cfb68e131fc`  
		Last Modified: Wed, 11 Jun 2025 12:21:44 GMT  
		Size: 65.6 MB (65640755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e204187b29a43e4ec106f4ad6c42a78478cdf09f7ab0ba5d8e27c8151c087e`  
		Last Modified: Wed, 11 Jun 2025 09:09:16 GMT  
		Size: 162.3 MB (162314990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8b21303a657b816d65c5263c412f255a390099185975b10380173d9bf98c1f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16093223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d204d4905184e5ee7c1e755b4deb5111287485f061f8e7e1e4c9c3f111986323`

```dockerfile
```

-	Layers:
	-	`sha256:b675300656ddb88f39d9241e4f5c3747e64f5e8fa9c0b1d619fbdabc94eac2f8`  
		Last Modified: Wed, 11 Jun 2025 13:20:43 GMT  
		Size: 16.1 MB (16082987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5315cb718648785f3f1ad5894c2bcabbd95026f0f38c90becc8385e6a2739593`  
		Last Modified: Wed, 11 Jun 2025 13:20:45 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0fe91b2823abb0059a74610002e78de36fff2981413de126df43567c1f96216e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282872835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c27078cf432387030e543a6c4b29f2e246520a5bbe0d431aed77f872c7384d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1747699200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:766cbe9ca16b5ae7e32cf18657be459754ce87056cceebf6831ed9c18fd8a62b`  
		Last Modified: Tue, 03 Jun 2025 18:04:06 GMT  
		Size: 45.7 MB (45698630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b248e723f972fd882067b040659dac6bf0007c9489588821ca8240ce91487131`  
		Last Modified: Thu, 22 May 2025 02:29:17 GMT  
		Size: 23.6 MB (23589756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe087ac4a0ee4d60e25cc222cddf59cdeeee34ea48ec3d3c1cbcb898be35e05f`  
		Last Modified: Thu, 22 May 2025 12:13:22 GMT  
		Size: 63.0 MB (63013467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fa29825fcc6086962844c477c67d2b74406b6d95d3b6b775eb5b504d858d2e`  
		Last Modified: Thu, 22 May 2025 15:36:21 GMT  
		Size: 150.6 MB (150570982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2d30bf7dddc3d1e9a64703611fc405d9d51713931df116f1e8778195e1704c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15817508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a435871beab3ae31c3971b511f1f5d1e4b4ff432a2c62151b4c8d7dee8578326`

```dockerfile
```

-	Layers:
	-	`sha256:9658b68acbc3b469f28b117f78e338d308ce70a79917d12d64040ab2b3b6e4d8`  
		Last Modified: Wed, 11 Jun 2025 04:21:14 GMT  
		Size: 15.8 MB (15807272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a82fc9b3cfddbd5e14da74bce9c1343864292b382f6439f5abed64036844bbb`  
		Last Modified: Wed, 11 Jun 2025 04:21:15 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:08fe5832724b7956c017824d4e5e3e80b2226278e78cf2d36f5c3cb30cc6e211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.3 MB (324300073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9ad869cc435f69d995def276eff92bbb57790556475c1ce15eec6052aa89b6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1747699200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4d7c750dee99fc4f87ba2d4a7a97efd437e614ec9079e7fbf547ab9ce640bc68`  
		Last Modified: Tue, 03 Jun 2025 13:30:58 GMT  
		Size: 49.6 MB (49617866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945b158d051d6fdc917c4a2f2c9c640867150d5c68a1439dd536c0ff065f9eab`  
		Last Modified: Thu, 22 May 2025 02:48:22 GMT  
		Size: 25.0 MB (24976033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ec4c1b10ede551eb1553f94290e8793e9558296a1221a501ace332d77dd68f`  
		Last Modified: Thu, 22 May 2025 09:19:21 GMT  
		Size: 67.9 MB (67868897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabe9a83b4e284c8644e539892c0010aebd2c9ed62f38745ecef178ad23df68d`  
		Last Modified: Thu, 22 May 2025 12:29:43 GMT  
		Size: 181.8 MB (181837277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c76ba4510ff499f41b1a6646530de787111f236d33b8440e03a1576d3e577859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16134090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07035f74e7f08cfff444a10a23e5d32a2f55af04de630d339bca7af3ff6beb64`

```dockerfile
```

-	Layers:
	-	`sha256:1cb475c1e326dde11c574cb71e075cfe22eb1e7217ad5f74c69d2ece628db81e`  
		Last Modified: Wed, 11 Jun 2025 04:21:26 GMT  
		Size: 16.1 MB (16123834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6971baea913db71dff593e7deb831057b90f8ff0672a7f3deacf54bc815a7caa`  
		Last Modified: Wed, 11 Jun 2025 04:21:27 GMT  
		Size: 10.3 KB (10256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6657cffdf30e0c2d8ed41058489d44a657f1fa80f9943fac04775b586378645b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.9 MB (342894158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b5930cf1e788ef575b61ef4f91afbcb635653e442d64d3c9c02d6413bb694a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1a1a02b91b1c2266da4734f34b831bb020d740f7bfd0647d1828242b377de717`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 50.8 MB (50786017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13c1899ec001f75529ee8cd455eb4a23c4b9c5414c63db7730474213c55437b`  
		Last Modified: Tue, 10 Jun 2025 23:36:16 GMT  
		Size: 26.8 MB (26759161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521cd224c201b94f36b1b9e6ba5db4b89c6a8f696946eeacb5bc6b1ac6ed6f5a`  
		Last Modified: Wed, 11 Jun 2025 01:13:31 GMT  
		Size: 70.1 MB (70135021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9f8295eea0ba780cc76f5f5386ee69e8ded62413d3c410f0c2e4115397fe2c`  
		Last Modified: Wed, 11 Jun 2025 01:14:52 GMT  
		Size: 195.2 MB (195213959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3f821e02088d7ac0ed211fd203253a025afa9e2976d1f805536ee219429c88e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16291688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86959247ea0abba2df79d3138d75914e206d769227a6182945e4933a0830c6ae`

```dockerfile
```

-	Layers:
	-	`sha256:53c7b3cfc966152c77a7f74201f1cfdf9b55f0bbbdb827cd8362d105ad4bec4c`  
		Last Modified: Wed, 11 Jun 2025 04:21:39 GMT  
		Size: 16.3 MB (16281534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a779960f8cc74acbc1413a545969066bc5af083af37b00114965844c8cbe25b9`  
		Last Modified: Wed, 11 Jun 2025 04:21:40 GMT  
		Size: 10.2 KB (10154 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:39e2aea94bcb83ff5174d83f77cf91775102cc589eb06af5fba1f88a2f381eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.8 MB (313831045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8220b3082d1ab8355804f02e65fc8726abc1435dced31fe215a33e1469777b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1747699200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:27b34307efc56192fd4ca945f6323e2158a324121ac08b2b6be4739d1a7a2345`  
		Last Modified: Tue, 10 Jun 2025 08:48:47 GMT  
		Size: 49.5 MB (49538322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff848add2d23cbb649ad48161ea5c02c3695dbc152c477b6b7b6ddde8893826a`  
		Last Modified: Thu, 22 May 2025 06:18:44 GMT  
		Size: 25.6 MB (25629837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0328e102aaf6d1ba040810e1f44f2d4a53bb52688eaba926e1237110a438c0e2`  
		Last Modified: Thu, 22 May 2025 14:32:23 GMT  
		Size: 67.0 MB (67034333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f904d88e08bbb9fcf13920ac8532537a0d9caaf511da40144a066c17e06ec17`  
		Last Modified: Fri, 23 May 2025 04:44:02 GMT  
		Size: 171.6 MB (171628553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a449ee4a68377e0621d1c6703334173c33422f7ca17f822007c936e1661f4e8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69347511eeabfeb20c79083b7e2e78e7e25be862af8422b6be584e551bfae57d`

```dockerfile
```

-	Layers:
	-	`sha256:07870d3074339ca747ab1a9c8b9c4196ddf53c76c4e6215e1750e14031ee8347`  
		Last Modified: Wed, 11 Jun 2025 04:21:51 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a19f7348cb3cb5815ab3f4e22ea013ce1735cc83ce5ff7226a184a5f2185ca0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.8 MB (338824652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5bfd536bfd914931da3f3bee4733be700a63658370402e768a625ed6cd4788f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1747699200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:16f5e7cd9c9945be6c34f81a399d644f442eadb5c4f47f89a090f84971e9d67c`  
		Last Modified: Tue, 03 Jun 2025 18:04:05 GMT  
		Size: 53.1 MB (53087015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d194009a872a9d9be939ab0b551a2fd792af6fbbec9e72310f90b49fa15b755`  
		Last Modified: Thu, 22 May 2025 07:32:11 GMT  
		Size: 27.0 MB (26967476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66af6197342ea5f5e1fdaed350b46564c26eed8ea834f6255283150c0e746ab8`  
		Last Modified: Thu, 22 May 2025 12:41:13 GMT  
		Size: 73.4 MB (73381300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b667532fd4b72abbfb06d4f3d90c3f976b6ce441603b54c36aa5d9eb83fd85`  
		Last Modified: Thu, 22 May 2025 16:55:12 GMT  
		Size: 185.4 MB (185388861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f39dee6f1ae34bac1842add915996fd79903ccd7bf851c381a2a7cada00283ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16040956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75dadca3939b5fe4c75aa7eb694d2cca3f3eccf1b830813b9bfd3a7c72b462f3`

```dockerfile
```

-	Layers:
	-	`sha256:869e0b56dbbc3526613368a3c1b7db964fdc7b68a60136a96803805e3223e394`  
		Last Modified: Wed, 11 Jun 2025 04:21:57 GMT  
		Size: 16.0 MB (16030749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e50a7e82ae5f11a598ff2dfe802851998a004a11d99c080f0cbcb0b13a0f9052`  
		Last Modified: Wed, 11 Jun 2025 04:21:58 GMT  
		Size: 10.2 KB (10207 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:0d83223e3f53c52e666f313ba3a00fe274d50b62d9378f76d5d34f87998c08e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.4 MB (408389960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939ec1fbe7245b75d6577550b9de8fea50b78e4ed042956475499949e89e6743`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1747699200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:70274c6f176412a652733a045be62228bfceb31afa5c428bc73eb440514be7e5`  
		Last Modified: Tue, 03 Jun 2025 14:40:24 GMT  
		Size: 47.7 MB (47737557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db4d1c372b0a8bcc5558ebc33a0807a079cce1bf7f64840912ce33adbe79d6f`  
		Last Modified: Wed, 21 May 2025 23:22:57 GMT  
		Size: 24.9 MB (24915395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d77ca161501cc8afd738216058d54ab2ad4f404972c41e87bffedc3f8f0766`  
		Last Modified: Thu, 22 May 2025 01:09:16 GMT  
		Size: 66.9 MB (66891223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5afbeb1d7adfdf8c5da2c61d9a3ddddc1979f60739963d3d305e86b3f0f68d0`  
		Last Modified: Thu, 22 May 2025 02:29:16 GMT  
		Size: 268.8 MB (268845785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f8449c958b0c1612b661417a4ff2f6dcd03a4dda71c56c944c2f3c4f22e72a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16105694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b019ecf8f33e9773567d6e5b57cb867ebad6c897eb1c91ad141ead96fbb51cbc`

```dockerfile
```

-	Layers:
	-	`sha256:27a755c73678df61e7b03ac3b8599ad8a78bf7e837d462ab72673506d2fd9a57`  
		Last Modified: Wed, 11 Jun 2025 04:22:10 GMT  
		Size: 16.1 MB (16095486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2af7578894e3d71d395e9492e0d1ec744692d25f681b329aa2dda5ad518cc77f`  
		Last Modified: Wed, 11 Jun 2025 04:22:11 GMT  
		Size: 10.2 KB (10208 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d57c7ad545bc0c38ab2758c2c2a06f75a1e06b4a728a32366c81218428670ba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.5 MB (306499661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8026cba8778485ddeea5c4b6f063f257ccefd75c9b722f137f829ea2e8a2aa3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a52b4c8ce9959e1107790b0cf878188904eecb5b1ccf411d93d6ab16036dc160`  
		Last Modified: Wed, 11 Jun 2025 02:03:33 GMT  
		Size: 49.3 MB (49343092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf0965e23eb9d70e72f15582a2cb686bcf1857eb924b4d704542fc37d206146`  
		Last Modified: Wed, 11 Jun 2025 02:51:24 GMT  
		Size: 26.8 MB (26769281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc44cd2b9aa97b3fbb56995ed62a657167162e1278b818c7bc6bd60f13d1e12`  
		Last Modified: Wed, 11 Jun 2025 07:20:39 GMT  
		Size: 68.7 MB (68689048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a662117a21d6756827011b9a9ab400fa9db860df9a5da8d3d1a1a8597172c7`  
		Last Modified: Wed, 11 Jun 2025 11:00:40 GMT  
		Size: 161.7 MB (161698240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:98a10f6e1cacddf487ba9d6cc84e03a9aa69ff01ad2c3ae1f7e6689ac2f67da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16088768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38867d0847e9aa3cc7858d65dbb7277cecac6ea10846276e2eeea3f0070a6a87`

```dockerfile
```

-	Layers:
	-	`sha256:6c5a5481488bbe4a9be4f7f0a03b2001cca8feeeb6e48826bf380c6b6bcc2649`  
		Last Modified: Wed, 11 Jun 2025 13:22:04 GMT  
		Size: 16.1 MB (16078592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:922e6e6f9518f191e7921c07bad9fcfd114eb50637eb14e095a971de69370ca0`  
		Last Modified: Wed, 11 Jun 2025 13:22:05 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json
