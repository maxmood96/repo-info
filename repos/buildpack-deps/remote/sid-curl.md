## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:5dade3d2f4e427b04eb27b5da01236a98e141a2b4c2985f6a039520c901c10c0
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

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7c309b31aa4fe6ffca4869db0155727d8630637a53a928bb6e199e19c9cb8263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74867248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fa08c6cf0f8ecb9c81c41e618b5757171db73bd80d96cb2c435ae0f1e467529`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6b1598688dd5948f64dc955f58b0dcf5627fc6bbc5754f5ea08612c6d3bace8b`  
		Last Modified: Tue, 10 Jun 2025 23:26:12 GMT  
		Size: 49.3 MB (49263317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05cec2bdcd950987565d27e6bef170159a9fdde6f46531b0889933354046db48`  
		Last Modified: Wed, 11 Jun 2025 00:01:47 GMT  
		Size: 25.6 MB (25603931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1feb8a384e642dde260c601391b03025af1da3762278b44feaeeac839b3bb92b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4118298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4393bb8d424eee93edd8f4d13999fd1564611de191ec9f529f08466c754d56a5`

```dockerfile
```

-	Layers:
	-	`sha256:b7a846425f3f4a6600119efbf76f861347b9a91fc883793241a0920d02199abf`  
		Last Modified: Wed, 11 Jun 2025 01:20:38 GMT  
		Size: 4.1 MB (4111494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eeabc0d12a799240f305b7e7509a46ff35815765c0aaf7a805ec9d4de0d8538`  
		Last Modified: Wed, 11 Jun 2025 01:20:39 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm variant v5

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

### `buildpack-deps:sid-curl` - unknown; unknown

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

### `buildpack-deps:sid-curl` - linux; arm variant v7

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
		Last Modified: Wed, 11 Jun 2025 04:58:57 GMT  
		Size: 23.6 MB (23601456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

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

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

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

### `buildpack-deps:sid-curl` - unknown; unknown

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

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:19ddef69b0c3678f54bcade0b5dc880a4ab07bc764938d209e9358b32c73ec19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77545178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51befaf6ff2d9d551f1ebcffb383b622a61c63094ebbd29f57aca1fc2288904b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1a1a02b91b1c2266da4734f34b831bb020d740f7bfd0647d1828242b377de717`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 50.8 MB (50786017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13c1899ec001f75529ee8cd455eb4a23c4b9c5414c63db7730474213c55437b`  
		Last Modified: Tue, 10 Jun 2025 23:36:16 GMT  
		Size: 26.8 MB (26759161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:23fdd76a6f1967d002b0a981fcf9d9efbe9fc9bf724551476817bb7fecc6f6d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4115395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a787d533f4f61aef3f9a9e98274b8a1aa8daef26d25ddf43949afab74a5afc3a`

```dockerfile
```

-	Layers:
	-	`sha256:73e16e60dddf00b5ccd14c6142455c5ff1299eb84335dbeec25c26c23700daf1`  
		Last Modified: Wed, 11 Jun 2025 01:21:00 GMT  
		Size: 4.1 MB (4108614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c16e1a3b1bcce0c618cb6f0025c85e958b3653e4ea3c391ae502340c4c9a22a5`  
		Last Modified: Wed, 11 Jun 2025 01:21:01 GMT  
		Size: 6.8 KB (6781 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; mips64le

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

### `buildpack-deps:sid-curl` - unknown; unknown

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

### `buildpack-deps:sid-curl` - linux; ppc64le

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

### `buildpack-deps:sid-curl` - unknown; unknown

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

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:fccd74e61e40aee3bb92522daaa1254aa92e8cb90f6f5ac5ef513b96673297b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72689470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adad498e6a12c5a017d59ee9d89b324bde784b3c3505288301068a9683cdb3e3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1749513600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0009e91f3f8c4153a02b39dc6e9b3c5a36cc3c8e1a157d73e8f9e91097515059`  
		Last Modified: Wed, 11 Jun 2025 02:03:30 GMT  
		Size: 47.7 MB (47749671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df49454d4e709bab7fd6d2461b736d24ce3db865904adb84e1af7a3e0716ace`  
		Last Modified: Tue, 10 Jun 2025 23:34:49 GMT  
		Size: 24.9 MB (24939799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7f85f101d3a77c0afed931c1aa1e4e9b4ccbeee44af0cfd0aa62cf030b45cba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4110819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a2d9d4ca29f73ca36715c1446e4fe02e16b0b2f725042d696b51264130d32b`

```dockerfile
```

-	Layers:
	-	`sha256:0add62d72aaf8e87148d29aaa9a6d8b01d88870ab642104f4ec7e3d2f07bca68`  
		Last Modified: Wed, 11 Jun 2025 01:21:15 GMT  
		Size: 4.1 MB (4103984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6692f736f748ca19d11cc3a7aec3bc416376ea5ec6aef25efd2eb4be885cfd40`  
		Last Modified: Wed, 11 Jun 2025 01:21:16 GMT  
		Size: 6.8 KB (6835 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; s390x

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

### `buildpack-deps:sid-curl` - unknown; unknown

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
