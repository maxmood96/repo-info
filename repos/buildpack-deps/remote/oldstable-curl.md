## `buildpack-deps:oldstable-curl`

```console
$ docker pull buildpack-deps@sha256:99473079230b3bbe95e5ee2ad099b5d4ed8d347904077e2149f4271545f3f193
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

### `buildpack-deps:oldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:effd98e24bd78714b0bbf1291db0754a37b72a2326ba43c852d631b6389e31cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72510357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e05b065dc842c67950d7cd6125498849509f06b63683addf43f8754d3d80a3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:27:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb445e472b1bad54f5a28edd51b11aec79eca8513394866a261891be9da6a343`  
		Last Modified: Tue, 04 Nov 2025 00:28:00 GMT  
		Size: 24.0 MB (24029301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f0f22d77704e79923bb461185ac4e44fd7ef723dea71389b59ca8a70529d56b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4520507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15790e32d48ff63b1d012d020952aa777f8e9ed9a0e06e60da23841e96637038`

```dockerfile
```

-	Layers:
	-	`sha256:cedcb267af0d016e7e1c264b03a9f05032790c2a4b6a97a8dca981518ace84b4`  
		Last Modified: Tue, 04 Nov 2025 09:20:52 GMT  
		Size: 4.5 MB (4513691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44ecda704af07061e1139f773dbb8fb8ae190b5d47fa9c2a0fdbf6135cd56fc9`  
		Last Modified: Tue, 04 Nov 2025 09:20:53 GMT  
		Size: 6.8 KB (6816 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:fa337b94b37af08728e6625fcb6c5862cc9aa93a1c1203e317f4ada752dc4102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68721848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c554653f8a70c63ed3c521ed8e0dd4b787df9f79dcaab627d9f0790fa03495b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 01:27:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d0780482d9b97d506bfd55bf3b805f2de1b9731c75e1b5800b5d53bb5388e1d8`  
		Last Modified: Tue, 04 Nov 2025 00:12:37 GMT  
		Size: 46.0 MB (46016089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68533da42b7795728d851e519aa05d6a90a43ea0bd8e6cf63e7cd6acc86ac61f`  
		Last Modified: Tue, 04 Nov 2025 01:28:06 GMT  
		Size: 22.7 MB (22705759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f1b0d6bbcd264031791a43e5ce9986647829f904049329fdedc9ac51a2815ffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4524388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1decfd7dbe7feb4ff142ebdff6b01e7b7b6b61a2b9c66341bc4c1e6acf4d0e04`

```dockerfile
```

-	Layers:
	-	`sha256:790bbee4787791eaa4ee94ec53cbfca6f7526f9fd9226e2cd7cbec013df9b83a`  
		Last Modified: Tue, 04 Nov 2025 07:06:00 GMT  
		Size: 4.5 MB (4517507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:178b0c2a1393baee33e8f04992eb1bfc2ebbc6936f5d2b2e732f7de15a1b2c0f`  
		Last Modified: Tue, 04 Nov 2025 07:06:01 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8a26cb5acfc534e680a283cf2192905b5edd272d191a06f776a9feac402bfaa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66131316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cfc9024d3f4fbb06ed9f3a218779730cee005c0350d0755eab6ef379a6f5fd8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:461f215c759f019a0fb4d33c976a91c4c2e4b033762b07a2f81bac66dee9e613`  
		Last Modified: Tue, 04 Nov 2025 00:12:30 GMT  
		Size: 44.2 MB (44196437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad602f359c1ad647108cc57270e592fc1f62f8ffd947a100fecee62a4a0d017`  
		Last Modified: Tue, 04 Nov 2025 00:39:15 GMT  
		Size: 21.9 MB (21934879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8c955bc7010f54072329805761463e4e132564ff2dadfb2753ddc048ae94bee8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4522861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39003deb10622733193c353b798f01f6b05646c097c5baa25e1f642744096bf3`

```dockerfile
```

-	Layers:
	-	`sha256:e6089f827a607f1c00566d18232674272cc1437d5dce3c71ca92feeacd2c1952`  
		Last Modified: Tue, 04 Nov 2025 11:22:23 GMT  
		Size: 4.5 MB (4515980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddea26a5ee4fa1b81557f120691091a6e6341058c224da7a7e3db3d10c91d198`  
		Last Modified: Tue, 04 Nov 2025 11:22:24 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7b0f713f15fb5970d338eb06e4902c0b1c3492ffb23a7dde36305d21af6d1b57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71957992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd3e8a0f1c9bfc02cea007c3b90815ba91d4ab95c57379e2bc006449b86b6c3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:30:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5463896571d3ff5317461a64229e9e4cb27d6d877114079419cf8b4fc96b0c02`  
		Last Modified: Tue, 04 Nov 2025 00:30:33 GMT  
		Size: 23.6 MB (23598514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b7d921d0b82c5535f5cfaf66b0ee28c78a3bb7b4267bf18bcbd30fe2120554f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4520849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c13693a864e48d6e217659bd731b2ef871f1776df3576d9cc838f71da099cdc4`

```dockerfile
```

-	Layers:
	-	`sha256:9cd77926cc94a4727dcdbb42cba950fdb2b7d6c0229e498192eba4280c88cca3`  
		Last Modified: Tue, 04 Nov 2025 09:50:49 GMT  
		Size: 4.5 MB (4513952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f99b18e3e3c64efff752af0d01067f2b1835ecdbbf970037a02f0f663501f709`  
		Last Modified: Tue, 04 Nov 2025 09:50:50 GMT  
		Size: 6.9 KB (6897 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6837fae77ec914cda04bc47d1863db1aa50989f33913f524dbac04f1b2e0b9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74331483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc59ce059319b492341a5e5493316a00a190b3c3c931a99348ea816eee48fd8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3a9907ae02a89d2535bb875a11c05038e0be4fa333c35747cd42f6f7b49e018d`  
		Last Modified: Tue, 04 Nov 2025 00:12:58 GMT  
		Size: 49.5 MB (49467114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce6be8e6c76b859a7e1808f7c9de22684a829f5386b5bf2011b85482d4d192f`  
		Last Modified: Tue, 04 Nov 2025 00:26:27 GMT  
		Size: 24.9 MB (24864369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7f5cfb811b62e6750f8fb25907f724bd6f6e3c2e2bd0b1258a1e32caf3798368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4517606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4a5e47f5da5a2eb001f13f867b82e3f23745af60b5a1ab805946327c77b418`

```dockerfile
```

-	Layers:
	-	`sha256:8266072de40461865ec888644775e227aae4c172ba0f0dc05f82d8aa47b3775a`  
		Last Modified: Tue, 04 Nov 2025 09:26:35 GMT  
		Size: 4.5 MB (4510811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce5976127c9cc32e865c5f1f1a6513dd10d40b665760db54fba40d53dfa74103`  
		Last Modified: Tue, 04 Nov 2025 09:26:36 GMT  
		Size: 6.8 KB (6795 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8dd0e6869330da6eaeb86067ba3025451d2ff0c9b3be4be6d6a2b59c8e40da1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72374544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3745ec6acb0fa96bea05e3037b35c61848e44b17c48eca0e6b01198bf5fd6f20`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1760918400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4ff7a7a0be4afa0c088333063434d872e5a67b49bc2165e0d5f1c8b45e31c387`  
		Last Modified: Tue, 21 Oct 2025 00:19:28 GMT  
		Size: 48.8 MB (48760743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ada83e05f36ace3b39ede326eee5e8c640f47f0d217601cc47ce49334a0f7e2`  
		Last Modified: Tue, 21 Oct 2025 17:26:33 GMT  
		Size: 23.6 MB (23613801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1f64dc80f912c051150225de454966d3d686c099a78f33bf464f01dfd2876509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 KB (6693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d7388131f1dc489233553ec0778cc18bca2b1e05db337c55c2dbe878824bdab`

```dockerfile
```

-	Layers:
	-	`sha256:9fcd1b45f6a765d165dad245229f5d6dc9b8564c54c02584367d2b59b1c8ab28`  
		Last Modified: Tue, 21 Oct 2025 19:19:49 GMT  
		Size: 6.7 KB (6693 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:02a98251995ea35d4466d37c5d3ab23cc061ffc5dba04b76f193489111164ffb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (77999334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3058559b2e16941292c20b2e912a29740a53335ca73cb40f5ab5fc5f060417c2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:24:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:dcdb26575d996c21e1eb1166ca8252365548a95e0791c754c1a66e3abe07a271`  
		Last Modified: Tue, 04 Nov 2025 00:12:39 GMT  
		Size: 52.3 MB (52327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a69074b98f99ca928580ca93ef45b80d247ceb89abd2c09f9515ba7ef4ea70`  
		Last Modified: Tue, 04 Nov 2025 00:24:46 GMT  
		Size: 25.7 MB (25672054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:97bd69fbc0c8b039b6e418dc7e79cfa0e8fc00a91896e180cee3c17bdacd9181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4525164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369cc6f49cc1500d954f6d73be8fd07833f5f245f4480e25226825b49a167da9`

```dockerfile
```

-	Layers:
	-	`sha256:fed0b9fe8466d1e929817d89a57bcfb706098c60c300c4629d621ebce6d47b06`  
		Last Modified: Tue, 04 Nov 2025 08:22:38 GMT  
		Size: 4.5 MB (4518315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a088c7f62806c4e667526c14c0857a47b468625e8fe920e0b3a5e5d7fd2b064c`  
		Last Modified: Tue, 04 Nov 2025 08:22:39 GMT  
		Size: 6.8 KB (6849 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ab1f0a34341a6ec7791a5ecaa4707840a2e39cf96ca8216d9e9b233ff79bee55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71165510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9d90c5ab1b49b976dc33597f7827d9e59f4d07114c68b754f035523a520c771`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 03:16:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0a071bbc557d9d42732d58a1d6434bf94baf5f06b391c076c996395c193e41bf`  
		Last Modified: Tue, 04 Nov 2025 00:12:11 GMT  
		Size: 47.1 MB (47138093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a580bca43f6d623617841d967d82ecc7cf55ebeb22ce79064b23dd0b4a10ce0`  
		Last Modified: Tue, 04 Nov 2025 03:16:55 GMT  
		Size: 24.0 MB (24027417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3f99b531a772e6fc542171323307be8816346f39371381baca6c8e8f9725e8b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4517311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf8ac7662e89639422bf146c4c2ee0fc11e0843e3ccc460f99ffa8f1f3a11ece`

```dockerfile
```

-	Layers:
	-	`sha256:7445465fb4ad6f9b0e92d3f6926826679ba840baaaf59731b8101fe8192008ba`  
		Last Modified: Tue, 04 Nov 2025 10:00:44 GMT  
		Size: 4.5 MB (4510495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db9b005fa9bf6ccc5defc48d52f1866a0c96d485ed6c7e18c8b0c34c3469eaba`  
		Last Modified: Tue, 04 Nov 2025 10:00:44 GMT  
		Size: 6.8 KB (6816 bytes)  
		MIME: application/vnd.in-toto+json
