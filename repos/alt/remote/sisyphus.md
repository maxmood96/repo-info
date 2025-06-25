## `alt:sisyphus`

```console
$ docker pull alt@sha256:e93b84a9c93db9c5bc4f491742b8eb7d85f3ac75c1d0b5bdc2a9082dac32f4e4
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
$ docker pull alt@sha256:6227c8403553c5c78b680edf62b495612385b3c15d53c2af0182333fe59cbf61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46199050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a0ddaeab7f3098d8f126e2c47eff6edea31b3ba38b18d470680232f598ab99`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Jun 2025 09:58:45 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Wed, 25 Jun 2025 09:58:45 GMT
LABEL org.opencontainers.image.licenses=GPLv3
# Wed, 25 Jun 2025 09:58:45 GMT
ADD alt-sisyphus-x86_64.tar.xz / # buildkit
# Wed, 25 Jun 2025 09:58:45 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Wed, 25 Jun 2025 09:58:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fadc52eaf7b1ea8984cd7b6356d2dcef2893de78903e23a64759d2446a24dea2`  
		Last Modified: Wed, 25 Jun 2025 20:23:27 GMT  
		Size: 46.2 MB (46198858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca58c790fc7ecc612e484dddeef97eb9d36ea13f35a163b5529eb91fdb02deb`  
		Last Modified: Wed, 25 Jun 2025 17:22:05 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:sisyphus` - unknown; unknown

```console
$ docker pull alt@sha256:636fdde5ac749abb2b2cffc73e2544fd0f038ecebae182316ace174330cefc69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2604624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca59823e11e4c73e208ec9ff2686f62d2125edd782e9c2139190a15defd403a5`

```dockerfile
```

-	Layers:
	-	`sha256:8375fdd93a40b17acb62ef049e39b75befbb528952707fbcc31113f6158c55f3`  
		Last Modified: Wed, 25 Jun 2025 19:07:36 GMT  
		Size: 2.6 MB (2598697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d16fc8420463de8b0d197377c0fdbeb6d1a16d782cf97f0778ad49e0998dece0`  
		Last Modified: Wed, 25 Jun 2025 19:07:37 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:sisyphus` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:cfa9dd04067ee51db060d08ccfaf01a839f250ea15b0e7f247d2de1fb5c7d9b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (44961521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86e473e2e6b1075bd4a21096744b778417a0d11c73f620a65da70da8e45c0c78`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Jun 2025 09:58:45 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Wed, 25 Jun 2025 09:58:45 GMT
LABEL org.opencontainers.image.licenses=GPLv3
# Wed, 25 Jun 2025 09:58:45 GMT
ADD alt-sisyphus-aarch64.tar.xz / # buildkit
# Wed, 25 Jun 2025 09:58:45 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Wed, 25 Jun 2025 09:58:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f284ac3c42d057f757f5612ebc912434bb93ca57dab9047de64ad77686123996`  
		Last Modified: Wed, 25 Jun 2025 19:18:24 GMT  
		Size: 45.0 MB (44961330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3155bb3712071a9ea0d863f2bfafd8c8cc093caa17e24425a314afc6ef34ea`  
		Last Modified: Wed, 25 Jun 2025 19:18:19 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:sisyphus` - unknown; unknown

```console
$ docker pull alt@sha256:1055258faaf2bd534ee33ce85b3b70b771e263d0b52cdb3821adb0464b76cabb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2604087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001d0e444b2c79be7db4c4efa0e09214cf2aeebfbe75cf439c12ee7937b0117d`

```dockerfile
```

-	Layers:
	-	`sha256:1900553f18b8595c1354e14da3af7ac86d07f0c9afc74cb6a87cb2494fcc1f4b`  
		Last Modified: Wed, 25 Jun 2025 22:07:30 GMT  
		Size: 2.6 MB (2598114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aba35b35874b7c7a1b5f0d719aca53576e95a80ffc12b739a2ec113048eeba75`  
		Last Modified: Wed, 25 Jun 2025 22:07:31 GMT  
		Size: 6.0 KB (5973 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:sisyphus` - linux; 386

```console
$ docker pull alt@sha256:c0ed8f2d997d109966d7136a6330910a032b9277c43ba877b78ab2be4ec9ed8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46276059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815bf802aa83d6650b0a01af944bb529ff4b59d9211d61d8a5d5c0645e9a1105`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Jun 2025 09:58:45 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Wed, 25 Jun 2025 09:58:45 GMT
LABEL org.opencontainers.image.licenses=GPLv3
# Wed, 25 Jun 2025 09:58:45 GMT
ADD alt-sisyphus-i586.tar.xz / # buildkit
# Wed, 25 Jun 2025 09:58:45 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Wed, 25 Jun 2025 09:58:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:fe7b2196caf0fcd84b698b465ef893c972842fdedd9452228d92c559b13fdd1f`  
		Last Modified: Wed, 25 Jun 2025 17:15:38 GMT  
		Size: 46.3 MB (46275869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1932bed047a35f74a080592ba27e7959b2ac2b1f634e0cc27f750f4ee46ee2a`  
		Last Modified: Wed, 25 Jun 2025 17:15:34 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:sisyphus` - unknown; unknown

```console
$ docker pull alt@sha256:a292fd3d6b03d6aa1737633f274e0eac12ed98ca766076ac0eec05ac5cd0f772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2603328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29d049a8781b2e7b8f8af3a1212698c9ad428418e013182af73ea7ccf39b5628`

```dockerfile
```

-	Layers:
	-	`sha256:ad62768819ac66ff763fcb36eda75d7c7d7d77b6df39c162a3283b23c919995b`  
		Last Modified: Wed, 25 Jun 2025 19:07:47 GMT  
		Size: 2.6 MB (2597423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71878018ab0959fd7db2883a6d70d8f371fe70f064f6d7677b1c8333ba801d39`  
		Last Modified: Wed, 25 Jun 2025 19:07:48 GMT  
		Size: 5.9 KB (5905 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:sisyphus` - linux; riscv64

```console
$ docker pull alt@sha256:8aa9a2c92bb2f27c51459ab23d0f73b39fda7fe65e84dee686950cbdc4526e80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44145553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d41d75641a7a84f358790a0d1237ac6f60966eb8da70b99e0cfceeb61bc0b927`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Jun 2025 09:58:45 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Wed, 25 Jun 2025 09:58:45 GMT
LABEL org.opencontainers.image.licenses=GPLv3
# Wed, 25 Jun 2025 09:58:45 GMT
ADD alt-sisyphus-riscv64.tar.xz / # buildkit
# Wed, 25 Jun 2025 09:58:45 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Wed, 25 Jun 2025 09:58:45 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ad138a7ec3dcfab9b17617d9fefe6b6cb1caceb8d225aec35d754ba8c34a4fbe`  
		Last Modified: Wed, 25 Jun 2025 17:17:57 GMT  
		Size: 44.1 MB (44145361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64348292f002f54cf97acc1afb36eb8be82f25a6e003129db304628cb314bc55`  
		Last Modified: Wed, 25 Jun 2025 17:17:52 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:sisyphus` - unknown; unknown

```console
$ docker pull alt@sha256:7a0e14f5c71ceb255ecbd52b2aa27c9b534f340ee59ba96c8579183f48c3f450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2603306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d3635db0d477c2b24f8248344abe2de04963b3987a5567aec8ad88459575bfd`

```dockerfile
```

-	Layers:
	-	`sha256:24d1e5cee4713aa5718a9a3e90f85638f11447cd6a454b6a7692286a9e070400`  
		Last Modified: Wed, 25 Jun 2025 19:07:52 GMT  
		Size: 2.6 MB (2597359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:899b9e563972ec81c30f7f5f3bf0d3620db7e721eee0c773cf29a7b064009d07`  
		Last Modified: Wed, 25 Jun 2025 19:07:53 GMT  
		Size: 5.9 KB (5947 bytes)  
		MIME: application/vnd.in-toto+json
