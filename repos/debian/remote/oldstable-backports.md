## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:f4e36cc0215256f1255df8ca7ffe8eaf405b0c9967e801f962c8e2485e723bce
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

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:92f54a15f4b5b005a1eb0619c6baa39a8bd1411a71a920063e661e4ec4551675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48489003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da30e9dfc4f0d893be9fb02b5e48cc8b3e4a5ae4dcd1c9fd7d7fa307ed0d77f3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'oldstable' '@1771804800'
# Tue, 24 Feb 2026 18:51:43 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:aea3a0b839183380665b79229091a1411f529f3b24a4b76dc7c8a83ea8b6ace9`  
		Last Modified: Tue, 24 Feb 2026 18:43:11 GMT  
		Size: 48.5 MB (48488778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb8ffa01107742858089e9a79da7d4ac7cd19784bb2459fc50fc660372213c3`  
		Last Modified: Tue, 24 Feb 2026 18:51:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:fa9020356dc77e277f6c66875fa8b7f06f8c76630ac14b03543d37997a0cf6fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e8daa31d88c469dca357a20c0b33b56b3be69c3645d4f359fc455265f9f374`

```dockerfile
```

-	Layers:
	-	`sha256:ccc587be749bd26c33273596a0412122e72b2255d52eff7bb34795eb2502ffe4`  
		Last Modified: Tue, 24 Feb 2026 18:51:50 GMT  
		Size: 3.7 MB (3734076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d182a2d7caf6cfcaf589f7e1a29a18f84e6fc3ecc9bf908790a108d9912ce5f2`  
		Last Modified: Tue, 24 Feb 2026 18:51:49 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:5f24d7781e4f1625d2dc35e8bdf4f8ba30c5efcc824b26dd55513ecf56ed98c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46021883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4d49371ef1859c21dae65bb59d41b7dd0a5bea3461efc6e58ed506eacac8aa0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'oldstable' '@1771804800'
# Tue, 24 Feb 2026 18:52:39 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c846fd717552f2ee0bb4184cafde3c24da2beebc7dd4e91515298fe2444a18ab`  
		Last Modified: Tue, 24 Feb 2026 18:41:59 GMT  
		Size: 46.0 MB (46021660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a8808f2fea36f943446f5791a27609ac56170c7b0e3acaa6956cc54879aa60`  
		Last Modified: Tue, 24 Feb 2026 18:52:46 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:46cea6d38b0ea5b970c06325fdf72237cbba84ff37f7ede009a77297500abaa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c08f61f2b000e282e1c51bec3a5303aa74df4818a092c2e00e96759e712c31`

```dockerfile
```

-	Layers:
	-	`sha256:7f2f5db820506490561887c439a2f67a8a2e1bb9ffc813f9e46f891d5d51b1b6`  
		Last Modified: Tue, 24 Feb 2026 18:52:46 GMT  
		Size: 3.7 MB (3734277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92c723b3c16bf1447a51c6c41b7e7a6489f20dd01edc268d13c0b83f584b867c`  
		Last Modified: Tue, 24 Feb 2026 18:52:46 GMT  
		Size: 5.9 KB (5866 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:76f359ed1e74eafdf5137882393a1b8f4343fcc053813d81aa9ce44af66bb3d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44208051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a83e3f7463dba71803a4953821c3e303ffef56eee415c90d3131b142763fc903`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'oldstable' '@1771804800'
# Tue, 24 Feb 2026 18:56:02 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c968a94901f3b19ddeb57f5af9cd1d3c49d807278961744677d2fb27f85933d6`  
		Last Modified: Tue, 24 Feb 2026 18:42:23 GMT  
		Size: 44.2 MB (44207825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4db67e69605ad5a0d8b7155fabb142cf37821fd75917ae270f68c592b76b25`  
		Last Modified: Tue, 24 Feb 2026 18:56:09 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e7a3e194e33a52b0c522e72e2846dc3c7c12c603cdc4600f6c847a70de66224c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3742121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2dba067e5a2fd05e745d2da008efea3f1ebef36ec1e301d39ef34635180b88f`

```dockerfile
```

-	Layers:
	-	`sha256:ac5f842ac40f75c69c3c5625fdce919f452c02d3aa6f4daeabf6e8010fb0c3a2`  
		Last Modified: Tue, 24 Feb 2026 18:56:09 GMT  
		Size: 3.7 MB (3736255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52241bedfb7a6110750b24d69ebf65b4472fed5db9479545349e68ff5f67acb6`  
		Last Modified: Tue, 24 Feb 2026 18:56:09 GMT  
		Size: 5.9 KB (5866 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:c77e7df2210b95effedd741a0efce0e1e0e583e4e3774849d2adb36b8790faa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48373436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3e55449962b34d41f3bc1ad55c0b4799976dba72b3efad80ab96d81e301de1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'oldstable' '@1771804800'
# Tue, 24 Feb 2026 18:56:31 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:904d07d2475fd07efd70f176954fcbe9615a9d4dc89fde07b5c476806a8b7041`  
		Last Modified: Tue, 24 Feb 2026 18:43:02 GMT  
		Size: 48.4 MB (48373213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526978bb0a4205f6a954b0ef57680392632c80e9798325c9e0f4b324bc98eb9e`  
		Last Modified: Tue, 24 Feb 2026 18:56:37 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:12c9bc01d2e601315531afcc525a347f5e014b7210ac942f611314e169333f46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70cf93cbc42c14671d1149e367d36cdbe658d149c3e100977d5ca5f21649946`

```dockerfile
```

-	Layers:
	-	`sha256:b424100d85c2180200188228d5b72551b21c3c551753a26b5c0c427d43cf6e80`  
		Last Modified: Tue, 24 Feb 2026 18:56:38 GMT  
		Size: 3.7 MB (3734291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6032e941cc1fb0946bffb1e7b86f2313b677b677a5b35077fb7077616905b201`  
		Last Modified: Tue, 24 Feb 2026 18:56:37 GMT  
		Size: 5.9 KB (5878 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:5f5eafab759ed496dc367b8f0ccb58fb50ff1d4026636afa050320c43908e88d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49478084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45e31d2a207617aa57dd30abb63c35784ccd6cdfe2a5df97b50878422b21ccf7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'oldstable' '@1771804800'
# Tue, 24 Feb 2026 18:53:24 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8f35aa03a3d1122bb6dd5b376477130dfc756f834c71c057bb1f3b269b9e9f85`  
		Last Modified: Tue, 24 Feb 2026 18:42:23 GMT  
		Size: 49.5 MB (49477861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a9f621b3e390f77ffe70588cd3ef88008c0ee633a9f493bde7924587f9ee33`  
		Last Modified: Tue, 24 Feb 2026 18:53:30 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:52de965405fa90e1ee99a65dbaba388d57e518d8b617b96c5cfef7d41b432fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722945778590fb0c6a9949c2e1bde3f6b36d6d961b44ff037bd5a42d7416aa3b`

```dockerfile
```

-	Layers:
	-	`sha256:7c9626842cd9c48b9dd87cc3ea654dfaaa2edc259212db45bcea36d0eff90733`  
		Last Modified: Tue, 24 Feb 2026 18:53:31 GMT  
		Size: 3.7 MB (3731272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33f1d286d88f23b33af3c073be44cadf7dc59811072e4b1585714b2aea1694a7`  
		Last Modified: Tue, 24 Feb 2026 18:53:30 GMT  
		Size: 5.8 KB (5793 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:bf8f1d74524131ac9f0cc573260a724385d015e2d4582184916695a0856e666c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48782738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e5e53f591763da71667536ce69a0f676a063db855e9f461572bc78b2e31cd08`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'oldstable' '@1771804800'
# Tue, 24 Feb 2026 18:53:56 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:57b77bd37e73a6c01c646f8caf80c6a7c7e2079c6dfbd8fc4905db539b73639e`  
		Last Modified: Tue, 24 Feb 2026 18:42:37 GMT  
		Size: 48.8 MB (48782510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1ddd1019ea760cc0fccf2f04b23f4451189a2f14ca00c147cb48825b214d11`  
		Last Modified: Tue, 24 Feb 2026 18:54:13 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a46c3ae89d7a89db582bef4930e021d027a459026f5d7b36f82e53f4cb4c2c0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 KB (5632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65fec94b26c8dfb921812295153912d03b9a9ea34c3b6c498ec6d00ec5683a25`

```dockerfile
```

-	Layers:
	-	`sha256:5aba4a841a17f4db913d8cea8585ae7182346fd206555fc8a5cfb3d7299adbfe`  
		Last Modified: Tue, 24 Feb 2026 18:54:13 GMT  
		Size: 5.6 KB (5632 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:2dc1516c5a023aadc7d339eab6378331896ceb33698ab28739a5d607b34fd8fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52337027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b6ac6afc619fbcca0aa1051b5f5fe3e00f9b27101bea4565e0e3a49ee7f12a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'oldstable' '@1771804800'
# Tue, 24 Feb 2026 18:54:02 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:da1317e86242c74f450b977878d2ed53f0330a33b84b0bad125028ce138f136f`  
		Last Modified: Tue, 24 Feb 2026 18:43:05 GMT  
		Size: 52.3 MB (52336802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825df5c739ff7d090f8b7200b729b097eae2ebbba2fa6f8c7ac98f06a3481b87`  
		Last Modified: Tue, 24 Feb 2026 18:54:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:97fcf79dbcf411926206d16a9698aa7566d4c3e26aaa725535a98e9a75679284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3744270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c98bdeee8b9734a299706ec6ec1d987fafa694a5e7693610d25757dead4a5bf`

```dockerfile
```

-	Layers:
	-	`sha256:7a185b3ced1a9bedd6521879ba1cbeb2b884c05a330b17c957b98d7196daa2a5`  
		Last Modified: Tue, 24 Feb 2026 18:54:21 GMT  
		Size: 3.7 MB (3738434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b98903e700ff1f1294ae841e326c27d02b3100ee217e1c7fbfaea05a5cc51c25`  
		Last Modified: Tue, 24 Feb 2026 18:54:21 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:d06dceebb017b9c221c1b6912882e8dcef8abfff50d9d30535096a145dd0d7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47148315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2327445f7e955c18970568f4ca9fd1a0dace5adfb8fce5c0defd9722e0f17b2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'oldstable' '@1771804800'
# Tue, 24 Feb 2026 18:52:55 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:13c3eece7ec30eb0b511052312115dfe33385f1b7efa78631816a9f663b98352`  
		Last Modified: Tue, 24 Feb 2026 18:42:10 GMT  
		Size: 47.1 MB (47148092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba60724af1a91f37b22af8e302b382e7e8a8d9da3bd8e8ab2fc7631d1753e9f3`  
		Last Modified: Tue, 24 Feb 2026 18:53:15 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7342dd3ed9f0c0278b16be2ee8eca01cad3162a0dbe0722b3647bd6ce98f6db1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afb655fb6883fcff44526b9d16f5990d7a552b31fe09561ae1cbb10072809cc1`

```dockerfile
```

-	Layers:
	-	`sha256:11e4dc00cb8f56e82c43174a896a607158606590d0fe11ca32135ad14a248ecb`  
		Last Modified: Tue, 24 Feb 2026 18:53:16 GMT  
		Size: 3.7 MB (3730914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63c955d9a6f0376b72127f1cd82ef423b34ca2f8518bb091d2133c5178f4e381`  
		Last Modified: Tue, 24 Feb 2026 18:53:15 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json
