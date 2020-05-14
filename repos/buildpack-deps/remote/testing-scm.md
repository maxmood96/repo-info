## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:c7d6b884120f456d0e7e53e2dc195abd4209edd6a51718a8a48624933a189005
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

### `buildpack-deps:testing-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:ab47d3f1dbe06408df692f46a98a76aa18edc5872a3bd6fbc966f3c2b235c89a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.4 MB (125440650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76913da811d8da3882a928b42d4ca633fcff9063d252e19aa3782bfbdac2d03c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:19:45 GMT
ADD file:19778292422b784c4eb17d79e7632fc1e3619b6bbbcf16a37bb6179a5c725b1b in / 
# Wed, 13 May 2020 21:19:45 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:25:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:25:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:26:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5ce4ab219a2f8bc551eb2502df5b719a1d8a32c4bbb00b3629001ebb6c5e0b94`  
		Last Modified: Wed, 13 May 2020 21:25:41 GMT  
		Size: 51.4 MB (51384672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f458d7d6918561d3665fcf7c6a15ac5f015d15f94fe4c18152b31a6b390477d`  
		Last Modified: Wed, 13 May 2020 22:43:48 GMT  
		Size: 7.9 MB (7934430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a19396f1ca9e830aec22ccedc673036a5d9fa5707ad170217dadb18689b7f61`  
		Last Modified: Wed, 13 May 2020 22:43:48 GMT  
		Size: 10.5 MB (10463198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:131834a7118626dab711b9bd62471ab667200154b199826ed2ae74c2733ea3e2`  
		Last Modified: Wed, 13 May 2020 22:44:10 GMT  
		Size: 55.7 MB (55658350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:4398c094731f979565a270076f821246d204716378b9c75b9fc1c2e28ccecf34
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120326102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4639eae6f8dab75979a3915f93e0270ca0c9647d7141379b6cd6eeac2c66bb6d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:48:54 GMT
ADD file:e9c6ac7bf8b044473fb44adc857ae60fa2e57fd69c08908b01eef97b087e3aaa in / 
# Wed, 13 May 2020 21:48:57 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:25:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:26:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:27:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:320cb68d32ad923f9944bd8a4839f75e3e1b446fca01a999d67c9a756e55e632`  
		Last Modified: Wed, 13 May 2020 21:58:23 GMT  
		Size: 49.4 MB (49358454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba87e7b395f65b77fc7adc10d5b082bf26da938cfc39952a2c778fefe01abbb`  
		Last Modified: Wed, 13 May 2020 22:53:37 GMT  
		Size: 7.5 MB (7514341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cbc2e3e25ce7b85de9e1d951a3097b9fce980d94c1f8057796afe92a9caab58`  
		Last Modified: Wed, 13 May 2020 22:53:37 GMT  
		Size: 10.2 MB (10157745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c30dd7626fa8f7db8c898aa5539da563d7599d5f8b5a67074b71bd6bd58f2054`  
		Last Modified: Wed, 13 May 2020 22:54:02 GMT  
		Size: 53.3 MB (53295562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:43e229726ec9f74ce77a889ec8604aa57bf9399be3b04c00f629e1cfe089d440
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115652760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9dde45babdfc6349e6ee552bcfcebc76c7d2c759ebb3c5ef5b309af2a070532`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:02:10 GMT
ADD file:85e3bb4657a3517a43e0275a958ad028f3f1684bc8a1a2ab4370553a106583be in / 
# Thu, 23 Apr 2020 01:02:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 04:03:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:03:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 04:04:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:584761cab5c57084a1bd0e36523834571e95168e0a6245926b908313dd826549`  
		Last Modified: Thu, 23 Apr 2020 01:10:09 GMT  
		Size: 47.7 MB (47659184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e340b2750c5a3fef5b49207324ded3ab2bab0ec5b13355bc0b1479b14ed1fe`  
		Last Modified: Thu, 23 Apr 2020 04:28:03 GMT  
		Size: 7.3 MB (7255985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a158eb7564ad64eba8f5106f2f533b09bdfce834baf124daae77ec75837670`  
		Last Modified: Thu, 23 Apr 2020 04:28:03 GMT  
		Size: 9.7 MB (9672905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c73dfc1241c0df6667cc7df3946c524d3e6c3ae8ddd128d21feb342d8fa7069`  
		Last Modified: Thu, 23 Apr 2020 04:28:46 GMT  
		Size: 51.1 MB (51064686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:c35df4a2635394b4dd4876e48ff35e61e8d62d251d9fde5e7a5e5aeb57314fac
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124400769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:289449ac44a4fb30b37696fa8ad656d3acbfdb2e61144e27d8a5e2a948ea9379`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:41:52 GMT
ADD file:642f1f8b3928c38913b91b5770e5ef77e0467db31d0e7342848c66b97b0cefce in / 
# Wed, 13 May 2020 21:41:58 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:19:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:19:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:20:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:da14fdea4bf7eaa36b82ecde9ee461379c7eb32fac279c7d1bce1452edd5bf2f`  
		Last Modified: Wed, 13 May 2020 21:52:10 GMT  
		Size: 50.3 MB (50328349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d18f3d952fdbc982edca77fab71409bebc6a0b410a5f13ffe6fd2685b6020c`  
		Last Modified: Wed, 13 May 2020 22:38:11 GMT  
		Size: 7.8 MB (7809463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382abc5b67b7c0e46916f728a90e7aa0866070c3a67e581de6b5904092e6ca45`  
		Last Modified: Wed, 13 May 2020 22:38:11 GMT  
		Size: 10.5 MB (10459917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30ad6c82e2b7a536da67a837bec581308704d1e15eaf6e92c24578b56e187d9`  
		Last Modified: Wed, 13 May 2020 22:38:32 GMT  
		Size: 55.8 MB (55803040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a303993a3bb0c7a379de4a06bdbed195495a884cf4b3975a853196474bb832c7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129389060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d8da5f15778721d9350fab811b66adc60c0c43235023226378161fbbe44c4b3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:38:53 GMT
ADD file:8842691c10d9cacf5f52fd9fdb3b0f3a9a5ed4212d9f2ab558d17e5efd9a758f in / 
# Thu, 23 Apr 2020 00:38:53 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:39:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:39:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 01:40:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0bf245c0cdf57ebbfbaf49d796259272bf11094420c0537965c4d322d66b4e55`  
		Last Modified: Thu, 23 Apr 2020 00:43:49 GMT  
		Size: 53.1 MB (53124775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3766da29a92d4e7819901f2cd3fd92af428a41fa1efecc94dadb17f8bd6e6d`  
		Last Modified: Thu, 23 Apr 2020 01:58:36 GMT  
		Size: 8.1 MB (8110585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891810791eccf312b55bd366b84147115acf3dc533fd07cc22ed2ce3dd771b1`  
		Last Modified: Thu, 23 Apr 2020 01:58:36 GMT  
		Size: 10.7 MB (10657349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b2d4fc44bb2b15f9080c349ce508b8e7c2e640679fb59aaf2f9f78b4b2b456`  
		Last Modified: Thu, 23 Apr 2020 01:58:59 GMT  
		Size: 57.5 MB (57496351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:0939b5381ab6e4429f579843e54684e734ede31e0038bb1de713a5ee273043e6
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.1 MB (123065191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eabcc2e2701504f3b27aed6c37c8b256414212212c81276f99790c8e9061b6d5`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:08:38 GMT
ADD file:01a8dba65674c16c3bae58d6e4cf7693a0616ee5efc5495e513ba4454fdaa97b in / 
# Thu, 23 Apr 2020 00:08:39 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:46:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:47:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:48:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1ccb563ff5d3d7b0b42a931c0aef1761ab04927c47d729b21ae98a7788ef6af2`  
		Last Modified: Thu, 23 Apr 2020 00:15:41 GMT  
		Size: 50.7 MB (50694211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cc1749bc72a1c4ea633b9f43ee46469e3c9b9fca82f799a577fbddf0a0295d`  
		Last Modified: Thu, 23 Apr 2020 01:06:10 GMT  
		Size: 7.5 MB (7460628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed375c9815816af90643e25af4799e3d5c112ac07bc80b13cc5976a394275f53`  
		Last Modified: Thu, 23 Apr 2020 01:06:11 GMT  
		Size: 10.3 MB (10324480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b47876b2590563400c1a797f7f51c2152380cb414e543cb90b037dbd2cee06`  
		Last Modified: Thu, 23 Apr 2020 01:07:06 GMT  
		Size: 54.6 MB (54585872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e570131f196784a19d8d3c757254dfa14e25f3aa3e5f493f7328646aa6bae324
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.2 MB (136190022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df0b3ff5c7610c9cc2c9fa97b0cbce9ed77529245efc3ebe950a5c14ccebfe3b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:32:36 GMT
ADD file:93aa541f8747875de57b6848e6e2df3b2ae7cdc03dcee5489fcfc1bbf45c4920 in / 
# Thu, 23 Apr 2020 00:32:41 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:39:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:40:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 01:41:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23044bc1c77de90086fe2791c49374dbad1ff9af6b3b4dde5f4d46fc92e6a936`  
		Last Modified: Thu, 23 Apr 2020 00:48:13 GMT  
		Size: 55.9 MB (55855771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b244e406f7e60e72181a1fc05e23631e55e349385a03256c692ed685e75d61`  
		Last Modified: Thu, 23 Apr 2020 02:21:35 GMT  
		Size: 8.4 MB (8356173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77bb62044b675b46ae88158a62f5e93b36bed0459b07a8e50881cd48a7d4070e`  
		Last Modified: Thu, 23 Apr 2020 02:21:35 GMT  
		Size: 11.0 MB (10975739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3335db3829bab72102f9d1637bea7f1aeb652766860510ad63400bf5e283430`  
		Last Modified: Thu, 23 Apr 2020 02:22:09 GMT  
		Size: 61.0 MB (61002339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:678dbeadca77e527bd13f9093f3c8f9b1a51f7b45c381d30034d5cffb3f68d20
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.8 MB (122843813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5db9e3418d8d69fc2f027b13dc05bf523fcebdb4d4bff4bb4475f0adf514827`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 13 May 2020 21:41:47 GMT
ADD file:fbad911feb95f3e7b45e9aa72be8710716eb8fbf3ba846fcaea87309eb9ba2be in / 
# Wed, 13 May 2020 21:41:49 GMT
CMD ["bash"]
# Wed, 13 May 2020 22:37:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 13 May 2020 22:37:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 May 2020 22:37:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9ac9db0ba497fe825137b138e8deceb06a532f1ba6b367b8e68834caedf8e442`  
		Last Modified: Wed, 13 May 2020 21:46:15 GMT  
		Size: 50.0 MB (49994654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160b7562ce5394b96e6b7064989f4900b8d47965a7aab9b7f344e8f1514b24d2`  
		Last Modified: Wed, 13 May 2020 22:47:29 GMT  
		Size: 7.6 MB (7600664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b048fed0769ebce58b27d4fdbbae456c1810f6b85546360e3b80e36bb4be9d4`  
		Last Modified: Wed, 13 May 2020 22:47:37 GMT  
		Size: 10.3 MB (10347812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1e2837c528350ba56db4cda999ef6e93553ecf1d30819aa7eb54b31808155e`  
		Last Modified: Wed, 13 May 2020 22:47:50 GMT  
		Size: 54.9 MB (54900683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
