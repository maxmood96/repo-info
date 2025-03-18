## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:a438ae7fcab4698e8fe5ce035b77eeaa175177a85e1837a8814389bdb35af143
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

### `buildpack-deps:sid-curl` - unknown; unknown

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

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:74ee3ae850668f4ab9f67bd38bdcafda91c3a4b19739b94642b4c724da6a1733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70726670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a87af87a2047241d546d31d75affdc36ef7f718a94138322e581f4642f04ec25`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:181ed5745a356167f17446082e0f91fa4520dec07c3cc08122f73d6e68f0ec6f`  
		Last Modified: Mon, 17 Mar 2025 22:18:17 GMT  
		Size: 45.8 MB (45764033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce18890e4323b22dabb2af5cd6dd6ee47e0cbe22914fe96ed5ec5652746adc9b`  
		Last Modified: Tue, 18 Mar 2025 03:09:17 GMT  
		Size: 25.0 MB (24962637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a71070e5bcdc852fe244126e9c62ef57839ba1c57645a021b1ffe1ff633478b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3974102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d166e0d9fa2a6e206b9b5b937212848b29ebfa58eb8fa5c190ef3d9275d6ab`

```dockerfile
```

-	Layers:
	-	`sha256:3cd8aa89daccfc89d6695a3857f4d9f42e785b4de79b6dff2a21e21a3ae48961`  
		Last Modified: Tue, 18 Mar 2025 03:09:16 GMT  
		Size: 4.0 MB (3967238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb61975362d879917019afefc1c213d4b362c258867f698b50a5b4aecc9b06e1`  
		Last Modified: Tue, 18 Mar 2025 03:09:16 GMT  
		Size: 6.9 KB (6864 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; arm variant v7

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

### `buildpack-deps:sid-curl` - unknown; unknown

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

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

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

### `buildpack-deps:sid-curl` - unknown; unknown

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

### `buildpack-deps:sid-curl` - linux; 386

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

### `buildpack-deps:sid-curl` - unknown; unknown

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

### `buildpack-deps:sid-curl` - linux; mips64le

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

### `buildpack-deps:sid-curl` - unknown; unknown

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

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:bb6b86896c67d51995414fc2a0a4e717b3e8798e9743aa517fd2a669f7b1895b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (78995589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92cbc73c2d28c0e0f2936abe9fe4b552f4293cff0cdbb79391471d22890b85db`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4f7ad9881f20bb4c15e9c02d5c71121438e0f80af4492bc3595dca35345480d6`  
		Last Modified: Mon, 17 Mar 2025 22:22:55 GMT  
		Size: 51.2 MB (51201856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277e01a580518b309bd39ae29e17784505bd4ae5bf702764ef69018aabfb218e`  
		Last Modified: Tue, 18 Mar 2025 00:01:23 GMT  
		Size: 27.8 MB (27793733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f7f48a5adad28de33790cf6f78ac6ea19615526c32739b5fa27b7f1ef0845afa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3975080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68f66fc6098c02f5204694ea301086576254b5c2e0fa449761285ee217f8ec2d`

```dockerfile
```

-	Layers:
	-	`sha256:452708de4beb26a55b4584447c6dec5edcfa4d5ae225708d8fdff722c4a11c27`  
		Last Modified: Tue, 18 Mar 2025 00:01:23 GMT  
		Size: 4.0 MB (3968244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:305ce59fb16d8a1bf8e3d1bd7e1877de2177a7fc0b931c35a45833ac54919149`  
		Last Modified: Tue, 18 Mar 2025 00:01:22 GMT  
		Size: 6.8 KB (6836 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:sid-curl` - linux; riscv64

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

### `buildpack-deps:sid-curl` - unknown; unknown

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

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:5bf4465f9269710d45b4dd77c307d8ea946abd79c3ed78de71808e39166460a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74974060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead82ff34dd0ffd7f338fed7f20842a6d1c629752e2bb297245cea708ba451c0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1742169600'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:18840c5918002e02a891410ac8cb796ccc166700f997d1063ab46da46dc721f8`  
		Last Modified: Mon, 17 Mar 2025 22:42:36 GMT  
		Size: 47.6 MB (47571368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d448240a5617efe437620dbc6c199b4b34036766dc8ba22365b81ef5e32d08`  
		Last Modified: Tue, 18 Mar 2025 02:50:47 GMT  
		Size: 27.4 MB (27402692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:sid-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b7a7faadf26b4ea72e36fa14e3a66ae1372d285151ab35c7f0b17ff61281c6cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3973522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f404a1ae108675ea73a6f15e7844b22c36b6b905abdbf7f1176b0dc52d694e9f`

```dockerfile
```

-	Layers:
	-	`sha256:8c259c35786d85c6666fa9747f4a4b3077dee9a87256adf79de5c641add12fe4`  
		Last Modified: Tue, 18 Mar 2025 02:50:47 GMT  
		Size: 4.0 MB (3966718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e9c11841aa41dd9070c9794c23f7fcaff0228c5274d332c62af7218c4ea2d2c`  
		Last Modified: Tue, 18 Mar 2025 02:50:47 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json
