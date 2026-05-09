## `buildpack-deps:bullseye-scm`

```console
$ docker pull buildpack-deps@sha256:aaf0c0c7821ed77674274bf1970cac7cf5601669d83edc10e0baabb5fde3dbd6
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

### `buildpack-deps:bullseye-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:029ba1396a2e608dc66b58ed5156b42678037c0c904250e285e68bcd4235a4b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124314848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f973b9df1f72e3a8b7004df1b0d161fd8479dad31bb169cf9f2806aa69ad4e1c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:40:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:26:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1c662d8f6b122c4f09d6ae1b210df55a5ba6e7b529807c0757ccba0c1ac508e0`  
		Last Modified: Fri, 08 May 2026 18:23:06 GMT  
		Size: 53.8 MB (53763343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9888e096307133d2fbd60bcb00b491486db0aecbd10ad65207abf37059a9af`  
		Last Modified: Fri, 08 May 2026 19:40:30 GMT  
		Size: 15.8 MB (15790695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f960812f05fbc5416b446a8fd445ccdc345be2a630ee73fbe4b2644bb91848`  
		Last Modified: Fri, 08 May 2026 20:26:40 GMT  
		Size: 54.8 MB (54760810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b4a043e9fa15a56f67e611b02ff6e975fd7cc380b1827649ca740cbcceca770f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7928693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eab9a8c51b7ded6152756e3be8a4a204721bc378be6144ad12aed19772fc45f`

```dockerfile
```

-	Layers:
	-	`sha256:2388f0dfe4c79de5c43416d32a47443a67c1c1423422db33301851b973ef186c`  
		Last Modified: Fri, 08 May 2026 20:26:39 GMT  
		Size: 7.9 MB (7921377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:081e16c75ad3f5453258354b0641ec0db4e03a5933973b563691e1e56613bd98`  
		Last Modified: Fri, 08 May 2026 20:26:38 GMT  
		Size: 7.3 KB (7316 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2a98722723ddd1d67ffcade53f9d0a070296f3523250bba2311403e84d9b0e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114611681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d631de5e6669c59ecda3a19a2a2ec3f6e26d7111e38505504ebb2779f27e49`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:44:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:34:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4cb33fa51e00f2c5cad3e12a59f701c1cb73526295425e2f64b4cb13b9375c4f`  
		Last Modified: Fri, 08 May 2026 18:37:03 GMT  
		Size: 49.1 MB (49055106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba52e9af1266c17416a17c315f698fb07fc71701dcf95b70a57e9d0f65c70ea`  
		Last Modified: Fri, 08 May 2026 19:44:47 GMT  
		Size: 14.9 MB (14905070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd446ccde0d71af76f958e25aea6b705f55351a4c8727e3397b0e759244004a`  
		Last Modified: Fri, 08 May 2026 21:35:04 GMT  
		Size: 50.7 MB (50651505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1e5dba12c18d60f2ef54b64da7e3bfaff12c0f20dc65f3beed80e5b37bd0d481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7930159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a00c29802c2cc1c2d065084980d299ac6bd01ee671b33bc160a6266f097571`

```dockerfile
```

-	Layers:
	-	`sha256:dab5a8afc751f6fc7e4f2a98adedfac7f349bf737c075e3658a0a6731537f2dc`  
		Last Modified: Fri, 08 May 2026 21:35:03 GMT  
		Size: 7.9 MB (7922779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40a3fee8f63849b1a8e8a191211b4e932f35384c69b3c7fb16b1403fba76168b`  
		Last Modified: Fri, 08 May 2026 21:35:03 GMT  
		Size: 7.4 KB (7380 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:32b6d7ad4daf3ded6e6b1b02fe78e82384bc4698a32aa0e33fe2de9725c18e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122914454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65a080a71a2ef499efcd1f45754af9e6ab6a2d7213b5410af232a1ac1e320c5a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:42:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:31:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d20a72a3ae72af0f6239652b45dcc6f5eda87bb797e4c05972c586c32afca3f`  
		Last Modified: Fri, 08 May 2026 19:42:32 GMT  
		Size: 15.8 MB (15774834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de92af39e07f00fd21cc384e0f5108a74acadedc0acecf16d700d606eedccd3`  
		Last Modified: Fri, 08 May 2026 20:32:13 GMT  
		Size: 54.9 MB (54886410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e911a2c0461d4511c308d5644687488ef5cedcff5b6897dd7879be7e1253d4b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7934506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374d16bf41c692b39eb702624d69dd373183050f3cd2c524bd4efdac8265889e`

```dockerfile
```

-	Layers:
	-	`sha256:5ecbeb6ccc102b831b7c36ce094edac94a7164461a15f9632702fdda421fcf6d`  
		Last Modified: Fri, 08 May 2026 20:32:12 GMT  
		Size: 7.9 MB (7927111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5efd7378455f9b1bbedbb81b45a5370f4de44fde2f8563310b4e98a098d03bca`  
		Last Modified: Fri, 08 May 2026 20:32:11 GMT  
		Size: 7.4 KB (7395 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bullseye-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e3e050696034e3fb4bcc4deb855fb70f47451863fdf768818df9b026ee6010a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127061611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a209bffcd2cbf6afe2baeeee27942ebf7973aa510d59ca6bb077d7d32de902`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:42:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:02:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:737d996bc05c156425b11be5deec8366db5d7a009f49d85b480b1daec555cf4a`  
		Last Modified: Wed, 22 Apr 2026 00:16:40 GMT  
		Size: 54.7 MB (54705161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f313e1ea7e09266848088c3a09b07b715bfc6a8bb9980dc9b80da0fb20132694`  
		Last Modified: Wed, 22 Apr 2026 01:43:07 GMT  
		Size: 16.3 MB (16295616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae525ab0fbeb04dd4bb1d8468feefde68ce73f1bb5bc987c27f9283ecf43104`  
		Last Modified: Wed, 22 Apr 2026 05:02:53 GMT  
		Size: 56.1 MB (56060834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bullseye-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f6e8fcc11d79842cfb72f3847f55f09c581e6cb6c78766db0465ff4b48b8c217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7924241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89edbfb8fc274d599fe8f93dedce86b452bd7db36ec8000e310b223e185a5216`

```dockerfile
```

-	Layers:
	-	`sha256:6234661890a8a5ca56972dea09f37deebe12801b82a55889ba9e328936c7401b`  
		Last Modified: Wed, 22 Apr 2026 05:02:52 GMT  
		Size: 7.9 MB (7916947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9de5b62056006caf97edba534125d2e82485cab3dc3506a0d4f98c0c6fe6b447`  
		Last Modified: Wed, 22 Apr 2026 05:02:52 GMT  
		Size: 7.3 KB (7294 bytes)  
		MIME: application/vnd.in-toto+json
