## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:7c492f13cb90976c7f8dd0d93ce469f70079395f44e5f4893f393e2a25a57149
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

### `debian:bullseye-backports` - linux; amd64

```console
$ docker pull debian@sha256:87f5c61c5f59ae6c592b9545e11ab18412014bac426b8fa6e2195b0cef08a1fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53739099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd3ccedb6758db3eacac7496bf35b27986ba60b6c6f04b2007d56fc1bd0241d4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Mon, 03 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:478cb73646107d7b3f891aa53abaed926667463844c07b1d924bd760ae03f38a`  
		Last Modified: Tue, 04 Feb 2025 04:23:03 GMT  
		Size: 53.7 MB (53738873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05976c607ddbdb2b0af034e077cd4d5dabfee4676fbf2d4c2b327b178d04b6bd`  
		Last Modified: Wed, 05 Feb 2025 03:08:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:008e985d78d1081d9bd5bdd3ebd70e07601aeb55c72067883c4bd56a033b274a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3923363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eafc2e6c3dd87d20016bd8e002c57fe47e64ea9c0efd015138a31183295ed10`

```dockerfile
```

-	Layers:
	-	`sha256:b48c1339f7c1a7baf356c2528409c60b1cfc1ea2fc34c591d9945052830610b3`  
		Last Modified: Fri, 21 Feb 2025 00:10:23 GMT  
		Size: 3.9 MB (3917516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c60eeffc84232a5452f05061cb9e0b638b7e7b4237569adac34d4374079c4f0`  
		Last Modified: Fri, 21 Feb 2025 00:10:25 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:54e1692018237bda19f02d8c2266dfdcb6de4ee5318919933b3973845d2315ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49025018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4fdf44b58dbdae9ebb04f155a79b769dfa0f54fadffd523a989e513551387e7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1738540800'
# Mon, 03 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7dafa8b67e9b20318af5959237616a556f517d3359b4cec5bc2b6899a7c8336b`  
		Last Modified: Tue, 04 Feb 2025 04:34:07 GMT  
		Size: 49.0 MB (49024794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851f5317130855db2b6a4ffccffe5a74ad49d902a7f7d501e2f7d2a295165d13`  
		Last Modified: Mon, 10 Feb 2025 13:05:35 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8a414992249074ca6f5c2a3f7581db676e6537b84c826bbf6ea1589ba034c163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3924977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b9c74681c52b20e867c9547bf349397f78dc47b12b6e3f0a943f64b23d7184`

```dockerfile
```

-	Layers:
	-	`sha256:79447fcdc0d4e38427375040f0bdb0ba9456aed64ecb7ef9881f5db51f7a52c6`  
		Last Modified: Fri, 21 Feb 2025 00:10:23 GMT  
		Size: 3.9 MB (3919078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:537a8442fdde76be2acd2355714169f0e0d65adad2a7fdb04704d6d7cb9f5388`  
		Last Modified: Fri, 21 Feb 2025 00:10:24 GMT  
		Size: 5.9 KB (5899 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:c54847e6a4e7f83792770f2a523fa6a40ecb0865b606275dc1e70241b930e824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52245920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66bfeb2a486365f04645c50b14aab6d4062e40c1db829b2ba5684079af40077`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Mon, 03 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0038ef039a89ede34c57806e684dc9d9be7dcd22d3c08b90deb36bb22a2c7122`  
		Last Modified: Tue, 04 Feb 2025 04:34:59 GMT  
		Size: 52.2 MB (52245695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5780ecdff0eab4eed257ba2aec0e1fb40af208655b1879904b04ddc1e4154de`  
		Last Modified: Wed, 05 Feb 2025 13:08:26 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:89244c1c8ca911d00d1f2acfba6a6f9f1d067588fc8f492d49c061ad5c26e772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3923011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c033d8afe8328077e06033991f040dc6ea243fc65c2049201b59338f06f19ed`

```dockerfile
```

-	Layers:
	-	`sha256:4423241d43dd768929e3989a413aaa273e22618507e3a9a3f67700e71379785b`  
		Last Modified: Fri, 21 Feb 2025 00:10:31 GMT  
		Size: 3.9 MB (3917096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c1967d7af96c6688e2564eee95a89668e9b438ac5d90de1d364577164d07c0c`  
		Last Modified: Fri, 21 Feb 2025 00:10:30 GMT  
		Size: 5.9 KB (5915 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:72d49568cfb74b2c4f91e1c5a5066e3eb475181e6c4e5dac433cd00cc1474a7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54676182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7805f3dfcd03ba8319ec4b489bf62a42495b2226720343e426d7efb80d22477e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1738540800'
# Mon, 03 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c2b5327eac1fcd49233dc8f6e5417e7e2efeea16edfcbff9dd025f389e15b11e`  
		Last Modified: Tue, 04 Feb 2025 05:01:41 GMT  
		Size: 54.7 MB (54675956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbd350b4fc944ce6f68f4e22f314cfc6cbbd4af26e73cc1a592b86e080f4d7e`  
		Last Modified: Tue, 04 Feb 2025 13:34:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8ced4bb7a057420c2ac504d2d9eb183dbebe8b71445b45b157e11170537b2876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3919852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5ad560ed07e33b6f729743c0c784660f7259b3334102a68f4c02c5b4c8bc2ab`

```dockerfile
```

-	Layers:
	-	`sha256:3b1f98f2d55fa15623e663fac1fda36dc9bffe1fa40b4b1e269f92f581e5f43a`  
		Last Modified: Fri, 21 Feb 2025 00:10:24 GMT  
		Size: 3.9 MB (3914023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f3fdac979fe438c20479d716d5cab842e4f9c878c37b46fc1afc30c59e57fc3`  
		Last Modified: Fri, 21 Feb 2025 00:10:25 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.in-toto+json
