<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `alt`

-	[`alt:latest`](#altlatest)
-	[`alt:p10`](#altp10)
-	[`alt:p11`](#altp11)
-	[`alt:sisyphus`](#altsisyphus)

## `alt:latest`

```console
$ docker pull alt@sha256:a32f2a8a3aaa0bde41263bbdf9fd23264fc846feb280f5adb961ab4f34e5f5c5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `alt:latest` - linux; amd64

```console
$ docker pull alt@sha256:c531cd4847b41d8d1a8ec3b4d3a50dc5e77701eed43fdc920b99c1da7e2ecaf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46128310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c8ea9cc3fa1f105f9fb0de319e94ed933ed44d2989ab33388da6d8ae3c0315`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Oct 2025 08:07:04 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Wed, 08 Oct 2025 08:07:04 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Wed, 08 Oct 2025 08:07:04 GMT
ADD alt-p11-x86_64.tar.xz / # buildkit
# Wed, 08 Oct 2025 08:07:04 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Wed, 08 Oct 2025 08:07:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d96357fefe31612c78d6a92d165931ef1124fbbd5ec027261469aca6396fde78`  
		Last Modified: Wed, 08 Oct 2025 17:48:59 GMT  
		Size: 46.1 MB (46128119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62dd7807dca6da990ca673c2ea95c935cf9e5e0084d0b17d95eb53138f09a3d2`  
		Last Modified: Sun, 07 Dec 2025 17:56:36 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:latest` - unknown; unknown

```console
$ docker pull alt@sha256:0153aac345a18e3147e2bf94481039965713c3d467e5fb066f069250f8613f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2603009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af5a89abbb7d0f390c34c6d55dff2310a9b005b3832479b90fbac599ef758918`

```dockerfile
```

-	Layers:
	-	`sha256:71c53261a087d7395439ce644be9ef8d46527928fe6e1dbbe50762074d645a1a`  
		Last Modified: Wed, 08 Oct 2025 17:48:58 GMT  
		Size: 2.6 MB (2596595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c50711920d93f04c093124fe9b614cfc12393ce0d0c01e6d44784c69ea93baa5`  
		Last Modified: Tue, 09 Dec 2025 09:01:11 GMT  
		Size: 6.4 KB (6414 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:latest` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:4cdbbef2a9658b82d50a9276519199f81e6dfea58ad319813375439fa43b3f8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44868440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e36874cc878ef8ecdde980dc9805fc6eee02f70cb70d798bbef9ea82cde1e9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Oct 2025 08:07:04 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Wed, 08 Oct 2025 08:07:04 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Wed, 08 Oct 2025 08:07:04 GMT
ADD alt-p11-aarch64.tar.xz / # buildkit
# Wed, 08 Oct 2025 08:07:04 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Wed, 08 Oct 2025 08:07:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0da08a336324d0a4553aeaf55b0433bf25d5c712f1422d27577d898b87211b01`  
		Last Modified: Wed, 08 Oct 2025 17:50:14 GMT  
		Size: 44.9 MB (44868249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b17e29e80e459b5365c7f85d552bcf4f4379ae02ea764ce82526abbefe3a697`  
		Last Modified: Mon, 08 Dec 2025 08:43:01 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:latest` - unknown; unknown

```console
$ docker pull alt@sha256:d2a2267f33071e1bab402ab81682d68be01d934acf7392ef2c221f5703333c8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2602500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:325c7a962f125a4c8a1078956e89c5ae5733e8fa4d7f3a16d00cb443bfa9ebcb`

```dockerfile
```

-	Layers:
	-	`sha256:7957d889c5fe800102cf7dccd26b0b50feac3f029b7154c86a3506936176e1ef`  
		Last Modified: Tue, 09 Dec 2025 09:01:13 GMT  
		Size: 2.6 MB (2596024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2669596d2960c435c3306e8d842678d11618bebe3ef74d34c59cb7b53ec971e`  
		Last Modified: Tue, 09 Dec 2025 09:01:11 GMT  
		Size: 6.5 KB (6476 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:latest` - linux; 386

```console
$ docker pull alt@sha256:1b4c9b8702abeb38a0477b6e6e7e71113d9ad5de701494ae580151f8b1b1f97d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46158713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bdca72282b226b4d7b4f2883c6bbdeaf577da3a28c40f41d01acfd1f1660393`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Oct 2025 08:07:04 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Wed, 08 Oct 2025 08:07:04 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Wed, 08 Oct 2025 08:07:04 GMT
ADD alt-p11-i586.tar.xz / # buildkit
# Wed, 08 Oct 2025 08:07:04 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Wed, 08 Oct 2025 08:07:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:586aa7572cc32e39fefac3ad917314f6bd305dc2f183091cb89681d81d34af50`  
		Last Modified: Tue, 09 Dec 2025 09:01:31 GMT  
		Size: 46.2 MB (46158521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238bc14ebda4d4fbd69c75bd3f66627f5d77db534fc80731a704bd19feb6b086`  
		Last Modified: Wed, 08 Oct 2025 17:50:21 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:latest` - unknown; unknown

```console
$ docker pull alt@sha256:64bf98af4281495f5e2510eea685eeba3eeeb2530c11e566521b47961e4f2b8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2601707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc360762205fab597c3a8e38ca78cb8a7bc9bec71e7701e1fb321aa7c6fb7d1`

```dockerfile
```

-	Layers:
	-	`sha256:d8bd65100d4d58a17012fcdc685de672c1115dee6831ed13c5cb13591bb24566`  
		Last Modified: Tue, 09 Dec 2025 09:01:17 GMT  
		Size: 2.6 MB (2595316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33504082609e76e0dd204cfae139fbdde918a7b6b82b66cf79da6daf049154cb`  
		Last Modified: Tue, 09 Dec 2025 09:01:19 GMT  
		Size: 6.4 KB (6391 bytes)  
		MIME: application/vnd.in-toto+json

## `alt:p10`

```console
$ docker pull alt@sha256:49706c0ee9eb0fe1870cd7e1839d041fe24259bd8dc13a6c63923b3b30908aa6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `alt:p10` - linux; amd64

```console
$ docker pull alt@sha256:8397a3981aec0a4b2c4de8574645ae3761a227a95bd18a1a1a3fa78ad9f3003b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47433019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a8cec37b1a93389a6318b475ce11f9e8365f3c47063b75c41e6d3e13fbd825`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Oct 2025 08:06:39 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Wed, 08 Oct 2025 08:06:39 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Wed, 08 Oct 2025 08:06:39 GMT
ADD alt-p10-x86_64.tar.xz / # buildkit
# Wed, 08 Oct 2025 08:06:39 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Wed, 08 Oct 2025 08:06:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:5379df2a135565cefeaf1ad63845c1404287727d259ae3e2eccdea7c21efa65a`  
		Last Modified: Wed, 08 Oct 2025 17:48:08 GMT  
		Size: 47.4 MB (47432828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8fa3f54f75d4bdd53dc8886ff47e548a02eef5311326fcdf7eb01e7d0060e30`  
		Last Modified: Wed, 08 Oct 2025 17:48:06 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:p10` - unknown; unknown

```console
$ docker pull alt@sha256:07fc9248a61dfb42804903e471b28d5d6aacf1e287d93f9715431b4253921ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2602870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab379bb3dfae0d30287accfe10fa5da325e5c910194ff2c49856e4e39368b710`

```dockerfile
```

-	Layers:
	-	`sha256:e43567c73e9983fc0acb9d91053d4a714a781228999c01dc88c33bc50ac4c2b0`  
		Last Modified: Tue, 09 Dec 2025 09:01:37 GMT  
		Size: 2.6 MB (2596750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8167b0556ba52b17024bf61c1a10e4842a938818e961f3ad55a0fd6336dd644a`  
		Last Modified: Tue, 09 Dec 2025 09:01:36 GMT  
		Size: 6.1 KB (6120 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:p10` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:4c0315fec7fef895408e2c3a554626b9eb9637f28ad690b2792423216ffd5ec0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46604992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:101d8187377deff3662d3e09fcb7dd74a3740dd64b8c6c85cd7b7845a4cbfa5a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Oct 2025 08:06:39 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Wed, 08 Oct 2025 08:06:39 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Wed, 08 Oct 2025 08:06:39 GMT
ADD alt-p10-aarch64.tar.xz / # buildkit
# Wed, 08 Oct 2025 08:06:39 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Wed, 08 Oct 2025 08:06:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b5ffa4d2a440d5d41625aae108edc255de09d88caa35fd69020ee542a953d283`  
		Last Modified: Wed, 08 Oct 2025 17:49:12 GMT  
		Size: 46.6 MB (46604802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b312a296cb392bf337401884ded3568eb254d9d84b94397e40d92cff260bd8`  
		Last Modified: Mon, 08 Dec 2025 13:13:14 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:p10` - unknown; unknown

```console
$ docker pull alt@sha256:34eab97f8a5c914d2ba814b96543957fc231f42bf850d8e6d01cdb9f867cbc82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2601563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06060dda0af10d13d6743ea7cbac49a268aaf7ac06354b66ccb055b153e3445`

```dockerfile
```

-	Layers:
	-	`sha256:8e097425beadddb45a46445330a56713e14b4b39954d752cc233cb36ef9da18b`  
		Last Modified: Tue, 09 Dec 2025 09:01:37 GMT  
		Size: 2.6 MB (2595391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1417b98060518fd2cc0ecf151bb7342a7b2fe0860e7081357e29c1ba65e9f84d`  
		Last Modified: Tue, 09 Dec 2025 09:01:36 GMT  
		Size: 6.2 KB (6172 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:p10` - linux; 386

```console
$ docker pull alt@sha256:2eca87190beaa0ae87022cc1cb0618485780b13a93c66aad69f01b94afcd1f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48200480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e9dc21ae5eb3c26afc395ee7d200a4b82818969db370bd90070c26a906c465a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Oct 2025 08:06:39 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Wed, 08 Oct 2025 08:06:39 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Wed, 08 Oct 2025 08:06:39 GMT
ADD alt-p10-i586.tar.xz / # buildkit
# Wed, 08 Oct 2025 08:06:39 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Wed, 08 Oct 2025 08:06:39 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b52cfb3be8a5d874a52e9a9e940bc9268e64a9c8a430fb27a011ed051603ddd0`  
		Last Modified: Tue, 09 Dec 2025 09:01:57 GMT  
		Size: 48.2 MB (48200288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0211cd3afdc4b059f4da6ec5b974df501cae7cd08ad5e6de2f31ec4f2c5f4c42`  
		Last Modified: Tue, 09 Dec 2025 09:01:40 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:p10` - unknown; unknown

```console
$ docker pull alt@sha256:8022ecbece004066b075b0ed4a9fcdda81c57dfc5db1f672670e3663043567e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2604702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec898f37f128f77926c1ab7e58e61b951ab93ba4a1b20dfdc7aebbe960d0a78`

```dockerfile
```

-	Layers:
	-	`sha256:2fca9f9378b6663a9a787374488a5e6dacf549e4f2f6be4dfbf86f7781e4c3f1`  
		Last Modified: Tue, 09 Dec 2025 09:01:42 GMT  
		Size: 2.6 MB (2598598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e346d0586e9af82a6d2b4772d1fa13b32c972ec9992cfa9d2b1f64dc78bfa5dc`  
		Last Modified: Tue, 09 Dec 2025 09:01:40 GMT  
		Size: 6.1 KB (6104 bytes)  
		MIME: application/vnd.in-toto+json

## `alt:p11`

```console
$ docker pull alt@sha256:a32f2a8a3aaa0bde41263bbdf9fd23264fc846feb280f5adb961ab4f34e5f5c5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `alt:p11` - linux; amd64

```console
$ docker pull alt@sha256:c531cd4847b41d8d1a8ec3b4d3a50dc5e77701eed43fdc920b99c1da7e2ecaf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46128310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c8ea9cc3fa1f105f9fb0de319e94ed933ed44d2989ab33388da6d8ae3c0315`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Oct 2025 08:07:04 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Wed, 08 Oct 2025 08:07:04 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Wed, 08 Oct 2025 08:07:04 GMT
ADD alt-p11-x86_64.tar.xz / # buildkit
# Wed, 08 Oct 2025 08:07:04 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Wed, 08 Oct 2025 08:07:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d96357fefe31612c78d6a92d165931ef1124fbbd5ec027261469aca6396fde78`  
		Last Modified: Wed, 08 Oct 2025 17:48:59 GMT  
		Size: 46.1 MB (46128119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62dd7807dca6da990ca673c2ea95c935cf9e5e0084d0b17d95eb53138f09a3d2`  
		Last Modified: Sun, 07 Dec 2025 17:56:36 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:p11` - unknown; unknown

```console
$ docker pull alt@sha256:0153aac345a18e3147e2bf94481039965713c3d467e5fb066f069250f8613f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2603009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af5a89abbb7d0f390c34c6d55dff2310a9b005b3832479b90fbac599ef758918`

```dockerfile
```

-	Layers:
	-	`sha256:71c53261a087d7395439ce644be9ef8d46527928fe6e1dbbe50762074d645a1a`  
		Last Modified: Wed, 08 Oct 2025 17:48:58 GMT  
		Size: 2.6 MB (2596595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c50711920d93f04c093124fe9b614cfc12393ce0d0c01e6d44784c69ea93baa5`  
		Last Modified: Tue, 09 Dec 2025 09:01:11 GMT  
		Size: 6.4 KB (6414 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:p11` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:4cdbbef2a9658b82d50a9276519199f81e6dfea58ad319813375439fa43b3f8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44868440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e36874cc878ef8ecdde980dc9805fc6eee02f70cb70d798bbef9ea82cde1e9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Oct 2025 08:07:04 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Wed, 08 Oct 2025 08:07:04 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Wed, 08 Oct 2025 08:07:04 GMT
ADD alt-p11-aarch64.tar.xz / # buildkit
# Wed, 08 Oct 2025 08:07:04 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Wed, 08 Oct 2025 08:07:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:0da08a336324d0a4553aeaf55b0433bf25d5c712f1422d27577d898b87211b01`  
		Last Modified: Wed, 08 Oct 2025 17:50:14 GMT  
		Size: 44.9 MB (44868249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b17e29e80e459b5365c7f85d552bcf4f4379ae02ea764ce82526abbefe3a697`  
		Last Modified: Mon, 08 Dec 2025 08:43:01 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:p11` - unknown; unknown

```console
$ docker pull alt@sha256:d2a2267f33071e1bab402ab81682d68be01d934acf7392ef2c221f5703333c8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2602500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:325c7a962f125a4c8a1078956e89c5ae5733e8fa4d7f3a16d00cb443bfa9ebcb`

```dockerfile
```

-	Layers:
	-	`sha256:7957d889c5fe800102cf7dccd26b0b50feac3f029b7154c86a3506936176e1ef`  
		Last Modified: Tue, 09 Dec 2025 09:01:13 GMT  
		Size: 2.6 MB (2596024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2669596d2960c435c3306e8d842678d11618bebe3ef74d34c59cb7b53ec971e`  
		Last Modified: Tue, 09 Dec 2025 09:01:11 GMT  
		Size: 6.5 KB (6476 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:p11` - linux; 386

```console
$ docker pull alt@sha256:1b4c9b8702abeb38a0477b6e6e7e71113d9ad5de701494ae580151f8b1b1f97d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46158713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bdca72282b226b4d7b4f2883c6bbdeaf577da3a28c40f41d01acfd1f1660393`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Oct 2025 08:07:04 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Wed, 08 Oct 2025 08:07:04 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Wed, 08 Oct 2025 08:07:04 GMT
ADD alt-p11-i586.tar.xz / # buildkit
# Wed, 08 Oct 2025 08:07:04 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Wed, 08 Oct 2025 08:07:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:586aa7572cc32e39fefac3ad917314f6bd305dc2f183091cb89681d81d34af50`  
		Last Modified: Tue, 09 Dec 2025 09:01:31 GMT  
		Size: 46.2 MB (46158521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238bc14ebda4d4fbd69c75bd3f66627f5d77db534fc80731a704bd19feb6b086`  
		Last Modified: Wed, 08 Oct 2025 17:50:21 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:p11` - unknown; unknown

```console
$ docker pull alt@sha256:64bf98af4281495f5e2510eea685eeba3eeeb2530c11e566521b47961e4f2b8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2601707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc360762205fab597c3a8e38ca78cb8a7bc9bec71e7701e1fb321aa7c6fb7d1`

```dockerfile
```

-	Layers:
	-	`sha256:d8bd65100d4d58a17012fcdc685de672c1115dee6831ed13c5cb13591bb24566`  
		Last Modified: Tue, 09 Dec 2025 09:01:17 GMT  
		Size: 2.6 MB (2595316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33504082609e76e0dd204cfae139fbdde918a7b6b82b66cf79da6daf049154cb`  
		Last Modified: Tue, 09 Dec 2025 09:01:19 GMT  
		Size: 6.4 KB (6391 bytes)  
		MIME: application/vnd.in-toto+json

## `alt:sisyphus`

```console
$ docker pull alt@sha256:795149fec5d9f6b9954253186637701ac139940f500631dc31a2973a2b7887cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown

### `alt:sisyphus` - linux; amd64

```console
$ docker pull alt@sha256:77a000e8902c9f8c3d75abbbd6ad4b37b883cf4aa54bf9bef325e55a130e5cf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46469371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b70dbc38fc028dbea704537c07b43eaf64ec00dcbf1182261fef04eaac5d00`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Oct 2025 08:06:13 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Wed, 08 Oct 2025 08:06:13 GMT
LABEL org.opencontainers.image.licenses=GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Wed, 08 Oct 2025 08:06:13 GMT
ADD alt-sisyphus-x86_64.tar.xz / # buildkit
# Wed, 08 Oct 2025 08:06:13 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Wed, 08 Oct 2025 08:06:13 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4f513c4ecc36e21844fbde3bcfbd3c50ea06b2db3202d2c77ef5b09a56c45f45`  
		Last Modified: Wed, 08 Oct 2025 17:48:34 GMT  
		Size: 46.5 MB (46469180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b7edb8fa05c9eab302cf5e23d72da00078a158045945c7cd91e4e7416291b7`  
		Last Modified: Wed, 08 Oct 2025 17:48:32 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:sisyphus` - unknown; unknown

```console
$ docker pull alt@sha256:bb3b9cf89c64a1e19ee1ef0be2fab76dd48dddfc4f20afe6a0dae7db911a63fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2608690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:229ffa9dd985feeb1e66fa2d73f306de2c73d3fad70b543ad3001654771f1d72`

```dockerfile
```

-	Layers:
	-	`sha256:3cde3df9f006a3fd1eefd7fc6f85e56ca276972de230b5b61b330dffd69d2b35`  
		Last Modified: Wed, 08 Oct 2025 17:48:32 GMT  
		Size: 2.6 MB (2602569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb8505a978441d22f7e3629438d4a154af8b3bf1be2280558f7438eb60a1eac6`  
		Last Modified: Wed, 08 Oct 2025 17:48:31 GMT  
		Size: 6.1 KB (6121 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:sisyphus` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:60d50b2c54e05daf67f835942e126c007da0fb8e14e5bbf260d7be80d0e3b043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45185712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f00d6e285e3a09cf21f8fdd17ee6ed228f3b77520e1ba2936efef1be9d962f70`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Oct 2025 08:06:13 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Wed, 08 Oct 2025 08:06:13 GMT
LABEL org.opencontainers.image.licenses=GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Wed, 08 Oct 2025 08:06:13 GMT
ADD alt-sisyphus-aarch64.tar.xz / # buildkit
# Wed, 08 Oct 2025 08:06:13 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Wed, 08 Oct 2025 08:06:13 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:cedd18aa944a350d23a6e34e3fcfb2e5b69cd20745359ef1415d91960be7bf9a`  
		Last Modified: Tue, 09 Dec 2025 10:31:42 GMT  
		Size: 45.2 MB (45185520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553855a2ee49253f73b882384a77f84ee3e9c668e6fb4ef912495897fe37095e`  
		Last Modified: Wed, 08 Oct 2025 17:49:36 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:sisyphus` - unknown; unknown

```console
$ docker pull alt@sha256:c792cc11a2c79c4768072719b2a88b15341ebaa8a9d590d0b8d93f832fe24dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2608156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4873df1c448874a592957692f7c2864882758d3c6149992c13529bad8dada3b`

```dockerfile
```

-	Layers:
	-	`sha256:3c03a5cd79ad6dbebc6f94f2a3e0a10cd78df05b95bea96f8a48a0ab2a1099a8`  
		Last Modified: Wed, 08 Oct 2025 17:49:36 GMT  
		Size: 2.6 MB (2601986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d895d69ba773b49da197487434aff12ceeefc0d0ad1108d14c7c5f756b0b6cda`  
		Last Modified: Mon, 05 Jan 2026 19:02:50 GMT  
		Size: 6.2 KB (6170 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:sisyphus` - linux; 386

```console
$ docker pull alt@sha256:ad98bac0de89bf408d9ac39eb1914b3f22a7ca28904d829d52f5ae7bd0eb0749
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46527938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:619076fa57501e47dc73371a70868c59b694d902415e75ca8086a81a45f9c333`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Oct 2025 08:06:13 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Wed, 08 Oct 2025 08:06:13 GMT
LABEL org.opencontainers.image.licenses=GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Wed, 08 Oct 2025 08:06:13 GMT
ADD alt-sisyphus-i586.tar.xz / # buildkit
# Wed, 08 Oct 2025 08:06:13 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Wed, 08 Oct 2025 08:06:13 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:43535e6c39e4cabbb688b13d91224413dc1e74e3c6d355b52f3e42f22507762f`  
		Last Modified: Tue, 09 Dec 2025 22:33:03 GMT  
		Size: 46.5 MB (46527749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b216f60e037e2f6bc29f2ca93ceca28bbde8d938c5151b8b8f8f20cf4a6a62f4`  
		Last Modified: Tue, 09 Dec 2025 22:32:55 GMT  
		Size: 189.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:sisyphus` - unknown; unknown

```console
$ docker pull alt@sha256:2843779fb1a234771f92b21b7ea352224e0eb696d78a0876d68dfd134e383436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2607398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc79be584afaf18601b0c8e81ba57a9b8e62e0ea315b88566cc005c442f97022`

```dockerfile
```

-	Layers:
	-	`sha256:12432b238525a2a810dc9b586a0afb6be5207d98e47f6a54d860027d96336cec`  
		Last Modified: Wed, 08 Oct 2025 17:49:20 GMT  
		Size: 2.6 MB (2601295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72aba750bb6462186a3e3b98d155565710626a2fb79436f3b80fb0b794385f8d`  
		Last Modified: Wed, 08 Oct 2025 17:49:20 GMT  
		Size: 6.1 KB (6103 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:sisyphus` - linux; riscv64

```console
$ docker pull alt@sha256:845066cd98a8169c886c961b50de8c659d67ab43219a06d1195ad4325537ec1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.4 MB (44408217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:344fc85c860d7ec929e02552c2f1943d3109ca2cffbc76b20ebe97045dea013e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 08 Oct 2025 08:06:13 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Wed, 08 Oct 2025 08:06:13 GMT
LABEL org.opencontainers.image.licenses=GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Wed, 08 Oct 2025 08:06:13 GMT
ADD alt-sisyphus-riscv64.tar.xz / # buildkit
# Wed, 08 Oct 2025 08:06:13 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Wed, 08 Oct 2025 08:06:13 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:280d9ae7e606ab73553e2c47a618735393ef3df6074ce94a34564388acbd0aab`  
		Last Modified: Sat, 17 Jan 2026 10:48:52 GMT  
		Size: 44.4 MB (44408025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f6cc3a42dd3440224bfa9fdf4c40890ba83d704734dce236a1bd0a28ebc6c8`  
		Last Modified: Wed, 08 Oct 2025 17:50:35 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:sisyphus` - unknown; unknown

```console
$ docker pull alt@sha256:4c4586202d185c3dc1ef2c59b44f202186bcdf3bd142170f300d8ce4a7e5cabc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2607382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ec87cfe1a950a797b9188e5076776e80a8e150d0be548c7a004cf86d623d5c`

```dockerfile
```

-	Layers:
	-	`sha256:f7bfdc636b2df6a9b21f5a841728c7fc38e2837b0373a0258f0194e84a8428ea`  
		Last Modified: Sat, 17 Jan 2026 10:48:31 GMT  
		Size: 2.6 MB (2601237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1442934513b0dff1f98ab9a1e4883d3be0c1bae1934aa7307f92006ea710eb3c`  
		Last Modified: Sat, 17 Jan 2026 10:48:29 GMT  
		Size: 6.1 KB (6145 bytes)  
		MIME: application/vnd.in-toto+json
