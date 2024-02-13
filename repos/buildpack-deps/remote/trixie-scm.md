## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:3ea3579d245c79a18544087c6d91c219edd3b0337a74f4eb36256a9e2e178361
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

### `buildpack-deps:trixie-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a3fcacb276a237f179f61690e5dcf33fcae1cd25c9d66e28b5c273bba37c9737
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.6 MB (145635764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20a1c0ac84dc2701c68aa9b881afc91e9a799e4038b2d8e2b53539ea03dd105c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:40:05 GMT
ADD file:fdbc095d632d315bfdea7b6a7cb53bfc7d32b5f6d604481cc9ff350c6ee09e3a in / 
# Tue, 13 Feb 2024 00:40:05 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:28:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:28:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:02ffa0574dfa0456dc05b0e175a93781ebc31447cddca3de402d11ac2734c97a`  
		Last Modified: Tue, 13 Feb 2024 00:46:31 GMT  
		Size: 52.3 MB (52331572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8b4acf3d75cdfabf855170e302e7faa684ea2ab5ed2c5f7ca4ab289f942ae3`  
		Last Modified: Tue, 13 Feb 2024 01:34:58 GMT  
		Size: 26.8 MB (26849910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63e96ba6a4df5f9a034d0f042c6ba596296abfca3f619a6c6625bec56ca08f02`  
		Last Modified: Tue, 13 Feb 2024 01:35:16 GMT  
		Size: 66.5 MB (66454282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:b838c3dc66a1a215063f98adf3d8e14768aa083ecda160e1a56919533aac4201
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.8 MB (138758338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:152fbe5a782479f6d405e1df9c69ab00418bcf8eef4beb82731fd5c35dcc575d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:11:00 GMT
ADD file:8084501970c8177779352fb042faf935926737abda51187262ee0b2cabb246de in / 
# Tue, 13 Feb 2024 01:11:00 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:50:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:51:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6eafce9f3c4ac029ffad9441b0ad63ffd00fa23ea2ac500527ce7dcf6ceec0f3`  
		Last Modified: Tue, 13 Feb 2024 01:17:23 GMT  
		Size: 49.4 MB (49418395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ca4176ba40503694123907b12411c085ef59844a004a61e19e8ca4ed6fdc68`  
		Last Modified: Tue, 13 Feb 2024 01:58:08 GMT  
		Size: 25.2 MB (25242967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283ca3166ffd80ea83ab111c2390bc95b099bd6fd3a16ebb965559ad02fb483f`  
		Last Modified: Tue, 13 Feb 2024 01:58:33 GMT  
		Size: 64.1 MB (64096976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9916b4e4d28beb0ccf7c8da3e9126dc3f7cdb6be859659f29de26f717d285171
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.8 MB (132795258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfcc0c57c5387e8ee87f425a5b5c418ee5b74927d02b6035d0f6ed30083107f3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:24:05 GMT
ADD file:f3b7f1f27caea165ab01da75acbaae7e03df94488e3cfefa977f306caf975209 in / 
# Tue, 13 Feb 2024 01:24:06 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:23:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:24:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:579ea7eccb92178525cb18bd8dc77986380b3f914f60227ce0c74c4ada08c61a`  
		Last Modified: Tue, 13 Feb 2024 01:31:46 GMT  
		Size: 46.9 MB (46914007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ba2a252ec366e26c0dbd94c623c7e6c905afe0f198ac0d2cd9f018673abbf3`  
		Last Modified: Tue, 13 Feb 2024 04:32:13 GMT  
		Size: 24.4 MB (24422541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d8b8f779f6f6934c8df0f23fb560ca92edd571c516e89d73b9eb684de34c1c`  
		Last Modified: Tue, 13 Feb 2024 04:32:36 GMT  
		Size: 61.5 MB (61458710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:72860f7e24a59e3a5327ffdda80ee0b9118a53789dbb50a2f53ccc6a0492e44a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.1 MB (145123577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac7ec8b348e610c9910071f8e26c3de4db6e8c345b8bbdc78c81547992faa4b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:43:09 GMT
ADD file:b40105fd74cc055edd0e68436fc1b45799a62376b3530660f3a93d3c606cb590 in / 
# Tue, 13 Feb 2024 00:43:09 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:44:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:44:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bcbaf42bd4ac1f9cb9ae9a8d53c22847171447fef1719f5037eaeed94f945284`  
		Last Modified: Tue, 13 Feb 2024 00:49:06 GMT  
		Size: 52.2 MB (52194112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e56f725cf4defa388afd50973a22d727c0eea3662f1f6927b2da7c29431eccc`  
		Last Modified: Tue, 13 Feb 2024 01:50:22 GMT  
		Size: 26.4 MB (26367599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddbc13be4438f9f8d894060aed3c33f0d7346f4270baeb1a88d2666d594e5e6`  
		Last Modified: Tue, 13 Feb 2024 01:50:38 GMT  
		Size: 66.6 MB (66561866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ca387afdf0e91d05db41030b363b68a3df8bf459fa80447c8aaa0e92d6748c46
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.3 MB (149296900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e01436b9ac474e17d8a06155260b7b95b4b6bcc35a0ad139578ccd2d36a12d94`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:45 GMT
ADD file:48adfe9ef1da0d6e87fe297dd6cf8e9e117db33c490c41c77b6f2aadda29a275 in / 
# Tue, 13 Feb 2024 00:41:46 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:27:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:27:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b1a72a4bdfc8e16b8965d5db9e85a05a0f23a851b8b45d3b9e7376d79f2f223b`  
		Last Modified: Tue, 13 Feb 2024 00:49:03 GMT  
		Size: 53.2 MB (53166976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52348cdaee951cfde5088d97935929bf6f09626868b2b48c50a688783d5fad8e`  
		Last Modified: Tue, 13 Feb 2024 01:35:17 GMT  
		Size: 27.9 MB (27886423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f591e946a39d16953fde73e2ef14b2bfd79e49f9bd7d3f7f47afa1b2b5265f`  
		Last Modified: Tue, 13 Feb 2024 01:35:43 GMT  
		Size: 68.2 MB (68243501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8bc4f8dc524d8284e66aa0912fdab04075f18ca180a4cceca14b9cb16237f183
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143321479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35309638f06a7ca72ae389aca8f405bf09710253cb995f985d34e77ea6a76921`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 02:10:56 GMT
ADD file:9e81c7cdd0919c81ec6e4c8e7ef69562482e6c6184b0d333d4967432528f527e in / 
# Tue, 13 Feb 2024 02:11:01 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:11:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:13:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9e34ce429d95dc24c45b2002b054092ba5fa55ce42b0cd3741fac5028688537e`  
		Last Modified: Tue, 13 Feb 2024 02:22:24 GMT  
		Size: 51.4 MB (51404528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9823263b2593dafa6b195b9b1d81ef1eb1be76f5ae911f0a51ed22fa2c480af`  
		Last Modified: Tue, 13 Feb 2024 04:31:05 GMT  
		Size: 26.7 MB (26662654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141af89200b4b870fed00cbeab38968248af7ce012b97890ac09be125e872ee1`  
		Last Modified: Tue, 13 Feb 2024 04:31:59 GMT  
		Size: 65.3 MB (65254297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d77ae466a3b63ce78c37e94a45ecdcbf0785f1a3ce276e6b3514233624afb230
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154386490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e1b98ec2c42050bd63cf0ec1b4520c25cb528c265b8831e4c2e1207d639f3f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 22:32:14 GMT
ADD file:9862d7fda5f3fc5c48229d44a182f0619051f084c461b10ae5cd841f609dd876 in / 
# Wed, 31 Jan 2024 22:32:17 GMT
CMD ["bash"]
# Fri, 02 Feb 2024 01:52:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 02 Feb 2024 01:53:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:fbf7f53bb9540a00260474ff7da2e470dc3eecfdc9849d2cfb73bb9e5f549622`  
		Last Modified: Wed, 31 Jan 2024 22:38:21 GMT  
		Size: 56.2 MB (56198785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c66c2f24b74b885aed137e39b5414d66a8906b77e1d860f925d28c45bbbdbc`  
		Last Modified: Fri, 02 Feb 2024 02:30:49 GMT  
		Size: 26.3 MB (26252282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24561474467a520bc8085c580cb92087055164baf8702494e9b2e1dc34825ce8`  
		Last Modified: Fri, 02 Feb 2024 02:31:11 GMT  
		Size: 71.9 MB (71935423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4b88686067389882715870e2ba53aef7d41489aeecf6f097e49daae466bfbedf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.0 MB (146950201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b09ced20dd0f1590d7b05d51dd14a6d1ebf2fc4a502255d2e7080781bacb2c54`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:21:00 GMT
ADD file:f20e5306e56598f8b82f84922c40c9e2f7e47e2a8c85bf30e7e3a6a9e21b9401 in / 
# Tue, 13 Feb 2024 01:21:03 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:37:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 02:38:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3bf5d0a5ac97061d670703e5273b82b1ecbc5b9bf33962fb4024d89b066daf10`  
		Last Modified: Tue, 13 Feb 2024 01:32:45 GMT  
		Size: 51.7 MB (51742323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb5ddb994c56eadc492865ce2e238a4c712cc671751f0a8231b33027bdaa2a3`  
		Last Modified: Tue, 13 Feb 2024 03:00:46 GMT  
		Size: 27.7 MB (27653777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd1bb14fde65edf4d3cc63eb384e2aad7fa969df7a3d75e3b18a18e361903aef`  
		Last Modified: Tue, 13 Feb 2024 03:01:01 GMT  
		Size: 67.6 MB (67554101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
