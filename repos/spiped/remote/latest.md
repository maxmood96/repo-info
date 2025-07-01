## `spiped:latest`

```console
$ docker pull spiped@sha256:5de26a5e7996ab768b0c1b3dfc95e4753615bcfcda40ebd94c413516c46fb04a
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
$ docker pull spiped@sha256:9ce1fc0dc2d1f996039a56a7cfbd378133b51755333301f848efca7a7fad5776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 MB (30685410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1921127603a2388cd25100dc1a40dd4a882e503c99c18a1c94affea6d8318c76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
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
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884b3efe4f51fb3f46017d32a189e76502c05ebbe62a4f3734f609d087648aef`  
		Last Modified: Wed, 11 Jun 2025 04:49:02 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775ddb002179312e93532c834e5a8082a2d73feda8078b2ce73b951b3e45020d`  
		Last Modified: Wed, 11 Jun 2025 04:49:06 GMT  
		Size: 1.9 MB (1856413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714ec40b518a9456e36344a7732ddbd1daf761542ba21f6350a63ed6f652917a`  
		Last Modified: Wed, 11 Jun 2025 04:49:18 GMT  
		Size: 4.9 MB (4888712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c379236ab7a7ce88d18f78e77b41389fcef6e28730401b67ed4d35afb95ed2c2`  
		Last Modified: Wed, 11 Jun 2025 04:51:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5150130b703fde6b91fc459f573bafe2bd5048ddab660d82204dc88bc8ff26c7`  
		Last Modified: Wed, 11 Jun 2025 04:51:47 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:f1d93a3b47e53aefe111a468b535741ebf3c44b479196c920c1131ae3945be4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3616956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe8b73dbdca091b6a3cfc7fc1cbe516b479f8cf66cfb32973f1c08f4f92467b`

```dockerfile
```

-	Layers:
	-	`sha256:e11d0f6c12be4f061b56a863eadca9d24cba81ade81668d540c29d14815dca80`  
		Last Modified: Wed, 11 Jun 2025 07:04:34 GMT  
		Size: 3.6 MB (3601814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7398098987796bea294105e7389cac1c9b15dc4f47d3389c2ad39ad6daced0f`  
		Last Modified: Wed, 11 Jun 2025 07:04:35 GMT  
		Size: 15.1 KB (15142 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:latest` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:b5143746337b9bac98b518650f2e9ed5b4b9886eabd460426ceb3de5ec9f386b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.8 MB (35818470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37585eab662d0b615e056a5ef9795b640ce9a89a931957d10ef73e596f21268b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697f876cc248b0c7ec91a68879fb0ecc212568f3e4a637e295be916be6edeeb8`  
		Last Modified: Wed, 11 Jun 2025 02:35:31 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd86f82bcea91f9ced30eff144ee24770b00b7f2c177420dbd9ac9b49a43079d`  
		Last Modified: Wed, 11 Jun 2025 02:35:31 GMT  
		Size: 2.2 MB (2247471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df866991bdf5e32b6e9c1f1eb9720415e874e95be0247c4694eff05e37ca98b3`  
		Last Modified: Wed, 11 Jun 2025 02:35:32 GMT  
		Size: 5.5 MB (5491782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68a815d97977aedeb7c8399fd91c72bd238a307f23708808c8a427312e4eb47`  
		Last Modified: Wed, 11 Jun 2025 02:35:31 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bb490ebf89b9d37cf331e0e031ca55e54357903611110f42a60ffa4f0765c9`  
		Last Modified: Wed, 11 Jun 2025 02:35:31 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:0cf35df2d4678aa90666b297ace71852e525bb0d58e8a619042d808ec755eb66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3618194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a83a2fc05bd0588064870c4991b5732847da041258de103593e4278457a0e5`

```dockerfile
```

-	Layers:
	-	`sha256:ca4a2821dcebb2491eb6b24e0f92a32a0dbabed04f40af44570075175a909d20`  
		Last Modified: Wed, 11 Jun 2025 04:04:32 GMT  
		Size: 3.6 MB (3603021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2fbdf9a4be762dbccd1fa0a114ca7fb82d1621e3ffb4599640ec48fb9a7faee`  
		Last Modified: Wed, 11 Jun 2025 04:04:34 GMT  
		Size: 15.2 KB (15173 bytes)  
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
$ docker pull spiped@sha256:1f81a83169a2f8dc6b44819dedd42d66f5bbe5df87852868fff1df284ba9c279
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34350952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2037d0b0ecd0c097289e1415f39b5c2ead5667748a82c541c41a13b12c892ef2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 02 Apr 2025 21:12:22 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58de45a649e69d16b556199d2ab1e1a3f7d125d46b9cd16e1089e96d7cefa826`  
		Last Modified: Wed, 11 Jun 2025 02:40:40 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3d4626d3f4bbc854f1c1234cf6b0ee2c193de1051deb16f7c2891f16fca96f`  
		Last Modified: Wed, 11 Jun 2025 02:40:40 GMT  
		Size: 2.1 MB (2069158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf4f64f3ab37142abe901c392f0f67b586f082fa0ae0ab4a03ab39171b8b8ec`  
		Last Modified: Wed, 11 Jun 2025 02:40:41 GMT  
		Size: 5.4 MB (5392400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de79387160e54ed225d3a0a3a8ff4c57a454eee6fd186181d4ec1cbd9ef331f`  
		Last Modified: Wed, 11 Jun 2025 02:40:40 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f8e7b261543a312c7b1ad7c07a65a3f9349ddc7982903e31f44a8c0f340b2c`  
		Last Modified: Wed, 11 Jun 2025 02:40:40 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:latest` - unknown; unknown

```console
$ docker pull spiped@sha256:e6c50e6a029398c99b2b9176f2b69309f59e0d3af95a76db4c89f46c471e2c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3632127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695b35f06bbfbb170bb2e5e78b7fd2261c394b6496b0d6f48bcaf52dc30fb02d`

```dockerfile
```

-	Layers:
	-	`sha256:36828141ff79d8fb67953b34fd662f613d4b733b01245cf17dfe86ac8cd65dda`  
		Last Modified: Wed, 11 Jun 2025 04:04:46 GMT  
		Size: 3.6 MB (3617087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9a6dbc92f810f611f28ab51c90eb087f7373028e32f74d3b80c9d77b668eaaa`  
		Last Modified: Wed, 11 Jun 2025 04:04:46 GMT  
		Size: 15.0 KB (15040 bytes)  
		MIME: application/vnd.in-toto+json
