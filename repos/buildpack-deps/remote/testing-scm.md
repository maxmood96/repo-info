## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:d1fecd7b209f91f197a7a3ff3563326e040ba4d8089c4dd602c010d1f2ab1c1a
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

### `buildpack-deps:testing-scm` - linux; amd64

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

### `buildpack-deps:testing-scm` - unknown; unknown

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

### `buildpack-deps:testing-scm` - linux; arm variant v7

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

### `buildpack-deps:testing-scm` - unknown; unknown

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

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

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

### `buildpack-deps:testing-scm` - unknown; unknown

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

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:334361a1bf3f29fe6f8acaedeec7f7345ef63dfdac922742bb891c530a9e2560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.4 MB (157391448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992d3703dd646c5e39281b4d55a73752826f729e4198d43c57403bc97eb82f0d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 01:42:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:02:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8e493ed078c2b75bcf190124b24d66f817692d9bedad987963efb47f7e3eef1b`  
		Last Modified: Wed, 22 Apr 2026 00:16:48 GMT  
		Size: 50.0 MB (49982635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c764a369daed85f9b52e15146ccfcd0c76380aeab0914a25d45d32d7e95e4f6b`  
		Last Modified: Wed, 22 Apr 2026 01:42:57 GMT  
		Size: 28.3 MB (28284785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7091ca31d67d63360b5bd63eedb35bca55f65b3881e95a9b699db1be7692a36f`  
		Last Modified: Wed, 22 Apr 2026 05:03:09 GMT  
		Size: 79.1 MB (79124028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:984f881a890f1f2adddc0a64046c72abbf8a8a464c081ccb3e8ccbf08fc37659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8275186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0e140924d6859475832c328c152756ed2377945006f418ace5c378b9059605c`

```dockerfile
```

-	Layers:
	-	`sha256:4e6126001c73d95dc1574f0be1126b90a935028b2628436cbe74960e06f2f78c`  
		Last Modified: Wed, 22 Apr 2026 05:03:08 GMT  
		Size: 8.3 MB (8267942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:519e3e3e095d99b1b6a3ca312ab057ec0c486adde1a09dabeb6cd368e4c78633`  
		Last Modified: Wed, 22 Apr 2026 05:03:07 GMT  
		Size: 7.2 KB (7244 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:11ca7ee293907cc7d51efd74015a4f3b2e006bbae0cd1cf0984db5614ba0d767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166840195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e29ad521146303e1069e39d6b03aed87f861975e354406ee2fccfc1732e3c0a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 03:39:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 09:37:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4acf335ca95a581f78a61de78111418bda596ddf71257299393203995ee7ea4f`  
		Last Modified: Wed, 22 Apr 2026 00:15:35 GMT  
		Size: 54.0 MB (53983935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d29dcef074d70bcd1e851f17e286abd94e829b11cf89631a079de7a5d724304`  
		Last Modified: Wed, 22 Apr 2026 03:39:43 GMT  
		Size: 29.4 MB (29406037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd57b32a5dc3e8581a7c19ba8dc6ae535a2865291f197fe5f63b9c08c56a590`  
		Last Modified: Wed, 22 Apr 2026 09:38:28 GMT  
		Size: 83.5 MB (83450223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a5c2f2e5735510c42e89f222a376504c2fdacdd9ea50a807f462b9766066f1ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8266119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d6431f9c033ebe37c070719678e93a1d98c7fa1a9377cf0431721f16a9715f`

```dockerfile
```

-	Layers:
	-	`sha256:6443c7d2e526755c395464a246c5db855543a2707c062862ebca0ccd3f753311`  
		Last Modified: Wed, 22 Apr 2026 09:38:26 GMT  
		Size: 8.3 MB (8258821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1658930f3625afe0271951d7967f6e032af104fe500b587008e2de7dd696091e`  
		Last Modified: Wed, 22 Apr 2026 09:38:25 GMT  
		Size: 7.3 KB (7298 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:a0ff15214d005cf8a270269c3a62333ebb70653b9a1a0ca8701f6ac87112f587
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148650595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a024470884d4b8199ab93772008e455d4614e4e2640eec259ede6be7c83f1c4f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1776729600'
# Thu, 23 Apr 2026 16:15:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 25 Apr 2026 23:06:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:04fb0dd36a6b62569331264b3dc244d1f567b4ad68c8c1b27f9d22978f421544`  
		Last Modified: Wed, 22 Apr 2026 02:14:57 GMT  
		Size: 46.8 MB (46771523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67bcef726e432bfd28120bec18ce459483cfe5851a88769e35186b7e9186e99`  
		Last Modified: Thu, 23 Apr 2026 16:16:58 GMT  
		Size: 26.6 MB (26575473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c088d66fe4b03f57a1b249457eed3a1d678ec813dfb34d56e5a011edc2f10bf`  
		Last Modified: Sat, 25 Apr 2026 23:10:22 GMT  
		Size: 75.3 MB (75303599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:85cdae5bb11cd42432c3481485847d67aed8eab18e31e8669cbd217be20c0c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8268804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d5b9a0dcf0d500e290b2c88be60081a5a658b73cb1db2309a15fa8a12506e12`

```dockerfile
```

-	Layers:
	-	`sha256:2487364d0d1b100d00512533ef51cc6b8729dec979454d82708a8ee4e1da7b6b`  
		Last Modified: Sat, 25 Apr 2026 23:10:13 GMT  
		Size: 8.3 MB (8261506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09b3792c0eb3138f9ad629bd5c4bbc9e0ea8eca06d767924744f6ca3761390ed`  
		Last Modified: Sat, 25 Apr 2026 23:10:11 GMT  
		Size: 7.3 KB (7298 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:5006ba2ee5359ed065f5ae9301b0784f284b2069fa51785270168062c4382a52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152676592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:779352ae7bf5f942756b6d24b1bd60230a577bd4a7b95c1490b74ae4b34cd6b3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1776729600'
# Wed, 22 Apr 2026 02:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 04:20:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a1060191b9434ca828b6395f3c2782a999320b4babb35dd20cb17592437fdf4a`  
		Last Modified: Wed, 22 Apr 2026 00:15:37 GMT  
		Size: 48.4 MB (48407607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca628a02ce8552e3ffa145824b47810287e1d695728e354379828ee1a246028c`  
		Last Modified: Wed, 22 Apr 2026 02:32:22 GMT  
		Size: 26.8 MB (26781237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4284620042de7e700765e6cf3d08ae5e2f2bfa319c3f4a48a20ef1a1a7fa7b15`  
		Last Modified: Wed, 22 Apr 2026 04:21:17 GMT  
		Size: 77.5 MB (77487748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ab9c50c2f3cae9930d915ed409506436b0a37c75b29164328d4c490f0e83f30c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8258177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8e81187e72e11360f0f14c772509cd23462cb981a892164d9a55a7fbea55426`

```dockerfile
```

-	Layers:
	-	`sha256:c1395a60324030cd7083fc91a47d648376eaf001b2ee253e4723656afdfb5cf4`  
		Last Modified: Wed, 22 Apr 2026 04:21:16 GMT  
		Size: 8.3 MB (8250911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43bbe01565e3cea1fb95912beee17a621277e5992440aac749a251d464421196`  
		Last Modified: Wed, 22 Apr 2026 04:21:16 GMT  
		Size: 7.3 KB (7266 bytes)  
		MIME: application/vnd.in-toto+json
