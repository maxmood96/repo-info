## `debian:forky-backports`

```console
$ docker pull debian@sha256:4d65c2fc3c09a3a25786226382e8a1ef9964f7e77eed6a9be4537d44d444c2b2
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

### `debian:forky-backports` - linux; amd64

```console
$ docker pull debian@sha256:c952ada59d6e72fd884edfcecf43e809aadae342724034cc416da7e80ca4cdce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48758013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4dc0ff18f142531ae7a367c66b5aac55a0b3c44cdc7ad646dc0c7ebcca9d4b0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1782172800'
# Wed, 24 Jun 2026 01:15:00 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:447e2db1403dde86cfbb4e736a0555036d98321ddc327da9305db2a007cde1f2`  
		Last Modified: Wed, 24 Jun 2026 00:28:17 GMT  
		Size: 48.8 MB (48757790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ad2f062146779d1a3cab2da94fbd3579582fc973d8bcbbae6067071d735c22`  
		Last Modified: Wed, 24 Jun 2026 01:15:06 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:94a05f1701c1f8a49a0f7e2ad429fff232a771fc98c3d34faac6f559738abbe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3156490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85f90b85e78352e772be29877fb61682252765a8479481115579629ffe1be958`

```dockerfile
```

-	Layers:
	-	`sha256:fa7462a68b51076d8911f2e4d5c8bde43bb78a205af336f5245df1b855370982`  
		Last Modified: Wed, 24 Jun 2026 01:15:06 GMT  
		Size: 3.2 MB (3150713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8623477b124f8d4bf44f89042dc366be229f03315d669d8c72b65bec4cf37a3`  
		Last Modified: Wed, 24 Jun 2026 01:15:06 GMT  
		Size: 5.8 KB (5777 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:45b94a3efd36d3d61e088747a94307b2849fcb2608aeedc41f22f45928ccfa6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45653314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2f99b20d576bd5d9e0dd840cecbb8578aa8cd6e2b19b42216b3a87a0eab58b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1782172800'
# Wed, 24 Jun 2026 01:14:45 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:36ada862ffe71636cce33b70f21dd2f7cfc66ebaeabbfa49191690cfe0284fba`  
		Last Modified: Wed, 24 Jun 2026 00:27:47 GMT  
		Size: 45.7 MB (45653092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984847151b9a1a2b63311f8a769e787e513ed5c24755644d68387a1f187406e6`  
		Last Modified: Wed, 24 Jun 2026 01:14:52 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9cd7f5e66d719eba2ce35899392434c5b42e930eeb721e5b67cd121f1e39e646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3157909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c7cb4ec9d7dc608f342c6f05592a76c3ea3bae885487e4fe097e4c4fdd8637`

```dockerfile
```

-	Layers:
	-	`sha256:2ad7998e51f4e75418f761758a2152318fb1ba98b998368760f951d15ad0e3cf`  
		Last Modified: Wed, 24 Jun 2026 01:14:52 GMT  
		Size: 3.2 MB (3152075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:483b7a155540a4e5d5e8232f91702afb6d2d2871dae65089cce1e1af107d860d`  
		Last Modified: Wed, 24 Jun 2026 01:14:52 GMT  
		Size: 5.8 KB (5834 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:bbf38fc89a0e962a0a09791257019379d8ce4cdaada4b4ff83b64afc618f6e8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48768935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b19daf4c9a7c82ad1fe92e64c38f30322bf9ea037cd74c34dada58a7b6669f31`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1782172800'
# Wed, 24 Jun 2026 01:14:50 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f5991d5bb2fa21186c9152bf0a9fa1c9c73892f68235c440c9967628fa5ecac9`  
		Last Modified: Wed, 24 Jun 2026 00:27:35 GMT  
		Size: 48.8 MB (48768712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588bae55b83d2bb0788e68c83ffd726b50bc46c727e0f50d9137c1272f6b6358`  
		Last Modified: Wed, 24 Jun 2026 01:14:56 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:46adc014907877cfdde456e3a5660ecb1e13e9528bbec31ac54824129c378b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3161228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b92d9a30de866573af0dc09e56640683b05252e35a69de8261dd53eb35d9e81`

```dockerfile
```

-	Layers:
	-	`sha256:da1a3111a8ec88a47c4763cf4a4b49a71b44259759eaa611761a9c07c5932d5d`  
		Last Modified: Wed, 24 Jun 2026 01:14:57 GMT  
		Size: 3.2 MB (3155383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c69a89084a7977ae6b8953ef382a9458b8b42e2fab96afbf7dce89dfcd042fd`  
		Last Modified: Wed, 24 Jun 2026 01:14:57 GMT  
		Size: 5.8 KB (5845 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; 386

```console
$ docker pull debian@sha256:359e95bae3774975d043735c22301023e5e3822eb3254ab57772c0acb797c2af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50051254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce19127024232218ea34b298f0940982b3b3a4a4e2b07af3e41491a942361cc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1782172800'
# Wed, 24 Jun 2026 01:15:02 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:9b65e2e922e5570b1d72c057efc4f398b0b14051ad2a0b581d6669e50195e288`  
		Last Modified: Wed, 24 Jun 2026 00:28:28 GMT  
		Size: 50.1 MB (50051032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e685ecbf9e7276357fb64f01f2266d349240e455f9e0fc2542f373b70a980754`  
		Last Modified: Wed, 24 Jun 2026 01:15:08 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:bdfc762c49c33e8044390dafde49f70b1e9e4349906494b29b4ffb4013809848
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3153678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c84d3fc487402ce7401aed2c5448d873e4d410f90e17b348ff10f9ece5c45a3`

```dockerfile
```

-	Layers:
	-	`sha256:77908e4b5c6057c76734396bb6f00589882b62bbc1f2d2eead3d6bb838766875`  
		Last Modified: Wed, 24 Jun 2026 01:15:08 GMT  
		Size: 3.1 MB (3147917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12fa5689d1b58bbc3df93c4ff940101f116caeddc3db90b0f45f34bc1524cc2f`  
		Last Modified: Wed, 24 Jun 2026 01:15:08 GMT  
		Size: 5.8 KB (5761 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:edf9ef7037de3572f55e2205a14beb7720f75613eb387c89eeb26c18bc5d2f8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54079251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b556e9ed9c87eec2f918b6ecbef1aeac6c6e3a6cf99142aeb7dc6c958b9dba1c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1782172800'
# Wed, 24 Jun 2026 01:13:36 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:18c7f7605567d97bd2e11cd865b7616a79a2f59d49d2c2db26f6e2d2ee14157b`  
		Last Modified: Wed, 24 Jun 2026 00:28:03 GMT  
		Size: 54.1 MB (54079029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdeab56578157d35371c65c5098613d91ad58c2acd3463326c0e03a11bc55c3`  
		Last Modified: Wed, 24 Jun 2026 01:13:57 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7ca487e39a2670aca8fa42e7dcb469266b1a1588f737ec17cd26504b837b8078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3160014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:743fef015caf0ede78176c13017fd701a2b3a0aa96aa90ccefa5e3cee72ae412`

```dockerfile
```

-	Layers:
	-	`sha256:a8dcf122afeb054f28a15b72ff9dd4732949de6d9f29fd48ce961050488fd068`  
		Last Modified: Wed, 24 Jun 2026 01:13:57 GMT  
		Size: 3.2 MB (3154210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:920e305aed51c9c96030e977bb1a2d1e96c51cc538841490b573c2728cd8de61`  
		Last Modified: Wed, 24 Jun 2026 01:13:57 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; riscv64

```console
$ docker pull debian@sha256:aa6e7a39a3a0c8a5423ba95e4d47d7af1e0c6a3f6264d41f05e3ae4d50676e44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46847814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e579d0b58cf9fe29dd6c583ceb77a102feff5bab30dee27a9d287bf674cee2cb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1782172800'
# Wed, 24 Jun 2026 18:32:24 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:198a866fee61102466333b8b7e43c7a497d2c89dc9749834f261975581cdb8a7`  
		Last Modified: Wed, 24 Jun 2026 03:25:50 GMT  
		Size: 46.8 MB (46847590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0d6e7d7f381dad4f641e0eddf0dcfd5700b7769d81e793f647b9beb5501371`  
		Last Modified: Wed, 24 Jun 2026 18:33:17 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7ce91c469a4a800d7d89ba5814f69ff8218c34314c3118bfa4383c80e836a7ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3148017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab4544d4584e2e7c90f3e1c48ced5130c4ec4b165a9d18d266084de50289f42e`

```dockerfile
```

-	Layers:
	-	`sha256:fd6ce941b9a049de0848060fb5772201ff219c6fa3d5b0563a2e7b8ab0c2d5d2`  
		Last Modified: Wed, 24 Jun 2026 18:33:18 GMT  
		Size: 3.1 MB (3142213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d93877ff57d1c95c1b0a91afd3d9110e1d2ff9b1b88f9da606c5c88d9fb0b5ae`  
		Last Modified: Wed, 24 Jun 2026 18:33:18 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; s390x

```console
$ docker pull debian@sha256:1536f66196bc40b1f05a476ffd4bef3c18ff89db14fd9095778b2d5da7483ed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48492061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e2624353b3a4c8801877cbafa13766ef707f91ade3c65f08578ecc838749b98`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1782172800'
# Wed, 24 Jun 2026 01:14:03 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a0b2fd23e0800fbbfc85ca591b838ee879d8a24facc5eea58fda6e804f1b9315`  
		Last Modified: Wed, 24 Jun 2026 00:27:12 GMT  
		Size: 48.5 MB (48491838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8df39c9e14570086e376289f03b376c170f2e19c3f807b65b96f326435e3a6e`  
		Last Modified: Wed, 24 Jun 2026 01:14:13 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:fdfd1621f5c2e2cbb47a3a80a13037413dc77d32f3f2c0fb727ae9d71d023d38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3157942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16bc96449c77343402b52dd7544207fe08143149f7cb3c78895ea072ba8495b`

```dockerfile
```

-	Layers:
	-	`sha256:a70abfe6c3c7a43c1897a49c756eabc4c8fc85bcbc60a99500e5c85c30d5fb2d`  
		Last Modified: Wed, 24 Jun 2026 01:14:13 GMT  
		Size: 3.2 MB (3152164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:980593c9bb1487e86437335d530ca10a1dd4ffb84fd7406c2d6823a479a3fe02`  
		Last Modified: Wed, 24 Jun 2026 01:14:13 GMT  
		Size: 5.8 KB (5778 bytes)  
		MIME: application/vnd.in-toto+json
