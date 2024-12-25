## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:1c388767c3d043d39e520adb31ea4e3e0f19543f0f1417cdf1401221b19a4b67
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
$ docker pull buildpack-deps@sha256:32a64988dee0d893978fb5a8314422a4d8ef539af24a7180043ead121115a3d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.6 MB (376632454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c73a4d0fd62e983efd1523fbe2415e8ea4f929150824b5b65447323ca2f6d438`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f5cb15ca6b13e712531ab64cf0ca7c69c2e82cc28e9adaf6b4610737a1ba0734`  
		Last Modified: Tue, 24 Dec 2024 21:32:33 GMT  
		Size: 52.2 MB (52225405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a81d57692e85975a86c41b040ba4d1697f343d6fa8db79612558993ad0d1444`  
		Last Modified: Tue, 24 Dec 2024 22:15:30 GMT  
		Size: 21.4 MB (21415241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b414df4f5677fe59988b95799e3893179cfd33808399b76d8526efe756540435`  
		Last Modified: Tue, 24 Dec 2024 23:16:08 GMT  
		Size: 67.1 MB (67136807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb2ed8b0ad98a7a774d1e0165b208e918ae26077fa56af6fbf50d871969f0c3`  
		Last Modified: Wed, 25 Dec 2024 00:14:08 GMT  
		Size: 235.9 MB (235855001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ec3f4b26582881885501b391a7114b1f1114574283f1d05b32c6343cef3fda11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16917009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:524aef0580b68d69d62f051f9379d69d5d5868b9f60f878a015597d5469a5400`

```dockerfile
```

-	Layers:
	-	`sha256:3ba89a24d181bea11ff1c1e03d85605d48958f98ccf5afe4ea76b5d196b4661b`  
		Last Modified: Wed, 25 Dec 2024 00:14:05 GMT  
		Size: 16.9 MB (16906833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d39810204e5ea95390bb8face94df9f7b315c37b63e73b8a00766619c37523bc`  
		Last Modified: Wed, 25 Dec 2024 00:14:05 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:b26444cd0d681f606c551cbc47d5359d3a35df7aaaa5bfa387a55db0946944cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.1 MB (341051906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdca5a8949c11cde8efcf040ca643bd10e9b98cb77c9d3d2f2d311ff2061f0f9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5bc33f333779e1bf21a11cec34fde351758a9648cea4a206cd5ca5e5c267d5ca`  
		Last Modified: Tue, 24 Dec 2024 21:33:52 GMT  
		Size: 48.8 MB (48771903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef48cdc7993c776d6ccec56389e66a4c68ee1ceec1afa89a25ae9e60ac171c2`  
		Last Modified: Wed, 25 Dec 2024 01:31:21 GMT  
		Size: 20.3 MB (20307127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3bfde18be32fb9febe492f8f4a14b4e0ea8e6484b78dfcceca3b9ea06b7f0b`  
		Last Modified: Wed, 25 Dec 2024 04:50:04 GMT  
		Size: 65.0 MB (64979315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a019435961c09eda5659511278b7a3e6fcb97fa2348f2b9bbb5058eec0e10ab`  
		Last Modified: Wed, 25 Dec 2024 06:22:41 GMT  
		Size: 207.0 MB (206993561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8aa3da245cd29d5b01e273939e95c9a1e262c2209d59b77faa56fb79c235a87a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16678645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9965da3de7dfa1cb79327286c20a29e4d7e4f4ba0d7042ef2092b123578958bd`

```dockerfile
```

-	Layers:
	-	`sha256:d279f46e2725f98665b235e8fcebe2d50d128a5855b3f6c13dfb204ce12c6f04`  
		Last Modified: Wed, 25 Dec 2024 06:22:37 GMT  
		Size: 16.7 MB (16668410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08abb6e79c521c1e4fa1c9c0b5a876ec642b80eb7d3cdd8f305f100373eaeb6f`  
		Last Modified: Wed, 25 Dec 2024 06:22:36 GMT  
		Size: 10.2 KB (10235 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:55385985caedb19950b81c9de475696914e04672e836beb3c49f895ae604d806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.7 MB (321702301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6b34f202cc9b7e97c8977b98f75093537b9a0ac583436bf3e2f98d37f2cb5d5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b3be1b8d31fc4a12cecca1f9e259b73553bed584845788fd1fc2b66b29ec0da2`  
		Last Modified: Tue, 03 Dec 2024 01:29:47 GMT  
		Size: 46.7 MB (46707234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9942887cd0e4c0dbd616c261161d431660cfe04df19f0fb88f7040ab43995e`  
		Last Modified: Tue, 03 Dec 2024 07:37:28 GMT  
		Size: 19.6 MB (19598543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e09ace64d434f04ef956980b3273a080b684493925dd0ee78451c801f466f0`  
		Last Modified: Tue, 03 Dec 2024 17:17:42 GMT  
		Size: 62.0 MB (62009521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff06fd2d61b65d377aaab6adf0bb8120fbb9c2e98330722bd3c1c1dac2b6a938`  
		Last Modified: Tue, 03 Dec 2024 20:09:22 GMT  
		Size: 193.4 MB (193387003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1c7748deb3acaee05b2c2a23e55bac1b3ea86610b8cf98f2701b585873e98aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16732337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08f9154eeb6c0b65c758f69fdaefe7849c9ba13a1080413b077e77af7aab7be1`

```dockerfile
```

-	Layers:
	-	`sha256:a3774835b78bdec0bc10768902dd8784a7302b6c4bda4c4f4f571b9c60c0ac2b`  
		Last Modified: Tue, 03 Dec 2024 20:09:18 GMT  
		Size: 16.7 MB (16722101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06696dd3871b1157c5fa70e82fdb3835c17190237bc1370b85860a2e7e8e6981`  
		Last Modified: Tue, 03 Dec 2024 20:09:17 GMT  
		Size: 10.2 KB (10236 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:97442ab83e2b6f235041f396abce2d1142ae1ad09710efd52e3edc88be3d7ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.9 MB (367938255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1742daefc131ddd25a6bfab0eab8d7d655ade029a65265ebaf48317430d22983`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5111921f4f194856cc1156a3664c32c64df54cbd5ad15f8c94081cb0e3440253`  
		Last Modified: Tue, 24 Dec 2024 21:35:38 GMT  
		Size: 52.4 MB (52432315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20d0977c0428e556b738a4854988cc1f65b6192c33c235195555a4b1c8e5d58`  
		Last Modified: Wed, 25 Dec 2024 01:50:20 GMT  
		Size: 21.1 MB (21052154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c053c3d6a126675dc183ace458ad37733e728fe47e857880914a939b478acc30`  
		Last Modified: Wed, 25 Dec 2024 08:13:21 GMT  
		Size: 67.2 MB (67168126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd71f7066ad884b9a59d6d52db1fcbbc0cbc769277eadc23750c3b6eb1becf2`  
		Last Modified: Wed, 25 Dec 2024 11:22:43 GMT  
		Size: 227.3 MB (227285660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1e86f948425ccfddb3c466d631a4b304a90af92801385c7f2488123281c7d778
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (17004049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba0d234e16335e232599e0bd7d21917b91e9ac5e67c8eadd9384dee47743b5b3`

```dockerfile
```

-	Layers:
	-	`sha256:b8c5078dc46b8d2be771ff5db29ce5f1f80b823e1db4b2b59b73f78bb571c31c`  
		Last Modified: Wed, 25 Dec 2024 11:22:39 GMT  
		Size: 17.0 MB (16993793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34c66caa1e7dcc2201b3cdd9c1b686d92139853ba163ce5ad8179261e330b6b1`  
		Last Modified: Wed, 25 Dec 2024 11:22:38 GMT  
		Size: 10.3 KB (10256 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7ad63a6a134601a30c341d206de9797d3d7c057dd35f4b59923815100b476154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.7 MB (384666514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84e4b8b980593ba5890660b93a0ae8da2eba36168fbb137ca0ea27d81f30d279`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:314d11be1a34669d77f82c7dd25250c0aca0d10b528a45fcc768df2c73d1a359`  
		Last Modified: Tue, 24 Dec 2024 21:32:39 GMT  
		Size: 53.0 MB (53038809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794215da1008afee770eb56416f34dd01e9c2b54727b8c520b5cbb72c9a0c70e`  
		Last Modified: Tue, 24 Dec 2024 22:14:45 GMT  
		Size: 22.5 MB (22515087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ff84ea00dd6664e516545fe56b76d43f131cd690417ebf04c5ddfefe8e3e2e`  
		Last Modified: Tue, 24 Dec 2024 23:16:18 GMT  
		Size: 69.0 MB (68990976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b21eb7266f6e728aff41972e0cf10e3d04cd05adb1408cd7db0a66313c9d9d`  
		Last Modified: Wed, 25 Dec 2024 00:14:27 GMT  
		Size: 240.1 MB (240121642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9ca0eac46b1c8fcfd9ead9a868d1c340b4acf292e4f5ef98b6b545de5477ddf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16885806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44f382bea74d8df662957706aa00c6ae2b332a5ad4a87dfbca0f050b2f78368b`

```dockerfile
```

-	Layers:
	-	`sha256:5ec184dcbd9cb872b5a304594ea5a99267febadd83348e47272c1e1ef285734d`  
		Last Modified: Wed, 25 Dec 2024 00:14:22 GMT  
		Size: 16.9 MB (16875652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69b2637d75a3806497a8c7201bbcccfee4820a6b4fb757d7cfad0e7095a95d12`  
		Last Modified: Wed, 25 Dec 2024 00:14:22 GMT  
		Size: 10.2 KB (10154 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:97caf8af9ccb753cb7f0a15dd4d6e7b85df199b941e53e473528de89c603957f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.7 MB (352719608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62f24378805246617f053066f67939fc8f86f8c2e0536c869801c4c57300b4a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:547779e8d3d4ddde41b340ccc5c55eed6547696507cc0168eca950de620def24`  
		Last Modified: Tue, 03 Dec 2024 01:28:45 GMT  
		Size: 51.5 MB (51502465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fd17db4d55a0362abe181f4687b9308ab24eba56bf7c357aaf0150dda37b50`  
		Last Modified: Tue, 03 Dec 2024 15:47:12 GMT  
		Size: 21.7 MB (21747415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faad181192abe7945e2597dbe5a13adb7a6c4fc91c9cc8ed7907444e118bfa3f`  
		Last Modified: Tue, 03 Dec 2024 23:25:18 GMT  
		Size: 66.1 MB (66061059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df5e2e3f8704cd8f57eadead12d86fce2f48f9c5471960a3d7caa911e1ba9be`  
		Last Modified: Wed, 04 Dec 2024 04:49:12 GMT  
		Size: 213.4 MB (213408669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a8fc1d3466ccfed6239df0794a374e4154c2dbe91e7dfb3c88eb714ec9781125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 KB (10009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab85850533c58616e5ba9342b19d94baa414e3caae56b247f2fd7324b4e2aba1`

```dockerfile
```

-	Layers:
	-	`sha256:e8a2386f905b3062ec0484433f9fdb32f3b1814e63a581a4fb0f013698107e33`  
		Last Modified: Wed, 04 Dec 2024 04:48:53 GMT  
		Size: 10.0 KB (10009 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:600d3cf79eccbf7381312255a82c13807b24b21a16ee988dc5fb2a8ebccdee19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.3 MB (383327166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aad30ddd14037b2136d932413c954e588068ac38a9982ea112a4e02f948bd85`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8080cf22cba920897d6f69f8cd18b32c615d4fe71eec9143a4055b490742fcea`  
		Last Modified: Wed, 25 Dec 2024 00:33:18 GMT  
		Size: 56.0 MB (56045011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec24b97fe03e846eeb6353a5a5009e4324e4fb188c11fce7c104a3a8159b2eed`  
		Last Modified: Wed, 25 Dec 2024 06:15:11 GMT  
		Size: 22.8 MB (22807309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e50f3565c17459e6c7bc9c56584bd324fe52f1c6e466111fabada8021af303`  
		Last Modified: Wed, 25 Dec 2024 09:44:46 GMT  
		Size: 72.5 MB (72541403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1946eb24f69cccebe5177b0b0ba2cd388c65cfbfae06a7fe1aca26f2232b1b1`  
		Last Modified: Wed, 25 Dec 2024 12:54:58 GMT  
		Size: 231.9 MB (231933443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:af12280fc296f24396ee9f6794c760526002d7098ad9a788e5a321059586ed37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16900049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2266c7b99e23b9f4b66a545708452f6e94d8c5b84baf2c4d8c83e1ee810fddfa`

```dockerfile
```

-	Layers:
	-	`sha256:738fee2396046b1bd76b73b6b2479d9618a091a15d7b4ea3f09c91100d9768af`  
		Last Modified: Wed, 25 Dec 2024 12:54:53 GMT  
		Size: 16.9 MB (16889841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:500348364592a070e3a2ce16adb210bf9f4e0d754d3aa979a5551320569b829f`  
		Last Modified: Wed, 25 Dec 2024 12:54:52 GMT  
		Size: 10.2 KB (10208 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:b62037a1072a5493b0806b2a40083efab88c113730b7224737967891488d4838
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **456.5 MB (456452555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142a3b0445696930eb25b8c778bb03541260e32c1e43e395347b63316ec8736e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:34dc7eee421e2547a72cc18fd960cb61e4cc000ae2301ebea5c1db40e2f928c9`  
		Last Modified: Tue, 24 Dec 2024 21:35:00 GMT  
		Size: 50.7 MB (50711803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b3be9202d049cfd8fab2840745aba862531c266ca24caab8785a1201a2bb14`  
		Last Modified: Tue, 24 Dec 2024 22:26:29 GMT  
		Size: 20.8 MB (20829455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a9bbab72f01dce27644d4f039f493ac5e6e54ff93d5cddb115f95af7c7ff7d`  
		Last Modified: Tue, 24 Dec 2024 23:21:04 GMT  
		Size: 66.2 MB (66171360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54187c1e7b21de5b4cd18d27400647f4fdf2cb2ef2acc86a335258b7e6a877c1`  
		Last Modified: Wed, 25 Dec 2024 00:34:52 GMT  
		Size: 318.7 MB (318739937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:68dc09db9129d24f164526c9c74706cac222ede2349ca25f774adece6924fd7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16960145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a0b8f28ea33804fa8dff20e345656aefcfc11e14b7e86bbf09bf0e5270cb39`

```dockerfile
```

-	Layers:
	-	`sha256:9089f3524de6e9c5ee01095eb8f7378fa6116de0039f2caf84500f7a3c66c04f`  
		Last Modified: Wed, 25 Dec 2024 00:34:10 GMT  
		Size: 16.9 MB (16949938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c59c94f65a1124b3f9e715104ff580b87fe615fa7c8bbe79add536cc5e45d607`  
		Last Modified: Wed, 25 Dec 2024 00:34:07 GMT  
		Size: 10.2 KB (10207 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:5fb8df5aec0f1bf3e1c63677c9b85d80b4d47496a00915b749001c9a36f76688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.0 MB (349968658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23b1fc9ef55cf610c16aa9bd5ae7342b67a4c08d2ab0ed65ccdb0272977c242`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1734912000'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6d2cec60b297953cc4fd2d941f10377b6dad5bfe41703a7cd8819244b88d9c21`  
		Last Modified: Tue, 24 Dec 2024 21:46:45 GMT  
		Size: 52.2 MB (52169916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a975a9a4c83047fb6ec13cd27d1e9c9a446b78d685e928ba2f4297e75463ff9`  
		Last Modified: Wed, 25 Dec 2024 00:17:26 GMT  
		Size: 22.6 MB (22621261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a51670f291e5f6590a069589cb9515f14909c76a4c6118030edb7558e2bad72`  
		Last Modified: Wed, 25 Dec 2024 03:30:15 GMT  
		Size: 68.3 MB (68331428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0238aa16ef303a54d69a3e916a88c6fb29327dcb81f0abd6108089d4bd34f45`  
		Last Modified: Wed, 25 Dec 2024 05:13:05 GMT  
		Size: 206.8 MB (206846053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:210a1ad831cd5071fe9abd99e99dda6ab9b92b7bfb2bd88d1ac14b3c8aaff0f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16693615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9271d4876b9452523d5d62d7e7591f8db3da03f75cd517dca6cfbb8413ee76f9`

```dockerfile
```

-	Layers:
	-	`sha256:8c354271fc65879cce3a01b75a8fc28ee85f6d7c9fcf0dada2013bb8edc321b6`  
		Last Modified: Wed, 25 Dec 2024 05:13:03 GMT  
		Size: 16.7 MB (16683439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b6589f8d9930a64d3e98197dae2c67bcec12b99c7adef5ea4e0941a1b452bcb`  
		Last Modified: Wed, 25 Dec 2024 05:13:02 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json
