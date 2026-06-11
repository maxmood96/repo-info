## `buildpack-deps:forky-scm`

```console
$ docker pull buildpack-deps@sha256:98626d2579eca42b6b667e08eb6e8111a656019128990dfbb8a34f16dceb45a9
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
$ docker pull buildpack-deps@sha256:de78026f57ace1c0cbf266796099d88d6dd30a12e256f3e589b3e1e59a6c84c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152621404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:887ce2368f0d8e615c7ed675071108671fd85e248af1b712b2a045bba00d5eee`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 00:42:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:24:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5721d6b62cfc7a7bfa692b95ea547e4ea39b5e2bfe1bd3e1a88886f80c2846e4`  
		Last Modified: Wed, 10 Jun 2026 23:40:06 GMT  
		Size: 48.8 MB (48779274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151e7f09040bcd4eed376c1a5f9491753b37de5abb58b8a75ba459283597e98a`  
		Last Modified: Thu, 11 Jun 2026 00:42:43 GMT  
		Size: 26.9 MB (26918682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179cae8636ce74da9ebed51456902f2692dd3678e97e9754ec177a9fa70c41be`  
		Last Modified: Thu, 11 Jun 2026 02:25:00 GMT  
		Size: 76.9 MB (76923448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:84742978c442bc71906a5b49fe711dcc5e4918ef072eeb19199da25c12c75197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8263164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c328402ead77b75ad253658b132c41887052fc5a80b36713fd8bc0ddf56466`

```dockerfile
```

-	Layers:
	-	`sha256:ca542a5aef985e5922f85d58c6f4ffbd4093ae5b30c8048cce6a1710abb12077`  
		Last Modified: Thu, 11 Jun 2026 02:24:58 GMT  
		Size: 8.3 MB (8255898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42a08af81e8932b6373dba0912b3d87744828b8c8e1d7034223be9e8e2f7613c`  
		Last Modified: Thu, 11 Jun 2026 02:24:57 GMT  
		Size: 7.3 KB (7266 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:89775f8ccfa18dd84285e7cef823c5188b8e97093175c92b562d4e169227dce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141690211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54e648ad0ae44ac3424e0070e245a3fea243ca846b3cc6128a3ea9589790537`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 01:25:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:44:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cd14977d91415ae0c2f3a09dcc1dbfa071bbc9d1eaf7ceed6655fe0e671e8d27`  
		Last Modified: Wed, 10 Jun 2026 23:41:34 GMT  
		Size: 45.7 MB (45676562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f62967a713e6868315df8fff6281864c11e6f1bf85c4ff4746f06a1c2c7935c`  
		Last Modified: Thu, 11 Jun 2026 01:25:13 GMT  
		Size: 24.6 MB (24579632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6ed9ff89ddc0e8e4bde82bcf767d8515b2d3abebc9c2125ed74145f8b0678e`  
		Last Modified: Thu, 11 Jun 2026 02:44:42 GMT  
		Size: 71.4 MB (71434017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c80f9354f22d4c2b136cef5e90db84f7516caebeac8b63c726bc08d96cc9ac18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8263133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa7307b655a2064d37cb5c42ab9b5df2045fa78e3a400079d9488780b141a62`

```dockerfile
```

-	Layers:
	-	`sha256:4e747053702bf423a9b1bbe4e8e9071bb0a234971a2d241ae84a5c4a304992d2`  
		Last Modified: Thu, 11 Jun 2026 02:44:40 GMT  
		Size: 8.3 MB (8255803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa7ff8ca311beac69635032fe4ea05c6557de467b7a85e40bea099a792ffe6b6`  
		Last Modified: Thu, 11 Jun 2026 02:44:39 GMT  
		Size: 7.3 KB (7330 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:74f313f375949d15dd392d02dd5942536b6a85aaec23d6cc52b0e136d9db1d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151067789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf042339bf86b99d500bd4009350f0697a50f2803cec1b8c334106ec4842fa52`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 00:44:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:dbdf5115192d6ba17e54d5f2d3cd16e18cba052a9281223f09caff8a3d00462b`  
		Last Modified: Wed, 10 Jun 2026 23:40:03 GMT  
		Size: 48.8 MB (48795608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436ebeebafee761b67c6633aca1ce7141531b193dc4a7a4858fb1b0cd75f8462`  
		Last Modified: Thu, 11 Jun 2026 00:44:25 GMT  
		Size: 26.2 MB (26180818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ee4c1e50172e312806c4dbe7a83e0af194a21bea22010950b3fa28c7df82f4`  
		Last Modified: Thu, 11 Jun 2026 02:25:15 GMT  
		Size: 76.1 MB (76091363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e996aebbb1fd127512bde8bf7f8d8adfc2eba41b534af5ea804dceb58dead5ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8274746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb2cbb4d0db785720e9bd45327c108b1e99d0a659f1790460d162c0e0412c34`

```dockerfile
```

-	Layers:
	-	`sha256:870c369ddf16c6f66985f43359653769d1f16c468f9bd6e5187b468291bdc084`  
		Last Modified: Thu, 11 Jun 2026 02:25:13 GMT  
		Size: 8.3 MB (8267400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c481f5962014201db13eb82363ac0dba434ce5577cc948e98cba6d0b3daa58bf`  
		Last Modified: Thu, 11 Jun 2026 02:25:12 GMT  
		Size: 7.3 KB (7346 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:bb6bd55414d08961f2d22e5ae15293f96c3e7edfbfe3554c08b427a0ff57934c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157316496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d78a340e99ca4988949853c3e11099d24d939b25a536f6fb9018e717bb5b94`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 00:45:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:24:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d6a4be7a6be3ed3c4d92863f22edf1e7aa21046c79f8c96f534040141953aff3`  
		Last Modified: Wed, 10 Jun 2026 23:40:24 GMT  
		Size: 50.1 MB (50076810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efb4928ebe54ee107e6463403a2a4853abe521d8dabe3603a0df92499fa85ed`  
		Last Modified: Thu, 11 Jun 2026 00:45:11 GMT  
		Size: 28.2 MB (28164931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d199197c3ac4542d3e5be264b601c0923a198de45a4b527c9ba6b3bd662bd12f`  
		Last Modified: Thu, 11 Jun 2026 02:25:02 GMT  
		Size: 79.1 MB (79074755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ae786e793e6f17783a811c83a271ab1321e5ad19ca23295725d4c16e6cc31386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8258633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432c58c194570b3853acbf77d2e14d5e7f1a1a12c76b320cfae19af801ede9c8`

```dockerfile
```

-	Layers:
	-	`sha256:885647d61370a1132ee42f5b0256af258a6934656d88a8fd6e0722f2f1785cd5`  
		Last Modified: Thu, 11 Jun 2026 02:25:00 GMT  
		Size: 8.3 MB (8251389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:184250539e40921896803d08282cf80aa5c586648e8eab56ce4ae6eaaec36238`  
		Last Modified: Thu, 11 Jun 2026 02:24:59 GMT  
		Size: 7.2 KB (7244 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f23a656104ff37603d66b08dbadee385f3d034582f12cfcbab57ad51b4009a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166751228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40118e7055f963d9315f64da0ee4b73e7f87a60d74de651e5397695a0ab2f62e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1779062400'
# Wed, 20 May 2026 01:13:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 06:51:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:2e5564b9da7290f7430ffd86cfc5f2b22a68586fade0aa81c8610704c43fd41e`  
		Last Modified: Tue, 19 May 2026 22:35:40 GMT  
		Size: 54.0 MB (54021281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24877c775bac285836892c60f877392eff4299b16fa48a35fb91c222b64558d`  
		Last Modified: Wed, 20 May 2026 01:13:54 GMT  
		Size: 29.3 MB (29285894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4dc79d08e369fda0605c037025da8b1333ff074dcf4bb801aa3f65c8ba0a35`  
		Last Modified: Wed, 20 May 2026 06:51:44 GMT  
		Size: 83.4 MB (83444053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0e5269854ab2c6d586b111a966c6bc3631a411c6a7d7aa8b07675a6a9fb15c3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8260159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:278e6ab5856a94fd1a4d23d1bb65cbcffab583f07989ec64cef3d616e4f39d0f`

```dockerfile
```

-	Layers:
	-	`sha256:03d62303dc507ee61bc6cb27960caf658e491c81b9eacba9d7fedc882256a369`  
		Last Modified: Wed, 20 May 2026 06:51:42 GMT  
		Size: 8.3 MB (8252861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4595418f93ac97cff4bea8c02008a38b099d87ab6d13f67d11d7501635c2c01`  
		Last Modified: Wed, 20 May 2026 06:51:41 GMT  
		Size: 7.3 KB (7298 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:ad6ab885b9be3afbcf3071bb96ba16b619fc1be388e79015fb82ee40fbbb462d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149379171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a2c6f6d1fce9383f97de64869526ea4ade528cd9717de172bbb7c5fd5b48fd2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1779062400'
# Thu, 21 May 2026 13:54:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 23 May 2026 06:35:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:233e2e85000f46d884ecdf2b81662e2915ae4bce2cfd6a573318e4ae99ee6839`  
		Last Modified: Tue, 19 May 2026 23:36:02 GMT  
		Size: 46.8 MB (46833187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa3768beafc01f566f53361a18d9c7150398a0575500ad1f3d3da15fa52ceea`  
		Last Modified: Thu, 21 May 2026 13:55:52 GMT  
		Size: 26.5 MB (26452165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08cd7be41266745c4f7d19936b352c5ff3ac5eb09c842b6781680c621924b23`  
		Last Modified: Sat, 23 May 2026 06:38:55 GMT  
		Size: 76.1 MB (76093819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:613eee62aa43cebaa06ff590e2c9af822a492b11263ade2ff8986902fb8f1f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8263602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d1cb070ee6a06ed3de52fd1655cdc212df7631daac8b1dcbc289549b5fb791`

```dockerfile
```

-	Layers:
	-	`sha256:38029cf1e049724d577786c6b4e207e317e8c1edc05db2666bacbe8a63e25a34`  
		Last Modified: Sat, 23 May 2026 06:38:45 GMT  
		Size: 8.3 MB (8256304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c28c4b4e165588095f629dbf28cece23eb539d54e37e8c8b463e83a253c2ecb`  
		Last Modified: Sat, 23 May 2026 06:38:42 GMT  
		Size: 7.3 KB (7298 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:505842d071c75c8e342d17e7235af47031195e371f18abd13354eb6cb3975a1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152668601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c887cae119bdd3858743c49f2890c8c0ea64949c306e3a3ca0ff5b08a109db41`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1781049600'
# Thu, 11 Jun 2026 01:43:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 03:26:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5198203a924daa24fe6af49f715c31ab29dfca39eea778fa09abc744d2bad231`  
		Last Modified: Wed, 10 Jun 2026 23:41:11 GMT  
		Size: 48.5 MB (48513108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede4a9f8d2cf16954d7483762c1a757bd649ba11bd48dc0e08d51861877f2e58`  
		Last Modified: Thu, 11 Jun 2026 01:44:12 GMT  
		Size: 26.7 MB (26680114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccda3e4041c62fdf0380dbc6e327f0ed32531c1d9a4fb592c7a1580acb6a13d0`  
		Last Modified: Thu, 11 Jun 2026 03:26:59 GMT  
		Size: 77.5 MB (77475379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:566c82e3e5428f6999e4006eaa2288ad2feedaa108ceee4333945777bb6e0b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8241018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:becd8f6b371022159b85bce576d8b4d21c5f1ff8900f29856368dbb66bda1acf`

```dockerfile
```

-	Layers:
	-	`sha256:be85d9037f7647860ee660636dcdc677aa95c70ff7c5f0e8a1f13a215a6547f2`  
		Last Modified: Thu, 11 Jun 2026 03:26:57 GMT  
		Size: 8.2 MB (8233752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab875089c0a5d98d387f0ae494152de8a31e61cb2ff6e196df3f8fa38dcf34d5`  
		Last Modified: Thu, 11 Jun 2026 03:26:57 GMT  
		Size: 7.3 KB (7266 bytes)  
		MIME: application/vnd.in-toto+json
