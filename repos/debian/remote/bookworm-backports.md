## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:e5bd224e4960e313308f34b7082244e8f25f52df2067dc3f29fa9146e662981a
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

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:2c0b686251bc0d55cd132f64a70f9bf1a426bbc98a51f80b71ed85ab496448a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48480782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d61758d3201507ee7c60e26e689333bc140dbee0426138abd4694755ab03a9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9479ea2a9f3beb2253a64315b5d0739e779ca0336744e11242cc3f635a8d33`  
		Last Modified: Mon, 29 Sep 2025 23:46:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:84ee47dc5cbef6b5927767800b884861a70fae1190b0a84e34ade6fce6003acc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fd1d9a194b409947623eefdcffe9897115340e8a9de0a3456bcd66d9644d71`

```dockerfile
```

-	Layers:
	-	`sha256:8bc21ff9806b2b20205e9453b4a75f957adb255fecdc8a05804c5bfb3e9554c6`  
		Last Modified: Tue, 30 Sep 2025 00:25:29 GMT  
		Size: 3.7 MB (3733431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6122eb136f47560ed72f63e9247b528949e5b810f384fe6489823d7d84e3f3b4`  
		Last Modified: Tue, 30 Sep 2025 00:25:30 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:39251ef71048e5a19e4a3fba1858c5af444a905dea2ec7ca4628892d381c54be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46015802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb29eb8be5786642eeab4e4371c2e3147d9204d05e5f0e28e365c849f8794de1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d6b0ca95b13ee68ac33e867e046c01d5a40daee1d76922dab47dd1edf2533e94`  
		Last Modified: Tue, 21 Oct 2025 00:19:45 GMT  
		Size: 46.0 MB (46015580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a5ec4b061ae3cd8aabf7816e98f9cb7c21461e0a01aa7ef9e91491fab410a0`  
		Last Modified: Tue, 21 Oct 2025 01:15:38 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:00cf3317fe024b1a94abb25303e6a96b591a632fe29ed9d9eee861c5a3de6468
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f82fb31012a1f39a8de00a22042f6ab5c67e751b02e44dd345a3f8aa85f043`

```dockerfile
```

-	Layers:
	-	`sha256:508d51150f388f61e7d73efac2c7dbbf3e0fd6b6c5ecebf4c139fca9c1fde38d`  
		Last Modified: Tue, 21 Oct 2025 06:23:39 GMT  
		Size: 3.7 MB (3733632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d11b19eabb61e297b29da68aafee503e7d941e5bbc47a33047d6d9956a88435`  
		Last Modified: Tue, 21 Oct 2025 06:23:39 GMT  
		Size: 5.9 KB (5903 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:7424a57794dd3a54fb1a9331437e9f0ec9215c5c904e3afc9ef424de92ea96a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44196147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97acf440bd33e4e781a26f05da66cc802a79d722d4a0d2c1cb61bccc8a4af7c2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:03e514ef7fa283c62434ceaa5569a1dfd7eb8f0bc5744761a741cccd05a62353`  
		Last Modified: Mon, 29 Sep 2025 23:34:15 GMT  
		Size: 44.2 MB (44195923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a6bb4061ac84d349126abbf12137b369635ae6dad6099a5a53c3658a72a364`  
		Last Modified: Mon, 29 Sep 2025 23:51:00 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:135e80b8cf9c6d3e63647368f7628e7d33c738e2fa5b30690035db849e0a547d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3741513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d729863d439b1397a5e6b9203cf788c6edd3805f0f95056ac16f8dc8853547bc`

```dockerfile
```

-	Layers:
	-	`sha256:af21efd5e4aa7b4377ce3b29a49f99048e434405585bad1a86a7caa971da3974`  
		Last Modified: Tue, 30 Sep 2025 00:25:41 GMT  
		Size: 3.7 MB (3735610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92829d5180c228dd0352ad94be32affc94f018cb9fb448da854eaa55b9151349`  
		Last Modified: Tue, 30 Sep 2025 00:25:42 GMT  
		Size: 5.9 KB (5903 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:557f97dd58f56654c6f3b2a98dde3a91241371b8cee6ba987f75bfed48033ebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48359139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a3922cf186c4b588045a576e4c2573c8577f1a06eb2c6f4cc0a4c6f65c9e84`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f7b43f0d0a8b99591b27457b368e70a582002600d32503fd07798c1bee7cd134`  
		Last Modified: Mon, 29 Sep 2025 23:34:16 GMT  
		Size: 48.4 MB (48358915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bed25696d99082f4840fdd52ee66229a0b736b74d695da432fcf3831a536f9c`  
		Last Modified: Mon, 29 Sep 2025 23:47:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b01ed65bfdfee83618b91f98b4e3502f9ad7ad22c8e742005eb0c69327552f0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f1841716acb9e130259e8112ea52e888435834a8aa01932791f9fb0630835d`

```dockerfile
```

-	Layers:
	-	`sha256:97e3a150423411ea7ab2f6420a5fdd91d6fbaa8d514a1cefabb991cf11e10035`  
		Last Modified: Tue, 30 Sep 2025 00:25:46 GMT  
		Size: 3.7 MB (3733646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceed2ec3b8ef306e98b03874d41bc8dbf7993626ec32284e18dcb56a0a8537b3`  
		Last Modified: Tue, 30 Sep 2025 00:25:47 GMT  
		Size: 5.9 KB (5915 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:cd259c53973df2022ea169a7484065b1794d837cc73d515abd34a308a8503191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49466876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b01a632740a94b5f2cbfa43d13c5c3c0381414dbd3c2b1c9e4a23f700bbb8478`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2212ccc79525753c3f36994bd936e194dcec09d69b21786be4caa60f697693d8`  
		Last Modified: Mon, 29 Sep 2025 23:34:26 GMT  
		Size: 49.5 MB (49466651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7be66e09565f0db19610cccba508c38e25df7ef550e41499173929544feb1e62`  
		Last Modified: Mon, 29 Sep 2025 23:46:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:82750694de90e0467f750d67c924743ef5e8406cb3224bd0efd53b1a5602fcca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42af920df2ec3020d360a7769d5e88817b8373c3c4f6fefeec52408170c91208`

```dockerfile
```

-	Layers:
	-	`sha256:6452855ba0db8d8815ea54142686f8472a5b4d2abce611dfb8dad15dda2c837a`  
		Last Modified: Tue, 30 Sep 2025 00:25:51 GMT  
		Size: 3.7 MB (3730628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed2d4948a773f5221a3e817ca0bcbf7d0bf1b57d18fdb8b14ed167f2d9186310`  
		Last Modified: Tue, 30 Sep 2025 00:25:52 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:7b44a5b1248a85adce704282385fbd65b3fcbd53adb0e465f830b48356b80ce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48760967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42a49df2d32d9c89e99a2367876df53230b2d289104024b9bb4b79311724054`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4ff7a7a0be4afa0c088333063434d872e5a67b49bc2165e0d5f1c8b45e31c387`  
		Last Modified: Tue, 21 Oct 2025 00:19:28 GMT  
		Size: 48.8 MB (48760743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b21ec7cde651bba78c2172870d970898cec8bbf18d8eb75ead7505f7b1912a3`  
		Last Modified: Tue, 21 Oct 2025 01:15:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a9f1abc166535d4c26b79e27ed18b8ab58fa387b501834045a2aa594a6f999b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfd0f0ca4be26a322e6ec1959eb06e46c39812141b7e658a17f932f506e28f90`

```dockerfile
```

-	Layers:
	-	`sha256:9fd43369573c2a0ca965bdbf14d41f1a4468fa47753c90a71ad36adc20620ed9`  
		Last Modified: Tue, 21 Oct 2025 03:25:39 GMT  
		Size: 5.7 KB (5671 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:cd6aef2d16c3b56697f5b4d235cb7bf5ae6fa9c053c05e3f61757b22d0636526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52327009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342a3e0630fd67b633240486edbfe2355dfe2fee346280a1d3ccfe03d1d5fca5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:297b234228c60cb6a9bc0156bdf582119f3c4f22112d7d2e8128e4d1403158cb`  
		Last Modified: Tue, 21 Oct 2025 00:19:36 GMT  
		Size: 52.3 MB (52326787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe40523b540dbe90a8ec0a939b28ab21b1c6fb7529b952e925c7754c4e6ce69`  
		Last Modified: Tue, 21 Oct 2025 01:16:16 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:38d5069ff1700f3f9dea30da05e2324ca27f61ca35617811643f98db5e6e00d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3743659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:602a3ea92b47006099aed58ed9e5792cda00150808e6efdabd5425561abd596f`

```dockerfile
```

-	Layers:
	-	`sha256:c010df8b98aa8aa83a78dd8f9d50b8d73efcddb2bdf7eb21232174f81775ee86`  
		Last Modified: Tue, 21 Oct 2025 03:25:42 GMT  
		Size: 3.7 MB (3737787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcd64eab9442d5d085202b731b1bf781f90cbc25b914a45027ee24b7f218816f`  
		Last Modified: Tue, 21 Oct 2025 03:25:43 GMT  
		Size: 5.9 KB (5872 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:64bb220e6e94164c2de011cc89a9d2c1b3ea63713bce456b09f886319f44e6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47137744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d7a3da41c25ab548e9a1e8919e7323e7a6c1f41caa13e3902c63655daf60ab`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:769a86a44e9ad2fad1b0132047fcc9c080f859777f09d3856b818bc85f1c5895`  
		Last Modified: Tue, 21 Oct 2025 01:19:50 GMT  
		Size: 47.1 MB (47137521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494a85c391839355765ebb6cb991b6e9fe3997dc0ebc5601102e36ca496cf31f`  
		Last Modified: Tue, 21 Oct 2025 01:17:29 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:729b1794d8f4946bdcbfdc86622a4f82ceb72d0e070100deb27507a58c0a6f80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daa40f807d640c122847b1c4dfe082c2ed6b46e8e7e3b85c6edf4713a1f54b34`

```dockerfile
```

-	Layers:
	-	`sha256:015d11b72c60cf93d20bd28f5456deb8237c56d06cac2eb9b138cc4e7afcdd6b`  
		Last Modified: Tue, 21 Oct 2025 06:23:58 GMT  
		Size: 3.7 MB (3730269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f857dd84655426f03d656ce5d0a0cd645e6abdb1f990aed81b985eee7703e63c`  
		Last Modified: Tue, 21 Oct 2025 06:23:59 GMT  
		Size: 5.8 KB (5846 bytes)  
		MIME: application/vnd.in-toto+json
