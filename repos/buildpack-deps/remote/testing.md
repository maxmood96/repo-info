## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:ca0b8d42c4f3e8fcbe3fcd732aebacf8c0054bb6c598c33531c4f587840de8b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:testing` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:adcae8030b0aa64e7bb07e6f0b4255484b7afa6f9d29e4b3ceb10596f39458a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.0 MB (351968273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61a7ac63da9e7de76076d6e1cd275dbe8d3cf949231e4d11aa0b7032be545b8c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1782172800'
# Wed, 24 Jun 2026 01:41:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 02:28:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 03:17:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:447e2db1403dde86cfbb4e736a0555036d98321ddc327da9305db2a007cde1f2`  
		Last Modified: Wed, 24 Jun 2026 00:28:17 GMT  
		Size: 48.8 MB (48757790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fbe9d185e99fa84c122139e8f5eb118264f12c2739d72b125a4024012aa961`  
		Last Modified: Wed, 24 Jun 2026 01:41:37 GMT  
		Size: 27.9 MB (27906956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46dfc6d731baee823ba1e8a0ef9ac7372d172c399b7f8df359b41cefe80fb1d`  
		Last Modified: Wed, 24 Jun 2026 02:29:04 GMT  
		Size: 76.9 MB (76935076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3545d83483dcf3e9eaf76f7e5108943250b442d163860a5e1c02fb89f04d2b8e`  
		Last Modified: Wed, 24 Jun 2026 03:18:08 GMT  
		Size: 198.4 MB (198368451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:48057e3792c2281b7e9bfc65e1aadf74d1f75f724bf7d7d22dca984410cd25db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16837910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdbed35ab657df56f9153082c4c8d50eb2297eea45d223751a0f32c033e9140c`

```dockerfile
```

-	Layers:
	-	`sha256:3201dfbd208c4df64454f59a2559006b963558350158791bf3ceb8f4c25f2851`  
		Last Modified: Wed, 24 Jun 2026 03:18:04 GMT  
		Size: 16.8 MB (16827766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a42024a85800bc31b89ae7572cb0a7e965b5d70ea0a15deecd4f12983e96c09d`  
		Last Modified: Wed, 24 Jun 2026 03:18:03 GMT  
		Size: 10.1 KB (10144 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2a9b77483281c9cf73a32658393a99e8e425d0b4ea81b2a746cb3da64cb5c826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.7 MB (297736273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea635d815e025b92493b6f6bd09f27dba69b2e54b269888f19e23e36061c4ec9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1782172800'
# Wed, 24 Jun 2026 02:24:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 03:55:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 04:18:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:36ada862ffe71636cce33b70f21dd2f7cfc66ebaeabbfa49191690cfe0284fba`  
		Last Modified: Wed, 24 Jun 2026 00:27:47 GMT  
		Size: 45.7 MB (45653092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf71912b2942b0ebe3b4c7af5551cd81a88d82445a23cdcd992766cd0205984`  
		Last Modified: Wed, 24 Jun 2026 02:24:21 GMT  
		Size: 25.3 MB (25303025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a287630ebd05be610d1bd9ec5b41e3ec448f5108e677e06ae212b2cc7db5b5`  
		Last Modified: Wed, 24 Jun 2026 03:55:36 GMT  
		Size: 71.5 MB (71494015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1809679b129c306033211e4110264009702f6c9c8e444d7a380418218c444d`  
		Last Modified: Wed, 24 Jun 2026 04:19:03 GMT  
		Size: 155.3 MB (155286141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fac8d9ce3160da89abf0b7893dccb4dee936b2021b9226e5f5bba1135abf9947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16620451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30aebc66918ce88122468244f98ca19540a42399c565b92f982c206893e89973`

```dockerfile
```

-	Layers:
	-	`sha256:491aa7047889f2d2112f527a2d06ecfa4c44190597ac107d333622e4f99093b9`  
		Last Modified: Wed, 24 Jun 2026 04:18:59 GMT  
		Size: 16.6 MB (16610242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16ee871a987af26be9d0eee6861aed2bbdcc57d7b02114fffba8f5e725e65036`  
		Last Modified: Wed, 24 Jun 2026 04:18:58 GMT  
		Size: 10.2 KB (10209 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bdd5579e884d3dcbc50f5b81bd2372dd6bc1b318d8d351f38eb9ee63878f1a6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.5 MB (340467816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:868aae4b2dd8768cee89a3aa40b6b323186a51ba093a3907e0633703c4b0de9e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1782172800'
# Wed, 24 Jun 2026 01:45:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 02:35:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 03:17:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f5991d5bb2fa21186c9152bf0a9fa1c9c73892f68235c440c9967628fa5ecac9`  
		Last Modified: Wed, 24 Jun 2026 00:27:35 GMT  
		Size: 48.8 MB (48768712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6ca5e706504383a18ce6cb67cbeb352fc200523287b4db4c777b56d674314f`  
		Last Modified: Wed, 24 Jun 2026 01:45:13 GMT  
		Size: 27.1 MB (27111423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8e562ebc808640f266dfa12e53d32bf4287ffa8b4390ee319de6e6435fd2fb`  
		Last Modified: Wed, 24 Jun 2026 02:35:38 GMT  
		Size: 76.1 MB (76103880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e0533929b76db64145777ec5a876bfb5e027a3f6e076dbcd8fd4e15f4b8ead`  
		Last Modified: Wed, 24 Jun 2026 03:17:50 GMT  
		Size: 188.5 MB (188483801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ea71dfc90e57fe185a430142f34b140d6ea97c9f8faf15ef10d473860f024902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16944147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878bfed4d177c0b3d036a0a498483008c28ec2bd5dcdf67375828ecfa1099753`

```dockerfile
```

-	Layers:
	-	`sha256:931fdd14bd7ead53f1d53ffa14c0d4e7e2a6f4f3bdbcf41b9808e38c373a10ac`  
		Last Modified: Wed, 24 Jun 2026 03:17:46 GMT  
		Size: 16.9 MB (16933922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03264676e671cd270e452dfb91031373b7dfaec3f320f9f90f6ee358a7ff1fa3`  
		Last Modified: Wed, 24 Jun 2026 03:17:45 GMT  
		Size: 10.2 KB (10225 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d8f523b51f1c08f6626246f4655d821306e6818d966daec3f9151d146fc68f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.7 MB (359689688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec0968d15783c899e7623d73e8b6ccd29d8f833a62990b60f4544d1eaddce57`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1782172800'
# Wed, 24 Jun 2026 01:44:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 02:35:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 03:17:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9b65e2e922e5570b1d72c057efc4f398b0b14051ad2a0b581d6669e50195e288`  
		Last Modified: Wed, 24 Jun 2026 00:28:28 GMT  
		Size: 50.1 MB (50051032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dfcdfe53f6d94291d31eb390003496590b495637ff3e5a6cf06797e1f95ca6`  
		Last Modified: Wed, 24 Jun 2026 01:44:13 GMT  
		Size: 29.0 MB (29031133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddc528aadcedc0c9f7a6312eec32c2938c9dd4c859a0eb047c8c80c1080e3e8`  
		Last Modified: Wed, 24 Jun 2026 02:35:26 GMT  
		Size: 79.1 MB (79105606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277b7569ee96480ed5172e994c75a3ed5bffad6a6fbd954f9afdb8c6e108c6a6`  
		Last Modified: Wed, 24 Jun 2026 03:18:16 GMT  
		Size: 201.5 MB (201501917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ed021345641238195382e04dab558df12d4e96d6f90f9dc9063a23874d75f648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16807888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2932492e0f7eb50437ea9c74d2c9e553eb17e833d7ac55aeabb9427724aa59d2`

```dockerfile
```

-	Layers:
	-	`sha256:88b22f0a51fa8e780c024a78372a7c340f734b2f94ce080f81f54bac7c5ab5b9`  
		Last Modified: Wed, 24 Jun 2026 03:18:12 GMT  
		Size: 16.8 MB (16797765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:659c5bbd3284f78b43bb6a1972c9f8edfa3dc1a330a7a01bc308c27e62b2bce6`  
		Last Modified: Wed, 24 Jun 2026 03:18:11 GMT  
		Size: 10.1 KB (10123 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0b9fb4967940c89682f3afba55dfedc361a657ca39314e8f05ae276295a52458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.0 MB (364027871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48a4f62c5368f04934a557dc9a6f6e725e42a26bfa4059f44aca1d07816f145`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 04:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 10:26:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 12:45:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a6e9fc5fff5ecef539442636839ebbab04ed9b3cd7caa39a93b1023297047494`  
		Last Modified: Thu, 11 Jun 2026 00:22:03 GMT  
		Size: 54.1 MB (54103105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ae67043641e8afbaed6931d7c5b7fbf2860dd1ffd02c08f3ccdcf4f71c0dc8`  
		Last Modified: Thu, 11 Jun 2026 04:44:57 GMT  
		Size: 29.3 MB (29286641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2adee366a695e860bba6b9b864396a612d4bad8c56699d51febd6115cfbf5f`  
		Last Modified: Thu, 11 Jun 2026 10:27:41 GMT  
		Size: 83.5 MB (83454656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53dc25232a11567acb43059c509a72ae012e0c9b18ffe28586086475b14dd1d1`  
		Last Modified: Thu, 11 Jun 2026 12:46:42 GMT  
		Size: 197.2 MB (197183469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3b569748e7363427af9e35e9d78f326f4bb80088f3d552e5a697d69109a1626e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16826849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a12d57cacdcfcd9cff31d56ccf96d26f2a32008c26d201ac838b879a1d5e5df`

```dockerfile
```

-	Layers:
	-	`sha256:44c584be55d8044c6227aab42b49b4de5966c55f2a1886fa747f76888e9f6412`  
		Last Modified: Thu, 11 Jun 2026 12:46:37 GMT  
		Size: 16.8 MB (16816673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31fcc86ec9f97062395db47ae5dff21655b82ceb0eb8446d689bf18d0b93d9fa`  
		Last Modified: Thu, 11 Jun 2026 12:46:36 GMT  
		Size: 10.2 KB (10176 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:86e2bc741d45d221cad453e46b175df8bb073c54fb1d5ea279ede612c1220799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **483.6 MB (483605041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eebca1ee6e62d36b3f056bdd724eb147628d63f9757b8980724387a0c86c3b7b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1781049600'
# Sat, 13 Jun 2026 04:38:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 14 Jun 2026 16:52:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 15 Jun 2026 18:45:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6ed3cb07ce8ad88fd9ce6ed049f21f5d3412d5a91293105a260fd0d8e0631f44`  
		Last Modified: Thu, 11 Jun 2026 02:45:18 GMT  
		Size: 46.9 MB (46868403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbb714707e363663ab0edd89dc96807f795de4da64598f885f54d7c7c44ada6`  
		Last Modified: Sat, 13 Jun 2026 04:39:40 GMT  
		Size: 26.5 MB (26471353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f3c19fe899b06864910dfe2969dca7d63f75a9c740280bf6017b248680b7d6`  
		Last Modified: Sun, 14 Jun 2026 16:56:08 GMT  
		Size: 77.7 MB (77667866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c213baeea96014b6cdcdf5f218c2b77e14567b8ec30c51af6812231ce35bd2`  
		Last Modified: Mon, 15 Jun 2026 19:01:57 GMT  
		Size: 332.6 MB (332597419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7d9c553aba6be5f653166139f5b5621b146e4ba5c51fd8853366fabc9bc9b142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16910772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc6e790504ba681eddc56190c364f7ea3c6f256b3452ef24b5c8542c36b9ccd3`

```dockerfile
```

-	Layers:
	-	`sha256:658ad52bfcb40042074c273d9d51fd4779a186d232d71d741dfa60064a428ad4`  
		Last Modified: Mon, 15 Jun 2026 19:01:12 GMT  
		Size: 16.9 MB (16900595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14f1f806847fc60bfce64a7e01ba794675627f606b838b5235936eec8d4834d4`  
		Last Modified: Mon, 15 Jun 2026 19:01:07 GMT  
		Size: 10.2 KB (10177 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:42aba0829cec7101633f69ba45695cd1a0702bd9326a9603cf21136cbd807071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.7 MB (325710089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a4a6f6d96147e8185b8bd4954a4dde170c273bbfee6384e00a5a3544817351d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1782172800'
# Wed, 24 Jun 2026 02:46:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 04:30:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 05:17:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a0b2fd23e0800fbbfc85ca591b838ee879d8a24facc5eea58fda6e804f1b9315`  
		Last Modified: Wed, 24 Jun 2026 00:27:12 GMT  
		Size: 48.5 MB (48491838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43575a3ea94da16bd123e8c57b5643233473a759e5bc49fa7c335021337677df`  
		Last Modified: Wed, 24 Jun 2026 02:46:16 GMT  
		Size: 27.5 MB (27502684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13ca6cf4b3c6ff832c7a9acd30b12a22b5d426165eed58f9db505c1599816789`  
		Last Modified: Wed, 24 Jun 2026 04:30:45 GMT  
		Size: 77.5 MB (77501977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c185bb686923545550ebbae636b105fc8288558f6db071fd1a65c79eb62e55`  
		Last Modified: Wed, 24 Jun 2026 05:18:49 GMT  
		Size: 172.2 MB (172213590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f30e7cad5590f5a78ea63522b67b502ac2d48716549a799c300d285d78c30f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16618560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8fd36db05a2769205f91417ad83b742aa16eb52c68e572379661e088a7bb0c8`

```dockerfile
```

-	Layers:
	-	`sha256:83c024062fd6b01a7a509523a2dd64cf0bc259689e140683cab97a55272cd651`  
		Last Modified: Wed, 24 Jun 2026 05:18:44 GMT  
		Size: 16.6 MB (16608415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:827a4d0dc2df6a1e5d3e831bf1f4fc60db2e8ba668b2af70448fa50b95736be6`  
		Last Modified: Wed, 24 Jun 2026 05:18:44 GMT  
		Size: 10.1 KB (10145 bytes)  
		MIME: application/vnd.in-toto+json
