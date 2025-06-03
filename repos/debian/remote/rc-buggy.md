## `debian:rc-buggy`

```console
$ docker pull debian@sha256:fa0b4710d7ae067f938b6fb5e3afebed0bfac32e55b981e8b79f2b495b74479d
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

### `debian:rc-buggy` - linux; amd64

```console
$ docker pull debian@sha256:9fb7f960249012ca142f6f0b6975990834240d493161e08a7b56f8b68ef9e76b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49250775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de9e3ada96e03034fe37c4d39295f3e82e4f5d153b788c186dba00e9d486d432`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:21c8f2db1ca60de292da0e982c4bd4b81bfe468b8d652fac5b9003ceedf12013`  
		Last Modified: Tue, 03 Jun 2025 13:37:28 GMT  
		Size: 49.3 MB (49250549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc156c37878e51581c01ad00fa54196f95a7ce710af083e21d65fee2edb1b58`  
		Last Modified: Wed, 21 May 2025 23:12:05 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:5674aa3df2baac502c79c5184ae89133385cddbf79d541f4868608284c459c3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3090664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d383469aa625e41023675f688d251b38554e9cdd572e45a0b03158acc3ce67`

```dockerfile
```

-	Layers:
	-	`sha256:e2b718a4e837f6ff33bb5debdbfbe6e41ab5da178d10b2b408ac5cc81c7aafdf`  
		Last Modified: Wed, 21 May 2025 23:12:05 GMT  
		Size: 3.1 MB (3084565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb4b6b9c1cede90ad1340ec49a6a15c73c1956df1e3b76591f4eaa001d503e06`  
		Last Modified: Wed, 21 May 2025 23:12:05 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; arm variant v5

```console
$ docker pull debian@sha256:d79630f5f504d6c52dcf71e357645f0268fee00ed3d2a2607d2a487a0ee26fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47443118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43b473a8524a5ea4965da8598dcfc2eee8ade63cd0e6f4d2576ff8d37c4e0ab`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:0f211461130ff11866a85e649352ceeb2f6ebc110118114f92b30349c5de358f`  
		Last Modified: Wed, 21 May 2025 22:28:23 GMT  
		Size: 47.4 MB (47442893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8bf1ef901b2049251d961f8c84ce9e370ba4b9352fa6b08319ec10472e7657`  
		Last Modified: Wed, 21 May 2025 23:13:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:c0b9659e0b70abe72dd6ea5c9d37f9af5a6ae46ece232db20fc37a384a1f6a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3100041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d5507c3cf7dfe41c67f1eeedc4fd0018871a5b8541cc0f6bc8fbcf580e7baa`

```dockerfile
```

-	Layers:
	-	`sha256:e722c6c303fddd0e74f9540f8a47d814a637ffa6dc38029169c33d91cf90473f`  
		Last Modified: Wed, 21 May 2025 23:13:24 GMT  
		Size: 3.1 MB (3093882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dce1b606f09b44e93067d744869a94e53a3d280f40bb8218696597b3c807910`  
		Last Modified: Wed, 21 May 2025 23:13:24 GMT  
		Size: 6.2 KB (6159 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; arm variant v7

```console
$ docker pull debian@sha256:402576c58d5d50fb0cf3f42558bd44c86a5daa44c9d9c5b364d5334cff699d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45698855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78a63f6593da1caa532b591320c46c02bf97d3e6c9300b970a692946dfddb0a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:766cbe9ca16b5ae7e32cf18657be459754ce87056cceebf6831ed9c18fd8a62b`  
		Last Modified: Wed, 21 May 2025 22:29:51 GMT  
		Size: 45.7 MB (45698630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd09f7fcf2b7b761a82c1ed68a0c7f0ecf7bf121533c7498049c8ad4131898a0`  
		Last Modified: Wed, 21 May 2025 23:14:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:4d7977f1c63f36bc13d5746ad2936e89d55666755641028a346e7c1396312c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3092106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae1b40a4bad02722f88099fa19dacae6e274488bca28d933edc3e922c1be45d3`

```dockerfile
```

-	Layers:
	-	`sha256:b7a07d485463c64eed5adcea9de2d508903830dab0a82aab9e4591134c28935e`  
		Last Modified: Wed, 21 May 2025 23:14:47 GMT  
		Size: 3.1 MB (3085947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbdae115ca077256b43be02b82fba921575bc6a916c5cb9745aa86f6d6e2b243`  
		Last Modified: Wed, 21 May 2025 23:14:46 GMT  
		Size: 6.2 KB (6159 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:134f394c777937e7bf05ea7ef45aa95f8960aedb7c4957aee34fe10a47de8c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49618093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa6a09579d19dbf057b56824973a12820593ffc587516d9818ccbd8c53dd001`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:4d7c750dee99fc4f87ba2d4a7a97efd437e614ec9079e7fbf547ab9ce640bc68`  
		Last Modified: Tue, 03 Jun 2025 13:30:58 GMT  
		Size: 49.6 MB (49617866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a6fddc8e55feefd6e671056be4398960acc08978896cf622894298d1d8ce12`  
		Last Modified: Wed, 21 May 2025 23:13:45 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:7f461cf46a90ccafdc5520a9622f03fe2e7e99745ba9842c18de472e9c193108
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3092236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0575e1d85e848b218e8913a9e9fb5f4c335f4d01b9adfba81a5bd63e5315421e`

```dockerfile
```

-	Layers:
	-	`sha256:cbfb19fbf2993c5cf33b895de43de9b83243ca48a2aeba0fff5c93b02d569b56`  
		Last Modified: Wed, 21 May 2025 23:13:46 GMT  
		Size: 3.1 MB (3086058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc7f610f9abdf9f816830d32aa1ed5ab8b9d31e59e164b04798b7deeb5088569`  
		Last Modified: Wed, 21 May 2025 23:13:45 GMT  
		Size: 6.2 KB (6178 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; 386

```console
$ docker pull debian@sha256:115d1b30108ae91c78a2df11a5e82ea4afb57e98548f7296fd4554095b9dd350
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50760605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c688cef3cce6dd8ae3dc29ac684c61e6027a8c94889202efcf3dbdbcf9cbbbe6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:5c296d6dda96e0fb26dc4760b3366cec8a0723558334f5c902e1c373d0e43ab6`  
		Last Modified: Wed, 21 May 2025 22:28:10 GMT  
		Size: 50.8 MB (50760379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1821392b98f0d55096aaa26a08a6ed4411b0342a27aa5acec9b1ad1648d0f72f`  
		Last Modified: Wed, 21 May 2025 23:11:56 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:69b20dcd55d46e4fc7095007cc039f893072aa89060ea8574b902f13c17ff830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3087841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:face50f3a6e8aa8a1d5c18ede5bef02cabbe7b96ea48acdad6349f276893c030`

```dockerfile
```

-	Layers:
	-	`sha256:024c0b3e2a89aa8f95819ccbdee102c22a8d104cfc4ece56b36e840dcb5ff8be`  
		Last Modified: Wed, 21 May 2025 23:11:56 GMT  
		Size: 3.1 MB (3081764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ccabb423661384348189a58287f803c022d27637a617027d1ad2d964e34a59c`  
		Last Modified: Wed, 21 May 2025 23:11:56 GMT  
		Size: 6.1 KB (6077 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; mips64le

```console
$ docker pull debian@sha256:3f3522cc244f8b53d0e24904bc7fc5dec2551c22879ce1706f4a0f2571b10c74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49538548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffc96215dacc3c9d74c41c9d51464ec0df373968e26aaa2c22425f511383d4a5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:27b34307efc56192fd4ca945f6323e2158a324121ac08b2b6be4739d1a7a2345`  
		Last Modified: Wed, 21 May 2025 22:28:50 GMT  
		Size: 49.5 MB (49538322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971d21f9878ddd89b2325499718b323f6d1932407fb0e449bff9e78f82348325`  
		Last Modified: Wed, 21 May 2025 23:20:54 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:b61fa4d39afd98f24642fef207dddd59f631111ce26373f2e8c749ae758569f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 KB (5932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fa5753a11bd78a01d63d5fdda6f05a15fee799af644026731c6e1a4de6a4b3b`

```dockerfile
```

-	Layers:
	-	`sha256:96a902afbeb4c878b17a659caebc19fb34cb24a8bd1679c19c33451feaae6704`  
		Last Modified: Wed, 21 May 2025 23:20:54 GMT  
		Size: 5.9 KB (5932 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; ppc64le

```console
$ docker pull debian@sha256:fa9a9ac08621be0e35323ef21eab2445dfbec95f751c8030a9c83f3177b1b4d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53087241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4807f8b8e550b57d4a11084e7c745344c9648c730a9772e01fc02ba0861f23f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:16f5e7cd9c9945be6c34f81a399d644f442eadb5c4f47f89a090f84971e9d67c`  
		Last Modified: Wed, 21 May 2025 22:28:48 GMT  
		Size: 53.1 MB (53087015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf54279df24b6dad454a4e0abf8b772409e3f3c78de4a2f436206558861c06b`  
		Last Modified: Wed, 21 May 2025 23:14:56 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:f143c2c8dfa8e60c562dfc6aac14d3b416521d4d6d78be96ca9d3d82ee0347ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3100583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6450acd4d2c84944a21c07371852092f38f45a8b4e2b764f4dd5e76294a022`

```dockerfile
```

-	Layers:
	-	`sha256:5ebe2487c44202a6220dda0d91360af08f3bc1e3510a3c905988af8b1e206782`  
		Last Modified: Wed, 21 May 2025 23:14:56 GMT  
		Size: 3.1 MB (3094452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08810882487f9616e5e5499e472991f10f59964629266ca7271cc05400de853e`  
		Last Modified: Wed, 21 May 2025 23:14:56 GMT  
		Size: 6.1 KB (6131 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; riscv64

```console
$ docker pull debian@sha256:47e892616d9e26f3663833e088d182c37b8b74ca42078f55f8db94128e89fd96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47737783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e53390e89950cb9f1376e80aec981bb78ff41557664b83738094d399c5f4962`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:70274c6f176412a652733a045be62228bfceb31afa5c428bc73eb440514be7e5`  
		Last Modified: Tue, 03 Jun 2025 14:40:24 GMT  
		Size: 47.7 MB (47737557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094373b03423d5a4e12457cfd79e0bcb76b57bbb3bfd11381992f27744357ed3`  
		Last Modified: Wed, 21 May 2025 23:19:27 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:63f9d7fe4c8557517c1f0fd31782c0c819933e761574a755ef75f3e306802f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3083023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bdc0c7d5cb7a614eec4726468e15528f65f1e64ce5d21116455a30bf61bb6b8`

```dockerfile
```

-	Layers:
	-	`sha256:6c2fd59f85524099f79c078710838759f64bf2e031abff5d64041841c377460e`  
		Last Modified: Wed, 21 May 2025 23:19:28 GMT  
		Size: 3.1 MB (3076892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab897afabe6aabf6828ba7107746706261399674ed2d71a2461a1822afd6e96a`  
		Last Modified: Wed, 21 May 2025 23:19:27 GMT  
		Size: 6.1 KB (6131 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:rc-buggy` - linux; s390x

```console
$ docker pull debian@sha256:129c040b3190fea0afa88a0d43bd8cc31f1e995eacde2dc6953139e6bf3f44b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49325887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4ce24b77ec75189ee5fd4ba350191f0cc3ebd506c66354552dae8ca49ef3b6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian rc-buggy main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:719077674b144dec5ce39e78bd5eb75fa6363d159411371db443b10356484cce`  
		Last Modified: Wed, 21 May 2025 22:29:06 GMT  
		Size: 49.3 MB (49325662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dcf2aadb7bd2349d749223fa5b6a32c89e35f10f25a153f6a128b40e53e9a0a`  
		Last Modified: Wed, 21 May 2025 23:14:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:rc-buggy` - unknown; unknown

```console
$ docker pull debian@sha256:a72436d6583e78fa4d5df1f7dd297920ddd93a71d503c67460f4c6baf0b90dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3098483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b8c4be3af485bbf5cb942deae66f40c345fc39589c8f746ba8884d965d738aa`

```dockerfile
```

-	Layers:
	-	`sha256:42e23d4609a7db10c961471dbcc1971f0f313170dbf9d4c6ae8f1f68daba02fd`  
		Last Modified: Wed, 21 May 2025 23:14:17 GMT  
		Size: 3.1 MB (3092384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eec2487029b1b8293a84f62eee823b51c59ef0dfe2c5c6ec295968bb436340ba`  
		Last Modified: Wed, 21 May 2025 23:14:17 GMT  
		Size: 6.1 KB (6099 bytes)  
		MIME: application/vnd.in-toto+json
