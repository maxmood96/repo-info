## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:0d6e9a85d1e632b9398b5021455bfd29ef0a9bc8f446f973fbaccb2cdd5c79cb
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

### `buildpack-deps:unstable-curl` - unknown; unknown

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
$ docker pull buildpack-deps@sha256:1462ecdaf1f80ea6299f72b7f24cd2fc1085e5d135d00bb1c15117c8c48ace8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69288386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4de4038123052ff39549b1543dfc64d086b9d53352dafa99d5a88ec546c7ba6f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1747699200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:766cbe9ca16b5ae7e32cf18657be459754ce87056cceebf6831ed9c18fd8a62b`  
		Last Modified: Tue, 03 Jun 2025 18:04:06 GMT  
		Size: 45.7 MB (45698630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b248e723f972fd882067b040659dac6bf0007c9489588821ca8240ce91487131`  
		Last Modified: Thu, 22 May 2025 02:29:17 GMT  
		Size: 23.6 MB (23589756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:60c3615fc6e9125883b8253f01f9e9c828e161b7e02fd4933ea45565c243e7d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4004794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c1091361550cb9b2cb26f5ab0103db43da4a5451786321fe56e4246519f421`

```dockerfile
```

-	Layers:
	-	`sha256:2bfbcd98e5cbf3590285398178b2b73851bc0ca462fc18ec506cc7e95b95f408`  
		Last Modified: Thu, 05 Jun 2025 08:47:27 GMT  
		Size: 4.0 MB (3997930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:477b78f74185b49abaf38c673e5adbbe94ac5ac0b0ecc31366570aca1b2c3547`  
		Last Modified: Thu, 05 Jun 2025 08:47:28 GMT  
		Size: 6.9 KB (6864 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b78f989028c2c93ea81827a11563c39121dbd4583eb4eec119c095cd90def747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74593899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4494982ae30620e19904cabe26b1f716f940f723c3b746851aa9fb46b1d8b0cf`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1747699200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4d7c750dee99fc4f87ba2d4a7a97efd437e614ec9079e7fbf547ab9ce640bc68`  
		Last Modified: Tue, 03 Jun 2025 13:30:58 GMT  
		Size: 49.6 MB (49617866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:945b158d051d6fdc917c4a2f2c9c640867150d5c68a1439dd536c0ff065f9eab`  
		Last Modified: Thu, 22 May 2025 02:48:22 GMT  
		Size: 25.0 MB (24976033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4903b50d39e515af980eeab4a89cdc0212cb25030a0f00bb08b0de6502574634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4004851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8437dfda8103c0cd47f7e8827d9cf524d6ba1f7876a3c530e01d547419267dc`

```dockerfile
```

-	Layers:
	-	`sha256:f810e6056517c438079de557d26fd0dbe0f4a6dfc75638e8777585cf46239692`  
		Last Modified: Thu, 05 Jun 2025 08:47:34 GMT  
		Size: 4.0 MB (3997967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b1d0337d2cf128132d6c0d9af576ac7ec4e5a16564645bcc6382a6295925fe4`  
		Last Modified: Thu, 05 Jun 2025 08:47:34 GMT  
		Size: 6.9 KB (6884 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; 386

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

### `buildpack-deps:unstable-curl` - unknown; unknown

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

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:0b96b97a6702a08e7e012563c87d04d4718c11d8254cfcec861891c6fef9ce64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75168159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213ebe73666422481c3b128740f6b07d451c2377d2bfb5f1981b8b668833aa5c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1747699200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:27b34307efc56192fd4ca945f6323e2158a324121ac08b2b6be4739d1a7a2345`  
		Last Modified: Tue, 10 Jun 2025 08:48:47 GMT  
		Size: 49.5 MB (49538322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff848add2d23cbb649ad48161ea5c02c3695dbc152c477b6b7b6ddde8893826a`  
		Last Modified: Thu, 22 May 2025 06:18:44 GMT  
		Size: 25.6 MB (25629837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ce3749956f896aeea1746bb48d523bbafac29d80452d136d4905c57f5b90d05c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 KB (6636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81e5048220f5581db960debf41dabb82c7e00fc7a36915816380d70fb129ff55`

```dockerfile
```

-	Layers:
	-	`sha256:aa05ee817519d8bfdad3b14f6b18c085fa2685d8a9ac533dd42158f2ed50342f`  
		Last Modified: Thu, 05 Jun 2025 08:47:47 GMT  
		Size: 6.6 KB (6636 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c1af6420f8d510aa97ba914e60f51069156dbcd4d87357062560d9f9e07e55ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80054491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a33faf22d755c0470c3efa89199816148c421367e2e1737e80db8cd7a59656a5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1747699200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:16f5e7cd9c9945be6c34f81a399d644f442eadb5c4f47f89a090f84971e9d67c`  
		Last Modified: Tue, 03 Jun 2025 18:04:05 GMT  
		Size: 53.1 MB (53087015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d194009a872a9d9be939ab0b551a2fd792af6fbbec9e72310f90b49fa15b755`  
		Last Modified: Thu, 22 May 2025 07:32:11 GMT  
		Size: 27.0 MB (26967476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6b969bc2fe2ca07fbfb60f810e158fade41303a5bd3d4a17fbfde6620c6f29b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4013473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f80fba626d0c1d0acc38523d0078521fbb912f7f5d5f845def42ef77422ba83`

```dockerfile
```

-	Layers:
	-	`sha256:16cf814f16c05f505cfd745e842343fc46959a0914600cdd6a37e523cda4a4a8`  
		Last Modified: Thu, 05 Jun 2025 08:47:52 GMT  
		Size: 4.0 MB (4006637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:639d2d44ea5d08b0225f250439c37601bd6ca3bb4c5da132e642b3da5a0fe69d`  
		Last Modified: Thu, 05 Jun 2025 08:47:52 GMT  
		Size: 6.8 KB (6836 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; riscv64

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

### `buildpack-deps:unstable-curl` - unknown; unknown

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
