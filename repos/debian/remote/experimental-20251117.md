## `debian:experimental-20251117`

```console
$ docker pull debian@sha256:7ca3acea04aefb13c9583abf32b809ca9679cfc67ef1cf122f626abb4aa7bb90
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `debian:experimental-20251117` - linux; amd64

```console
$ docker pull debian@sha256:481c2381076f7fbc28b8154460d9a4389b88d1e91f66495e3ab1411391915aab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48500653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7057494b78e9f3db0f9a1e3fe683b241a90228c55846d31d58674399a72d2e1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'unstable' '@1763337600'
# Tue, 18 Nov 2025 03:59:36 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:ebb6f524ed90adde54a9f4d17444ac19cd8f6184737db36990502d24f6238972`  
		Last Modified: Tue, 18 Nov 2025 02:35:55 GMT  
		Size: 48.5 MB (48500432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ccc067607cd76c584dbaa4ef627533f2bcce35f92651ff256a68f19cc6b150`  
		Last Modified: Tue, 18 Nov 2025 03:59:52 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20251117` - unknown; unknown

```console
$ docker pull debian@sha256:2a8beb169a3123dc6c19229974b0a2532d832d5f53b2d9c5e1fe742657a55af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3135956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82bdb1c2afc61acd2e9b02c8c4451079aaf9dec8ff31899732b274c6c1fab54e`

```dockerfile
```

-	Layers:
	-	`sha256:cee8df0246fbde5e76dd4f6a62c57af59fb3a04b90b097a4088602b37be53968`  
		Last Modified: Tue, 18 Nov 2025 04:27:20 GMT  
		Size: 3.1 MB (3129855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b5435e491393e04f3a6f5409749623796c650ad0bb9ed303e88538caba882f5`  
		Last Modified: Tue, 18 Nov 2025 04:27:20 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20251117` - linux; arm variant v7

```console
$ docker pull debian@sha256:3b7672a7f71f55844cd0d0b151f833c13e8ba6e27ff55b871fe42e5cab572321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45003917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e34a74c882c6d2d23b0847bcc8f0540a63f1d4acf22bd1537ea9dc677369a81a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'unstable' '@1763337600'
# Tue, 18 Nov 2025 02:21:23 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:267f833a73e131fd8684b2bcc92d07db850ee3f961510fbde8708183a89efa81`  
		Last Modified: Tue, 18 Nov 2025 01:14:28 GMT  
		Size: 45.0 MB (45003696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b707b8b8ba9b9da4774a93994791f11a7548041913d281664b868caa825292`  
		Last Modified: Tue, 18 Nov 2025 02:21:35 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20251117` - unknown; unknown

```console
$ docker pull debian@sha256:e347b8fced6008b5cf859302544e1ce4a545c945abd7b0d11367c086c78020d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3137396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b26a28af67921dc141f7131d3b13c5ac8d4f498b29a727688dc6835c5c5c4e6d`

```dockerfile
```

-	Layers:
	-	`sha256:f71f1443628358441bc2b0b98e898f66aebfcd9c3ddf92b1dfbcfe8c8cb939fb`  
		Last Modified: Tue, 18 Nov 2025 04:27:24 GMT  
		Size: 3.1 MB (3131231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e997d465fefe48dfcf4e3dd400e7ac8ff2d544e963dc93f1893ca9c392e0367`  
		Last Modified: Tue, 18 Nov 2025 04:27:25 GMT  
		Size: 6.2 KB (6165 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20251117` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:053d93011560761be03b02a9765305e1bebe25fd61984c1d7506d4d11647f31d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48591615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dd43431e8bcf8a545772bf64af88f0e8bec8d75aad35bbfbdd0842f3de00ca5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'unstable' '@1763337600'
# Tue, 18 Nov 2025 02:16:28 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:7129e03ffe07f11f37ee21420d1c496c52179a0e3d41a9ee36ecb84b95d53e2d`  
		Last Modified: Tue, 18 Nov 2025 01:13:36 GMT  
		Size: 48.6 MB (48591394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef38101a174d844502d6a433266881a45ffaf8d57cef1bb285fb865a1868c2d3`  
		Last Modified: Tue, 18 Nov 2025 02:16:39 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20251117` - unknown; unknown

```console
$ docker pull debian@sha256:38bf93fbae55ef1e8872e5845146f8a40fe0a249138efe20d60a2c5637ace435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3136889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aba5ae357f693a794e70fbe55255b85d982bfb9cb6a2261e4a68cd3a928b0477`

```dockerfile
```

-	Layers:
	-	`sha256:c6dd6863f50750f87d79378b2200c1385bd677dd4fd2a8bac058afb1fd513883`  
		Last Modified: Tue, 18 Nov 2025 04:27:29 GMT  
		Size: 3.1 MB (3130708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:881ef6c52deb03219b76bdc2b8b7612b25be0b0d6a615837c68c2d5952cf71f8`  
		Last Modified: Tue, 18 Nov 2025 04:27:30 GMT  
		Size: 6.2 KB (6181 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20251117` - linux; 386

```console
$ docker pull debian@sha256:5a553dde395b275d60bb86b4347ea744516e95397f9771518ee9591466487e8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49833387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb39015814d30c2a198e034e28701188c483694791d0497d2f91af20b63b5804`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'unstable' '@1763337600'
# Tue, 18 Nov 2025 02:15:59 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:0379926ee4324d150add0261c7fcc7dff6964018399d8ebddb75c52ee1c27b9e`  
		Last Modified: Tue, 18 Nov 2025 01:13:54 GMT  
		Size: 49.8 MB (49833166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24609ec8cf63ea6c8c833a72ca5c50f2ec8261bb4bddf99715932722fdf4091`  
		Last Modified: Tue, 18 Nov 2025 02:16:11 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20251117` - unknown; unknown

```console
$ docker pull debian@sha256:565bb508137f2fead40a02a04c534795332e95f08213a8222a44ca7199bd4f1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3133138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaedd3eb23ac1f8e18bb0f93eaf80000292a0271ce47b0a9aba6952b49e208c2`

```dockerfile
```

-	Layers:
	-	`sha256:41362f214e74b11573810bff0a51ab38c9f5d5440a2261687d297a53c5392749`  
		Last Modified: Tue, 18 Nov 2025 04:27:33 GMT  
		Size: 3.1 MB (3127059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8df8d3461e49f87252857e22acb289e6bbb55b9724c39115fd5c3fa86d94c30c`  
		Last Modified: Tue, 18 Nov 2025 04:27:34 GMT  
		Size: 6.1 KB (6079 bytes)  
		MIME: application/vnd.in-toto+json
