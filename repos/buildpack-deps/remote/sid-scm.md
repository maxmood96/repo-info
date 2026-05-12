## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:064bd4a1cfea3ec4cdb7878b94a1f3ac0e2444a5032f1b3dc3001e43c7210c18
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

### `buildpack-deps:sid-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:b03672cdfe671386566cfef46bf117b1223ff308732366866db363fc6c314de4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152494567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38af298ee78b3a5ddd02cfce6716225a4e5c5a9338e0d92832ff8899e70a9c1d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:40:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:26:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:099d3355eff9ccff1f5ee3b288e1ead2e7035e89d68d0fc80f60a9bd7a9815e3`  
		Last Modified: Fri, 08 May 2026 18:23:36 GMT  
		Size: 48.7 MB (48702238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fa57e83b29efeaf3d37af3434d6c21acf443c2346367f49caf4c6efea18b60`  
		Last Modified: Fri, 08 May 2026 19:40:55 GMT  
		Size: 26.9 MB (26893395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ea472587b5d0ea5e4527a273544c8354a60d406eef30abe1f16c1a2e24fce9`  
		Last Modified: Fri, 08 May 2026 20:27:15 GMT  
		Size: 76.9 MB (76898934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2ea8f6f6a018c3cda7f5a71ca1163ecf69d064472d170aa243d90ded9a5aba77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8277559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3216de38a6229b62a7d303feb1994f3639de22d726952401a87998e2688e891f`

```dockerfile
```

-	Layers:
	-	`sha256:b51ce408db6e3d3a3bbb603aae9ce5a388784c1f5ac9c6934779c6ee7cbe7814`  
		Last Modified: Fri, 08 May 2026 20:27:13 GMT  
		Size: 8.3 MB (8270305 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:145c83dfe081971a14466beaf939d7bea72803a1ba0707035fd6b74e839d6afa`  
		Last Modified: Fri, 08 May 2026 20:27:12 GMT  
		Size: 7.3 KB (7254 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ae2c147036eaa2e06ba57acb7b8ae112ba7940f1c293301dda8acc9b6c2bb7b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141691278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:952ed40f2b224fa97aeab56fa37485f5b831bfd715a99aec4c3f1035fb5741c7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:44:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 21:35:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:79db944cb324910e68326e7a22d4bc47bd01eb269d35b1d153975be52958d92f`  
		Last Modified: Fri, 08 May 2026 18:37:35 GMT  
		Size: 45.6 MB (45609975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ca5da1f5f4fb120cd7b2b40034ee2f9bf3ebf8737773b984403a970bf3e2fd`  
		Last Modified: Fri, 08 May 2026 19:45:01 GMT  
		Size: 24.6 MB (24605248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd8b20f1b602807fdd595831094bc74ca40f7858af75fa5510dd6910595d566`  
		Last Modified: Fri, 08 May 2026 21:35:25 GMT  
		Size: 71.5 MB (71476055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:70b755347908980a5dbb7fb6dc58d18ac9562254b2cccb20b1d1fac08f99bb98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8277528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b50da3e512c814fab50fa3fd4d4fe6e1dbc8b465ae1e6497d2e3a8529eacc266`

```dockerfile
```

-	Layers:
	-	`sha256:322f39e8a7a1ab42f7216abc1a71c92b56628ebd9ac4455657f5c79ce3b6fe82`  
		Last Modified: Fri, 08 May 2026 21:35:23 GMT  
		Size: 8.3 MB (8270210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d575f9fcb1a6b71a779076aede3f80175c86bd328e6be4ab289b4bc8dbda1d2e`  
		Last Modified: Fri, 08 May 2026 21:35:22 GMT  
		Size: 7.3 KB (7318 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:cf9310fac0d6cf828801d7709b365519cc874f672030065f8e08ac0cc637e019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (150970440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95728c514d48f4d4255893be972bc7f12bfc1270f2b912639ec4cedcfa2c7c68`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:42:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 20:32:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:99699fbc842c790e8471e4039d9c409499f27c659ef9c4d3336a0743660ec819`  
		Last Modified: Fri, 08 May 2026 18:26:06 GMT  
		Size: 48.7 MB (48734151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a8fe1ac3f05529fe3bd8a59a20b641133e27374191e01da78aeed091f2bc7b`  
		Last Modified: Fri, 08 May 2026 19:42:43 GMT  
		Size: 26.2 MB (26171326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44d2c5450e62d768f4b870f1d64fbe0f35f64842962a55a3e8078b24f599148`  
		Last Modified: Fri, 08 May 2026 20:32:44 GMT  
		Size: 76.1 MB (76064963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:85a1ffbd07f144807b33d2314bf584dc6661ba7e1f84fe9be40af67d0d0a4d16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8289141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:677016a96cb361bac7c8fbad173345a591ac9d6d26de61e59d8a7ec758770c03`

```dockerfile
```

-	Layers:
	-	`sha256:9499a8195b2c924d8099e6ed579bd7ac27d48d3faeff39f1279ec70658a22af2`  
		Last Modified: Fri, 08 May 2026 20:32:43 GMT  
		Size: 8.3 MB (8281807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89503697ef233577ea3232d994a8ffb006f01a07ebfb1d8d062d8f6377cf2dee`  
		Last Modified: Fri, 08 May 2026 20:32:42 GMT  
		Size: 7.3 KB (7334 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b373b23ac962728a92b87067bb9f24717256193decdfabd12be430715712df45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.3 MB (157342149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe55168b31d432d5dc48a28bf0de4395f698951c99329dda6419e8d52f30e21b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 19:44:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 23:05:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:673cf326009083501c3fabdd17567c937b894deb57d94461178ef18820adb917`  
		Last Modified: Fri, 08 May 2026 18:32:00 GMT  
		Size: 50.0 MB (50006715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e321fedc955b961c2c658a44d5ca3cbf39d67286d1387087c4563c14de6beaf2`  
		Last Modified: Fri, 08 May 2026 19:44:11 GMT  
		Size: 28.2 MB (28209562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50aed63d3cc12b285e748a36467b5f1679aeea9320464d6cdbf22ef3646a881c`  
		Last Modified: Fri, 08 May 2026 23:05:49 GMT  
		Size: 79.1 MB (79125872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:73856751e0d97c88dfcc03a64a1c874bc6f29394a811d4e5450bc2320f5e9f9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8273020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54f65c429db5bd4b5cbf7e1d2e65fee976cee2685d75e639acc17495e930a75`

```dockerfile
```

-	Layers:
	-	`sha256:deb2fdf91a1e7f576f731d18b89d3bd638e58fe2408fbed9fbb3a025228a6585`  
		Last Modified: Fri, 08 May 2026 23:05:47 GMT  
		Size: 8.3 MB (8265788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e778993dd59d7f9d0410c32521410e807512b6bc6a82900ee678303d33a2d38`  
		Last Modified: Fri, 08 May 2026 23:05:46 GMT  
		Size: 7.2 KB (7232 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:400c977e968a7c50372c9f5dfcfcda57ba857168f4f9e4fa6a82f6d6eb846e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166758642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1f08d72035ebcd4d6b07426fd06a6a0cddaa7a1cc395c512084a3492f48d746`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 22:31:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 09 May 2026 03:28:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9f402971e72fa142c9d15dd5eaca638787cb5c2e5a412bb3f2a7c4f896ed18ae`  
		Last Modified: Fri, 08 May 2026 19:45:34 GMT  
		Size: 54.0 MB (54028078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14bf1fa31e28d06ce5dc3e4b127ed62c78c28290930f8041edab4719b7e2e73`  
		Last Modified: Fri, 08 May 2026 22:31:40 GMT  
		Size: 29.3 MB (29286747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc335114670a5a7b57fda466c409652b52365286d8f06c4929c70e5424f0edc`  
		Last Modified: Sat, 09 May 2026 03:28:39 GMT  
		Size: 83.4 MB (83443817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b4a5922e8701bb34d0686c961edecc7dbf6191a8cd29dc5715b8ffd306d7e6c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8262549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe12c6ed7cd8c0682828ceb01215c92693f4d76b66a752b4222cdcec8a506bf`

```dockerfile
```

-	Layers:
	-	`sha256:c022a8e1c58d265692c6bed4ad8e15ed10badb7c0db5f93df75a701dd9c06ebf`  
		Last Modified: Sat, 09 May 2026 03:28:37 GMT  
		Size: 8.3 MB (8255263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cade0e66213ec7d4e2d0844bbaf27bb6ba9b63860e07123fe763b692e115c54`  
		Last Modified: Sat, 09 May 2026 03:28:37 GMT  
		Size: 7.3 KB (7286 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:92a08c10eeeb210a05561cec750849521999a13293f0ee2d36d050de11e51a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148605270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60a5978fccc8fa704dc1da9d5955722be336010632c3f58c825321719c1b42e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1777939200'
# Mon, 11 May 2026 00:52:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 May 2026 00:41:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:291921d355da34dfbce324263312328392c6a6c78ee971f9b4d7d37f1527cd2e`  
		Last Modified: Fri, 08 May 2026 20:26:01 GMT  
		Size: 46.8 MB (46838649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340855859b1344ded89a6e027caa6be811a60e26a4f08013b27235c463879b0e`  
		Last Modified: Mon, 11 May 2026 00:53:36 GMT  
		Size: 26.5 MB (26453358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5edc8a79553eb62a40d99b38aaa32211fc341a1f9cbd23a6cfe2581ef0fd704`  
		Last Modified: Tue, 12 May 2026 00:45:17 GMT  
		Size: 75.3 MB (75313263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9d5c6f7b824d880e3a468dc7a1947b4a90dea4fb0f7eb4a4ad16d79da03e5b5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8266649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1c8c871ff831a14d6dcae5404d23df702d19579d2379ff88a5e2b88e3908140`

```dockerfile
```

-	Layers:
	-	`sha256:5a99e4460f43613856645494c5602ee26e5458ff787f391170bb050985336be8`  
		Last Modified: Tue, 12 May 2026 00:45:08 GMT  
		Size: 8.3 MB (8259364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfe195eaa633b634643a6b7e6aa3d6b8915f76c91cff1cc239c647ae5d81ee52`  
		Last Modified: Tue, 12 May 2026 00:45:06 GMT  
		Size: 7.3 KB (7285 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ee8e036daa7321dcb0ac41240a86f2e09a87d00bb225f94cec25657350fb1eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152560509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1256489d7d52a27d65cb3d306fa7197d663024627525b1bae725ff5d46fa70a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1777939200'
# Fri, 08 May 2026 20:53:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Fri, 08 May 2026 22:33:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:107669ad500d1f91592ad03e52cc25095058c6b4b2e83b9adad6737bfa81cd40`  
		Last Modified: Fri, 08 May 2026 18:28:19 GMT  
		Size: 48.4 MB (48444076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc97077ab9739db4cafdc266dad352532794bc43462c59a59b2c72e9905c9a6b`  
		Last Modified: Fri, 08 May 2026 20:53:40 GMT  
		Size: 26.7 MB (26690958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff287d664c958fce4515d8b2c20dabe46ef9c7409eb524b5663736abf250d5a`  
		Last Modified: Fri, 08 May 2026 22:34:02 GMT  
		Size: 77.4 MB (77425475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5558fb6c634e226812bfc9d617bd013a4e58fd4aa2ce99f363992e9a7ae58eca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.3 MB (8255412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce3345d105438f74095b98a46032d1388bc2d903b6e6fde87352b489d56482cc`

```dockerfile
```

-	Layers:
	-	`sha256:6bbed308cc92d5b7116e936ec134dc590c4384ea99b57d95bd3b3973cec0aed8`  
		Last Modified: Fri, 08 May 2026 22:34:01 GMT  
		Size: 8.2 MB (8248159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bc0e33d114ff9ed44f1da1e8609c2f6d6f4d12763dc72c12b52434c487ec48b`  
		Last Modified: Fri, 08 May 2026 22:34:00 GMT  
		Size: 7.3 KB (7253 bytes)  
		MIME: application/vnd.in-toto+json
