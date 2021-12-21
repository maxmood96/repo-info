## `buildpack-deps:stretch-scm`

```console
$ docker pull buildpack-deps@sha256:78c7e275aaa8141594fe08e659995abb209ab2a2a60df578c6b9a140a59198e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:stretch-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:9fa9fd8b1bcf50ba6ae239f82ff37e95b7575f71f98224cfbfd103afc330fc52
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.8 MB (110787854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a04ee51ca350a8c82804e8e8a6269ea97c0d565ce4d9b4f4303ab48954b94e2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:24:31 GMT
ADD file:4937a62e9e92f367221357a58d7438d1f76546bf3669281431633aebcfd7839d in / 
# Tue, 21 Dec 2021 01:24:31 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:56:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 01:56:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 01:56:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6a56b4def9c45045931a9cf99e9365b558347ae41ec8bfb104a7787e1c3129b0`  
		Last Modified: Tue, 21 Dec 2021 01:31:13 GMT  
		Size: 45.4 MB (45381404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0a7240797a1605f51c11e7c8f49754a8a78c89616dec348fa937886702d115`  
		Last Modified: Tue, 21 Dec 2021 02:04:58 GMT  
		Size: 11.3 MB (11301861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbb8704bdb1f04110dfee1bc6e00f421a37681ff4f136c12337f31c1ccd62bb`  
		Last Modified: Tue, 21 Dec 2021 02:04:58 GMT  
		Size: 4.3 MB (4342385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:737a610bfddaa0e7c87d11580b07707489348ac0fb4cdf2f2265ff2e60246c1b`  
		Last Modified: Tue, 21 Dec 2021 02:05:16 GMT  
		Size: 49.8 MB (49762204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:fbf588a92cde2e8687dfbe8ef8363dc4351ddae620e469ed0504158c09fac145
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.6 MB (106589675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119de5497a77d7e42de837ee815ac9ba1636c994c1701dbd9ee95c5c6a9286bb`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 02:57:10 GMT
ADD file:a2c8513298faf10e5f3b6a070d46acca10a79d9dd50302c55604df9fecb26b2a in / 
# Thu, 02 Dec 2021 02:57:11 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:53:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:53:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:54:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8bd29eaaacb1755f329ce7db7d99eb138c06aad3ab1bb6e8c3b0017596eb1f69`  
		Last Modified: Thu, 02 Dec 2021 03:15:21 GMT  
		Size: 44.1 MB (44091702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e812372186481b18e85105bf8f717c7b3462bcd83b7cbd968f30acebe2349d`  
		Last Modified: Thu, 02 Dec 2021 04:06:51 GMT  
		Size: 10.4 MB (10352021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0272bf1fb82e41a2bd28b3fed21300f54f34aaade421e0b2a669c53136a0d8f`  
		Last Modified: Thu, 02 Dec 2021 04:06:49 GMT  
		Size: 4.2 MB (4161467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef01a32bbeafe701640335a32963992267219bd6a13f945952f4ce3212002f2`  
		Last Modified: Thu, 02 Dec 2021 04:07:26 GMT  
		Size: 48.0 MB (47984485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0172e0d4d1c1f19d4655aacbea408e67df8eb8475b1e7621eb9afb92ebd7a3df
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.1 MB (102119996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432cd3c1456be6f1af7d50578878f66db074e4c02aa841ef6d3d85ce0aae9b1e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 09:10:39 GMT
ADD file:1f947e5a3f8b1da292340501298edf2b879183aea9e90531f21c2b22500e79ad in / 
# Thu, 02 Dec 2021 09:10:40 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 11:49:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:49:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 11:50:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fdee104a33d14b2fdafeeaca15f0252d32280549d3cdc971244796c6e69ad0d3`  
		Last Modified: Thu, 02 Dec 2021 09:27:53 GMT  
		Size: 42.1 MB (42116754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d44a93596b701db7b6e00e592b43547b3bbb7e984a3634dd91b34eb72c03ef1e`  
		Last Modified: Thu, 02 Dec 2021 12:08:46 GMT  
		Size: 10.0 MB (9956149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a002f84bb513d353d241296eda1ba0f01560a1ded46af2fe62c236c787a7559a`  
		Last Modified: Thu, 02 Dec 2021 12:08:43 GMT  
		Size: 3.9 MB (3921247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbec5ebba783328c4a3d0185ed6fb278e4b0e213b45422bec84a45fb0a7b908f`  
		Last Modified: Thu, 02 Dec 2021 12:09:29 GMT  
		Size: 46.1 MB (46125846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:717fca11fd3fafbae5b0b0b73c3f29528033f0cd152ad3d21c971605e1edf931
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.0 MB (104999524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22b82002582da3382d365f9ef7a8fe92da08b3b4d951d9c37d2ca2cf08b7fff8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 08:10:09 GMT
ADD file:7be59c7e3b187d010c0e8625e45324f421a21518258e6bd35bab6e0e86c9494c in / 
# Thu, 02 Dec 2021 08:10:10 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:57:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:58:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 09:58:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6965f119641a6f16b55da01b7c12884960366228a181268b0bf7d0b7d50b2336`  
		Last Modified: Thu, 02 Dec 2021 08:44:30 GMT  
		Size: 43.2 MB (43173684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e211a2e7bbb27084e1f8cd62281719dc9d90e3ddb76b862e471b1cde61512cb`  
		Last Modified: Thu, 02 Dec 2021 10:08:36 GMT  
		Size: 10.2 MB (10216757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca410b1e11dc0ad76bc18c383eafa45a44c94916e27e4f327bc75a9373a250ca`  
		Last Modified: Thu, 02 Dec 2021 10:08:34 GMT  
		Size: 3.9 MB (3873863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c7b6f285f6115be3423f6435cf3cb41ad88d3e8e284f342de24037cc5c1824`  
		Last Modified: Thu, 02 Dec 2021 10:08:54 GMT  
		Size: 47.7 MB (47735220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d4a77c49f1d5cdd00178729dbdd5cca6182e43e0a96ba65c4e163337d1f3c312
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.3 MB (113286899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad2c55f451bb8716f6df3acf808298881aa02741a530e2e0a77c20d074a46b7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 02:42:27 GMT
ADD file:7211d8cf4427f9effab1662b9a54e89548974bde8e4162ccd44fddbc57024912 in / 
# Thu, 02 Dec 2021 02:42:27 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:16:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:16:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:17:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8450ec7364298e2205fbbb540c3ebcbfe46324826539d90ea2e28eeec0bec114`  
		Last Modified: Thu, 02 Dec 2021 02:52:39 GMT  
		Size: 46.1 MB (46097889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae41b4dcbaba225a7711cee1762ef03e55d931f9b8ae39653c61d413766c74e2`  
		Last Modified: Thu, 02 Dec 2021 03:25:15 GMT  
		Size: 11.4 MB (11359074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4378944bb911d45fda5ea1e6a9d56bf6be60774251aea45049160deba235176`  
		Last Modified: Thu, 02 Dec 2021 03:25:13 GMT  
		Size: 4.6 MB (4564943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fd039a786e792e776d9ad9ebbe0bb3444c8c7c458676a67bf483791c04408b6`  
		Last Modified: Thu, 02 Dec 2021 03:25:38 GMT  
		Size: 51.3 MB (51264993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
