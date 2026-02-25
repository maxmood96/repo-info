## `buildpack-deps:oldstable`

```console
$ docker pull buildpack-deps@sha256:9362c5ff63c95e6fd71d576bdca7f46d017b98d44fb979e47e45f5d60c3ec1b3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:oldstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b8d12fbc4f3afb47b1e8d765e688bc16c0a79310ec23a6673e28c036eed810b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.4 MB (348434182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc534a51b3f33834bce27e552e0e8a284bf13b0306b8390ead914156f5792692`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:03:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:33:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab3b37e4807fe48145826511e16a527bbc4695222ceb966669a4d16729b3b94`  
		Last Modified: Tue, 24 Feb 2026 19:18:52 GMT  
		Size: 24.0 MB (24038450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa27031269f0a970255d56a9e793fc2a9d6bb091463cd5e632af4ae274881601`  
		Last Modified: Tue, 24 Feb 2026 20:03:49 GMT  
		Size: 64.4 MB (64395853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c032818082ff938f43355abf00f71e5531be197952a109867259ad63a917c884`  
		Last Modified: Tue, 24 Feb 2026 20:33:56 GMT  
		Size: 211.5 MB (211511102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:aec2d651c6f0475147e79da5c54cc45772a897491435e94ae8854d9483e1b06c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15877950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4136afaef577d699234702ac91e141d55f8964373742ac79abbc7ec81653388`

```dockerfile
```

-	Layers:
	-	`sha256:a9fb2beb4a68b3462829fb74ba2ab1bd8bdb2e890f1578ee48058a565af2d0ec`  
		Last Modified: Tue, 24 Feb 2026 20:33:52 GMT  
		Size: 15.9 MB (15867762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aacd24daaca25a7637833fa8bbadb327ce53003d9f34b79e081c1c19666f5a71`  
		Last Modified: Tue, 24 Feb 2026 20:33:51 GMT  
		Size: 10.2 KB (10188 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c176cf3b306b1617f7087be1490c6c0160286ee048e2268827c5e0e912d9a770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.5 MB (315505674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb8c736278a057e44e3e82da093ca3e5c220c341d5439a2e3a2a7f975cdea322`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:55:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:15:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 22:17:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e6dff74bad3c0a4d20c6ddf48bb9ccf82f570d23f324336b4a4e2168c71b093e`  
		Last Modified: Tue, 24 Feb 2026 18:41:45 GMT  
		Size: 46.0 MB (46021660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d656499e87502826ec64f9b609b22ebce144a3b7eed7bbe76030f651d2bca9`  
		Last Modified: Tue, 24 Feb 2026 19:55:36 GMT  
		Size: 22.7 MB (22713821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ca0c210a5ad5c86b6ed12e63c950d08df64e05096f8461a5edc3033ee692d3`  
		Last Modified: Tue, 24 Feb 2026 21:15:23 GMT  
		Size: 62.0 MB (62008422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86fed3025fc85036061ecf46640e2a141173654bb4ee66f14b4618e9be639ccf`  
		Last Modified: Tue, 24 Feb 2026 22:18:26 GMT  
		Size: 184.8 MB (184761771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c93c68604c30562be3655d5c6ec715a0cb66f0c970f709dfa35eebadf9d6b1e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15674999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8828045418081c31f93ac64b4390d576155b6ad4697a7deb8c17b4c5f15389b`

```dockerfile
```

-	Layers:
	-	`sha256:5dd5570f6d23ff1c1a3d2bdd6c818574ce4ed7748dbb401b330f2f894b7c9cc1`  
		Last Modified: Tue, 24 Feb 2026 22:18:21 GMT  
		Size: 15.7 MB (15664746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50f3b57534260e27134a170768756a110d361f8695674113483a37339e5fc203`  
		Last Modified: Tue, 24 Feb 2026 22:18:20 GMT  
		Size: 10.3 KB (10253 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f06181fb9684b30d7b9fd30269ee92504cacfcbe7550fd2e9501696a2b8fabd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.2 MB (301207408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a1df4c4dfb421d0cfd229980cec668bcfd897a7d5b9855503c820388834b57`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:01:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:34:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 22:16:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:510542cb38bcb0c99cf41f8715bc80ae2e63df19b8399efbb11254ee0ddd4299`  
		Last Modified: Tue, 24 Feb 2026 18:41:53 GMT  
		Size: 44.2 MB (44207818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122a79376a0d51f606a8d45c17043adef288961e7b30a2332c485fac0427d825`  
		Last Modified: Tue, 24 Feb 2026 20:01:59 GMT  
		Size: 21.9 MB (21942084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9742857c89c3fff9f983a1595594994ae63f49f2e0dd92faaa9d5886d69aedc6`  
		Last Modified: Tue, 24 Feb 2026 21:34:25 GMT  
		Size: 59.7 MB (59651871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e7287ccbcb7bf73b3830e6358b3b051c963089d6d133011ac1109b6225fede`  
		Last Modified: Tue, 24 Feb 2026 22:16:36 GMT  
		Size: 175.4 MB (175405635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:40e8f59f869c49805a245799985a433aaaefc763557099a01e0719d0cfc5e73a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15680475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05149ce714df453ea0b2416b6b705174966d02acd94bb97241af9079960c745`

```dockerfile
```

-	Layers:
	-	`sha256:2917a13141506b6afd186b5d2d3d64505234b702ac694c54379c8864794ac3f8`  
		Last Modified: Tue, 24 Feb 2026 22:16:32 GMT  
		Size: 15.7 MB (15670222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9886e246be144a56562d4e569aa4d5d34d3d0024e1c2f4b017ea1def562a8bf`  
		Last Modified: Tue, 24 Feb 2026 22:16:32 GMT  
		Size: 10.3 KB (10253 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:adc6d8c3c358512d67f057da417b6a046adc76412a5138d98c591755cb4c7606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.5 MB (339498971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:017bfa0bef4c7d31909c58f23f3adf7a9ff50c9e4052afb8cd61d96944b979ff`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:14:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 21:27:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443d4217b87aad21c6acb58313c9038eb24571a4e9f81de2463aaf19d403a640`  
		Last Modified: Tue, 24 Feb 2026 19:24:13 GMT  
		Size: 23.6 MB (23604736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d27b842bb73f4af595ce58848c4c53ae713ca5c649636d25b483ca63bccc52`  
		Last Modified: Tue, 24 Feb 2026 20:14:46 GMT  
		Size: 64.5 MB (64479406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869fdd20a7335f51da5a8481862ac636a1e2f1cea7649274e79a5b2a176eaff1`  
		Last Modified: Tue, 24 Feb 2026 21:28:23 GMT  
		Size: 203.0 MB (203041619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a59d02a553130e4e0e7a888b11e17e7caadaa33444738c73da79913209397fbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15906532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:495496dd83e7f4dbcbbb569291cf0d259f0a08c2815e3c572511dae35628bf4e`

```dockerfile
```

-	Layers:
	-	`sha256:adf768f4dba4870a564a08140f0106438c5d6857d53f2eede7a2a768df37856c`  
		Last Modified: Tue, 24 Feb 2026 21:28:19 GMT  
		Size: 15.9 MB (15896264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c85687c1e6692bd234b51225cb0520f10929d55affcc61693608e76b8e1db6dc`  
		Last Modified: Tue, 24 Feb 2026 21:28:18 GMT  
		Size: 10.3 KB (10268 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:941d882e3d24d64192c092d7ee2dc5ca8a72c4a34494293c4c81ddb7c96ede35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (351015742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a48c545a36beec903a25481c17d2f618bc82e71394357fd37c22bf649db697f2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:24:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:56:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:18:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:443394a7d911f581670ce4df7959c82f7e8f0be02b5a7ba3c71bc5958012963d`  
		Last Modified: Tue, 24 Feb 2026 18:41:48 GMT  
		Size: 49.5 MB (49477853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31e1fab6283d72f6ce2de137bc123a8ab89a85f0baa0b6c11c2c6d28c359a32`  
		Last Modified: Tue, 24 Feb 2026 19:24:43 GMT  
		Size: 24.9 MB (24872106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383bd8d2ca9c40d67394c0121b8fdb7d7c8f44082342e21f4188fc611c88e9a6`  
		Last Modified: Tue, 24 Feb 2026 19:56:53 GMT  
		Size: 66.2 MB (66234334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8d5099ab94efc4776f4daf2e8f3ad838cdd3a0ad93d334f7e4465ee341b21b`  
		Last Modified: Tue, 24 Feb 2026 20:19:40 GMT  
		Size: 210.4 MB (210431449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bec43f37e6b3640cf378a612da85d5c2c103c51e56b7ed03df0f32d55d322265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15856155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:718da6f4558504b51f643b9983f7602f96198d0ba61ae622da4331c691082d76`

```dockerfile
```

-	Layers:
	-	`sha256:56e7b23096826c609ebbc8da780228054a408f9afca46dc93d865cfcfd4e1c7b`  
		Last Modified: Tue, 24 Feb 2026 20:19:35 GMT  
		Size: 15.8 MB (15845988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67eeb48920c6ff4a081f7b24e0c7225e67e7eecbd08080dc01c2f40528704a4f`  
		Last Modified: Tue, 24 Feb 2026 20:19:34 GMT  
		Size: 10.2 KB (10167 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:83825022e973f2ca668780df78cc8e16b0292715397a42666fc44ad3ca53bf06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.9 MB (325942379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f13e34dd8c28a681c4439e4611136a26699d2c58ba6f5900960b6327a9ebab38`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 16:06:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 21:28:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 22:13:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:001d31ce76be3df3174382025b0b9e2985ddc96d785143497e14a46cdcdcf951`  
		Last Modified: Tue, 03 Feb 2026 01:12:32 GMT  
		Size: 48.8 MB (48763257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e910e12f1ba466db5d640f799037fd1161885165d6ef1a46de53b55b08cfb02`  
		Last Modified: Tue, 03 Feb 2026 16:07:24 GMT  
		Size: 23.6 MB (23615398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e0ad746711a3754afd4dc1df1be9308a858da3b48f46cc1d318cd1dbf2cb47`  
		Last Modified: Tue, 03 Feb 2026 21:29:58 GMT  
		Size: 63.3 MB (63310108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8dcbde3e87bb22f75629b0dc4ffe06e760eb4211178024075579c18fee0e9fa`  
		Last Modified: Tue, 03 Feb 2026 22:16:40 GMT  
		Size: 190.3 MB (190253616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f3f6b6142452083426f797c33b55ff14439d79550d2bc3310671a14142ca3285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7648330d95574c6ed00f870ba37ebcda0455cb4f9a5871d666310c8ae47db1a`

```dockerfile
```

-	Layers:
	-	`sha256:9feaa2394f7bec757e07102025c8fe546574193ac7f551a30943f87df6aaca0a`  
		Last Modified: Tue, 03 Feb 2026 22:16:21 GMT  
		Size: 10.0 KB (10022 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e3469051c4b0817483622e5004614d88193b8ada64d2464841a59ea2be542599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.4 MB (362409418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a4418118f58cbcf94c0466fe5bd0489a6f6c6c7abe83813a4072ed08e6c2b1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 21:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 02:56:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 06:16:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ba53e63c4e3e4d88f0425bc79a37e364db9aabbff9c13ece5cecc63ec880f3`  
		Last Modified: Tue, 24 Feb 2026 21:19:17 GMT  
		Size: 25.7 MB (25671399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5eaeecfe60befcd3d5daac43038587e48eaaea46a2b5f8466018b05c5579686`  
		Last Modified: Wed, 25 Feb 2026 02:57:13 GMT  
		Size: 69.8 MB (69846164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f4312b16c51bbd6e954a27bda969cc71b767dbba23b0d13c6ef19e992222f9`  
		Last Modified: Wed, 25 Feb 2026 06:18:31 GMT  
		Size: 214.6 MB (214555058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c8eb99f48fcd31350b0b86077abbdec7cc7e35d6fb6c1872dd24891ceaff4a4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15854490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cfada6b6f4e8d7e0ff44aeb5326e0548866a480594bf8c89eadaf79b81de458`

```dockerfile
```

-	Layers:
	-	`sha256:a3cf46eeb8f0e10cf4dc8177a21ecb50fef1b6f9ef5c908dddc71456153a38bf`  
		Last Modified: Wed, 25 Feb 2026 06:18:27 GMT  
		Size: 15.8 MB (15844269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91b634055c104392188d81fd67dea40f45cf3f238cacce17ea7452a9c3e79b4f`  
		Last Modified: Wed, 25 Feb 2026 06:18:26 GMT  
		Size: 10.2 KB (10221 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b76320cdc2b080585f73c60739426dced6842dc842935f92cc0b7a4e9e2d10c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.2 MB (318233097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472d9b44c538f6eace488f1ae2bba27b36470fa5f2a39e58c1121ddcc0ba121d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:56:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 23:52:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 25 Feb 2026 02:14:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:00b1871f38dea81b1982e306480bd9f97cedf7b0cb3342e4bc84925e6082ade8`  
		Last Modified: Tue, 24 Feb 2026 18:41:26 GMT  
		Size: 47.1 MB (47148087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1490eda04f0dc8144e02f684cac28c2862b3a584dd3e8ad7e22b96b35409c89`  
		Last Modified: Tue, 24 Feb 2026 20:56:37 GMT  
		Size: 24.0 MB (24033874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d60976a172fdc4da11bc00a6a1bd9ac1b17420cd914b41c43278a69a7a6013d`  
		Last Modified: Tue, 24 Feb 2026 23:52:41 GMT  
		Size: 63.5 MB (63501714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1942969e3d77428b09cb0c9db5b82d0e36a4e03afd9b9c3361f42a5003de6f8`  
		Last Modified: Wed, 25 Feb 2026 02:15:51 GMT  
		Size: 183.5 MB (183549422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c2a9bfa2b332d6c04a587b202e1d9b2c7325cab63ecba452861284b6e0be9b17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15685549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fb50024af70da7c951983321f6946c9170d44e51dbe454f04eacb2435214405`

```dockerfile
```

-	Layers:
	-	`sha256:2da4e3e04004c6454be63f9b239530485717bbf6ae66d0c306629683baaf7cee`  
		Last Modified: Wed, 25 Feb 2026 02:15:48 GMT  
		Size: 15.7 MB (15675360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:195c7328bf25ad4e06fe12e87f8e2ee1286472f27ff2fece523eec998a05fa58`  
		Last Modified: Wed, 25 Feb 2026 02:15:47 GMT  
		Size: 10.2 KB (10189 bytes)  
		MIME: application/vnd.in-toto+json
