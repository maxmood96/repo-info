## `buildpack-deps:stable-scm`

```console
$ docker pull buildpack-deps@sha256:28cdd657bbff6b0810b348883508c2e2fc577e920e4d454b9037dcd2b5431196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:stable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c7de8e62461b2d541a2406feb9d00cf6955fcaf0ce3754854f9f36d61f0be75e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.0 MB (119978199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e3cdf5e068a0a59b3e3e7374e652c4947a493025cd005a5d01f0e643b81823`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:21:08 GMT
ADD file:d6d0bdf8cb07a7a0dc32e9df50ac80ca1a524c3fa48136892ded195061f2194c in / 
# Sat, 28 Dec 2019 04:21:09 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:47:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:47:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 04:47:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8f0fdd3eaac017684c880d836abdaf02f9db7ac8ecca970356482e3d8e315650`  
		Last Modified: Sat, 28 Dec 2019 04:25:39 GMT  
		Size: 50.4 MB (50379720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d918eaefd9de8a1595f56900fdb8ab65a03d64b1da1078da7c0b0bf6f7552a14`  
		Last Modified: Sat, 28 Dec 2019 05:01:44 GMT  
		Size: 7.8 MB (7811715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bf3e3107f525b7dea5b3cdfd15f62666066202105a0aaddbab2a02aefad1f7`  
		Last Modified: Sat, 28 Dec 2019 05:01:44 GMT  
		Size: 10.0 MB (9996202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27622921edb2aae9e0cb64f71a81b4a7cfef8f6a6c766514a018815834ba4e14`  
		Last Modified: Sat, 28 Dec 2019 05:02:00 GMT  
		Size: 51.8 MB (51790562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:8e843c2e7d52f8df01eb5335e14f17ec0ace71d770c2f73dbde8d1d47c93e04c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.7 MB (114671436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbf877d1bb27a44754a22041d3fe22599aa84aea2848152913e057e4ac1a7a8a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:50:15 GMT
ADD file:6bf18e7329237c55b3237dd7bcef2437b4d30b3bad8d3a037de6d1ee6fe15e78 in / 
# Sat, 01 Feb 2020 16:50:17 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:23:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:24:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 17:24:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a49adcb23ec5ae4b2bc57969491059ab926ea9897024ccc31d730f6e486869b4`  
		Last Modified: Sat, 01 Feb 2020 16:56:43 GMT  
		Size: 48.1 MB (48092958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44cfc28270cc4d9e5a56b5d90328d28400d6f679e3c31a617e0c01985c50d546`  
		Last Modified: Sat, 01 Feb 2020 17:45:22 GMT  
		Size: 7.4 MB (7358713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e67b93c00d7fd46fbaa05dcd0a78c9d537ed502d383825d961520179bb3c5611`  
		Last Modified: Sat, 01 Feb 2020 17:45:22 GMT  
		Size: 9.7 MB (9687040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f354c21bed32ff9aadfc15b814dd71b3349ba1d96491ed14485f84474c4c2ba`  
		Last Modified: Sat, 01 Feb 2020 17:45:47 GMT  
		Size: 49.5 MB (49532725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7d8584cfdd4528ee8194a263bcb6eef255ec4482dd2519280915d7f7f202f3ef
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109614795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9905532b6cbdc148edadfa3752949f6d267471ea31a943d0a855611261031909`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:58:42 GMT
ADD file:26fba5cd6ba1fe45f19fb80d1c8e54eac5189e2b93e521b2ba6d5a6b54175e81 in / 
# Sat, 28 Dec 2019 04:58:45 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:43:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 06:43:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 06:44:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:760e5af4a2ec2472d42b6773d075af9d2a006e0b7725ba9992e530f561d326f8`  
		Last Modified: Sat, 28 Dec 2019 05:07:11 GMT  
		Size: 45.9 MB (45859628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93dc761fecef183bb949ae59f45d1f618cc3e8879cb25946ab48737d1d8a59b0`  
		Last Modified: Sat, 28 Dec 2019 07:07:06 GMT  
		Size: 7.1 MB (7096250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73181b0fe903be79034378988be75730f983b13ada732a04ea4f46f73b332896`  
		Last Modified: Sat, 28 Dec 2019 07:07:06 GMT  
		Size: 9.3 MB (9343271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870abc97e939a1f3c484e5c9aec16d33497f3603c57bd4581d15915528703890`  
		Last Modified: Sat, 28 Dec 2019 07:07:28 GMT  
		Size: 47.3 MB (47315646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:695337f8bc57ebe1a366c949afc87481ab8706a406224887e3739eb56edc631e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **118.9 MB (118939372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d649ed6027b2a630a3cca9ae1b3a5ba0a9680a8763917fdcbd93059e6d3b188`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:40:50 GMT
ADD file:b423f4b0ed41dfe1334031fe9b21f7e1c88ccb031d7e8f2ff165d618323424d7 in / 
# Sat, 01 Feb 2020 16:40:53 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:18:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:18:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 17:19:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bc03a7ced18fc43ea9523dfb256d2c3fbb835dc0bb54bdb7fd309edf936a87e7`  
		Last Modified: Sat, 01 Feb 2020 16:46:06 GMT  
		Size: 49.2 MB (49171687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba9d528c1473d79c18b401d44ca06b9733d9c51a8699b98e8325c9de60b9739`  
		Last Modified: Sat, 01 Feb 2020 17:34:59 GMT  
		Size: 7.7 MB (7680993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:981400d5d268dc989681d5f308b7d2e381809f0bcc82429f443f7539cf6117ba`  
		Last Modified: Sat, 01 Feb 2020 17:34:59 GMT  
		Size: 10.0 MB (9983754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b2d547b8bc79a444406e56d724fb7d961c953e7f2797de4f55b29abee5605f`  
		Last Modified: Sat, 01 Feb 2020 17:35:22 GMT  
		Size: 52.1 MB (52102938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:4611184c519103a7f6ce2d9389e991e0066c3ecce7dd1e051fad224a2cbd76b3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122842687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc0b74eee789b58249ae694ffb245eb50bdedda3d3554280e5c66e69bd3d87a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:39:21 GMT
ADD file:b637f96d557a570f8ab83b28f7b9cdd128958359dd30dc2e03df70b799e132aa in / 
# Sat, 01 Feb 2020 16:39:21 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:23:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:24:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 17:24:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2b34644a479c82db66a603c0b0a1d990911345f8646498fa9b050f306d0e6bf2`  
		Last Modified: Sat, 01 Feb 2020 16:44:10 GMT  
		Size: 51.1 MB (51141949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2f611c9392c4fe86735b477d61fda0e95ea77486175a737114c51586ecce86`  
		Last Modified: Sat, 01 Feb 2020 17:42:17 GMT  
		Size: 8.0 MB (7981506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69713757cc2d87c3255331d40f5061a73ef412208961f1ddd67a59a375397fda`  
		Last Modified: Sat, 01 Feb 2020 17:42:17 GMT  
		Size: 10.3 MB (10338479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956cf07a321afcfed99809a380a1905660e378188fd33d97f136551450be347a`  
		Last Modified: Sat, 01 Feb 2020 17:42:36 GMT  
		Size: 53.4 MB (53380753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:369de1dcfc19a3ad2f0eb55f03aa0a20af6c7370ae546457f9c1fcd5e8d86a55
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 MB (130503394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b2e888517ac54c72f45696e03b81f1bf261091b92025132663acb18ae78f858`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:20:12 GMT
ADD file:7c5858835ffb42e32df47084d7f85ba9392c5e37ee636e19dfae15d858c5b6c4 in / 
# Sat, 28 Dec 2019 04:20:17 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:51:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 06:51:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 06:53:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0a9adf09915c3544b1264f206aec99890c8e5e5c358fc4327886fbdab3c9eecc`  
		Last Modified: Sat, 28 Dec 2019 04:27:21 GMT  
		Size: 54.1 MB (54132515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf9e003a90307c0e87a3bace1df7cc0c72889de0f3060d33cc175cd6bd9f40d`  
		Last Modified: Sat, 28 Dec 2019 07:21:47 GMT  
		Size: 8.3 MB (8252099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24889e07923c5eca1933bb3b0b8bdfc25a42834db78bae343f5fdf88cab3a23e`  
		Last Modified: Sat, 28 Dec 2019 07:21:47 GMT  
		Size: 10.7 MB (10727068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7fe26ecc5fde0ab3859074fdead6e20734403e4cbb2f1867793bbd27fe4290`  
		Last Modified: Sat, 28 Dec 2019 07:22:19 GMT  
		Size: 57.4 MB (57391712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:fb00a9c73a6d79bd9b9c501b0c7203f9606d52d56d547ced17a2d273dccceead
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117534030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033ef629642ef299eaee86d19a1baba82bc79283fa09e320506fc3a7502f89a1`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:41:51 GMT
ADD file:aeaf0b11195b2ba7eb7890ce128ad93c114a8e183a516cf2e4ea42da324c57ea in / 
# Sat, 28 Dec 2019 04:41:51 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 05:44:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:45:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 05:45:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3596c5a237f76c32832c1879a3d0c763989cb13fac0024673b03e9b549b868ea`  
		Last Modified: Sat, 28 Dec 2019 04:44:54 GMT  
		Size: 49.0 MB (48954508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a87e4c2949f278ec7636f6762169d70bd2588ed301cc3e2721aa830a9227fc`  
		Last Modified: Sat, 28 Dec 2019 05:53:25 GMT  
		Size: 7.4 MB (7380503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33b91142ed28640cd70826a84025844f0fa1e7bc50f10b67f6ee03ed2f013ae`  
		Last Modified: Sat, 28 Dec 2019 05:53:25 GMT  
		Size: 9.9 MB (9880177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23386745bcbf27928754e130693faba015951a5923f1fcf54478337f15c7e06`  
		Last Modified: Sat, 28 Dec 2019 05:53:39 GMT  
		Size: 51.3 MB (51318842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
