## `buildpack-deps:resolute-scm`

```console
$ docker pull buildpack-deps@sha256:d69eabf163c7e76bfad439514cbda958feadf27d9c4eecb3dcefb95ba43c132a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:resolute-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:6f42ffadc93b18911de03409f2d89c93c1ef69b3b64f3792ca12e2cdd4e4b452
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110431862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:178c3725b055ca8e3700e9d817d83f5368ad0c81e2a8cc6ceee1d588ff49ab32`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 04 Apr 2026 04:05:32 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-304ffa8f0a534831331ec9aeaa871465/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-304ffa8f0a534831331ec9aeaa871465/images/.temp_layer.4422.tar --tag 26.04
# Sat, 04 Apr 2026 04:05:33 GMT
RUN umoci config
# Sat, 04 Apr 2026 04:05:33 GMT
RUN umoci config
# Sat, 04 Apr 2026 04:05:33 GMT
RUN umoci config
# Sat, 04 Apr 2026 04:05:33 GMT
RUN umoci config
# Sat, 04 Apr 2026 04:05:33 GMT
RUN umoci config
# Sat, 04 Apr 2026 04:05:33 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-304ffa8f0a534831331ec9aeaa871465/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-304ffa8f0a534831331ec9aeaa871465/images/.temp_layer.control_data.4422.tar
# Tue, 07 Apr 2026 01:47:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:43:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:655220791869ab1ba86f5d3c5b0d94c913a6a8cf8683fdea8e7916ee88f08864`  
		Last Modified: Sat, 04 Apr 2026 05:27:13 GMT  
		Size: 41.5 MB (41542350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed07e694340e31e9eed28c5253a4ff1cc0c8f7493cdf0b3ca13f42ec724680b`  
		Last Modified: Sat, 04 Apr 2026 05:27:20 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0ed181995e2a65430d91cecd1b0c9448ba18e91657289a773540499a05c136`  
		Last Modified: Tue, 07 Apr 2026 01:47:39 GMT  
		Size: 19.5 MB (19519688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2456c0e34c4d5785a965539c3bceba8e90132a2bbf33605b390da2e5cc8d54b`  
		Last Modified: Tue, 07 Apr 2026 02:43:57 GMT  
		Size: 49.4 MB (49369437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:248c131bd47a78f62416a84adc8905fa1695871f2ee9d47ab4d34edca4775145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7230695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e73bb5e3769ef1574c69630ebc513667a4f07f53b46fc173acb8f1af9e0cfe1`

```dockerfile
```

-	Layers:
	-	`sha256:7ca7c9a0742857b890d99985aa9f52d9e5a53a3bd43881059ed649ca3f45403f`  
		Last Modified: Tue, 07 Apr 2026 02:43:56 GMT  
		Size: 7.2 MB (7223106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6895d105722a4d85fe9bf2d147ead31eeb1b433b9c750e9099a29c8ade9f12d`  
		Last Modified: Tue, 07 Apr 2026 02:43:56 GMT  
		Size: 7.6 KB (7589 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4d6f25c6e6d72f86956ea5caf1992768639c3818881b0ae120471fa99d66d623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.7 MB (108683281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4c87f244a8a0679e7f16e8d32ad47cd45ca09532d3de7568e1753c1933a5f4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 04 Apr 2026 04:06:02 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-304ffa8f0a534831331ec9aeaa871465/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-304ffa8f0a534831331ec9aeaa871465/images/.temp_layer.4460.tar --tag 26.04
# Sat, 04 Apr 2026 04:06:03 GMT
RUN umoci config
# Sat, 04 Apr 2026 04:06:03 GMT
RUN umoci config
# Sat, 04 Apr 2026 04:06:03 GMT
RUN umoci config
# Sat, 04 Apr 2026 04:06:03 GMT
RUN umoci config
# Sat, 04 Apr 2026 04:06:03 GMT
RUN umoci config
# Sat, 04 Apr 2026 04:06:03 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-304ffa8f0a534831331ec9aeaa871465/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-304ffa8f0a534831331ec9aeaa871465/images/.temp_layer.control_data.4460.tar
# Tue, 07 Apr 2026 02:02:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 03:50:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:609ab57421bd1af42a2b2ba2e2fa7e8ecd4799a9f5478b998c431021edf149ba`  
		Last Modified: Sat, 04 Apr 2026 05:27:48 GMT  
		Size: 38.6 MB (38635912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586c5ef90be606d76a44b9d9e3c477683a177afdb1d76415467cf717d2a82b53`  
		Last Modified: Sat, 04 Apr 2026 05:27:50 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7202b8e7923ca67214b00184e828809cde5cddc5d6309b3bdd7b3f3633608e0e`  
		Last Modified: Tue, 07 Apr 2026 02:02:53 GMT  
		Size: 17.8 MB (17808440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0077ad7689713967a2f0889dececafb19e80be737bd78c4bf24b3fa46a6e8344`  
		Last Modified: Tue, 07 Apr 2026 03:50:20 GMT  
		Size: 52.2 MB (52238524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:42919a3ec74ce5f4bafafe457e88dee7b4c7b421201ec9c61c65d9dc705d6b89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7231264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af080e997b77928a2fbc20747a4e2fea89185835730eb7b046435d8e024d12eb`

```dockerfile
```

-	Layers:
	-	`sha256:7b39059c0d3cc0c7baa16700bb18128279fdddb5a0e3915ff472e2cdbadaa687`  
		Last Modified: Tue, 07 Apr 2026 03:50:19 GMT  
		Size: 7.2 MB (7223611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c648671484f95881d49e68a52e164ba749c1fadfc0d99e09be91585fa6bf7df`  
		Last Modified: Tue, 07 Apr 2026 03:50:19 GMT  
		Size: 7.7 KB (7653 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:75aae80b487b00fb4964e2e168571a9ead3975234638c757384d31a807ad5658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.7 MB (108714714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dff441e29514269d9f571b824aafb56e142efc2414db1a8a68244fb149e553c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 04 Apr 2026 04:06:02 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-304ffa8f0a534831331ec9aeaa871465/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-304ffa8f0a534831331ec9aeaa871465/images/.temp_layer.4500.tar --tag 26.04
# Sat, 04 Apr 2026 04:06:02 GMT
RUN umoci config
# Sat, 04 Apr 2026 04:06:02 GMT
RUN umoci config
# Sat, 04 Apr 2026 04:06:02 GMT
RUN umoci config
# Sat, 04 Apr 2026 04:06:02 GMT
RUN umoci config
# Sat, 04 Apr 2026 04:06:02 GMT
RUN umoci config
# Sat, 04 Apr 2026 04:06:02 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-304ffa8f0a534831331ec9aeaa871465/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-304ffa8f0a534831331ec9aeaa871465/images/.temp_layer.control_data.4500.tar
# Tue, 07 Apr 2026 01:50:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:54:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3adbe9630754b60af479b17234d49e6f8fbb4bfaa9ce7591eb53f4d0d7557402`  
		Last Modified: Sat, 04 Apr 2026 05:27:27 GMT  
		Size: 40.7 MB (40727458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b562786a71fd42412a7597ce892521333eadde3c55792af2ab4f739d0600dca`  
		Last Modified: Sat, 04 Apr 2026 05:27:30 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa397811b421545ceff0b85c28a1afa2f7bc44d4e85bca8b00e9893c4d9b023`  
		Last Modified: Tue, 07 Apr 2026 01:50:40 GMT  
		Size: 19.1 MB (19054738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281357072d00fc5a73b5f55573ac682159e80b9dca001191bcd4bc14f250fe3a`  
		Last Modified: Tue, 07 Apr 2026 02:54:21 GMT  
		Size: 48.9 MB (48932125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5050413ee9aca95738c94533250adfd03c68cc52c1445779b463e4645a809f19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7237162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a755210baa4f4925b054cd6f4e723c69506e1dcb2669c83e4207e36e3892f468`

```dockerfile
```

-	Layers:
	-	`sha256:4a6daa74088024c2109c5bfdfb0439acf27f77887042c3374f8dfcad35910fe0`  
		Last Modified: Tue, 07 Apr 2026 02:54:20 GMT  
		Size: 7.2 MB (7229496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c25d929e32a33298bf0cde0b8cafe7c84adfd9668400651722b7bb5146590274`  
		Last Modified: Tue, 07 Apr 2026 02:54:20 GMT  
		Size: 7.7 KB (7666 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9e4287cb5cf075bc18bcdc55d3729c6d25fd4cc25e7a11d14ffd0faebfe9fd39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.2 MB (124197215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea13ad9c0d204fce5b7d6c2da0328f64dfe83d3fc6aa9c3e2bfd70156c1bbe1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 04 Apr 2026 04:06:14 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-304ffa8f0a534831331ec9aeaa871465/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-304ffa8f0a534831331ec9aeaa871465/images/.temp_layer.4420.tar --tag 26.04
# Sat, 04 Apr 2026 04:06:14 GMT
RUN umoci config
# Sat, 04 Apr 2026 04:06:14 GMT
RUN umoci config
# Sat, 04 Apr 2026 04:06:14 GMT
RUN umoci config
# Sat, 04 Apr 2026 04:06:14 GMT
RUN umoci config
# Sat, 04 Apr 2026 04:06:14 GMT
RUN umoci config
# Sat, 04 Apr 2026 04:06:14 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-304ffa8f0a534831331ec9aeaa871465/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-304ffa8f0a534831331ec9aeaa871465/images/.temp_layer.control_data.4420.tar
# Tue, 07 Apr 2026 04:25:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 09:58:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0db7ebb2f8444a7effc07cc060085d3ebb0c3b962818809de2885138fa645def`  
		Last Modified: Sat, 04 Apr 2026 05:27:38 GMT  
		Size: 46.7 MB (46739906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7250b37d4175277ba214b7494c79a05938f8c42cb3deff8c57b2eb4d7951bfbc`  
		Last Modified: Sat, 04 Apr 2026 05:27:40 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c404c821f83acd9c9ffb53162181be6e1ceab2de93b8b1a7f8de617f8c0383`  
		Last Modified: Tue, 07 Apr 2026 04:25:28 GMT  
		Size: 22.0 MB (21990388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d483f13091e34784b72a22ab7d97877821d8d9ed739fc2a369fd01b53e3d1b46`  
		Last Modified: Tue, 07 Apr 2026 09:59:00 GMT  
		Size: 55.5 MB (55466530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:20128bb0cfae39e6ba4cb6386b870c6f7b6807f5eea579aff5243e4876f84bbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7237800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192a112092df40b991ca60ac20f67b32acb6c2344c0ebc92943984dca08ecf18`

```dockerfile
```

-	Layers:
	-	`sha256:b00a65729e038a9404b322a71a59f44ba16366287612a9b8a036f5960d61773a`  
		Last Modified: Tue, 07 Apr 2026 09:58:59 GMT  
		Size: 7.2 MB (7230179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:099705b07c2fd02f8da6ee8dbd753570d569ed37ddfbfff81dc73bcf1d915dd2`  
		Last Modified: Tue, 07 Apr 2026 09:58:58 GMT  
		Size: 7.6 KB (7621 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0fde6125e421ccd3b8dd64d4920ea59b7d9c0a20c4b947b247eb3308a7de7026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111615093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e1e88a8342734f7bfc86f9124c78afae44acc92b8ecb914206e0cd59ff60a22`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 04 Apr 2026 04:05:44 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-304ffa8f0a534831331ec9aeaa871465/images/ubuntu:rockcraft-base /home/buildd/rockcraft-ubuntu-304ffa8f0a534831331ec9aeaa871465/images/.temp_layer.4472.tar --tag 26.04
# Sat, 04 Apr 2026 04:05:44 GMT
RUN umoci config
# Sat, 04 Apr 2026 04:05:44 GMT
RUN umoci config
# Sat, 04 Apr 2026 04:05:44 GMT
RUN umoci config
# Sat, 04 Apr 2026 04:05:44 GMT
RUN umoci config
# Sat, 04 Apr 2026 04:05:44 GMT
RUN umoci config
# Sat, 04 Apr 2026 04:05:44 GMT
RUN umoci raw add-layer --image /home/buildd/rockcraft-ubuntu-304ffa8f0a534831331ec9aeaa871465/images/ubuntu:26.04 /home/buildd/rockcraft-ubuntu-304ffa8f0a534831331ec9aeaa871465/images/.temp_layer.control_data.4472.tar
# Tue, 07 Apr 2026 03:06:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 04:55:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7c96d396be582fc05093f32b90cd5b1c2be561cf9796984e4d98970af9e3a443`  
		Last Modified: Sat, 04 Apr 2026 05:28:08 GMT  
		Size: 41.1 MB (41111819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785212a2a8b96d4c46d9a8329a0b670629b299d2fed351c8d272623742a1d571`  
		Last Modified: Sat, 04 Apr 2026 05:28:11 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491ddb5859b16f8ab18fd34c9d1c09ef79b6439a31e6acd8be59f733c33f24b5`  
		Last Modified: Tue, 07 Apr 2026 03:07:13 GMT  
		Size: 20.0 MB (19996433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e16b88f0482d9b88a9270a37778d6b9a5c23a0f91e7ca38afb66a35b1cbc00e`  
		Last Modified: Tue, 07 Apr 2026 04:56:26 GMT  
		Size: 50.5 MB (50506453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:645033f6a1a294e2c55963f40d39e62a90f623f0698a96c376c95c936aac90ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7231423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c542bb4c6f14d0afb3f8927c4c158343e7c1badec4ac9aa6cc061bbc5121eb52`

```dockerfile
```

-	Layers:
	-	`sha256:d3e2aa51927c11a9d66e34a8d9b9588c3838d829dfa8e46de2beb524bbf1824b`  
		Last Modified: Tue, 07 Apr 2026 04:56:26 GMT  
		Size: 7.2 MB (7223835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70ff77ca94ed2162d3bc6af7b101aecd503ef92f867036cac3e3f55209eb403f`  
		Last Modified: Tue, 07 Apr 2026 04:56:25 GMT  
		Size: 7.6 KB (7588 bytes)  
		MIME: application/vnd.in-toto+json
