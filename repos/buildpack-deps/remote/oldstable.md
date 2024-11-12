## `buildpack-deps:oldstable`

```console
$ docker pull buildpack-deps@sha256:4d15729c8eeb65bb265a30fe8a40747be2108ddc0afc976073bbf3061aa7fb01
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:oldstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:53dfb2729c2ea5c681e9cc5b42af756ee2c8454c5a17c50c941e6ebddfb77e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.5 MB (322476759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a13bb52d64137bbfef4f596c20eb11be62bc22b837c7a8e686bf135c43ac16`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f895247ac53f8ccaff2388685ac5288e243187f243654f4af6205a31f8b693`  
		Last Modified: Tue, 12 Nov 2024 02:37:53 GMT  
		Size: 15.6 MB (15557923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d199724b11b5ccb55a34503a046bfe20064837b3f7beb547b9a3eab1cb57e0`  
		Last Modified: Tue, 12 Nov 2024 03:14:06 GMT  
		Size: 54.7 MB (54735758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293ef60bdfab8ecc34823af26b3df1d9742e9cb94c1103aa66259e0d57784e72`  
		Last Modified: Tue, 12 Nov 2024 03:59:17 GMT  
		Size: 197.1 MB (197074298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6a30dd51335eb7fa371f0c5c3578e31ea1e657405af15cdbe610a70b0f860481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15107915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7616d68f81bc999bf5452b8b43940cd3b46d540ea4f71115ce69871554a2588`

```dockerfile
```

-	Layers:
	-	`sha256:5be5f4ee1b44d0e9aa1dba97561bc4d202ac1188a34c0a7994c931dec99f8303`  
		Last Modified: Tue, 12 Nov 2024 03:59:15 GMT  
		Size: 15.1 MB (15097684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5f4c658a590f8d5785004ec575558228d9e61e0d82304feeb72e9e60105c912`  
		Last Modified: Tue, 12 Nov 2024 03:59:14 GMT  
		Size: 10.2 KB (10231 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7b8ca851482f3ac5dd83f7f776c70287f0e396c927ced8b45b5ea35dc87974e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.2 MB (283245288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69abe948f0dfc547c7a71483c492df89477394a305ebdb17f6869f98afa00207`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:d2ab4547fbd8c2ffd1467397e3bf7357c565dd0ddab7b1fe46a7af555c5a2d58 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a95f74ee8cb74ceb08cfe11180d99d077de86d07cce20c373d10c20ce9885b49`  
		Last Modified: Thu, 17 Oct 2024 03:07:14 GMT  
		Size: 50.2 MB (50241596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f418fba84fbaf7bab67bcb059341b214f170e38610e4b70f45295fd8324614f`  
		Last Modified: Sat, 19 Oct 2024 00:56:46 GMT  
		Size: 14.9 MB (14877684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27a9032c7c4d1cfb31e96212773919f51ec2f6be760fc0f5c35bafbcdb50249`  
		Last Modified: Sat, 19 Oct 2024 06:37:59 GMT  
		Size: 50.6 MB (50613654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0525b656ff73752501ad6cdcf4137840983e49d8b07af0619e3185c5e925fb`  
		Last Modified: Sat, 19 Oct 2024 08:10:07 GMT  
		Size: 167.5 MB (167512354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:99b4df02852c5c9ef436da722253c6fd613682c2b9bce412b4b84eccb3100d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14908379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfbdcebad2cc9a5cf666dadee37e579872b3e9128215ef08cb6e2ff416e2cb19`

```dockerfile
```

-	Layers:
	-	`sha256:265b31aeaa92380f8c3f6425c52713027f95784e4b52573f632e8e7d38cebf55`  
		Last Modified: Sat, 19 Oct 2024 08:10:03 GMT  
		Size: 14.9 MB (14898075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b941b2a22320cb6c9bf38cc58a5be6077fbb15967c5c3ad3119f189d6344a351`  
		Last Modified: Sat, 19 Oct 2024 08:10:02 GMT  
		Size: 10.3 KB (10304 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6fcca6c2686873d338b72e222bcb158f9b6f212d9496aa46386d1570f3ccd69d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314286584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9960592e533e108fb3fcc1d20fc49c509fe953e1b3a136de1b615a35aea5ff42`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1deb2c2ef23607994f7238c8d97d113f5ebd868b8eb64a0c10d2e0983f036a39`  
		Last Modified: Sat, 19 Oct 2024 01:11:09 GMT  
		Size: 15.7 MB (15747789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbc6072bf5318ca0f9f250b4fcc6254d92483650689f0b0d77274be187abd96`  
		Last Modified: Sat, 19 Oct 2024 05:18:19 GMT  
		Size: 54.8 MB (54832658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13f3e7a61817231ad609702b6918e16648b3eec453567dbedd80952df7e3957`  
		Last Modified: Sat, 19 Oct 2024 06:17:47 GMT  
		Size: 190.0 MB (189971242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:820241d97196cee59900426af9c3bb7e6490fc2906443c04683fa92e277a2b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15110154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e441d6a78110371211f6fa8bd15f27a2b2446e97f40e2cefa3b4aaee7748bd`

```dockerfile
```

-	Layers:
	-	`sha256:3f974dae5571e312b034e2e30b7c42b00e5cd62d80d5aa904fc79d3c8f7ee648`  
		Last Modified: Sat, 19 Oct 2024 06:17:43 GMT  
		Size: 15.1 MB (15099830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:268bfc28ef38d7046c158f0988d2a132ffa8e524a824f7c055f6abd6bf05a9aa`  
		Last Modified: Sat, 19 Oct 2024 06:17:42 GMT  
		Size: 10.3 KB (10324 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:40024780c8ab41709798e05afd646c7d83816bbb7bb97d6886d978aaf4b5f314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.2 MB (328166848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfaf42b79695cbbb92c8d381a03a9d409a6148104819b2da33347b8905185497`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 28 Apr 2023 21:58:08 GMT
CMD ["bash"]
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:401daab178046178ea38abc84ce80fe4a7e7530a75e6b198a161344b358750f7`  
		Last Modified: Tue, 12 Nov 2024 00:54:54 GMT  
		Size: 56.1 MB (56093682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7489e598cae5c0812e1ddaf1d0b649b6033369bedffceac2506c8d523d0a1c5d`  
		Last Modified: Tue, 12 Nov 2024 02:37:53 GMT  
		Size: 16.1 MB (16061669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d3219f513bfa7d5289477f316932047bf97c5e63cdb25a5f5d84119699c8fa`  
		Last Modified: Tue, 12 Nov 2024 03:14:14 GMT  
		Size: 56.0 MB (56032476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989e2f9c439cb2101c7b9646a5f44226e8fce450b536fbbdf42b489a8b29cfc2`  
		Last Modified: Tue, 12 Nov 2024 03:59:24 GMT  
		Size: 200.0 MB (199979021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:99aa603c582d2d59b66ba6c53f22a13729334619991cd21f2ac319cccfcb9581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15096234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df97f8ff7c85fa15f17cd6dcd3ea675c70d7e49971247d6cba5f01f7f4b6b7e3`

```dockerfile
```

-	Layers:
	-	`sha256:66246ecf14a66fc01ddb14bad096f8a122ae7266dab2f9f517d0c2e78278d6c3`  
		Last Modified: Tue, 12 Nov 2024 03:59:17 GMT  
		Size: 15.1 MB (15086025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:471d13d8c1ae4297812155d8e61a16689ac6eaf1dea869327f30e24d8bcbcef3`  
		Last Modified: Tue, 12 Nov 2024 03:59:16 GMT  
		Size: 10.2 KB (10209 bytes)  
		MIME: application/vnd.in-toto+json
