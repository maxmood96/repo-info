## `buildpack-deps:trixie`

```console
$ docker pull buildpack-deps@sha256:644dc894d9f9eccc72e5a91822a7a443be368d77936a8311278e5727ba6d1087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:trixie` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b8a3e8466cf7cb16fb41534824990837c3567d736574b5be4894a40713f93995
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.2 MB (407207425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:660c67ac59352e42df731c6b35275ad3e32375454b2758c799e83475c2f3a490`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:53:36 GMT
ADD file:99b2f09b38f37e8fb43da4af7e905a316ef0ae5d1372e182af7a4467ef8d7d73 in / 
# Wed, 10 Apr 2024 01:53:37 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:31:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 05:32:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 05:33:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9e95c2810bf71ea304ff068100fda778bbde84d0612d720b0cab3e6069e85fa0`  
		Last Modified: Wed, 10 Apr 2024 01:59:53 GMT  
		Size: 52.3 MB (52332312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b66a844a336d24bd3d65fb1c2fa52cd05dba564c7d3c1a7655648d2891df776`  
		Last Modified: Wed, 10 Apr 2024 05:39:03 GMT  
		Size: 24.2 MB (24160926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b614b95f18c1108db17cec7a97089473d2212ca808e2961450b05f7c8a9b8df4`  
		Last Modified: Wed, 10 Apr 2024 05:39:20 GMT  
		Size: 66.5 MB (66507194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671296c28cd479ab3548d565abb3c791aad56c962796b92cf9ee78571a095d3a`  
		Last Modified: Wed, 10 Apr 2024 05:40:00 GMT  
		Size: 264.2 MB (264206993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:3b6575b9402d51f3a03b2176db11553ee32ae6bd1b88368c9c534faa9fba631a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.4 MB (370391429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ecda2df711b961ebe559c0cb54ac4a96c4babb57f6110a1fed59bbc7520691d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:52:01 GMT
ADD file:0476c16083d61e234237e2ef7156b893d991ebc8124b8bc6710b73ef2fe671d0 in / 
# Wed, 10 Apr 2024 00:52:04 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:52:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 04:52:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 04:54:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5c8c28d868d5d3991cbf017b63d5fac41114aa7d2eac7b1224fcb86c76b143f4`  
		Last Modified: Wed, 10 Apr 2024 00:58:20 GMT  
		Size: 49.4 MB (49422136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3293a18c8b358e708c54799a531104a9ddde33e702e4608e103d0b33b15cb3a9`  
		Last Modified: Wed, 10 Apr 2024 04:58:50 GMT  
		Size: 23.0 MB (23041769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f2f7b0c3bd000167dd0d210fe7cfeb3c2d1dc31c6b0e387868179dfae14c44`  
		Last Modified: Wed, 10 Apr 2024 04:59:12 GMT  
		Size: 64.1 MB (64146624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced71e62ea7f0a370d9f25f14344a8e74098dc06090a6a2cd039fb4abf8e2ba2`  
		Last Modified: Wed, 10 Apr 2024 05:00:01 GMT  
		Size: 233.8 MB (233780900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:91755931238fed298b1844948375ac6f1fe6cbff9a81283520481a845acc190b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.8 MB (348844394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0afcafeaf1c1255a342fa5928e88d3b07ec02194205d568467066f25abac2b26`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:01:55 GMT
ADD file:656b365d8d9314f1217c95cc1d4d7cfb6bec38e30aea70bfb00983db7de41d64 in / 
# Wed, 10 Apr 2024 01:01:55 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:55:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 06:56:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 06:58:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a2733bd62bd4d649c9ab65374a55302ef287fbb5318c00121743e3223bf33e52`  
		Last Modified: Wed, 10 Apr 2024 01:09:16 GMT  
		Size: 46.9 MB (46920080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02643c0d13132e32e3d948fe0f9e603b1f3bc4e4dab635e89566aabcd733d1d4`  
		Last Modified: Wed, 10 Apr 2024 07:04:59 GMT  
		Size: 22.4 MB (22355167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf1919d5931d6716bea45e42bed91785de5a79886b5964c4c66b4d9c8a6032e2`  
		Last Modified: Wed, 10 Apr 2024 07:05:20 GMT  
		Size: 61.5 MB (61512870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5b3872cf16cb823cc1b2320f8bcc636226e7c28e36da659115f880b2547f04`  
		Last Modified: Wed, 10 Apr 2024 07:06:11 GMT  
		Size: 218.1 MB (218056277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c95ea4c7d22305fbf472831944c91528ef84af4918f47bbc693328f3232c8320
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.1 MB (395142626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3087be1a604bbceb81c34baca1d1ccf70b03d4f082c9e8a44a9355f926173b2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:42:14 GMT
ADD file:d3b8312bf9d9df431c2580a0add351c37786bf532e919d2af2638c2fb93062ff in / 
# Wed, 10 Apr 2024 00:42:15 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:29:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 04:29:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 04:30:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:782f2de9bf3353a68116b53b16ae9a2387174b31cc46b4c9b4cf99de0a6e1af4`  
		Last Modified: Wed, 10 Apr 2024 00:48:17 GMT  
		Size: 52.2 MB (52193812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ae77305c2bd54ea5f2ca2a76ab1cd96f744878b54d2b45e6edd47242bfa248`  
		Last Modified: Wed, 10 Apr 2024 04:35:41 GMT  
		Size: 23.9 MB (23879162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e30f8a1b424817119b09ab00860f59903c62298e404ea6d5a47596c436e9353`  
		Last Modified: Wed, 10 Apr 2024 04:35:56 GMT  
		Size: 66.6 MB (66613328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c48bff8f4af3dd20a85f1f4e98faebb5053af09f7a98bc9a9db8646faa76b6c`  
		Last Modified: Wed, 10 Apr 2024 04:36:29 GMT  
		Size: 252.5 MB (252456324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; 386

```console
$ docker pull buildpack-deps@sha256:796f0808ae2bf9115d8031b9df027652348125234769dbe6ca35d95a060dffa3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.7 MB (403696514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a1f540d5830dcc8f94eb59b89f50e93f88aad90571764fb5bdb8a08a40c03e8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:00:02 GMT
ADD file:abcf303260a61d60a322026090059894acd6d5974cf95cb5cb95fe741e8c848d in / 
# Wed, 10 Apr 2024 01:00:02 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 08:02:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 08:03:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 08:05:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b9c103e72d23fc0564cc4fad24e0b07faa513b25fa3de0abf18a1f87404c69e1`  
		Last Modified: Wed, 10 Apr 2024 01:07:16 GMT  
		Size: 53.2 MB (53185201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb37a62071dbdc2899d5951d1f2678198daf20ba94c1f7a6aba672426d57abf`  
		Last Modified: Wed, 10 Apr 2024 08:11:19 GMT  
		Size: 25.3 MB (25280044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae970712d2c71f79030573939e97a1829dd250a8a07f02e21ee728e259da55a4`  
		Last Modified: Wed, 10 Apr 2024 08:11:42 GMT  
		Size: 68.3 MB (68288024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b593050942e9409dc21c8831567abeaeba261f144b6725cc9f6f38c7d3dfd55`  
		Last Modified: Wed, 10 Apr 2024 08:12:41 GMT  
		Size: 256.9 MB (256943245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:f03e178c9abf4112b3462aca11b751002244d4290ceb7c13be55fc086d3cda06
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.1 MB (374054854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375690a33878b671637de5260b41fbf3653065bc084c04483f0c1aa4b3304065`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:57:26 GMT
ADD file:1d56c0518f96fbddc9f17bccae9409ff53346bec87d25d10c7fbe2282a4dffbe in / 
# Sat, 30 Mar 2024 20:57:32 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:37:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:38:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:45:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:31000c4b13782d0f1e2c555def998a165929c959d46324718bfb86e7b5258c7b`  
		Last Modified: Sat, 30 Mar 2024 21:03:24 GMT  
		Size: 51.4 MB (51410980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840e914144b7ecbd5ac22a02324f48082e178507504eaf966c25bf9c4c1255a5`  
		Last Modified: Sat, 30 Mar 2024 21:49:50 GMT  
		Size: 24.6 MB (24624661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e46a7c1596412850ec91cc8e73fb58f10bdabe00c3a3878e5c415760e1882c`  
		Last Modified: Sat, 30 Mar 2024 21:50:40 GMT  
		Size: 65.3 MB (65297807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab6e7309cbb19498b04d6ce239394888a75868da207aba050aad04cb90d117d3`  
		Last Modified: Sat, 30 Mar 2024 21:53:10 GMT  
		Size: 232.7 MB (232721406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:35562d8bf2d6cdf11b5d126781cd52fb3ffdc18dd83008e263202ab90e2d524b
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **417.9 MB (417938778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cd1e1ae07812b50b51314e325502083ffe731b0b9ae1c94dd3d50ee3d1fc124`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:28:55 GMT
ADD file:f2e3cbd5cfb4aff8ec6395d52d929fd664d9648429ab4d9e1153ee9f8459da76 in / 
# Wed, 10 Apr 2024 01:28:58 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:03:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 07:05:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 07:14:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c75969f9d1cfa02f8bb4ac9be57d10b36fc89340facd55e8f3ee886024860d42`  
		Last Modified: Wed, 10 Apr 2024 01:34:52 GMT  
		Size: 56.3 MB (56250111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c594ec063ba0274cc2cf2f1cfb2f564c330c348dec7ab928f2424a30b4f1bee`  
		Last Modified: Wed, 10 Apr 2024 07:20:14 GMT  
		Size: 26.3 MB (26256738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038140cbd597a5abde48b6e2e138b1f52f404b75dc59349b57feeff15b2c6e42`  
		Last Modified: Wed, 10 Apr 2024 07:20:35 GMT  
		Size: 72.0 MB (72001312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b17367194c5bc37cd324a2445540eb33d5dea1722a7c2bae6b5ca0854025cb8`  
		Last Modified: Wed, 10 Apr 2024 07:21:24 GMT  
		Size: 263.4 MB (263430617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0164f9923c8e6980319a1f3fe971d7556cb421bee8f773aa1054da81436ec778
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.4 MB (385389760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4cd473ada26aa0cfbf217556f029a89f9f42e0b572648f06d7b879bf4281eb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:38:00 GMT
ADD file:a05ac36ba0a9e12dfdf53ad56de60918b6f7f530f4b32b570bdbbce0a7bc514d in / 
# Wed, 10 Apr 2024 01:38:04 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:05:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 07:07:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 10 Apr 2024 07:10:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a7403c42a27ad5d5ea9a8c3224d14c269f7cb3da9339e45b20c533dcbe911289`  
		Last Modified: Wed, 10 Apr 2024 01:50:55 GMT  
		Size: 51.8 MB (51761790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c24ff3eb07a21f2639bb7d99f5c6a035571ca068e5457d79f063f14100f020`  
		Last Modified: Wed, 10 Apr 2024 07:33:51 GMT  
		Size: 25.3 MB (25297536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ec7f7c2fddd776232182d05cb2a896283dac486022dfe898eacb7640fe1e5c`  
		Last Modified: Wed, 10 Apr 2024 07:34:07 GMT  
		Size: 67.6 MB (67588152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f17a89cc72e722c317692c022172c8734c5d6ef10cdfcc45eef7f32c2687073`  
		Last Modified: Wed, 10 Apr 2024 07:34:45 GMT  
		Size: 240.7 MB (240742282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
