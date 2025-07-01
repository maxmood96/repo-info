## `buildpack-deps:scm`

```console
$ docker pull buildpack-deps@sha256:3b97ea706c0141790a261f01b4ed18cbad55825bdb5a307905b14bc2b885de54
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

### `buildpack-deps:scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:fab1b6389a07a117b06169a1c2bc5a4a3d3f5d7315dea5ebf4d7ad49606d7f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136909774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:184202217278e8f818fab1583a99bbd9a5899a5d461e1fbf45efb3e3bf02dae1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eb73e993990490aa137c00e60ff4ca9d1715bafb8e888dbb0986275edb13f`  
		Last Modified: Wed, 11 Jun 2025 00:01:09 GMT  
		Size: 24.0 MB (24015708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b8a0660a31403a35d70b276c3c86b1200b8683e83cd77a92ec98744017684a`  
		Last Modified: Wed, 11 Jun 2025 00:02:18 GMT  
		Size: 64.4 MB (64399794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:11e44d930a2f569bf0fa1a303f10f1aebc4f579351fabc75178981a453284443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7965233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a9519b3e2b7eb9fd89b6722558ef430c8b9b2f927613ce81e24bc085c9a3af`

```dockerfile
```

-	Layers:
	-	`sha256:2c4a4e6e6d9c9a2d2628943c7e558ad6c32d7c26b62d59ec013e043b548f60ff`  
		Last Modified: Wed, 11 Jun 2025 02:23:50 GMT  
		Size: 8.0 MB (7957578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e5556a6a3d30aa93a721e0ffbafa0679def010d6d8d83615fd0eac148f6f901`  
		Last Modified: Wed, 11 Jun 2025 02:23:51 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:cdfcb170210ec6c51287c3177bb79057400d58cb84f4a84fd1989592591c950d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130718688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f6fbefe8b727cb31305ba562577b346203bf161c2ea7f39c1ba7907a902f9c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fe4bc1cbdee9e4aabbc6c58a2156f300e4c3158cfb501698b1878215892a8763`  
		Last Modified: Wed, 11 Jun 2025 00:30:31 GMT  
		Size: 46.0 MB (46026587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7973a0421a43933f783f2da8c4e6210bbcb63636694bdb47f5939d46f0cd8e74`  
		Last Modified: Wed, 11 Jun 2025 03:12:54 GMT  
		Size: 22.7 MB (22694196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd263284be736a4785fb0c489cf441580757a05d8cb52c26f07ba8f071d621a`  
		Last Modified: Wed, 11 Jun 2025 12:34:20 GMT  
		Size: 62.0 MB (61997905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0314cedd08a06fd1588c2af9b91cb4b081afb72ff3ce961654dbbb80b980d569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7967167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b43b876192810068fe65aef4941d76241e1a48a423989cb377fb316529cd5966`

```dockerfile
```

-	Layers:
	-	`sha256:9749d89ef0486d90b067b898cec7d94f9288de39b764254ed572e9a1e1d9b38d`  
		Last Modified: Wed, 11 Jun 2025 07:19:47 GMT  
		Size: 8.0 MB (7959444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bf27f80968b372da4324bf3438d9f73d11248ba8ed9c8deba30b3864cd3dce9`  
		Last Modified: Wed, 11 Jun 2025 07:19:48 GMT  
		Size: 7.7 KB (7723 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2ff4198bcf865923d022cd6d0841c74edcc17a6f2e63516899f3e0cefef65c72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125789771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e330ef581600e7fedf524e08d9c7ae8fd8e7e548a5f9fce582ed29faf05b6aa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:df7fd9070ca37866fcc3543148432e42d1e1723497b9b47c1e35615a2ca676ec`  
		Last Modified: Tue, 10 Jun 2025 22:46:46 GMT  
		Size: 44.2 MB (44208210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7ffa2f9b76643f2e264873b25d4450552d1d018f96ebfda08d41449ffa7dad`  
		Last Modified: Wed, 11 Jun 2025 06:07:15 GMT  
		Size: 21.9 MB (21924642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe8855ed7a68d9f8fe7d302fae88c166a75915bfbd2d109d79128b51764e3ec`  
		Last Modified: Wed, 11 Jun 2025 13:11:47 GMT  
		Size: 59.7 MB (59656919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1f001ed674c422cd3c4531484a047ccbb83c77b6b67638904e542b76983d7c31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7966586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6685c1ffb1281b5d283499a9d6757caf4d2a965be858d63cc0aaf7720bf4d648`

```dockerfile
```

-	Layers:
	-	`sha256:79994d1fc362a7b02c51ee81563ba29f2e5c5eb7d73ba6731435c516083f534a`  
		Last Modified: Wed, 11 Jun 2025 16:19:54 GMT  
		Size: 8.0 MB (7958863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:107672138441adad9f55e241db0203c1314e708d637f79e53fa33d31e5383bb9`  
		Last Modified: Wed, 11 Jun 2025 16:19:55 GMT  
		Size: 7.7 KB (7723 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:cbaf1b8bf88156c0fdef725edb33c34a5e1e2b69b0a9dc64f0c3211868670db3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136253261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c9e0090d3ef403a9382192f9e68672dd37cceebfe69f07a1a19bd30f51ccff`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e137b9ec173f900a44376f31987bb15c0f5bb562aa6f8ad5db5a090ec88b2e`  
		Last Modified: Wed, 11 Jun 2025 02:56:23 GMT  
		Size: 23.6 MB (23551557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f5719d6358cc525f45e16c04ce36e5245978df9021dec8d0619729d9de8537`  
		Last Modified: Wed, 11 Jun 2025 10:32:40 GMT  
		Size: 64.4 MB (64362852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:65450536dc5c794754729d5b04512a9bc4fb57dcf85417dbc5dacc60dd9627f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7971730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a5bf1c52c36a633cc0685e43086a5bfc3f395a73b52eea730922a54c72e41d`

```dockerfile
```

-	Layers:
	-	`sha256:1f5d8b2f028541ffb1bc0ae84dd21954fe2c57c244fe922c2a668e3232e86dd4`  
		Last Modified: Wed, 11 Jun 2025 13:20:01 GMT  
		Size: 8.0 MB (7963983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f01e71f401688719f25ef4fe439e2ae61e13ac5f1516109454d94de7cdcbbb3a`  
		Last Modified: Wed, 11 Jun 2025 13:20:01 GMT  
		Size: 7.7 KB (7747 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:7440bffa3edfe318d5b5272ae65e72c9e0409c758eece13e667eaac1b9d8d0e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140559671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b4486d446a9af6b6b4fb571faaca94c06d6decc7f6444c49c009e0b05145f52`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:3477877077c4dd3cd4c5555fccaa126bf060154fdda28f3bd49fdf6b50940639`  
		Last Modified: Tue, 01 Jul 2025 01:14:34 GMT  
		Size: 49.5 MB (49477421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62c8f46577375004356dcdcda0b1eb9cdda01e0943d00443270daca69a2ba1d0`  
		Last Modified: Tue, 01 Jul 2025 02:24:27 GMT  
		Size: 24.9 MB (24856933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2952009550cca50c5a8b42bdeb6e9116dacc2baceb5799f97bf16934eed752ae`  
		Last Modified: Tue, 01 Jul 2025 03:20:00 GMT  
		Size: 66.2 MB (66225317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:83e054b03e5a5d9ff20dd3290749a077812d71baa3f314f2bfdcd83ae6182fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7962721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3981fba1870d9fd3220ffcf022fb36b7c1e6e56f6c5d97217d29eb2b24b4af10`

```dockerfile
```

-	Layers:
	-	`sha256:cde02496da231e6ac29718044c3cfa791e4dd425cdeeb814faf539c40a9c12c5`  
		Last Modified: Tue, 01 Jul 2025 04:20:11 GMT  
		Size: 8.0 MB (7955093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93e57414e82f867152f2876c6d4a1a8f41be7b69b31077265d5af4e5580f8210`  
		Last Modified: Tue, 01 Jul 2025 04:20:12 GMT  
		Size: 7.6 KB (7628 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:c5fa8aa15c9d9b6d8a8231fdc3bd876bb4cd3ae156165aa0012717d09d5d8b49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135682904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beedefecdfca808792d43e8ed0999fa21f700419443b0e4207a8c23b12433573`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:348f1ed415b5b1e1f9982a78ffeb15637cbc5b41f93b83724c5938c2c226a58a`  
		Last Modified: Tue, 10 Jun 2025 22:47:59 GMT  
		Size: 48.8 MB (48775597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ad14aceadbd8dec6fff454480e4e098f48c504f528663aa483f102aed68047`  
		Last Modified: Wed, 11 Jun 2025 13:00:39 GMT  
		Size: 23.6 MB (23598558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1117c8734bd4897d340d37aa929ac7b2c46b5a9f691f51a958aabc871f6639b1`  
		Last Modified: Wed, 11 Jun 2025 21:03:24 GMT  
		Size: 63.3 MB (63308749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6206653cbd2aef53c06e2d9a0e2a3c484f1a46ec5abdfd9eae047797fc380aeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 KB (7497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70985218f874530b5d6fb2a079b9c1603e2f0228173b95fc9ddc7c3f0406ed13`

```dockerfile
```

-	Layers:
	-	`sha256:c8859a87661d317ba7efcac029bcd846de7f4ed57b5780bd3d2bf6626194da60`  
		Last Modified: Wed, 11 Jun 2025 22:20:04 GMT  
		Size: 7.5 KB (7497 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:797966dfd3d642ec48a4f7203cbc788166fbf1170ee064493e00390e49319fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.8 MB (147834478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3d9912717fdf101c885bc3ec99118c85fde6e69147a5e2118901dc1316ba238`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:65d348c3abfb8493d4b77022d58f0afc8e2daa19b2af853f803aef5c836212f9`  
		Last Modified: Tue, 10 Jun 2025 23:28:11 GMT  
		Size: 52.3 MB (52337357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bcd3217ebdd78ee7f5f6a67c7b4b49ee252ec2305007272d04d562f9e83004`  
		Last Modified: Wed, 11 Jun 2025 17:40:53 GMT  
		Size: 25.7 MB (25657425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f5e3e648b0af066a27f67ff1ab192ecc1e665ef5dd174521d0a856b9bff018`  
		Last Modified: Wed, 11 Jun 2025 22:39:56 GMT  
		Size: 69.8 MB (69839696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3f80cf5c76e7bb9c56e8878161457bdeecf1eae23b9509875c7bc0487eb42f84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7973138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae06bd1232d1e6d747067396d7daf96d02592efc2ea4e2cf673d9869b12fcdf`

```dockerfile
```

-	Layers:
	-	`sha256:bc5dd0d61de288bd8c7caf288b549a26bdeacec216037288261dda7ee6b7ba3a`  
		Last Modified: Wed, 11 Jun 2025 22:20:08 GMT  
		Size: 8.0 MB (7965445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40df6d81eaf5107ff771042c2ae96b4e7982584ec8225db875807d3c911a483c`  
		Last Modified: Wed, 11 Jun 2025 22:20:08 GMT  
		Size: 7.7 KB (7693 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ed843001f1b3f45c73bfe95d6c5c067510fa8f1b86cfd16c6307b6c49791de72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134662657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b864fb3b6a800dac1ce099df7d0b6216bba96b9e317391dc4209230fe361be0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:92d876c60c42d9677caf30587cba2266fe6860ddc50efdd0a6fcec154e589f76`  
		Last Modified: Tue, 10 Jun 2025 22:48:13 GMT  
		Size: 47.1 MB (47149408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83030d8a694f635685bec1602230ad1d5fec4773d5158ddbd025887cae3655fe`  
		Last Modified: Wed, 11 Jun 2025 10:15:26 GMT  
		Size: 24.0 MB (24015002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c056714c54676358218cd75dc0c5d3298e3c0e7e53c127fdefd363c4380d95`  
		Last Modified: Wed, 11 Jun 2025 12:03:11 GMT  
		Size: 63.5 MB (63498247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dc32bbdf9d44466eaedff6acc5ad7bdeabfdc4beb5ab74791492facc4256004a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7961546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c2bb39e400e75651d2dc5efa9cde5f82cba83e6951377c19db2b4a41c109ef`

```dockerfile
```

-	Layers:
	-	`sha256:58c2b4dfcaaaecfbd54d26cdd3dd84504db2f75c6f408381ec6c1852140bd577`  
		Last Modified: Wed, 11 Jun 2025 10:20:06 GMT  
		Size: 8.0 MB (7953891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c3346c436426297438c1589aa23161365020410347a2df0f78b9103958a5cfa`  
		Last Modified: Wed, 11 Jun 2025 10:20:07 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json
