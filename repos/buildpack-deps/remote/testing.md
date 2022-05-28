## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:fafb61b62857e39f525d9e77e18f4b048fcf95ab6e771f0a47dcec7ec653a1e7
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

### `buildpack-deps:testing` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9b4c5be6792e96fde23c8749d70d5f8d5f8c74a92ec7d269bc6aa1ec94e0884f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.9 MB (335919542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2509e2248cd184f434ffe4450deb6c18048e63e0f1decda139e3481256701c14`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:19:50 GMT
ADD file:05d40d360d088a73d2d9ea8361742b3b0e7f5ac80923374f84acf3d1be6c7798 in / 
# Sat, 28 May 2022 01:19:52 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:39:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:39:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 02:39:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:40:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1afe78e67a22dc5c619d5518a1d45e8f5ca31628fa6b7caa3b645c4fba19faaa`  
		Last Modified: Sat, 28 May 2022 01:24:12 GMT  
		Size: 52.9 MB (52947713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a14d423114bf1291f01f267de6950924fd08d5221af6a2165d1f4201c7bf04`  
		Last Modified: Sat, 28 May 2022 02:48:03 GMT  
		Size: 8.0 MB (7999256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485b5a45d253cd5d3bdc472baa541897f0b1cdd23ca5be5de99b1a0191168b34`  
		Last Modified: Sat, 28 May 2022 02:48:03 GMT  
		Size: 11.3 MB (11264637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382e92fdb71925d6bd27ce2b56e500157d771af41de9acecd3517fb9e466c750`  
		Last Modified: Sat, 28 May 2022 02:48:21 GMT  
		Size: 57.6 MB (57585777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0744b12fb3f81fc9141414bb1a3a91f0a07482002cf9af86439a79360222a1be`  
		Last Modified: Sat, 28 May 2022 02:48:57 GMT  
		Size: 206.1 MB (206122159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:6e739743d1a206b4ed39725e6aa9067c5b6c2b271e9974ae55fd40a7dd1cc968
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.6 MB (306599333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942f65374532665d4f801d762521f85ed12fe95379b553724d6d131622d08d27`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:49:02 GMT
ADD file:14b16b308b28ed8604a9f98d47e92522f709988224084eb5d2dfd30d3511e4a4 in / 
# Wed, 11 May 2022 00:49:03 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:01:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:01:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 02:02:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:05:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0baf2800ae4e68af843862199b558f14eac2766cea5651c0837cbd8ee827981f`  
		Last Modified: Wed, 11 May 2022 01:03:42 GMT  
		Size: 50.7 MB (50737437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1cacfec2c73325f6ee9727f3ee99a764a10620c61e467c786773e82fac2589`  
		Last Modified: Wed, 11 May 2022 02:26:52 GMT  
		Size: 7.5 MB (7536108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9a878bece2839158834198a327d030c397685382713b32bee43b9de34889dc`  
		Last Modified: Wed, 11 May 2022 02:26:52 GMT  
		Size: 10.9 MB (10927476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222936f7ad04c2a63502712adf47f0d5e8415536d3b0815b84016fc8a214d3bc`  
		Last Modified: Wed, 11 May 2022 02:27:43 GMT  
		Size: 55.2 MB (55173746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e6bfd8430c731df5f5e74b96e86f72bed8ce3f757d400f59154c64d456507f`  
		Last Modified: Wed, 11 May 2022 02:29:46 GMT  
		Size: 182.2 MB (182224566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a344cdde065ae2aa0c12074e8c2d7c3a7ee9be98e4392bb33d901311f0e86e4d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.0 MB (293974582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9665e902c9e1f81bf9cc68189d21f382108b9199fe532b11eb3b7cedd032f17e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:47:29 GMT
ADD file:ae0b1a579333a3c7912430243fe91f71f32d0e234d52667dd937f7cd23a8d3d2 in / 
# Wed, 11 May 2022 01:47:30 GMT
CMD ["bash"]
# Wed, 11 May 2022 03:18:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 03:18:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 03:19:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 03:21:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1fdc9e441250146f7b7c78b0264138dc69a0b46d264373157ac1c2cdba7a552d`  
		Last Modified: Wed, 11 May 2022 02:02:37 GMT  
		Size: 48.5 MB (48475916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb8d2e8ff6478f1fc3388064baa5d6e059276c7a093a627bc6dc36d79ed4107`  
		Last Modified: Wed, 11 May 2022 03:43:50 GMT  
		Size: 7.3 MB (7269457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864281f702c002b286df6a1ef302fe0c7cde6323a4e78ec43b18718d930be2b8`  
		Last Modified: Wed, 11 May 2022 03:43:51 GMT  
		Size: 10.9 MB (10933463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f541bea22fba3f321a2207e36d3b3f6d26f89a61dabbd9a1305ed9b9938b15f`  
		Last Modified: Wed, 11 May 2022 03:44:37 GMT  
		Size: 53.2 MB (53179745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15f3636c3b2d37b4f8c5433d7bb4f6c441925e423935c03e91cc58399d6b5d0`  
		Last Modified: Wed, 11 May 2022 03:46:25 GMT  
		Size: 174.1 MB (174116001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f7d38375ad352e7f068fb2169e2264bd2d7f8ab47725e0f72dc88f6eaad33666
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.4 MB (328408240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8bdac2a6d8bcc3f2ba59b99497c5fe61ad61fff418f77cca86775d9e0d8c6da`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:46:19 GMT
ADD file:a50b6ecf9ed84e6e3bb43f96fd036c7ebaad7f94df16c3637d6dd19a6dc91701 in / 
# Wed, 11 May 2022 00:46:20 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:23:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:23:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 01:24:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:25:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:45306f5029ed7ce5685e65dccfaecf3f4a79040520f3ffb65eac76781218fea1`  
		Last Modified: Wed, 11 May 2022 00:52:36 GMT  
		Size: 52.0 MB (52041343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5de1fe22d36e48b637912dbd432cf236f1d956231296b275af61bc5cc951b1a`  
		Last Modified: Wed, 11 May 2022 01:34:36 GMT  
		Size: 7.9 MB (7853647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f57f959274f20ecbbfac9d0dd7e9dcbbc904e7eaf49a4ff37e3149afcbb2247`  
		Last Modified: Wed, 11 May 2022 01:34:37 GMT  
		Size: 11.0 MB (11041680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ec64d54ab363857036338cc3377146eb8961f5b02e14d7ea1b925353b370d6`  
		Last Modified: Wed, 11 May 2022 01:34:57 GMT  
		Size: 57.6 MB (57605368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7b6ae33da6dcd4875f53044d0e67087c5b8c8780fbda31415e9aa49ae4ef707`  
		Last Modified: Wed, 11 May 2022 01:35:33 GMT  
		Size: 199.9 MB (199866202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:34a719c00e4acecdc1d76558ca1fb6279d8e10d3d630f30a50bc9cbe2703b0a8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.0 MB (338960409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cd1d68c8b51ea83674c3b8b38c10d5bc493591100ca2723d6620c95b807754c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:38:49 GMT
ADD file:ba6ab6618a6fab6f0a1d80573b329e26b602c060d940b76c1774ddab96982cd9 in / 
# Sat, 28 May 2022 00:38:51 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:08:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 01:08:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 01:09:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 01:10:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d1098d76e3f40923a061abc8c2e6697409b0a2428eab6f37ae394a7b491b1cad`  
		Last Modified: Sat, 28 May 2022 00:45:27 GMT  
		Size: 53.9 MB (53948486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:052560f7b1294898c71f369cf5ba0727eeecd6b6ba0e30c151347d6333c1f5e7`  
		Last Modified: Sat, 28 May 2022 01:20:08 GMT  
		Size: 8.2 MB (8176480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee8b2d3f9aaae772a2ef7c3c5860d032dcd57b82cbaba04dcf2e741bf9b5895`  
		Last Modified: Sat, 28 May 2022 01:20:08 GMT  
		Size: 11.5 MB (11464416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbe8878cdce718f0b7deab1bba8c2471c5e61e909f442fce25f4d619d2ab8be`  
		Last Modified: Sat, 28 May 2022 01:20:31 GMT  
		Size: 59.0 MB (58992104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c4e7fec4100b63a6a20ae4c2a69746640436163427098f13c0efd229821a63`  
		Last Modified: Sat, 28 May 2022 01:21:05 GMT  
		Size: 206.4 MB (206378923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:2c91247c20f714f3c89d04f44f5b80fe8b3fd881b9d0eac592b2dc180bd2eb53
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.2 MB (316189195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0af2fea3853f194e9c9415d0e55650974196d12121b3fcc9d3e0d4f3daf66d48`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:09:18 GMT
ADD file:0db9365eff38bea353e789709159951d557685e098127d950e467c83468aadd7 in / 
# Sat, 28 May 2022 01:09:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:45:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 01:45:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 01:47:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 01:53:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:409912beaa99ac80f6ec57bce7ac6621f4659f5f43cdaf3152de94639a634798`  
		Last Modified: Sat, 28 May 2022 01:19:34 GMT  
		Size: 52.1 MB (52061634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6976dd6800a501b4f86f988f732f79809a62582465ed0c2a06afe5c24d753b1`  
		Last Modified: Sat, 28 May 2022 02:21:04 GMT  
		Size: 7.5 MB (7506250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c469859fffca391e2318192162949a194958f00b7d4d3e4aaf787a8d79865cde`  
		Last Modified: Sat, 28 May 2022 02:21:05 GMT  
		Size: 11.0 MB (11019527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5addbbcd3adf2891ddf68850f2a8a25112410557e4531d8e3918d9c5ea011ff1`  
		Last Modified: Sat, 28 May 2022 02:21:54 GMT  
		Size: 56.3 MB (56313089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f716aef1344fbb6eae0c40aacc7b5610b9c053301faec0b6d0627d377aa4156a`  
		Last Modified: Sat, 28 May 2022 02:24:03 GMT  
		Size: 189.3 MB (189288695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:6599608ef6e2e32b7ec9910c96d3bbc69ead68cbf9a0f3a35510da1cc55024b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.0 MB (345974647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16074f3e37a74863a4a40f9cd66a029aafda44a143159d7681b2dd657c456c8a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:30:46 GMT
ADD file:151ed5fad83d0b4f27c9bb34e41c649df7b7b9cbe789e3036c44d12cf1f53a71 in / 
# Wed, 11 May 2022 01:30:51 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:07:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:08:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 May 2022 02:11:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:27:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:49991d23fb52aaf7937c711b0196364a5011e41402f3ea986702027fadd27e0e`  
		Last Modified: Wed, 11 May 2022 01:41:30 GMT  
		Size: 57.2 MB (57150441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac162b59dc7eb516878ceab4828d006f42ec802f1755cbd5bc3126bf8d03c9e`  
		Last Modified: Wed, 11 May 2022 03:46:29 GMT  
		Size: 8.5 MB (8496430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f4172550a38e5e5676e20f279186dcd1ebf123a9b2693d032e98814590d62a`  
		Last Modified: Wed, 11 May 2022 03:46:29 GMT  
		Size: 12.1 MB (12065559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b1c75bb53e1b4ca0c91d2d1a0d8344e323b723c6a10f2b51bb99bb0cd6f948`  
		Last Modified: Wed, 11 May 2022 03:46:59 GMT  
		Size: 62.3 MB (62308040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65815a6849cdba46fa1750a43dbdaabab9f89a778d6499516a1645b7bd9838f8`  
		Last Modified: Wed, 11 May 2022 03:47:47 GMT  
		Size: 206.0 MB (205954177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:af353d1a3a4a5a9d4d12c7c94b1a996de3ff20bd9f0ff494c2985bc36f5f6d13
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.8 MB (307821808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4089f3b364e01fe523c3b639f62b66da2d9a94d8a58fa937ab02e9d87e8078e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:41:57 GMT
ADD file:4a6691f8332d56b3f631afa5579acf89d2271614f4a4f77baa24e59c0b2b3016 in / 
# Sat, 28 May 2022 00:42:02 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:20:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:20:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 May 2022 02:21:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:22:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5c219aa5bd4928fd8e410d747805f6d8a6cede332d701af0c9e39dca3b50c70d`  
		Last Modified: Sat, 28 May 2022 00:48:58 GMT  
		Size: 51.5 MB (51490385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b51eb782be06235f2446e523178fdce20039860905eeef1a177ee2ab9b7b259`  
		Last Modified: Sat, 28 May 2022 02:34:14 GMT  
		Size: 7.7 MB (7662349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077ec432669cf9233ec7c2120b3f33664a5d8ac0f8d2a61de67643c292801208`  
		Last Modified: Sat, 28 May 2022 02:34:14 GMT  
		Size: 11.2 MB (11157636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7881263aae598e496a174ca6809ac1657096989286b9533de93d9151065f0e`  
		Last Modified: Sat, 28 May 2022 02:34:28 GMT  
		Size: 56.9 MB (56890824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74eeb6e30d970435be02d5716fc8dcc5c5324f9bf45618a7f1bf4ebad716403d`  
		Last Modified: Sat, 28 May 2022 02:34:56 GMT  
		Size: 180.6 MB (180620614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
