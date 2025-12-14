## `buildpack-deps:forky-scm`

```console
$ docker pull buildpack-deps@sha256:08eb3a076cb7b76bb7af14c0cd54056476bf1407ed4dfc0a44ed3dee49668b4e
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
$ docker pull buildpack-deps@sha256:89ee12ef3d638e436c7b07056f853ea2a4927fa5a5fec0aa21c234554cb725d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144113067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f999d524f9bb0082ce8f9910de354f804c32f9bd6158557ce5c4cd406000e283`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1765152000'
# Mon, 08 Dec 2025 23:07:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:06:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c7cbbee3050ecd826301596e459f3fa12ca32f5ba2b65d33b56172341d2cd3ff`  
		Last Modified: Mon, 08 Dec 2025 22:17:14 GMT  
		Size: 48.5 MB (48512511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd84557bf7a7d4887bb1011af57bc292a828ae0385421a537869e26f5aaf10da`  
		Last Modified: Mon, 08 Dec 2025 23:07:35 GMT  
		Size: 27.2 MB (27173913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3215057bcdb48e2c916ff65379297925ae8e829013691d71877d63ff1c9875`  
		Last Modified: Tue, 09 Dec 2025 00:06:50 GMT  
		Size: 68.4 MB (68426643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f39d908f6c2cb698666bbb3bacf20a4c766956ea8c53eb18a4956f3842824a8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7767527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fc253dc367c5e508ba6bcc10f68918bd2c4a71161e61809f3bfd1f51fa2b462`

```dockerfile
```

-	Layers:
	-	`sha256:6ffba8a22c38365154e2fdcf6a55c56d4452a0bb32fcc43c220d279d18881056`  
		Last Modified: Tue, 09 Dec 2025 02:22:06 GMT  
		Size: 7.8 MB (7760262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb9f95ba649f794112d7f4430f3514aa504bd0f0bc9931b429eb8cafa0216398`  
		Last Modified: Tue, 09 Dec 2025 02:22:07 GMT  
		Size: 7.3 KB (7265 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:24f8a8d460a5a1d387aa1ee0a33ac4c41f0d6daf52f1ae2078e113ae58c680e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.3 MB (133264538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe930c57d964bc1e80194204ee00e014f023c84b835afcd346c0dd236111a2e8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1765152000'
# Tue, 09 Dec 2025 00:06:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:33:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:97c0e703f22fcbdd1717c90c9c81bde96e65c1c3051ad73d18fbc908c8b17e4d`  
		Last Modified: Mon, 08 Dec 2025 22:15:47 GMT  
		Size: 45.0 MB (45048041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b854bd09bce55cace36b7ecdbfa75886d833623af6ae1398f2375a0e142faf`  
		Last Modified: Tue, 09 Dec 2025 00:06:18 GMT  
		Size: 24.9 MB (24891051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86748a5099afd63ee13abe1176b7acb78164e7a321b3c6f806a0e35be9209643`  
		Last Modified: Tue, 09 Dec 2025 01:33:42 GMT  
		Size: 63.3 MB (63325446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2e2cb4a3a725a9a531c1c812794bb2637387695046c354a68e88827d3da21e67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7768090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c8cc130acacf27c632b12a77d17caab8326a7d84b22662c63f8ee5b221cd595`

```dockerfile
```

-	Layers:
	-	`sha256:289e5ec13992d9372d106d44f55fc622d16d222f6c86de4598c2e1e9b8c15665`  
		Last Modified: Tue, 09 Dec 2025 02:22:14 GMT  
		Size: 7.8 MB (7760761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3555bd3589ae03d86eac8ad204df54e80593a65100ebdce1bbe68263e07b6827`  
		Last Modified: Tue, 09 Dec 2025 02:22:14 GMT  
		Size: 7.3 KB (7329 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:481ab170e99bd06749d3baef4e52a28ecc869bb97e8d3cc6823f740763e78c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143199284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33257a4492190dc0eadddafddef76f4637a65201aec29c47a998ade92a9be0b8`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1765152000'
# Mon, 08 Dec 2025 23:10:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:11:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:60db063fe1f6101cd454be84b0b672c499625ca27e05c40ddaf285db3af29997`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 48.6 MB (48599337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ca0bfa7c46cad923ad76830a45cbb46a0f64043f0882f050c618ba02ce26a2`  
		Last Modified: Mon, 08 Dec 2025 23:11:11 GMT  
		Size: 26.5 MB (26471794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbb44f039710af557b0ba0fa38e5cac191cdc4b476b1d20bccc4bfc817fec4e`  
		Last Modified: Tue, 09 Dec 2025 00:11:48 GMT  
		Size: 68.1 MB (68128153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b2beb2b652a94d508b8d869fed0ad2e5b37e6f23f3d8be05d9cba075489ca77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7774632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90bcef746c45ad93c16a65e117178c14e5941483830099f5fb0b434e61a708b`

```dockerfile
```

-	Layers:
	-	`sha256:98abe5092c5b52fae8693b962688aaa6cd2bc148afe569d721396c96383d54dc`  
		Last Modified: Tue, 09 Dec 2025 05:20:56 GMT  
		Size: 7.8 MB (7767287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5cd1a2e388cf33efd016a823baba59c8ccfa33ce6ab3bea56e699d6ab333c6a`  
		Last Modified: Tue, 09 Dec 2025 05:20:57 GMT  
		Size: 7.3 KB (7345 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:1eebace0999adecef7153260c9f875b64790e5624da85f9a65dce40df90eceda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148665202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbeeb2170013586fe463d32c8c5faf0d16ca9e44d02726c35c6324321d901afa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1765152000'
# Mon, 08 Dec 2025 23:14:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:23:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a5d3e60f8c1eac1ccb5aac1ab5735dd586fe448287d7c7d1d7f59a687bd9b9b1`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 49.9 MB (49874580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345ab10e575001e02de99efc833f717c00ab06eb63e6d406d2e8435c5550eb4b`  
		Last Modified: Mon, 08 Dec 2025 23:14:41 GMT  
		Size: 28.4 MB (28410871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb46e4ab022b5cb381fa5686d522dbfe46b1ccf9e09d5c6900981036d69143da`  
		Last Modified: Tue, 09 Dec 2025 00:24:34 GMT  
		Size: 70.4 MB (70379751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d7a8896d62d0ca05afc421afeb7bc633d94e8b72613b59f847ffa07d061e4905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7763638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869b77a2a8b737155cce8b6df66a9fab6b21a0726abcdd0354718854f735e214`

```dockerfile
```

-	Layers:
	-	`sha256:2a66a092df4f3e6cad61324d4530c7491f07374dc782b644dbe96099c6125ce0`  
		Last Modified: Tue, 09 Dec 2025 02:22:27 GMT  
		Size: 7.8 MB (7756397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdf24948edb43d14a271283abb01b1532bc8d7203975f18cdc35c838d7f1e29b`  
		Last Modified: Tue, 09 Dec 2025 02:22:28 GMT  
		Size: 7.2 KB (7241 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:282e63fa0ef5da7ac0336a93437451a0b06216d0bd5cca8ba9d07597813e32d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156197037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c177f70aaacf8396ef402cac82342ac97137157e15f575f77bfd1e755b21603`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1765152000'
# Mon, 08 Dec 2025 23:21:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:09:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ca6b6474de59c13edb40994c0579d1471aee6a7743baa1f84bd96cf0fbd414da`  
		Last Modified: Mon, 08 Dec 2025 22:50:05 GMT  
		Size: 53.4 MB (53413786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16460d60e48e0172db82e752033b5336b64df38a32ba4e288da4b3068cc402ff`  
		Last Modified: Mon, 08 Dec 2025 23:21:53 GMT  
		Size: 28.9 MB (28864526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff96e6fb6ec2cfd3a984712824e772995b886f15a30aa9cd1af807a917dc615`  
		Last Modified: Tue, 09 Dec 2025 02:10:10 GMT  
		Size: 73.9 MB (73918725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:159f320aa73917aba120433176afaa44ead95f3e2dd2a8cd38fd6451a925c54f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7774686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658063f4e7c5956ec12919c0cfb5929aae391913c5d09ca480380446322729f2`

```dockerfile
```

-	Layers:
	-	`sha256:53a3d31a9edb534ddd6b4e95caa61f733f33583707f57a2e2cf2d65b78b14c2a`  
		Last Modified: Tue, 09 Dec 2025 05:21:10 GMT  
		Size: 7.8 MB (7767389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:015886c42a59d014af6dd65751896787e6c30ba26d07ff58223ac5f9ae184646`  
		Last Modified: Tue, 09 Dec 2025 05:21:10 GMT  
		Size: 7.3 KB (7297 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:43c779b5e19e2fc1872e6d44b77a8a7ca207787393a18c308cb67b7272d0bdc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.7 MB (145681327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3d278ef30351ec8f1edde90c5a2216d40ce4abcf9e3e1935ef13a0c65aec81`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1765152000'
# Thu, 11 Dec 2025 08:32:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 14 Dec 2025 08:34:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:002664050c13ca9d4571d9c24b2cd8235785825417d0a59db3d16cec4b277530`  
		Last Modified: Tue, 09 Dec 2025 01:49:57 GMT  
		Size: 46.8 MB (46840355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79762d676bf44b71b19af2f5e9bf3520032115760ca18d18b1e487b509a74b9a`  
		Last Modified: Thu, 11 Dec 2025 08:33:56 GMT  
		Size: 26.4 MB (26411155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:899e9bcb2a2f2dedd16603a638381275feefb5833c5f56fd53977194d927e781`  
		Last Modified: Sun, 14 Dec 2025 08:38:25 GMT  
		Size: 72.4 MB (72429817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fce42cd753f415ab35d6d0e0f69536e57104392da4128af610e1a691fae3e362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7760961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da71ac906f7cbed973832ddc433331b0b4bda21bd2c5569d5b1e3c9a7314df4`

```dockerfile
```

-	Layers:
	-	`sha256:df245a1316d4e860abfa8ca4e79c843583b6791da80af3566ba3c3430fd4ef53`  
		Last Modified: Sun, 14 Dec 2025 11:20:17 GMT  
		Size: 7.8 MB (7753663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb3716eef1a86b8ccefd3cc1d8ef579d9b6ee6b398b3cadc12ab89bacd2f9d83`  
		Last Modified: Sun, 14 Dec 2025 11:20:18 GMT  
		Size: 7.3 KB (7298 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:89dbc2acb777e21324953ed245772363d56e9a8dd6f0d92bc00aa912ffe3649f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.8 MB (145753581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13197cd45c8247e0c6d611eac9ef77ac3375eaf5f0f043de5c73848ba6c2c64b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1765152000'
# Tue, 09 Dec 2025 00:10:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:46:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:88e5ed2f2b5ebe4c22b20536e853aae0963f42dcc4ff80e14e14172e983096b3`  
		Last Modified: Mon, 08 Dec 2025 22:20:13 GMT  
		Size: 48.3 MB (48319837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d47897a01efebe9154a3fe179f72cecb78c93572d95a8b9465a3989d8d1df11`  
		Last Modified: Tue, 09 Dec 2025 00:11:09 GMT  
		Size: 28.3 MB (28292167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2eaf6cdb14f443f0f3f48efe5aed619dde90987e70aea45fa92849adbe0c9f7`  
		Last Modified: Tue, 09 Dec 2025 01:46:48 GMT  
		Size: 69.1 MB (69141577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:09dead26179934813e3ff4cb61dd7bfd766a22014845c934b463465ff18c0473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7768440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d672847cee08dae389de5ffdbbcfc4fc925f6f7b438d7b4b521c49060ca4eae`

```dockerfile
```

-	Layers:
	-	`sha256:e44b55c17e786f82d94db199fa02ece3346d61526d7332a9a3481bfdb59fb26b`  
		Last Modified: Tue, 09 Dec 2025 05:21:22 GMT  
		Size: 7.8 MB (7761175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78e9bb5e1fa0d14e02f5e8abf92897594d45bd656cf456e020debb75908fcc58`  
		Last Modified: Tue, 09 Dec 2025 05:21:23 GMT  
		Size: 7.3 KB (7265 bytes)  
		MIME: application/vnd.in-toto+json
