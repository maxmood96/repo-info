## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:0c50416519cf982c7d4d696839bce95f9569ec6b29c0beb99738375818105003
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

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7648d854cefa0a06121b94592ddf1ecdbd233af3b0afa94de4a77431c089d1fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76723157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faedd7c6ceadb7f60d3737fc6a3ba4f72178558e08b6dd625cfe75e8d1aaf6ba`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:42:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bdd122fd70d19475cad994fa0bd624dc1524d2143c57c7c1f3f9e23fe40ddb0a`  
		Last Modified: Wed, 10 Jun 2026 23:40:10 GMT  
		Size: 48.8 MB (48801212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250af42f2a097a32d106444385fc18ff806e3b5890910b0e364be8e50256f63d`  
		Last Modified: Thu, 11 Jun 2026 00:42:46 GMT  
		Size: 27.9 MB (27921945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6478f234a11e69c36298b52d66440e937aee15fe333feb54bd53fddf9dabd36d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4054117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5663f39d66f2bb196befad0f4da632b09ea2ab43b3ff944fed6ee65923838fa`

```dockerfile
```

-	Layers:
	-	`sha256:f7ea0b72556750a3bbb9ad1dfc5ebe3420d1950e15ab71c616a1bb872f2fa62e`  
		Last Modified: Thu, 11 Jun 2026 00:42:45 GMT  
		Size: 4.0 MB (4047356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57f980a6de489dd9ded326d7e7a4ffd0b2ae3365e6583e545de20249a49e9713`  
		Last Modified: Thu, 11 Jun 2026 00:42:45 GMT  
		Size: 6.8 KB (6761 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5df6ba36d8c156aa2eb3e12de93defe080adea52437f03ccbab8b0db9f6db12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70222070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d00a391a33730d0d8e5bbb4953d745a86c042a1e0f9b1a65d97ca50b1a9ae47b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1779062400'
# Wed, 20 May 2026 00:04:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1c98d9ac4796e25c1d81c99407f882de7bda76effb4d3c6a5d937bf755cc2313`  
		Last Modified: Tue, 19 May 2026 22:36:23 GMT  
		Size: 45.6 MB (45618956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1515c975babc2c0d71d5cf9a3ec0808ae1a576e22e50913d437d07a60ef65f`  
		Last Modified: Wed, 20 May 2026 00:04:13 GMT  
		Size: 24.6 MB (24603114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3bdfc35f79dd5bfa0730a44014dacae9399d3a01ed51b0fe8fe60d77647faefc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4070160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72b74c5e46288e195813dbce45c26f7e4972fd0f8be0cf772ec6c4d197af245`

```dockerfile
```

-	Layers:
	-	`sha256:a2b3db00d1b06c2eb955d9d486d6f836b6790ccfe08535a08bc448cc880d623e`  
		Last Modified: Wed, 20 May 2026 00:04:11 GMT  
		Size: 4.1 MB (4063336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f61cd2d46fae31cdb34c4a8164d5fc735305d8cb08339a9804ec83718251d8d`  
		Last Modified: Wed, 20 May 2026 00:04:11 GMT  
		Size: 6.8 KB (6824 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f1c5684056780adf5938b84f6556d281f128686a9c6695a2b66981d97ccfd513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75942854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56acaf5d6f220fb2073b0159034f511208da04076b557b5f4f2fc49705ec39ea`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:44:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:015f4a5f6bd3bcaa5c5acf626b97030c3007c4b91e864c4cfabf1be5d52e7648`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 48.8 MB (48818557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bde100970346a8633eb293a95aaa718b901d789108bd4e63e4f66d9d3771ea`  
		Last Modified: Thu, 11 Jun 2026 00:44:23 GMT  
		Size: 27.1 MB (27124297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1cfe9d1ab18162089195db3a5ea4d33516cd02dccf20f5b9d4f3d07924b863ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4059556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857334696a409c2ced6b95c74c88c2a9925eefd67a80b6f49f11dc35be52a897`

```dockerfile
```

-	Layers:
	-	`sha256:8028b1960efd439548990b1b7caae7dd88b7b61e5564fe3c0470091ea8f86876`  
		Last Modified: Thu, 11 Jun 2026 00:44:23 GMT  
		Size: 4.1 MB (4052715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b33d67b68faa91981241aec3565e668468013ef834f0f37ed7056a72369561d4`  
		Last Modified: Thu, 11 Jun 2026 00:44:23 GMT  
		Size: 6.8 KB (6841 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0409263217e9886083e2565b487f9054a507dd3ebbb92a7b62ab76828813afae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78225483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a439fea09a07816f794ae94ab1035c3b21f3bc4565309d4996d0489ac979ce7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1779062400'
# Tue, 19 May 2026 23:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:506409f9b5466021b987fde6d84a8bc529520e50798929836cef94e3223d354c`  
		Last Modified: Tue, 19 May 2026 22:37:32 GMT  
		Size: 50.0 MB (50016004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1f3d5431169cdd29adb39f5cf26f13e071f7217f28223b49e250857b02be6d`  
		Last Modified: Tue, 19 May 2026 23:25:28 GMT  
		Size: 28.2 MB (28209479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:229793405d66a94c04b0584ed3cba918cb7570659966b449baebd77384600dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4065698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d580ef5fb7b82ee065179410a4b791e3b5cc55ff1af362da54810c6725ed142`

```dockerfile
```

-	Layers:
	-	`sha256:7822bd9cdb000d91530ca710caed45c90e91f6f6b3c8c455ff8718276b865e6f`  
		Last Modified: Tue, 19 May 2026 23:25:27 GMT  
		Size: 4.1 MB (4058959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a996f61c39d11b423719c2cbaf86ae9da2174e08ab80dd339066ea0bfe49d92`  
		Last Modified: Tue, 19 May 2026 23:25:27 GMT  
		Size: 6.7 KB (6739 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:57bd51c546bfc13f4e79649f65ccd2a1038c4afbf9572c121e8353f94ce8e299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83331652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c9655743205644a3453c19fc8cdaa0109b277f00de3316e525126a3885a532`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1779062400'
# Wed, 20 May 2026 01:14:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0bda88a8fa865607f7a3bfe01b25fa99681c2572077bbfaf6b7e16e1f51b5b50`  
		Last Modified: Tue, 19 May 2026 22:36:39 GMT  
		Size: 54.0 MB (54046122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ac92e3c123ea205d76f5d82b79747aea7ae5197399f942393a1c3ea0ec0034`  
		Last Modified: Wed, 20 May 2026 01:14:34 GMT  
		Size: 29.3 MB (29285530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7870940223067223dd0be75342a0ff8999dab849d96e90f167d39350927d787b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4072486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16eeec580f689fb4209abd37b3f1f9fa9e59e348999d771c661661d103aa1f2e`

```dockerfile
```

-	Layers:
	-	`sha256:a04a81230acd06b8d54bc9e45c2bdf4bfcdf0064da02deaec5ddc203e4ba8a9c`  
		Last Modified: Wed, 20 May 2026 01:14:33 GMT  
		Size: 4.1 MB (4065693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99e253c2552d29f76e0692737dae4d9a8120f5ab2b79ce6e59cfb0921023e68f`  
		Last Modified: Wed, 20 May 2026 01:14:32 GMT  
		Size: 6.8 KB (6793 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:4d9eeae701d8b30c6a0945885dc9bb8954ed9aa25f1ff9409ee18c2f32344dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73259234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54740da28d920e5141faa3e9eead9e0a218a634f74abd1f6d322cefd3973d876`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1779062400'
# Thu, 21 May 2026 13:57:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d609dbe8a64103ca9a52594c54358bca867134ca11c5bdbab5024849e5765438`  
		Last Modified: Tue, 19 May 2026 23:39:28 GMT  
		Size: 46.8 MB (46808398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9071891294e630f1468302f4618eeabbee9f63f74797f1ce63bdd2a40a26945`  
		Last Modified: Thu, 21 May 2026 13:59:23 GMT  
		Size: 26.5 MB (26450836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:922306353132985d821cba6374c0cb159d752946cf32fe93467d5fd0454c64a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4060333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4482e2ed8be319745275281862700d2cf159dc90fcc9558463e9416fb8966a85`

```dockerfile
```

-	Layers:
	-	`sha256:f33292fac043bddc1764616f4f09a2aba155bfa4c670b02538fb4b6ee8af5e63`  
		Last Modified: Thu, 21 May 2026 13:59:19 GMT  
		Size: 4.1 MB (4053540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d40b084d09361c1202cff9b348bac8c42219955d1c6ff0fd7f5a6a2898a8cef3`  
		Last Modified: Thu, 21 May 2026 13:59:18 GMT  
		Size: 6.8 KB (6793 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f356f8b31e613906746839737dae8f975d2f3e56dd71363ca1517afba930c1fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75145068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d63b1df2844066cca05fb03b9c67637b3e3cbddb4852740ec9291d5aa63b463`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1779062400'
# Wed, 20 May 2026 00:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b2de0004fb71a1e4abdd27d0619b3567a865a43b4039f4f3ca7e11b6e7bf8ca5`  
		Last Modified: Tue, 19 May 2026 22:36:09 GMT  
		Size: 48.5 MB (48454253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558e98e58fdd0e7e9d312d1df7e45d14fcbde914744efb8b87cc091a75f459ef`  
		Last Modified: Wed, 20 May 2026 00:18:56 GMT  
		Size: 26.7 MB (26690815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fef33a60fbbea1d1168df19d074fc93db1ac613b02972c4b2f25072302fbdc11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4070022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf9942fb1fd905ca42251453cbb8cd5426d8be4897e3f0ca9e461105bc6c583`

```dockerfile
```

-	Layers:
	-	`sha256:70882327a02350ed47bbb23951fa1d854cd48588ec75ffecd5437268c83118d6`  
		Last Modified: Wed, 20 May 2026 00:18:56 GMT  
		Size: 4.1 MB (4063261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d88594689e86f4926dcf852f68a8abdb170c20a08e48a08299f6d229a3b0c1c`  
		Last Modified: Wed, 20 May 2026 00:18:56 GMT  
		Size: 6.8 KB (6761 bytes)  
		MIME: application/vnd.in-toto+json
