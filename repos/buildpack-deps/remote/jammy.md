## `buildpack-deps:jammy`

```console
$ docker pull buildpack-deps@sha256:35457157c06db1132f87dafcc21385abb5d97c542680c856526f9481db86faa8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:jammy` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e7cacba24084cd459c248a57ea733c45131417fbe775648a859cc0f73dcd50e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.1 MB (249066787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e6f0d302822653c5be3126d2ed2e495c02d294362ddf25777d8c9e3756ab0b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6828c7dda7e5e4b9c82ddb483379bdc791aa9b7cecdce2c883c603e7806ea9a`  
		Last Modified: Mon, 01 Sep 2025 23:07:56 GMT  
		Size: 7.1 MB (7106278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3856fb40e8823986f0d2b16e4bb928a603347223ee232458482a4a5a7b70b7`  
		Last Modified: Tue, 02 Sep 2025 00:12:14 GMT  
		Size: 39.5 MB (39487201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7b65e6fafecd199cb99814a4d4bc3298d0c486580723cf34f8b5c6f8a0d4f1`  
		Last Modified: Tue, 02 Sep 2025 04:27:02 GMT  
		Size: 172.9 MB (172936373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9f53ce0bb9585214f1d5623af56ce5cd98b5a36407f19caafb028803274b989b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11849737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d36242650dfaae2e599113f88ad7e1b7dc534f7c2380f6ef5362be3004c00ba`

```dockerfile
```

-	Layers:
	-	`sha256:03dde242051f62edb4122dd6706db600872a4b4f5ffeb79b3f73b9d44a42f3d6`  
		Last Modified: Tue, 02 Sep 2025 04:19:26 GMT  
		Size: 11.8 MB (11839534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:903790ec039fa1638d35cc2535769906f7b78d86f608c1775f6c19f2e9962e18`  
		Last Modified: Tue, 02 Sep 2025 04:19:27 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b6a910f886eb885652d04152ccfcbb0aa639f824e4938415db269f0bada0589d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.3 MB (216299782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed22e838036cc01c478b941a8017979d1f272b949366f0c697f354eed8058dc7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:1b718ac25471aa07aabcef27ec2e737bdbf36fd950c8d6e6103ad3dfeacd8e98 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9e6391cf5a380a152971ee67d9bbbdd494023e7e2a2da9c7b92dd6d51593fee6`  
		Last Modified: Mon, 01 Sep 2025 23:13:56 GMT  
		Size: 26.6 MB (26642908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bcfda65d1847d88965f302b038b1be953284583ebd165847009e51bcab6359`  
		Last Modified: Tue, 02 Sep 2025 00:11:15 GMT  
		Size: 7.0 MB (7010211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5839f3de1edd0068423e4ae7e1e8d6070d3ebddb4b805fa9906bbef0f54e2c05`  
		Last Modified: Tue, 02 Sep 2025 12:59:48 GMT  
		Size: 42.3 MB (42251995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2beb96fe290c51797cdd40352bc2694233b141a6ff13ad7fa58e3dbc8194915d`  
		Last Modified: Wed, 03 Sep 2025 14:11:46 GMT  
		Size: 140.4 MB (140394668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6f717adfb5c5e76a801e81798a9623f028dbdd337881423a806f623d95f9fadb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 MB (11639006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d6ad5a30a80edbe3de840811a9d2da1cd6b540b87ca736f416f073893e82f71`

```dockerfile
```

-	Layers:
	-	`sha256:9d92bc7cbdc1f3093dd5a686f42f3c46a8c20d37049749e4906c4beb1b244fb0`  
		Last Modified: Tue, 02 Sep 2025 04:19:37 GMT  
		Size: 11.6 MB (11628743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa63321c05fdd7496353c539ab7f7315dc36eedddb6a0847c373e5588623a26b`  
		Last Modified: Tue, 02 Sep 2025 04:19:38 GMT  
		Size: 10.3 KB (10263 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f5dee007520dfb0f9cc8a5ce949f27ed915a4e0b6aab192af8d6d08c3b9b0354
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 MB (240249528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7352fb36f91e90b7da1ba1216889447c6a0f648891e026fcaadc43d52ae2a114`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573b56f55094f2d14930c686b1a46091f6f5d62cadec0da94af57c5297b32867`  
		Last Modified: Tue, 02 Sep 2025 01:18:59 GMT  
		Size: 7.1 MB (7051940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508724dd86b6f1e696d30cba1d227b5e49b51dccaa040b0346816bfab7e8160d`  
		Last Modified: Tue, 02 Sep 2025 03:45:54 GMT  
		Size: 39.4 MB (39384407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c74be5359884f0e8e03df384411227c79f54873e15ae9c009b0514c5ecd3d1`  
		Last Modified: Tue, 02 Sep 2025 09:41:52 GMT  
		Size: 166.5 MB (166451712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ce87104d49850859484ef285ad3bff31665b562ceb099f72bd7ca1d4ef6bc81e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11845483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c8dfbc2cd34326c63dfc9eee32af00985cfdaddf3b0abbd1bf304541f8cd2f`

```dockerfile
```

-	Layers:
	-	`sha256:5c0b275c7a3cf528cadfaf559a50b64b88bab7bf25f29e6393c06ee253433dfe`  
		Last Modified: Tue, 02 Sep 2025 10:19:33 GMT  
		Size: 11.8 MB (11835201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5d8622a23eda5409d07f4d75305772fb666b378bf4016b1dcfcdcdcbcdb1b9b`  
		Last Modified: Tue, 02 Sep 2025 10:19:34 GMT  
		Size: 10.3 KB (10282 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9da2e71c24894dd4033744e45e3f45ba74542f840a6236937ec6778608b8c6eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269810357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d94c1c57cd02a7588175aa693292c6e4508d700d08ecfcf9ea31b335cd0c5b1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:da179546f976792ede40255758ecaed39b1e36eacf91ef3899fb0ec36863ccd6 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f898542d1cc6dfc233b10b2c9c711f920b80c44eb0a9c8b0df300ebedc3f27fd`  
		Last Modified: Mon, 01 Sep 2025 23:16:55 GMT  
		Size: 34.4 MB (34443224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3f77bc9e4ab6e5fb5af578f087cd1cd7d1b42df4ce3edcb7205e77fa641e55`  
		Last Modified: Tue, 02 Sep 2025 00:12:15 GMT  
		Size: 8.2 MB (8184933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06d2fcee6246a83413eafcec3d64fbc5be759a0ab354df9c761fc5007cd6746`  
		Last Modified: Tue, 02 Sep 2025 05:24:06 GMT  
		Size: 43.8 MB (43760164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10d7edd685c2fbf1e8c5842486db95ff4f30daa5e21dd95de3d6225c6713da2`  
		Last Modified: Tue, 02 Sep 2025 12:59:57 GMT  
		Size: 183.4 MB (183422036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:262a5e75fb936afc2b4ee2a65aa32eef50c7b0342c175459bcaf80291daa04a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11809134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1abf7099d882108279c2743145dd8f2837f88cf0185b4b52195274af404783a`

```dockerfile
```

-	Layers:
	-	`sha256:01be9f109ca4d96721e38a1c3fe39eae3f9e767a300a20738fe86112cd433013`  
		Last Modified: Tue, 02 Sep 2025 10:19:42 GMT  
		Size: 11.8 MB (11798899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee325842ac73bfdd9274469a370832361eafed0c075c7c7eded94cba2d6823a3`  
		Last Modified: Tue, 02 Sep 2025 10:19:43 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:489fdef8a51f95eeb931b30ec800babfb1dd29a9f366528da25ac83106eacb22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274258651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83a385dac04ac1c7c81b9397256e98f2b55de964751874884d25380766c0a69d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:35770e06fa2c1cc2b759aaab361c62ab900fac2d6b612a4403b76189d7f2ce82 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1de6ca2b6a61e33f0f8fae9da1d47f9afcb02341cbe72eeb6eed6979ef59b090`  
		Last Modified: Tue, 12 Aug 2025 17:04:15 GMT  
		Size: 27.0 MB (27042020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2831747a0034f903385b005efb41ad90f86cbeed2dfb31e5afbe06beb4de45b9`  
		Last Modified: Tue, 12 Aug 2025 17:26:12 GMT  
		Size: 7.1 MB (7118185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328660fbda39277d782f765a5900fe7c253fb97800d915b2c262f417749954f0`  
		Last Modified: Tue, 12 Aug 2025 20:48:45 GMT  
		Size: 42.3 MB (42304868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa27faef0952308c571df3bdefad5e4c2300bdd3124664ca7930e9385a81eebb`  
		Last Modified: Wed, 13 Aug 2025 04:30:39 GMT  
		Size: 197.8 MB (197793578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1dccd3e3c1e9bb3802e510740651b6e5d31ec5503a793b7032d544fb089b6741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.8 MB (11790062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead826dc2aaff8f2478f12b1725767670bde5dbdf969a4c77e57687fef3e4432`

```dockerfile
```

-	Layers:
	-	`sha256:38e489bd7739ba64d6fbfdbdefbc126a132251d72089f44b03fad3ae2b448bf9`  
		Last Modified: Wed, 13 Aug 2025 04:19:43 GMT  
		Size: 11.8 MB (11779827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b09b98a3270112cd0b0a9ea23e1c59ef3742f0d27f9c9817ba56135aecfdb1c`  
		Last Modified: Wed, 13 Aug 2025 04:19:44 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b4a662babc502cca1e3e9801ff68a6969c9a61dcd54f6326a5dfa70eddee873a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (223037019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8eab41e86af2eedc241d3eacf9496ccf30b29daf09f98c92cc5f4e7d647adbb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ARG RELEASE
# Fri, 28 Apr 2023 21:58:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Apr 2023 21:58:08 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:29917512cc6cafe60268e67a6ab4ee1e581cd8f4c2bca9a228ba5a680375b746 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["/bin/bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2109104756ac117958527cffddc193d2cf33d0621953649a7d5800a93fa86665`  
		Last Modified: Mon, 01 Sep 2025 22:59:18 GMT  
		Size: 28.0 MB (28003668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa3acd4828544874bb6a8619273470054d87a7f950b1770dff8640fbeed8822`  
		Last Modified: Mon, 01 Sep 2025 23:08:39 GMT  
		Size: 7.0 MB (7018642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5fc7403e651ec72941a77cf7eb2a35d461bb2dbe2f532ebf625eed2e5ab8e5`  
		Last Modified: Tue, 02 Sep 2025 00:18:29 GMT  
		Size: 39.4 MB (39419805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bdfe7414620055e4a4b88b87dd117752621491f3a4a835a699b337c7ba9482`  
		Last Modified: Tue, 02 Sep 2025 13:00:18 GMT  
		Size: 148.6 MB (148594904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7d4966a54faad1a896bbcfe960869afe16e563d3d43fd42e58d9a6e8a8daeb6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11663614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:333ebb03d53f867f4c6f1b0f56cd8e20e17d0f1ed8ffd637240cb9bbeaf501ac`

```dockerfile
```

-	Layers:
	-	`sha256:b6072b0b66ec42621b545f9d926e748ea46c7522290d0994d8f7d9573b68e032`  
		Last Modified: Tue, 02 Sep 2025 04:20:16 GMT  
		Size: 11.7 MB (11653411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d26ede4d6641c609fe3740ba611ddb531ae207d54fcfd531fc97d431090d3f55`  
		Last Modified: Tue, 02 Sep 2025 04:20:17 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json
