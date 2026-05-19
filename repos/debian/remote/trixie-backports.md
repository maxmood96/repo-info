## `debian:trixie-backports`

```console
$ docker pull debian@sha256:139c105ecce7ce1d7d586ded3f6be8bcbe1a0d1ce54c67b7bb9dda5d94ed3edf
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
$ docker pull debian@sha256:2a34daebc82e9209c8a3f5927b69525a95d9d465a490394cdcb042162bc66a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49310848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abca1888d442e9767bc50dce3909f6c12425d3986b24dd8e13cc5f2d97f58c71`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:58:31 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2e21d88bd18b970bd4a90cd15e68362f29ca4fecf4abca6a1975989e4ede9e0`  
		Last Modified: Tue, 19 May 2026 22:58:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8404bb6076b3a58d22935ccdeb16baf69ee25c3a8155f815117a742c848dbd85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3176739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f28fa44aa7a654af12a558e171ddf7f3e4fe222cc249d353517bc6ba0ed17c6`

```dockerfile
```

-	Layers:
	-	`sha256:bfc96292d6d3390b79529700be23d9af78220bcfe51c6e172fc2bd338d194ccb`  
		Last Modified: Tue, 19 May 2026 22:58:38 GMT  
		Size: 3.2 MB (3170955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23b72a186e4e2ebbe7f3cd1b0adeddd9acc9ade96f8bc0b4a14ae572271c72d8`  
		Last Modified: Tue, 19 May 2026 22:58:38 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:dab2fdec0461ba742c81074a1d2576eccefaf766a2a86bbe35309562493c2ffc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47488270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0886a42656ad5fdf5c502e8432aed80e28f325e385760df5c023bd3bbc822d4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:57:30 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6cf4508cae9439867ef520e234c0d389bafbf206c9c5e0966546716701d698c7`  
		Last Modified: Tue, 19 May 2026 22:36:48 GMT  
		Size: 47.5 MB (47488046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104f05f516f41e4cfb2c86ddf7f15a8fabe9d19a4e7e2fe717d2c16b5dfa11bd`  
		Last Modified: Tue, 19 May 2026 22:57:36 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ce1df8bcc35267afd0d857c2355ee64c3cb7b886cf07989823b9de77e357ea1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6271e146f1c97428132d1de93c86ea30c62c325d8620f3361b0072f61663cfa2`

```dockerfile
```

-	Layers:
	-	`sha256:100bde38472008198bb8cfe4ae5117fabf3ccd300cbe9f7c3b0f5f6d731f493c`  
		Last Modified: Tue, 19 May 2026 22:57:37 GMT  
		Size: 3.2 MB (3173892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c266bc659d1406d6e520520d8aa68ae7c7e99ad672817f28eb6724b071cffff4`  
		Last Modified: Tue, 19 May 2026 22:57:36 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:035d7c9326449eb6c1b80f9ef0894eeb0003832aa0f760e9ba93b13744edd7b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45742255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6a0abbe3ede4f52d82bcd6f71167dc26cdb7e17dc3346b44c404ab17b4e3884`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:57:23 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:16329e57da118ecb493828b7b07e7a4228b11fef4bc65ec0fa8d7fc9fac39b62`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 45.7 MB (45742031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ee6f6369af775aef6bc400f8f3acd5c6003b650994c9ec3375057df9b48769`  
		Last Modified: Tue, 19 May 2026 22:57:29 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1c2720bf7a8e45029ca06f6e30c551f72051e286e67b4650f136a2ef698c8211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bab6bc7eec39a4d40a19883f8c926b242b6d41ebec635ea613a13f736dd9e3c`

```dockerfile
```

-	Layers:
	-	`sha256:6b1a04ae2c4a1106742ac7ef5d3a64ba1df15f34940093bc77896fd7aee72d22`  
		Last Modified: Tue, 19 May 2026 22:57:29 GMT  
		Size: 3.2 MB (3172329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92a83036c45330c3df8bb85a0aeddefee0be0e762f1d0a39c09a60f66630f7cb`  
		Last Modified: Tue, 19 May 2026 22:57:29 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:11308f16d485f599cd235641cc4f77d75f49007602f73960f5c1f068a036de2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49672445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2942a0fd62e632a49d2c5389974620257f54124f14efac6867949037f821435`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:55:43 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a83c25c60f37aa72cbdc20c38496817a10269a775c8d342bfcd47473e015cf0`  
		Last Modified: Tue, 19 May 2026 22:55:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:56a75e8db687ba484f3db0f8c6abbdd268e751a8935005b7bb91e984a0a7c68f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545e2272a392fa1d2958038d625b645de0aeeb1f17dbea1bd431898261222bc2`

```dockerfile
```

-	Layers:
	-	`sha256:c697631cdb8f98056467ff881e5ca51e9339a41cd6de3dd7c634c94e81fe77e5`  
		Last Modified: Tue, 19 May 2026 22:55:50 GMT  
		Size: 3.2 MB (3171799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d396cefd67f13d57a2f3d1e2ae250481b1b3285579da5ae5f32b97a0ef3dbc92`  
		Last Modified: Tue, 19 May 2026 22:55:50 GMT  
		Size: 5.9 KB (5851 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:8900048524199a51b931696ef3e11270ca8c6345764774c26acb25ad87a29590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50829778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8078ee971a35aa362ba41f232f4650362464ce9a751bef14a345b76636271bf2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:57:10 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:702490bb2e15df54351c309dd60c88b6e99c780b0fc6b105f387ef3f216f1ea3`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 50.8 MB (50829554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8e107fff90c9e6d212d215bb4491616eb3788ec0637981a39704fe2f47c449`  
		Last Modified: Tue, 19 May 2026 22:57:16 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:02f3be72fcf25499194573f4f69fd34eeb6743d60014b69e58139c2385d3e7ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3173924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f599d6fc6f298104765d6faea7dcb8df5bb85c2f45ef216cd1cf222b4fb9e8`

```dockerfile
```

-	Layers:
	-	`sha256:7a664625d19148a46215a61f01872e326d163930b783d4ac054ed272c44d9ad2`  
		Last Modified: Tue, 19 May 2026 22:57:16 GMT  
		Size: 3.2 MB (3168157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3395803bafe866ab67d7096eaee7d46e47c1d752b7a1c139450726a51ef6740`  
		Last Modified: Tue, 19 May 2026 22:57:16 GMT  
		Size: 5.8 KB (5767 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:2535b3816fb65acb78b0fe1bf8100ccb212f512b4fd6e639d63e6ba46043d885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53132406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:269623484eabe6a5ed625462965338c3de713bd3f559223c2ac8f4d27b677316`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:56:41 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:55497c62a793e62a2e78a3fd85fcedf060da73e331ad107733199ea991106b96`  
		Last Modified: Tue, 19 May 2026 22:37:59 GMT  
		Size: 53.1 MB (53132182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30bb4511492aa27af293278ca3ea85d114dc4dd3e7967e3e116cb43c00a9382a`  
		Last Modified: Tue, 19 May 2026 22:56:51 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6a77be1f77ef242dfd369a2315c4101e2d41beac11de2f897061414cb944a0c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3180278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e625c10fea75225842a69e0e51c04686b842e9d252ab143aed816fb7df6f309b`

```dockerfile
```

-	Layers:
	-	`sha256:221cf38c3f7cda369e59c10b368f46f31231fc8a7a3ee1933ed53f0353d36217`  
		Last Modified: Tue, 19 May 2026 22:56:51 GMT  
		Size: 3.2 MB (3174468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3657bf38f927cc100e4e50411e8d0108dd051eeec92c73131da2792ad4ad2c5`  
		Last Modified: Tue, 19 May 2026 22:56:51 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; riscv64

```console
$ docker pull debian@sha256:3d6b5718395f6bd6ec15eaa7ac4bc89f6c7f32099167ba12a7745ec18bc69bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47798616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979bc5d6dbdd1d727bde5cb776ca573dbdbfef935f6a4348306e4719060b236a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 13:55:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:16def90c932096937daf06d99b8e59a8b74b84aeebf2940aac17817b2f543a80`  
		Last Modified: Fri, 08 May 2026 20:37:07 GMT  
		Size: 47.8 MB (47798394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381e1646c2e4cbae5277f28e430c7a9542d34d639f95bcf8a77ac2b27f7be13a`  
		Last Modified: Sat, 09 May 2026 13:55:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4ba900d8847ccfa0552e7c955e2de18a688fc62bd5197ef8d624e02b9f8ad6eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3169048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5052578fba7fd48588d4369aa43fd43b9d57d2ad5e3305c43bb5c93888a13b07`

```dockerfile
```

-	Layers:
	-	`sha256:1ec35c4ba706a68adb29de2963141694aca9c53994efe6dee47ae02d91c680bc`  
		Last Modified: Sat, 09 May 2026 13:55:55 GMT  
		Size: 3.2 MB (3163238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06cab8f2b3c077beccc295b04f3297fe61264bf5eee3c1158202b91b9d3c5522`  
		Last Modified: Sat, 09 May 2026 13:55:55 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:0ca0077cc2ada51249e3b066dfc26a30f5df0caf60e3b267ac3a60d74d48f932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49380004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:792f635bbbca447ad05c5098e5e1df76ea1cb02265bc8e3d17fe6d0b9a30b97a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 22:56:37 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1540dbb0587ae9097c9d04c50809503aa74d42814940d640c6659645acc0bc6c`  
		Last Modified: Tue, 19 May 2026 22:37:00 GMT  
		Size: 49.4 MB (49379780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba25a01940d1cb84ef211537a043436506602dd15a4719c400a836ac0387dd17`  
		Last Modified: Tue, 19 May 2026 22:56:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6cb1929abc2658b07e0932acf68ca94d499079207d5b1127aadb7aabb9cc1441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:521f19cf72dce7ba48e26fa87358d57e40e8d893d19c4b92f40eb3d006257975`

```dockerfile
```

-	Layers:
	-	`sha256:c7464d5ce62a0147997b12537e72e8055eea18d6de8cd5762c5c4335650f717d`  
		Last Modified: Tue, 19 May 2026 22:56:48 GMT  
		Size: 3.2 MB (3172402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1734da734ba5b2fb9fce8324dbfc63efa01a1d8206596d19b0bb97d82f2fc98b`  
		Last Modified: Tue, 19 May 2026 22:56:48 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json
