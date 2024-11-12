## `debian:testing-backports`

```console
$ docker pull debian@sha256:abb874bdd731b12530fcf655179f890c7f6a2778c24656f93dfb21ae65b425ce
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:8edb5dce5ec52ba0c7012a9256fb747d805a37cf824e5be449b3b2a060b7f1f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53227005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83d22a3b31de081e03a5bb665f80b774cda34f4ce8ed92edd725cd0f7fe9facf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c1f3f669a92f4b53dd069b7da2ebc504d2fdec161442dba2fc3ea1f47ff18b14`  
		Last Modified: Tue, 12 Nov 2024 00:55:03 GMT  
		Size: 53.2 MB (53226783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f2ea5591a4be6352458e31058c333ce6e5df58056138e126eca5fa3025b6b5`  
		Last Modified: Tue, 12 Nov 2024 02:01:56 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:90d043435cf23c1dc2b5beb943d434d2013ddc8bb5b84dbf3a314b12d644ebf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3256221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:463f78ea29e8e60c8993f46e7409de662f0ef15507e32aea47eaf6bbc1b22c75`

```dockerfile
```

-	Layers:
	-	`sha256:9b0d0b42d8f71f3155c872c355aa1c519a3a619d0a0e7ff6a25914e943779c1f`  
		Last Modified: Tue, 12 Nov 2024 02:01:56 GMT  
		Size: 3.3 MB (3250384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6563a87cdd7f85803848a92709f491e1bdd114ca2ef1bf6280945937a18d974`  
		Last Modified: Tue, 12 Nov 2024 02:01:56 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:502eb0676ea1b229b320c9e3b3efa24da2daa2b89ccb9550f169c01732ac55f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50091732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b15f25e12a13028c1034888213db4268ce01ba4ca4a0c3baeeb63de33d902774`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:fae024d27da506b9bd0ac9b4d19ffe11c3051833566027ab2ec9fa38ccfc60d6`  
		Last Modified: Tue, 12 Nov 2024 00:57:50 GMT  
		Size: 50.1 MB (50091511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e850f118e5e0ce899e486dff107b2f2edea224556e11800d85d027c268a4428f`  
		Last Modified: Tue, 12 Nov 2024 02:02:02 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:55a3a2f638a7e3f73ebbd8364b87b0c69120e645b30f9846b37b4850d0008cb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3259095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f2939c9059a5178e3e3e57fc99e9c30817dce7fc62401c73fe8f043c309a22`

```dockerfile
```

-	Layers:
	-	`sha256:25d430bcd16cda55feebaf9d7da480cf88541cb129d69ac1f2ea97ca4b6d7696`  
		Last Modified: Tue, 12 Nov 2024 02:02:02 GMT  
		Size: 3.3 MB (3253206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3108487cd419ff8109fc1b225a9a278907ff3c4349aa831a785dcd2a08baab1`  
		Last Modified: Tue, 12 Nov 2024 02:02:02 GMT  
		Size: 5.9 KB (5889 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:3020e78f16ffa8c1d70fe94b13bf91652542dcca48832025909a4589b7bcb0bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47681990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35df4749a4fdeb30ca19a8e333686e16f53cffd3aa2cfdfb0155d2fb9545a282`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8a41c4ab4721e31ecd32aa6d61bcc616175d3b644a415c850776edb689aea28c`  
		Last Modified: Tue, 12 Nov 2024 01:01:44 GMT  
		Size: 47.7 MB (47681768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb430c09158755f1857ccec716abca382d3cbc6fb03df06448179802f2c6a753`  
		Last Modified: Tue, 12 Nov 2024 02:21:31 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e52275f5b2dbe60feba52283cd44106465acccd7bb1667f2a87652b5b6521e50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3257831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29be3d02a8a122ab788bb1c2541d2ed951255cfbebc729c7d97d03e82e195940`

```dockerfile
```

-	Layers:
	-	`sha256:7d04f6ff43878b2bfd264f1c95f76b6e103fe9b3a75909007a72effd5c8690f3`  
		Last Modified: Tue, 12 Nov 2024 02:21:31 GMT  
		Size: 3.3 MB (3251942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e6ed357182f7a92cff0818204326f5cd0f003db6da605bb61efb1db86295718`  
		Last Modified: Tue, 12 Nov 2024 02:21:30 GMT  
		Size: 5.9 KB (5889 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:ca36a30ca3fe6f23ad86f0b01e99d961558bcce605824cb16f12580f75c6d4ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53670178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e2fd0b17c717b3eceaed96e5f920ee2ac72e428491529177e491784bd66f7ee`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:697066b3c41c0e748488c93a09f55bc690bda5c8785f15567dcf01882737727d`  
		Last Modified: Tue, 12 Nov 2024 01:01:55 GMT  
		Size: 53.7 MB (53669956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff61ad201891fa6ad37889a6abe337bf0e91452cecebd8edff3f52f9828a512`  
		Last Modified: Tue, 12 Nov 2024 02:23:24 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d75ba11814ed5525a419a5006198287073152ef04e79b5b8efd860dec80c07aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3261780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68932f771ada261142d5b994b029f491f33c808dd6e36e30246c1dff7d76c45a`

```dockerfile
```

-	Layers:
	-	`sha256:22d6177a58b56a87d83bdf2729514ec6b14f4aaa3059c874379c4990620965b5`  
		Last Modified: Tue, 12 Nov 2024 02:23:25 GMT  
		Size: 3.3 MB (3255875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca76d3be2111ab70ec6f1becd00645d5821eeb6fa29c573248102203f9426396`  
		Last Modified: Tue, 12 Nov 2024 02:23:24 GMT  
		Size: 5.9 KB (5905 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:bd4bbd3d0b6df7a68690dcb92b60abdc561b747c019a71b39c272b79a7eb717e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54095350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b24602843360d357793e8131fd199a0e8451afd645d41c39d1f6c6020bc6140`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ebaceb2adce4e48542d982329688aae2f8ea7fa15690220497554834f91e6c94`  
		Last Modified: Tue, 12 Nov 2024 00:55:14 GMT  
		Size: 54.1 MB (54095128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733db58d0b2d32a3c75cda0dae6f7795f093fce6023a0a024245159cf59f8cfb`  
		Last Modified: Tue, 12 Nov 2024 02:02:04 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:0e75682fdf4ed6173630b46f7a7c6babe69361c34d538851bda662b5ae45fa92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3252680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d78e8702da5e1e408bc4b5392986441bebc4ab97a5dae6c00ae27d32ca29c10`

```dockerfile
```

-	Layers:
	-	`sha256:672aeb06b4eb36f05c382dd0d8f6131d6765016effd4db26f2f5a7d01d0739ab`  
		Last Modified: Tue, 12 Nov 2024 02:02:04 GMT  
		Size: 3.2 MB (3246860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df9b7b4686125e037c017721688342d47a3f86cce140f22fcbc65fd505bd251e`  
		Last Modified: Tue, 12 Nov 2024 02:02:04 GMT  
		Size: 5.8 KB (5820 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:981524aab36f2ecef76246ec7affa672bbd5e0831f5f64d87a551bd7023f7c09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52200648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b101f48648bdd3aa7793dd6dbd64eaa01a25e84860c368c77cb6914c90cfa07f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:78f8f8ad9107cb9f86579cd1a8356509b19cfad57ae98d66bf8059baaa51f13d`  
		Last Modified: Tue, 12 Nov 2024 01:05:18 GMT  
		Size: 52.2 MB (52200427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c473a8a33cb8fa9f6dbf739226acff7441466c1941753bb81c6baab4bb1251`  
		Last Modified: Tue, 12 Nov 2024 02:03:56 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:02a8f96c5e6e474ffe3f5436547727050b32d0938c960db4ddf8c696a2ce32e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e1a1fea991e37343923ab1e20c87de426f7fd109e98d792f5d3a73a6d763d16`

```dockerfile
```

-	Layers:
	-	`sha256:79735f650fad107008c8124fe2429b823f0e3af68afaa97ef7f4f5f36ad4e448`  
		Last Modified: Tue, 12 Nov 2024 02:03:56 GMT  
		Size: 5.7 KB (5661 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:9464643620ec8307bbabc24d7c62934fbc1e22fe46a633b7fbcb09de3c06e570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57193810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b08bee6a8e5564bce7a13ec69d2659a8d7d572ecd7f200cd984e11cfbf649075`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:bfaf6689cfe5b1b679ac91d30f4af58230d4b1ee582374f94222935bb55a9ea3`  
		Last Modified: Tue, 12 Nov 2024 01:03:35 GMT  
		Size: 57.2 MB (57193587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c992c4a7400af5c41ab587012a03d000955b72dc7ee8c2dfd413f4130a6fb2c5`  
		Last Modified: Tue, 12 Nov 2024 02:24:15 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:63a28fe8c3f80a6da579f97e6b4cacd42ee705014ac7caafc49f0b2a0f7e7097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3259950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8f4aa4edaf1bc1c1356a7430a0378bd6e10a88d7816a103d8288f8e75cd97eb`

```dockerfile
```

-	Layers:
	-	`sha256:f6f71b3956b8dd2d13629ed0e6f51566ee2a516b5215b455cd6e0bccc398cb0c`  
		Last Modified: Tue, 12 Nov 2024 02:24:15 GMT  
		Size: 3.3 MB (3254087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27d458462eab7ddd82e3910d99b273538980dfdb6ea7bc46bd458e9f5698db98`  
		Last Modified: Tue, 12 Nov 2024 02:24:15 GMT  
		Size: 5.9 KB (5863 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; riscv64

```console
$ docker pull debian@sha256:74444102214da32684a997ad0b20bd5192623ee551762c83cf1899e5578e4235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51645493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ca56e9f17bb49220e773a43aaa80c5b45924f7bc4c681ca74676b4e79cc797`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0729db62194d7136f2fe2b07c568644d474ded0210a32e0efc8f2fe5ebcc6a17`  
		Last Modified: Tue, 12 Nov 2024 01:03:14 GMT  
		Size: 51.6 MB (51645271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0740a5c868263d6c7c51280c3219ae63322f00280656c0a5ba8913ca2cb2a989`  
		Last Modified: Tue, 12 Nov 2024 03:42:25 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2ab79751175c0b4240d19ca6c769724320fe508c082a363f25937e206505a0fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3248857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e217bca8064c15f26b8dd60a4b0eb7307dab61366cd45cac22dd75396bc8777`

```dockerfile
```

-	Layers:
	-	`sha256:81d26e92108e2ebf7382487629ac6dc106b71cfa0c54f05d84eb02c2d4f06721`  
		Last Modified: Tue, 12 Nov 2024 03:42:25 GMT  
		Size: 3.2 MB (3242994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abf763ed763cc32bf7cf053d8b623ae22cefbbc6c9ef4aba65e57151fd378ea8`  
		Last Modified: Tue, 12 Nov 2024 03:42:25 GMT  
		Size: 5.9 KB (5863 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:a863318886cabdce03d986f4a00a5368a904baff625f4a589e77f497c9ff2e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52885752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ec93830430fd538d52decf25aac85f60bd3c8eaecbd6e8c280ad29f8f680556`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:670975d8b290040812e8ec5deddc536b98b5da6de159f4a0aa63b04735db617e`  
		Last Modified: Tue, 12 Nov 2024 01:04:16 GMT  
		Size: 52.9 MB (52885530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc8c6092d294ef7f12208f70788e0a73bee62b70a83d3a77ac46f1996cd2cc5`  
		Last Modified: Tue, 12 Nov 2024 02:22:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:testing-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d469c1a4a7e8c5c361a6ed0d22a6f3b20ff54442acfc307829730e1e5b06a786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3257817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6d4c7114ead05fcab3e27e2ddf17f02c9487a5af4bb496c8d14f64478cd2e0`

```dockerfile
```

-	Layers:
	-	`sha256:eaac3bb850dbca113318f099fa5d06cea0621eef3ad92c1e8ad3cacddf1a40a5`  
		Last Modified: Tue, 12 Nov 2024 02:22:13 GMT  
		Size: 3.3 MB (3251980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c713081b71fd695e57b61d5fd0658cb12ae46e1b542e222f9f2057a4bddf034`  
		Last Modified: Tue, 12 Nov 2024 02:22:12 GMT  
		Size: 5.8 KB (5837 bytes)  
		MIME: application/vnd.in-toto+json
