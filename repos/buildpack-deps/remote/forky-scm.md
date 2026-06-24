## `buildpack-deps:forky-scm`

```console
$ docker pull buildpack-deps@sha256:bb594fd9f2c99ea816d8c902ff211c4a543f7a6974ae17c3c08143fdc836433c
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

### `buildpack-deps:forky-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2880c7d5050105b9372c9b16f403c08fe5699af71996d21c2748bc1e98596aa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.6 MB (153599822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dedf5aac6aeef3e289cddeb67d441343397cae8ccd7bc0f6f3df2f5bb9a38ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1782172800'
# Wed, 24 Jun 2026 01:41:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 02:28:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b8fc85d169a99c4568f764e95c631aa9c22036d0b8d79c94d2a2182b51723da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8255875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6424e1402fd32592e38a21a3648c9f5d4fb9e8c51b3419e39b701853f8be6ac0`

```dockerfile
```

-	Layers:
	-	`sha256:67a241ae9e25a7fb0f0239bf05262a71bbe80bb329ad3cb22ed7c567eda5af05`  
		Last Modified: Wed, 24 Jun 2026 02:29:02 GMT  
		Size: 8.2 MB (8248609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ca1f50c85b8ae6392b3b3fa30b4c204de9d639442124dc26ed18a2ca848a29f`  
		Last Modified: Wed, 24 Jun 2026 02:29:02 GMT  
		Size: 7.3 KB (7266 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b734cf3f99d3aaeae095f9efa6b4f88d2c2fa79ebdb6cda792c2047e582afc91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142450132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f2a7115405743bc8070d4dc06463eba2d41e7805b7f99ee11920af8ef4c862`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1782172800'
# Wed, 24 Jun 2026 02:24:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 03:55:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:244fe91333017bfe55bf5034f1485924c2c87198d3ce49ba2fd5cc2ef8d32022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8255844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c68e0f398110b1942b752b7a7917aa3d2e714c471c9776a6f8f18e98bd1f46a`

```dockerfile
```

-	Layers:
	-	`sha256:38490acf989dea03fe545ff02959dfd42d8a6e98a2f7730c27e737bf7f199764`  
		Last Modified: Wed, 24 Jun 2026 03:55:34 GMT  
		Size: 8.2 MB (8248514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f229daa549deb43ea9e3ebfbbc694044f1d5bbe99bbc1db6138005a47a738a7a`  
		Last Modified: Wed, 24 Jun 2026 03:55:34 GMT  
		Size: 7.3 KB (7330 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:abae0a7704d96d8a72982b236dc8044d4575c7f3234ab002f69a25b5cdb7dcff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (151984015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df674701c491f5fa6d85e3b15dae82527205a8b83fc103f7833def1237431cbf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1782172800'
# Wed, 24 Jun 2026 01:45:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 02:35:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a5c7ff91964cc8744ac9036833423096bd1074b1d96517f48fb544db089dfd56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8267457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8436b766ba7e3a68d20e95a43bace54e1602ae97a085a25e32549b76d87d22ce`

```dockerfile
```

-	Layers:
	-	`sha256:74c4e8acd4ce52001ef91895006412b5f63d1c9e131e2ecdf74318500b81df67`  
		Last Modified: Wed, 24 Jun 2026 02:35:35 GMT  
		Size: 8.3 MB (8260111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:737bfd03f5c93f77110b5e56b860e6d211c3d4a7730622ff571c078d0379fd4a`  
		Last Modified: Wed, 24 Jun 2026 02:35:35 GMT  
		Size: 7.3 KB (7346 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:462c3f0e648e7597b1e768127817739962aa5b5a4dc34e107be12dc136b30e54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.2 MB (158187771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c6345ddc7f4783338a97da7a5586e3c4647dd004a3be173af90791e0c515670`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1782172800'
# Wed, 24 Jun 2026 01:44:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 02:35:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:11923400c75adba68715f9e80322aad9417b0b0cd20e0760a623b4cf9472b0d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8251351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a1668e9895e8b7fe59a272dfc1e3fca334a458a3d1dc948478fa79e057e9323`

```dockerfile
```

-	Layers:
	-	`sha256:52f14ca957031b124c16317f92f512fbe00d5990ed3c5cf49639e3ad8ad2c6fb`  
		Last Modified: Wed, 24 Jun 2026 02:35:24 GMT  
		Size: 8.2 MB (8244107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b074022e14c21a178558ead780769f520377983b4762ccbc30eff278f04bbed`  
		Last Modified: Wed, 24 Jun 2026 02:35:24 GMT  
		Size: 7.2 KB (7244 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:34d8bfc62e69a1d197ed08bdc7b1a6413ad184bb445779ee241dbf132bbd33c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166844402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d24af7329820ac365a04fa4a081a375bf783f76e7d68e030af7c994e56da33b3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 04:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 10:26:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5b17ef84f535aed2b25d0ce02c622953a7dffc0445517b660588e0087571847b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8248142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa09049504c2e444c6ef5316d4aaa8d8e96292a8102c3d689fe32507d386058`

```dockerfile
```

-	Layers:
	-	`sha256:afe3f2869be97e32088392dafe4f6e66d142956326d969b7dc16a951a2a020e0`  
		Last Modified: Thu, 11 Jun 2026 10:27:39 GMT  
		Size: 8.2 MB (8240844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef1f179ab8321fee5c88eff2e983299f1748d13c8352fffb88d187aabf310569`  
		Last Modified: Thu, 11 Jun 2026 10:27:38 GMT  
		Size: 7.3 KB (7298 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:b70d83f1041a78aef007118065c9e549948de48d6d0fe431314bfc002f85f19c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (151007622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b8e45b153612c5ea833ab4b66b7f67e5ce34c0714f97964f2162ef46a80017`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1781049600'
# Sat, 13 Jun 2026 04:38:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 14 Jun 2026 16:52:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:121b9e3d9d17055db9dfe27a3e3a802ce2aed41f83be422e4b756e417c740b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8248194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1509cae6b50834681483ba283c842a7ddeaff3ce76d62d5c1b69986ee5f562e2`

```dockerfile
```

-	Layers:
	-	`sha256:f5d764cfb59a283f8c510b95311c6a7c4f5a5d01afba039fb20ed3a9513f4841`  
		Last Modified: Sun, 14 Jun 2026 16:55:58 GMT  
		Size: 8.2 MB (8240896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8728aef37af0bb24a05bffb8c471e068745db070ea0765b2cfabf130706e0d8`  
		Last Modified: Sun, 14 Jun 2026 16:55:55 GMT  
		Size: 7.3 KB (7298 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7c4a317d2afca9124b6687e852eeb5bcbf076600f8760fda143e0a13972a28f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153496499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676c3d5720b9ec8a7b5bda374d1bf9ee02e014c19b04f56d447307142cf1f187`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1782172800'
# Wed, 24 Jun 2026 02:46:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 04:30:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
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

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5d04bc8783760525e786948d36a899c88c77d7b17762ece4df33364207519a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8233729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4145a655da2dd644c1f1a402197dfd43f935cd8777c5c5450443534ee987ba80`

```dockerfile
```

-	Layers:
	-	`sha256:047c81ca056990894591cc9b42e85c98199826462c6fda6556734f89a8d4e545`  
		Last Modified: Wed, 24 Jun 2026 04:30:42 GMT  
		Size: 8.2 MB (8226463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68e5c72c51f5557e04587594680aaef8a31c277be96e32ebfa8f4b3e9fda2621`  
		Last Modified: Wed, 24 Jun 2026 04:30:42 GMT  
		Size: 7.3 KB (7266 bytes)  
		MIME: application/vnd.in-toto+json
