## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:a489c48e470e7382dff6a6a53820a1c2bef1c5a7b57b156ff2618d4c0e82b364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:sid-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8a44139b3d200d34c0c1045f63857af72c09525f295a87c48a85478c7bd90bfb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.9 MB (125868272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f0a86150031b76b34c549dd3b3286c5f6aaec34898ab2acc647b68509343562`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:21:58 GMT
ADD file:5d2d72d29ae1c01dc7f5bf337c78d40925a9843052910f79f066f681a2ec43e6 in / 
# Thu, 23 Apr 2020 00:21:58 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:58:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:58:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:58:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2bbc6b8c460d7ed40af9e8f69693608780022541107dbb47c4a717e0a15e84f4`  
		Last Modified: Thu, 23 Apr 2020 00:26:48 GMT  
		Size: 52.0 MB (51979787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af86ee5a9d864ef79346df3bd57faa5631e1b16cc83353b543768d6d306d88f3`  
		Last Modified: Thu, 23 Apr 2020 01:04:33 GMT  
		Size: 7.9 MB (7934538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb4c0ecf8059fde4ddfb61bd7bca435c46f56832aba0b7726caffbe9f0eb90c`  
		Last Modified: Thu, 23 Apr 2020 01:04:33 GMT  
		Size: 10.3 MB (10297783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab49313f0d6d21322b207f20dcc4226bec4418a685bbed264ea4a288a05ad50`  
		Last Modified: Thu, 23 Apr 2020 01:04:49 GMT  
		Size: 55.7 MB (55656164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:8598fcb65bfe8b48bb12b7df50b7f0dab61359e516517f16f0258c32c2f508b4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.8 MB (120757549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded75965015434f9169ebcf51f924c44bd222aabf1dd470767e150920d0e42a1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:54:30 GMT
ADD file:a75ce77565b83a916eece2d56e963b63f9ee7367ef197d8c290ff79a800514a6 in / 
# Thu, 23 Apr 2020 00:54:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:36:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:37:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 01:38:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e7313629a61ef455f6387257ffb8f19dafc5546554a81db1483683758531fe25`  
		Last Modified: Thu, 23 Apr 2020 01:02:16 GMT  
		Size: 49.9 MB (49937767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1c899094d7c95a1d63461502d6a6462086ecd6082030f55fd59fefae8e1088d`  
		Last Modified: Thu, 23 Apr 2020 01:51:55 GMT  
		Size: 7.5 MB (7515305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d19b16385622348c287bab3a3358b580809022125ad4d1aca43b5c38cdfcf2e`  
		Last Modified: Thu, 23 Apr 2020 01:51:55 GMT  
		Size: 10.0 MB (10008578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d28a5518079a2ea55f8d7914040ed566f0aeaf677bcab2bccae6721ddb28f3`  
		Last Modified: Thu, 23 Apr 2020 01:52:25 GMT  
		Size: 53.3 MB (53295899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f0dd34d43c68930cf5bb89b18ba628d94d7deb505b594581f1389375f09e0d7c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115670965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:602273a0e69e87a35ab1c47dfc3363a5d3ba765fddbb1182a8dab3821c5af6e8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:05:52 GMT
ADD file:465fed22a1d7f049dd801ccbefcbf7935f5c5f16afe77b6b85ec70d29f68c29a in / 
# Thu, 23 Apr 2020 01:05:54 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 04:19:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:19:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 04:20:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:beb14aff5b9321076d299a3cbc700d0f2230140c74e6d1556733e1f8a03e877e`  
		Last Modified: Thu, 23 Apr 2020 01:13:09 GMT  
		Size: 47.7 MB (47659080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9435f19640aaff696311982d6c431b3aaf1673d5f2f94be3106dc7fed67539b3`  
		Last Modified: Thu, 23 Apr 2020 04:32:42 GMT  
		Size: 7.3 MB (7257375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27313d2b2136e2d0cc017a27c4974044c01dbfdfd2f863ba921839d87686147e`  
		Last Modified: Thu, 23 Apr 2020 04:32:42 GMT  
		Size: 9.7 MB (9672965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1d15e346be4952d2bfeeaa0a5c2b14e01c0f703d6ca46ef995a185e3465efc`  
		Last Modified: Thu, 23 Apr 2020 04:33:06 GMT  
		Size: 51.1 MB (51081545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e3ba12e2235d011e4f880e849a32e67a1afde170328f47a247878a10b1bb5267
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124399187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee784a6fb5c1a9b7355bbbca5e59aad03af09ffb015da1b89212b1595b0e0eb2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:45:26 GMT
ADD file:22517e10f0b5d2760fafa2367b5a187d7ecef96291f15a746c24bfa50f756219 in / 
# Wed, 13 May 2020 21:45:29 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:27:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:28:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:28:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ad0025dc69d6f0241b2f5b614e96cef6e1fd54c9ef07b726338235b4766714ea`  
		Last Modified: Wed, 13 May 2020 21:54:40 GMT  
		Size: 50.3 MB (50328664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2de8e099b34fe681d2134dc5800a33dcf2d66893cc852ada1704e600b8e46fac`  
		Last Modified: Wed, 13 May 2020 22:41:03 GMT  
		Size: 7.8 MB (7809465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2735cc8b188a094edcf282e931946b14d50022e973d985f72d13b23f3a1a810`  
		Last Modified: Wed, 13 May 2020 22:41:04 GMT  
		Size: 10.5 MB (10459849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c718f2ae452283da0b15ae79d609faee60fe428710fa0ad565afc8198c9f8a`  
		Last Modified: Wed, 13 May 2020 22:41:27 GMT  
		Size: 55.8 MB (55801209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e27a60a0a17a94274ff5ec656aec95e9b91c140b4f9eff455f68bfaf6814b9c1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129411621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec484b6d9ab84cfd7ddb42cdb8d8335cfeba49403992a500c11031196b7b3519`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:41:06 GMT
ADD file:5651707cdeb4825b44f6e8cca314dc9b453dbc8c9eb87d4235235b6f6065edd9 in / 
# Thu, 23 Apr 2020 00:41:07 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:53:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:53:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 01:54:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6b90db2302f3b878a7e51a668d323ec00b33326362c4983e10df2b689e081dcc`  
		Last Modified: Thu, 23 Apr 2020 00:46:19 GMT  
		Size: 53.1 MB (53123711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce77e9469d5af64bf3279f4b449bc6a887436148b9e1690295858e67ff72aaa`  
		Last Modified: Thu, 23 Apr 2020 02:02:44 GMT  
		Size: 8.1 MB (8112210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea37667c03d37033a105606940d504f39ee410a6c8103822b0079326b905c448`  
		Last Modified: Thu, 23 Apr 2020 02:02:44 GMT  
		Size: 10.7 MB (10657220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c990c61d17e4dd94174396267f80a8189c9884fbbc6d7385359954821f14a9c5`  
		Last Modified: Thu, 23 Apr 2020 02:03:06 GMT  
		Size: 57.5 MB (57518480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:c210941f60dd7b8389604195924be8bd9be46ddd7d8ee7ba1b85a79ef7ab8ce7
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123079536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e278b7bfe0e5085045fd0431298878eab8be225375ac2a180f4f64376c29a47`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:11:00 GMT
ADD file:66d4b8806942796ca49e31a046824a633333dba393126281f5c12e26efea8e7f in / 
# Thu, 23 Apr 2020 00:11:01 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:56:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:56:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:57:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e50f308fab9e31aebf27548f07771af5a99a609ac88a60bbf74cd4f85125c24f`  
		Last Modified: Thu, 23 Apr 2020 00:19:59 GMT  
		Size: 50.7 MB (50696153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81374d42ab3f43b1e9a01bc0af60264f1036fe997a6abb2a98e309bef8774229`  
		Last Modified: Thu, 23 Apr 2020 01:13:33 GMT  
		Size: 7.5 MB (7461350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f82f88069fa53135d2819a8aa2d5e279767bf7aaf186c38c0b84e09717b63d7`  
		Last Modified: Thu, 23 Apr 2020 01:13:34 GMT  
		Size: 10.3 MB (10324460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cd0a1c2f8318544a7575e0094d5dceea034ae91f430e4404b8d5eec3a37b90`  
		Last Modified: Thu, 23 Apr 2020 01:14:29 GMT  
		Size: 54.6 MB (54597573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:47514cd12706f5649ef0c492ea69d02d591dd2b5b835163441cca8911ccaebdb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136238088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50b06a61df7e2bff8f4bf48743a4240ecc8a6635307d2edb86bc9fa83b7f4e7b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:38:45 GMT
ADD file:d55bd2bc22fb060f41d4316af4a741b519580bd2eaf76cbbbf9e3b88355447eb in / 
# Thu, 23 Apr 2020 00:38:48 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:59:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 02:00:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 02:02:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1757960a31f3d7e8a61f52b30d276d1605aa71eec0c10f82c131db13d7402512`  
		Last Modified: Thu, 23 Apr 2020 00:52:17 GMT  
		Size: 55.9 MB (55855455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6563142de6e877d15e44abd8c25bfd401d3b30ad60789123881110c1b09c3973`  
		Last Modified: Thu, 23 Apr 2020 02:26:04 GMT  
		Size: 8.4 MB (8357037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8308c7f5986dc304d470a4bb73bbf6316be522707269361fee59307548cc763`  
		Last Modified: Thu, 23 Apr 2020 02:26:04 GMT  
		Size: 11.0 MB (10975930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3548c6fd949381bbdfaf54bfbac4ddccdce7a765b0656dee4776b58726b776cc`  
		Last Modified: Thu, 23 Apr 2020 02:26:43 GMT  
		Size: 61.0 MB (61049666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:d9965c72e63f0329b0a51a0eabd7cbe9c8963fe2211f0ed68601144e9e8b9303
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.3 MB (123266847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:836d274776dafcf7cf897530f4a6f3ee6436d73633710588aa05d3b5c5142ded`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:52:32 GMT
ADD file:8af210766ac887956b2d532d05d6f2685732ae449b64cc451bb1892dd0d39fc8 in / 
# Thu, 23 Apr 2020 00:52:35 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:58:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:59:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 01:59:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cfdfbea2787f2ac0078069f7f5d3094e3b61cefcec7239ac77ce892b23d101ba`  
		Last Modified: Thu, 23 Apr 2020 00:56:39 GMT  
		Size: 50.6 MB (50581330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b13e3ca73b27934f52752169891ab565d3136558697ae5958bb58e05acdcc84`  
		Last Modified: Thu, 23 Apr 2020 02:08:41 GMT  
		Size: 7.6 MB (7601311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf12399d434a43c9b18e6f51ac8d33334d68063a5e80a24b4db1e4a3c589fbe`  
		Last Modified: Thu, 23 Apr 2020 02:08:40 GMT  
		Size: 10.2 MB (10183921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f8e5e512c3996df54edcff78ec858912c1ee2a69734a97f7856f6d851b39e1`  
		Last Modified: Thu, 23 Apr 2020 02:08:55 GMT  
		Size: 54.9 MB (54900285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
