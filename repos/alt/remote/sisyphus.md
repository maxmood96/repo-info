## `alt:sisyphus`

```console
$ docker pull alt@sha256:c7421cbf44aedaa68ee768f9c6a3324ee04ddf3387fc8394da7725b11559316e
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
$ docker pull alt@sha256:6f7fea3d1247c5ee6a916be2ead216c209ed05bac5229f3d28149684019ee051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45505331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adca784378c208389d56c53082d07dee60ac6179df0bd4d33470ea4a6c3db35a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Dec 2024 14:36:44 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org]
# Mon, 16 Dec 2024 14:36:44 GMT
LABEL org.opencontainers.image.licenses=GPLv3
# Mon, 16 Dec 2024 14:36:44 GMT
ADD alt-sisyphus-x86_64.tar.xz / # buildkit
# Mon, 16 Dec 2024 14:36:44 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Mon, 16 Dec 2024 14:36:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4a707a4b524da355aa2661fc84e24d6a08c202cf5fda50161e2d329195657ab3`  
		Last Modified: Mon, 16 Dec 2024 19:28:54 GMT  
		Size: 45.5 MB (45505141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7e687c280fedf3243dc7fbe55445e4ec02ead2f1d2b11851f7df09e9380e52`  
		Last Modified: Mon, 16 Dec 2024 19:28:54 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:sisyphus` - unknown; unknown

```console
$ docker pull alt@sha256:8d13aacc89a13fac4bd29a7bbe29eafc06b0ab560323655339ba9ba1d079f16c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2539290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0d0322b24417506c3abf9852ad3a54b49d63669b2ca9e5915e02a97bcdbb5b6`

```dockerfile
```

-	Layers:
	-	`sha256:b150d472e8d5bb0dcb21e5f962a82a6a48f74172d3de608ae8adc7a341e916c4`  
		Last Modified: Mon, 16 Dec 2024 19:28:54 GMT  
		Size: 2.5 MB (2533363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e132186628c570f5a24fdc80509d846ad0f441405ec029c4779c7e42be14c654`  
		Last Modified: Mon, 16 Dec 2024 19:28:53 GMT  
		Size: 5.9 KB (5927 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:sisyphus` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:e6bf293b72ed6aecd514b7d91f6ec0fa3dcc9ea29e8ef1c414bd8262f3892ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 MB (44254122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910629b4193f2cbc56bab2fe15015a7b71a9d0da77aacae8767dec661c4374f6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Dec 2024 14:36:44 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org]
# Mon, 16 Dec 2024 14:36:44 GMT
LABEL org.opencontainers.image.licenses=GPLv3
# Mon, 16 Dec 2024 14:36:44 GMT
ADD alt-sisyphus-aarch64.tar.xz / # buildkit
# Mon, 16 Dec 2024 14:36:44 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Mon, 16 Dec 2024 14:36:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ea1735b70c58d9efb5003f5dfc209e327de3647324cadde458c8e93afcf15dd8`  
		Size: 44.3 MB (44253931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba48eda5e1ae93b6f3f1c9181465a233ef6ddd8c59e0c4e4d4a78ef88d348a96`  
		Last Modified: Mon, 16 Dec 2024 19:29:14 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:sisyphus` - unknown; unknown

```console
$ docker pull alt@sha256:f8d4a3c5ca8ca00712540fe30c579c046fbd34309bb9c5190b43a09efe173132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2538753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5207a659d9b3b493055bf8782b8f2a6f9fce075f58490c5b390efa362e8ccabc`

```dockerfile
```

-	Layers:
	-	`sha256:69d494c76e5d451ad675cf882d0761c341c3c1e58057ce9d6cdba7e8397995da`  
		Last Modified: Mon, 16 Dec 2024 19:29:14 GMT  
		Size: 2.5 MB (2532780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd991cd33bbafb53ffcf8dfbb1f27c399c9a5b8fa23a6f954de97c2e49335ce8`  
		Last Modified: Mon, 16 Dec 2024 19:29:14 GMT  
		Size: 6.0 KB (5973 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:sisyphus` - linux; 386

```console
$ docker pull alt@sha256:6c8c0dff2b88e84a2b5d3fa11a0a5c51789bd06e131dba746f897357eba048a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45639954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6771b2eb983c39698335e1fd3e8f29872da34b4008d57a08ee982e54fa8edae`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Dec 2024 14:36:44 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org]
# Mon, 16 Dec 2024 14:36:44 GMT
LABEL org.opencontainers.image.licenses=GPLv3
# Mon, 16 Dec 2024 14:36:44 GMT
ADD alt-sisyphus-i586.tar.xz / # buildkit
# Mon, 16 Dec 2024 14:36:44 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Mon, 16 Dec 2024 14:36:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:def943c8cffd415034ddfb74d8f0a578f4e6c938973fba283ed07adba55cdd47`  
		Last Modified: Mon, 16 Dec 2024 19:29:03 GMT  
		Size: 45.6 MB (45639764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3681c9fb5a9618c6a3a82e1e226eca51c93c7503673ebacadcc0d4a4599d75c`  
		Last Modified: Mon, 16 Dec 2024 19:29:01 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:sisyphus` - unknown; unknown

```console
$ docker pull alt@sha256:eced92d674166746f5e113fafab8ad4bd46d03a2ed014c6eb793c842ef06976a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2537994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1600cb93ac90657ce45b571e27cd9a04128fba7e39dd2849571ba288c46ae4bd`

```dockerfile
```

-	Layers:
	-	`sha256:75107a66673639a1ef669bb04ca4842aa86b4e8ecbac60cb695be7c026de17ab`  
		Last Modified: Mon, 16 Dec 2024 19:29:02 GMT  
		Size: 2.5 MB (2532089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f484c446b47290b41bff29655469976ec8e0bd471a35c5036221b22d42f0a6f`  
		Last Modified: Mon, 16 Dec 2024 19:29:01 GMT  
		Size: 5.9 KB (5905 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:sisyphus` - linux; riscv64

```console
$ docker pull alt@sha256:9febaece423faba191f374279ac3c8c1e10955324039024573e91af7422a3099
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.5 MB (43490441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ec68f85f0afed86d2ea3bf3d2af60ee3dc0406df9a26c1a9fe769c73dbe902d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Dec 2024 14:36:44 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org]
# Mon, 16 Dec 2024 14:36:44 GMT
LABEL org.opencontainers.image.licenses=GPLv3
# Mon, 16 Dec 2024 14:36:44 GMT
ADD alt-sisyphus-riscv64.tar.xz / # buildkit
# Mon, 16 Dec 2024 14:36:44 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Mon, 16 Dec 2024 14:36:44 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:60b576ed3f359143510ff313ce327adab2c0f10f63d352a0e668b669c74b1713`  
		Last Modified: Mon, 16 Dec 2024 21:06:00 GMT  
		Size: 43.5 MB (43490250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54fc37e6507857ae3a2fdc4a8ae3aff6eb9e43d985f77bde5c90cbb9e72b9e8`  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:sisyphus` - unknown; unknown

```console
$ docker pull alt@sha256:b6ddb1e9a0bdc34a754066bd79539aedd9699c6a1cfdf41cc7b09972f321e7d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2537978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fff6ec339f566d0f19bfefbedfd8487c69a9e7e01692e7c500487e9df4bdfb9`

```dockerfile
```

-	Layers:
	-	`sha256:2e6390fa390e4826ea21d3a88edb3eaf771387080f195a9f020b4a04abd5494e`  
		Last Modified: Mon, 16 Dec 2024 21:05:55 GMT  
		Size: 2.5 MB (2532031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99b1d10e49b0feb7cb96d6098f024930df063589f2a05726b8ff62504dbe4f7c`  
		Last Modified: Mon, 16 Dec 2024 21:05:54 GMT  
		Size: 5.9 KB (5947 bytes)  
		MIME: application/vnd.in-toto+json
