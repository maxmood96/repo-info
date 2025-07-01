<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `spiped`

-	[`spiped:1`](#spiped1)
-	[`spiped:1-alpine`](#spiped1-alpine)
-	[`spiped:1.6`](#spiped16)
-	[`spiped:1.6-alpine`](#spiped16-alpine)
-	[`spiped:1.6.4`](#spiped164)
-	[`spiped:1.6.4-alpine`](#spiped164-alpine)
-	[`spiped:alpine`](#spipedalpine)
-	[`spiped:latest`](#spipedlatest)

## `spiped:1`

```console
$ docker pull spiped@sha256:b24d1da5cd7b4cbdc11e0999a5cfdb17100349f85bac746d0b714dc058713680
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

### `spiped:1` - linux; amd64

```console
$ docker pull spiped@sha256:f024235d7d4b7ac15321ac72ed498a8d434bbbd7f9d8d0d36be53da87df25e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37092878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:183163d0d944e9d983fc0fc54bd5157683aee8bdb8392721576a76094a6e0f87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1f8137b3ad170ffa7d770356846abbdf19e430595a9178087561b3ca455179`  
		Last Modified: Tue, 01 Jul 2025 02:25:12 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe485cb9d23519f0a164b99b25a0ad550cd91b74937b1b7dcd0b7610ba9e001`  
		Last Modified: Tue, 01 Jul 2025 02:25:12 GMT  
		Size: 2.4 MB (2402186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a98678754959fcab1fc3f78ed113c25c95e205f688b8790629b36b068c0ab60`  
		Last Modified: Tue, 01 Jul 2025 02:25:13 GMT  
		Size: 6.5 MB (6459008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d6a59c7311572be36dbd5e3c1ba0c513b1bcdbfc90e753fcd1c2ad63737bc1`  
		Last Modified: Tue, 01 Jul 2025 02:25:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd51d0b9ef1b733debf31dcce3f7403d689618a4968ab25a91ac0abfc797e50`  
		Last Modified: Tue, 01 Jul 2025 02:25:12 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:a9fc2fc0ec4038e840061044303009a791f0482a5d65111d1d143ce080efed32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3646833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e9d2bcb152456db5eddab8c13fce698c7aa3711e7c9ad18efd5ed2bdc2b37e`

```dockerfile
```

-	Layers:
	-	`sha256:719b075249a5c633a8c2f05fdcbb742ddbb973547d88e956d2202f5cc7d63d08`  
		Last Modified: Tue, 01 Jul 2025 04:04:24 GMT  
		Size: 3.6 MB (3631793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0db246d3f81fb31c55b5fa1f19a9f43aff5e58d219aa498b4bce180897338aa`  
		Last Modified: Tue, 01 Jul 2025 04:04:25 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v5

```console
$ docker pull spiped@sha256:edfa7b83c9f8ee095eb099239510d502de1e4e6fdf36282155f5d6b50dbdd558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32910050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548563c4dc7cc83e0bb8cd164d713e337e594f1ee43311f72ec06791c1d3e05b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1751241600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:57a7872a7ce75b95d171f720f215d4e72b887ae709c5c0b319f93f704bd71e07`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 25.8 MB (25762460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdeda97ad3e2bfeb1d3da9c2974ad5a2c99c3e677e7a0bbf83533aade7cd82a4`  
		Last Modified: Tue, 01 Jul 2025 06:06:13 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b015f9cf9720a5f7103f294ee6e0c72347162738b657d7cc364d82671218bad`  
		Last Modified: Tue, 01 Jul 2025 06:06:13 GMT  
		Size: 2.0 MB (1998255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb8faf9556c23d3f1c82805b010663e3d984f720f954bbc9386f772e1333680`  
		Last Modified: Tue, 01 Jul 2025 06:06:15 GMT  
		Size: 5.1 MB (5147794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513460512172493f117e7067379286e818ae86fe7ce944345d9ec2b66ef46cec`  
		Last Modified: Tue, 01 Jul 2025 06:06:15 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7002e87c88b3ff6535e6ef95670695376e770765466157c1157761dabaa3b6`  
		Last Modified: Tue, 01 Jul 2025 06:06:15 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:b9eb9338ad2bdd8479b7af1c056a5b0a3d9b454ce8435fba336c464655162def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3617772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf50c92b57e843e26b74b4fdcd2ff8554bf290c95380d75d463d16d21947405`

```dockerfile
```

-	Layers:
	-	`sha256:72f914733eb752d7149eb2889fe6aca3fff4dc02f26e3f54048256b46ca97511`  
		Last Modified: Tue, 01 Jul 2025 07:04:31 GMT  
		Size: 3.6 MB (3602631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4264d4f8cbf4f891ca4470ed5261eeec9bf119f8314058c131199c3c16aa5710`  
		Last Modified: Tue, 01 Jul 2025 07:04:32 GMT  
		Size: 15.1 KB (15141 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm variant v7

```console
$ docker pull spiped@sha256:a9056df29fc608ce23bc5dd89dc73f1a307dd9cc4568f5afd41b502d550f6df7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30685415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806c1815a756a80dea14be79bca020e3baed38d716388800957b574f0449bd3f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597af0c309b7db16d2c9db9f5a05c8fb33c035fb856d112618880dcde74569ce`  
		Last Modified: Tue, 01 Jul 2025 08:41:57 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d355dc9037959af02a5eac3c08c6bea5ff76da6c5f8b9ecd8b5238c4120e2561`  
		Last Modified: Tue, 01 Jul 2025 08:41:59 GMT  
		Size: 1.9 MB (1856403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c81922d2a12fdaad2eb54bb04cd3b0c2bac3a11a46ae194dee09b6fabe19ca`  
		Last Modified: Tue, 01 Jul 2025 08:41:59 GMT  
		Size: 4.9 MB (4888729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffddab181147161eeea726d48ba35bdda88798eb1f01088936e0a2e1c504b1be`  
		Last Modified: Tue, 01 Jul 2025 08:42:00 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519780b72af2f1f76b6735aef05a2e27b4b3b1afcadb20e866b52573b972d165`  
		Last Modified: Tue, 01 Jul 2025 08:42:00 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:56902fbbb55664d04fa71461186bd80218b54741ce42cbf8f7dd1698a2c1e028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3616956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583e68298827faedfb87b8d3a4aef23a19414d8182654f0f42034fa25265917a`

```dockerfile
```

-	Layers:
	-	`sha256:387fa230ca4e849a14728db4e945101e8b4dedfd68d0f1c541a58909d05930d1`  
		Last Modified: Tue, 01 Jul 2025 10:06:25 GMT  
		Size: 3.6 MB (3601814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5342bde067b2c60b808c0e0c2163b6a94861245f2b8087f6b10672b26b3646e`  
		Last Modified: Tue, 01 Jul 2025 10:06:26 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:cb209a48321512b849336cd10c6560447be53ad290df7a860442c5216b6b67fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35818465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1cc3d28c3a9914cdb656dcf5d520529b8c305813f97c784a58f33179287988c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231e64ee4b5f73f139be78cb871d48da14f4b1dde4442c3680881c8140fd7645`  
		Last Modified: Tue, 01 Jul 2025 06:32:43 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5dfd631fd81409727d860791d9b9b6301269985e8d02aa430d9148de3a91d2`  
		Last Modified: Tue, 01 Jul 2025 06:32:44 GMT  
		Size: 2.2 MB (2247442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed4b303d135a1395d15758dc19dc51eeca88061a24d212f84e90b95306f70f6`  
		Last Modified: Tue, 01 Jul 2025 06:32:44 GMT  
		Size: 5.5 MB (5491805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb383cde600396af7576eb1e1929316bdd09e7d23d3a03ab149e6613051d7850`  
		Last Modified: Tue, 01 Jul 2025 06:32:43 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46860d961f86decd94ae2c98a18d41491d7680a16f4331103c45c377079c003b`  
		Last Modified: Tue, 01 Jul 2025 06:32:43 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:dfb105bb1e8502c6b894305204bb0c3e029593546f920bfde0c951593da7032c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3618195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab67e54e4e0d74cf47c4f310ae3e3ebe8b87245e9b823d5c22662d1d0551662a`

```dockerfile
```

-	Layers:
	-	`sha256:62e6f1c4922e84d9260e8db09416c559a49eade9985d5c695e08eed1151ea958`  
		Last Modified: Tue, 01 Jul 2025 10:06:30 GMT  
		Size: 3.6 MB (3603021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:022d8c338da24b914cc498f53553ae887ea588c82f2745d039d832907c64d79a`  
		Last Modified: Tue, 01 Jul 2025 10:06:30 GMT  
		Size: 15.2 KB (15174 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; 386

```console
$ docker pull spiped@sha256:2ae45143c8464d1e8028c71a85b8288a9fad75dad6cbcd89a106a47626da2f76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37571424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80c6c1f290a11dff25ed2454b33e0e53277928fca72b3f15ba41f3508c9a1c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69af88f2dc291d20127149271d6671a3e59d0068cfd749eb55deb04f1d7459a`  
		Last Modified: Tue, 01 Jul 2025 02:23:54 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d494dd3202196292826fc985ae49292e9a71e7090c807a8869bdddaa46c45ec`  
		Last Modified: Tue, 01 Jul 2025 02:23:56 GMT  
		Size: 2.4 MB (2400597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932373df38b715de5ffb94d4b32f5c6e73c151c695d7ea13e767c5df0181f1be`  
		Last Modified: Tue, 01 Jul 2025 02:23:55 GMT  
		Size: 6.0 MB (5956855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a2e6bd84c3787c115d1ba31d3d2ac86927e93a0114500f401b294db73c3d4`  
		Last Modified: Tue, 01 Jul 2025 02:23:54 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78781d70ba16205c2f14a56c5935115ac76747396c7b5a4c30cb03d166242658`  
		Last Modified: Tue, 01 Jul 2025 02:23:54 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:6f611c7a53cb09390bbbdf6a188b72d6c09dc978c088e7417467483e92c69f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3640776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9f4c5278b0d61d117ca913ec12a122fda52178e19cf2e48371e477c5f9678f`

```dockerfile
```

-	Layers:
	-	`sha256:b0f54856e78d0c4a73990c9e74721953414afefe16ae3e08fb0e19e569dcea5f`  
		Last Modified: Tue, 01 Jul 2025 04:04:47 GMT  
		Size: 3.6 MB (3625772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:690b107191a61808dd88bc4ecea63f1c75046e3df06949dedfb3ce135527f916`  
		Last Modified: Tue, 01 Jul 2025 04:04:47 GMT  
		Size: 15.0 KB (15004 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; mips64le

```console
$ docker pull spiped@sha256:44a7ea572ee5ded3f2ceeb336ebf9f4b19e5c1721cd638675de7ea6a2365a05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36174227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e178694b114b2b500387f26b4a03570b5397e036a413c99d5252b6a40471ab8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ac3f61581c7f5755d8598b3a0857c417db0251b17c0e4e4f43a5fc0e24023524`  
		Last Modified: Tue, 10 Jun 2025 22:48:26 GMT  
		Size: 28.5 MB (28516717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bdd8e35937df27b0968ae8a23741b39da32971cd7b93300071387fb995566f`  
		Last Modified: Wed, 11 Jun 2025 12:58:47 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b256192f977eee0878018b3b88849faac10e38c96758feb6025fe97506622e3`  
		Last Modified: Wed, 11 Jun 2025 12:58:49 GMT  
		Size: 1.8 MB (1842270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8dbd97c4f500cedd0e46e05c6718376077029907325d8b425eaa1868dd89711`  
		Last Modified: Wed, 11 Jun 2025 12:58:50 GMT  
		Size: 5.8 MB (5813695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7e8d0a0cba57075c6e87aa5c196d709f79ddf523ee3af39a64ddf7bf645fc8`  
		Last Modified: Wed, 11 Jun 2025 12:58:47 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89390ae038a588fb2fbecb5444cc0f64955ddba34a4c65c9f0922cb722826aaa`  
		Last Modified: Wed, 11 Jun 2025 12:58:48 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:82053f23f3186d8684d3e7b169e166514810bb0b54ed29568f52924dfd2c8221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac7464c90ddadce8fd091e3ad3f97cdad7caaa5783f4f82d90906e9ab0d1e3e`

```dockerfile
```

-	Layers:
	-	`sha256:172483dac84d11e985c77a0c8e905873e020a5da1c9bee18ef7cb5331e5ada85`  
		Last Modified: Wed, 11 Jun 2025 16:04:35 GMT  
		Size: 14.9 KB (14897 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; ppc64le

```console
$ docker pull spiped@sha256:c58d64ee71cf3e45b328bd638a32df319eef1a0c887eb365b160a23f9b604f76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41099495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:699a5db20c84993b79136a82d34f8e553a2ca2f4c735955ab4740b51c612ce41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8daad143bb73c232d3d7b4fbf252f9ae53f1093169175862ea9fa1fb6be299`  
		Last Modified: Tue, 01 Jul 2025 04:52:54 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef84c7d520603a0c29edd02d1a5e67b201844dfaa547b487306f5705b768ad0`  
		Last Modified: Tue, 01 Jul 2025 04:52:54 GMT  
		Size: 2.6 MB (2583814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5cd14b2072612934415faa6e5ae5ff14fafdef4657cb483b0fe2376a6083078`  
		Last Modified: Tue, 01 Jul 2025 04:52:54 GMT  
		Size: 6.4 MB (6441321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5ce146e01f1fa63ab28a20ea208895273db520b7409532e81e69473944657e`  
		Last Modified: Tue, 01 Jul 2025 04:52:54 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d6dcf71250e742ba5b5120a558e381380c225c16ef14b9767678e24e321199`  
		Last Modified: Tue, 01 Jul 2025 04:52:54 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:df9764e3642fee766eff2fa2f3f045907c1c9de6e6f1e86798218afa16c8bb89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2377e9baa00a65147c12a752086b6d52a841d9ad74d1fbe55a2ce0edc92aa7`

```dockerfile
```

-	Layers:
	-	`sha256:d5fec28410667c567395f8e1644afd3e24d2755137be16f95a2ddb3ca7e9eb19`  
		Last Modified: Tue, 01 Jul 2025 07:04:47 GMT  
		Size: 3.6 MB (3617578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:213ed2703a3001a48e4784e291448cec9aa70dc2577cceb42ba758aac2b124b2`  
		Last Modified: Tue, 01 Jul 2025 07:04:48 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1` - linux; s390x

```console
$ docker pull spiped@sha256:4fd4fbd6bff6c2c5371378c01c1f88e356947691114480d2225f898b3000e017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34350835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d713089640911023d2144ecef46d942cd0fe841cb5f66c135b0ab5d52c8d021b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba9efd7d502df0495e76d2ad6412680292de681f1395b2821647a3d1e97ba4e`  
		Last Modified: Tue, 01 Jul 2025 08:32:33 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd21e11fd96caa46030e4fe7febc0e97471ec90db3dccdaaccd5c566b9404f1`  
		Last Modified: Tue, 01 Jul 2025 08:32:33 GMT  
		Size: 2.1 MB (2069107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cafac6ec34f9ef7c9c61c4d2278a341ae8a6a9c0ce9958ae15c674791211bc0`  
		Last Modified: Tue, 01 Jul 2025 08:32:34 GMT  
		Size: 5.4 MB (5392378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cda6f2703215be4a50214148313828abc4214a6af401c666d95b8446faf1917`  
		Last Modified: Tue, 01 Jul 2025 08:32:32 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf6c91c959f3941a785c6415b49de727da398596985451ce16e536a9618289e`  
		Last Modified: Tue, 01 Jul 2025 08:32:33 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1` - unknown; unknown

```console
$ docker pull spiped@sha256:525d3a4635569b93f7d1469dfc44704e94d745918e7bbd3c14e9c4c0d1283d84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ed18d0ce13dffef4b6a74771b1e94f6d4db70700ec1c1fa5b6485ccc5c962e`

```dockerfile
```

-	Layers:
	-	`sha256:74acb3ebe1d8b70825dcf67516fa625cc1d71a31147357bdc2611f05b46a4364`  
		Last Modified: Tue, 01 Jul 2025 10:06:41 GMT  
		Size: 3.6 MB (3617087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bc47448be78caae6aaa25230ee767f37502b180009094be68bb80479ff02d0f`  
		Last Modified: Tue, 01 Jul 2025 10:06:42 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:19cab0821b57af25c5e04f34834de199acba4d5a909887ce0f093a3200c51243
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
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

### `spiped:1-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:622df849c8857cb4538c0b252cf0b5e94d10a2b5af1222af4d54ce9016270049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83432e0291e920e3ef7ce3c7690aba0f53cf7250e10452315d154dccfe1df29f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114b63918a29534fea2f0cc34ca9459cf360301d5cc6e425a943254bd857bdfd`  
		Last Modified: Thu, 08 May 2025 23:05:03 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e3893b92c8e046b61bf235250bedbecb6eca134316b11bfb15c8cd1b337f3d`  
		Last Modified: Thu, 08 May 2025 23:05:03 GMT  
		Size: 7.9 KB (7914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc9dd67e9904979842828a3e75301a0c379da1bb45dc75cdc2bd6631a028a32`  
		Last Modified: Thu, 08 May 2025 23:05:03 GMT  
		Size: 107.6 KB (107617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff4e9164a4259b4803c6d934508ad8476b4416d7097f2cbe68db83e91a69ab0`  
		Last Modified: Thu, 08 May 2025 23:05:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3edaa59ccf7fe4418cc9f918ad66772163c1de22c3afd74314e1beee778bc5`  
		Last Modified: Thu, 08 May 2025 23:05:04 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:7ddf892427f7350fc633c5740ef8895f88d29ce3651ae3347a7ae8ed45e86fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc93f0f4d7a7ab59381d2ca94b5c48169a0eb0d534f6e06db48944a6a1cd9aef`

```dockerfile
```

-	Layers:
	-	`sha256:6dd8a7492609939d1b2f1cbf941b9c4607360ff5f25aaad3a379b6be4dde9aca`  
		Last Modified: Tue, 17 Jun 2025 23:31:45 GMT  
		Size: 79.8 KB (79822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0122061363abb1f4f3d5cb12184c88a3d21d651f9a1aeaf7e10ac5934d6919da`  
		Last Modified: Tue, 17 Jun 2025 23:31:46 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:022488b36873fd89f1a451ed66a2b4aed67a9ddb352d2bd608cf892376ae8972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3463148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33792a429e90fd9ea05a651fefc730ad65a8006e4c32639a335044afbd4c5952`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066b47e1325b9f6db29d2d135e8ce6b8fcbf90a8f37138d1f3356a294928613b`  
		Last Modified: Fri, 14 Feb 2025 23:04:54 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014f6178dbec0d9fa86b0b438929f32378f60d88338518b7952956c6aa1b5cb7`  
		Last Modified: Fri, 14 Feb 2025 23:04:54 GMT  
		Size: 7.9 KB (7917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc93d94752878827fd3532056a9d5c692ac38ff04c63b32f88673aa8964416a`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 89.1 KB (89120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc26ca6070e6d3cc776fbb063b850e250863b079bb9b4fedcf001b518f004387`  
		Last Modified: Fri, 09 May 2025 01:34:25 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb66a68852a74dbb6d6be32e7fd436e99a797bb5340892e84aacf1474567e04a`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:8cc6f6a6d91b5f59a3cfa4d8bef00dd3556faac0bcc6400c61260c9e8730e0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8d4b9bee6645579beaf8fbe1c143f10516e131664def6ca2c559cfa1f31504`

```dockerfile
```

-	Layers:
	-	`sha256:3263ee3077e76a9dbb13eecc31527a10d5efdefe3d39ec4c458f0e1132247531`  
		Last Modified: Wed, 02 Apr 2025 21:50:26 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:dee3984d26da4f0e8f36051324b3037dc9ccbe1860bc73d0c20cb5d580b67ec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3189083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14664fb61592fe16a4ad57c810d3b1649982058dd7505d05565d350c40e2ea78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8fb51fad1dc40f454b85c84a615197e58cde8fdc5f21b35dc45af3c97d1fa7`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef3321472ab9d21d883d24b575a54b890a3e93b9b0a5b44204d21656d78680a`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 7.9 KB (7928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa2395c1ed98837c525acd35fd9fdccb1a68a1b50574550c75f56789cdcefe6`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 81.7 KB (81650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1631d9b9eaabe691dc7301f342ee863beab1cba416bc55834b0dcd64d811d52e`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16aa8ceacc34b79b201841242c1d739910f64d43a16351ecd1b4e063785ae3d7`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:01fc29e009708c7ec4e299f0ab229f389ceb7f44379a0e50e9c4116c11ac1887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d3a8021f9021b79e00c3aa6168baba8e1d2d75d1c2107977f5af4eaa46e39a`

```dockerfile
```

-	Layers:
	-	`sha256:44cabd4b7cd6d156567d0a5c80d300c59411572e356ff5c2bf8ddb27a1f9f941`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 79.9 KB (79858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abc6d037c51e675c4900f1eaeb5150e1f382d37f0f1b0f592f7bae802181c645`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:9bf1fb1b6d22643c494712c0e64d1180ae0f262b6b8970f3e2d8dcef3fef6a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4102905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9c2bd1fb5fe20d7cbaf48186ea092dbc2d13b35d73505074e36eda2950836b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcfdf5e57fbe5c7d9308257021972c3c8049235b8418078c63b52659f3c141c`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860d1ac7e6f5ff9e4c32fa1aa64bcf81c200cb1e7e28b8d5ed59a0614cecead6`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 7.9 KB (7920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29683b13029a57b0b382b6e15838ae6d55e7fb4e17335eb9458398a3b28cc51c`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 100.6 KB (100575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcdf172b649e9fc88d25bf9587c92d962a199e6c7a0e1a98c2ec6c89c54aacb`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a43ba3519841070ae5d0384c94c52fc8d37791bfa6e9ad35b22b8b9702d29a`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:43a680d67479907610aad7509796ef596f5fed0d289448130c1196039d21ded2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b365f16aaf205dfc1b9640897e812784f27ed48fde6a42a374087e79452d0922`

```dockerfile
```

-	Layers:
	-	`sha256:4eb7794745d2b89ac646620f0f7c4237fc16799b36487de5b5f09a981ec8188f`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 79.9 KB (79878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9823c97e3177ff4bc824966f8e095cc5f8a3ab0acacb35eeeea76a628c98b570`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:10f7aa16af762acbfb63005c00877699fa29c2e4bb04d75d1d70ec20a60f5453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3593008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa790ea4f84c7bd9a039089ae50b44f58ea302f037ea74e3b405bc3febd96b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e7ff7711b41a9071a294c97e4058917e28c3c7e20059009e0b630880394156`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce2dc85c8b1ec7a6c1ad258c05589aa70dba5fe5290558cc0e4548d1bcdd5de`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 7.9 KB (7913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af8ae2ced3573d3e4de1a677b4b5a3c011895466b9c210fd74fe255cb8d77b8`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 120.1 KB (120090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa87e2679113a95903cfd2867ff588bcf12b0fd8ddfac21b77727f8b7d3d894`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22470fcb8710e32223fea8e79f0b28488b0ab51c65567241c529bd203b95215`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:766834152c333f40d598d1f36bd56d11f810d2e19ed86d7e91571b9367515fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8983e1e4860bdae956bb8f365e0bcc2f2cf38f76ce6566d65f6937140d1443`

```dockerfile
```

-	Layers:
	-	`sha256:0344d1265ed83fac16730c24d70471283f93d11c5749243cdcf7ba8e3cf80a76`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 79.8 KB (79797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de475a73cdee8c96006bf8d6c10118db82ed20c810abe06bd1dcb3b224bfaf98`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 14.3 KB (14265 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:88487ee5729022576bc8477226c823b846fcb546e116fd1817a9b49c7a8248df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3696294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e37765c7075b9c5e9f7aa70b2b311f8eb578373a5b127e41648ff035f02b2de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f29133aa5ac2dc7f7caf05bec17a3f120b130b0a9f8a931b87d42bda5e00ee7`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceed22f9dc598f4a83d2574a1236b9eb55845a886691ca27d260af8e52d0a5b8`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 7.9 KB (7921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e550c947cd96d7d5dbfd565fa3ae85434cb2481820d65ac92504416d056beea9`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 112.6 KB (112643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47cfc80ff9405d7424905e6aa74f541ec5830861bef1b1218605b7d66fcec7b9`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0e844805fa1d0d457d1513e5b9d92436e3ab8e65548a31fbbc18ed1c2c743b`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:fdca1b5f72932ee6bcfc55a37feb9c860f41b530efa43e63aec701932b3cf4da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 KB (92255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58422f604e757b9c7c12519d56f597a89ae27e12f2339cf2cc67b4b5a19bb384`

```dockerfile
```

-	Layers:
	-	`sha256:2df4c6cf5666abc03d36c3ff177b1360db4c2531a9cd9923b404e7ff491bec9b`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 77.9 KB (77905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7ad33b282085052031ca00d32c203a26ce45455daf796d327bb6cdbdcf3e8aa`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:d93e8574bb82dd81dafcf25f7625ed7818c3a0e31066bbddf64006b83d78aba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3459532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a635f525ddca22947829af6f197712b92c46682f40c9dbe63063aa381f9a9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a279c5ee271afcec6d3150e694efda4e5d36691f2d7ebe160636c0ab5a79b1ec`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015b70b993c8cc00dfe1e78ec875878062b451bd4ec2b326794c36444cb3105e`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 7.9 KB (7904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d040e2d542829d397e472ec2982c4857e357fe408f645da0693ef90321e2c7`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 98.8 KB (98804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0e579239e2446edd70320e6ec295380d239d0b2fb8045fbda0d7753c161f59`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f11cda2eddc9aaf6455435d16dfafc74f718d637e59cb8c549b1310659e0f68`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:6ef91094d879feac7520f82fdd946b0c798b74a1208a22482597eb403e08bd3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c9ad713acd2272c15e5bd4e3532ba9df6910776b9db0bb063b585453f134ab`

```dockerfile
```

-	Layers:
	-	`sha256:b046cc017c3f020547f0314366d83fb03c8803458406b56bdd3904750ccb915b`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 77.9 KB (77901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de0c335e4f12af3686646881008f04ba3bc438d3f15fbd38fbc3998d12514728`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:8e1cc9b73ed1eb178d6d22338fc661c8f3386b5d33086e11fca8483e38bc0123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9100e7b9db6a61a9d6818b301afcaf1e2753a632dba5e84dbdf9ea416bfe685b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408f712244d227bb17176b3c9833183d94d7e5078a0071c6bb815f7c6acd044b`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3d2b3d93cf3babc3c2c43519cfac5c89b009dddf9f6329ccb604067e1c25d0`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 7.9 KB (7919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924f34f1a30b83eb8fe0d105f78a3ddb08291d7062c11e0a807ca3576dd2e638`  
		Last Modified: Fri, 09 May 2025 01:34:29 GMT  
		Size: 96.9 KB (96901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa01324514a5afcdaa7ba2727d95863ff56033c4f01975371de7c453ccdf8e1`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3162a370a5d0aff74dea2a1ddb49f120b995ec42d4b29c7bcb3c2f10a91fc1`  
		Last Modified: Fri, 09 May 2025 01:34:29 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:97f9242d5c7292f0782ce10a5d3a0549df652a9380a4f408bf9ede75116a30aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e792a9515a7540fa01538367eccf186ff2dd8158a7dccadf4d37f635a3679c`

```dockerfile
```

-	Layers:
	-	`sha256:7c31c769211e50a701dc70ffd6261e2d0664c6f3b50fd444ad2665b22b1d6e5c`  
		Last Modified: Wed, 02 Apr 2025 21:52:19 GMT  
		Size: 77.9 KB (77871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4988863227d01a39c5e290493124efb4304413f32a12e6879ffda4c3a86afd0d`  
		Last Modified: Wed, 02 Apr 2025 21:52:20 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6`

```console
$ docker pull spiped@sha256:b24d1da5cd7b4cbdc11e0999a5cfdb17100349f85bac746d0b714dc058713680
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

### `spiped:1.6` - linux; amd64

```console
$ docker pull spiped@sha256:f024235d7d4b7ac15321ac72ed498a8d434bbbd7f9d8d0d36be53da87df25e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37092878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:183163d0d944e9d983fc0fc54bd5157683aee8bdb8392721576a76094a6e0f87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1f8137b3ad170ffa7d770356846abbdf19e430595a9178087561b3ca455179`  
		Last Modified: Tue, 01 Jul 2025 02:25:12 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe485cb9d23519f0a164b99b25a0ad550cd91b74937b1b7dcd0b7610ba9e001`  
		Last Modified: Tue, 01 Jul 2025 02:25:12 GMT  
		Size: 2.4 MB (2402186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a98678754959fcab1fc3f78ed113c25c95e205f688b8790629b36b068c0ab60`  
		Last Modified: Tue, 01 Jul 2025 02:25:13 GMT  
		Size: 6.5 MB (6459008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d6a59c7311572be36dbd5e3c1ba0c513b1bcdbfc90e753fcd1c2ad63737bc1`  
		Last Modified: Tue, 01 Jul 2025 02:25:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd51d0b9ef1b733debf31dcce3f7403d689618a4968ab25a91ac0abfc797e50`  
		Last Modified: Tue, 01 Jul 2025 02:25:12 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:a9fc2fc0ec4038e840061044303009a791f0482a5d65111d1d143ce080efed32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3646833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e9d2bcb152456db5eddab8c13fce698c7aa3711e7c9ad18efd5ed2bdc2b37e`

```dockerfile
```

-	Layers:
	-	`sha256:719b075249a5c633a8c2f05fdcbb742ddbb973547d88e956d2202f5cc7d63d08`  
		Last Modified: Tue, 01 Jul 2025 04:04:24 GMT  
		Size: 3.6 MB (3631793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0db246d3f81fb31c55b5fa1f19a9f43aff5e58d219aa498b4bce180897338aa`  
		Last Modified: Tue, 01 Jul 2025 04:04:25 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v5

```console
$ docker pull spiped@sha256:edfa7b83c9f8ee095eb099239510d502de1e4e6fdf36282155f5d6b50dbdd558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32910050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548563c4dc7cc83e0bb8cd164d713e337e594f1ee43311f72ec06791c1d3e05b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1751241600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:57a7872a7ce75b95d171f720f215d4e72b887ae709c5c0b319f93f704bd71e07`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 25.8 MB (25762460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdeda97ad3e2bfeb1d3da9c2974ad5a2c99c3e677e7a0bbf83533aade7cd82a4`  
		Last Modified: Tue, 01 Jul 2025 06:06:13 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b015f9cf9720a5f7103f294ee6e0c72347162738b657d7cc364d82671218bad`  
		Last Modified: Tue, 01 Jul 2025 06:06:13 GMT  
		Size: 2.0 MB (1998255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb8faf9556c23d3f1c82805b010663e3d984f720f954bbc9386f772e1333680`  
		Last Modified: Tue, 01 Jul 2025 06:06:15 GMT  
		Size: 5.1 MB (5147794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513460512172493f117e7067379286e818ae86fe7ce944345d9ec2b66ef46cec`  
		Last Modified: Tue, 01 Jul 2025 06:06:15 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7002e87c88b3ff6535e6ef95670695376e770765466157c1157761dabaa3b6`  
		Last Modified: Tue, 01 Jul 2025 06:06:15 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:b9eb9338ad2bdd8479b7af1c056a5b0a3d9b454ce8435fba336c464655162def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3617772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf50c92b57e843e26b74b4fdcd2ff8554bf290c95380d75d463d16d21947405`

```dockerfile
```

-	Layers:
	-	`sha256:72f914733eb752d7149eb2889fe6aca3fff4dc02f26e3f54048256b46ca97511`  
		Last Modified: Tue, 01 Jul 2025 07:04:31 GMT  
		Size: 3.6 MB (3602631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4264d4f8cbf4f891ca4470ed5261eeec9bf119f8314058c131199c3c16aa5710`  
		Last Modified: Tue, 01 Jul 2025 07:04:32 GMT  
		Size: 15.1 KB (15141 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm variant v7

```console
$ docker pull spiped@sha256:a9056df29fc608ce23bc5dd89dc73f1a307dd9cc4568f5afd41b502d550f6df7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30685415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806c1815a756a80dea14be79bca020e3baed38d716388800957b574f0449bd3f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597af0c309b7db16d2c9db9f5a05c8fb33c035fb856d112618880dcde74569ce`  
		Last Modified: Tue, 01 Jul 2025 08:41:57 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d355dc9037959af02a5eac3c08c6bea5ff76da6c5f8b9ecd8b5238c4120e2561`  
		Last Modified: Tue, 01 Jul 2025 08:41:59 GMT  
		Size: 1.9 MB (1856403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c81922d2a12fdaad2eb54bb04cd3b0c2bac3a11a46ae194dee09b6fabe19ca`  
		Last Modified: Tue, 01 Jul 2025 08:41:59 GMT  
		Size: 4.9 MB (4888729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffddab181147161eeea726d48ba35bdda88798eb1f01088936e0a2e1c504b1be`  
		Last Modified: Tue, 01 Jul 2025 08:42:00 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519780b72af2f1f76b6735aef05a2e27b4b3b1afcadb20e866b52573b972d165`  
		Last Modified: Tue, 01 Jul 2025 08:42:00 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:56902fbbb55664d04fa71461186bd80218b54741ce42cbf8f7dd1698a2c1e028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3616956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583e68298827faedfb87b8d3a4aef23a19414d8182654f0f42034fa25265917a`

```dockerfile
```

-	Layers:
	-	`sha256:387fa230ca4e849a14728db4e945101e8b4dedfd68d0f1c541a58909d05930d1`  
		Last Modified: Tue, 01 Jul 2025 10:06:25 GMT  
		Size: 3.6 MB (3601814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5342bde067b2c60b808c0e0c2163b6a94861245f2b8087f6b10672b26b3646e`  
		Last Modified: Tue, 01 Jul 2025 10:06:26 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:cb209a48321512b849336cd10c6560447be53ad290df7a860442c5216b6b67fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35818465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1cc3d28c3a9914cdb656dcf5d520529b8c305813f97c784a58f33179287988c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231e64ee4b5f73f139be78cb871d48da14f4b1dde4442c3680881c8140fd7645`  
		Last Modified: Tue, 01 Jul 2025 06:32:43 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5dfd631fd81409727d860791d9b9b6301269985e8d02aa430d9148de3a91d2`  
		Last Modified: Tue, 01 Jul 2025 06:32:44 GMT  
		Size: 2.2 MB (2247442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed4b303d135a1395d15758dc19dc51eeca88061a24d212f84e90b95306f70f6`  
		Last Modified: Tue, 01 Jul 2025 06:32:44 GMT  
		Size: 5.5 MB (5491805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb383cde600396af7576eb1e1929316bdd09e7d23d3a03ab149e6613051d7850`  
		Last Modified: Tue, 01 Jul 2025 06:32:43 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46860d961f86decd94ae2c98a18d41491d7680a16f4331103c45c377079c003b`  
		Last Modified: Tue, 01 Jul 2025 06:32:43 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:dfb105bb1e8502c6b894305204bb0c3e029593546f920bfde0c951593da7032c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3618195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab67e54e4e0d74cf47c4f310ae3e3ebe8b87245e9b823d5c22662d1d0551662a`

```dockerfile
```

-	Layers:
	-	`sha256:62e6f1c4922e84d9260e8db09416c559a49eade9985d5c695e08eed1151ea958`  
		Last Modified: Tue, 01 Jul 2025 10:06:30 GMT  
		Size: 3.6 MB (3603021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:022d8c338da24b914cc498f53553ae887ea588c82f2745d039d832907c64d79a`  
		Last Modified: Tue, 01 Jul 2025 10:06:30 GMT  
		Size: 15.2 KB (15174 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; 386

```console
$ docker pull spiped@sha256:2ae45143c8464d1e8028c71a85b8288a9fad75dad6cbcd89a106a47626da2f76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37571424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80c6c1f290a11dff25ed2454b33e0e53277928fca72b3f15ba41f3508c9a1c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69af88f2dc291d20127149271d6671a3e59d0068cfd749eb55deb04f1d7459a`  
		Last Modified: Tue, 01 Jul 2025 02:23:54 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d494dd3202196292826fc985ae49292e9a71e7090c807a8869bdddaa46c45ec`  
		Last Modified: Tue, 01 Jul 2025 02:23:56 GMT  
		Size: 2.4 MB (2400597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932373df38b715de5ffb94d4b32f5c6e73c151c695d7ea13e767c5df0181f1be`  
		Last Modified: Tue, 01 Jul 2025 02:23:55 GMT  
		Size: 6.0 MB (5956855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a2e6bd84c3787c115d1ba31d3d2ac86927e93a0114500f401b294db73c3d4`  
		Last Modified: Tue, 01 Jul 2025 02:23:54 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78781d70ba16205c2f14a56c5935115ac76747396c7b5a4c30cb03d166242658`  
		Last Modified: Tue, 01 Jul 2025 02:23:54 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:6f611c7a53cb09390bbbdf6a188b72d6c09dc978c088e7417467483e92c69f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3640776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9f4c5278b0d61d117ca913ec12a122fda52178e19cf2e48371e477c5f9678f`

```dockerfile
```

-	Layers:
	-	`sha256:b0f54856e78d0c4a73990c9e74721953414afefe16ae3e08fb0e19e569dcea5f`  
		Last Modified: Tue, 01 Jul 2025 04:04:47 GMT  
		Size: 3.6 MB (3625772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:690b107191a61808dd88bc4ecea63f1c75046e3df06949dedfb3ce135527f916`  
		Last Modified: Tue, 01 Jul 2025 04:04:47 GMT  
		Size: 15.0 KB (15004 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; mips64le

```console
$ docker pull spiped@sha256:44a7ea572ee5ded3f2ceeb336ebf9f4b19e5c1721cd638675de7ea6a2365a05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36174227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e178694b114b2b500387f26b4a03570b5397e036a413c99d5252b6a40471ab8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ac3f61581c7f5755d8598b3a0857c417db0251b17c0e4e4f43a5fc0e24023524`  
		Last Modified: Tue, 10 Jun 2025 22:48:26 GMT  
		Size: 28.5 MB (28516717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bdd8e35937df27b0968ae8a23741b39da32971cd7b93300071387fb995566f`  
		Last Modified: Wed, 11 Jun 2025 12:58:47 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b256192f977eee0878018b3b88849faac10e38c96758feb6025fe97506622e3`  
		Last Modified: Wed, 11 Jun 2025 12:58:49 GMT  
		Size: 1.8 MB (1842270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8dbd97c4f500cedd0e46e05c6718376077029907325d8b425eaa1868dd89711`  
		Last Modified: Wed, 11 Jun 2025 12:58:50 GMT  
		Size: 5.8 MB (5813695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7e8d0a0cba57075c6e87aa5c196d709f79ddf523ee3af39a64ddf7bf645fc8`  
		Last Modified: Wed, 11 Jun 2025 12:58:47 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89390ae038a588fb2fbecb5444cc0f64955ddba34a4c65c9f0922cb722826aaa`  
		Last Modified: Wed, 11 Jun 2025 12:58:48 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:82053f23f3186d8684d3e7b169e166514810bb0b54ed29568f52924dfd2c8221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac7464c90ddadce8fd091e3ad3f97cdad7caaa5783f4f82d90906e9ab0d1e3e`

```dockerfile
```

-	Layers:
	-	`sha256:172483dac84d11e985c77a0c8e905873e020a5da1c9bee18ef7cb5331e5ada85`  
		Last Modified: Wed, 11 Jun 2025 16:04:35 GMT  
		Size: 14.9 KB (14897 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; ppc64le

```console
$ docker pull spiped@sha256:c58d64ee71cf3e45b328bd638a32df319eef1a0c887eb365b160a23f9b604f76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41099495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:699a5db20c84993b79136a82d34f8e553a2ca2f4c735955ab4740b51c612ce41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8daad143bb73c232d3d7b4fbf252f9ae53f1093169175862ea9fa1fb6be299`  
		Last Modified: Tue, 01 Jul 2025 04:52:54 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef84c7d520603a0c29edd02d1a5e67b201844dfaa547b487306f5705b768ad0`  
		Last Modified: Tue, 01 Jul 2025 04:52:54 GMT  
		Size: 2.6 MB (2583814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5cd14b2072612934415faa6e5ae5ff14fafdef4657cb483b0fe2376a6083078`  
		Last Modified: Tue, 01 Jul 2025 04:52:54 GMT  
		Size: 6.4 MB (6441321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5ce146e01f1fa63ab28a20ea208895273db520b7409532e81e69473944657e`  
		Last Modified: Tue, 01 Jul 2025 04:52:54 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d6dcf71250e742ba5b5120a558e381380c225c16ef14b9767678e24e321199`  
		Last Modified: Tue, 01 Jul 2025 04:52:54 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:df9764e3642fee766eff2fa2f3f045907c1c9de6e6f1e86798218afa16c8bb89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2377e9baa00a65147c12a752086b6d52a841d9ad74d1fbe55a2ce0edc92aa7`

```dockerfile
```

-	Layers:
	-	`sha256:d5fec28410667c567395f8e1644afd3e24d2755137be16f95a2ddb3ca7e9eb19`  
		Last Modified: Tue, 01 Jul 2025 07:04:47 GMT  
		Size: 3.6 MB (3617578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:213ed2703a3001a48e4784e291448cec9aa70dc2577cceb42ba758aac2b124b2`  
		Last Modified: Tue, 01 Jul 2025 07:04:48 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6` - linux; s390x

```console
$ docker pull spiped@sha256:4fd4fbd6bff6c2c5371378c01c1f88e356947691114480d2225f898b3000e017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34350835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d713089640911023d2144ecef46d942cd0fe841cb5f66c135b0ab5d52c8d021b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba9efd7d502df0495e76d2ad6412680292de681f1395b2821647a3d1e97ba4e`  
		Last Modified: Tue, 01 Jul 2025 08:32:33 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd21e11fd96caa46030e4fe7febc0e97471ec90db3dccdaaccd5c566b9404f1`  
		Last Modified: Tue, 01 Jul 2025 08:32:33 GMT  
		Size: 2.1 MB (2069107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cafac6ec34f9ef7c9c61c4d2278a341ae8a6a9c0ce9958ae15c674791211bc0`  
		Last Modified: Tue, 01 Jul 2025 08:32:34 GMT  
		Size: 5.4 MB (5392378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cda6f2703215be4a50214148313828abc4214a6af401c666d95b8446faf1917`  
		Last Modified: Tue, 01 Jul 2025 08:32:32 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf6c91c959f3941a785c6415b49de727da398596985451ce16e536a9618289e`  
		Last Modified: Tue, 01 Jul 2025 08:32:33 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6` - unknown; unknown

```console
$ docker pull spiped@sha256:525d3a4635569b93f7d1469dfc44704e94d745918e7bbd3c14e9c4c0d1283d84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ed18d0ce13dffef4b6a74771b1e94f6d4db70700ec1c1fa5b6485ccc5c962e`

```dockerfile
```

-	Layers:
	-	`sha256:74acb3ebe1d8b70825dcf67516fa625cc1d71a31147357bdc2611f05b46a4364`  
		Last Modified: Tue, 01 Jul 2025 10:06:41 GMT  
		Size: 3.6 MB (3617087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bc47448be78caae6aaa25230ee767f37502b180009094be68bb80479ff02d0f`  
		Last Modified: Tue, 01 Jul 2025 10:06:42 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6-alpine`

```console
$ docker pull spiped@sha256:19cab0821b57af25c5e04f34834de199acba4d5a909887ce0f093a3200c51243
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
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

### `spiped:1.6-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:622df849c8857cb4538c0b252cf0b5e94d10a2b5af1222af4d54ce9016270049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83432e0291e920e3ef7ce3c7690aba0f53cf7250e10452315d154dccfe1df29f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114b63918a29534fea2f0cc34ca9459cf360301d5cc6e425a943254bd857bdfd`  
		Last Modified: Thu, 08 May 2025 23:05:03 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e3893b92c8e046b61bf235250bedbecb6eca134316b11bfb15c8cd1b337f3d`  
		Last Modified: Thu, 08 May 2025 23:05:03 GMT  
		Size: 7.9 KB (7914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc9dd67e9904979842828a3e75301a0c379da1bb45dc75cdc2bd6631a028a32`  
		Last Modified: Thu, 08 May 2025 23:05:03 GMT  
		Size: 107.6 KB (107617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff4e9164a4259b4803c6d934508ad8476b4416d7097f2cbe68db83e91a69ab0`  
		Last Modified: Thu, 08 May 2025 23:05:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3edaa59ccf7fe4418cc9f918ad66772163c1de22c3afd74314e1beee778bc5`  
		Last Modified: Thu, 08 May 2025 23:05:04 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:7ddf892427f7350fc633c5740ef8895f88d29ce3651ae3347a7ae8ed45e86fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc93f0f4d7a7ab59381d2ca94b5c48169a0eb0d534f6e06db48944a6a1cd9aef`

```dockerfile
```

-	Layers:
	-	`sha256:6dd8a7492609939d1b2f1cbf941b9c4607360ff5f25aaad3a379b6be4dde9aca`  
		Last Modified: Tue, 17 Jun 2025 23:31:45 GMT  
		Size: 79.8 KB (79822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0122061363abb1f4f3d5cb12184c88a3d21d651f9a1aeaf7e10ac5934d6919da`  
		Last Modified: Tue, 17 Jun 2025 23:31:46 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:022488b36873fd89f1a451ed66a2b4aed67a9ddb352d2bd608cf892376ae8972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3463148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33792a429e90fd9ea05a651fefc730ad65a8006e4c32639a335044afbd4c5952`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066b47e1325b9f6db29d2d135e8ce6b8fcbf90a8f37138d1f3356a294928613b`  
		Last Modified: Fri, 14 Feb 2025 23:04:54 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014f6178dbec0d9fa86b0b438929f32378f60d88338518b7952956c6aa1b5cb7`  
		Last Modified: Fri, 14 Feb 2025 23:04:54 GMT  
		Size: 7.9 KB (7917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc93d94752878827fd3532056a9d5c692ac38ff04c63b32f88673aa8964416a`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 89.1 KB (89120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc26ca6070e6d3cc776fbb063b850e250863b079bb9b4fedcf001b518f004387`  
		Last Modified: Fri, 09 May 2025 01:34:25 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb66a68852a74dbb6d6be32e7fd436e99a797bb5340892e84aacf1474567e04a`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:8cc6f6a6d91b5f59a3cfa4d8bef00dd3556faac0bcc6400c61260c9e8730e0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8d4b9bee6645579beaf8fbe1c143f10516e131664def6ca2c559cfa1f31504`

```dockerfile
```

-	Layers:
	-	`sha256:3263ee3077e76a9dbb13eecc31527a10d5efdefe3d39ec4c458f0e1132247531`  
		Last Modified: Wed, 02 Apr 2025 21:50:26 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:dee3984d26da4f0e8f36051324b3037dc9ccbe1860bc73d0c20cb5d580b67ec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3189083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14664fb61592fe16a4ad57c810d3b1649982058dd7505d05565d350c40e2ea78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8fb51fad1dc40f454b85c84a615197e58cde8fdc5f21b35dc45af3c97d1fa7`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef3321472ab9d21d883d24b575a54b890a3e93b9b0a5b44204d21656d78680a`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 7.9 KB (7928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa2395c1ed98837c525acd35fd9fdccb1a68a1b50574550c75f56789cdcefe6`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 81.7 KB (81650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1631d9b9eaabe691dc7301f342ee863beab1cba416bc55834b0dcd64d811d52e`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16aa8ceacc34b79b201841242c1d739910f64d43a16351ecd1b4e063785ae3d7`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:01fc29e009708c7ec4e299f0ab229f389ceb7f44379a0e50e9c4116c11ac1887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d3a8021f9021b79e00c3aa6168baba8e1d2d75d1c2107977f5af4eaa46e39a`

```dockerfile
```

-	Layers:
	-	`sha256:44cabd4b7cd6d156567d0a5c80d300c59411572e356ff5c2bf8ddb27a1f9f941`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 79.9 KB (79858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abc6d037c51e675c4900f1eaeb5150e1f382d37f0f1b0f592f7bae802181c645`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:9bf1fb1b6d22643c494712c0e64d1180ae0f262b6b8970f3e2d8dcef3fef6a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4102905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9c2bd1fb5fe20d7cbaf48186ea092dbc2d13b35d73505074e36eda2950836b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcfdf5e57fbe5c7d9308257021972c3c8049235b8418078c63b52659f3c141c`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860d1ac7e6f5ff9e4c32fa1aa64bcf81c200cb1e7e28b8d5ed59a0614cecead6`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 7.9 KB (7920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29683b13029a57b0b382b6e15838ae6d55e7fb4e17335eb9458398a3b28cc51c`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 100.6 KB (100575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcdf172b649e9fc88d25bf9587c92d962a199e6c7a0e1a98c2ec6c89c54aacb`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a43ba3519841070ae5d0384c94c52fc8d37791bfa6e9ad35b22b8b9702d29a`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:43a680d67479907610aad7509796ef596f5fed0d289448130c1196039d21ded2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b365f16aaf205dfc1b9640897e812784f27ed48fde6a42a374087e79452d0922`

```dockerfile
```

-	Layers:
	-	`sha256:4eb7794745d2b89ac646620f0f7c4237fc16799b36487de5b5f09a981ec8188f`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 79.9 KB (79878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9823c97e3177ff4bc824966f8e095cc5f8a3ab0acacb35eeeea76a628c98b570`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; 386

```console
$ docker pull spiped@sha256:10f7aa16af762acbfb63005c00877699fa29c2e4bb04d75d1d70ec20a60f5453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3593008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa790ea4f84c7bd9a039089ae50b44f58ea302f037ea74e3b405bc3febd96b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e7ff7711b41a9071a294c97e4058917e28c3c7e20059009e0b630880394156`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce2dc85c8b1ec7a6c1ad258c05589aa70dba5fe5290558cc0e4548d1bcdd5de`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 7.9 KB (7913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af8ae2ced3573d3e4de1a677b4b5a3c011895466b9c210fd74fe255cb8d77b8`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 120.1 KB (120090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa87e2679113a95903cfd2867ff588bcf12b0fd8ddfac21b77727f8b7d3d894`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22470fcb8710e32223fea8e79f0b28488b0ab51c65567241c529bd203b95215`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:766834152c333f40d598d1f36bd56d11f810d2e19ed86d7e91571b9367515fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8983e1e4860bdae956bb8f365e0bcc2f2cf38f76ce6566d65f6937140d1443`

```dockerfile
```

-	Layers:
	-	`sha256:0344d1265ed83fac16730c24d70471283f93d11c5749243cdcf7ba8e3cf80a76`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 79.8 KB (79797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de475a73cdee8c96006bf8d6c10118db82ed20c810abe06bd1dcb3b224bfaf98`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 14.3 KB (14265 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:88487ee5729022576bc8477226c823b846fcb546e116fd1817a9b49c7a8248df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3696294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e37765c7075b9c5e9f7aa70b2b311f8eb578373a5b127e41648ff035f02b2de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f29133aa5ac2dc7f7caf05bec17a3f120b130b0a9f8a931b87d42bda5e00ee7`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceed22f9dc598f4a83d2574a1236b9eb55845a886691ca27d260af8e52d0a5b8`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 7.9 KB (7921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e550c947cd96d7d5dbfd565fa3ae85434cb2481820d65ac92504416d056beea9`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 112.6 KB (112643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47cfc80ff9405d7424905e6aa74f541ec5830861bef1b1218605b7d66fcec7b9`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0e844805fa1d0d457d1513e5b9d92436e3ab8e65548a31fbbc18ed1c2c743b`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:fdca1b5f72932ee6bcfc55a37feb9c860f41b530efa43e63aec701932b3cf4da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 KB (92255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58422f604e757b9c7c12519d56f597a89ae27e12f2339cf2cc67b4b5a19bb384`

```dockerfile
```

-	Layers:
	-	`sha256:2df4c6cf5666abc03d36c3ff177b1360db4c2531a9cd9923b404e7ff491bec9b`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 77.9 KB (77905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7ad33b282085052031ca00d32c203a26ce45455daf796d327bb6cdbdcf3e8aa`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:d93e8574bb82dd81dafcf25f7625ed7818c3a0e31066bbddf64006b83d78aba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3459532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a635f525ddca22947829af6f197712b92c46682f40c9dbe63063aa381f9a9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a279c5ee271afcec6d3150e694efda4e5d36691f2d7ebe160636c0ab5a79b1ec`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015b70b993c8cc00dfe1e78ec875878062b451bd4ec2b326794c36444cb3105e`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 7.9 KB (7904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d040e2d542829d397e472ec2982c4857e357fe408f645da0693ef90321e2c7`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 98.8 KB (98804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0e579239e2446edd70320e6ec295380d239d0b2fb8045fbda0d7753c161f59`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f11cda2eddc9aaf6455435d16dfafc74f718d637e59cb8c549b1310659e0f68`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:6ef91094d879feac7520f82fdd946b0c798b74a1208a22482597eb403e08bd3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c9ad713acd2272c15e5bd4e3532ba9df6910776b9db0bb063b585453f134ab`

```dockerfile
```

-	Layers:
	-	`sha256:b046cc017c3f020547f0314366d83fb03c8803458406b56bdd3904750ccb915b`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 77.9 KB (77901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de0c335e4f12af3686646881008f04ba3bc438d3f15fbd38fbc3998d12514728`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:8e1cc9b73ed1eb178d6d22338fc661c8f3386b5d33086e11fca8483e38bc0123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9100e7b9db6a61a9d6818b301afcaf1e2753a632dba5e84dbdf9ea416bfe685b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408f712244d227bb17176b3c9833183d94d7e5078a0071c6bb815f7c6acd044b`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3d2b3d93cf3babc3c2c43519cfac5c89b009dddf9f6329ccb604067e1c25d0`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 7.9 KB (7919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924f34f1a30b83eb8fe0d105f78a3ddb08291d7062c11e0a807ca3576dd2e638`  
		Last Modified: Fri, 09 May 2025 01:34:29 GMT  
		Size: 96.9 KB (96901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa01324514a5afcdaa7ba2727d95863ff56033c4f01975371de7c453ccdf8e1`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3162a370a5d0aff74dea2a1ddb49f120b995ec42d4b29c7bcb3c2f10a91fc1`  
		Last Modified: Fri, 09 May 2025 01:34:29 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:97f9242d5c7292f0782ce10a5d3a0549df652a9380a4f408bf9ede75116a30aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e792a9515a7540fa01538367eccf186ff2dd8158a7dccadf4d37f635a3679c`

```dockerfile
```

-	Layers:
	-	`sha256:7c31c769211e50a701dc70ffd6261e2d0664c6f3b50fd444ad2665b22b1d6e5c`  
		Last Modified: Wed, 02 Apr 2025 21:52:19 GMT  
		Size: 77.9 KB (77871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4988863227d01a39c5e290493124efb4304413f32a12e6879ffda4c3a86afd0d`  
		Last Modified: Wed, 02 Apr 2025 21:52:20 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.4`

```console
$ docker pull spiped@sha256:b24d1da5cd7b4cbdc11e0999a5cfdb17100349f85bac746d0b714dc058713680
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

### `spiped:1.6.4` - linux; amd64

```console
$ docker pull spiped@sha256:f024235d7d4b7ac15321ac72ed498a8d434bbbd7f9d8d0d36be53da87df25e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37092878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:183163d0d944e9d983fc0fc54bd5157683aee8bdb8392721576a76094a6e0f87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1f8137b3ad170ffa7d770356846abbdf19e430595a9178087561b3ca455179`  
		Last Modified: Tue, 01 Jul 2025 02:25:12 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe485cb9d23519f0a164b99b25a0ad550cd91b74937b1b7dcd0b7610ba9e001`  
		Last Modified: Tue, 01 Jul 2025 02:25:12 GMT  
		Size: 2.4 MB (2402186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a98678754959fcab1fc3f78ed113c25c95e205f688b8790629b36b068c0ab60`  
		Last Modified: Tue, 01 Jul 2025 02:25:13 GMT  
		Size: 6.5 MB (6459008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d6a59c7311572be36dbd5e3c1ba0c513b1bcdbfc90e753fcd1c2ad63737bc1`  
		Last Modified: Tue, 01 Jul 2025 02:25:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd51d0b9ef1b733debf31dcce3f7403d689618a4968ab25a91ac0abfc797e50`  
		Last Modified: Tue, 01 Jul 2025 02:25:12 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:a9fc2fc0ec4038e840061044303009a791f0482a5d65111d1d143ce080efed32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3646833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e9d2bcb152456db5eddab8c13fce698c7aa3711e7c9ad18efd5ed2bdc2b37e`

```dockerfile
```

-	Layers:
	-	`sha256:719b075249a5c633a8c2f05fdcbb742ddbb973547d88e956d2202f5cc7d63d08`  
		Last Modified: Tue, 01 Jul 2025 04:04:24 GMT  
		Size: 3.6 MB (3631793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0db246d3f81fb31c55b5fa1f19a9f43aff5e58d219aa498b4bce180897338aa`  
		Last Modified: Tue, 01 Jul 2025 04:04:25 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm variant v5

```console
$ docker pull spiped@sha256:edfa7b83c9f8ee095eb099239510d502de1e4e6fdf36282155f5d6b50dbdd558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32910050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548563c4dc7cc83e0bb8cd164d713e337e594f1ee43311f72ec06791c1d3e05b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1751241600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:57a7872a7ce75b95d171f720f215d4e72b887ae709c5c0b319f93f704bd71e07`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 25.8 MB (25762460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdeda97ad3e2bfeb1d3da9c2974ad5a2c99c3e677e7a0bbf83533aade7cd82a4`  
		Last Modified: Tue, 01 Jul 2025 06:06:13 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b015f9cf9720a5f7103f294ee6e0c72347162738b657d7cc364d82671218bad`  
		Last Modified: Tue, 01 Jul 2025 06:06:13 GMT  
		Size: 2.0 MB (1998255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb8faf9556c23d3f1c82805b010663e3d984f720f954bbc9386f772e1333680`  
		Last Modified: Tue, 01 Jul 2025 06:06:15 GMT  
		Size: 5.1 MB (5147794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513460512172493f117e7067379286e818ae86fe7ce944345d9ec2b66ef46cec`  
		Last Modified: Tue, 01 Jul 2025 06:06:15 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7002e87c88b3ff6535e6ef95670695376e770765466157c1157761dabaa3b6`  
		Last Modified: Tue, 01 Jul 2025 06:06:15 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:b9eb9338ad2bdd8479b7af1c056a5b0a3d9b454ce8435fba336c464655162def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3617772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf50c92b57e843e26b74b4fdcd2ff8554bf290c95380d75d463d16d21947405`

```dockerfile
```

-	Layers:
	-	`sha256:72f914733eb752d7149eb2889fe6aca3fff4dc02f26e3f54048256b46ca97511`  
		Last Modified: Tue, 01 Jul 2025 07:04:31 GMT  
		Size: 3.6 MB (3602631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4264d4f8cbf4f891ca4470ed5261eeec9bf119f8314058c131199c3c16aa5710`  
		Last Modified: Tue, 01 Jul 2025 07:04:32 GMT  
		Size: 15.1 KB (15141 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm variant v7

```console
$ docker pull spiped@sha256:a9056df29fc608ce23bc5dd89dc73f1a307dd9cc4568f5afd41b502d550f6df7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30685415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806c1815a756a80dea14be79bca020e3baed38d716388800957b574f0449bd3f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597af0c309b7db16d2c9db9f5a05c8fb33c035fb856d112618880dcde74569ce`  
		Last Modified: Tue, 01 Jul 2025 08:41:57 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d355dc9037959af02a5eac3c08c6bea5ff76da6c5f8b9ecd8b5238c4120e2561`  
		Last Modified: Tue, 01 Jul 2025 08:41:59 GMT  
		Size: 1.9 MB (1856403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c81922d2a12fdaad2eb54bb04cd3b0c2bac3a11a46ae194dee09b6fabe19ca`  
		Last Modified: Tue, 01 Jul 2025 08:41:59 GMT  
		Size: 4.9 MB (4888729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffddab181147161eeea726d48ba35bdda88798eb1f01088936e0a2e1c504b1be`  
		Last Modified: Tue, 01 Jul 2025 08:42:00 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519780b72af2f1f76b6735aef05a2e27b4b3b1afcadb20e866b52573b972d165`  
		Last Modified: Tue, 01 Jul 2025 08:42:00 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:56902fbbb55664d04fa71461186bd80218b54741ce42cbf8f7dd1698a2c1e028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3616956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583e68298827faedfb87b8d3a4aef23a19414d8182654f0f42034fa25265917a`

```dockerfile
```

-	Layers:
	-	`sha256:387fa230ca4e849a14728db4e945101e8b4dedfd68d0f1c541a58909d05930d1`  
		Last Modified: Tue, 01 Jul 2025 10:06:25 GMT  
		Size: 3.6 MB (3601814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5342bde067b2c60b808c0e0c2163b6a94861245f2b8087f6b10672b26b3646e`  
		Last Modified: Tue, 01 Jul 2025 10:06:26 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:cb209a48321512b849336cd10c6560447be53ad290df7a860442c5216b6b67fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35818465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1cc3d28c3a9914cdb656dcf5d520529b8c305813f97c784a58f33179287988c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231e64ee4b5f73f139be78cb871d48da14f4b1dde4442c3680881c8140fd7645`  
		Last Modified: Tue, 01 Jul 2025 06:32:43 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5dfd631fd81409727d860791d9b9b6301269985e8d02aa430d9148de3a91d2`  
		Last Modified: Tue, 01 Jul 2025 06:32:44 GMT  
		Size: 2.2 MB (2247442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed4b303d135a1395d15758dc19dc51eeca88061a24d212f84e90b95306f70f6`  
		Last Modified: Tue, 01 Jul 2025 06:32:44 GMT  
		Size: 5.5 MB (5491805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb383cde600396af7576eb1e1929316bdd09e7d23d3a03ab149e6613051d7850`  
		Last Modified: Tue, 01 Jul 2025 06:32:43 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46860d961f86decd94ae2c98a18d41491d7680a16f4331103c45c377079c003b`  
		Last Modified: Tue, 01 Jul 2025 06:32:43 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:dfb105bb1e8502c6b894305204bb0c3e029593546f920bfde0c951593da7032c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3618195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab67e54e4e0d74cf47c4f310ae3e3ebe8b87245e9b823d5c22662d1d0551662a`

```dockerfile
```

-	Layers:
	-	`sha256:62e6f1c4922e84d9260e8db09416c559a49eade9985d5c695e08eed1151ea958`  
		Last Modified: Tue, 01 Jul 2025 10:06:30 GMT  
		Size: 3.6 MB (3603021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:022d8c338da24b914cc498f53553ae887ea588c82f2745d039d832907c64d79a`  
		Last Modified: Tue, 01 Jul 2025 10:06:30 GMT  
		Size: 15.2 KB (15174 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; 386

```console
$ docker pull spiped@sha256:2ae45143c8464d1e8028c71a85b8288a9fad75dad6cbcd89a106a47626da2f76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37571424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80c6c1f290a11dff25ed2454b33e0e53277928fca72b3f15ba41f3508c9a1c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69af88f2dc291d20127149271d6671a3e59d0068cfd749eb55deb04f1d7459a`  
		Last Modified: Tue, 01 Jul 2025 02:23:54 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d494dd3202196292826fc985ae49292e9a71e7090c807a8869bdddaa46c45ec`  
		Last Modified: Tue, 01 Jul 2025 02:23:56 GMT  
		Size: 2.4 MB (2400597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932373df38b715de5ffb94d4b32f5c6e73c151c695d7ea13e767c5df0181f1be`  
		Last Modified: Tue, 01 Jul 2025 02:23:55 GMT  
		Size: 6.0 MB (5956855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a2e6bd84c3787c115d1ba31d3d2ac86927e93a0114500f401b294db73c3d4`  
		Last Modified: Tue, 01 Jul 2025 02:23:54 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78781d70ba16205c2f14a56c5935115ac76747396c7b5a4c30cb03d166242658`  
		Last Modified: Tue, 01 Jul 2025 02:23:54 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:6f611c7a53cb09390bbbdf6a188b72d6c09dc978c088e7417467483e92c69f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3640776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9f4c5278b0d61d117ca913ec12a122fda52178e19cf2e48371e477c5f9678f`

```dockerfile
```

-	Layers:
	-	`sha256:b0f54856e78d0c4a73990c9e74721953414afefe16ae3e08fb0e19e569dcea5f`  
		Last Modified: Tue, 01 Jul 2025 04:04:47 GMT  
		Size: 3.6 MB (3625772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:690b107191a61808dd88bc4ecea63f1c75046e3df06949dedfb3ce135527f916`  
		Last Modified: Tue, 01 Jul 2025 04:04:47 GMT  
		Size: 15.0 KB (15004 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; mips64le

```console
$ docker pull spiped@sha256:44a7ea572ee5ded3f2ceeb336ebf9f4b19e5c1721cd638675de7ea6a2365a05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36174227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e178694b114b2b500387f26b4a03570b5397e036a413c99d5252b6a40471ab8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ac3f61581c7f5755d8598b3a0857c417db0251b17c0e4e4f43a5fc0e24023524`  
		Last Modified: Tue, 10 Jun 2025 22:48:26 GMT  
		Size: 28.5 MB (28516717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bdd8e35937df27b0968ae8a23741b39da32971cd7b93300071387fb995566f`  
		Last Modified: Wed, 11 Jun 2025 12:58:47 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b256192f977eee0878018b3b88849faac10e38c96758feb6025fe97506622e3`  
		Last Modified: Wed, 11 Jun 2025 12:58:49 GMT  
		Size: 1.8 MB (1842270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8dbd97c4f500cedd0e46e05c6718376077029907325d8b425eaa1868dd89711`  
		Last Modified: Wed, 11 Jun 2025 12:58:50 GMT  
		Size: 5.8 MB (5813695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7e8d0a0cba57075c6e87aa5c196d709f79ddf523ee3af39a64ddf7bf645fc8`  
		Last Modified: Wed, 11 Jun 2025 12:58:47 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89390ae038a588fb2fbecb5444cc0f64955ddba34a4c65c9f0922cb722826aaa`  
		Last Modified: Wed, 11 Jun 2025 12:58:48 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:82053f23f3186d8684d3e7b169e166514810bb0b54ed29568f52924dfd2c8221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac7464c90ddadce8fd091e3ad3f97cdad7caaa5783f4f82d90906e9ab0d1e3e`

```dockerfile
```

-	Layers:
	-	`sha256:172483dac84d11e985c77a0c8e905873e020a5da1c9bee18ef7cb5331e5ada85`  
		Last Modified: Wed, 11 Jun 2025 16:04:35 GMT  
		Size: 14.9 KB (14897 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; ppc64le

```console
$ docker pull spiped@sha256:c58d64ee71cf3e45b328bd638a32df319eef1a0c887eb365b160a23f9b604f76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41099495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:699a5db20c84993b79136a82d34f8e553a2ca2f4c735955ab4740b51c612ce41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8daad143bb73c232d3d7b4fbf252f9ae53f1093169175862ea9fa1fb6be299`  
		Last Modified: Tue, 01 Jul 2025 04:52:54 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef84c7d520603a0c29edd02d1a5e67b201844dfaa547b487306f5705b768ad0`  
		Last Modified: Tue, 01 Jul 2025 04:52:54 GMT  
		Size: 2.6 MB (2583814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5cd14b2072612934415faa6e5ae5ff14fafdef4657cb483b0fe2376a6083078`  
		Last Modified: Tue, 01 Jul 2025 04:52:54 GMT  
		Size: 6.4 MB (6441321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5ce146e01f1fa63ab28a20ea208895273db520b7409532e81e69473944657e`  
		Last Modified: Tue, 01 Jul 2025 04:52:54 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d6dcf71250e742ba5b5120a558e381380c225c16ef14b9767678e24e321199`  
		Last Modified: Tue, 01 Jul 2025 04:52:54 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:df9764e3642fee766eff2fa2f3f045907c1c9de6e6f1e86798218afa16c8bb89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2377e9baa00a65147c12a752086b6d52a841d9ad74d1fbe55a2ce0edc92aa7`

```dockerfile
```

-	Layers:
	-	`sha256:d5fec28410667c567395f8e1644afd3e24d2755137be16f95a2ddb3ca7e9eb19`  
		Last Modified: Tue, 01 Jul 2025 07:04:47 GMT  
		Size: 3.6 MB (3617578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:213ed2703a3001a48e4784e291448cec9aa70dc2577cceb42ba758aac2b124b2`  
		Last Modified: Tue, 01 Jul 2025 07:04:48 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4` - linux; s390x

```console
$ docker pull spiped@sha256:4fd4fbd6bff6c2c5371378c01c1f88e356947691114480d2225f898b3000e017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34350835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d713089640911023d2144ecef46d942cd0fe841cb5f66c135b0ab5d52c8d021b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba9efd7d502df0495e76d2ad6412680292de681f1395b2821647a3d1e97ba4e`  
		Last Modified: Tue, 01 Jul 2025 08:32:33 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd21e11fd96caa46030e4fe7febc0e97471ec90db3dccdaaccd5c566b9404f1`  
		Last Modified: Tue, 01 Jul 2025 08:32:33 GMT  
		Size: 2.1 MB (2069107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cafac6ec34f9ef7c9c61c4d2278a341ae8a6a9c0ce9958ae15c674791211bc0`  
		Last Modified: Tue, 01 Jul 2025 08:32:34 GMT  
		Size: 5.4 MB (5392378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cda6f2703215be4a50214148313828abc4214a6af401c666d95b8446faf1917`  
		Last Modified: Tue, 01 Jul 2025 08:32:32 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf6c91c959f3941a785c6415b49de727da398596985451ce16e536a9618289e`  
		Last Modified: Tue, 01 Jul 2025 08:32:33 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4` - unknown; unknown

```console
$ docker pull spiped@sha256:525d3a4635569b93f7d1469dfc44704e94d745918e7bbd3c14e9c4c0d1283d84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ed18d0ce13dffef4b6a74771b1e94f6d4db70700ec1c1fa5b6485ccc5c962e`

```dockerfile
```

-	Layers:
	-	`sha256:74acb3ebe1d8b70825dcf67516fa625cc1d71a31147357bdc2611f05b46a4364`  
		Last Modified: Tue, 01 Jul 2025 10:06:41 GMT  
		Size: 3.6 MB (3617087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bc47448be78caae6aaa25230ee767f37502b180009094be68bb80479ff02d0f`  
		Last Modified: Tue, 01 Jul 2025 10:06:42 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:1.6.4-alpine`

```console
$ docker pull spiped@sha256:19cab0821b57af25c5e04f34834de199acba4d5a909887ce0f093a3200c51243
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
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

### `spiped:1.6.4-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:622df849c8857cb4538c0b252cf0b5e94d10a2b5af1222af4d54ce9016270049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83432e0291e920e3ef7ce3c7690aba0f53cf7250e10452315d154dccfe1df29f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114b63918a29534fea2f0cc34ca9459cf360301d5cc6e425a943254bd857bdfd`  
		Last Modified: Thu, 08 May 2025 23:05:03 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e3893b92c8e046b61bf235250bedbecb6eca134316b11bfb15c8cd1b337f3d`  
		Last Modified: Thu, 08 May 2025 23:05:03 GMT  
		Size: 7.9 KB (7914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc9dd67e9904979842828a3e75301a0c379da1bb45dc75cdc2bd6631a028a32`  
		Last Modified: Thu, 08 May 2025 23:05:03 GMT  
		Size: 107.6 KB (107617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff4e9164a4259b4803c6d934508ad8476b4416d7097f2cbe68db83e91a69ab0`  
		Last Modified: Thu, 08 May 2025 23:05:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3edaa59ccf7fe4418cc9f918ad66772163c1de22c3afd74314e1beee778bc5`  
		Last Modified: Thu, 08 May 2025 23:05:04 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:7ddf892427f7350fc633c5740ef8895f88d29ce3651ae3347a7ae8ed45e86fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc93f0f4d7a7ab59381d2ca94b5c48169a0eb0d534f6e06db48944a6a1cd9aef`

```dockerfile
```

-	Layers:
	-	`sha256:6dd8a7492609939d1b2f1cbf941b9c4607360ff5f25aaad3a379b6be4dde9aca`  
		Last Modified: Tue, 17 Jun 2025 23:31:45 GMT  
		Size: 79.8 KB (79822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0122061363abb1f4f3d5cb12184c88a3d21d651f9a1aeaf7e10ac5934d6919da`  
		Last Modified: Tue, 17 Jun 2025 23:31:46 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:022488b36873fd89f1a451ed66a2b4aed67a9ddb352d2bd608cf892376ae8972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3463148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33792a429e90fd9ea05a651fefc730ad65a8006e4c32639a335044afbd4c5952`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066b47e1325b9f6db29d2d135e8ce6b8fcbf90a8f37138d1f3356a294928613b`  
		Last Modified: Fri, 14 Feb 2025 23:04:54 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014f6178dbec0d9fa86b0b438929f32378f60d88338518b7952956c6aa1b5cb7`  
		Last Modified: Fri, 14 Feb 2025 23:04:54 GMT  
		Size: 7.9 KB (7917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc93d94752878827fd3532056a9d5c692ac38ff04c63b32f88673aa8964416a`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 89.1 KB (89120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc26ca6070e6d3cc776fbb063b850e250863b079bb9b4fedcf001b518f004387`  
		Last Modified: Fri, 09 May 2025 01:34:25 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb66a68852a74dbb6d6be32e7fd436e99a797bb5340892e84aacf1474567e04a`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:8cc6f6a6d91b5f59a3cfa4d8bef00dd3556faac0bcc6400c61260c9e8730e0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8d4b9bee6645579beaf8fbe1c143f10516e131664def6ca2c559cfa1f31504`

```dockerfile
```

-	Layers:
	-	`sha256:3263ee3077e76a9dbb13eecc31527a10d5efdefe3d39ec4c458f0e1132247531`  
		Last Modified: Wed, 02 Apr 2025 21:50:26 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:dee3984d26da4f0e8f36051324b3037dc9ccbe1860bc73d0c20cb5d580b67ec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3189083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14664fb61592fe16a4ad57c810d3b1649982058dd7505d05565d350c40e2ea78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8fb51fad1dc40f454b85c84a615197e58cde8fdc5f21b35dc45af3c97d1fa7`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef3321472ab9d21d883d24b575a54b890a3e93b9b0a5b44204d21656d78680a`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 7.9 KB (7928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa2395c1ed98837c525acd35fd9fdccb1a68a1b50574550c75f56789cdcefe6`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 81.7 KB (81650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1631d9b9eaabe691dc7301f342ee863beab1cba416bc55834b0dcd64d811d52e`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16aa8ceacc34b79b201841242c1d739910f64d43a16351ecd1b4e063785ae3d7`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:01fc29e009708c7ec4e299f0ab229f389ceb7f44379a0e50e9c4116c11ac1887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d3a8021f9021b79e00c3aa6168baba8e1d2d75d1c2107977f5af4eaa46e39a`

```dockerfile
```

-	Layers:
	-	`sha256:44cabd4b7cd6d156567d0a5c80d300c59411572e356ff5c2bf8ddb27a1f9f941`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 79.9 KB (79858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abc6d037c51e675c4900f1eaeb5150e1f382d37f0f1b0f592f7bae802181c645`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:9bf1fb1b6d22643c494712c0e64d1180ae0f262b6b8970f3e2d8dcef3fef6a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4102905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9c2bd1fb5fe20d7cbaf48186ea092dbc2d13b35d73505074e36eda2950836b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcfdf5e57fbe5c7d9308257021972c3c8049235b8418078c63b52659f3c141c`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860d1ac7e6f5ff9e4c32fa1aa64bcf81c200cb1e7e28b8d5ed59a0614cecead6`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 7.9 KB (7920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29683b13029a57b0b382b6e15838ae6d55e7fb4e17335eb9458398a3b28cc51c`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 100.6 KB (100575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcdf172b649e9fc88d25bf9587c92d962a199e6c7a0e1a98c2ec6c89c54aacb`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a43ba3519841070ae5d0384c94c52fc8d37791bfa6e9ad35b22b8b9702d29a`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:43a680d67479907610aad7509796ef596f5fed0d289448130c1196039d21ded2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b365f16aaf205dfc1b9640897e812784f27ed48fde6a42a374087e79452d0922`

```dockerfile
```

-	Layers:
	-	`sha256:4eb7794745d2b89ac646620f0f7c4237fc16799b36487de5b5f09a981ec8188f`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 79.9 KB (79878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9823c97e3177ff4bc824966f8e095cc5f8a3ab0acacb35eeeea76a628c98b570`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; 386

```console
$ docker pull spiped@sha256:10f7aa16af762acbfb63005c00877699fa29c2e4bb04d75d1d70ec20a60f5453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3593008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa790ea4f84c7bd9a039089ae50b44f58ea302f037ea74e3b405bc3febd96b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e7ff7711b41a9071a294c97e4058917e28c3c7e20059009e0b630880394156`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce2dc85c8b1ec7a6c1ad258c05589aa70dba5fe5290558cc0e4548d1bcdd5de`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 7.9 KB (7913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af8ae2ced3573d3e4de1a677b4b5a3c011895466b9c210fd74fe255cb8d77b8`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 120.1 KB (120090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa87e2679113a95903cfd2867ff588bcf12b0fd8ddfac21b77727f8b7d3d894`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22470fcb8710e32223fea8e79f0b28488b0ab51c65567241c529bd203b95215`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:766834152c333f40d598d1f36bd56d11f810d2e19ed86d7e91571b9367515fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8983e1e4860bdae956bb8f365e0bcc2f2cf38f76ce6566d65f6937140d1443`

```dockerfile
```

-	Layers:
	-	`sha256:0344d1265ed83fac16730c24d70471283f93d11c5749243cdcf7ba8e3cf80a76`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 79.8 KB (79797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de475a73cdee8c96006bf8d6c10118db82ed20c810abe06bd1dcb3b224bfaf98`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 14.3 KB (14265 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:88487ee5729022576bc8477226c823b846fcb546e116fd1817a9b49c7a8248df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3696294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e37765c7075b9c5e9f7aa70b2b311f8eb578373a5b127e41648ff035f02b2de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f29133aa5ac2dc7f7caf05bec17a3f120b130b0a9f8a931b87d42bda5e00ee7`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceed22f9dc598f4a83d2574a1236b9eb55845a886691ca27d260af8e52d0a5b8`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 7.9 KB (7921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e550c947cd96d7d5dbfd565fa3ae85434cb2481820d65ac92504416d056beea9`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 112.6 KB (112643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47cfc80ff9405d7424905e6aa74f541ec5830861bef1b1218605b7d66fcec7b9`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0e844805fa1d0d457d1513e5b9d92436e3ab8e65548a31fbbc18ed1c2c743b`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:fdca1b5f72932ee6bcfc55a37feb9c860f41b530efa43e63aec701932b3cf4da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 KB (92255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58422f604e757b9c7c12519d56f597a89ae27e12f2339cf2cc67b4b5a19bb384`

```dockerfile
```

-	Layers:
	-	`sha256:2df4c6cf5666abc03d36c3ff177b1360db4c2531a9cd9923b404e7ff491bec9b`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 77.9 KB (77905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7ad33b282085052031ca00d32c203a26ce45455daf796d327bb6cdbdcf3e8aa`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:d93e8574bb82dd81dafcf25f7625ed7818c3a0e31066bbddf64006b83d78aba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3459532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a635f525ddca22947829af6f197712b92c46682f40c9dbe63063aa381f9a9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a279c5ee271afcec6d3150e694efda4e5d36691f2d7ebe160636c0ab5a79b1ec`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015b70b993c8cc00dfe1e78ec875878062b451bd4ec2b326794c36444cb3105e`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 7.9 KB (7904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d040e2d542829d397e472ec2982c4857e357fe408f645da0693ef90321e2c7`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 98.8 KB (98804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0e579239e2446edd70320e6ec295380d239d0b2fb8045fbda0d7753c161f59`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f11cda2eddc9aaf6455435d16dfafc74f718d637e59cb8c549b1310659e0f68`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:6ef91094d879feac7520f82fdd946b0c798b74a1208a22482597eb403e08bd3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c9ad713acd2272c15e5bd4e3532ba9df6910776b9db0bb063b585453f134ab`

```dockerfile
```

-	Layers:
	-	`sha256:b046cc017c3f020547f0314366d83fb03c8803458406b56bdd3904750ccb915b`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 77.9 KB (77901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de0c335e4f12af3686646881008f04ba3bc438d3f15fbd38fbc3998d12514728`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1.6.4-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:8e1cc9b73ed1eb178d6d22338fc661c8f3386b5d33086e11fca8483e38bc0123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9100e7b9db6a61a9d6818b301afcaf1e2753a632dba5e84dbdf9ea416bfe685b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408f712244d227bb17176b3c9833183d94d7e5078a0071c6bb815f7c6acd044b`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3d2b3d93cf3babc3c2c43519cfac5c89b009dddf9f6329ccb604067e1c25d0`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 7.9 KB (7919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924f34f1a30b83eb8fe0d105f78a3ddb08291d7062c11e0a807ca3576dd2e638`  
		Last Modified: Fri, 09 May 2025 01:34:29 GMT  
		Size: 96.9 KB (96901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa01324514a5afcdaa7ba2727d95863ff56033c4f01975371de7c453ccdf8e1`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3162a370a5d0aff74dea2a1ddb49f120b995ec42d4b29c7bcb3c2f10a91fc1`  
		Last Modified: Fri, 09 May 2025 01:34:29 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1.6.4-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:97f9242d5c7292f0782ce10a5d3a0549df652a9380a4f408bf9ede75116a30aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e792a9515a7540fa01538367eccf186ff2dd8158a7dccadf4d37f635a3679c`

```dockerfile
```

-	Layers:
	-	`sha256:7c31c769211e50a701dc70ffd6261e2d0664c6f3b50fd444ad2665b22b1d6e5c`  
		Last Modified: Wed, 02 Apr 2025 21:52:19 GMT  
		Size: 77.9 KB (77871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4988863227d01a39c5e290493124efb4304413f32a12e6879ffda4c3a86afd0d`  
		Last Modified: Wed, 02 Apr 2025 21:52:20 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:alpine`

```console
$ docker pull spiped@sha256:19cab0821b57af25c5e04f34834de199acba4d5a909887ce0f093a3200c51243
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
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

### `spiped:alpine` - linux; amd64

```console
$ docker pull spiped@sha256:622df849c8857cb4538c0b252cf0b5e94d10a2b5af1222af4d54ce9016270049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83432e0291e920e3ef7ce3c7690aba0f53cf7250e10452315d154dccfe1df29f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114b63918a29534fea2f0cc34ca9459cf360301d5cc6e425a943254bd857bdfd`  
		Last Modified: Thu, 08 May 2025 23:05:03 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e3893b92c8e046b61bf235250bedbecb6eca134316b11bfb15c8cd1b337f3d`  
		Last Modified: Thu, 08 May 2025 23:05:03 GMT  
		Size: 7.9 KB (7914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc9dd67e9904979842828a3e75301a0c379da1bb45dc75cdc2bd6631a028a32`  
		Last Modified: Thu, 08 May 2025 23:05:03 GMT  
		Size: 107.6 KB (107617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff4e9164a4259b4803c6d934508ad8476b4416d7097f2cbe68db83e91a69ab0`  
		Last Modified: Thu, 08 May 2025 23:05:03 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3edaa59ccf7fe4418cc9f918ad66772163c1de22c3afd74314e1beee778bc5`  
		Last Modified: Thu, 08 May 2025 23:05:04 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:7ddf892427f7350fc633c5740ef8895f88d29ce3651ae3347a7ae8ed45e86fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc93f0f4d7a7ab59381d2ca94b5c48169a0eb0d534f6e06db48944a6a1cd9aef`

```dockerfile
```

-	Layers:
	-	`sha256:6dd8a7492609939d1b2f1cbf941b9c4607360ff5f25aaad3a379b6be4dde9aca`  
		Last Modified: Tue, 17 Jun 2025 23:31:45 GMT  
		Size: 79.8 KB (79822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0122061363abb1f4f3d5cb12184c88a3d21d651f9a1aeaf7e10ac5934d6919da`  
		Last Modified: Tue, 17 Jun 2025 23:31:46 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:022488b36873fd89f1a451ed66a2b4aed67a9ddb352d2bd608cf892376ae8972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3463148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33792a429e90fd9ea05a651fefc730ad65a8006e4c32639a335044afbd4c5952`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066b47e1325b9f6db29d2d135e8ce6b8fcbf90a8f37138d1f3356a294928613b`  
		Last Modified: Fri, 14 Feb 2025 23:04:54 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014f6178dbec0d9fa86b0b438929f32378f60d88338518b7952956c6aa1b5cb7`  
		Last Modified: Fri, 14 Feb 2025 23:04:54 GMT  
		Size: 7.9 KB (7917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc93d94752878827fd3532056a9d5c692ac38ff04c63b32f88673aa8964416a`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 89.1 KB (89120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc26ca6070e6d3cc776fbb063b850e250863b079bb9b4fedcf001b518f004387`  
		Last Modified: Fri, 09 May 2025 01:34:25 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb66a68852a74dbb6d6be32e7fd436e99a797bb5340892e84aacf1474567e04a`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:8cc6f6a6d91b5f59a3cfa4d8bef00dd3556faac0bcc6400c61260c9e8730e0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8d4b9bee6645579beaf8fbe1c143f10516e131664def6ca2c559cfa1f31504`

```dockerfile
```

-	Layers:
	-	`sha256:3263ee3077e76a9dbb13eecc31527a10d5efdefe3d39ec4c458f0e1132247531`  
		Last Modified: Wed, 02 Apr 2025 21:50:26 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:dee3984d26da4f0e8f36051324b3037dc9ccbe1860bc73d0c20cb5d580b67ec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3189083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14664fb61592fe16a4ad57c810d3b1649982058dd7505d05565d350c40e2ea78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8fb51fad1dc40f454b85c84a615197e58cde8fdc5f21b35dc45af3c97d1fa7`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef3321472ab9d21d883d24b575a54b890a3e93b9b0a5b44204d21656d78680a`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 7.9 KB (7928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa2395c1ed98837c525acd35fd9fdccb1a68a1b50574550c75f56789cdcefe6`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 81.7 KB (81650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1631d9b9eaabe691dc7301f342ee863beab1cba416bc55834b0dcd64d811d52e`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16aa8ceacc34b79b201841242c1d739910f64d43a16351ecd1b4e063785ae3d7`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:01fc29e009708c7ec4e299f0ab229f389ceb7f44379a0e50e9c4116c11ac1887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d3a8021f9021b79e00c3aa6168baba8e1d2d75d1c2107977f5af4eaa46e39a`

```dockerfile
```

-	Layers:
	-	`sha256:44cabd4b7cd6d156567d0a5c80d300c59411572e356ff5c2bf8ddb27a1f9f941`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 79.9 KB (79858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abc6d037c51e675c4900f1eaeb5150e1f382d37f0f1b0f592f7bae802181c645`  
		Last Modified: Wed, 02 Apr 2025 21:51:13 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:9bf1fb1b6d22643c494712c0e64d1180ae0f262b6b8970f3e2d8dcef3fef6a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4102905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9c2bd1fb5fe20d7cbaf48186ea092dbc2d13b35d73505074e36eda2950836b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcfdf5e57fbe5c7d9308257021972c3c8049235b8418078c63b52659f3c141c`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860d1ac7e6f5ff9e4c32fa1aa64bcf81c200cb1e7e28b8d5ed59a0614cecead6`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 7.9 KB (7920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29683b13029a57b0b382b6e15838ae6d55e7fb4e17335eb9458398a3b28cc51c`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 100.6 KB (100575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcdf172b649e9fc88d25bf9587c92d962a199e6c7a0e1a98c2ec6c89c54aacb`  
		Last Modified: Fri, 09 May 2025 01:34:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a43ba3519841070ae5d0384c94c52fc8d37791bfa6e9ad35b22b8b9702d29a`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:43a680d67479907610aad7509796ef596f5fed0d289448130c1196039d21ded2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b365f16aaf205dfc1b9640897e812784f27ed48fde6a42a374087e79452d0922`

```dockerfile
```

-	Layers:
	-	`sha256:4eb7794745d2b89ac646620f0f7c4237fc16799b36487de5b5f09a981ec8188f`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 79.9 KB (79878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9823c97e3177ff4bc824966f8e095cc5f8a3ab0acacb35eeeea76a628c98b570`  
		Last Modified: Wed, 02 Apr 2025 21:51:30 GMT  
		Size: 14.4 KB (14436 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:10f7aa16af762acbfb63005c00877699fa29c2e4bb04d75d1d70ec20a60f5453
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3593008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa790ea4f84c7bd9a039089ae50b44f58ea302f037ea74e3b405bc3febd96b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e7ff7711b41a9071a294c97e4058917e28c3c7e20059009e0b630880394156`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce2dc85c8b1ec7a6c1ad258c05589aa70dba5fe5290558cc0e4548d1bcdd5de`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 7.9 KB (7913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af8ae2ced3573d3e4de1a677b4b5a3c011895466b9c210fd74fe255cb8d77b8`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 120.1 KB (120090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa87e2679113a95903cfd2867ff588bcf12b0fd8ddfac21b77727f8b7d3d894`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22470fcb8710e32223fea8e79f0b28488b0ab51c65567241c529bd203b95215`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:766834152c333f40d598d1f36bd56d11f810d2e19ed86d7e91571b9367515fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8983e1e4860bdae956bb8f365e0bcc2f2cf38f76ce6566d65f6937140d1443`

```dockerfile
```

-	Layers:
	-	`sha256:0344d1265ed83fac16730c24d70471283f93d11c5749243cdcf7ba8e3cf80a76`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 79.8 KB (79797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de475a73cdee8c96006bf8d6c10118db82ed20c810abe06bd1dcb3b224bfaf98`  
		Last Modified: Wed, 02 Apr 2025 21:51:03 GMT  
		Size: 14.3 KB (14265 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:88487ee5729022576bc8477226c823b846fcb546e116fd1817a9b49c7a8248df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3696294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e37765c7075b9c5e9f7aa70b2b311f8eb578373a5b127e41648ff035f02b2de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f29133aa5ac2dc7f7caf05bec17a3f120b130b0a9f8a931b87d42bda5e00ee7`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceed22f9dc598f4a83d2574a1236b9eb55845a886691ca27d260af8e52d0a5b8`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 7.9 KB (7921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e550c947cd96d7d5dbfd565fa3ae85434cb2481820d65ac92504416d056beea9`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 112.6 KB (112643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47cfc80ff9405d7424905e6aa74f541ec5830861bef1b1218605b7d66fcec7b9`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0e844805fa1d0d457d1513e5b9d92436e3ab8e65548a31fbbc18ed1c2c743b`  
		Last Modified: Fri, 09 May 2025 01:34:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:fdca1b5f72932ee6bcfc55a37feb9c860f41b530efa43e63aec701932b3cf4da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 KB (92255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58422f604e757b9c7c12519d56f597a89ae27e12f2339cf2cc67b4b5a19bb384`

```dockerfile
```

-	Layers:
	-	`sha256:2df4c6cf5666abc03d36c3ff177b1360db4c2531a9cd9923b404e7ff491bec9b`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 77.9 KB (77905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7ad33b282085052031ca00d32c203a26ce45455daf796d327bb6cdbdcf3e8aa`  
		Last Modified: Wed, 02 Apr 2025 21:53:15 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:d93e8574bb82dd81dafcf25f7625ed7818c3a0e31066bbddf64006b83d78aba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3459532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a635f525ddca22947829af6f197712b92c46682f40c9dbe63063aa381f9a9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a279c5ee271afcec6d3150e694efda4e5d36691f2d7ebe160636c0ab5a79b1ec`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015b70b993c8cc00dfe1e78ec875878062b451bd4ec2b326794c36444cb3105e`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 7.9 KB (7904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d040e2d542829d397e472ec2982c4857e357fe408f645da0693ef90321e2c7`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 98.8 KB (98804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0e579239e2446edd70320e6ec295380d239d0b2fb8045fbda0d7753c161f59`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f11cda2eddc9aaf6455435d16dfafc74f718d637e59cb8c549b1310659e0f68`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:6ef91094d879feac7520f82fdd946b0c798b74a1208a22482597eb403e08bd3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c9ad713acd2272c15e5bd4e3532ba9df6910776b9db0bb063b585453f134ab`

```dockerfile
```

-	Layers:
	-	`sha256:b046cc017c3f020547f0314366d83fb03c8803458406b56bdd3904750ccb915b`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 77.9 KB (77901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de0c335e4f12af3686646881008f04ba3bc438d3f15fbd38fbc3998d12514728`  
		Last Modified: Wed, 02 Apr 2025 21:53:03 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:8e1cc9b73ed1eb178d6d22338fc661c8f3386b5d33086e11fca8483e38bc0123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9100e7b9db6a61a9d6818b301afcaf1e2753a632dba5e84dbdf9ea416bfe685b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN apk add --no-cache libssl3 # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408f712244d227bb17176b3c9833183d94d7e5078a0071c6bb815f7c6acd044b`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3d2b3d93cf3babc3c2c43519cfac5c89b009dddf9f6329ccb604067e1c25d0`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 7.9 KB (7919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924f34f1a30b83eb8fe0d105f78a3ddb08291d7062c11e0a807ca3576dd2e638`  
		Last Modified: Fri, 09 May 2025 01:34:29 GMT  
		Size: 96.9 KB (96901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa01324514a5afcdaa7ba2727d95863ff56033c4f01975371de7c453ccdf8e1`  
		Last Modified: Fri, 09 May 2025 01:34:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3162a370a5d0aff74dea2a1ddb49f120b995ec42d4b29c7bcb3c2f10a91fc1`  
		Last Modified: Fri, 09 May 2025 01:34:29 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:97f9242d5c7292f0782ce10a5d3a0549df652a9380a4f408bf9ede75116a30aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e792a9515a7540fa01538367eccf186ff2dd8158a7dccadf4d37f635a3679c`

```dockerfile
```

-	Layers:
	-	`sha256:7c31c769211e50a701dc70ffd6261e2d0664c6f3b50fd444ad2665b22b1d6e5c`  
		Last Modified: Wed, 02 Apr 2025 21:52:19 GMT  
		Size: 77.9 KB (77871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4988863227d01a39c5e290493124efb4304413f32a12e6879ffda4c3a86afd0d`  
		Last Modified: Wed, 02 Apr 2025 21:52:20 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

## `spiped:latest`

```console
$ docker pull spiped@sha256:b24d1da5cd7b4cbdc11e0999a5cfdb17100349f85bac746d0b714dc058713680
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

### `spiped:latest` - linux; amd64

```console
$ docker pull spiped@sha256:f024235d7d4b7ac15321ac72ed498a8d434bbbd7f9d8d0d36be53da87df25e28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37092878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:183163d0d944e9d983fc0fc54bd5157683aee8bdb8392721576a76094a6e0f87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1f8137b3ad170ffa7d770356846abbdf19e430595a9178087561b3ca455179`  
		Last Modified: Tue, 01 Jul 2025 02:25:12 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe485cb9d23519f0a164b99b25a0ad550cd91b74937b1b7dcd0b7610ba9e001`  
		Last Modified: Tue, 01 Jul 2025 02:25:12 GMT  
		Size: 2.4 MB (2402186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a98678754959fcab1fc3f78ed113c25c95e205f688b8790629b36b068c0ab60`  
		Last Modified: Tue, 01 Jul 2025 02:25:13 GMT  
		Size: 6.5 MB (6459008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d6a59c7311572be36dbd5e3c1ba0c513b1bcdbfc90e753fcd1c2ad63737bc1`  
		Last Modified: Tue, 01 Jul 2025 02:25:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd51d0b9ef1b733debf31dcce3f7403d689618a4968ab25a91ac0abfc797e50`  
		Last Modified: Tue, 01 Jul 2025 02:25:12 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:a9fc2fc0ec4038e840061044303009a791f0482a5d65111d1d143ce080efed32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3646833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e9d2bcb152456db5eddab8c13fce698c7aa3711e7c9ad18efd5ed2bdc2b37e`

```dockerfile
```

-	Layers:
	-	`sha256:719b075249a5c633a8c2f05fdcbb742ddbb973547d88e956d2202f5cc7d63d08`  
		Last Modified: Tue, 01 Jul 2025 04:04:24 GMT  
		Size: 3.6 MB (3631793 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0db246d3f81fb31c55b5fa1f19a9f43aff5e58d219aa498b4bce180897338aa`  
		Last Modified: Tue, 01 Jul 2025 04:04:25 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v5

```console
$ docker pull spiped@sha256:edfa7b83c9f8ee095eb099239510d502de1e4e6fdf36282155f5d6b50dbdd558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.9 MB (32910050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548563c4dc7cc83e0bb8cd164d713e337e594f1ee43311f72ec06791c1d3e05b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1751241600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:57a7872a7ce75b95d171f720f215d4e72b887ae709c5c0b319f93f704bd71e07`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 25.8 MB (25762460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdeda97ad3e2bfeb1d3da9c2974ad5a2c99c3e677e7a0bbf83533aade7cd82a4`  
		Last Modified: Tue, 01 Jul 2025 06:06:13 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b015f9cf9720a5f7103f294ee6e0c72347162738b657d7cc364d82671218bad`  
		Last Modified: Tue, 01 Jul 2025 06:06:13 GMT  
		Size: 2.0 MB (1998255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb8faf9556c23d3f1c82805b010663e3d984f720f954bbc9386f772e1333680`  
		Last Modified: Tue, 01 Jul 2025 06:06:15 GMT  
		Size: 5.1 MB (5147794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513460512172493f117e7067379286e818ae86fe7ce944345d9ec2b66ef46cec`  
		Last Modified: Tue, 01 Jul 2025 06:06:15 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7002e87c88b3ff6535e6ef95670695376e770765466157c1157761dabaa3b6`  
		Last Modified: Tue, 01 Jul 2025 06:06:15 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:b9eb9338ad2bdd8479b7af1c056a5b0a3d9b454ce8435fba336c464655162def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3617772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf50c92b57e843e26b74b4fdcd2ff8554bf290c95380d75d463d16d21947405`

```dockerfile
```

-	Layers:
	-	`sha256:72f914733eb752d7149eb2889fe6aca3fff4dc02f26e3f54048256b46ca97511`  
		Last Modified: Tue, 01 Jul 2025 07:04:31 GMT  
		Size: 3.6 MB (3602631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4264d4f8cbf4f891ca4470ed5261eeec9bf119f8314058c131199c3c16aa5710`  
		Last Modified: Tue, 01 Jul 2025 07:04:32 GMT  
		Size: 15.1 KB (15141 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm variant v7

```console
$ docker pull spiped@sha256:a9056df29fc608ce23bc5dd89dc73f1a307dd9cc4568f5afd41b502d550f6df7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30685415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:806c1815a756a80dea14be79bca020e3baed38d716388800957b574f0449bd3f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597af0c309b7db16d2c9db9f5a05c8fb33c035fb856d112618880dcde74569ce`  
		Last Modified: Tue, 01 Jul 2025 08:41:57 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d355dc9037959af02a5eac3c08c6bea5ff76da6c5f8b9ecd8b5238c4120e2561`  
		Last Modified: Tue, 01 Jul 2025 08:41:59 GMT  
		Size: 1.9 MB (1856403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c81922d2a12fdaad2eb54bb04cd3b0c2bac3a11a46ae194dee09b6fabe19ca`  
		Last Modified: Tue, 01 Jul 2025 08:41:59 GMT  
		Size: 4.9 MB (4888729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffddab181147161eeea726d48ba35bdda88798eb1f01088936e0a2e1c504b1be`  
		Last Modified: Tue, 01 Jul 2025 08:42:00 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519780b72af2f1f76b6735aef05a2e27b4b3b1afcadb20e866b52573b972d165`  
		Last Modified: Tue, 01 Jul 2025 08:42:00 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:56902fbbb55664d04fa71461186bd80218b54741ce42cbf8f7dd1698a2c1e028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3616956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:583e68298827faedfb87b8d3a4aef23a19414d8182654f0f42034fa25265917a`

```dockerfile
```

-	Layers:
	-	`sha256:387fa230ca4e849a14728db4e945101e8b4dedfd68d0f1c541a58909d05930d1`  
		Last Modified: Tue, 01 Jul 2025 10:06:25 GMT  
		Size: 3.6 MB (3601814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5342bde067b2c60b808c0e0c2163b6a94861245f2b8087f6b10672b26b3646e`  
		Last Modified: Tue, 01 Jul 2025 10:06:26 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:cb209a48321512b849336cd10c6560447be53ad290df7a860442c5216b6b67fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35818465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1cc3d28c3a9914cdb656dcf5d520529b8c305813f97c784a58f33179287988c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231e64ee4b5f73f139be78cb871d48da14f4b1dde4442c3680881c8140fd7645`  
		Last Modified: Tue, 01 Jul 2025 06:32:43 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5dfd631fd81409727d860791d9b9b6301269985e8d02aa430d9148de3a91d2`  
		Last Modified: Tue, 01 Jul 2025 06:32:44 GMT  
		Size: 2.2 MB (2247442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed4b303d135a1395d15758dc19dc51eeca88061a24d212f84e90b95306f70f6`  
		Last Modified: Tue, 01 Jul 2025 06:32:44 GMT  
		Size: 5.5 MB (5491805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb383cde600396af7576eb1e1929316bdd09e7d23d3a03ab149e6613051d7850`  
		Last Modified: Tue, 01 Jul 2025 06:32:43 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46860d961f86decd94ae2c98a18d41491d7680a16f4331103c45c377079c003b`  
		Last Modified: Tue, 01 Jul 2025 06:32:43 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:dfb105bb1e8502c6b894305204bb0c3e029593546f920bfde0c951593da7032c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3618195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab67e54e4e0d74cf47c4f310ae3e3ebe8b87245e9b823d5c22662d1d0551662a`

```dockerfile
```

-	Layers:
	-	`sha256:62e6f1c4922e84d9260e8db09416c559a49eade9985d5c695e08eed1151ea958`  
		Last Modified: Tue, 01 Jul 2025 10:06:30 GMT  
		Size: 3.6 MB (3603021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:022d8c338da24b914cc498f53553ae887ea588c82f2745d039d832907c64d79a`  
		Last Modified: Tue, 01 Jul 2025 10:06:30 GMT  
		Size: 15.2 KB (15174 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; 386

```console
$ docker pull spiped@sha256:2ae45143c8464d1e8028c71a85b8288a9fad75dad6cbcd89a106a47626da2f76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37571424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80c6c1f290a11dff25ed2454b33e0e53277928fca72b3f15ba41f3508c9a1c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69af88f2dc291d20127149271d6671a3e59d0068cfd749eb55deb04f1d7459a`  
		Last Modified: Tue, 01 Jul 2025 02:23:54 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d494dd3202196292826fc985ae49292e9a71e7090c807a8869bdddaa46c45ec`  
		Last Modified: Tue, 01 Jul 2025 02:23:56 GMT  
		Size: 2.4 MB (2400597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932373df38b715de5ffb94d4b32f5c6e73c151c695d7ea13e767c5df0181f1be`  
		Last Modified: Tue, 01 Jul 2025 02:23:55 GMT  
		Size: 6.0 MB (5956855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a2e6bd84c3787c115d1ba31d3d2ac86927e93a0114500f401b294db73c3d4`  
		Last Modified: Tue, 01 Jul 2025 02:23:54 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78781d70ba16205c2f14a56c5935115ac76747396c7b5a4c30cb03d166242658`  
		Last Modified: Tue, 01 Jul 2025 02:23:54 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:6f611c7a53cb09390bbbdf6a188b72d6c09dc978c088e7417467483e92c69f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3640776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9f4c5278b0d61d117ca913ec12a122fda52178e19cf2e48371e477c5f9678f`

```dockerfile
```

-	Layers:
	-	`sha256:b0f54856e78d0c4a73990c9e74721953414afefe16ae3e08fb0e19e569dcea5f`  
		Last Modified: Tue, 01 Jul 2025 04:04:47 GMT  
		Size: 3.6 MB (3625772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:690b107191a61808dd88bc4ecea63f1c75046e3df06949dedfb3ce135527f916`  
		Last Modified: Tue, 01 Jul 2025 04:04:47 GMT  
		Size: 15.0 KB (15004 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; mips64le

```console
$ docker pull spiped@sha256:44a7ea572ee5ded3f2ceeb336ebf9f4b19e5c1721cd638675de7ea6a2365a05e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 MB (36174227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e178694b114b2b500387f26b4a03570b5397e036a413c99d5252b6a40471ab8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ac3f61581c7f5755d8598b3a0857c417db0251b17c0e4e4f43a5fc0e24023524`  
		Last Modified: Tue, 10 Jun 2025 22:48:26 GMT  
		Size: 28.5 MB (28516717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bdd8e35937df27b0968ae8a23741b39da32971cd7b93300071387fb995566f`  
		Last Modified: Wed, 11 Jun 2025 12:58:47 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b256192f977eee0878018b3b88849faac10e38c96758feb6025fe97506622e3`  
		Last Modified: Wed, 11 Jun 2025 12:58:49 GMT  
		Size: 1.8 MB (1842270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8dbd97c4f500cedd0e46e05c6718376077029907325d8b425eaa1868dd89711`  
		Last Modified: Wed, 11 Jun 2025 12:58:50 GMT  
		Size: 5.8 MB (5813695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7e8d0a0cba57075c6e87aa5c196d709f79ddf523ee3af39a64ddf7bf645fc8`  
		Last Modified: Wed, 11 Jun 2025 12:58:47 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89390ae038a588fb2fbecb5444cc0f64955ddba34a4c65c9f0922cb722826aaa`  
		Last Modified: Wed, 11 Jun 2025 12:58:48 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:82053f23f3186d8684d3e7b169e166514810bb0b54ed29568f52924dfd2c8221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 KB (14897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac7464c90ddadce8fd091e3ad3f97cdad7caaa5783f4f82d90906e9ab0d1e3e`

```dockerfile
```

-	Layers:
	-	`sha256:172483dac84d11e985c77a0c8e905873e020a5da1c9bee18ef7cb5331e5ada85`  
		Last Modified: Wed, 11 Jun 2025 16:04:35 GMT  
		Size: 14.9 KB (14897 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; ppc64le

```console
$ docker pull spiped@sha256:c58d64ee71cf3e45b328bd638a32df319eef1a0c887eb365b160a23f9b604f76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41099495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:699a5db20c84993b79136a82d34f8e553a2ca2f4c735955ab4740b51c612ce41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8daad143bb73c232d3d7b4fbf252f9ae53f1093169175862ea9fa1fb6be299`  
		Last Modified: Tue, 01 Jul 2025 04:52:54 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef84c7d520603a0c29edd02d1a5e67b201844dfaa547b487306f5705b768ad0`  
		Last Modified: Tue, 01 Jul 2025 04:52:54 GMT  
		Size: 2.6 MB (2583814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5cd14b2072612934415faa6e5ae5ff14fafdef4657cb483b0fe2376a6083078`  
		Last Modified: Tue, 01 Jul 2025 04:52:54 GMT  
		Size: 6.4 MB (6441321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5ce146e01f1fa63ab28a20ea208895273db520b7409532e81e69473944657e`  
		Last Modified: Tue, 01 Jul 2025 04:52:54 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d6dcf71250e742ba5b5120a558e381380c225c16ef14b9767678e24e321199`  
		Last Modified: Tue, 01 Jul 2025 04:52:54 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:df9764e3642fee766eff2fa2f3f045907c1c9de6e6f1e86798218afa16c8bb89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc2377e9baa00a65147c12a752086b6d52a841d9ad74d1fbe55a2ce0edc92aa7`

```dockerfile
```

-	Layers:
	-	`sha256:d5fec28410667c567395f8e1644afd3e24d2755137be16f95a2ddb3ca7e9eb19`  
		Last Modified: Tue, 01 Jul 2025 07:04:47 GMT  
		Size: 3.6 MB (3617578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:213ed2703a3001a48e4784e291448cec9aa70dc2577cceb42ba758aac2b124b2`  
		Last Modified: Tue, 01 Jul 2025 07:04:48 GMT  
		Size: 15.1 KB (15088 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; s390x

```console
$ docker pull spiped@sha256:4fd4fbd6bff6c2c5371378c01c1f88e356947691114480d2225f898b3000e017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34350835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d713089640911023d2144ecef46d942cd0fe841cb5f66c135b0ab5d52c8d021b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Wed, 02 Apr 2025 21:12:22 GMT
RUN set -x &&	groupadd -r spiped &&	useradd -r -g spiped spiped # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	apt-get update &&	apt-get install -y libssl3 --no-install-recommends &&	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Wed, 02 Apr 2025 21:12:22 GMT
RUN export DEBIAN_FRONTEND="noninteractive" &&	set -x &&	buildDeps='libssl-dev libc-dev gcc make curl ca-certificates' &&	apt-get update &&	apt-get install -y $buildDeps --no-install-recommends &&	rm -rf /var/lib/apt/lists/* &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
VOLUME [/spiped]
# Wed, 02 Apr 2025 21:12:22 GMT
WORKDIR /spiped
# Wed, 02 Apr 2025 21:12:22 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Wed, 02 Apr 2025 21:12:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 02 Apr 2025 21:12:22 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba9efd7d502df0495e76d2ad6412680292de681f1395b2821647a3d1e97ba4e`  
		Last Modified: Tue, 01 Jul 2025 08:32:33 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd21e11fd96caa46030e4fe7febc0e97471ec90db3dccdaaccd5c566b9404f1`  
		Last Modified: Tue, 01 Jul 2025 08:32:33 GMT  
		Size: 2.1 MB (2069107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cafac6ec34f9ef7c9c61c4d2278a341ae8a6a9c0ce9958ae15c674791211bc0`  
		Last Modified: Tue, 01 Jul 2025 08:32:34 GMT  
		Size: 5.4 MB (5392378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cda6f2703215be4a50214148313828abc4214a6af401c666d95b8446faf1917`  
		Last Modified: Tue, 01 Jul 2025 08:32:32 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf6c91c959f3941a785c6415b49de727da398596985451ce16e536a9618289e`  
		Last Modified: Tue, 01 Jul 2025 08:32:33 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:525d3a4635569b93f7d1469dfc44704e94d745918e7bbd3c14e9c4c0d1283d84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ed18d0ce13dffef4b6a74771b1e94f6d4db70700ec1c1fa5b6485ccc5c962e`

```dockerfile
```

-	Layers:
	-	`sha256:74acb3ebe1d8b70825dcf67516fa625cc1d71a31147357bdc2611f05b46a4364`  
		Last Modified: Tue, 01 Jul 2025 10:06:41 GMT  
		Size: 3.6 MB (3617087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bc47448be78caae6aaa25230ee767f37502b180009094be68bb80479ff02d0f`  
		Last Modified: Tue, 01 Jul 2025 10:06:42 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json
