## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:31e37d64beae8ea73de7c1be361fd1b23e61ffc19a8938427281d1c6b34e57c4
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

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:5270c29f5b0cbb79b43542c490b479767f75dd9bdfefc97ecd4b0ba05f253922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48502270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:897b5e4e2badf65bce685660c5a9ddfa9b5d572f4277fa84bf02070128c2bcbb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'oldstable' '@1781049600'
# Thu, 11 Jun 2026 00:15:58 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:9347f484150dbe9983a6bd278db05accfaead3a8dbfb600e0a4db46731c78140`  
		Last Modified: Wed, 10 Jun 2026 23:41:06 GMT  
		Size: 48.5 MB (48502046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b25289af95f91dd1426f833b35b2904291ae2a8ac4f34a4a3ce273ffa45634`  
		Last Modified: Thu, 11 Jun 2026 00:16:04 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4cb4f590eb6c46a4faa3a09c61d991309167eab6eac1ab5e4d87f7072057eb8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e03434dc4546db5646ae9e04918f61a1351b28b5619368b45084eca6e96521d`

```dockerfile
```

-	Layers:
	-	`sha256:d2044882aec473f39ddff24506346ae634fbaf8357601e44e97a5d286c4de081`  
		Last Modified: Thu, 11 Jun 2026 00:16:05 GMT  
		Size: 3.7 MB (3734112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85d82cd0b4d669bccd572466e8696e22ae2b4d0074fb3433e6d1a47ee27316ea`  
		Last Modified: Thu, 11 Jun 2026 00:16:04 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:4e1ea93b50064f9a762251e739ed7f54f1140a77bae8e90c5a92ae63243e0ef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46038412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79dcb5785c9bcc3c9fb66c8e4c01e736f9a5c577e43b7f8b04cfc3cfca9f1e89`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'oldstable' '@1781049600'
# Thu, 11 Jun 2026 00:15:55 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d20f32b72a79ca7537e089f596bb93bd2af59e258b733e002eeb6f290736cedd`  
		Last Modified: Wed, 10 Jun 2026 23:38:44 GMT  
		Size: 46.0 MB (46038188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a108437b808fb9334f6e05c3a74b90de8f631681ad5b72f3ccd12d8c65f5d020`  
		Last Modified: Thu, 11 Jun 2026 00:16:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1323161382c5b9269054326cd6ec3d01d2879b5b9b2053b777deb9392b48668f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8776bc0ee3f57b3039b9a5d2e37302ad582d5a0dd2226031ed725a9fa6cd1caf`

```dockerfile
```

-	Layers:
	-	`sha256:75de918a12bc740b96bce82ff9b9cc35ddaab3b3142b74e31e0d32aa3df11613`  
		Last Modified: Thu, 11 Jun 2026 00:16:02 GMT  
		Size: 3.7 MB (3734313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50298948f919b6be5db8b717ce22b3a79d7a6ce90c145be72b8e20f793506986`  
		Last Modified: Thu, 11 Jun 2026 00:16:01 GMT  
		Size: 5.9 KB (5866 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:07f2b235d64ae12b7a27e5f7caffa8c138efc64451e27720ed5568723333d860
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44208294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3907c6179ebc668e18ff203a66236ce48a3ed7e608bcb55f152ccc8a171a22`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'oldstable' '@1781049600'
# Thu, 11 Jun 2026 00:15:13 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2b9657dbecb6b81567b11fccd5c44ea0616abfb91e7d77a9d0b86e0713b75c8f`  
		Last Modified: Wed, 10 Jun 2026 23:42:28 GMT  
		Size: 44.2 MB (44208069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06a9c18ff78e1b838fea6a41e2f304513f0666e5d207d3451058c8949b6d48f`  
		Last Modified: Thu, 11 Jun 2026 00:15:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:50a8ba7953f503d2011d214a326ea022a5b1fc359a2480b6ae5a749e97509239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3742157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a7ae2c4b3e85e1efdd3ef28a8cd1fa99d80d7885b256e812a6d3018d014e190`

```dockerfile
```

-	Layers:
	-	`sha256:7f4058d5eba88f24c00cf48b414e0b48facd148b17729be1ebb25dc644e3c47d`  
		Last Modified: Thu, 11 Jun 2026 00:15:19 GMT  
		Size: 3.7 MB (3736291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:065bbda002fffa732a5be6ad4b6331831d3b2acc0d45669e4f1465212683e863`  
		Last Modified: Thu, 11 Jun 2026 00:15:19 GMT  
		Size: 5.9 KB (5866 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:fa6ce5d1b71332c2ab94ddcff6157e5fd69fa24a5b5458f5eac76842ee721518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48389242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00656639147e3330b45ac14cbd3ad342949eedccfeae7ee770ac865cf37546d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'oldstable' '@1781049600'
# Thu, 11 Jun 2026 00:15:35 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:235e533a58c20e6b7b493f127e93c241fbaf901f4b0b284c17c677b6d10efe2c`  
		Last Modified: Wed, 10 Jun 2026 23:39:45 GMT  
		Size: 48.4 MB (48389019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d38fe9bb7357be7df699cb56ed9315a9c4197135cb0b8ac4263d7574c9553fb`  
		Last Modified: Thu, 11 Jun 2026 00:15:42 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:11fcf180843674e006fa2d3f172b698f781c0f385c04ed2d8f66b7e8d87f6ad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf6599e6e23fec52c9067b1f6636006bceddef9f8c2e9387c974b42c192dccf`

```dockerfile
```

-	Layers:
	-	`sha256:5ab86e3603b64249a01434f3a4dcd547e926ed55f17ea0e762ae93a90a17b340`  
		Last Modified: Thu, 11 Jun 2026 00:15:42 GMT  
		Size: 3.7 MB (3734327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48ac08b913b3d0038a2ddc59fdc9d17042c1d98ddd96bde88243efc933b8af97`  
		Last Modified: Thu, 11 Jun 2026 00:15:42 GMT  
		Size: 5.9 KB (5878 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:dcc75aa6a6e6cb01fed3a5fe7d97730227224a467fbe3f14b0527cb1ab5d5d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49491433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6c1b70f359a3415c5d5d2cb18342225fd3ea99126a6bd047483399330c9d250`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'oldstable' '@1781049600'
# Thu, 11 Jun 2026 00:15:56 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e92b0214a7b727547f7c604fc3bb5c2bb1cb742a4d389c221579fa0a4a7d2974`  
		Last Modified: Wed, 10 Jun 2026 23:40:37 GMT  
		Size: 49.5 MB (49491210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc442888c0d389bcc011654f4510a40924af3be524e0511e1a7da01b6f0fb1e`  
		Last Modified: Thu, 11 Jun 2026 00:16:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:0903c2889dfdb1efe0568026c611e7e1ab6eb9a7c93c50f5e759225e41ed1c26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cefb9b2e4b162147aa85d580586a21f2779c85fff52a73c929ef7f5604dcebd2`

```dockerfile
```

-	Layers:
	-	`sha256:5bf8535a4db61b453f4cbf437aa40b172573e8504a4ff2ae6cbecd364312df11`  
		Last Modified: Thu, 11 Jun 2026 00:16:03 GMT  
		Size: 3.7 MB (3731308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4735aed7ce518a340e737d90f87c8f72ae68bca6503d1809da3be56b28310314`  
		Last Modified: Thu, 11 Jun 2026 00:16:03 GMT  
		Size: 5.8 KB (5792 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:4d8ef44bcd20715e2be4ca9647bb875cdb52a4431fdf10a31da3d42b86e8cce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48792934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d890be016eb511dd72a948e6c2b520c1704cae05b37c00b80dbe2c71ecf02f3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'oldstable' '@1781049600'
# Thu, 11 Jun 2026 00:16:26 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c719015f034521740cd5df6c00b1b1017ef7d6d499b2558ca3cd559c3da4ad1b`  
		Last Modified: Wed, 10 Jun 2026 23:40:57 GMT  
		Size: 48.8 MB (48792710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35875400f56d9637545c2d41879e13e52eb2e9e6a39f0701b2b83e2b36413b3`  
		Last Modified: Thu, 11 Jun 2026 00:16:57 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1beb6ddb4910f7026f237e6f1f1a44ce10cdee00a36851e756d815dbfec60f46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 KB (5634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f368beb8c3f4ab10d5ccdc37e7b013d1d6a5d44ab39d67faf1c57854903ec087`

```dockerfile
```

-	Layers:
	-	`sha256:c88afc40493d087a106abdc6330feff29532f49aa869a3dd7d6bc490dffef060`  
		Last Modified: Thu, 11 Jun 2026 00:16:57 GMT  
		Size: 5.6 KB (5634 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:c905e733ab63f1185ddae0827a17c97e44b4670a6079a734e52240ad3a064c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52340431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ec3c7c8c9a113cd4daa9743c6a45a65619afb1bdd6257bbc3647f9b9937ff7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'oldstable' '@1779062400'
# Tue, 19 May 2026 22:56:03 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:965e5732b0fc2b11c43946e18092bb1263fe840327cf5e5dc6ce639276a5acb8`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 52.3 MB (52340209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96fbe54a81134e8ffa4d2024fac1342267d660b98712e11cd30a828c7044991`  
		Last Modified: Tue, 19 May 2026 22:56:14 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:859530b39225d58309aa42901a77f7a8389b5d494f9f9bf2cb044f700ae75870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3744288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c22eb2e9091b82b039d790561dd8e05901fdd7a7cce1ba25759bb9bec1c612fa`

```dockerfile
```

-	Layers:
	-	`sha256:28a0c9b47cdaf097ce7a29eb7b33e91bb2777410cdce25e1963e7dfa370c09b5`  
		Last Modified: Tue, 19 May 2026 22:56:15 GMT  
		Size: 3.7 MB (3738452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:933937742e2e858750397f304d4abfee4a3d4294f9f1f6f6ed3473562f4f8516`  
		Last Modified: Tue, 19 May 2026 22:56:15 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:fa2879238f700224b9119aa546eb4b8daddb40e34592fed909a3f4baf2a663b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47161726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2ce4f56f4227ca9cd9ea726666eb7f1676d8ae2a8f677443d6f7702dfd7f82`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'oldstable' '@1781049600'
# Thu, 11 Jun 2026 00:14:49 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e7015b2004af20c3bf4afd76b9c4ab29a6dba6434a632fa123682ce27c695e85`  
		Last Modified: Wed, 10 Jun 2026 23:41:33 GMT  
		Size: 47.2 MB (47161503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9197adb7efc5bfe2099398a05b44fa5f55b281c6becb39b34e53c544333be870`  
		Last Modified: Thu, 11 Jun 2026 00:15:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c214800156a61aee1d501612b1b076ce6d9136216d4356ce792a9f237882a321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5e2aa0ca0f301cb2267bea9d8210964f4c4e35293a56b86c31ffa3acdff6809`

```dockerfile
```

-	Layers:
	-	`sha256:21b65f3467d1607c3018b42564c275f27e2adb4a2d42a5f777fd05a2b4fd3f5d`  
		Last Modified: Thu, 11 Jun 2026 00:15:01 GMT  
		Size: 3.7 MB (3730950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41ebedfbcc99c1cd5196246f6ec6994d48fd8d0d6476636ae7a8b6013e7b0172`  
		Last Modified: Thu, 11 Jun 2026 00:15:01 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json
