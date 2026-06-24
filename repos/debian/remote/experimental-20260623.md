## `debian:experimental-20260623`

```console
$ docker pull debian@sha256:1db70adbff6d82926408bcffed91f98a150315b97aa8a051de3692ca3681a7d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:experimental-20260623` - linux; 386

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

### `debian:experimental-20260623` - unknown; unknown

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

### `debian:experimental-20260623` - linux; ppc64le

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

### `debian:experimental-20260623` - unknown; unknown

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

### `debian:experimental-20260623` - linux; s390x

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

### `debian:experimental-20260623` - unknown; unknown

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
