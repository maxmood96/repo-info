## `buildpack-deps:oldoldstable-scm`

```console
$ docker pull buildpack-deps@sha256:190191e3a02c364d2538051d10cf6b972bf5f388de64ee88a0cd912f98d7b294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:oldoldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d3872f4bbda84746d3e023839278b5380cc83b5f2e57e27812e359cdcfec8cec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.9 MB (119898680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e42250bcc32f41abbf71048b5d3f02f09de55ed4c1502afbaef04096b190463`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:34 GMT
ADD file:2fa5242038736e48eaca794d061079c1cbd32fcc4336250001523c41b3177276 in / 
# Tue, 04 Jul 2023 01:20:35 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 03:32:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 03:32:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8eb6dba554cffc072c7a6c696c8a23fc311e543399d84ab3ebc55c07ab54414f`  
		Last Modified: Tue, 04 Jul 2023 01:26:01 GMT  
		Size: 50.4 MB (50448743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e4f798b8796023ecee944e089e79871ca261eedc4a2ee6a38b08418d9160f4`  
		Last Modified: Tue, 04 Jul 2023 03:53:27 GMT  
		Size: 17.6 MB (17579065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90cef27337073d2443e1c3dd4305cf98d70eadb31c10c267225d9639f1cd6de4`  
		Last Modified: Tue, 04 Jul 2023 03:53:43 GMT  
		Size: 51.9 MB (51870872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1b4d9a7f073580e03ec7c8b3e0243dd260f0d9a360b5d6428cf51566261433df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.5 MB (109497548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce83dc96a23dafaf7a58ec0f31d70b644e4715d465e1128b15d0bd604e283def`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 00:58:31 GMT
ADD file:e1c7c10335e2ac86eba02c2785d0ff530cba87131e91c42924072b4010418f93 in / 
# Tue, 04 Jul 2023 00:58:32 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 05:54:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 05:54:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b19cf971d5ed51e0bba0bd71ccd7b797ad4873a62fee0f49588f6ef19a58e659`  
		Last Modified: Tue, 04 Jul 2023 01:03:55 GMT  
		Size: 45.9 MB (45916488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de49cbcb6a4fd553472f2cf39947eef7d00374517274e95f1a822bfb3c8e2cb`  
		Last Modified: Tue, 04 Jul 2023 06:20:51 GMT  
		Size: 16.2 MB (16211416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:551952269cb797c2c924c3af99a03099c86099cd8186bdda487b965d4f08fff3`  
		Last Modified: Tue, 04 Jul 2023 06:21:10 GMT  
		Size: 47.4 MB (47369644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:042c8cbba1e5ec8945d2a178da4a4ab2a7aa52c981f75e0ff0949d2fc8422b11
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118905912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6568bf4370a5bad76d3890ece5e6279395b2d0ae33a68af33183174c29a61ed9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:59 GMT
ADD file:a61276f534601d7b193af24e35c16b73a2913511d2b1ad997c9a8cb907685257 in / 
# Tue, 04 Jul 2023 01:58:00 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 05:58:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 05:58:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5e2555ae6edde2e7933c533234cb224b6d7ef3a3c90041851e31fe29ab7197c9`  
		Last Modified: Tue, 04 Jul 2023 02:02:18 GMT  
		Size: 49.2 MB (49238644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:503bef164a5c225a74d09ad3b129d3bff71bea2ad1fb291b63c6d342493b62ba`  
		Last Modified: Tue, 04 Jul 2023 06:22:50 GMT  
		Size: 17.5 MB (17450024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3816d11f9d5d9a3bb643dd5c7291e610012ec9eef9c769ce5f6107abdf1eb6d`  
		Last Modified: Tue, 04 Jul 2023 06:23:05 GMT  
		Size: 52.2 MB (52217244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldoldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c8e540d022779ddb0a2e6fdb3d322469c3d320d485cf84cefb7f9dff9c5024f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122787487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44252762afe1bc6205da39e4217bfd4fda4800ee9de78325ef92703f7312a27`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Jul 2023 01:39:11 GMT
ADD file:6ecab94f7cb2bc0740a669cfef73f0837a2ecf6475dfb0fc072cbd1a7f60ec41 in / 
# Tue, 04 Jul 2023 01:39:11 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 05:33:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Jul 2023 05:34:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9b3c3fd2dd1697ce9fed8a2be0142b2d1294d424c56d0ce6d44bb8055d77e35d`  
		Last Modified: Tue, 04 Jul 2023 01:44:33 GMT  
		Size: 51.2 MB (51206276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a0e83aa5cadecbd9663b4464fa33665e930f60918a3178f75983604fc64d38`  
		Last Modified: Tue, 04 Jul 2023 05:40:47 GMT  
		Size: 18.1 MB (18095483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88eede3a0f204f9d3d5eae24a7e5f5ddd9f533ad476bf4e77ee81a22bdb07f9a`  
		Last Modified: Tue, 04 Jul 2023 05:41:07 GMT  
		Size: 53.5 MB (53485728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
