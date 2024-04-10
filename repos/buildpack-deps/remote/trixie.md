## `buildpack-deps:trixie`

```console
$ docker pull buildpack-deps@sha256:3a64a1489f1756df5e53d7c403fc23a8073551e82cb5c16237a7183becfc12a7
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
$ docker pull buildpack-deps@sha256:fe328d3acf2b3a1a04177df6e3646804a9c723702f41246f2c2fa94c7e6b251f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.8 MB (348835489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e28be6a8566ffe770a5445f44f18fb23f396f27b864c9026e51f6e931967929`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:53:21 GMT
ADD file:9990a7eaf964c91061a89c6f3c73bd2cf46fceceeb29631f82793bfb0fa7b946 in / 
# Sat, 30 Mar 2024 20:53:22 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:27:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:27:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:29:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:63216cf879d84931e7e67b6b738c215b8c22e457696bae63761b1b497d2c425f`  
		Last Modified: Sat, 30 Mar 2024 20:55:51 GMT  
		Size: 46.9 MB (46920458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bad76f6b11a78bc1657e0bbaf9989e755e9ed77d96a034e6db10b4491bb36a1`  
		Last Modified: Sat, 30 Mar 2024 21:31:35 GMT  
		Size: 22.4 MB (22355117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9c6e3e6ce96fb41f02f466b843d37cc564ba933de9a8c733b54cc9095a60c0`  
		Last Modified: Sat, 30 Mar 2024 21:31:53 GMT  
		Size: 61.5 MB (61505430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0848461b9b4785f45b667a3db634a643e594beab111e48a523e8e61699cf6d4`  
		Last Modified: Sat, 30 Mar 2024 21:32:30 GMT  
		Size: 218.1 MB (218054484 bytes)  
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
$ docker pull buildpack-deps@sha256:b2ad1b73972958501ce343e89c50cce82100bae16b76b6bc5ef5b1aff64a0b7b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.7 MB (403686311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a34d9f9875407c704830efd5253be522bdd79b77702e7fc776a1574f903e74d5`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:34 GMT
ADD file:dfc91743f00a1945b1f5adea0e11cd7014a494abff4f925fdec2d862590827fd in / 
# Sat, 30 Mar 2024 20:52:35 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:18:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:18:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:20:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5662ce26ec5ad23a19169ca47537638540e5da52821348b3b694502e8edef442`  
		Last Modified: Sat, 30 Mar 2024 20:55:37 GMT  
		Size: 53.2 MB (53184906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30679de5af79fc6eb953c23c9c35823675bcc6b2fd1fbee826536c5a7efa9d13`  
		Last Modified: Sat, 30 Mar 2024 21:22:54 GMT  
		Size: 25.3 MB (25279496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:346270e2a64ccc1d66f8b93818a9e57da01a691477de26749204ec49a036134e`  
		Last Modified: Sat, 30 Mar 2024 21:23:18 GMT  
		Size: 68.3 MB (68287345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e313f7d227590d173c7c917355cd9f941004d00a942880bbeb46db2d83afb99a`  
		Last Modified: Sat, 30 Mar 2024 21:24:18 GMT  
		Size: 256.9 MB (256934564 bytes)  
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
$ docker pull buildpack-deps@sha256:b6a4bafac2ba0b871a1f18bbb27dddfb9a0a953676d504d3fb63ebfe71fb018e
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **417.9 MB (417935469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2c74e473a6533b08cb81ca0078daf0be3d6bc8863752d6f85ce9fa2a46466c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:56:03 GMT
ADD file:7282f67fe7f663b8a0f5cf3616a170dcc53fdf139337c4f21bed996a3d0775c4 in / 
# Sat, 30 Mar 2024 20:56:05 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:39:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:40:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 21:44:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:45e42c51a4ddac2a4311bf4b5a8705633c437e10f1b8c91c4593d340ba0962d2`  
		Last Modified: Sat, 30 Mar 2024 20:58:51 GMT  
		Size: 56.2 MB (56249503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9e1c5aaf7d7ea5f4be8203b9bdbcb7b16c1d880f525979ca2c5fa0892bc1a3`  
		Last Modified: Sat, 30 Mar 2024 21:46:39 GMT  
		Size: 26.3 MB (26256388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b28cc0d4e61b8cd8c7b7e7f0f32f02fdf18eeb78863a40518a35ae1fa157877`  
		Last Modified: Sat, 30 Mar 2024 21:46:59 GMT  
		Size: 72.0 MB (71999507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2009a081181198024762b32de41b803175d353b112711a89807dd88ce6533ffd`  
		Last Modified: Sat, 30 Mar 2024 21:47:47 GMT  
		Size: 263.4 MB (263430071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c8ce9d22b81b531b84fcd0053c1764223025ee0237517271d259d5cc0b334754
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.4 MB (385391050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0557450db20d19e4286d71e7df5a0cbcbcd96ed024ed60dbab7ec653d2c8d0bf`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 21:19:34 GMT
ADD file:83a8ad7df79b8a9b94bcc30a6b1144e147cf3cd3cd59b8f74b8de0fd6102578f in / 
# Sat, 30 Mar 2024 21:19:36 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 23:47:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 23:48:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Sat, 30 Mar 2024 23:50:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c3fd712eb18d2c039779f2db381d96fa2525319b2d94f6db360102c06fc56a06`  
		Last Modified: Sat, 30 Mar 2024 21:29:16 GMT  
		Size: 51.8 MB (51761704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5c9531fcca2758fb32cb7137e7be8468b4be74cb60df515b4f984a0d5190b0`  
		Last Modified: Sun, 31 Mar 2024 00:09:05 GMT  
		Size: 25.3 MB (25297306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd869558e192852f59615a3c48ccbd98eb100935a473d9f83c786dfc340d8877`  
		Last Modified: Sun, 31 Mar 2024 00:09:19 GMT  
		Size: 67.6 MB (67586886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac5abf6bb25592cd6dcd1e039eb244572ed2262313de81026bd18e4ea9078e6`  
		Last Modified: Sun, 31 Mar 2024 00:09:54 GMT  
		Size: 240.7 MB (240745154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
