## `buildpack-deps:forky-curl`

```console
$ docker pull buildpack-deps@sha256:e779b0a414ab58d27f38fb1cc4d33e24edd61bebb0bb483233360045cfe4f1a8
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

### `buildpack-deps:forky-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:1ba9a0fc2f2048c852bf79ccea5dbd0199a7a547cb6ddd225119774b3220de59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75899436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e1b40c2f0585d78d3bb9eb1efa3b5ce87e1d5ee5041a4e0f9d371cd31ebb6c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 19:19:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:501906f379a13fc3675791cbd6304f648074973affcb965be0bef8b0aaa34ab5`  
		Last Modified: Tue, 24 Feb 2026 18:43:03 GMT  
		Size: 48.7 MB (48677181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9812e820910835e26da6ba184eb7321a186fd35437a98105291c93a0a34f38b7`  
		Last Modified: Tue, 24 Feb 2026 19:19:41 GMT  
		Size: 27.2 MB (27222255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d6302ea1d043883c4b9b33ae4d98310a9b5b369017375be86a5e384ba0f45c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4133554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79803e23f3aa419d0e46e68b92ddff0640c3fe1e1fe358c6d22e003eda6969bc`

```dockerfile
```

-	Layers:
	-	`sha256:7987d0982cec6c8c637723ca82f7b3f260ecd63d25f4845f17b74e5c26d0ba2b`  
		Last Modified: Tue, 24 Feb 2026 19:19:41 GMT  
		Size: 4.1 MB (4126781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8234c73f6d88a9e842829136975b665dda844f4c54f7382442d63bf0d88c4b9b`  
		Last Modified: Tue, 24 Feb 2026 19:19:40 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:87cd5a454968b0dac37f3afc005e5f8c7380c15ef5f8885095cf571a2a2df08d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70573408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7682e44ef7c43f8adbdf2e76608e6504f2de19c91efec3e11937199ff6ea96dc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 20:04:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b74010850dba4ef4e0d65d4c6bda126a2de154bff6afcac42cad46a2cbe16fc5`  
		Last Modified: Tue, 24 Feb 2026 18:42:08 GMT  
		Size: 45.7 MB (45653048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e2692d078b62360ce66efa48798cce1ada6ffaf0e61c3560fb4e15c2ba9d74`  
		Last Modified: Tue, 24 Feb 2026 20:04:20 GMT  
		Size: 24.9 MB (24920360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8db3c1b402fe118464c0a88a37b181abe079a26f80fe8b864eebac8ab3097370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4135114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c7a934ace96a9f2ac081b048ae570e34acc8193ab4186589d985ca288f4f14`

```dockerfile
```

-	Layers:
	-	`sha256:5a51e874ebc37b9f93233c040a8a53d65d20c2cc3044e05359d17f0fff1b6724`  
		Last Modified: Tue, 24 Feb 2026 20:04:20 GMT  
		Size: 4.1 MB (4128277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f78b35b631bf6b8ef395f600a251feba69a5b1ea83ff70f025c2840fe700678c`  
		Last Modified: Tue, 24 Feb 2026 20:04:20 GMT  
		Size: 6.8 KB (6837 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d5f0877e60198a4c48eac4124c795d73d26bc856ecc3750ca144b1180179f5b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75237474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:794d79dc97fbda743fabd83945f99d94c249a30570552927c1dec44ede74e205`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 19:24:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:dc3ce43fbcc581a6cb3e0909e03d7e31c0ff1d4d76469e15d6610d1403f2a7e0`  
		Last Modified: Tue, 24 Feb 2026 18:42:39 GMT  
		Size: 48.7 MB (48705026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa1e5eafe63e2070e8b626137e2f3ba642d42241f716e9259b73098475d4205`  
		Last Modified: Tue, 24 Feb 2026 19:24:42 GMT  
		Size: 26.5 MB (26532448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e89a0cae677ec7b3115bce30bc07a2e2224b559356ba546a58884a9ef325b58f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e1e91c9af9d340f5da29e3a7b07ff6b3e7f85cf2d5a6e1fae5a9fdbd79c7ba`

```dockerfile
```

-	Layers:
	-	`sha256:c3a34acd923b6fbeee7e08c00007b7b1cb5ed1dec1813859bbfc8819a8bef647`  
		Last Modified: Tue, 24 Feb 2026 19:24:41 GMT  
		Size: 4.1 MB (4136336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e844cc61d05193195042dcdc24344f0e06f46f7277b16e4015f93ae12e8ac67`  
		Last Modified: Tue, 24 Feb 2026 19:24:41 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:6fe36d0a56c8b657c488ab6dc52b91b9372c1085834cb4c03071de015e79a114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.5 MB (78507133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46068f08f629d7a1226e2db37346c948632dde379ece728e54675703ead56fcb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 19:24:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:143f133830d056570eb26009a5886b146c40a6e16bbee60113f54a6baa1643eb`  
		Last Modified: Tue, 24 Feb 2026 18:42:19 GMT  
		Size: 50.0 MB (50011968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9094d4208101e32ebf3f9d4d940d804f0a8bcef435b536316812340ebc9e6f8d`  
		Last Modified: Tue, 24 Feb 2026 19:24:54 GMT  
		Size: 28.5 MB (28495165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0bf121eec02bb157547a5f6bca30f1caec97ef1e16f58b60c09094f4fc917cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4130630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18c9e416ace438940dcabb76f3812795ac16ab47895c015afaba8f6102380017`

```dockerfile
```

-	Layers:
	-	`sha256:2d84407a38a185bf7ba9e01b5900bae9eb9b0b97bf991a57ae555dd1c790f9f5`  
		Last Modified: Tue, 24 Feb 2026 19:24:54 GMT  
		Size: 4.1 MB (4123879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df7001c933d7c3506ff178f3adf15199bc43308135da5053dd5c9f52396fb75b`  
		Last Modified: Tue, 24 Feb 2026 19:24:54 GMT  
		Size: 6.8 KB (6751 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ce728342f63f98879feb15fc1ff489b4b9b8c38ec991020b8911c455028d69b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83155720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42191009ad1771f513122370eec45538980134644c627fb7a0fb030c3b9d62c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 21:20:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f1e7241652efbb83270036a6221c3c25c51e9feb8307ee3c94f7e0d52832e1af`  
		Last Modified: Tue, 24 Feb 2026 18:42:31 GMT  
		Size: 53.6 MB (53641787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa31de94cb423730059f9604b4ef3f6954ef0ad086f5d48144efd62317b2c2e`  
		Last Modified: Tue, 24 Feb 2026 21:20:56 GMT  
		Size: 29.5 MB (29513933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8e416f7529f981ebd4b589eb065c0fda8a006af810df8e9107678d2323be0c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4137465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:990c15c58c7cc83b1e76609c75229889b352637f81f8e6278e97c0472388947f`

```dockerfile
```

-	Layers:
	-	`sha256:a56dbe4b184c0099498e40e5b379e19ff6537cdf8201acab5c161807d3ead181`  
		Last Modified: Tue, 24 Feb 2026 21:20:55 GMT  
		Size: 4.1 MB (4130660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eded74d17adcedb2f7a5e2d5bba897e9c67520d9679003348a0b2c76f64be5ce`  
		Last Modified: Tue, 24 Feb 2026 21:20:55 GMT  
		Size: 6.8 KB (6805 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8c9f5e1eefc334c59fe7f761f7f13c1c629774f2d53a8461971a1a66366bf8a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73688782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c054bc329c88818f7ccf803baa750a8f0a5d6034e011cd06a088a551c85605`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 19:07:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:db31b4401b1ad39bc8394e302320dc063e12e2c0464e6a8103701611daac2f3e`  
		Last Modified: Tue, 24 Feb 2026 18:43:31 GMT  
		Size: 46.9 MB (46914404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce7ea7a6a4533bb42137b98ae7cf7eb86a1fd6eefe9d713522264d613c05e62`  
		Last Modified: Tue, 24 Feb 2026 19:09:30 GMT  
		Size: 26.8 MB (26774378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:dba09edab51ecf05ef330cb57e5430224e717e5774746c04307b7551772fcf45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4125300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbbb78774c79582ebd46461c9cff37951f8221cafc898cc6f965dbc66491050d`

```dockerfile
```

-	Layers:
	-	`sha256:3c6072a8e713ffc10b3da24d41cf15be43824c4492bdb0d817dc4f20cb888453`  
		Last Modified: Tue, 24 Feb 2026 19:09:25 GMT  
		Size: 4.1 MB (4118495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c989c1f4cd0b907804c15c4841ad8c8eed6ab6f5e4393145e6a18a1bfeedf292`  
		Last Modified: Tue, 24 Feb 2026 19:09:24 GMT  
		Size: 6.8 KB (6805 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:da431ee75ff98f2276497d62620a13ba7393d7ae5f28b312aa15f1e59a04f8a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75453605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbbc4d851cbca8d9358761f181eafd285aaf3735a622f1d271e3de9abe3d74c0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 20:57:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f21354992e07f04a7de86938f41ff3c72cb8dc33252e2b2320b4169695270de1`  
		Last Modified: Tue, 24 Feb 2026 18:41:36 GMT  
		Size: 48.4 MB (48448352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81bc3d23a1ad94963e56617c5ddcf27c1a360185386d60459632a29eefc99c91`  
		Last Modified: Tue, 24 Feb 2026 20:58:20 GMT  
		Size: 27.0 MB (27005253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cb4e89aacfc1285e19664c99a7624684e2608a4fdee1bafb27d7abc30916e737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4134963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e87a4ddc001799a81a6ffb52bb3e8f233939ba3ee77b5f36d912933b9a9ff6`

```dockerfile
```

-	Layers:
	-	`sha256:8e429e8614aceb56fccb4259f0c93be7d65eed2738d7cedf4ba22b1f89cac8af`  
		Last Modified: Tue, 24 Feb 2026 20:58:19 GMT  
		Size: 4.1 MB (4128190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:667e37bbd35f3ddba5c875e6faf2861ffdd901a60126fc43649d3d5d71aa2672`  
		Last Modified: Tue, 24 Feb 2026 20:58:19 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.in-toto+json
