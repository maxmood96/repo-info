## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:bf07ecdd0b915cf1cf590d07fc53b23ae7594e0ad6b05140b5ff04b04fb7ab7f
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

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:654513afd24124c5268771565fd51383c1fd9c0f99418ed0d2edb95931800554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74886854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77cdb0a9def6cb7b0386a8391ac13c5b122fc34dd110daeb4469148605a2e0f0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1751241600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:603de70df79137e44ed9b8e9d2eec3a1b8eb889b8a8650df1a6bfc2ba9798f72`  
		Last Modified: Tue, 01 Jul 2025 01:14:45 GMT  
		Size: 49.3 MB (49267699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b752883ea09044589f48c52df49289712f416806e7b67e6d3b283e6c96ac266`  
		Last Modified: Tue, 01 Jul 2025 02:25:34 GMT  
		Size: 25.6 MB (25619155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:45b2382862ae5fea93784e968e24b713b101ab3ed5c945358893c804e681177b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4123152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ba1b3c3e18944708504d4344276b111d2a6dde0df6e17fe396317d87c5b4f06`

```dockerfile
```

-	Layers:
	-	`sha256:562cf80b8109bd1774485edd87c58f7f8a7c689f665a42ff8c84ce566eb1f714`  
		Last Modified: Tue, 01 Jul 2025 04:20:48 GMT  
		Size: 4.1 MB (4116348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28af60a53eca2b641a4e7099ac92c04cde933992f292ae4df4441de7c28da685`  
		Last Modified: Tue, 01 Jul 2025 04:20:49 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:b238526e441563e724b85d82a1cb1a127695daf26407bbabcb0e1496c339742f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71763824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753c5fca6eadc7c5ff9148f165fafa6cd69dab63cbd2d21a76d96622531523b7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8344b2028cc05a08f8b0b577cc9430fd30421d98f7302a20cc79a7392635ca51`  
		Last Modified: Tue, 10 Jun 2025 22:47:59 GMT  
		Size: 47.4 MB (47435203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e8ec6927bc0cb7d56e990391b853ec23d7d3eb74a5f1f9500df8d5cf23ea4d`  
		Last Modified: Wed, 11 Jun 2025 03:13:46 GMT  
		Size: 24.3 MB (24328621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9216cdcbc23d88cb2f42f09bc16c07e5af7a37473f126912fdac387d0013c8ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:733900ab8d90e40c32c3d316efe78062e3f1b7251e88516472778cb7597c394b`

```dockerfile
```

-	Layers:
	-	`sha256:e47d697387141f1b5bc6313fe79050d670beb63fd33121a227d2b991a350a280`  
		Last Modified: Wed, 11 Jun 2025 04:20:56 GMT  
		Size: 4.1 MB (4123729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2505eb332215b3aa679bc514fcb3feb47098df8d09827255da840f6e2003309d`  
		Last Modified: Wed, 11 Jun 2025 04:20:57 GMT  
		Size: 6.9 KB (6864 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:2095cc863bd975584d63a2d76546cf9dafd0158d4e64c26fea62a353724237cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69309281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b8ff0fb62f77ef88e2d31147b56cdeedd818b3d57f3b820949e0da08e5cfea1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0ceacdda8a07413d9c26c141b0f4894fae020e6ab65ff0188cce0bfe5e0c66eb`  
		Last Modified: Wed, 11 Jun 2025 01:10:03 GMT  
		Size: 45.7 MB (45707825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b841f0ab46f7d7bc86d75d499d470af27c2315d80feaa41746c1f9e6d995ef`  
		Last Modified: Fri, 13 Jun 2025 17:03:18 GMT  
		Size: 23.6 MB (23601456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5766a16244b4a5f33e099931f537bf79bd6179bf216e5efa84135cf15b4c1191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4119851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a85d067a1358b86e911adc3fa9d549eb1d794a82d64c76938e807ccebd8719`

```dockerfile
```

-	Layers:
	-	`sha256:3cd905b564c5349002558d26e061be67a090f8b2c36465823da0840c5bcbc57c`  
		Last Modified: Wed, 11 Jun 2025 07:20:26 GMT  
		Size: 4.1 MB (4112987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c69cac302cf7cbb904905b55f9ba67424abf9ceb0c579624a0576145bd4b0a17`  
		Last Modified: Wed, 11 Jun 2025 07:20:27 GMT  
		Size: 6.9 KB (6864 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:dffe4b7f52fe14f38ec07af3f655f294d0e58689e9a5c20045939c93b7a61cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74628216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac5079fda72395642ac1ca98753b1d9ca16d99acf25eb2d6c2242a9c0feb9d8c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4b10e85b1b46df396d3cb4118de7b2483607b89bcd163318c9756c711f9a3ef9`  
		Last Modified: Wed, 11 Jun 2025 00:37:10 GMT  
		Size: 49.6 MB (49629348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae44e59140036c47291ca98d6f5cbe09bbc2c6ff2f7067e6ed8f93f2a9ed0b71`  
		Last Modified: Wed, 11 Jun 2025 08:13:09 GMT  
		Size: 25.0 MB (24998868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b95a97b14bfff46cee4af236428aa0cf7348ae44dcfdda6ea73cba5f7cbf5da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4119907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4fa1fa0170e625a3504f68420a1f882779f31672c49b2408e17cd036d7c69a3`

```dockerfile
```

-	Layers:
	-	`sha256:21eec5c3b68d76c5162152d063fb71ec58529c4c0a575911985c3fa82937d05c`  
		Last Modified: Wed, 11 Jun 2025 10:20:23 GMT  
		Size: 4.1 MB (4113024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dd1dfa113e1ec8cbac301d2200b85a057fe7ed30c64851594d59286d3d1406f`  
		Last Modified: Wed, 11 Jun 2025 10:20:24 GMT  
		Size: 6.9 KB (6883 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:4848cb8958e59c8a99bac261484cac96913f11a63b6407b912418b851cca5a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77564681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f13fba4530d699681e350a1a6046a40b1734a761458d39fc34fee8a39e2a6f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1751241600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:41ea081e29dc4034ec31a49ac48ddbf738b840fd4d226f5678cb63f00b10ab33`  
		Last Modified: Tue, 01 Jul 2025 01:15:01 GMT  
		Size: 50.8 MB (50790707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d224078a83c5498b9115edbeec34eecaddc04a9e2e47f0e71d34a7e780a2059`  
		Last Modified: Tue, 01 Jul 2025 02:24:36 GMT  
		Size: 26.8 MB (26773974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5ab817c95a9a87697518b7f53cc6d7b9eab350c517fc22d6e195563bd930bf27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4120244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54c4d23417ce2440b19b36f28dfcc8baec06b1517d5f9bd05fd8a728f0bf8807`

```dockerfile
```

-	Layers:
	-	`sha256:7db5376dca3bb6b0daed7846deacb032e32aa5501c1a7af5a30b436ab76fd363`  
		Last Modified: Tue, 01 Jul 2025 04:21:02 GMT  
		Size: 4.1 MB (4113462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa89909bfb0ee9f9f14e0ab57c5eec90906fc5bc279788fbde05eb1d31e7bdb9`  
		Last Modified: Tue, 01 Jul 2025 04:21:02 GMT  
		Size: 6.8 KB (6782 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:736d556118c98f04baaf5ed6af93fb2ff43f0768919e881716a85f1a415ab770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75205324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75ef1e5d1901dc2b53b608215bda89d5c73d3e85618337df07e4d4953c501ffc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:54a8735d26fa76df64dcf3824b7f78b58d44ea01ab0788f2fc33afa2bac4f1ad`  
		Last Modified: Tue, 10 Jun 2025 22:48:52 GMT  
		Size: 49.6 MB (49553255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06ee97fbcbae75cf1777c40791b1a1c25100c4b6ad8a9ed9323cceb66a38ba5`  
		Last Modified: Wed, 11 Jun 2025 13:02:36 GMT  
		Size: 25.7 MB (25652069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dcfc08e37a4072f695cc43faa4e5e4d6b75eda3f90c66fe8e05a0f49a0f881f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 KB (6637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff4c7cc821cb1c55b46d66545c7b243ba67c7b44f6d3d54c7744ccb47b458c81`

```dockerfile
```

-	Layers:
	-	`sha256:d0fa1bcd89009ccad16bf025df0b28955a4c5336467890c1b27f77fac83be450`  
		Last Modified: Wed, 11 Jun 2025 13:20:50 GMT  
		Size: 6.6 KB (6637 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b6b29a2a99a0b8fe0cbe2853fb47fab3753c2a1bcee9bb86a46622be2675a8bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80082305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a63cc49fdd5f0373888a70c72635838264c9c26d84b3cc3ec3382ec65a5f785`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f34e3f5941a9b9d7f66cc62bea1f477c727df8c87b640bd63d443c8cb4c08203`  
		Last Modified: Wed, 11 Jun 2025 00:27:42 GMT  
		Size: 53.1 MB (53098680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f227a2066e39def58b490c6183c1c743b3db44ed881ae2f1d7f6c8febfbc6b1`  
		Last Modified: Wed, 11 Jun 2025 17:42:13 GMT  
		Size: 27.0 MB (26983625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d4b40b0a0a3574ceae17f7c0b11e7f632777717d79f075e67ea08c7d02a6ed3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4131409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543a13b707a4d306fd7b280d0d9dd213d4602109a973a2ca2e7bea67c970dd4f`

```dockerfile
```

-	Layers:
	-	`sha256:326225cf8779a59b7520d3e213efd5d2c4a65c824ab6c3a632ac4829b70cfc1d`  
		Last Modified: Wed, 11 Jun 2025 19:20:52 GMT  
		Size: 4.1 MB (4124573 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff65942bd488f45244d05fb2dda98afd8f274808557b322f7b01a466de633340`  
		Last Modified: Wed, 11 Jun 2025 19:20:53 GMT  
		Size: 6.8 KB (6836 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:d0634f4ca8ef432fe4e5a6f97834ef6566193409b32f7c3545333962aac7515c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72710402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f373cc57bcde4de73b79210120045874c92075ae5e2f932ef82dc84b996c4ec0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1751241600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:42f7c08d656e09c01f14d35a847143f84e881d1ac3f16f3ba511348bbbaa7d82`  
		Last Modified: Tue, 01 Jul 2025 03:27:03 GMT  
		Size: 47.8 MB (47756066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a4ef3bea202b6f661456b37f5106a6a6e0acda6439394bd6618c6150a35c24`  
		Last Modified: Tue, 01 Jul 2025 02:22:42 GMT  
		Size: 25.0 MB (24954336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5497e20292f151afda9297e6e3184eaa7a156b1d6d42049ae82baf9cbc06f652
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4115685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ac6cb738fc2a1e1dd7a3330ca224ad0b1bb727bbe6dd2198be9bf7f5b6875c`

```dockerfile
```

-	Layers:
	-	`sha256:e127e6ba2ee46cb75c1b7b09deabdaf0eafb2f8a6023c394dfa6064ede62ad3a`  
		Last Modified: Tue, 01 Jul 2025 04:21:11 GMT  
		Size: 4.1 MB (4108850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fa5889f086e2e9067b7dbe415cd146af117731cbaaff83543968cb5625cf1ae`  
		Last Modified: Tue, 01 Jul 2025 04:21:12 GMT  
		Size: 6.8 KB (6835 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8a10c9dfbded227154ef086b01ca2b4a489795654f41f7eaf36aeae5657acd5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76112373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb7d0b364f20f178372032ccd43a8b0f1306c0a6885bbcd429e77dd50c4f9db`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a52b4c8ce9959e1107790b0cf878188904eecb5b1ccf411d93d6ab16036dc160`  
		Last Modified: Wed, 11 Jun 2025 02:03:33 GMT  
		Size: 49.3 MB (49343092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf0965e23eb9d70e72f15582a2cb686bcf1857eb924b4d704542fc37d206146`  
		Last Modified: Wed, 11 Jun 2025 02:51:24 GMT  
		Size: 26.8 MB (26769281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2346cc3445cf1fdc85c944d073a27683c7a9ad152a519a8618f72b1f487c4cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4129772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebdc0f4fc6fd90b262d9c247645a36529cc0b09359c7c9af1017d8f6479df9b0`

```dockerfile
```

-	Layers:
	-	`sha256:4847de9815074a250340958fbaafb4aee167ef8c7f020fd69ef374f578d70f47`  
		Last Modified: Wed, 11 Jun 2025 04:21:20 GMT  
		Size: 4.1 MB (4122970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e0bb5c017fe3b12ca1a4d1072389eb7ba51bdd2bb3aa70831f4a77b1ec2751a`  
		Last Modified: Wed, 11 Jun 2025 04:21:21 GMT  
		Size: 6.8 KB (6802 bytes)  
		MIME: application/vnd.in-toto+json
