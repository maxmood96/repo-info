## `debian:trixie-backports`

```console
$ docker pull debian@sha256:468cf471257e1731a47bf71fba4ee3e219b69cb42f9c75909a17d49128e4541a
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:trixie-backports` - linux; amd64

```console
$ docker pull debian@sha256:5958b43a46d72b772c660e874519ed71d252fddf636acd35c01504549610cf96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49247132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f748ac839983f7fe6d36af36f2b994d33bfee1d97d338e1e1a3c5863bd7e5b1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b8364400c35b20e530ea76455b7a73bf615b17d9d6734e0c2539034d9fe0bed1`  
		Last Modified: Wed, 21 May 2025 22:28:00 GMT  
		Size: 49.2 MB (49246908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83dc13c6b2bd4e39ba2a21b365b90c4c874a991cc978bcc11f7b58e8274f03d1`  
		Last Modified: Wed, 21 May 2025 23:11:58 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a14e69c90b22ee3622534d26ec42d48958637a01ac0cd3f4371fee98ff1c28f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3090088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16e918bfcb0e962264e763d92d822c3acc79fe01ed087911b6e4670b6082df5`

```dockerfile
```

-	Layers:
	-	`sha256:82f8fb4bc99d3fcd4d018c1d5155c30dc39c71899a250e8fa513691ef6338f28`  
		Last Modified: Wed, 21 May 2025 23:11:58 GMT  
		Size: 3.1 MB (3084261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c598ddd00cb26b7ad13c91b9e0a4abd52012f8c1034e7bce5385c38793177b76`  
		Last Modified: Wed, 21 May 2025 23:11:58 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:3adfa0b08d293b2ffe6bd7295cfd801b4f54ccb47406173c16540f2b496c0393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47438366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4789f12b2855898ad23055635587481d26e220fffe07cf8cfe2bb4fb503aa19`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:9616f5c2624aa57711d4d3a917ef21ea33c33b9e29ed21732abc6456aa133801`  
		Last Modified: Wed, 21 May 2025 22:30:36 GMT  
		Size: 47.4 MB (47438143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad88042ca2c00da8105dbc07a0a32e798d9294a3de827637271b89abaaca563c`  
		Last Modified: Wed, 21 May 2025 23:12:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2344247af5ec1ec46b6d7c641e3cf4c5cb6dc58d83b2fa604714fd64368a5b7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3099449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89620472eb69e8301aae51757c8e2b37787def9d82b28b3a02c504fb2378f1d0`

```dockerfile
```

-	Layers:
	-	`sha256:0fe77ceb0d8e2032aacc68d294f9e4b1fef2cb1f0f014cf0b3f347763d286a2f`  
		Last Modified: Wed, 21 May 2025 23:12:45 GMT  
		Size: 3.1 MB (3093570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca3d1dfa45957f12a3a6f16d3e33c7311d19f8951c3609195cc84b85b5183429`  
		Last Modified: Wed, 21 May 2025 23:12:45 GMT  
		Size: 5.9 KB (5879 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:f5589f4a65b91a2a5d3465cc8598ac70969082e82bdc2582068f337dcb5204cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45691041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3714cc9a4b8c71a3606a165dcc22b0e13faaa7797cbb1c168efacf2ec3387175`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d82ad715078dca1bd38ac71d3c9c872661d1bdfae377c84300033db7bf3581fc`  
		Last Modified: Wed, 21 May 2025 22:32:07 GMT  
		Size: 45.7 MB (45690818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1be2ca20bbb1decfba39cac82895ce98ab539c04724ba61ba8b13b98df6d18`  
		Last Modified: Wed, 21 May 2025 23:13:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:adb610405f3a9b5e259a2f9f5308e1336d66cc139f8ca53a27020f28afae33e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3091514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89cd255bd0c0c4ba42976a944cba841a1a3b83a6860380141f700b35c8da8cbc`

```dockerfile
```

-	Layers:
	-	`sha256:f4a64528f42fdee75dd0aa903768a74fa4eb9b8e9e535962b1150a574acc1c2d`  
		Last Modified: Wed, 21 May 2025 23:13:45 GMT  
		Size: 3.1 MB (3085635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d38dad595b8131fabcad31eaebb3b28562b0ec570e55f665d55bc1ceb0f2ae03`  
		Last Modified: Wed, 21 May 2025 23:13:45 GMT  
		Size: 5.9 KB (5879 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:0ef55dfda9ccf77357dc862a6f7605b5ff008713ae6daa1c655fc0610e6e8e8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49618518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b580b932bf619d1716c424b38c1331d058d32bb5de8855c31c377146e82e4fb7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:397826b9fe635f12caff1a603eb12c37426a5b3dc563e0adff2debff0c68a6b0`  
		Last Modified: Wed, 21 May 2025 22:31:07 GMT  
		Size: 49.6 MB (49618294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b510e21ce6d17ff08b8c1856059beaaa5bc30498fb9dd4cb7fa1b431df625f`  
		Last Modified: Wed, 21 May 2025 23:13:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:eca2a2fe9615342f0923dbea47ba1646018de0c4ad6460676f66570f0acd90e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3091637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:768195f762d3fce6a2e6a37e12391aee788b57c21f668269280c2bddd06184c0`

```dockerfile
```

-	Layers:
	-	`sha256:ce3844466a1d98856d0bcfadde11fe2bd73aa854974505b65c1415be2e13bcbe`  
		Last Modified: Wed, 21 May 2025 23:13:10 GMT  
		Size: 3.1 MB (3085742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5edb4c35f1e8f732e17ff2bdbac5264feaa5f532c888009f991497fc405c38e6`  
		Last Modified: Wed, 21 May 2025 23:13:09 GMT  
		Size: 5.9 KB (5895 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:174dd864bf75cf14a04794f4b37010156478dd9598bec438a78d309a2f865811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50761502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdb932038d7980b40652d28eb052873872aab7b0e192b8b86fde8a91c433301`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7e1acd19dab9f7ab62b7570b85e71035e78cd9d9b9bff975df4b0a635578c7be`  
		Last Modified: Wed, 21 May 2025 22:28:11 GMT  
		Size: 50.8 MB (50761280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8badb7f6e2ea9828c3799ae13128ef9dd88c6ba4bcecdde909d9a4ed9abd45d2`  
		Last Modified: Wed, 21 May 2025 23:12:04 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1632640abdaf5a98e96924b5026b0fe3394a76e7403c0c4f891ebfd2f7bfa685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3087275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7c5c060148b086913b1faa095ce44629f2f261f9b86facb9a1873a06ca21328`

```dockerfile
```

-	Layers:
	-	`sha256:d0f5716139151cb1a828413b7a7d01e5980740193524bd455505c6df970646f2`  
		Last Modified: Wed, 21 May 2025 23:12:04 GMT  
		Size: 3.1 MB (3081465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:421f817da47914911f4502016bed598a92d70fe2f6a894d42ce3ac148c29069f`  
		Last Modified: Wed, 21 May 2025 23:12:04 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:5cb98c52333e2dae42ec91c182d7e1d479ca89dde8c00d96a5dedb9b2bca16fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53080766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c8e6f111968b3c0e6f46de05c26d7cb7e6bc4611dc5ee3d51dd4f805b3746bd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:25dfffa4126a91eb76c700c90bfdc9a9e15f34c7438a81f16c8a6999bbde6e45`  
		Last Modified: Wed, 21 May 2025 22:32:01 GMT  
		Size: 53.1 MB (53080544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b070368bffaeb415fb4af8f745ab4ecda7a4f0c0886a2de1a35e44d9823210d`  
		Last Modified: Wed, 21 May 2025 23:13:07 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8110a46381d0861036d204e5b4713550d261ba6b01ea131bc082383a20dbf201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3099995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94a26f98c0118f4eaf7da2136ace51da487eb28b8b8559e27d50be58aeafee8`

```dockerfile
```

-	Layers:
	-	`sha256:0e0d5e88b7cc051d1d90e6fdce770820bb37faa74324901cf816d0b182392293`  
		Last Modified: Wed, 21 May 2025 23:13:07 GMT  
		Size: 3.1 MB (3094142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:110f3060173293604f1c395b7f1b8a01092456b5c05f9317a5bef2256934479a`  
		Last Modified: Wed, 21 May 2025 23:13:07 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; riscv64

```console
$ docker pull debian@sha256:5dda9493c2f71b14f32f6cb6cbe0bb618ba0a27121a299cd462ffbe8ccbe21e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47731635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2f5684d0345dde5fbc53d521e4c8b6cd8ff7f97deb04ee68ee07c24ded0255`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c83c5fa20952cc8610d790073e97537e7832127593042fa9c620fa910fe6f6b9`  
		Last Modified: Wed, 21 May 2025 22:36:51 GMT  
		Size: 47.7 MB (47731411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c76a89250b44472ce3437ce62c0bc2a7ec7bd04f171a4deb5d688484c18d64d`  
		Last Modified: Wed, 21 May 2025 23:15:57 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f3c4f6d692f9b366c7727a8325c47a86971dd14d934520fe2efb21add8452751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3082435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ac767ac5d814a6ae5fdb5eddcf2ae42e6c751a32db70c8be5562f49128d760`

```dockerfile
```

-	Layers:
	-	`sha256:95e7edd06c1d58ae9ef8b8bb3582faa001192cfbf7536a5addc7ba2da70b276f`  
		Last Modified: Wed, 21 May 2025 23:15:57 GMT  
		Size: 3.1 MB (3076582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e34fc796f10eecdc2795032d86d4d92508755b674574453db8b065694d1573d`  
		Last Modified: Wed, 21 May 2025 23:15:57 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:bc9e76283766e8af6c6f57cdc47b7b5acc49f52208b275dec961acea866e375f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49322447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41812d6de2dda14c13fb4f2d76ca61c5ebcfb5f09804d73ff44030356f7d1cd3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:71c8524b25c34592c256fbae9045d0ade48f5e9889d37c5b2190092fa9017d48`  
		Last Modified: Wed, 21 May 2025 22:31:46 GMT  
		Size: 49.3 MB (49322227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0cdc1f19ac4a1a0f65616bf7056f9fae06415055a397f45692b7ecc6cdeef23`  
		Last Modified: Wed, 21 May 2025 23:13:11 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c41b5eadadaa2953970bdef06207a3a5cb2b938d764cfeb1161fa16d3e901b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3097907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a58be5d40367c03a778a36042e2f19b03079a0939820dc0a99a2c97703faf068`

```dockerfile
```

-	Layers:
	-	`sha256:0fa238bbf86fe77aee1f3f0eb1ba60408d07e5e98c084c85c24d32fb69412de2`  
		Last Modified: Wed, 21 May 2025 23:13:11 GMT  
		Size: 3.1 MB (3092080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82d8a9afb5f8c4aaadd58ae7c44f9fd3f393e30a6b52cc77e4e242eedbb96ffd`  
		Last Modified: Wed, 21 May 2025 23:13:11 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json
