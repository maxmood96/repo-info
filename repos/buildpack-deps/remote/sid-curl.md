## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:07ac017a558e7466715462cbcf737c28efa4e25943c7145eb67bb751830ff3ad
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
$ docker pull buildpack-deps@sha256:204fc7cb93e6b1c5d3701d9bb7b17f47f36c32312b13aab7a3e1eecb149cae55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73507803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d3aa6b1c65c3ca1c85ad847490f6b3aaaa53facd8fbf401d4ddec6b5807971`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9d0fec2ddc88227c9ea9ee67204e0e6a57a98553e405c78f6403be7627bc3834`  
		Last Modified: Tue, 03 Dec 2024 01:27:34 GMT  
		Size: 52.1 MB (52141610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e69332be439e88615e518602f8f7a133592f44d454cc5181ec830b7d4907dc`  
		Last Modified: Tue, 03 Dec 2024 02:28:57 GMT  
		Size: 21.4 MB (21366193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3c19b6e7dc1bfd1817f85314eb3cad6f9b646341f80cd03cd40656b1ede3672b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4050455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f15c4d7443fd64f1c8254c1ccb0d676a805bf354e184fbf250932ab147b99693`

```dockerfile
```

-	Layers:
	-	`sha256:8b30370abcd3c800357528cee52c171f19f828ebd96c3d2beb8fb8bb113da450`  
		Last Modified: Tue, 03 Dec 2024 02:28:56 GMT  
		Size: 4.0 MB (4043653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44bc99210dbb035b3c8e40a98c8830893bcf5823bcaab362c506ced9d2e06c17`  
		Last Modified: Tue, 03 Dec 2024 02:28:56 GMT  
		Size: 6.8 KB (6802 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e0c26364853da5e75896f031d3d2066ca0b0ebea6064c0802e48cb002b909a39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68963624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2e1229b95235bac1c5cbcf446d7e9e39ec403dd559a52fa597f5ea92286169`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:73a543e699956c37f431f5272a06bec8db5c16078190c6cd83886ca8de7b3dce`  
		Last Modified: Tue, 03 Dec 2024 01:27:39 GMT  
		Size: 48.7 MB (48676786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f2a807b7a079a7e314d111ccef3f84d1aec497cac9fbafa581f1603c0f9618`  
		Last Modified: Tue, 03 Dec 2024 05:24:32 GMT  
		Size: 20.3 MB (20286838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:81227ab69595f9829c5e51c760a792f754393155a80fa9e5c7ea97270b64b66c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4052738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd6a50c2ec5b6f28659d8ac5731b5b191b0bef1493df2890fece6c6bda7b1918`

```dockerfile
```

-	Layers:
	-	`sha256:8a6d09a593299d0ecf8ccbedf48989b9fa1e80596cba5f0888fd729d08e03de0`  
		Last Modified: Tue, 03 Dec 2024 05:24:31 GMT  
		Size: 4.0 MB (4045875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3815fe36d9422647ced3357e6453c8f5a123a633108c99d47a75621924d53a30`  
		Last Modified: Tue, 03 Dec 2024 05:24:31 GMT  
		Size: 6.9 KB (6863 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:cc4b2bdff03629d69feb728d273e0d532e0d425550d77fc4d428a98662e506ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66305777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08dd76319b781f4765aebe68e8f8f83425d978da56b8908c1f9a09fd10cd4fac`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b3be1b8d31fc4a12cecca1f9e259b73553bed584845788fd1fc2b66b29ec0da2`  
		Last Modified: Tue, 03 Dec 2024 01:29:47 GMT  
		Size: 46.7 MB (46707234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9942887cd0e4c0dbd616c261161d431660cfe04df19f0fb88f7040ab43995e`  
		Last Modified: Tue, 03 Dec 2024 07:37:28 GMT  
		Size: 19.6 MB (19598543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:07eef967eb655fb18f0d2c2c11f4c816279a67bdd59790b99251f3f5e1d908e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18671eba9c6dac63abf5e1aacde8418a8ec079f015aba5a58f71d647b0eb7f11`

```dockerfile
```

-	Layers:
	-	`sha256:a73bb5456d7763921c5061137bf4a7b19f10585c609ef3370e5bd8e6975c4870`  
		Last Modified: Tue, 03 Dec 2024 07:37:27 GMT  
		Size: 4.0 MB (4044673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c5cb0ef0323af3e1a3e008d5e57343569405babcfaa127188257693204bc034`  
		Last Modified: Tue, 03 Dec 2024 07:37:27 GMT  
		Size: 6.9 KB (6864 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8ea9887f4714527d9d5254f762de02c92d4f7bae369fa18b0ba9ee5d8a5f7a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73347527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b445d459eed6e2aaa0ca2873d2fef7a47c8f779e4e527578f018fee5542d5d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b484292747a3f8af5e498e897086e128c39ecc7aa3e027f8ce6a7b27ab3585c8`  
		Last Modified: Tue, 03 Dec 2024 01:31:21 GMT  
		Size: 52.4 MB (52363551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb4e12ac809713029b921818f315112d9a68fd814039c91956b3cdd9d07cd03`  
		Last Modified: Tue, 03 Dec 2024 05:39:40 GMT  
		Size: 21.0 MB (20983976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:efb2879bdbe93ed419ee51ad67c5b73260cbe9762f879b6525c357a6a1c79dfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4054793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0104e88a325a66592832bfa12159a43f2db9c0662ddc2a476e9b5b61eefe533`

```dockerfile
```

-	Layers:
	-	`sha256:21a43c5405ce1ce47e7024330b2a77d04d6962e99937eb27750094d8f9088a75`  
		Last Modified: Tue, 03 Dec 2024 05:39:38 GMT  
		Size: 4.0 MB (4047909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e42bbda426096d69b867a0dc63238898e7dbec844f816cdc22f46d8ec7561d9`  
		Last Modified: Tue, 03 Dec 2024 05:39:38 GMT  
		Size: 6.9 KB (6884 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:8dae1c26ca64bef3fd697b7cf02f4b2c366e85a6c73f01b5e0b9afb622c5fdb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75501171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875a11a23487b00a03f1f0044e25daf842fb4cdab0a6dcdb4c3a2f74eda5811d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ef86bca2ffea293f73079f660a3399886008871df454d90312b7145d4395af98`  
		Last Modified: Tue, 03 Dec 2024 01:27:14 GMT  
		Size: 53.0 MB (52973420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183206547155d13d62e451041e3603fd7f5a0f4b1d6c8db0eaaf7ca1b4e51b07`  
		Last Modified: Tue, 03 Dec 2024 02:14:44 GMT  
		Size: 22.5 MB (22527751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fc30c76fa56490aa8d4359be5a51f884a93180fe27ba95093b6f4249461d8ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4046182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526990c3201f01d1bd4d6d57dcf3e812be838f5800ba8ff10188b3839c34d19c`

```dockerfile
```

-	Layers:
	-	`sha256:ef89ebeb6f21e1f73525cefa6b3bb32a2c605d18a8f97b9fd5da7036c0295c46`  
		Last Modified: Tue, 03 Dec 2024 02:14:43 GMT  
		Size: 4.0 MB (4039400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d6a2f676cc8e92c792af6635a13a376cb77dde477c35e1d9465bf4009920b0d`  
		Last Modified: Tue, 03 Dec 2024 02:14:43 GMT  
		Size: 6.8 KB (6782 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:62e1a2cab54ce402ef56d67975b9e97f7db49042e7d9bcf2803dad0e2b4f5507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73225428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f90f18670b8a0f2f53c92f8dd49e6e04300c5b5b5ee0a08f2c595286336db07`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 12 Jan 2024 22:06:44 GMT
CMD ["bash"]
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1f6d00c97864e98dad498c4c1087cda2fb16f2ac6e7a71ac1353418dd4215995`  
		Last Modified: Tue, 12 Nov 2024 00:59:58 GMT  
		Size: 52.3 MB (52275237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ee73bc743170bb5e4087d57c95a63d610fb1282220d73ff90af4707b831d99`  
		Last Modified: Tue, 12 Nov 2024 18:03:00 GMT  
		Size: 21.0 MB (20950191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2cd9138da59d486eee86b97f0b2ef5c327cbddacc8555d0ca1e2f100ddab0c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 KB (6635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e8f2688580c7be9086b175b4a45597708a571c9d0545210c877212967e0e9a`

```dockerfile
```

-	Layers:
	-	`sha256:6c68010a95014043302ab3a4f944d5dd5ce7882ce431430ff613035bcd549ba7`  
		Last Modified: Tue, 12 Nov 2024 18:02:58 GMT  
		Size: 6.6 KB (6635 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:47ee79acdeb89205c257ecbedda3b0eb55e581f832165079a17a7b01cd288b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.8 MB (78781979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32bcf58578328b1231b58d5b8944d36bc4ba40ee49ae98c44558d7b7ed3a54ea`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f96af90d82a1692028e6cdf912ac7419c2ecdd75603a19fc1f1b3b9e9bd29a53`  
		Last Modified: Tue, 03 Dec 2024 01:29:07 GMT  
		Size: 56.0 MB (55979543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5109fb930f5078004be0affb782c6af72db917a8e8c95675e33088c19131df3`  
		Last Modified: Tue, 03 Dec 2024 04:37:41 GMT  
		Size: 22.8 MB (22802436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1264f415c874219bf1d93ed1a65ffb3823a4a931fed9bcc0dd443056df716e5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4053760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39caff4ffb294476abd1b4095aa9254d65feebe0abe1b8add2b60d2243cee46b`

```dockerfile
```

-	Layers:
	-	`sha256:cf5ac8a981390a4e2c3640c75cbafcab45c0cda33f1490731ff4029c7048ddfc`  
		Last Modified: Tue, 03 Dec 2024 04:37:40 GMT  
		Size: 4.0 MB (4046924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9669a33d493726e89d132782bdb9de12e182fd2b8f0009472a97ff07522a0575`  
		Last Modified: Tue, 03 Dec 2024 04:37:40 GMT  
		Size: 6.8 KB (6836 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:b586a30adedcf91253b4e723a2fb98577d3112ba0edafae4a3169cbbe4b467c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71455404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f858b529436819defd2e23a4d8d4cc35636897a62586414cf76f538931ad6e5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6a129056497962be3ca4efb9ff44f747d1222200200be5fae7999b10e3156cc0`  
		Last Modified: Tue, 03 Dec 2024 01:29:15 GMT  
		Size: 50.6 MB (50632627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d233c7b4fb57ebb3fc06e5b0c070fac8c8f89639814479f25441c1938943ba`  
		Last Modified: Tue, 03 Dec 2024 02:51:09 GMT  
		Size: 20.8 MB (20822777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d4b9830bd87fccccf6e3080d90de56b90eaabeba62546b0628aefaa4ae2da16b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4043359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103e57e6a56d779b28625d6494beb70b785b3fc5feb250ae02f6560c186c31de`

```dockerfile
```

-	Layers:
	-	`sha256:bbef88f018a4f6f847dcbacbd9fae201001983766aaa9ba52cf76fcc836d22c6`  
		Last Modified: Tue, 03 Dec 2024 02:51:06 GMT  
		Size: 4.0 MB (4036523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f42fe56ae477e436b08ca6348817a884c70598cd0cf20f64af658727e556813`  
		Last Modified: Tue, 03 Dec 2024 02:51:06 GMT  
		Size: 6.8 KB (6836 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:aa8bd5667c1e53625735710349a9740d77fa5aaa879d3a977adf6247b361421c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74643612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4653b03d76739840fe4be4479dc8274aefd31736a0302005a389e88cbf472bc0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1733097600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5d3fd94703dd00b00c7acc09539942c89a4634b13c2ae0ee29086b6288d43a47`  
		Last Modified: Tue, 03 Dec 2024 01:29:01 GMT  
		Size: 52.1 MB (52083835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79c38d4fbdb1d980e95882f99ea9064cdd90b1c1070a263467e442acb813b03`  
		Last Modified: Tue, 03 Dec 2024 04:08:31 GMT  
		Size: 22.6 MB (22559777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c50b19b70400d98afbb0a18ed63e699890ce23cddf01fc0abb0fbfe916dbfe6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4056542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0cb0567221a8fdf7e234accf3825319db8e5a4ce9cfa46e3d7f786610a1bdb5`

```dockerfile
```

-	Layers:
	-	`sha256:0e58fd28fae7b037ea9d243d9a380a50fd4bf594f2960b0e40d34a4510d2522c`  
		Last Modified: Tue, 03 Dec 2024 04:08:31 GMT  
		Size: 4.0 MB (4049739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:367e00e07da6a96ad160be887964afb0f841afb80806423c924a594dcf18c990`  
		Last Modified: Tue, 03 Dec 2024 04:08:31 GMT  
		Size: 6.8 KB (6803 bytes)  
		MIME: application/vnd.in-toto+json
