## `buildpack-deps:forky-scm`

```console
$ docker pull buildpack-deps@sha256:811a30c3e74654d2b9ddee99e91f72252319b557d6c7bb32a1b6f9dc99826b54
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
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

### `buildpack-deps:forky-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:3e508d8d0d148ba9153f32353aa45cce60b5ca851795749e3540da0cc479436b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152675607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09dd70a726009777ff45dd865cdf77a0f0773c5badaefa6d0d953d846b7c16d9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 01:39:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:45:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a35d765211154bb582ec48d2d95cc0c5953f360f8d0a39b91475c8b05f9c59a2`  
		Last Modified: Wed, 22 Apr 2026 00:16:42 GMT  
		Size: 48.7 MB (48697651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e592cd2ed9323d51731ff2e060da4790d904454d4dd8c0f58dc124b12854233`  
		Last Modified: Wed, 22 Apr 2026 01:39:43 GMT  
		Size: 27.0 MB (27008002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68baee722d285caf3b4327e15b2205e5b417d177e480c8c55a3ed01842c26381`  
		Last Modified: Wed, 22 Apr 2026 04:45:29 GMT  
		Size: 77.0 MB (76969954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9c3180b9da28ac113a6c93d3d03d5ab4b824e5c18172834fd55ab831962fcfa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8281134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb6c8bdd1a12caff19f6fe8721b9ff2a8552a65533046e42a27b57bb0b43e28`

```dockerfile
```

-	Layers:
	-	`sha256:a3034539a306adf9dcf2edfe6bb507be7701ffe50418058a80e8cd3857e4d0f2`  
		Last Modified: Wed, 22 Apr 2026 04:45:27 GMT  
		Size: 8.3 MB (8273868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92de776e45bdd3108c312164b6a6a45e62429214edc8e89a4867d73dd1ce37ee`  
		Last Modified: Wed, 22 Apr 2026 04:45:27 GMT  
		Size: 7.3 KB (7266 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:1eeeb119c701a16d6ff3855cc9a4bb848dd592fe89f92423bdbee3d9dacf8171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141782130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf23a14c75c8223cbf7c43712562b59d6bfa263185736234fae658dd8d82a86`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 02:18:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:52:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:616f54f84dee8932180832c344695078e63789301eb12467ca880323e3400586`  
		Last Modified: Wed, 22 Apr 2026 00:16:48 GMT  
		Size: 45.6 MB (45622135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61970639d217085f63010f6da0cad6e9f8e048924120803b4eb157ac1c2f651a`  
		Last Modified: Wed, 22 Apr 2026 02:18:59 GMT  
		Size: 24.7 MB (24685888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd2d4b24b5c349381f6b7163ca764f633bfc2f44c28abd2ae354570db164308`  
		Last Modified: Wed, 22 Apr 2026 03:52:38 GMT  
		Size: 71.5 MB (71474107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b60c7215904db79238b8037d953636f150b741e04a0f6136317dbec6839a10be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8279692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72c14e0f243979a01ea6f04a7b261647d8d333eb380707414654bb9513484220`

```dockerfile
```

-	Layers:
	-	`sha256:b636d6a5a8c20116513e73805d0036b9849a4de6572613ceb0b5c51a6b17ddcb`  
		Last Modified: Wed, 22 Apr 2026 03:52:36 GMT  
		Size: 8.3 MB (8272362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2d1d0ab046723f2f0b58a45e9e64ae0046447b8a735613f1b381e4d953e37b7`  
		Last Modified: Wed, 22 Apr 2026 03:52:36 GMT  
		Size: 7.3 KB (7330 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2f2b5e0b8db4ad59c74d02acb39480fb1af3444ac65fe569a2f8b1c5558bc2fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151120147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcadea832e931e7a0d5b6ada5d4b5d70a07b2b8e39cdf53dba19ae2677eb9762`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 01:43:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:52be3b7a34a0f7d63c36fadfd1767c3f064e11b65df7fb6243fae9b94dd9f7c8`  
		Last Modified: Wed, 22 Apr 2026 00:16:24 GMT  
		Size: 48.7 MB (48726104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7406cf4524d3710a69a6e4bbba357df8393b55da990695b89997aa04b54031`  
		Last Modified: Wed, 22 Apr 2026 01:43:16 GMT  
		Size: 26.3 MB (26289212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943416c03b0fa211b9ad3c070b785a9f8b5fea034656c1157181cce52e7b2b98`  
		Last Modified: Wed, 22 Apr 2026 02:32:45 GMT  
		Size: 76.1 MB (76104831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:57ed80bcfa0b8943ce74b88c4dc802168e8eca4d13c7ca61a75389a3435d9390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8293997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba864d32c01eec10c2ab54925e3746b571ec793bd8d8e25a240f1756952380cd`

```dockerfile
```

-	Layers:
	-	`sha256:c1249563bba592edc76d023e0b24309b336e37d6f96f6658b0d6a4a084c87331`  
		Last Modified: Wed, 22 Apr 2026 02:32:43 GMT  
		Size: 8.3 MB (8286651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c54dd03c62221549f69e73b3d4f3f3c0f0bfa0cd03dae32932289d641b1e3d3`  
		Last Modified: Wed, 22 Apr 2026 02:32:42 GMT  
		Size: 7.3 KB (7346 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:64f3b87958e0da9203286837b624274dacebcd4772bb8bbde2911c1756a3331b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.8 MB (156768362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0610db926d652c108609ab9e884476c9491a5b1387c727bdc79d9b7aa73daae7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 01:46:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 02:40:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0c655e94b1afc0d0a4a69ff26686a8cb9fd0349459a4008b02fd7dcb3e6d3ab8`  
		Last Modified: Tue, 07 Apr 2026 00:11:22 GMT  
		Size: 49.9 MB (49878389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74970d6f811b29c802a9f3c8d694bfd2f422255c20b66bcc271ba0c7bcc9dbfc`  
		Last Modified: Tue, 07 Apr 2026 01:46:17 GMT  
		Size: 28.3 MB (28298911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d376180d010f10a41a07c62fb3fa00f2442ee96ea8b7248d80a02311ec598b1d`  
		Last Modified: Tue, 07 Apr 2026 02:41:15 GMT  
		Size: 78.6 MB (78591062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9a45cb274c8a7af0a80a5848b83453fae2e5ccc39242c868ea43da0eae6d8668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8226274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80973f30cb61325a442d6084dd1bbab83f05bd0c6662a4694fd82e19a2dfafc7`

```dockerfile
```

-	Layers:
	-	`sha256:6ef44f3aa378e314757c6cdcd6a61a90987ed6b15baa75e301d1e6b0dc00494f`  
		Last Modified: Tue, 07 Apr 2026 02:41:13 GMT  
		Size: 8.2 MB (8219030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e8bb9794351945970eca4081106c685dba84b3d5e020ad71c11aac839a68f15`  
		Last Modified: Tue, 07 Apr 2026 02:41:13 GMT  
		Size: 7.2 KB (7244 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0fcc7a1665fd2aebf004502d23a67217572293504dda714a586ced21799efd3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (166031976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e768f5d93add2098643f500264830a8c9c6f5255d064288175fda4a8d05c87c0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 04:21:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 09:52:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:82a75a893b6c64944c6f9a45687c1a1f96d90f40ac32f7359ffe0b6755458be4`  
		Last Modified: Tue, 07 Apr 2026 00:10:12 GMT  
		Size: 53.9 MB (53851237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b159d77ae23ff0a537f251333a902815f558c4d2eb7e7cb1124f2b5ba37262e`  
		Last Modified: Tue, 07 Apr 2026 04:22:08 GMT  
		Size: 29.3 MB (29318642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea75b9cbb530f46935065289cc64cf7b3ac3d21234960ebf989aceb6ac5630b`  
		Last Modified: Tue, 07 Apr 2026 09:52:53 GMT  
		Size: 82.9 MB (82862097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:90b0b20ced25e406939c883f559f2514256cc26736a137c1a3e29543f5b65be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8215703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0801241440c54497770fdf5ae7493aa74cc88ffc0500fce6e18cbfaa6abc5d8c`

```dockerfile
```

-	Layers:
	-	`sha256:c38af59c4589d106d4766fc62156bd24e11833b95225dc5a88298fd71bbd8cd3`  
		Last Modified: Tue, 07 Apr 2026 09:52:51 GMT  
		Size: 8.2 MB (8208405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea05e9a154de790a6601cdd14c20dc4e4e819acaefc00daa8494bc628d1f091b`  
		Last Modified: Tue, 07 Apr 2026 09:52:50 GMT  
		Size: 7.3 KB (7298 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:f2cc8e10b94534aa989164bce1b767bbbeeb118c794611da909672226945aa62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.0 MB (148034955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f55d4318ebc13a989a95f99b7229243c4319dbced93ff2a17a9d253355e598f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1775433600'
# Thu, 09 Apr 2026 01:46:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 11 Apr 2026 02:45:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:63b5561c308233dcf634aa914acd8af4b95568018df569d4d43c4791c98cc9ba`  
		Last Modified: Tue, 07 Apr 2026 01:40:28 GMT  
		Size: 46.7 MB (46698175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d867396e8c8691cbd2e099e7a0d3c7c33eed2261193868cfa5cfdebbe037af`  
		Last Modified: Thu, 09 Apr 2026 01:48:33 GMT  
		Size: 26.6 MB (26580851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30d7c78d4e0f683fb07cd5e1493fc6c006352c3197e1c49758dde411d0f9d76`  
		Last Modified: Sat, 11 Apr 2026 02:49:35 GMT  
		Size: 74.8 MB (74755929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c9642b5b7edfdf0b74fe345a8b48b9b171a9d207b4a386f93fe7e2a2702267f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8219836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:650bca5e8b5ec33951b35abbb5496b9c40557d15687e14f1a86f8f466bb01f24`

```dockerfile
```

-	Layers:
	-	`sha256:1139cc032240bb1bdd9ee015d042f58bc31e82b7b6f5c76a3664d7e0857508ec`  
		Last Modified: Sat, 11 Apr 2026 02:49:26 GMT  
		Size: 8.2 MB (8212538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c15c539e7cac7f5ee96d86c7d672dd0bd487bbdc91a0188571fafd1dc1089d23`  
		Last Modified: Sat, 11 Apr 2026 02:49:23 GMT  
		Size: 7.3 KB (7298 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2cc36eca7c31519228f0044de4a5c6c93cb2ad156d4c0779008da030c9220784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (151987368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ae4abfe35aa643d87291a03ae576441cec8bd8c53b3897935e771dc8542586`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1775433600'
# Tue, 07 Apr 2026 03:04:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 04:54:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d387cf27b8c74bb29905817ad867265b401af02fdbc21b522a98041e86095a47`  
		Last Modified: Tue, 07 Apr 2026 00:11:00 GMT  
		Size: 48.3 MB (48291595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71640c6f0517962fef2d2cecd2252a1ad50dd36dcdfc5949b497510671693745`  
		Last Modified: Tue, 07 Apr 2026 03:05:15 GMT  
		Size: 26.8 MB (26816201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac6d200d226dcb1e9ec18c10fb8ae6afd2e2e5f3a76506193fd7ffbd528f5de7`  
		Last Modified: Tue, 07 Apr 2026 04:55:09 GMT  
		Size: 76.9 MB (76879572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5e56e53f0d8774856fa48ee560293010ec28273c8b83ff2000fd5df84c54a438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8209449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7efcf8b975d755b786c47b500517500dffcc6d38b0b5309a586e9e1564ab6aa9`

```dockerfile
```

-	Layers:
	-	`sha256:ef006bdae96dac3cc1d9789fb4f294994c74dd314b2f8b9226e47acc48b1d652`  
		Last Modified: Tue, 07 Apr 2026 04:55:07 GMT  
		Size: 8.2 MB (8202183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a83ebfeecd304edd0a398b6b8e8bfac9780baf51a665a566a327014c9082d87`  
		Last Modified: Tue, 07 Apr 2026 04:55:07 GMT  
		Size: 7.3 KB (7266 bytes)  
		MIME: application/vnd.in-toto+json
