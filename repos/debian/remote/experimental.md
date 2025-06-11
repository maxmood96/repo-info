## `debian:experimental`

```console
$ docker pull debian@sha256:b05718524874156a93abec7adb4ff4d7fd2ad2474013864b51fc0969eeff01db
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

### `debian:experimental` - linux; amd64

```console
$ docker pull debian@sha256:bb8e2851ce0391e4f7dd293e2cef49194b6dad8d83ef513509e8b3e34da2f9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49263545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51e2e73c4c41364c095db0914d8c4dedeb1a150236cf1930938e72d9d10b881e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'unstable' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:93fddcb908571811e3e13798129542e070826b8fa807722501c0632f40b7a77b`  
		Last Modified: Tue, 10 Jun 2025 23:26:02 GMT  
		Size: 49.3 MB (49263323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c892b2072ec578be31bae9f4551551469b915f3cb48aa2ba51aca06535533d6`  
		Last Modified: Tue, 10 Jun 2025 23:26:32 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:be783e883d826ae570397b6a1a7fdbeb9aacf70fd53ac7fec8863f3a7d415f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3174303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a644388f1c9f1552951eb993e5f48056c831375f07afb3f38153d6ab199ba066`

```dockerfile
```

-	Layers:
	-	`sha256:1f705ea3a6b21fa9fbdd7cba1183928822ff26c3ed4bd630922964e615d26a35`  
		Last Modified: Wed, 11 Jun 2025 00:25:22 GMT  
		Size: 3.2 MB (3168160 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dda7b6501093ce84e9dba17c6ff836a58b6cd4205d84def4a907fafe922ba0f`  
		Last Modified: Wed, 11 Jun 2025 00:25:23 GMT  
		Size: 6.1 KB (6143 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; arm variant v5

```console
$ docker pull debian@sha256:af02310977d84e3d8bb3540b1892ccb26f96b391679a09336a58fed94fb3a342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47435433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9b55ab34a79dfd36994f594afd42b6866f152ae653eeb1ae2abcd082f0e6b9c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'unstable' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:35b26be3db2c2b859092b762dff59c72b0c03d2bae1e82038859c9d965bd5c30`  
		Last Modified: Tue, 10 Jun 2025 22:51:26 GMT  
		Size: 47.4 MB (47435211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825120a575d1d5f560dc64e23ddd3431a76c77fd2f4ed39e0c01d931b8f3c0a8`  
		Last Modified: Tue, 10 Jun 2025 23:32:48 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:26d92ed7ca9adfee885f2044e62acb1bbb767d192b910d0ad8217dd5d6e01dc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3186562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80c50cc4690a71c5d94feffc7315001316af5bb0b2f24ef1a9e8f33aef0c28f`

```dockerfile
```

-	Layers:
	-	`sha256:73437a748cd9f9526fb6743d143278cba534d5e0ab9c969f287be073098df914`  
		Last Modified: Wed, 11 Jun 2025 00:25:27 GMT  
		Size: 3.2 MB (3180358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:143b8b6ebb8d5b67524a9a6e258ba95eec6363dcab72b7d5e0c792f6b06e2b97`  
		Last Modified: Wed, 11 Jun 2025 00:25:28 GMT  
		Size: 6.2 KB (6204 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:ca7a607209300c16a803b5c4a4a80a526f9c8f2d7e12e29ada0d5e6905826502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45708056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82154c3ade9ce4b010c3df2c6c1dac342ceb1b2ab85963f704eeca4c0f911a2b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'unstable' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:43e19f2584553796b1082d3a93ff71a29e6edd1d41b88cc17a96748bc227e74c`  
		Last Modified: Tue, 10 Jun 2025 22:53:05 GMT  
		Size: 45.7 MB (45707834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb596175fcb8b7a86b9e8a2e35fc1a9f7dcabb17c717b4b0112664d44b6e6646`  
		Last Modified: Tue, 10 Jun 2025 23:27:24 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:09833d62de0dbc460d63367a2d4b5b7cae8736c21bd3a5a4c4eaf85ebe32d36d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ce0a169d7fd7b90dcf6e3d06ccdf04d9fba5bb39d3abb761a9834bf62ff3f2`

```dockerfile
```

-	Layers:
	-	`sha256:985c5a0ad7c63177d49771973c0a16ed80206787fde9dd6ec1fb60cafd280bf4`  
		Last Modified: Wed, 11 Jun 2025 00:25:33 GMT  
		Size: 3.2 MB (3169542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11f141f6f4fe99bb2e0d7ed2de68620d3fe0eee97f06335231e4551e4b240444`  
		Last Modified: Wed, 11 Jun 2025 00:25:34 GMT  
		Size: 6.2 KB (6204 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:3129d5eb611537bf7fbdacccd3dbbe03570b1c71c1a46039448b2d419c10c6eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49629578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a204b4a786665aa20b05aff4e7ba121cdef95b6613814c6af4ebb7f094dcdcba`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'unstable' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:10b0d0cff4fea39bbea30e56a31680d59b2c50b23f946d73a6443cc57dfdbeae`  
		Last Modified: Wed, 11 Jun 2025 00:33:32 GMT  
		Size: 49.6 MB (49629357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b8c392852ce2a83856059c63abec336de5ba383bbd952e548a70ca18467bde`  
		Last Modified: Tue, 10 Jun 2025 23:26:03 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:ec4b9548ddde88f31fa6c207bfa76efe9d9d54204b1080d6180c63d8e95667fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce66473f6fe098f18dacbcaa08596421cb612d4ada7878b329eb41f96b9ec1b`

```dockerfile
```

-	Layers:
	-	`sha256:c82f5902da6a04bb7b268d00b597ceb642f2fd32116a2999f580b743fbfbbc65`  
		Last Modified: Wed, 11 Jun 2025 00:25:38 GMT  
		Size: 3.2 MB (3169653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:806b857541173310f2bf7e7881c711f202edd5ba0b40e9a1ddacd465ea881bf8`  
		Last Modified: Wed, 11 Jun 2025 00:25:39 GMT  
		Size: 6.2 KB (6224 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:de203a7e6a5899d2210fb40ca57eddcd9030c99eb7cef77e098ae65788e42afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50786244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a114ce5f7b9b94f3ea47afba6e8cc83bf11d0ee750fee45abe636e6850fe077`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'unstable' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:f395920f2feadf08d83feacf633e28ec2d6794555dff77f51e2c5a372b240daa`  
		Last Modified: Tue, 10 Jun 2025 23:26:11 GMT  
		Size: 50.8 MB (50786023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce849b3fc377ca771a0db8f60dd52a44b1f258abeb51a030268dc409bb9180a`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:f0006650ff35b0c5e3c5c1e2f018fd0c4dc6a71642ce6f0f72392c3ceac1a82a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3171479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc9d0475c1d011504877d811937d7b50d4ed9b7c59293b2b9c7c7ca8cfed38b`

```dockerfile
```

-	Layers:
	-	`sha256:6d2f4c0d63d5e0f13871cadd7ae82e83cf5fea0342167750301dc2fb2d3c9900`  
		Last Modified: Wed, 11 Jun 2025 00:25:44 GMT  
		Size: 3.2 MB (3165359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af3502512456d8913be3133a1d55b0a39033e139a4b0533b3656d63e43eb6a9b`  
		Last Modified: Wed, 11 Jun 2025 00:25:45 GMT  
		Size: 6.1 KB (6120 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; mips64le

```console
$ docker pull debian@sha256:b03249fb978ba423503cb7a49f467cdbb18b8dcd75433eb92ea71769d89fc2e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49553486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3daa5f7a71eb5fe1de38e11ded753b9efd36dae5cc320fac5de8e67841feb561`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'unstable' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:5934995d4f2735a68258a3b1204efe81100bc4e5be1d6a7c4dbbdbddc6c9b063`  
		Last Modified: Tue, 10 Jun 2025 22:51:13 GMT  
		Size: 49.6 MB (49553263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0404f02769dfdbdfae458d0b1cbdeb87926598807886d57523232483cd3375b9`  
		Last Modified: Tue, 10 Jun 2025 23:28:04 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:9584fc39c9b0964e359137ac252e4ee41b61163a6198f4bcbd935dcd49b970c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 KB (5977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13526a000e7de9a3fc22fdccfca654b77b56d3ebb59c035301f1811ff7eb690d`

```dockerfile
```

-	Layers:
	-	`sha256:f7ba9a772dcc5284210c932a11826644ff093318f1ef5f40f74237271f3aaef9`  
		Last Modified: Wed, 11 Jun 2025 00:25:49 GMT  
		Size: 6.0 KB (5977 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:acb4cddeebe5c130eaa41856524a1e87ba55e47d5bb2a05a6b04ef67d4a9ba71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53098906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd73d3eb8952a780eeb03258a2426fc5c3aaab30d69364bc7206fc570812ffb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'unstable' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:6e80ff87602d2788805e043201504661a095a93045c363ba07d56c6061b8d555`  
		Last Modified: Tue, 10 Jun 2025 22:54:08 GMT  
		Size: 53.1 MB (53098685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee614029d6456bbb6a28c247d01d09729c6f0340f8bb9fb6cdf453253911a050`  
		Last Modified: Tue, 10 Jun 2025 23:27:12 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:1c0afa3968dee09ab4dedb8a2c693ce3a6f6615741b573de79a2378496954a48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3187103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28e2c42b1606d9c36f0416f6b98c94afa283fb1ac7ccfe3c1a55062fde9e822`

```dockerfile
```

-	Layers:
	-	`sha256:9bd1d830814d647b15c7f32a81bb4bc7e116aaef8b7c811e2410d1975a3910fc`  
		Last Modified: Wed, 11 Jun 2025 00:25:53 GMT  
		Size: 3.2 MB (3180928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aed14547d7c7cb40892a621d6829b20277bf456ac61ea77e8908dbae9aa1191a`  
		Last Modified: Wed, 11 Jun 2025 00:25:54 GMT  
		Size: 6.2 KB (6175 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; riscv64

```console
$ docker pull debian@sha256:1b42171a6789b796ffa577b5dead739e02764bfe9c496e47c7ecb6aaa890c570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47749898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5be6821056931921b105b9277b22ec2018238a80e388423ec0c7fc58bb372cb9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'unstable' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:fd47043b8ec6f8ac006ddb64b2a5cc6c36d784232da83adb78d7e72747b0def4`  
		Last Modified: Tue, 10 Jun 2025 22:59:47 GMT  
		Size: 47.7 MB (47749677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5003249f8d468761014537f796504664d79a710df0d217fa948eb77792a6d51`  
		Last Modified: Tue, 10 Jun 2025 23:32:41 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:fca8a3d438d8b02e45fc3ca1a6a05dc9caa81f2f2bdf93ce9477afc91adabea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3166663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8b7c237fb8538251117932f08e6e453fb29f018ef779db5f788530f1682089c`

```dockerfile
```

-	Layers:
	-	`sha256:b661186378c4220d6ebbd2582875c0a99fc238be6d8af0616f85a565e561d50b`  
		Last Modified: Wed, 11 Jun 2025 00:25:59 GMT  
		Size: 3.2 MB (3160487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d599d629a2538e9e9c7ed562636e1e79d17da6b784ed69e845ffba411b04d39d`  
		Last Modified: Wed, 11 Jun 2025 00:26:00 GMT  
		Size: 6.2 KB (6176 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:c82ca2a3481823f17468020345a74a933517e67679ff02a24c6c846be188ee7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49343316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b8344363ad8c8575998e106828430a04770143179146c4ca6a983511519fdc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'unstable' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:c7c19a920f1caedd77d21398a6deca2f9dcefc268d7ef30e8e62edf9661b00bc`  
		Last Modified: Tue, 10 Jun 2025 22:54:01 GMT  
		Size: 49.3 MB (49343093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632b39e9d330db4bcc4a5c0306df856cd22bde9717f9c58b284e6bf28b64d021`  
		Last Modified: Tue, 10 Jun 2025 23:33:08 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:c02c7825610c9700cb2196779f3b49567e13ecaca3984c01dc84628cf280d047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3185004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe074d8f2eae226d0214b7520e39b132b7eb420d3eadce01254d60e0453bc9e6`

```dockerfile
```

-	Layers:
	-	`sha256:f993d5d7a5ac95aefcdfbbb3a209a43fe063b58b7bdc028b5f35c4b2ee1eaab2`  
		Last Modified: Wed, 11 Jun 2025 00:26:04 GMT  
		Size: 3.2 MB (3178860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccd216f7cf8492b0f6587b8ea5bff4b6cccc8f1f52bf04e6d98cb353f43297be`  
		Last Modified: Wed, 11 Jun 2025 00:26:05 GMT  
		Size: 6.1 KB (6144 bytes)  
		MIME: application/vnd.in-toto+json
