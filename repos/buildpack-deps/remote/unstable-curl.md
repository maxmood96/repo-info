## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:57b307aaa3b5238e4b4830ed55ffcfec98a2927fd9fe725ebe0403d1436706c8
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
$ docker pull buildpack-deps@sha256:a2788682f53c727debe5159f58c17bf9701acd5840a056d3ef008eaf0e5bb00f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73800876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6970ba6285920f38361def9c7b603339b3423d9f562fc26d9f1d7886a34bdf5`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:df0497091d0cfc8e931a73bef35cfd57d59f19322fcca6f87470d3b532a9d8c8`  
		Last Modified: Mon, 17 Mar 2025 22:17:40 GMT  
		Size: 47.5 MB (47542630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13cd1ca2661836ac2dcfb48519e1a1fcf2b3ddbc182b83cfd451a37cea0328fe`  
		Last Modified: Mon, 17 Mar 2025 23:14:04 GMT  
		Size: 26.3 MB (26258246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d2f2eccc24a5b2ddab2fceb30638c789f54b7447e18f08374242ddde0f58cc45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3965779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a295e4bfb28701e01e4f3d26b39dcc901231a9fd3a5fa6c00b291e0b9bd0ac`

```dockerfile
```

-	Layers:
	-	`sha256:041540c465b22579a880d623d4aa1a046ca288aa298f06374f3b7647b8ec0051`  
		Last Modified: Mon, 17 Mar 2025 23:14:04 GMT  
		Size: 4.0 MB (3958975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5013f7ddbf9e169be5bdda59b289a6f70b1babf8f7f725348d90af0cacda1e6e`  
		Last Modified: Mon, 17 Mar 2025 23:14:03 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:400bf794ffeb4799c3883935d768c247a8d4acb46b10788099219442dfe1d842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70598525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d2476c6896c6e65ab179ebcb46d9899c3c4f610a67785eff63d7602184abe7`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1740355200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:aec04388a5500e40b5b47dc94d28a38cfaac08b914f818d50d6fef28b32d9a5c`  
		Last Modified: Tue, 25 Feb 2025 01:31:20 GMT  
		Size: 45.7 MB (45691956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7909ec64897749d066538d04d73bf65a5bcacffc48c9bca80514cdb519fe3782`  
		Last Modified: Tue, 25 Feb 2025 05:16:49 GMT  
		Size: 24.9 MB (24906569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:88b341e4adeab1f2f61ec1f1d45f173fa93b4ccd6c612ab5ce7f87c53dfecf1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3977018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fe73376683552f380ea1bff2989b5ad861cf515baf86c5d6eac17a3942a50e9`

```dockerfile
```

-	Layers:
	-	`sha256:26158a09eae23cdf4ca56ba7353be85e60a3a85d3cd06acabe31779178c6f68a`  
		Last Modified: Tue, 25 Feb 2025 05:16:48 GMT  
		Size: 4.0 MB (3970154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b4ea90f938a6d4e6eb9705c8f03eb586575de7f3055df84665e0a71b25732b5`  
		Last Modified: Tue, 25 Feb 2025 05:16:47 GMT  
		Size: 6.9 KB (6864 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:eaa45ef1f287f0c87b4859aab7d2846a973403a2ddf6bc215c44cf7727433400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67968778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fcf95dd1a8029cb017112d2635aa23f2348308c5449fd571df1a5cd8149a58d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1740355200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3b9b505d2f2f0a849a74a095acfe5025f5d72fb01d82d04f1365cd960707119a`  
		Last Modified: Tue, 25 Feb 2025 01:32:18 GMT  
		Size: 43.9 MB (43880302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd562fc242f36f82e6cc8e66ce3b8e9aacffd6f2c454b8c1521cbb050ded690`  
		Last Modified: Tue, 25 Feb 2025 07:17:52 GMT  
		Size: 24.1 MB (24088476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8973d048bb4ad9873c53e627f5a5fe1423a79a0638a90ad4d65166a1641f3e96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3969607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a34eeef17b08f467fb2742b821307eab0b6b0254fd24207709672aa932ce91f2`

```dockerfile
```

-	Layers:
	-	`sha256:7348308e52175f7601f3e488c3c2779a279a6b36570b9b71d283e825133a3a4e`  
		Last Modified: Tue, 25 Feb 2025 07:17:52 GMT  
		Size: 4.0 MB (3962744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebe0bd1b9c0fd4107313bad7400d5e011b36811b867e3a064dd6ac6514e5abec`  
		Last Modified: Tue, 25 Feb 2025 07:17:51 GMT  
		Size: 6.9 KB (6863 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8a7cc753fa7fdd85df9c4a7a53e443a44600315c22bc89d46d1936fdb1562055
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73498665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2f1d0ba4118194996f7cd45cbb398f234bd7a6668e0a36dacc344849ae2fc3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1740355200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:82dee3ca1e84a7a17d41ea99cc856a25e454e910360ce904862612b751069507`  
		Last Modified: Tue, 25 Feb 2025 01:32:16 GMT  
		Size: 47.8 MB (47842599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8fdaf1ee62a1e8985dc4f6dd94f1ef4b21fdb86969059a5e1bf8b87bfc3b6ca`  
		Last Modified: Tue, 25 Feb 2025 05:42:44 GMT  
		Size: 25.7 MB (25656066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f26d9ad0adf7f423c81407deaf81a7d19b0e4f7107b685b41472f01804973ed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3970306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9375b8a5a6365dd1f5b794d9c9c364e0fc4de9fa836d6b147a68addcb413c217`

```dockerfile
```

-	Layers:
	-	`sha256:98d1824062b58021c276e86ee7cabedf4d9788ebf0c4620adab8bd148ae1cd24`  
		Last Modified: Tue, 25 Feb 2025 05:42:43 GMT  
		Size: 4.0 MB (3963422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3b564f3a7127e22560f201b564d506db4f73e84d428dbc227918219f4fbdf66`  
		Last Modified: Tue, 25 Feb 2025 05:42:42 GMT  
		Size: 6.9 KB (6884 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:97cfa441b941ce843b8e64821979dd906d34484a60046cf488a84aefd3a2fffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76259470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9782a0d783450d496881db896b052813aba2f4f816bf2076a9eecec8cb7cdf35`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f3d6c6a3aa49b126cd200d7ce5830c3bb8ef015d44bad711b523cd3cad501611`  
		Last Modified: Mon, 17 Mar 2025 22:18:06 GMT  
		Size: 48.9 MB (48863161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888eee8ccf6b7f4f49c878caf4a23b48de26dc0c12d38b4a0f13ce0b7214d834`  
		Last Modified: Mon, 17 Mar 2025 23:33:29 GMT  
		Size: 27.4 MB (27396309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:40aec232354a0e4dc6dbe28dd5bb7cdf894ea6fcda423cc2b0d54dbaaa1a92a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3962167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9774c6726c6676f3f7b0904397f4397aaa8238d00549a9fb2d32f34da395c345`

```dockerfile
```

-	Layers:
	-	`sha256:36109c4c900d01e2580194f48655821fb4ccf5a7303e2ba5400da6b080790598`  
		Last Modified: Mon, 17 Mar 2025 23:33:28 GMT  
		Size: 4.0 MB (3955385 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f145bcbaeb32ba813657130e55b66ec23eb53395c50ff744887aa2eb4f8730a`  
		Last Modified: Mon, 17 Mar 2025 23:33:27 GMT  
		Size: 6.8 KB (6782 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:d600a224322b1ac83e6f38b884dd1737bda081d9241daefd5f22eda4a1e3644c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73914019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8a848e994fb2403d5807248b856deacc3559d237a2c78339ca3bbe4374ae9b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1740355200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:34ea8e316aa47eaa9617f1b9a35d3a8120ea53cd407c4add1aafff37c0381edf`  
		Last Modified: Tue, 25 Feb 2025 01:31:10 GMT  
		Size: 47.7 MB (47672872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d13ce39ad4744d80777f693b612839d6935dc5ee1e34838c927f4fa9839112`  
		Last Modified: Tue, 25 Feb 2025 14:50:38 GMT  
		Size: 26.2 MB (26241147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5ea135a72da133950b47179c12f13222858b5cc982c9fed0d6e3d6a2d182ae0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 KB (6636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06c0dea48bd566c0710053bcf4fcc480e6ef199d791091fca6747fc492aaeff`

```dockerfile
```

-	Layers:
	-	`sha256:9372cdabd70ca0f502321828721ca11c6d2b886efe7c47b530e9e64a41867b16`  
		Last Modified: Tue, 25 Feb 2025 14:50:36 GMT  
		Size: 6.6 KB (6636 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2494d35de6f345102df0d3b32b40579656ec8543bec87cba7626a46e3a8ba4be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78856026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d85dfc3a4c305284c5eb80373f65cf6f9d6e2bca6b1613430d8c18bb005492d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1740355200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9370c4ccc640520942cbaafa9d1bba72d3a14bc22c93d4c585e6cf8f83d65274`  
		Last Modified: Tue, 25 Feb 2025 01:31:22 GMT  
		Size: 51.1 MB (51109956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064a14d42f5e429844e608bdea207bfc8db8bb3a74d08ade67bcacfe19c5fbf8`  
		Last Modified: Tue, 25 Feb 2025 04:33:25 GMT  
		Size: 27.7 MB (27746070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9eefe030cf723f850da2d17aae2ba79568d509e2cbcb18316734270e41bcaafd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3978006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c910b1dfb58d4078b1480c0add701fdc108396817fc8f8b1bdc89680c1cf0fb`

```dockerfile
```

-	Layers:
	-	`sha256:3b6ad4a085d9d2ae36f15020c9a65ecb3bf812f1c044a87db26b31f845dfbef5`  
		Last Modified: Tue, 25 Feb 2025 04:33:24 GMT  
		Size: 4.0 MB (3971170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73d7deed42ea49d91b713057b65727e3b1128135c70c4ce7c12804d4112f4c82`  
		Last Modified: Tue, 25 Feb 2025 04:33:23 GMT  
		Size: 6.8 KB (6836 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:3b9b2fd3533da866c837c75eee0ede5ec295ef3f85a042cf22282f21f60cfd8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.6 MB (71644189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6a86500e3980bbb8e2d40c73dffa31fe4ee6445549690611a83716b859b8766`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e088c063eb399e547ca6ed33d1ebd46f19289743d98703ba83311c2214184834`  
		Last Modified: Mon, 17 Mar 2025 22:34:26 GMT  
		Size: 46.1 MB (46065424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a540c8b69cf893a7a0a6c436d4761b79fd51f1845aa5b66555a58dc019b8cea8`  
		Last Modified: Mon, 17 Mar 2025 23:27:02 GMT  
		Size: 25.6 MB (25578765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3a08400d4064ed554996ee7dff984b86b75fec2c5ba9b107ee71ab7ee87f5d50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3957146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3718beb8abe6420d927e2baf23ad5888b5c5ac89cabdf4d666abe84a9945608a`

```dockerfile
```

-	Layers:
	-	`sha256:2732bac4576e50f6de3fd4f4184d683a377d95fec291369d34b5a38ca3eec79c`  
		Last Modified: Mon, 17 Mar 2025 23:26:59 GMT  
		Size: 4.0 MB (3950310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99a010d31075b9e934746fa417abede9d2cdfdb5aef57765cf5bf370ce57fe4e`  
		Last Modified: Mon, 17 Mar 2025 23:26:58 GMT  
		Size: 6.8 KB (6836 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9bfc1f75b6c330678bfeecb972d23b039582cdcd8872fd0f8c2bfc48680361f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74867096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:176e40243a2bf6075206546040ec9d22dcd849d956de2c08d25a50a2ce47a315`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1740355200'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bb029d344ac2942bf1f98be4221b2466495c100c4662a25e8e6338cf9c0f606e`  
		Last Modified: Tue, 25 Feb 2025 01:30:43 GMT  
		Size: 47.5 MB (47498543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a284e667f853bfd37a5b5f735f1448b941efd88d6ca35d51858f3d1bc02320`  
		Last Modified: Tue, 25 Feb 2025 04:05:10 GMT  
		Size: 27.4 MB (27368553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7448dcd052651cfa9c0809ed9e744bb96df3cec2c9bfe28ac18f44e5ba0f9a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3975668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44b72911c36c80ad1e40b01df1d9e481d685ec6bbb7e1728ddcc85ea533122b3`

```dockerfile
```

-	Layers:
	-	`sha256:82509b881a94aa8026e1387b51f5c0fbc08a5b5105a2ca69c776d773af3f88c4`  
		Last Modified: Tue, 25 Feb 2025 04:05:10 GMT  
		Size: 4.0 MB (3968864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3c5837435ad28f62ba69eac3b7418557085610c87bc41e31ce86d9e22a638a9`  
		Last Modified: Tue, 25 Feb 2025 04:05:10 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json
