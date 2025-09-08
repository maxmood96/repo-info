## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:59755e1233d30855014cdc7a9e14412007d96d3842c87bb0725603f8c8708d7c
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

### `buildpack-deps:bookworm-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0f66c5e288d9df084adeb860ac1b30259a14531df76d40c71d27dab7d3229203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72506606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bce08901097d10e3b76414ec785977a100362baa5877b6fbd5e66081cc86d14`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8fb375ec14f3df8b31b70d0216508565ab7264a7e16cac4f8cc07f8eca22445f`  
		Last Modified: Mon, 08 Sep 2025 21:12:37 GMT  
		Size: 48.5 MB (48480610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbb2080a06a2888e44131965340c1eccd23f4d49efe72176246649abfbf9d9`  
		Last Modified: Mon, 08 Sep 2025 21:54:14 GMT  
		Size: 24.0 MB (24025996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:784afa291fdf2f6fb180a1ee20a7335c75d1e828b7cfb6bbacf0a11545863fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4520551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d121ff53e06440348994ca46ff75d9603e781325ef9d399947ee4a76e1f5d16`

```dockerfile
```

-	Layers:
	-	`sha256:e16b5a13b9f15db58b607e5bdfc96252f1efc321f3c276c30ba810895bd4fb2e`  
		Last Modified: Mon, 08 Sep 2025 22:19:43 GMT  
		Size: 4.5 MB (4513691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:806ebbf374ab4ca19ba7065b3ce2fa63ada96c3d2d691afae84976046bd1942c`  
		Last Modified: Mon, 08 Sep 2025 22:19:44 GMT  
		Size: 6.9 KB (6860 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:7780129cf6798141f43b8785df367d7bc5427ea3efce8fa482f6be63d431aba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68718187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a5c2307c6e872956566579dfb73f59d516a577f01a0cbc98559a1ac9a253ad4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:cb78550743da54c438514c9643e672e9378df901e1cdbedec41078f3c369313d`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 46.0 MB (46015690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021282bc493daf4a7f690f4c5ff13dd6b9ca0b3670be69b20780afc009b935a3`  
		Last Modified: Mon, 08 Sep 2025 21:49:31 GMT  
		Size: 22.7 MB (22702497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:893b8a67dcc0b29b006b38ed4bb5a6d9d307d5c1c25b7186df495a765ade34b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4524431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c6cf04ac81b73f3309a5c7868e099faafe5e8b26fe2b7e2b04a1167912568c3`

```dockerfile
```

-	Layers:
	-	`sha256:3026393e895c81cc230de68de39ac982c05a33550ca658f738a48580a2fe804c`  
		Last Modified: Mon, 08 Sep 2025 22:19:49 GMT  
		Size: 4.5 MB (4517507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8acd60b8a70d0e5b6cddb57a68b515b18580d56cae89e7c0e81ef6908d95d98`  
		Last Modified: Mon, 08 Sep 2025 22:19:50 GMT  
		Size: 6.9 KB (6924 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:65138c5d1f551fe99caab2bb3d6a0548701a3538f7379630225c2c0d0324ffc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66127077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad3ef1fbfa9447d331eb79a039f74d9c1c65bffa40d51a959248331389160ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:66de9a3b6b96c15de3235377e1618295643161d16058e17bde51f54951c6ec21`  
		Last Modified: Mon, 08 Sep 2025 21:14:33 GMT  
		Size: 44.2 MB (44195998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efd1e8889a5c39ed7ad3628cf08e3daff474f9ff5b33972b323c79f306440f8`  
		Last Modified: Mon, 08 Sep 2025 21:55:01 GMT  
		Size: 21.9 MB (21931079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:74366a34b72e71e782e589cd3e3680ae0c110755a3a8e744f1f950929ed9d4b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4522904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abbe6176d9c7207a738241005f1869067a40aff8a06707e84b26bd85f832539f`

```dockerfile
```

-	Layers:
	-	`sha256:d4ebc0220fe7ac1c566f189805eb6df80dd6cc97dc17f0daf9f7487a46c44ef7`  
		Last Modified: Mon, 08 Sep 2025 22:19:55 GMT  
		Size: 4.5 MB (4515980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23873d23150a5bb3d6918269e50afdcb204fc4de1327bdf3562900bb13ef8755`  
		Last Modified: Mon, 08 Sep 2025 22:19:56 GMT  
		Size: 6.9 KB (6924 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a04bdaa87d1e0d2ae2eaa2f3eebacc95e484e6e05f2dd5bac1346d3f1ff8735c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71953808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa08eea578bd445e023db58556032d94b57d5c3d9ed16e5101470687668ec77b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a9331b686701a987bcd276cc69a0f676d471ccda1aa353d2f7fad017f2894cd0`  
		Last Modified: Mon, 08 Sep 2025 21:14:32 GMT  
		Size: 48.4 MB (48359019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e108925666d6d84c8fa32751877e66a295ad55c9fbd10142325b99d60e786e17`  
		Last Modified: Mon, 08 Sep 2025 22:21:46 GMT  
		Size: 23.6 MB (23594789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:95ee9f25ba9b0f25eb2307bed9a566c983f4b6fe4d3c5b99edc6261b76d4c3c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4520892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed0764e7e5890cc34051af2033cc4bab92883dac973430a1bf9cf0cc23991db`

```dockerfile
```

-	Layers:
	-	`sha256:4e9125a3c09617de10d3e7c3edf54af83dab929a6830b6448a160f724f3800e5`  
		Last Modified: Mon, 08 Sep 2025 22:20:01 GMT  
		Size: 4.5 MB (4513952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00dce961b2b2ac3ea2e3fab737b76ccd43de2e385dd6af584fb5c4b1241d5034`  
		Last Modified: Mon, 08 Sep 2025 22:20:02 GMT  
		Size: 6.9 KB (6940 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d1c56c3d826e42a9ca2203d2731984d2f7dd2b5f95b1639c63336b1588ffbedd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74327342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3516b906c762d89624baf14b09078e599323790d3c3ad0bd5919255442eb7a5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1757289600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5538e96bb7df1a7ef01bd7fcbf51f4cbc041246109c06cf661f7058c203851af`  
		Last Modified: Mon, 08 Sep 2025 21:12:26 GMT  
		Size: 49.5 MB (49466684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:822d7073f1bfbc05d754234ff0c82bf81a44dcb6b19979f28688d3054a71fa6a`  
		Last Modified: Mon, 08 Sep 2025 22:07:56 GMT  
		Size: 24.9 MB (24860658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b4f65327290105dba746fe7f63fb2aa5a23c762aa6fc6e7911dd09f557d457d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4517649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae6862b319c1ca3864c46b0ee3b45f0115fe0587cde0560fe4cbb63f01d6669`

```dockerfile
```

-	Layers:
	-	`sha256:8a93d0acdd7190a54e8ec30c7191cac0208c7e27b9317e7f425e43e115ec39b6`  
		Last Modified: Mon, 08 Sep 2025 22:20:07 GMT  
		Size: 4.5 MB (4510811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e423bb3a7fcd8bdf6bf61008eb48834c3f7f08b2189b17064e039391b40bc47`  
		Last Modified: Mon, 08 Sep 2025 22:20:08 GMT  
		Size: 6.8 KB (6838 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:3f71953104513ba7020effef5558f88afd9e6b539def3a111834ec69ab24bc38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72380316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6540f5b267d3f19d8dc76e6e004b720c52ffc345c6a441150ddb30434c4f6c20`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:39ab9a968f454fda0ebffae415d31434cb4c4b3f4bb9da0e89f360bd60fa3275`  
		Last Modified: Tue, 12 Aug 2025 21:09:50 GMT  
		Size: 48.8 MB (48776657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5bf976bc5466a2e4cdc6d87c28337bf663ea094da7d169694d61961d11248d`  
		Last Modified: Wed, 13 Aug 2025 06:38:46 GMT  
		Size: 23.6 MB (23603659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7bd274409d19a39b189167b12ce6049f520fee4634f92a98f9cdaafbd5edb8d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 KB (6693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5506fd53287b4162a1c26ba91bc94a4283685a306e817b14b0cf3edd76f5cf9a`

```dockerfile
```

-	Layers:
	-	`sha256:d1bf7c7978327e95b459be3fc7fd8058667b9fb34061afdc98b9d5d581f26c79`  
		Last Modified: Wed, 13 Aug 2025 07:20:04 GMT  
		Size: 6.7 KB (6693 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:6951ed9bb1e94b9fee3f62fb8a42f913e0843d5a4a84ff950d14d2502dd09198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78004116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63d4b341086961a1ddff5038d1b3a943735a81c1c96645f5a6b7320ad14cffc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:33bc01697f2fcceb00fe53fe1bf433b48dc127c82c1555f61eeddeda9d72ff40`  
		Last Modified: Tue, 12 Aug 2025 23:05:53 GMT  
		Size: 52.3 MB (52338077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f87ea767eb09118b3668a0dc44ddf5bf258db4f1bebc7989803cb1b75a66c9`  
		Last Modified: Wed, 13 Aug 2025 14:33:16 GMT  
		Size: 25.7 MB (25666039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4a811509fbfb567ebae0de4b94798fd445730d48e731f0487564258e04f88e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4518423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4024c9ffb56d23e45b3014fbba463b95af348d0ef10878112a92213db30f6fd`

```dockerfile
```

-	Layers:
	-	`sha256:c586a856b12a602176a8a5a0ec14c68f80338bdb78133fe91d8970ef42745ec3`  
		Last Modified: Wed, 13 Aug 2025 13:20:14 GMT  
		Size: 4.5 MB (4511532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9efc2b9829de6c347e7b75208474e579e0c1201fad567fa42b1b23a16c9d9ac1`  
		Last Modified: Wed, 13 Aug 2025 13:20:15 GMT  
		Size: 6.9 KB (6891 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0bf7db85aba6a375c40b16247bef64315fe77519e9e942b2235ffeb20cc6bed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71170038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ac7ca7fc7df28e2053fe4a931f1c45cc60535f5cd9462c669bf45f59e7b8eb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:635b31fd21bf059b6af0abf57b343066d0218ebb3e0b679927cc1752427a72da`  
		Last Modified: Tue, 12 Aug 2025 20:53:37 GMT  
		Size: 47.1 MB (47149866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af75c300f83884b3a2b4352096299334113ee00d6718ab116cdad0fd28ea4064`  
		Last Modified: Wed, 13 Aug 2025 03:14:49 GMT  
		Size: 24.0 MB (24020172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7d85ccf8304f5269340b4ba5cb7b6b04a5dbc6af171e27d1a1b8a28e0cd5c9f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4510581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e64c776a54e14a307d6359cfe3384bfe6fa83a4657ce0f78efb0baff9fe06c78`

```dockerfile
```

-	Layers:
	-	`sha256:c37467bac136adfc616b2ab4f0ce4159be902706600fa54a6bd03fec004b8e3c`  
		Last Modified: Wed, 13 Aug 2025 04:20:00 GMT  
		Size: 4.5 MB (4503722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6766f1d57908a056bcfe4e42fc0fef311867019ec5dd5472af9169b78cc3de21`  
		Last Modified: Wed, 13 Aug 2025 04:20:01 GMT  
		Size: 6.9 KB (6859 bytes)  
		MIME: application/vnd.in-toto+json
