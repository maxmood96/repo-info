## `buildpack-deps:jammy`

```console
$ docker pull buildpack-deps@sha256:a4e19d272f6e3807cce8b241120de265a3c09209e73614c3c50477a689e72b83
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
$ docker pull buildpack-deps@sha256:78326e4aaff44bc8a6aadb81f88304e4f0c74f420c716c2b3d26a7653abe2280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.1 MB (249058461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff921f821bdde4052e0510bc815681258b7b2eccd9e98d5014ee0b2df537abd`
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
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4340d07249a0b63b75c4a83ce1639f4f99213cb0868bed6fe3ee40cc7d6ba08d`  
		Last Modified: Wed, 09 Apr 2025 01:11:28 GMT  
		Size: 7.1 MB (7102787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5adc8f2734bf52dafa222e8dd003ab8b181bb0d921af2f753577e4bd1fcd6cef`  
		Last Modified: Wed, 09 Apr 2025 02:12:01 GMT  
		Size: 39.5 MB (39485582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5686083e8cc26971a90e9f3fc5d6c936390d5c4dbc33159b4f77c0d062760315`  
		Last Modified: Wed, 09 Apr 2025 03:11:42 GMT  
		Size: 172.9 MB (172937727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:861bf565acde68aa56ded4e3c6964100a1b65de637267656154c0bafa415346c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11465805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b88287b4b6b4fb204c0a1c4c5637672e63e3a313b6f7161b39dadf911bbce98`

```dockerfile
```

-	Layers:
	-	`sha256:4c0c3e5e15402ab5be3df2ad75424214cc6615910c3e89525fb16f5c96ab8f56`  
		Last Modified: Wed, 09 Apr 2025 03:11:39 GMT  
		Size: 11.5 MB (11455602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47b4c0f93d8aab7cb3dbf57b734dfc498e0858992f54903ab7aae2b12ab0bd3c`  
		Last Modified: Wed, 09 Apr 2025 03:11:39 GMT  
		Size: 10.2 KB (10203 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1ab6ea25e47b92ba56334d4d88785b85c9c7c4920dfcceaae6c6c4f2dd96e6b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.3 MB (216259776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d75757b616421fe998ea6154f45ee03d1fedf40c8d8bec8fab4ad0c3e014616`
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
ADD file:7e9e4d557a66a31de2a39930803dbe849ba710af36b4731e9cbc856f55c10018 in / 
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
	-	`sha256:eeaefd3c974dfe1d5e1b8eb1929496ae7befe434399b37e601701f6d012e3169`  
		Last Modified: Sun, 26 Jan 2025 07:02:14 GMT  
		Size: 26.6 MB (26639267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03a59df32a3c278c1a8e1b5a42ec5159ca064a182a7ceee73e4ebe1d86afa12`  
		Last Modified: Tue, 04 Feb 2025 10:44:17 GMT  
		Size: 7.0 MB (6998537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29d430e6e7df77b4a0c661b16f2f8366b006b35a623d472b34c14652775512b`  
		Last Modified: Tue, 04 Feb 2025 16:24:21 GMT  
		Size: 42.2 MB (42245704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8a5b769f2858f3c9c92b1bebd402e5050d772902feea65f509d8322e61561a`  
		Last Modified: Wed, 05 Feb 2025 00:27:00 GMT  
		Size: 140.4 MB (140376268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1a6f52f789365c20cb22e121b7b1547d94662674539b57c204eb99664576f596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11253785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82d593b500440c771b0650178b3993afb4ddfbdfa09cea837cf91cfbeab5236`

```dockerfile
```

-	Layers:
	-	`sha256:3a5ba0d6141552b1e5b70b2a8eb936a49aa0721fe6e28340c81936e99eee52d4`  
		Last Modified: Wed, 05 Feb 2025 00:26:56 GMT  
		Size: 11.2 MB (11243522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8f31378a702a68608b969b8ab62d6450ca4b2c4351b189abf5a71cb513317dc`  
		Last Modified: Wed, 05 Feb 2025 00:26:56 GMT  
		Size: 10.3 KB (10263 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e80364c830ad95278347c8f4d9b03eda340253fb61003585262e4db454f512c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 MB (240167314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad9178ccc6922cfa0e2b5a39c1ad54162eaa72ee083101588a56994caacd256`
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
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9c1e987316bb6701bafa74dadea41ea57299699f23daacaaeafa9fa05f6213`  
		Last Modified: Tue, 04 Feb 2025 09:02:41 GMT  
		Size: 7.0 MB (7040539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4d40d9b4a2a385703a53f399708272fe0719e35d402c2b48c88c4f929e5ab9`  
		Last Modified: Tue, 04 Feb 2025 19:04:54 GMT  
		Size: 39.4 MB (39385427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f73acf919c33e789d58ca954a2e8e505bfeb7d90b056407f3e22d9a575ebecb`  
		Last Modified: Wed, 05 Feb 2025 01:48:18 GMT  
		Size: 166.4 MB (166383166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0e28f7f9c2786cece1ad09cb435abaaa83af6750e82ced937f074a5c52235784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.5 MB (11458799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dceaca68448b951ed46ae104ce224a1bd6832758698e65106ac08dab05312736`

```dockerfile
```

-	Layers:
	-	`sha256:a309fcc1c1bab4a29960c1df2fccdb653da90b3340d2571cc79f352c64c279a2`  
		Last Modified: Wed, 05 Feb 2025 01:48:14 GMT  
		Size: 11.4 MB (11448516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52d6f1903f7f3392b61e85403b9d4c434688243b75a70dd66ba023e3a2f44813`  
		Last Modified: Wed, 05 Feb 2025 01:48:13 GMT  
		Size: 10.3 KB (10283 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:32b22c465b77e20ce0fb27563dbf046a85bfebcd95c474dc525f955a0d25ee5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269852029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42fdd060a753749b830d8da2f28351962b868d7ac52915a219507135370e842b`
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
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
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
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Sun, 26 Jan 2025 07:02:20 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c3f11d98bfde7b2d484e86a27f312061b41c7e65028517cbad025bac990450`  
		Last Modified: Tue, 04 Feb 2025 07:27:33 GMT  
		Size: 8.2 MB (8197665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e478e008c5d6761fb7b668913245a2e7b1eb03ac82bfd5b3dca2c5c60cacb60e`  
		Last Modified: Tue, 04 Feb 2025 15:51:13 GMT  
		Size: 43.8 MB (43767140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717d1e64daae9af00ac476d8868c2f4fd4b1a08416613854d552cf428e50eee9`  
		Last Modified: Tue, 04 Feb 2025 22:10:12 GMT  
		Size: 183.4 MB (183439289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:778f2d26b1dad3865ae4b60349971bbb30a075af843b79dcad5fbca3e408178e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11421897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdbb1142ecae3913368d399ffbd346fb3cddf116bf9250a7fb850637f67e424f`

```dockerfile
```

-	Layers:
	-	`sha256:6951c6ed85d33e657cdcf735a336099a26d2a04f5a2614a8f6b941bb38e3bc38`  
		Last Modified: Tue, 04 Feb 2025 22:10:06 GMT  
		Size: 11.4 MB (11411662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:712ebce541bb9c7f6c81c8d4d5c35d50f07cff6f095d673163a2d73d5b29c907`  
		Last Modified: Tue, 04 Feb 2025 22:10:06 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:cb005a903174af55be4fd9061bf76c495b4e36e10b7086806532cb43c95dde2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274231046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90f0b33982a82b2568cb04a4cfd62ae71d860a15bfc21a21e67fba19170c92d`
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
ADD file:c95ac39f820c01b1c0a2d18f3df09346a389f9989c91cb636f75de0e3d63c97d in / 
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
	-	`sha256:cfa2d73aa16649863373431bec34ae49863b8b03f19e2c1fa29af96b0ea254fc`  
		Last Modified: Sun, 26 Jan 2025 07:02:26 GMT  
		Size: 27.0 MB (27039007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247fcfe5b002f706b4c9b3a78341f202606a547ef405c7ad03e2e33f28fec027`  
		Last Modified: Tue, 04 Feb 2025 04:44:46 GMT  
		Size: 7.1 MB (7108060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb811904a9072aa1e8962df9982276480172376fb423cfcf8aaec3ebb4f9f8ca`  
		Last Modified: Tue, 04 Feb 2025 08:14:03 GMT  
		Size: 42.3 MB (42307263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70089f8fa6e86f416dcc916a3a84e0eb779463cd666ed04f5784d45aa423ea9`  
		Last Modified: Tue, 04 Feb 2025 10:06:46 GMT  
		Size: 197.8 MB (197776716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5d87b26854a76501137f25370979c3cedeea170eb08484a6de7863cc3ab793ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11404981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d611b10a561d0c1c1e91fca1cb463bd6a7438a1f550263f51f55fe5fa896893`

```dockerfile
```

-	Layers:
	-	`sha256:3989dddbb46fe2b99dc6e1c31bf8f63b02f6d180ab5b721f4266b7fba5596421`  
		Last Modified: Tue, 04 Feb 2025 10:06:19 GMT  
		Size: 11.4 MB (11394746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ace35bc54c917e2c6c94ff6c186d49d7dec0aec2f43deb0dd7110a21c813e6aa`  
		Last Modified: Tue, 04 Feb 2025 10:06:18 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:jammy` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:fef28f592e99044ac6763bf379baf76fcbe3b2ee1e14117f3b80ad5b935cbac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (223015469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4112aa77e1ca6f6d3da64d71a633cf5130367c31c03ad77cd4bb7294c6f460f0`
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
ADD file:39a6583c8b71c00e0ea7562cadb2b343caf5c0c274178520c7476e53faed2e3e in / 
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
	-	`sha256:7ed94a91c4e77c2e320a028b45fcefc9419c4df2b3d6494bf92ab5d08bba4d77`  
		Last Modified: Sun, 26 Jan 2025 07:02:32 GMT  
		Size: 28.0 MB (28000931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e0e0eba9503675f1ef20409d7abb0dc538cffb5361ed38070285248d79ca72`  
		Last Modified: Tue, 04 Feb 2025 07:33:18 GMT  
		Size: 7.0 MB (7007841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ceb4257b5f6dbcfe0b6e240c36bcdefe3066bed00810364bb9111fc2b142678`  
		Last Modified: Tue, 04 Feb 2025 11:41:04 GMT  
		Size: 39.4 MB (39420962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa0ab42cb859c05596b8815e66eeb4181beaed4725a822c23f7710f7be4af17`  
		Last Modified: Tue, 04 Feb 2025 18:05:33 GMT  
		Size: 148.6 MB (148585735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:jammy` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1de8d52a7207938dce8abc27416cf51749398bde1e88a088c1511bf7fc5d4ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11278102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52724580e895bddc4fce04f9cc60e1a90b760b444d0f769617828875caa6c564`

```dockerfile
```

-	Layers:
	-	`sha256:461c25ca01ed5ec06f9ed051716add0c1d94406139c325d27e784e74a2b5ca46`  
		Last Modified: Tue, 04 Feb 2025 18:05:32 GMT  
		Size: 11.3 MB (11267900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fecfee8395d8cb0f40aa5c068e1e731b36d366dedddb3e404df01f5b0c1749df`  
		Last Modified: Tue, 04 Feb 2025 18:05:31 GMT  
		Size: 10.2 KB (10202 bytes)  
		MIME: application/vnd.in-toto+json
