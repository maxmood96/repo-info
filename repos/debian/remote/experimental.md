## `debian:experimental`

```console
$ docker pull debian@sha256:6b31f1f54f322ce8f2b3135335d7290c97569af1ef8ece0de5b3de6e0c1f58c5
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
$ docker pull debian@sha256:f484aa1cf17b0b3bf522b1a7e5b96e2fdb315f8e1ed92bb9157bfa2d31ce1ed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52225627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f27b04b4840eeac859cd0a1292a7e81ccafcdba66ba785ff6882342b2ac68ee3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'unstable' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:8fbe4db86a41d84c034c0b7375e5f3bb45da516a36d906447b8f099df6f1c111`  
		Last Modified: Tue, 24 Dec 2024 21:32:35 GMT  
		Size: 52.2 MB (52225409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc4f4b299683997f85e127113ac48022eedbcdff2cb9ebe85d8ef85ecab9fb8`  
		Last Modified: Tue, 24 Dec 2024 22:14:09 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:a5a3d48afd0b83725cb8f61a5c7297636ea868f0005bdf5fbd7ed682e237ae82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3236549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b4f6e2daade180da869c5f6f47701e589eb62fae86bf69b1a3fc76cbcf1cea`

```dockerfile
```

-	Layers:
	-	`sha256:957ad3331e14cdeb6ef228d0ed06eee925a2b9fb80b5f1c17e1162edea30b427`  
		Last Modified: Tue, 24 Dec 2024 22:14:09 GMT  
		Size: 3.2 MB (3230405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:658b2e668b95e5b9e70fd5a1556320909048e9aa171581b6ccfcfe116a9dbfe2`  
		Last Modified: Tue, 24 Dec 2024 22:14:09 GMT  
		Size: 6.1 KB (6144 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; arm variant v5

```console
$ docker pull debian@sha256:ef3d9d7c1b04702037a7de9ea0e086630dff5a500d3e1ac887fcb0ee3f332dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48772126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ee3240d7e3115a9e45f5edd25972a940d7fb4547ea29764cb3258a1748a8dfe`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'unstable' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:3762ab95f7021ba34c1175027467ded65353f2c6419dc7eae90ec043e56cf68c`  
		Size: 48.8 MB (48771907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4534ff5aaa5ae37e9b6fec4a3575f25b4c94936b69af0e7d9743b8a1e91c31`  
		Last Modified: Tue, 24 Dec 2024 22:21:55 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:96c93c3fc276b4c4792e19cb18159d6126d6817dacb6a8e34db92dc887139977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3239436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ba23b93f91aa16003829e089d3efb524c6e35b166e1c82d839af0433e77f804`

```dockerfile
```

-	Layers:
	-	`sha256:ea7c1fadeeddbf2c97c81af6e2a16a647ab1584befc7335e8d6a7fc95237e121`  
		Size: 3.2 MB (3233232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f23d12d9d66158a74c2fd49adb11ed27a22022fbae398130e0b97ba7bca565c5`  
		Last Modified: Tue, 24 Dec 2024 22:21:55 GMT  
		Size: 6.2 KB (6204 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:a556d9a376c744395f3ef29191e357fbee8cf178444a9b3289b04b42ef2d001c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46763528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae14f884fddf6af484c1f622b90e795194bab6b0d766917519ee8b96d2c1d548`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'unstable' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:e3c1acc05fbef0b49b7beae5fe752774d0d837ae734c25831aac4c703b6387fd`  
		Last Modified: Tue, 24 Dec 2024 21:38:00 GMT  
		Size: 46.8 MB (46763309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd19c58d76a2527a787f1fcd1f969ac2dbcc0393d9aae73ca856ed424b4350f0`  
		Last Modified: Tue, 24 Dec 2024 22:18:33 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:a9075b0b056b1a438e5e90be46903922e10a97c0ec95045dd6da1273a80ffa32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3238177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d6aac0a885b2c334547da7fc0c44f3b40038a54bcf317fc48a862a3b6225fe`

```dockerfile
```

-	Layers:
	-	`sha256:b24b8e2d36c4013966ff790b801ae90dd32b1ace168ea01cb6eefcfc9f2068a0`  
		Last Modified: Tue, 24 Dec 2024 22:18:33 GMT  
		Size: 3.2 MB (3231973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6aee29acab48eaeeb55c0f84730dd25a782b289faae637d40277f52d0faa8763`  
		Last Modified: Tue, 24 Dec 2024 22:18:33 GMT  
		Size: 6.2 KB (6204 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:f6cae6c5766cd4f8287f10829d6d5125b1aa2b90ec2f76461438301f0854dff1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52432537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f21439f88f41a1f6cda7e737d07318077faffcc2abb43f3f58ee7748fb9d5a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'unstable' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:292cceccf1d705ec66776ac4a8f9a94e278d00802f8cbb2801a6bf344a35b844`  
		Last Modified: Tue, 24 Dec 2024 21:37:41 GMT  
		Size: 52.4 MB (52432319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47091b2c461839b5cd65f592edc8ea88743ab00a1bb3d48b83520f99cb260b0`  
		Last Modified: Tue, 24 Dec 2024 22:19:32 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:79065e970c1cab6d6a8ef91b823fc97b47049565c9cfa37daf3020ae6ccfb7a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3240212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf27852c6b91724051dedf7f51826b235390d5b56dbf47d6f90c83410a7af61`

```dockerfile
```

-	Layers:
	-	`sha256:6536328d522cabb89cfade6eba95dcca30edbbd19cb28bfd8fbcabb13fbe003e`  
		Last Modified: Tue, 24 Dec 2024 22:19:33 GMT  
		Size: 3.2 MB (3233988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf097984f9834f003997481a4a90b192b5550734b7b89592e45177ee1bfa27b6`  
		Last Modified: Tue, 24 Dec 2024 22:19:32 GMT  
		Size: 6.2 KB (6224 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:9e6175b576e38c9dc2d11c31dc0ca35b6151100b3cddb45f9973f03d42323d48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (53039036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa56258388378a592e803a62d8d0c6a1cc7e8a64997cdc560f311b12889a54c9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'unstable' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:38cd1a3ca278f6327b7f1997982125722985fc3e2b320756091d8fc5b6773896`  
		Last Modified: Tue, 24 Dec 2024 21:32:43 GMT  
		Size: 53.0 MB (53038813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4193ab109f02de393bbcabcfdb43c2a10ebe3302b7282392af678cb86482d5`  
		Last Modified: Tue, 24 Dec 2024 22:13:36 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:6a7912bb1a4f31eb6696b0ca4d525cc1162b53d65bf9e6568b5abbf1fd5c5ab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3233010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7600bc218231d56963f1cf2f8c8674604437cbf0f5ee5671121fac8929e1f3ff`

```dockerfile
```

-	Layers:
	-	`sha256:8754abf9cd29ff7c8e8391aa8ce46b7a816034ee6770c03d6d02090fc598f1dd`  
		Last Modified: Tue, 24 Dec 2024 22:13:36 GMT  
		Size: 3.2 MB (3226888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88fdf206f7418d2734fadf38afa15bff85d5e87d919c0718108c703baab95aa4`  
		Size: 6.1 KB (6122 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; mips64le

```console
$ docker pull debian@sha256:95db240142c0c49157e9e1321cb02e9d22f4841f47ed5c6c794e7a650a05ea3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51771556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7348b3dbd5ddafe995f96e42295bad1df53a78085739dc82d062c79dbd3dd5e1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'unstable' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:c7096bb99e4a357723a396c1bdc29df188367d48330c20e2a232e02ee8bc5c38`  
		Last Modified: Tue, 24 Dec 2024 21:36:39 GMT  
		Size: 51.8 MB (51771337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cc90332dbe076c93ff787c79b6fbd629bd29ad223da69df4602115f0a45af8`  
		Last Modified: Tue, 24 Dec 2024 22:20:39 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:0a3f5f7e9302fc71e6fe2402f37d4739ca3eec9ad6d5d7db78860dfa2b901777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 KB (5977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea88cf1c2e666e6c640c71fd305c0fb91c70454338ee46d7c5e8573f668d6fb`

```dockerfile
```

-	Layers:
	-	`sha256:52b5c798af92be0b0b7a9531beaa72393a738cb2f161be2641846ee74031a481`  
		Last Modified: Tue, 24 Dec 2024 22:20:39 GMT  
		Size: 6.0 KB (5977 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:38a14259d688c28d01aab278af3652a28e5f428a0da687b72067b96227848fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56045235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65201fc5c8f5c91b9e60e71678416baac904ca70b9587b3307298d28c0029905`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'unstable' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:d9980fec0b683b2f25b0fb51669ec6c213a473247e72f9d2a5380d723501a01c`  
		Size: 56.0 MB (56045015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4740594a629ac78f66fb4e8435da9325605e911eb6587a1c307662e57c6b038`  
		Last Modified: Wed, 25 Dec 2024 12:50:38 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:baff0dfad5e123d4d9c4899a16b830bc629ef8f3f2f18461c51efd38f330a35a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3240272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f045bc501b629a25e4ec8bce607f0ee447448b4f29c3aa05e3d260caf4222a`

```dockerfile
```

-	Layers:
	-	`sha256:d664b6f74a00a65855b8e25b3685001b4d6405b914adcabd939a1eba8ff44b2a`  
		Size: 3.2 MB (3234096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6e546e9278ca2b7a369c6a2aea7ad3fda325ba188ca17e77dd9f9ad1e964c38`  
		Last Modified: Wed, 25 Dec 2024 12:50:38 GMT  
		Size: 6.2 KB (6176 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; riscv64

```console
$ docker pull debian@sha256:d8e6070a27635e621cb98db1df6c16579b46e381cbb4b108fce3573aa0437dd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50712027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c8a0768488c984babb2648370919f37df3404956daa8be40a95283138bd0d4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'unstable' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:dc288a98bd46024eb30daac559cee25571d3e6c91b5e07e7b690ac4d1c1ae517`  
		Last Modified: Tue, 24 Dec 2024 21:45:56 GMT  
		Size: 50.7 MB (50711807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cadd142406015bb41b6afbf093002564194ee6d470136d576525fa1d72db32`  
		Last Modified: Tue, 24 Dec 2024 22:21:17 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:736a97770dfeaf6a68dc1b4c192fea9021306c85c2ab7f68001c9c0e16567352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3229960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b374f70a50b5f116bf7b4ac500d8294afa0b98c53c6c6dd44cece65f20e2ba0`

```dockerfile
```

-	Layers:
	-	`sha256:a0c1565afc5c392bee1db0e7d1989ea26ba192f3adf0e9143fa275352d3994c5`  
		Last Modified: Tue, 24 Dec 2024 22:21:18 GMT  
		Size: 3.2 MB (3223785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8782f6a7c6968ff7879a75cfb4d757675cdc69eb1bd0a71c7fdd813a60e39cb2`  
		Last Modified: Tue, 24 Dec 2024 22:21:18 GMT  
		Size: 6.2 KB (6175 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:ecad46c5cf9d793591a7df79e716b9b797005542e1c807086f6bd7f20f45b01d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52170138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e273c21cf26f8dc41cd4417c025f2567c46731595e2a225eba6d63e672bd455`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'unstable' '@1734912000'
# Mon, 23 Dec 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:247c1bedc0404d0af0d2f2ae3dcc36bc79be0841a3cba394aece41f061634e91`  
		Last Modified: Tue, 24 Dec 2024 21:38:58 GMT  
		Size: 52.2 MB (52169920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bec10b215ef2beb24d2873a11b555d6d58ffc3c575d7567e365e04a266c955a`  
		Last Modified: Tue, 24 Dec 2024 22:17:54 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:2cf78b9edff84631af4abf0c3a0edbe5307159445e83da7d01a38f3f2e132b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3238142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a9492ada8ef2ad964f04260af4e8c29252fcb09d68534802a6a93e316af839`

```dockerfile
```

-	Layers:
	-	`sha256:9241353980c0deacf22268fb87b50eff792b4c92e939ec01449c7d9fe4ad4a5c`  
		Last Modified: Tue, 24 Dec 2024 22:17:54 GMT  
		Size: 3.2 MB (3231998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f1547376cbbbc2c5daa5ab16c4ec94ee7c532853728b661c55a3d1bcfe96af3`  
		Last Modified: Tue, 24 Dec 2024 22:17:54 GMT  
		Size: 6.1 KB (6144 bytes)  
		MIME: application/vnd.in-toto+json
