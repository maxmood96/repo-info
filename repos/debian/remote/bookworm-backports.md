## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:584a5e458d3600c4672a41dfcba30adaed2d7c2d89f34a56d5ff82bebd84c401
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
$ docker pull debian@sha256:0b8dcec40b354747c12d72ccdede67916d62eff2a1299088b78697d6c5969419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46015806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ceb79d1c6d32115c53fe5e36bfe466806ce6d8dae103d604e7046d7d40ae8e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8f9dd65d850ae18d5d5161e690c6c0b615e72aceac0e3bbc51ed315faf762f0a`  
		Last Modified: Mon, 29 Sep 2025 23:34:08 GMT  
		Size: 46.0 MB (46015582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533e95c4e8579c2307f2c90a208d5b0e2d5fe11ddded0e4b073f6bbdd0f013f3`  
		Last Modified: Mon, 29 Sep 2025 23:50:19 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2eeb8e0162f5b80c0c62d8f6b6ba19c8a9c7b1d4ee0ddf16a3e489e459e93337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888c66a6daf10572bb4240c9f1a7ad9afa5be13bc005e8c97d5f1cdc2ad1478b`

```dockerfile
```

-	Layers:
	-	`sha256:a783a882020a303cb68f3b7c65fb4c4aab759cb2190975f21a896b3949719e60`  
		Last Modified: Tue, 30 Sep 2025 00:25:36 GMT  
		Size: 3.7 MB (3733632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:beda7d94e5c421011317767c4955acba92f82b6c582d6394a475cf7efb539787`  
		Last Modified: Tue, 30 Sep 2025 00:25:37 GMT  
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
$ docker pull debian@sha256:fef3d11a2250f2f2a4ad37abe0f71b01623292e01dd3d66b8f36821c9afaf3a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48760956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b707c7b2a9bd68ed97ec976918cf8e67345f0a730f7c0e3aea2181e63347b13`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7eacf7da1d9ca68e46013f3f56395614b995d68904a39e73d4a5bad90579014f`  
		Last Modified: Mon, 29 Sep 2025 23:33:18 GMT  
		Size: 48.8 MB (48760734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c3b57c107b50062b69b0d8a6b576e4cd103af1103f68e4fa9bb78d0af32076`  
		Last Modified: Mon, 29 Sep 2025 23:46:19 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9eb9b8f326f4b66212266861d5c2c9917fcf547baf378272b70194758f520d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e667e6fbf0f2dd20decb4399977e3ba0eec65ae3de248a7f70b02d1490a9466`

```dockerfile
```

-	Layers:
	-	`sha256:b7605d7d778604836040cbb2af577a36545ce6edb7493c4a318b7853df3517b1`  
		Last Modified: Tue, 30 Sep 2025 00:25:56 GMT  
		Size: 5.7 KB (5671 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:8955d1ff687501c740f69d3ebb91319890a0e7ced4e806385d4e45659d6df068
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52326988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec437b7fd76178d1a49c1d10db76200a089c945341142ac34bd10bb58c802ad`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:812b25f785969d275d8c3962568c03f83ccc4df31b95f01c0646d79d6d5069f3`  
		Last Modified: Mon, 29 Sep 2025 23:33:30 GMT  
		Size: 52.3 MB (52326764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ff4b7b29479969ede792b51254c033bbe4c3cde01950f21b5a300cff4ec4d4`  
		Last Modified: Mon, 29 Sep 2025 23:46:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2bc4f175bae142fbf819839b52d88cabb74b0d0210c01f08d388b7450ca24d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3743660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59891bf2c967262ffbba68bd10f8b90e8d382cb1fc2a7c7ce58c532abdd2cae0`

```dockerfile
```

-	Layers:
	-	`sha256:517bdceacdd671f7c6122d7642881a13e2f20a44edff8622b2816431c0c4f068`  
		Last Modified: Tue, 30 Sep 2025 00:26:00 GMT  
		Size: 3.7 MB (3737787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd13ed8fb95421b782d7bcad9329a8df5ff602f61b1cdeecf97e886a542569e7`  
		Last Modified: Tue, 30 Sep 2025 00:26:01 GMT  
		Size: 5.9 KB (5873 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:c6320a5cfd0482177f8583ab037fcc754fbe3996a608a6b5a0132dfbcd188724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47137668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d78ab18cb53ab67a52d98327a741081e0cac772d42e5580edc76334f7ccfa04`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:87d1bec83b35277b636c6e05b9418301b2f025752d7539cecae442f0b94d8fbe`  
		Last Modified: Mon, 29 Sep 2025 23:33:26 GMT  
		Size: 47.1 MB (47137446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2c1ae4991645ac5f73461ef7a431cdd80fef42f26a48dc2d11047ef52452556`  
		Last Modified: Mon, 29 Sep 2025 23:45:06 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:043bbba4b73fb59f3404f0060bf3cd29d7e5ecc4b45818a4cd0d99e4f6e5ffd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df09cb1f114bff8767133dbf88de10cd5ce415ab5d9e5c92ffe043a4c3f097cb`

```dockerfile
```

-	Layers:
	-	`sha256:ba10b30f8eedf2a1602ce8bffebbe9e1ab18809b8ccf7ec8c083e4fe8b3c5ede`  
		Last Modified: Tue, 30 Sep 2025 00:26:05 GMT  
		Size: 3.7 MB (3730269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:624c21ff82f59da7e01e9aaba9695b40651b56354f0f53f2f7b8eeabcbf4ed5f`  
		Last Modified: Tue, 30 Sep 2025 00:26:06 GMT  
		Size: 5.8 KB (5846 bytes)  
		MIME: application/vnd.in-toto+json
