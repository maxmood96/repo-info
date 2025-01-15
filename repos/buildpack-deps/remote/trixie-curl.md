## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:bc1dd67b2ba9c8b2dd0de47304d6e41779133fb4954f28d397af8f209e1be8e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:trixie-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:185277620d21cca71d9049fbfe57e4d0a0861665835c1f5643922eff3f78fb36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74248263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b448276c6947d117e941929ea20529eb1405f37e78de5e7e955fc1b98a8cc3ed`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9146d6057920f25892ed3e631287d1e0e740bd11f7e3dd39c76c478675de8456`  
		Last Modified: Tue, 14 Jan 2025 01:33:33 GMT  
		Size: 48.3 MB (48276092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b2bf2fe5435a7871b88dbb724a93352983bdb5ad01681e2165e7056a7fbf25`  
		Last Modified: Tue, 14 Jan 2025 21:22:01 GMT  
		Size: 26.0 MB (25972171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b23bcf663941e84dedeba50130583de1c1f9a9c29634c799f9221906ac8dd757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4035932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f867974e1bc4c7627ae4b5bbee069a0714bce3710ee0f30e8aca039ccecaf34`

```dockerfile
```

-	Layers:
	-	`sha256:ff944ab972c616ca3404889427eff6543a1486ca8a039534e1431c234bbb96b1`  
		Last Modified: Tue, 14 Jan 2025 02:33:07 GMT  
		Size: 4.0 MB (4029111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b011f3b2887db0f8e934462d977b6bf8f939f29b3f2c584bd49cf67e854f024`  
		Last Modified: Tue, 14 Jan 2025 02:33:07 GMT  
		Size: 6.8 KB (6821 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ba504575552c0ded31eb79845d149f3d8409a65cd15bd52d20768f0380cbfec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71105823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0026e107933520688e338cac7925f7262392d69451f667444730f0aaee4c463`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:76cad3cf5a6ccb480f47b45bb1e37068b6554531620fd6fa1a71d8bd07d07d73`  
		Last Modified: Tue, 14 Jan 2025 01:35:53 GMT  
		Size: 46.4 MB (46441720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb8fffcdf3a616be17dc58906cdefa8833c6afb82ce71878155d250e95d14d5`  
		Last Modified: Tue, 14 Jan 2025 06:09:57 GMT  
		Size: 24.7 MB (24664103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c38ad4e429f0d6e2efb7e18cb0f2ddbe6a78255d463d39665f6279fe51dce804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4044419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f55513a6660c0f1feb56272012a525f20f9a34ba0bd160f524107716c72a23`

```dockerfile
```

-	Layers:
	-	`sha256:ce65eebf9378c9dc7cc79206b976a31474a56b8d97d4388e5a3b28af06c2455d`  
		Last Modified: Tue, 14 Jan 2025 06:09:56 GMT  
		Size: 4.0 MB (4037538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1810432b9c8e3b913ac2156f672f09e0f6b88431be125657a94eb6b2a138634f`  
		Last Modified: Tue, 14 Jan 2025 23:21:21 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0a6c357b2a5550465bbb58c8cb50f1b528f6e0b3bcb2cc03e8e4699e5cbbe01b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68387206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1403e33a3f014b9f3a79bfd150de00b1bcd52579b0635858ef7266499b6c4d08`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:105ec2fcec8ae42e2b6cba4c3c8463bdd5ad21cffe232e9cfd7ed127e7ede3fa`  
		Last Modified: Tue, 14 Jan 2025 01:39:08 GMT  
		Size: 44.6 MB (44580459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881cf44810c526c17319a679eee937276e08c6767dabc96ffa22308bd53f7e1e`  
		Last Modified: Tue, 14 Jan 2025 09:00:07 GMT  
		Size: 23.8 MB (23806747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:816e5ecae2afe97b2716b2fd5e97c09a92fa84b86e4724086e7bf7abc1da653b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4037015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:416f156bb04b0ec4ba73c579a5ada9b1d5888217d9012f51892ef6cbdbbe423b`

```dockerfile
```

-	Layers:
	-	`sha256:97fe398e375c081a578a94fa2865d947b15ecab68026812febb5a3eb42b36ec2`  
		Last Modified: Tue, 14 Jan 2025 09:00:06 GMT  
		Size: 4.0 MB (4030134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc05a4160f4ad6a923accd00f3bd549f0f7dfdf8ccd93e41214ce85b9a48ebdf`  
		Last Modified: Tue, 14 Jan 2025 09:00:06 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:182fada39fdc6c95505ad2164b836e0093badd288562d764bf180d3ed7990992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74087992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf76bcd5c919898df4b79c33388c444d31ff341311606f28e2730404757f7f0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:53cf00e5414c63ec005c43ad8342c8e55028d137e29e95d889d4247b0586d248`  
		Last Modified: Tue, 14 Jan 2025 22:04:53 GMT  
		Size: 48.7 MB (48661509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6216ff9e1bca52cad6d9119375ff8a9fe28c8b52c130d5380d5ded38210e688e`  
		Last Modified: Tue, 14 Jan 2025 07:01:19 GMT  
		Size: 25.4 MB (25426483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:be326526a1b4ee79b2419c1e1713a55fd619c0538b7226b8b47ec950d9e3362b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4037707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:239ab26d9165c310503a146bb3b3e42eafad2cc45baff40871c2633f56c6797b`

```dockerfile
```

-	Layers:
	-	`sha256:73d360e4010aa3cbbd85a9d4b157c6b9c67e623551340303b8ae15f52ee8ade5`  
		Last Modified: Tue, 14 Jan 2025 23:21:27 GMT  
		Size: 4.0 MB (4030806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6096c2ff4f3bca1295534af7b507d2a71380c64572ee7898c209d91c6129c8b`  
		Last Modified: Tue, 14 Jan 2025 07:01:18 GMT  
		Size: 6.9 KB (6901 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:829e0f497253cee04547b28332edc9d885bfda4c11a53c910d33a8b29aa32126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76789778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c57f21450060e26690bec7359488005c87bea5b3c4aa8697e752584fc87c0616`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0b7bebb3fb62b18c851bbf703cf6a1caa57f7ffda09b0b23b4e4cf1051c666c9`  
		Last Modified: Tue, 14 Jan 2025 01:33:38 GMT  
		Size: 49.7 MB (49675708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628707934f13167c16796e4cf79505bf1ee994868dc399d6e208f3c459420999`  
		Last Modified: Tue, 14 Jan 2025 02:17:30 GMT  
		Size: 27.1 MB (27114070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d49eba8ba68664136b4744e925652ce87b63c61bc0b1ecca1481c7b95c5a9b88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4031669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5172433a86bc8705b59a3f63bfa5f1ab9fa909a7585f8bed96c1dbc703d54a48`

```dockerfile
```

-	Layers:
	-	`sha256:7a990eb1d51e78b6bf87a1c0fd93531f580b703ee8d5b66d8b57eb3221e2c714`  
		Last Modified: Tue, 14 Jan 2025 02:17:30 GMT  
		Size: 4.0 MB (4024870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9916a90caa8ff4f61d2a1f1ce52ccfd88cd8941ddf570cd7e603ef21a5b912ae`  
		Last Modified: Tue, 14 Jan 2025 02:17:30 GMT  
		Size: 6.8 KB (6799 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:fd98e3efa140486701af3bbad0bff036d650707ae765c07c4be22171c350d9a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74316934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83a748686d419b8c487d0d25d3f5da8fbf2607059a4fe9c9050131bfb153408a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'mips64el' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7fc12d8a734ed45514ae5135503d718e9ff7693017677de649ab963638a639fe`  
		Last Modified: Tue, 14 Jan 2025 01:37:16 GMT  
		Size: 48.4 MB (48390219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0115509fb5cc85eda38403b37d75aa0d68bc08deb77a8f9d926a1f8c06d921c`  
		Last Modified: Tue, 14 Jan 2025 18:14:22 GMT  
		Size: 25.9 MB (25926715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b3b21d911bdbbe951623248f5bf342419c79a1e98a16566e970307e88aca9b4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 KB (6654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad8f6edf913998dda0a3027d7f7b577a96f8bd3b884fdf75b8a2659163eb80e`

```dockerfile
```

-	Layers:
	-	`sha256:f424bcd5f01098e3348abfb322c6399e19c51c96f327ebfcd35261b1ecabefa0`  
		Last Modified: Tue, 14 Jan 2025 18:14:19 GMT  
		Size: 6.7 KB (6654 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0381397e21343cebe61176a3c0cd5c2ca207ff8b7be2ee7f940db48aaf62eed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79574371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e36e8a515112602a6b9bd1d62a9a71fe6d15a002775a321339c194376782da9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:826e70a2bdfac0f05c49b7611afcf30a311c862a1beca6fc4059e4b6cd0e1a4a`  
		Last Modified: Wed, 15 Jan 2025 02:37:31 GMT  
		Size: 52.0 MB (52043133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f126b14e556a94eaec41c5a29f9164224f92b1080c74dca2491c3f7b9120c320`  
		Last Modified: Tue, 14 Jan 2025 05:32:11 GMT  
		Size: 27.5 MB (27531238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e6718f563fdf9602886e8a236f58b8aca3c3dfe798705ceb2fd01787dc061252
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4045427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60992f7ff4eec8339a823703a9fa73186805183f9eb51b8e064c10e07e71f02c`

```dockerfile
```

-	Layers:
	-	`sha256:075dadbc11e09bf17632119066e745f6854da98d506b85fee4cf899347fd662e`  
		Last Modified: Tue, 14 Jan 2025 23:21:33 GMT  
		Size: 4.0 MB (4038574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed8cfd9e4f6cd07b0122d0cd8324aca6b289a5358b36ae7e43d33ab878866466`  
		Last Modified: Tue, 14 Jan 2025 05:32:10 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:58d2be83998bbc18fa10670d0b0c70e8f4fddb789619826f5d69dfcebdbb9be9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72184875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6862b1dc3c9b2ff34de8f8d10a2f2afdb9ced6c8607e867aec9edc89f87793e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:849b733ed481de97a7fedd0fd50f72d0749b6e5cba2793e9f254e7121e3b170b`  
		Last Modified: Wed, 15 Jan 2025 00:00:27 GMT  
		Size: 46.8 MB (46838301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:446f9a867ba71ad634e7a78190f0c825b1e9920d98acba23977b76b41165154c`  
		Last Modified: Tue, 14 Jan 2025 20:42:31 GMT  
		Size: 25.3 MB (25346574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7fb4fe41d2b2f1c1ed88ca6b41fa40b6c0e92f146603b3d58d01539e4f8c2c2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dadcb27eeafaa6744fcd26057265da76618f9dacfdf92b89c5ed6953abf98b88`

```dockerfile
```

-	Layers:
	-	`sha256:07b01b47d7dd369aed710c6f7bafa21c566b9066a67963946ebb33d8794fe961`  
		Last Modified: Tue, 14 Jan 2025 20:42:28 GMT  
		Size: 4.0 MB (4021295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf9531bf47d83717d8221e2165b2d1bf21c2f84d7e2b65585a3bc83ab0d5288b`  
		Last Modified: Tue, 14 Jan 2025 20:42:27 GMT  
		Size: 6.9 KB (6852 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:5b865744affabdad4facb9368d8812f747e8ec0e31ca392ebc0c053b8ecf8eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75461068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf2314672f275b669a992664c6651de73387cef151be9e2b91ed0c90b060b4f4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1736726400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a96882092e58b6b0f460c25e0b3fa57215487e6282387621e5c4dd2314637493`  
		Last Modified: Wed, 15 Jan 2025 05:05:54 GMT  
		Size: 48.3 MB (48329740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c639414a48a5e91286e442a3c2a376c94650966c4fede85d34f85e98bf430e8`  
		Last Modified: Tue, 14 Jan 2025 05:01:37 GMT  
		Size: 27.1 MB (27131328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ce6b9d24206705a412f9177de03c9404c3ea2ac5f2cbebaf286beaf26826a92c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4043063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61181940ce2f9066bdec1cb7b938d57c4629270144007ea59e58ca1a886bd653`

```dockerfile
```

-	Layers:
	-	`sha256:ae854e077279bf9625342eb2035af5231976d3216536358e02871ad68f502cd9`  
		Last Modified: Tue, 14 Jan 2025 05:01:37 GMT  
		Size: 4.0 MB (4036242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af5df9452122a62397f4a6f985e4c7b773a1f95dc211897bdb3db8fd9138168e`  
		Last Modified: Tue, 14 Jan 2025 05:01:37 GMT  
		Size: 6.8 KB (6821 bytes)  
		MIME: application/vnd.in-toto+json
