## `debian:experimental`

```console
$ docker pull debian@sha256:5869d3f9bc7a40b6b9b9e51faf694140cc778325372e5ca90dbc637e3713b694
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

### `debian:experimental` - linux; amd64

```console
$ docker pull debian@sha256:15c5bc342df464a8c9707af0984d4bf883b188afb4a05f41250fddb9aa257293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48778608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80713a953d3890e0e9ebc01d3c0bff85ce9f3b6d2cecb914a0ad3c7192993595`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'unstable' '@1782172800'
# Wed, 24 Jun 2026 01:15:51 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:045b4c8daf0382564ea34d12944c7fd75baeb0645434dc7993130fe8abd5469f`  
		Last Modified: Wed, 24 Jun 2026 00:28:37 GMT  
		Size: 48.8 MB (48778386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc151e1440969ee90957c0d71a544f20f23ed55757577f94ccb44ec3f2011e2`  
		Last Modified: Wed, 24 Jun 2026 01:15:57 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:686f80852b9685f02fbf826c45b0689f94ae090bfce247b676da93185cae9c14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3157767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5153977d1a923646c039e44b19c93e9ece70c5cb2e86423044f860887022a14`

```dockerfile
```

-	Layers:
	-	`sha256:dd87f0ae61f42898c7a4e42ae972c9233f0cb527e8b767d25f23975781412bd3`  
		Last Modified: Wed, 24 Jun 2026 01:15:57 GMT  
		Size: 3.2 MB (3151666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f87a84e7b6ba4280757f9bf9152495baed50ea4cc3da9afe4a924ec5fa208b14`  
		Last Modified: Wed, 24 Jun 2026 01:15:57 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; arm variant v7

```console
$ docker pull debian@sha256:790876fa2291a412ed99c2495d30179e2530bc750b37c8a0ec5f95fd18a31827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45678857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0c84c3a8f4005b55f3d90e0e3f1a43f87746964d1133eda254a166aea77e97d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'unstable' '@1782172800'
# Wed, 24 Jun 2026 01:15:44 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:9b3921c200941231211cfc04498a1fe1318b746d3cdbdf31ce7b899e85741821`  
		Last Modified: Wed, 24 Jun 2026 00:28:41 GMT  
		Size: 45.7 MB (45678639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea635c345e983ad2e59374f9ef5b34030ee1063a143d38b50f46060c270333b9`  
		Last Modified: Wed, 24 Jun 2026 01:15:50 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:a88c00afeb5787dd618af08996248ca6e9efd7b3c590dd52cb13b59b01629270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3159201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fa351a600687f26bf15a46f86a5cbc1d1d318e64b809509e0353abc5e2df9cc`

```dockerfile
```

-	Layers:
	-	`sha256:6bbaec63fb981eff7bb6b8c85ad6e90b86366ec0c392f20790015ed2b59ad944`  
		Last Modified: Wed, 24 Jun 2026 01:15:50 GMT  
		Size: 3.2 MB (3153036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e17277e5298e4ed3ba20b4728fcadea333bf37596c0db8b1bdfed0933c9131d9`  
		Last Modified: Wed, 24 Jun 2026 01:15:50 GMT  
		Size: 6.2 KB (6165 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:82bf71f64e9ded036badfed5c4366959ce5a8a6e1ba4461b5bc6a22a25289bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48799063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b406bce8bd5c154938475deb9bc9593937ca6516f466865ce6787faf73993b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'unstable' '@1782172800'
# Wed, 24 Jun 2026 01:15:22 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:191e338bd2713e3833739d14fb9446f4443dcab26ec38d74e9aff4b52cfc2148`  
		Last Modified: Wed, 24 Jun 2026 00:28:24 GMT  
		Size: 48.8 MB (48798843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ea215b64b3b553ea03ae64949f185860bb5846df831102d17a621852a34766`  
		Last Modified: Wed, 24 Jun 2026 01:15:28 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:a9930a2654ce1b36d960d7434eccae169d379a1aa68d1448bf60391ff4b288b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3162529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42fb6dc5f7be388107220b7216e5f06785fb6ae5b60a41dca1d29c77a1610ca1`

```dockerfile
```

-	Layers:
	-	`sha256:63672db1a299cddc5121869284ccba9161313679ec8feb6552cf3a5959a3d5d0`  
		Last Modified: Wed, 24 Jun 2026 01:15:29 GMT  
		Size: 3.2 MB (3156348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0f6ea31c39b72cd97fd4cabd7c26a9b0857f45762b1509fdc11af78138421c1`  
		Last Modified: Wed, 24 Jun 2026 01:15:28 GMT  
		Size: 6.2 KB (6181 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; 386

```console
$ docker pull debian@sha256:8866b9fcfe7f988fce7f8e5654afc896b0c75ee9b9b349c1d7cde051e7740e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50081183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b75e55ff70e2fe4d955f909f611b03b6592b707ff42567a3331bad1b7933c58`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'unstable' '@1782172800'
# Wed, 24 Jun 2026 01:15:32 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:bed0e6913ef7c7ed2ab16147605f7d539c9bceaa7c32bb8b2ead5e074741d2bd`  
		Last Modified: Wed, 24 Jun 2026 00:28:43 GMT  
		Size: 50.1 MB (50080962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91914a850def70437d0803fd792b7648ad19b439ab37dcf008eb3bab053c9e34`  
		Last Modified: Wed, 24 Jun 2026 01:15:38 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:3221cb256eb16c1b5918a70c4d73a40da5ffec745f9d84e32ef52859ced40906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3154944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff74e93bba584262fe089712e08af0e746050081976d6b9fd867794efb9b900`

```dockerfile
```

-	Layers:
	-	`sha256:fcc168c3cb9d1641e96e84ef7e6e0cf29798afd018d5bf83bdde96330c124951`  
		Last Modified: Wed, 24 Jun 2026 01:15:38 GMT  
		Size: 3.1 MB (3148865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87cbb4a9c93d74f7a059212555a479eef8feac94eed4a8023d55b173acce83c7`  
		Last Modified: Wed, 24 Jun 2026 01:15:38 GMT  
		Size: 6.1 KB (6079 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; ppc64le

```console
$ docker pull debian@sha256:1f40db0a107ca092a1ca302573d2657920910aa7b4cd1151ea5639df2a5f459c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54098205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:291f2f41a4f476a1efbe05a5ab46555c492692ef104c6c757fec22c0e296b342`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'unstable' '@1782172800'
# Wed, 24 Jun 2026 01:15:58 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:df0906e3cb637fbba0e983f5f83d8b95284187794c6fcd307923e2706e29c920`  
		Last Modified: Wed, 24 Jun 2026 00:31:03 GMT  
		Size: 54.1 MB (54097985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366d211411541eda782599897680c0ebe8042b2a8de5229ab7954e38c1771584`  
		Last Modified: Wed, 24 Jun 2026 01:16:11 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:d1ce40afed78f29517ce7618d22e42daac38dd1679f6b08b3634634b891cdb15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3161302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c778ec725c3f29c5212514b97c4d4cb50ef1ad616e56321d73ce0ae2f84d3e`

```dockerfile
```

-	Layers:
	-	`sha256:23ef88961c537bc392824d43b7bc35f4c267e216362a732155b31ddfac3e594f`  
		Last Modified: Wed, 24 Jun 2026 01:16:11 GMT  
		Size: 3.2 MB (3155169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc62e639c6b9fee6bbb0c010aefff4705a85d4f4b1878bec076d0ff36ebf903e`  
		Last Modified: Wed, 24 Jun 2026 01:16:11 GMT  
		Size: 6.1 KB (6133 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; riscv64

```console
$ docker pull debian@sha256:05b704c030753a75579db65f44950c8ef45d5604911416d281efc1cb42e52707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46898478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a6e885cecff7130690a50b8ac4567c1188d82ad7d878010473a48ad0753d546`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'unstable' '@1782172800'
# Wed, 24 Jun 2026 18:39:46 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:6b7601227df5b266f753a98126e9f052514747d83be2682008f432b63957e5ed`  
		Last Modified: Wed, 24 Jun 2026 03:43:42 GMT  
		Size: 46.9 MB (46898257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273b43c646528479d110363d56194ad61c18d56a5e3f0f64ecfbf7373129eb98`  
		Last Modified: Wed, 24 Jun 2026 18:40:40 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:25777288c978e54da2c6d38f4013ced9cfa1170c18e7c2d85a1c7f7a4cec3ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19ff39f89063a6f025110277f0602f33f6b9bfa72d64d2e7c7a8be820081498a`

```dockerfile
```

-	Layers:
	-	`sha256:30c6c52c00c1a7e48f59832e5e9d9dd63d6153ad5f8a6e667b01d11f412502d1`  
		Last Modified: Wed, 24 Jun 2026 18:40:44 GMT  
		Size: 3.1 MB (3143172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d297bd14a26d55c6ac64656731e8d3471f87167917831b02b7fa21b5a7b8dd50`  
		Last Modified: Wed, 24 Jun 2026 18:40:40 GMT  
		Size: 6.1 KB (6132 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental` - linux; s390x

```console
$ docker pull debian@sha256:f539a87e5ffc3fd25afc355af5107ff0c5e1e52f85747d7fa71a7a85623f457e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48518024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b303e50f37a85910f6a7aac7930812b71a7a10dcfe10f8bdd0c6f3b82cb713c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'unstable' '@1782172800'
# Wed, 24 Jun 2026 01:14:34 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:9d0a24e2e28b0d2f4b1099d1d9891107922d94e2cbcd230e7347b8eb742a5558`  
		Last Modified: Wed, 24 Jun 2026 00:28:47 GMT  
		Size: 48.5 MB (48517803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8dee08a47f52be7aaad8537b68398f610b26059f07e2b557ffea6828f505387`  
		Last Modified: Wed, 24 Jun 2026 01:14:45 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental` - unknown; unknown

```console
$ docker pull debian@sha256:ef33f2b21c86fd08a97845ce9817e2228e558c037f3c08658297cc6ac2c515f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3159218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef41666184a38fdb2e32d72cc9ed513194bccf2e5c958c9a71edac0f48b3275b`

```dockerfile
```

-	Layers:
	-	`sha256:57d0e78c73af40bc94cd66e94900189a2b742e9e044fd63cebe73dd0c7dd6b10`  
		Last Modified: Wed, 24 Jun 2026 01:14:45 GMT  
		Size: 3.2 MB (3153117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53547ea1c95939b7fd211217f55bb3c2eddbb703593f5e981468ccfc18532382`  
		Last Modified: Wed, 24 Jun 2026 01:14:45 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.in-toto+json
