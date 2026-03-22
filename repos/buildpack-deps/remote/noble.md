## `buildpack-deps:noble`

```console
$ docker pull buildpack-deps@sha256:48ed546e0c73411684342c477714cefb8e4ea5a9c506e4a17f602807c048aa54
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

### `buildpack-deps:noble` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:91ff78b9c352f3af24c9c2deb34544d6b07e9d6f5702fafe00fb36f44c61d9f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.4 MB (276405845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d89b18d9f0ed2f02959dc39db9d915894409f7bd61c6dba7e4d64dc882d9385`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:17:53 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:17:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:17:53 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:17:55 GMT
ADD file:3f78aa860931e0853077f09eb31eddbeeef8a9dd70977305b4876aa176770721 in / 
# Mon, 23 Feb 2026 17:17:56 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 02:32:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 03:19:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:817807f3c64e0b90b66edc7d90297f121cad2a7c2a3ee05a731557762f91e6c7`  
		Last Modified: Mon, 23 Feb 2026 17:51:17 GMT  
		Size: 29.7 MB (29731993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37893ef229d11c7b2e7f03e7e2fe577a02b63a79031bbac07a7ef958651051e`  
		Last Modified: Tue, 17 Mar 2026 01:15:32 GMT  
		Size: 13.6 MB (13631007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f5f092312887fc74115ed763ec50c8a9676eea7165abef3d8c52c483477c498`  
		Last Modified: Tue, 17 Mar 2026 02:32:58 GMT  
		Size: 45.3 MB (45336180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b408e304f4d647001ae4e98364eceb8bf6b931aea9b64d51d91e2ea9314769c`  
		Last Modified: Tue, 17 Mar 2026 03:19:59 GMT  
		Size: 187.7 MB (187706665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d8561873211e7dae0be2f24d771a4678505e19e50b880927c8b3cd34ff7482b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 MB (11743881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b0d79ebbdd871c09065aace92781d5c8999e138d6101329ed4e7ef30cd2ef3`

```dockerfile
```

-	Layers:
	-	`sha256:a19ecc3f081f6a1692b18ee55ffaa385ae9efc124e770442733e27da17ab3d79`  
		Last Modified: Tue, 17 Mar 2026 03:19:56 GMT  
		Size: 11.7 MB (11733741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7d8013628b98a1ca773db05d89875b730e292c97140dfded47aa3786efed713`  
		Last Modified: Tue, 17 Mar 2026 03:19:55 GMT  
		Size: 10.1 KB (10140 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a8df42238bbbc35f47443b9a2bc0bba728e509c57c062b860bc96234ba2ec2a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.5 MB (239544706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c5e290a885ecd2ff2d96fef3e02be29f93d114b010dd2d440cb39603c4de737`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:10 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:10 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:14 GMT
ADD file:834191023ea63b612bd409fecc858bd572114f2ce02aca5944385eae5eaf48f8 in / 
# Mon, 23 Feb 2026 17:19:14 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 02:17:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 03:17:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:51c4cbb22341ed2a12c82974973354e1be3db5c9041bb5fbe2640ced2f41020b`  
		Last Modified: Mon, 23 Feb 2026 17:51:31 GMT  
		Size: 26.9 MB (26859311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c79a21860b786c32e6868f43825286a9abe5aeca43531e53711cc81e1b02114`  
		Last Modified: Tue, 17 Mar 2026 01:15:19 GMT  
		Size: 12.8 MB (12788360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97af8802c5f7f09371fc7d46d1c29451aab79808257053014c546c491fe31242`  
		Last Modified: Tue, 17 Mar 2026 02:17:59 GMT  
		Size: 48.9 MB (48907500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45bed9ee973c3308f57bea6ac4d1d0f22491f2171b1e69ad86e9cb8264ec4ca`  
		Last Modified: Tue, 17 Mar 2026 03:18:24 GMT  
		Size: 151.0 MB (150989535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f730d1f89bf96a5966e4678db0aa916101ea418944c709bc50fe6cbce49f276e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11069627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7895e7c6ca58d196bb474513a67cbe4b054a179025a1070da224c92510d9e506`

```dockerfile
```

-	Layers:
	-	`sha256:da847aa5b301313a249ad8501dc29dc21597d8699d8f0c9a9d8f9f5cf300aa13`  
		Last Modified: Tue, 17 Mar 2026 03:18:21 GMT  
		Size: 11.1 MB (11059422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f07151ed8d0a993ac5d366399b5b2f65971abe8ebcbb827159e15578c68eafe9`  
		Last Modified: Tue, 17 Mar 2026 03:18:21 GMT  
		Size: 10.2 KB (10205 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:84b675c573a88fa171cad6e110b91870fd31a54e782e90d5d30ccf3b198dd3ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.0 MB (265995296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f4702a231981b721fda5ec9f98cd27cfd7dabb8f0936f78987d6787f434329`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:30 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:30 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:32 GMT
ADD file:2763d61bc43bd178306ae0d4151c2477166ebf199b8d7294d9ea410f9891993f in / 
# Mon, 23 Feb 2026 17:19:33 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:15:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 02:37:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 03:22:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:86790fc5660dcd86928b849ae0826aba701bf9e005e92c8f9e06c917e82c87f7`  
		Last Modified: Mon, 23 Feb 2026 17:51:24 GMT  
		Size: 28.9 MB (28869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c14c4233e7d75a38c201e9c5e7f07020dd6f8701769cbea2931551396595d3`  
		Last Modified: Tue, 17 Mar 2026 01:15:34 GMT  
		Size: 13.5 MB (13465941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffdfd4da2f901c5f0f5392f2a35c2f7cb79cb724fb15ffe1bfee62ff01588c6a`  
		Last Modified: Tue, 17 Mar 2026 02:37:21 GMT  
		Size: 45.3 MB (45307716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800500561c0380a53c04ba4ee474599d2aabf7be72a1b92dc65f6cf87750da20`  
		Last Modified: Tue, 17 Mar 2026 03:23:16 GMT  
		Size: 178.4 MB (178351930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:100451c7688657f7107d6db96af458c7e74204b33652518d74f7fc89d485a333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11293426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:763f941fbadd9ebfb63967628848acd0e57d08cdaf930e42673eea1602f85396`

```dockerfile
```

-	Layers:
	-	`sha256:1ebde25b4e7b80e345a1a02cec3e05c0efce7d82d495e77d3901d513531a7c4c`  
		Last Modified: Tue, 17 Mar 2026 03:23:12 GMT  
		Size: 11.3 MB (11283206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a313f9c9ac4c7db1392d5caea6b95d3a84ef6a4b98ce3ec6e21f957ddfd45834`  
		Last Modified: Tue, 17 Mar 2026 03:23:12 GMT  
		Size: 10.2 KB (10220 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:19c9847832a4058b47a7058c28e6d659a1c3fcbe02f9e295d1b49b3da9f8a327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.3 MB (292284587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:553a2b1d87f17cdb3a31b09e6fa9b465c8284c82d29f93ac3569b0cd3a38cf9f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:18:33 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:18:33 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:18:33 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:18:36 GMT
ADD file:2a89eb67bf550d9680999e3ff99dbaa17c251b6c343a241318e879a26da53fca in / 
# Mon, 23 Feb 2026 17:18:37 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 08:27:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 10:22:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 19:06:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f826c9b754a00ada9d9335ffdf3ffd40f6925a3223caac76cc429823b8621f9e`  
		Last Modified: Mon, 23 Feb 2026 17:51:39 GMT  
		Size: 34.3 MB (34310051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:702e63789dae837b8ef69e9f3d52d1fbec8927249cb62a287e89540342d490b8`  
		Last Modified: Tue, 17 Mar 2026 08:27:28 GMT  
		Size: 16.0 MB (15960269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51b69caffa9101ab3bf44986f0ada13c1cd07b65ab1ad0fa97b3b9a46ec4ff7`  
		Last Modified: Tue, 17 Mar 2026 10:22:37 GMT  
		Size: 50.4 MB (50381420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addbc554a0ff8a500de4f7ec17e77036f48944ebff9451e4b6015f8512890cd1`  
		Last Modified: Tue, 17 Mar 2026 19:08:05 GMT  
		Size: 191.6 MB (191632847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ccc8c2301c2cc7813a01e34dcfc97c2171d630bd82c1040b98ed49570e89c339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11240816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a293eb84197fd0dccff8005c8edb00c7abf6a4c180130663978dc98e84fe7bf`

```dockerfile
```

-	Layers:
	-	`sha256:7428ce62c10802fb4c0e8e674d145ef7f0894bde9d8a0ffe7464310878ab7b58`  
		Last Modified: Tue, 17 Mar 2026 19:08:01 GMT  
		Size: 11.2 MB (11230643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46f6584e7045536af837f2056d4d7415118619d0e8eac0a81571944600158dfd`  
		Last Modified: Tue, 17 Mar 2026 19:07:59 GMT  
		Size: 10.2 KB (10173 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:0fe37e467092b07c93cac9f4c41be0dada2577b773fc89df439b21c9704dd967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334307874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a32eeba6f53349e9ea9314451d52c752484dcf66b826f6fa120f30e62062bea7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:42:34 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:42:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:42:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:42:35 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:43:25 GMT
ADD file:1243b7db425cac690d91f87ad37c1beec0d95da6b3942dc8084039fe1cc2baf4 in / 
# Mon, 23 Feb 2026 17:43:30 GMT
CMD ["/bin/bash"]
# Sat, 21 Mar 2026 03:06:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Sat, 21 Mar 2026 15:10:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sun, 22 Mar 2026 20:26:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:866473980fd7aa6ac5a8a995315a35248ab945008a1938bd15f65082df53b2d3`  
		Last Modified: Mon, 23 Feb 2026 17:51:46 GMT  
		Size: 31.0 MB (30960145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee039942c223db7740f8c7ddba0be9d66f5b268eae6ff09af10e8dfe9568a44b`  
		Last Modified: Sat, 21 Mar 2026 03:07:14 GMT  
		Size: 14.3 MB (14336878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6420cc7f2b4e190b613ce207f09a81d634f7dfb443cfdc6a5a9f44997ee2ac9`  
		Last Modified: Sat, 21 Mar 2026 15:13:41 GMT  
		Size: 53.9 MB (53885269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25ed3578ec185ca92a1884ded7c073ecca81a9af2351588bc6271c7d5231296d`  
		Last Modified: Sun, 22 Mar 2026 20:37:26 GMT  
		Size: 235.1 MB (235125582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:af649f66d308ceff5611ed5aacd1741c2d67ac7f33c6296502376957afe1a5eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11234059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4742a94814e8f69abe21b09c2e60a81382ca9335a28fd1e07573b2d9df998249`

```dockerfile
```

-	Layers:
	-	`sha256:27f94493c8577d9bfef75a298b1291a8d65e037410b08b1a6748da9a74bc91e6`  
		Last Modified: Sun, 22 Mar 2026 20:36:53 GMT  
		Size: 11.2 MB (11223886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da369bd62842445920039a8c417761fe577d7e35278eff47550360f98a4e1778`  
		Last Modified: Sun, 22 Mar 2026 20:36:49 GMT  
		Size: 10.2 KB (10173 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:noble` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:fa6c30f71b55b01df27c4b948f020c47a72a06c626611315c58f769322ee5e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.8 MB (254776593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b3a6a3d31810804e3cb8e9fddeaea79e3b007b357af0619dcd742ca649fca6a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 23 Feb 2026 17:19:45 GMT
ARG RELEASE
# Mon, 23 Feb 2026 17:19:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 23 Feb 2026 17:19:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 23 Feb 2026 17:19:45 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 23 Feb 2026 17:19:46 GMT
ADD file:36da4c002083f47f3a54f9afaf09c1e01e856a8f55618e96eb26304b47eb72b6 in / 
# Mon, 23 Feb 2026 17:19:46 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:19:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 03:21:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 11:59:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:07785e1e3448bfcdd4a7c917fe2208c68391368db6b314a3bd60d0c083944c3b`  
		Last Modified: Mon, 23 Feb 2026 17:51:53 GMT  
		Size: 29.9 MB (29910381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:523f4e88b5222cb75f891e4de8500caa034cde5357f00050756cb250567a9997`  
		Last Modified: Tue, 17 Mar 2026 02:20:10 GMT  
		Size: 14.9 MB (14943132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a76719612dbd6842ab8a9594278243b164c7f4827d6634eddb5c7614791ea1f`  
		Last Modified: Tue, 17 Mar 2026 03:22:52 GMT  
		Size: 46.8 MB (46762058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014bc17eca9c9e568c9f27014cdb9eea2c95481f33bf71855c84948eac5a89cd`  
		Last Modified: Tue, 17 Mar 2026 12:00:31 GMT  
		Size: 163.2 MB (163161022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:noble` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0231766016668cb903c58fdd7c1fb0e64619b8bce174ccab5be5a8a18fda6832
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.1 MB (11084619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cff15ff9390d11b93bddfd1b9953ae4b4eba15da39d3beba19f3a51a780805d7`

```dockerfile
```

-	Layers:
	-	`sha256:0d30949fa7bce78ffc360b6e55053bedded5ee9a44a3641f12bcb3d0cd9e4639`  
		Last Modified: Tue, 17 Mar 2026 12:00:27 GMT  
		Size: 11.1 MB (11074478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0713dfb13d9a42c4195ce5cb5bf0866498826b2cf79888e42168b87823a9fa03`  
		Last Modified: Tue, 17 Mar 2026 12:00:26 GMT  
		Size: 10.1 KB (10141 bytes)  
		MIME: application/vnd.in-toto+json
