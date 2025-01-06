## `debian:trixie-backports`

```console
$ docker pull debian@sha256:4689c8fc5982fb10429c53d41bbe71f3412e25980a1a314f5e138eaaac75df2a
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

### `debian:trixie-backports` - linux; amd64

```console
$ docker pull debian@sha256:ad8d40276fe9264dc305a470550fb453a9fd8262322f5a116a23a66c15c47548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52212573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8285e8eaf1ea2b55f546812b2942ed960c141c9e04ccac199454ef9db92bb6d4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:5dc28167de372c586b840aa2cdcf07e2afc8e85b392a5dbb5552be77587eff75`  
		Size: 52.2 MB (52212351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bce0b04216594428cbae859ef820f745d2ef42d7da5e310686a3bdb64b083da`  
		Last Modified: Tue, 24 Dec 2024 22:13:51 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4ba5dc1a0ac3338fa3b7b8293d90597232ec3cfbee0558eafdbce8eb0aad9b01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3235887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b0df952094e42337604640b76aaaf87bba9d95c11be068b805dbfd0473c9a0e`

```dockerfile
```

-	Layers:
	-	`sha256:0d990596d7c88aad1d24dad5012dadf867c8e1e1f9d5dffa74969c92b540a3b4`  
		Last Modified: Tue, 24 Dec 2024 22:13:51 GMT  
		Size: 3.2 MB (3230061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e03bec8f7bc60f1b5dfbf1f98c5679cad28ce7e8f83db93d5822b426d2cccc7a`  
		Last Modified: Tue, 24 Dec 2024 22:13:51 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:d24e3745595fd1a0820500c59b363b638051beff096bbd44636dc2b7341d5c17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48739140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c4098a44743327675a73643fc9bc11068977ab840b42c522a2d4cfdbff9052`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b5a5271e09aab30795789f051d2425121101b650637f36e772bdb80c62bb4833`  
		Last Modified: Tue, 24 Dec 2024 21:35:34 GMT  
		Size: 48.7 MB (48738917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcabf9d7817e6df550e98e74f182c7facc4257db123d34be20aeff5d60ab93c3`  
		Last Modified: Tue, 24 Dec 2024 22:21:34 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e6ea88d069a5865220ed06df0d58957a18efc78220b8d2778c6d6d1a88bb0c6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3238757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7d2e6f0e71439a61b84c5535a69c5f6847aea4cca136385e2d477ddb13cfe73`

```dockerfile
```

-	Layers:
	-	`sha256:3756cb0d06a178cc238fbc857fa7628484d264182e4fd05cdeecfea431be4a9a`  
		Last Modified: Tue, 24 Dec 2024 22:21:35 GMT  
		Size: 3.2 MB (3232878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:305a6268ab8978dbda74c60dc4e314220036afd9aa315900f805d793bec54285`  
		Last Modified: Tue, 24 Dec 2024 22:21:34 GMT  
		Size: 5.9 KB (5879 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:2363769d1ca3314a795e5590095ef1f5ff61a8cde9f90a4b76d447579e9df024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46768187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fdf18fa4ddf3321c7340a11eb326e413b2cb1cb70ddc357c4121dab9ead9af6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7dbbd0b59e8fd2a826bed9f5cfe195c9cb61ad138accd85ab45d8f8eb5e53a51`  
		Last Modified: Tue, 24 Dec 2024 21:37:24 GMT  
		Size: 46.8 MB (46767965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37780ad88998d6f0bb1ca4d12af4946b1296959465eb516b5ac1c22c2785d73a`  
		Last Modified: Tue, 24 Dec 2024 22:18:13 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:47fc6fd143bc7d5958228e7c0889c4b39e6ac77aaf20d0f476d9855bf0b94ab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3237500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:098883ec706a3c0ae6758bdcd53d52e39d5f1ced596e3841d92d3d63944e4102`

```dockerfile
```

-	Layers:
	-	`sha256:445627877d516f48752e6cef80bc2788043e33057a70b532ff49eaeb95ecbecd`  
		Last Modified: Tue, 24 Dec 2024 22:18:14 GMT  
		Size: 3.2 MB (3231621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1777c9d82ec7531016273287f71afa55bd3b4b645db98ae105c78436277f6122`  
		Last Modified: Tue, 24 Dec 2024 22:18:13 GMT  
		Size: 5.9 KB (5879 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:40964487ba02b90ea3cd77933829995409da16e097850d8e9e11edb33456223e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52425793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3ebeb3dc0624d46d74ae342a220a27bbd3a29e5c1ee6d83996d9335eecbbf1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:655b7ff6f79a823125a6f22dacb056ef3cd9ab7e8eb5ffc6594ff4745e276b8b`  
		Last Modified: Tue, 24 Dec 2024 21:37:11 GMT  
		Size: 52.4 MB (52425570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1caf19ac661031cdf7ab802795b44bc2e41b97960920c89a0168d278ce152509`  
		Last Modified: Tue, 24 Dec 2024 22:18:49 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7a2022af1664d47f520e75fb22178d63f1f07e0f4de24ee6c6f670be952eda16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3240164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596fe7d7cc87f98ac0dc8309a046c81db94295b2d0a8262eebecdcd5533f6535`

```dockerfile
```

-	Layers:
	-	`sha256:a4a03b69a8398e6f11a0ee54199502c53fa118d4f8cc73d7edb9726542dc60c2`  
		Last Modified: Tue, 24 Dec 2024 22:18:49 GMT  
		Size: 3.2 MB (3234269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a721ff78bde422beb332f3991bc627d29df2a92bd070ebe5b2ee1e4a2a93384c`  
		Last Modified: Tue, 24 Dec 2024 22:18:49 GMT  
		Size: 5.9 KB (5895 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:d821a082b21aafb3274469c1dbed75251913d764a79e31fcbcf084ce2486cf4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (53029279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a3db79f6a1811eefceab4e3b44aa71f01fde2ac4ad55ebadd045c4220200508`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:099da81c5d3f4771071b424bb19cc8bfc272821672d87e1978f2f206f3040f4f`  
		Last Modified: Tue, 24 Dec 2024 21:32:39 GMT  
		Size: 53.0 MB (53029057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b89dfb8380eff0a28720a82a11d6c688d240eb12f31a614b5797899fea16a5d`  
		Last Modified: Tue, 24 Dec 2024 22:13:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:140b6086c0d5f3046dc9b347b1011d826dad6c0743b597ac5a15d8fa4fce33b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3232359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:922549d711e3bc00bf8f5d6129afaacdd5e65ee4da74e4063b231112e3ac2f5a`

```dockerfile
```

-	Layers:
	-	`sha256:eb479be0d2127449892c01a3fba064b66bb5f7833f8f4fb02bde18855452dc2c`  
		Last Modified: Tue, 24 Dec 2024 22:13:56 GMT  
		Size: 3.2 MB (3226549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68972f038913ae5a60995916493cea770d9f07e642cf5023aeb91e4448b25ece`  
		Last Modified: Tue, 24 Dec 2024 22:13:55 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; mips64le

```console
$ docker pull debian@sha256:fe32aa35aa11e957a8e45a66a43c14ac17db635b14a729868380fa20cd2e396b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51717068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac0242c957287e66e1c069756a278b3cbcfe801d7b09836d746e3ac3c4a19de`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'trixie' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3c43db2a2d96e4b42b073ee755704e1052dfc08d2fed2bad739906e6663926d9`  
		Last Modified: Tue, 24 Dec 2024 21:35:59 GMT  
		Size: 51.7 MB (51716844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2994a98c6c1973c762ac1abe6f5cc16596977793d08f7753dcd7418ccb3aafa7`  
		Last Modified: Tue, 24 Dec 2024 22:19:35 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2691602c6a9af7228d1543b4d65416c02412c38f178d0985c635a2f4f7c3dc64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e9a49e500fa60f174936590956e32ce92146f0f10339cdd6381cdbe782046e`

```dockerfile
```

-	Layers:
	-	`sha256:33504105bea10c15f40996cc89e8fb3d2c61879378355eef6b3550c12e0a719f`  
		Last Modified: Tue, 24 Dec 2024 22:19:35 GMT  
		Size: 5.7 KB (5651 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:156dc0111b616be92151a217f1a5743e96ba51a8d4bb102f1c2035bc533918ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56044326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6036af5e4a89c11cafc23c4c0089d384010873e70ebc0399d4057ba4601f33b9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7d0c0062851cd41c4b765bee1eaa246592e96d9c4a0268bfea5c5d2a73be0e62`  
		Last Modified: Wed, 25 Dec 2024 00:36:18 GMT  
		Size: 56.0 MB (56044104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27660b71b5caa6923bd2d7d7c0024bc1b8a12216e75557db11c4c9da7fa9dae7`  
		Last Modified: Wed, 25 Dec 2024 03:53:16 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7c4eea94c47c76720bd72c51f9e0d980845235f6fa39ef414d9ecfb174ca9719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3239598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10750e923d93cf29a3ab5f617bd9177e094eb3722f138a1403c74272890fc0e4`

```dockerfile
```

-	Layers:
	-	`sha256:b6808de91ce1a36a2a49d71962d0dca405400c0a526c4054f8a91c5f329ee004`  
		Last Modified: Wed, 25 Dec 2024 03:53:16 GMT  
		Size: 3.2 MB (3233746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7bb9aa4fdfc71ef3cae9d1ab1fbdec45da9294ddd70dcf8eb55bac78bdb2cb3`  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; riscv64

```console
$ docker pull debian@sha256:d209d0d4c916ec8f2eb6ad07937cc16c896196911ba1e5d1ce1cf67426cc6fb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50704794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7496ec80325737eb90519b1efe8ef2d1913ed42ef8ddd0584c4daa0030c815e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4a3888858b6d8f90bca9f8a3e822fec0d117f600035c0bd5f303435214a719f0`  
		Last Modified: Tue, 24 Dec 2024 21:42:18 GMT  
		Size: 50.7 MB (50704572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa1261fd5fffdb78a58400f5bb6c11c94a69e4b151c70324bf4470a60feb46d0`  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9f09417784f439a48dd2333609c1561bcdbdc69bebce19bf55bdcc02f34fd811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3229295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6fcecb56143d6aa222856e1ef2aa114b764b3cd0d59337d1e3e9b5746aa61e2`

```dockerfile
```

-	Layers:
	-	`sha256:99a24423eeb1eec58c107b5e1684d23ffde1b5d2a599e960e77984dc34819697`  
		Last Modified: Tue, 24 Dec 2024 22:19:25 GMT  
		Size: 3.2 MB (3223443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd6e7ee69539005fb9fc527b688ce6dc3df20cdf656578f79e7bca12367ee524`  
		Last Modified: Tue, 24 Dec 2024 22:19:24 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:fe00c32797b1daccd84738118852b782c95013587f375dd97c78014935b3c80a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52167760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c258fb146a750aef89ba851be4ac256bb851c03dafa6cc27be2c7af06a568e7f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e1fe280a5056c1901421b5598ff050c78aa067b752ad527583fba85c589bb647`  
		Last Modified: Tue, 24 Dec 2024 21:37:42 GMT  
		Size: 52.2 MB (52167537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975760492283d7b18109e1c28346e93cab2b58804c63452fa4cc44a526cf1656`  
		Last Modified: Tue, 24 Dec 2024 22:16:51 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:69d3d58096ae588c632313d1e9894b22eb91b806c5ed858b20372feea2f13465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3237481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c3ff4513c0cb8c21598c7bf414a6b9e6aa811a9632e74faf89aab203531509`

```dockerfile
```

-	Layers:
	-	`sha256:3e03f8938d06c6192c5d8ad6e1fe3d1e57f151fda8e7d550d04d10840d367c35`  
		Size: 3.2 MB (3231654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e35d7747a0e57d87c3a05fc5e00b0e502493c093fe76e3701f25e04353c8e16`  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json
