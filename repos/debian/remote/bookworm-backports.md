## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:15aa58f4e6f4a5f1b3246e0ba101c13b6825f7c875b9361788e377ed2b46a34b
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

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:9a4562cf5d66d8342030a269b39fbeaf409702a5c9c7db557a01f6c8ce1148d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48490766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae0ccae372898e6293eb0ab1b677e68801ebce8733b57eee703c493a150b826`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Mon, 07 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8daf244457fa30e1063b022babab0e9fbe06b189a7002d101cc7ed819b804ee`  
		Last Modified: Tue, 08 Apr 2025 01:11:26 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:74232f626241e5afaa043fa4c9c67265ad2efc9f6b17e215facea0c3790416aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57f00d5b6346c836eb15b592aa4757faca92bb3452e4e320634b8b12999d558`

```dockerfile
```

-	Layers:
	-	`sha256:a899694d303415b2b06f75cce0c0cb48173d4fff5c4a9253316b078245f57b6d`  
		Last Modified: Tue, 08 Apr 2025 01:11:26 GMT  
		Size: 3.6 MB (3620572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c96a12d945813f1277a1419eb2504b46ff3dc4bba2a32888cb353f9d2c092f9c`  
		Last Modified: Tue, 08 Apr 2025 01:11:26 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:142592c2949b81bf917a71519b45d8398bdbf6778e10f058635fb115dc1f9b4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46026413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844e0cced5ba787c51aa75801ace894724e2ffebfceebb1d56a53ddc507bf23d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1743984000'
# Mon, 07 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:444a58715eaf0dfd1bf39e8ed2c8a7ca67bc95fb2e8d072811ba720753b5bdd3`  
		Last Modified: Tue, 08 Apr 2025 00:22:50 GMT  
		Size: 46.0 MB (46026188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390ffa36dd77fa06c5a540b850771be95ca124805c82d895458bf56b0936fa3e`  
		Last Modified: Tue, 08 Apr 2025 01:11:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2bd0b55db4cecb9dd4e767e5c505d3b7c65394b482f950c76929c8d54b43e09c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de16546e0df957aac834cc3bded7709367efbd45021231f7dd71086806d04d31`

```dockerfile
```

-	Layers:
	-	`sha256:628a0a6580cbc7ca438259afd964cb4d3e95df66af87b9e262c353838983b1af`  
		Last Modified: Tue, 08 Apr 2025 01:11:06 GMT  
		Size: 3.6 MB (3620773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:412ec927a6f45d210d66db0e4bec3e96ade874818b10a2f88d55dcc007f0f8dc`  
		Last Modified: Tue, 08 Apr 2025 01:11:06 GMT  
		Size: 5.9 KB (5898 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:6c9dbf1f3ab3f2e73dda7256f765f338d917db719f819696e0ebfbb8c4a3804b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44196997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e1a0badf5fab7d5bc9e3850419491230f0672665977778012dd73ccc40907a7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Mon, 07 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e40f48a2e6d38c2746e98a645887fe65e2b335f766dc7c61af172a1356726d5d`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 44.2 MB (44196771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f551964e2cde57f2868e2c08c758a41ad4a96324ce182fe62721cafa1e1b59ad`  
		Last Modified: Tue, 08 Apr 2025 01:11:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7f38ec32595d6a5c1d567d2d54169ce0c0876d4f971716640cb34180d6df5df6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f62e2465cba2e13dcc4500726a77bde29dd39913be888ef462ac1df9440955`

```dockerfile
```

-	Layers:
	-	`sha256:1849fb1407d4ff5af0dbccb855f40090a48e88c28241026a948fb9749c7728ba`  
		Last Modified: Tue, 08 Apr 2025 01:11:03 GMT  
		Size: 3.6 MB (3622751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d957cdc8a5571ee76b1a54e4478a2e7f8838f5928644e68c78834903f65a93b`  
		Last Modified: Tue, 08 Apr 2025 01:11:03 GMT  
		Size: 5.9 KB (5897 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:dba071ef306700351d10028c9afca424488e7ddb3d16110113dbb04ff4da193f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48327695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea7582d650e8a5465a53453f45ca1b7d6d7cb82944c91205c74934ade2a95ac5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Mon, 07 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f551964e2cde57f2868e2c08c758a41ad4a96324ce182fe62721cafa1e1b59ad`  
		Last Modified: Tue, 08 Apr 2025 01:11:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:3187dcc6f6928f11b0d6642f43c790ae722cd8a6b888d886dda3e44f08b06ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d897b83d01dbf06223360c7cecbfb6c5f02c880de762b0d54a171b82f57d3c9`

```dockerfile
```

-	Layers:
	-	`sha256:481a4ee07a4656a1c6240e3f6f836c7f48f99fdc0e97fbda8257e6749a3276ae`  
		Last Modified: Tue, 08 Apr 2025 01:11:01 GMT  
		Size: 3.6 MB (3620787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e93dcee590bd493e37ab016e805587e3cc76b59fafc23da2dca79fadc60a34b`  
		Last Modified: Tue, 08 Apr 2025 01:11:01 GMT  
		Size: 5.9 KB (5915 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:e44af56dc669dd4374b4d30af1422432b6a1ac8494b7b16170e391f70985a8f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49478357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed63e8c2e66df09a903d75033eb422583c2d0ab72cc75836926dab92b7efb4d2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
# Mon, 07 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:437850497c82f7f6311c6cddf1db9d5ec53b7315e3733ed836cb00852f8fa683`  
		Last Modified: Tue, 08 Apr 2025 00:23:53 GMT  
		Size: 49.5 MB (49478131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c9851963a29f63f34f0e5b537b42a2534f346cefb6ac71f39ca976196802a7`  
		Last Modified: Tue, 08 Apr 2025 01:11:57 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e674ffebaeca90781ce0de53f0fc2ea19661b35cad9cf585d1b970c2b904ab53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3623563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3348d44edd3cf7e59283b03915df9b5af5eb23a9b64e2ffcad85580ba438f9ca`

```dockerfile
```

-	Layers:
	-	`sha256:10760b036efbb73b1aac9c59855580e203eb02d2ea5341fee7ee62eb25413a58`  
		Last Modified: Tue, 08 Apr 2025 01:11:57 GMT  
		Size: 3.6 MB (3617733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7209bbf324a1d9dc18b080e91c5b47801762f386572e4d48f7176329e8aaa74b`  
		Last Modified: Tue, 08 Apr 2025 01:11:57 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:41da3759aa827a9efc393b645df8634ef391f70865664ee368b39f23a9b3727a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48775090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d5f70670a03e614be69bbce15d17d45c665e13711719f5a7de0c3e12a0fc745`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1743984000'
# Mon, 07 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f5e7682657f9515783d77fb7efbdd12ea81bbe4c750080727193e5396dfa344f`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 48.8 MB (48774861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6264f3e1f7a4c688fb8d9dcc4429ba693f13469b2cd33fdb960c4d8e6bd0dedf`  
		Last Modified: Tue, 08 Apr 2025 01:17:57 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7ec2f92df6c1b9e2a0980dc26f666cb4be06ea4df5bd8d9405afb01899e2c7c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d2f7c3e5f6febddae3ea3bb2fe1eac4b0cce27e64d6f558d7c594fae405b5d6`

```dockerfile
```

-	Layers:
	-	`sha256:03ff74c29e135ed9d1e3bce5b5ea655d07d2ae4782f229b0c25c8398350d8831`  
		Last Modified: Tue, 08 Apr 2025 01:17:57 GMT  
		Size: 5.7 KB (5671 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:7cc3c959ae92b0cadbeb05bd120d9ea8caf152a3fb3314144e8d591e86f37bcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52331871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e3c0bb0720d875ec44095af1d3a9108d5cb59849eb3d8fa66b2ac6fbaa2d7c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
# Mon, 07 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:96130533c16d0aeecdcc4c64baab4a3adfb31877715c21a61125a04fe062f893`  
		Last Modified: Tue, 08 Apr 2025 00:23:16 GMT  
		Size: 52.3 MB (52331646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612eb552f506ddc5da5a6a9e04ee52ff53cdbf6461b369831a61aca726882231`  
		Last Modified: Tue, 08 Apr 2025 01:11:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:afe95a5b3034a19bf5a0365e30fd8488ef31f10fd05aca03aefcc281367a782d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3fd31fc6106d90b84d4c6433a97812edac9f0a6bc6028b7c814a65b11c8eaff`

```dockerfile
```

-	Layers:
	-	`sha256:521118eb4709715f5344b03d67eb7382aa83afc18574b0ed333049878890a442`  
		Last Modified: Tue, 08 Apr 2025 01:11:56 GMT  
		Size: 3.6 MB (3624832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d1f3c6c149bf1464ad2ddccfce529782ed74e2c55a56f260f48544fc411a0d3`  
		Last Modified: Tue, 08 Apr 2025 01:11:56 GMT  
		Size: 5.9 KB (5873 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:008d197cd0e3c6386a5bed0bb58d2961acbc165302b1eb33d3a5d206bcbd59b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47151220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aadd521cca79f4ae00e6704c74df0dd76b36ea70ce4c292c449c83dfcdd3fe6d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
# Mon, 07 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:02fcba40f83e05adf85891b5c708b183d1028fd36fd80528f148e95bf593ab77`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 47.2 MB (47150996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df45c1d7021a433e0be142f4567b50371e6c32554c52073900f24aca0bc521bd`  
		Last Modified: Tue, 08 Apr 2025 01:11:34 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b94a7cd43a4879ae36c0185190f25528c436e271ea42938a337d422f8dacfde8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6964c64be38c5722e5383bbbbf3188c73fe8de09250d91f7b931afced5ad5c3a`

```dockerfile
```

-	Layers:
	-	`sha256:efecf21adba2741ffed44397aae8c3065063213c6df092cf61a6b35f3a95d837`  
		Last Modified: Tue, 08 Apr 2025 01:11:34 GMT  
		Size: 3.6 MB (3620302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80efb54beb5b41f920b24f7d0b04d8ca413b3909e3c25ef3c7eca49df364f179`  
		Last Modified: Tue, 08 Apr 2025 01:11:34 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json
