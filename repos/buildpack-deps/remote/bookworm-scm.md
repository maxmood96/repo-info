## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:be1fb11542a78e2bc9225995780a5c5626c78911b706f0f9e9707b5f1a5f64a2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:bookworm-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:da8397bca49114e4bc755920fc4f27672268cc7ef3645459c7193de84b994905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136937285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91471f88c9df001c59ec1e3e9e715e48a7ab8e96bec2554d44bd760cc0ddff2d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf571be90f05e10949e4ae13071c81d3182077d926e3f84169a12e0ce2aec209`  
		Last Modified: Tue, 14 Jan 2025 20:32:59 GMT  
		Size: 24.1 MB (24058643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684a51896c8291a1769034cf6e10971c82a82c43b6b4588d1c71d215953eaa61`  
		Last Modified: Tue, 14 Jan 2025 03:18:17 GMT  
		Size: 64.4 MB (64398680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c8610f352bff81d06967092c6b759a88582a876ec2d6ffb94843407a7da5a56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7760401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a89845b58ed7a5ce4036e91cee1b781afca9805f374fbf1cf530cafaaea47d9d`

```dockerfile
```

-	Layers:
	-	`sha256:50b1d090afa73f8e2be911b9dfa4a3dfaebc58034384fcd8ebbd8d82511c5ea2`  
		Last Modified: Tue, 14 Jan 2025 03:18:16 GMT  
		Size: 7.8 MB (7752746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e85b91f44e7503048791f610b23643682bfadab6f19e8102e212bac849985f02`  
		Last Modified: Tue, 14 Jan 2025 21:00:26 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:3e0737500dd875c807744ac867dda252a26a3d09a44c7f49c58118fff327bdb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130735180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9a53b76f74ff2b00f306b39a9da674c6162651bb21d82e7b013c8cb9519cc2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:237814a70d9f7e95f3568236c75036fcef22a88f1a76245129eca111484c0351`  
		Last Modified: Tue, 14 Jan 2025 01:33:00 GMT  
		Size: 46.0 MB (46006814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538440badda779e62c187f05746a171687a461254bcff139b6eb8551e262665b`  
		Last Modified: Tue, 14 Jan 2025 06:08:28 GMT  
		Size: 22.7 MB (22733148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c357ca136a71558c91190c0b04e28bcfcf53691d1c9571249b744ec1b06079`  
		Last Modified: Tue, 14 Jan 2025 22:44:07 GMT  
		Size: 62.0 MB (61995218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8b278c5fdd204f340e1f1c49b41f3c541a49f5ed464034296bb9475d019180ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7762027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e051cacf8e0efa7efe336287813901e16e7dc125ad1db82f12ef824856b1e004`

```dockerfile
```

-	Layers:
	-	`sha256:26e891207b946a8d27ca7e6bcd7e7eacf8b2f2c88e02603ec204fe1beee70952`  
		Last Modified: Tue, 14 Jan 2025 21:00:31 GMT  
		Size: 7.8 MB (7754304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68287f4815f81e9d89f9479927f3e9b1e05ec2603cbff143b1dde9a582ef2d08`  
		Last Modified: Tue, 14 Jan 2025 09:32:09 GMT  
		Size: 7.7 KB (7723 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:49e4ccaedbca671c339d8a55242d7f25e1af167a096aca68b56da8a26e979622
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125784661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5d6202e1e5273856a4827dd5f9a1aaf9c5c9df9e95e406f72acc587373ce0c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c1d5439a488387eb665efad1c794c7763b21afaad1854c8bb55008399919c144`  
		Last Modified: Tue, 14 Jan 2025 01:34:58 GMT  
		Size: 44.2 MB (44184209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787291d61ca82895d27d086bfaf14ce01f401dfbf42f462addc8d1cae464ebab`  
		Last Modified: Tue, 14 Jan 2025 23:01:46 GMT  
		Size: 22.0 MB (21960077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6667f6e75dc8bed2e36123666ac457a4e0228141514ab32e65b9c6f6c7960e3`  
		Last Modified: Wed, 15 Jan 2025 00:14:45 GMT  
		Size: 59.6 MB (59640375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f893443c0cff99fae6cfd9ee2d82f7d9fa1764c42e4b44d6bd02b54a5f8860e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7761753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71830b5b97fe489d694c4fdd593c37b208f010a9b30f5fbbd200b1d5bb8f78f0`

```dockerfile
```

-	Layers:
	-	`sha256:ed0713d12be1303423be5246de90d43ee0ccba8f617f41d991598bef4a257e57`  
		Last Modified: Tue, 14 Jan 2025 21:00:35 GMT  
		Size: 7.8 MB (7754031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dab6ec41bbe5e21c735259ad96692c0dc9cc772b9c0cf51e02e186b1620bc8af`  
		Last Modified: Tue, 14 Jan 2025 16:15:25 GMT  
		Size: 7.7 KB (7722 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3d3e7297c13b3097bf5fb9991ffa9aad0816798a907a8fff792165491174b39a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136261554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413ebeaa354b3c0feb020579c81777bbfe6e0b44434cbb51e0423a9a5e072539`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 20:33:16 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b85d68f8a4dce392d372c8a196863eac6d111c36b714179b4ab30e00c00d1`  
		Last Modified: Tue, 14 Jan 2025 06:59:53 GMT  
		Size: 23.6 MB (23598225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:936252136b926e9bca27f4a5442f6a5d10c0ea4a23ca8b30c65de1bde666d082`  
		Last Modified: Tue, 14 Jan 2025 13:31:06 GMT  
		Size: 64.4 MB (64356433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e54b58bc89d63d6cb7a969a37a81bd05045e92b0531f2dea017d34389f50b348
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7766898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cfdf225184ecb259a96744ec5072a8b6321e328e75488d08232ee1c90c8287a`

```dockerfile
```

-	Layers:
	-	`sha256:ee5a579a1304a0cd9ab66a341c82f90bd0673cbb06d2d921649dc6204d1298a5`  
		Last Modified: Tue, 14 Jan 2025 13:31:04 GMT  
		Size: 7.8 MB (7759151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4b7039d4910144475f784c47b0f938b47a0c5c3de6783cc5280520c1dea87bc`  
		Last Modified: Tue, 14 Jan 2025 21:00:39 GMT  
		Size: 7.7 KB (7747 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b482ce2e8d148e88fd0007a96f91e58e715f59d9072a809c0dce17fd8f3b10fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140589604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ec4b1e09556d9239ce67d83949e7825bdc1697c29775497a4d69d099ea3ae4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:46529f83455afa979c42fcfe436f7b07f4eb4d873a153eb3dcb49167de675239`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 49.5 MB (49457745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259aab4e8ba3f728c64e0bf81358e3f88c26bfd9423ce075dd8f57c76656af67`  
		Last Modified: Tue, 14 Jan 2025 22:15:37 GMT  
		Size: 24.9 MB (24899359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6ad7abc4b78e8f72ee5d0067eb54abc9e1706469627b34bfe3208e0d8634e1`  
		Last Modified: Tue, 14 Jan 2025 21:03:16 GMT  
		Size: 66.2 MB (66232500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:60da79eee8a7f1d7bbbcb541fd6959d76491dc98718e887a2760c3d34e436e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7756451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30db2662975d13b38632d4671e5b4accf52f546ccc3b7da7e1cb2f73d94ec19f`

```dockerfile
```

-	Layers:
	-	`sha256:5e58b6091d920b879110992b86bdb241ba668ecea1f4f5f6789309cd0a3b1201`  
		Last Modified: Tue, 14 Jan 2025 21:01:46 GMT  
		Size: 7.7 MB (7748823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7f2f816823fdda6d7259bb2d6e1971fa0211fe3022940e90152fef77424da2c`  
		Last Modified: Tue, 14 Jan 2025 21:00:44 GMT  
		Size: 7.6 KB (7628 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:13ca5071ec13ff460953798daad666106c46ca2b2eb3dc82c41682d9220b121f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.5 MB (135512750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97c330b4cb04586912db66a6e8c539ea43706561671df5d25bd4e9fd1b2b540a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fa42b2983a081afbe5b1653f1c107472f7b73564ae2a3f6a75d6b4702023cc0c`  
		Last Modified: Tue, 24 Dec 2024 21:33:19 GMT  
		Size: 48.8 MB (48771644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb6e11ed066e836dca02164f5f47ac1b39b5177eecb98796a4c515c972272aa`  
		Last Modified: Wed, 25 Dec 2024 11:45:56 GMT  
		Size: 23.5 MB (23458082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988cb190aa8a2556e06728d7eacbb8faf4d6ab4515c38db72b67645a5fa04f41`  
		Last Modified: Thu, 26 Dec 2024 05:08:26 GMT  
		Size: 63.3 MB (63283024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e6cdb193561d8db1e02ebdca6d4fd5bba968cf0d7acefa02489879d47cc42af7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 KB (7497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3a2fa930db5487c1c9ba556acfcb71b70adaa00d244a4c6a4b1e2d165897e59`

```dockerfile
```

-	Layers:
	-	`sha256:12f1d48387ad7f8a6179c3861c94ffeba6a882d0d84c44a1bd6f3bde5a79f2e4`  
		Last Modified: Wed, 25 Dec 2024 19:15:08 GMT  
		Size: 7.5 KB (7497 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:05b4402223200277f406f99fc728e47988998b5946ff282b1a2f2b55db8967f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.9 MB (147875066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07253a39195775999a73cfa312e0fa0c5fa1cb97359e3cf5503e14f02d7368a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:60b6379697eb1bdc0a74d6aa762f7f8e36a4a46031b019e2c7651c9723194c8b`  
		Last Modified: Tue, 14 Jan 2025 20:37:16 GMT  
		Size: 52.3 MB (52313137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b1d1b75ad07ec92cebf5f30e6612d80907cb5a7323fdef7921893e816a53be`  
		Last Modified: Tue, 14 Jan 2025 05:30:15 GMT  
		Size: 25.7 MB (25717439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395bc8910e96064c02227d340de0ac8d0234f64dd58802df0e9bd0891ad39050`  
		Last Modified: Tue, 14 Jan 2025 09:41:58 GMT  
		Size: 69.8 MB (69844490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a9d572ddeddf65e9c94b552da6a41ddb37bb717818328f59458a028ff53349cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7768145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee4e94cc9d33bf313cfc300eb9c016f08f8e9c4621491174b10461db746fb4d`

```dockerfile
```

-	Layers:
	-	`sha256:231c3fce7984cd3e3de5dd5d140d65478f0236395546611c454b0e0421150d73`  
		Last Modified: Tue, 14 Jan 2025 21:00:49 GMT  
		Size: 7.8 MB (7760453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b75b5ea659daa8cc266903efd448b1e7d046a092e5d48598c2331e3ca388f11a`  
		Last Modified: Tue, 14 Jan 2025 09:41:56 GMT  
		Size: 7.7 KB (7692 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:01b6a266cd6fd65e7a039960f70085758b1f10c86e44b46c93ffa9e73ee325e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134687819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb1540b555f37fc63897ba134fcbee1336fa05214ea02b4106dfdab7c6f806f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:21aa15808dc85b52fca40d40118565ddcd1b7ca60220d34328c38ccbc43c6ec1`  
		Last Modified: Tue, 14 Jan 2025 20:37:18 GMT  
		Size: 47.1 MB (47131782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba976031c967b4215afb8ec45dd7db082bb0d532971c83a1e9acaaa24c91981`  
		Last Modified: Tue, 14 Jan 2025 20:37:14 GMT  
		Size: 24.1 MB (24057754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41403619947915f481f99b2b28eecf7aa168ff32ff64e044d73a504ac7472026`  
		Last Modified: Tue, 14 Jan 2025 09:09:48 GMT  
		Size: 63.5 MB (63498283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:43431e3c05d52134bf14cd8ac647f7653c418285c8a57b43e8f82a2234a7b925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7759606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bfd98c17e6ccc3684e467d8da2f6c63e0b36a8d9ab0ca4eb7c19532af3ec683`

```dockerfile
```

-	Layers:
	-	`sha256:4ae3f8ca10fc0bf6d4dfde1d1729c21f2cc9b50d407dae9f46c637af3a9aefa5`  
		Last Modified: Tue, 14 Jan 2025 09:09:48 GMT  
		Size: 7.8 MB (7751951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9b1cc5cbaaa15e7112b9c3483f5229704660930af2da7216c6770c6969087d9`  
		Last Modified: Tue, 14 Jan 2025 09:09:47 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json
