<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `alt`

-	[`alt:latest`](#altlatest)
-	[`alt:p10`](#altp10)
-	[`alt:p11`](#altp11)
-	[`alt:sisyphus`](#altsisyphus)

## `alt:latest`

```console
$ docker pull alt@sha256:fe144ad598def89591b3b3cec97cf5ea770a705a169728f9e9e85647a1a52b92
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
$ docker pull alt@sha256:9e9d9525ffe8e2931c99008c029afe96d0b8a2d408561e7f6aee71e52fa245e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45910960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97c70e35e5754c99e2739a341746ab94e4f118e9c63ceaba806e369af80075e9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Jun 2025 09:58:55 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Wed, 25 Jun 2025 09:58:55 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3
# Wed, 25 Jun 2025 09:58:55 GMT
ADD alt-p11-x86_64.tar.xz / # buildkit
# Wed, 25 Jun 2025 09:58:55 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Wed, 25 Jun 2025 09:58:55 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c549b474d68c334ae60850f6481337e40e1615de6ee08d713a54ca6bf5d0248a`  
		Last Modified: Wed, 25 Jun 2025 17:15:36 GMT  
		Size: 45.9 MB (45910769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d382247a69f7a8453c5cc93ac859d7240971656b533005b29d886b53efcd095`  
		Last Modified: Wed, 25 Jun 2025 17:15:31 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:latest` - unknown; unknown

```console
$ docker pull alt@sha256:8f20233542582367a280afe39b44b9d4e1348e5e6a60366111262b368da640cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2602179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5cde7f9b92b746b11b75b1850758efc884625e5b57cd74ca890aa3431802f28`

```dockerfile
```

-	Layers:
	-	`sha256:97de9ba866d80e3eecf725381a3f111e2836b96b56b45f8d1bb5b06856222bab`  
		Last Modified: Wed, 25 Jun 2025 19:07:20 GMT  
		Size: 2.6 MB (2595959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac4f0d42b1f964a775ad7c0cc04db64082db9a73265c9860d0365f00bc58d408`  
		Last Modified: Wed, 25 Jun 2025 19:07:20 GMT  
		Size: 6.2 KB (6220 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:latest` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:40c2a3e256454a55ca41000e300fe8c3a27f77c63aee0636f67f2432e0b8c35b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44635847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:163eb23372fe02f9ffdc60408142dcbac9616ce043db88387bc225c1f58d77e9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Jun 2025 09:58:55 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Wed, 25 Jun 2025 09:58:55 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3
# Wed, 25 Jun 2025 09:58:55 GMT
ADD alt-p11-aarch64.tar.xz / # buildkit
# Wed, 25 Jun 2025 09:58:55 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Wed, 25 Jun 2025 09:58:55 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:74a142dca9889a46e15d23ab0a0bffa86e6d7fb035fbacc6f3a752f505f13534`  
		Last Modified: Wed, 25 Jun 2025 19:18:54 GMT  
		Size: 44.6 MB (44635656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd32ab124cfe8126537d7dda4f2aeb0b3c4ba1b1dfc5e0f38d6aadbf359ab0cd`  
		Last Modified: Wed, 25 Jun 2025 19:18:49 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:latest` - unknown; unknown

```console
$ docker pull alt@sha256:2069a06b372b31c220d35a057c97f3df783176908e60381b37e7e262f20223a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2601666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99701a501446a1d48a323a3b692672fa8b53e9d7d7a772fbdf40d895bfbc44bc`

```dockerfile
```

-	Layers:
	-	`sha256:ff08878c9e5b89f044ad19fd4a706da313f9346c75843292a94bb6ffb0cd1220`  
		Last Modified: Wed, 25 Jun 2025 22:07:21 GMT  
		Size: 2.6 MB (2595388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6933d0efd47d6294491b86367a6d94fcbd6b49538df4b7e1a1943d5e62c43f2`  
		Last Modified: Wed, 25 Jun 2025 22:07:21 GMT  
		Size: 6.3 KB (6278 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:latest` - linux; 386

```console
$ docker pull alt@sha256:a2e9bfd42ed83511292684d59a9a2d8761c5d6241c1b7a75997144ac43cdca06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45934363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfd3bf78a867d3d71151df945bd6c3bf33fe94d30f8dd046cc063ad5f3f867f5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Jun 2025 09:58:55 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Wed, 25 Jun 2025 09:58:55 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3
# Wed, 25 Jun 2025 09:58:55 GMT
ADD alt-p11-i586.tar.xz / # buildkit
# Wed, 25 Jun 2025 09:58:55 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Wed, 25 Jun 2025 09:58:55 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e6daf3d63bc283e9784e906e695bd148a95b0fe6412400cfe8a0cca8939f81fa`  
		Last Modified: Wed, 25 Jun 2025 17:15:38 GMT  
		Size: 45.9 MB (45934172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ef5c23433a05fc6187c6c372a5e69a02710206c223d749b9df6030040b5564`  
		Last Modified: Wed, 25 Jun 2025 17:15:33 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:latest` - unknown; unknown

```console
$ docker pull alt@sha256:8e8d285d1afd127637088d3336eb09b76285625f84ce09ab36919c0782d4d30e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2600873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a2f06c2b829c84ece2f133749b9205617fa2dc316af3517b1e83c4c55f865c`

```dockerfile
```

-	Layers:
	-	`sha256:50b2878398bcf2fbdd206ec1d2f34b2294973961d025859c1cd5a9608cf88aa1`  
		Last Modified: Wed, 25 Jun 2025 19:07:32 GMT  
		Size: 2.6 MB (2594680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47c84a28aa0c7fe24ea1fca62cdca5499ad5a2a00276eae1571a25d3dbee2952`  
		Last Modified: Wed, 25 Jun 2025 19:07:32 GMT  
		Size: 6.2 KB (6193 bytes)  
		MIME: application/vnd.in-toto+json

## `alt:p10`

```console
$ docker pull alt@sha256:d8ccfb9ac82a8ce86856ac06819337713db7569a4be1a489ed373f5b42f0c8e7
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
$ docker pull alt@sha256:249d325d6d5d04e10870b78cef3efefc6d403b4c412a8665afafffe2b3c6d22f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47332895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac15d18d4ae703dbe1e634f8fb639b8cb664bb717b296e56bd82d415b8ee891`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Jun 2025 09:58:50 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Wed, 25 Jun 2025 09:58:50 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3
# Wed, 25 Jun 2025 09:58:50 GMT
ADD alt-p10-x86_64.tar.xz / # buildkit
# Wed, 25 Jun 2025 09:58:50 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Wed, 25 Jun 2025 09:58:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:480e18bfbaece893b4120aec7d59ce253382510906ac2630ccd15f17608c2be0`  
		Last Modified: Wed, 25 Jun 2025 19:26:38 GMT  
		Size: 47.3 MB (47332703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee7671a5fdcbe4f62ff8d6ce1324a2630852bc7ee999ae51c8a7ac6b88385a6`  
		Last Modified: Wed, 25 Jun 2025 17:20:56 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:p10` - unknown; unknown

```console
$ docker pull alt@sha256:5136ef874682386ee8daf479123f33c0be2f69a4bbf3ef734a60e9f91e82b0cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2600768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbdb248c96cae043278df54b1e1347a8c6835e190415ac299c5a77b5f28af8e6`

```dockerfile
```

-	Layers:
	-	`sha256:83a0b3eb8005609776c8325f48d92b053d82d38aa17113bdcf00bfba1c07bcaa`  
		Last Modified: Wed, 25 Jun 2025 19:07:25 GMT  
		Size: 2.6 MB (2594840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f822433a11dec4fc83249e5d754fdad2ebf5fbbf4d9d69b5bdef34735563140e`  
		Last Modified: Wed, 25 Jun 2025 19:07:26 GMT  
		Size: 5.9 KB (5928 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:p10` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:9100b11e85c3d2bc832cf13f950adbdd4b36cb83a885b057f4cc0eb8d8446370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46504570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea1dccf59a875c22508fd883561045b481ffed26a34e068813fb67b491af910`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Jun 2025 09:58:50 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Wed, 25 Jun 2025 09:58:50 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3
# Wed, 25 Jun 2025 09:58:50 GMT
ADD alt-p10-aarch64.tar.xz / # buildkit
# Wed, 25 Jun 2025 09:58:50 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Wed, 25 Jun 2025 09:58:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:902a44c3843ba64e11c460696be729cc0a5ead177ca27ff6ab7eb14a7b6e0343`  
		Last Modified: Wed, 25 Jun 2025 19:17:19 GMT  
		Size: 46.5 MB (46504378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f09eafe46e475e80d66b5a2c8754e4eb2afffdec7dd2746ec9d05a7e302e45b`  
		Last Modified: Wed, 25 Jun 2025 19:17:17 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:p10` - unknown; unknown

```console
$ docker pull alt@sha256:ad4e370f093cc6e18f67ccfae9fcca34a687f36445a3c424669073aa8c5660a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2599455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c47a68713bd8026f55a1f16a3097f428dbc37ccafbd5d45c9c4aa273795dcf5`

```dockerfile
```

-	Layers:
	-	`sha256:b9b2d1eb16cdb2fd1195e4f3164990255e7e5df23b3bb3fb021b6655104a2d06`  
		Last Modified: Wed, 25 Jun 2025 22:07:26 GMT  
		Size: 2.6 MB (2593481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90e2e9cf1f4106f8dbb1c61521fc260809306ebaf01f36e534dbae090bfbaeea`  
		Last Modified: Wed, 25 Jun 2025 22:07:27 GMT  
		Size: 6.0 KB (5974 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:p10` - linux; 386

```console
$ docker pull alt@sha256:6e88a406fe391e073a43ea3ffa526ba036f1a9e70c8bf7382fb3f02e9dba292a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48090962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c12a3eebd3e826f9c3c81aaffe429bc340d10dafed98c032b6ec6a0345ccec2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Jun 2025 09:58:50 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Wed, 25 Jun 2025 09:58:50 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3
# Wed, 25 Jun 2025 09:58:50 GMT
ADD alt-p10-i586.tar.xz / # buildkit
# Wed, 25 Jun 2025 09:58:50 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Wed, 25 Jun 2025 09:58:50 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:b7fb1daa05ace6fe84c0ec5233c059e3225ef921fecfe10739719bff1cf28888`  
		Last Modified: Wed, 25 Jun 2025 17:15:32 GMT  
		Size: 48.1 MB (48090771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18143f183f70586800770ae622a3766f930e9e1971f10ad230acd068a3af28e7`  
		Last Modified: Wed, 25 Jun 2025 17:15:26 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:p10` - unknown; unknown

```console
$ docker pull alt@sha256:8e80ea364584bc68b135f6c2a407ee475bb846dbe5adf769a914cfdce59ecc50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2602594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e6422a9fed6abb74021968664edd49099517c042afa63cd7d32bcfb128bd9dd`

```dockerfile
```

-	Layers:
	-	`sha256:ae39723402a0a670e14bb07fed6d85737e07365f7d4aaee7e307041125c4ec39`  
		Last Modified: Wed, 25 Jun 2025 19:07:32 GMT  
		Size: 2.6 MB (2596688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d11ca08d37e86c0ecaa9f313de7ba89117b6ddd7ed12f54b34a121d6d00b14f`  
		Last Modified: Wed, 25 Jun 2025 19:07:33 GMT  
		Size: 5.9 KB (5906 bytes)  
		MIME: application/vnd.in-toto+json

## `alt:p11`

```console
$ docker pull alt@sha256:fe144ad598def89591b3b3cec97cf5ea770a705a169728f9e9e85647a1a52b92
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
$ docker pull alt@sha256:9e9d9525ffe8e2931c99008c029afe96d0b8a2d408561e7f6aee71e52fa245e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45910960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97c70e35e5754c99e2739a341746ab94e4f118e9c63ceaba806e369af80075e9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Jun 2025 09:58:55 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Wed, 25 Jun 2025 09:58:55 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3
# Wed, 25 Jun 2025 09:58:55 GMT
ADD alt-p11-x86_64.tar.xz / # buildkit
# Wed, 25 Jun 2025 09:58:55 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Wed, 25 Jun 2025 09:58:55 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c549b474d68c334ae60850f6481337e40e1615de6ee08d713a54ca6bf5d0248a`  
		Last Modified: Wed, 25 Jun 2025 17:15:36 GMT  
		Size: 45.9 MB (45910769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d382247a69f7a8453c5cc93ac859d7240971656b533005b29d886b53efcd095`  
		Last Modified: Wed, 25 Jun 2025 17:15:31 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:p11` - unknown; unknown

```console
$ docker pull alt@sha256:8f20233542582367a280afe39b44b9d4e1348e5e6a60366111262b368da640cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2602179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5cde7f9b92b746b11b75b1850758efc884625e5b57cd74ca890aa3431802f28`

```dockerfile
```

-	Layers:
	-	`sha256:97de9ba866d80e3eecf725381a3f111e2836b96b56b45f8d1bb5b06856222bab`  
		Last Modified: Wed, 25 Jun 2025 19:07:20 GMT  
		Size: 2.6 MB (2595959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac4f0d42b1f964a775ad7c0cc04db64082db9a73265c9860d0365f00bc58d408`  
		Last Modified: Wed, 25 Jun 2025 19:07:20 GMT  
		Size: 6.2 KB (6220 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:p11` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:40c2a3e256454a55ca41000e300fe8c3a27f77c63aee0636f67f2432e0b8c35b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44635847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:163eb23372fe02f9ffdc60408142dcbac9616ce043db88387bc225c1f58d77e9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Jun 2025 09:58:55 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Wed, 25 Jun 2025 09:58:55 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3
# Wed, 25 Jun 2025 09:58:55 GMT
ADD alt-p11-aarch64.tar.xz / # buildkit
# Wed, 25 Jun 2025 09:58:55 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Wed, 25 Jun 2025 09:58:55 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:74a142dca9889a46e15d23ab0a0bffa86e6d7fb035fbacc6f3a752f505f13534`  
		Last Modified: Wed, 25 Jun 2025 19:18:54 GMT  
		Size: 44.6 MB (44635656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd32ab124cfe8126537d7dda4f2aeb0b3c4ba1b1dfc5e0f38d6aadbf359ab0cd`  
		Last Modified: Wed, 25 Jun 2025 19:18:49 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:p11` - unknown; unknown

```console
$ docker pull alt@sha256:2069a06b372b31c220d35a057c97f3df783176908e60381b37e7e262f20223a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2601666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99701a501446a1d48a323a3b692672fa8b53e9d7d7a772fbdf40d895bfbc44bc`

```dockerfile
```

-	Layers:
	-	`sha256:ff08878c9e5b89f044ad19fd4a706da313f9346c75843292a94bb6ffb0cd1220`  
		Last Modified: Wed, 25 Jun 2025 22:07:21 GMT  
		Size: 2.6 MB (2595388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6933d0efd47d6294491b86367a6d94fcbd6b49538df4b7e1a1943d5e62c43f2`  
		Last Modified: Wed, 25 Jun 2025 22:07:21 GMT  
		Size: 6.3 KB (6278 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:p11` - linux; 386

```console
$ docker pull alt@sha256:a2e9bfd42ed83511292684d59a9a2d8761c5d6241c1b7a75997144ac43cdca06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45934363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfd3bf78a867d3d71151df945bd6c3bf33fe94d30f8dd046cc063ad5f3f867f5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Jun 2025 09:58:55 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Wed, 25 Jun 2025 09:58:55 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3
# Wed, 25 Jun 2025 09:58:55 GMT
ADD alt-p11-i586.tar.xz / # buildkit
# Wed, 25 Jun 2025 09:58:55 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Wed, 25 Jun 2025 09:58:55 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:e6daf3d63bc283e9784e906e695bd148a95b0fe6412400cfe8a0cca8939f81fa`  
		Last Modified: Wed, 25 Jun 2025 17:15:38 GMT  
		Size: 45.9 MB (45934172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ef5c23433a05fc6187c6c372a5e69a02710206c223d749b9df6030040b5564`  
		Last Modified: Wed, 25 Jun 2025 17:15:33 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:p11` - unknown; unknown

```console
$ docker pull alt@sha256:8e8d285d1afd127637088d3336eb09b76285625f84ce09ab36919c0782d4d30e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2600873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a2f06c2b829c84ece2f133749b9205617fa2dc316af3517b1e83c4c55f865c`

```dockerfile
```

-	Layers:
	-	`sha256:50b2878398bcf2fbdd206ec1d2f34b2294973961d025859c1cd5a9608cf88aa1`  
		Last Modified: Wed, 25 Jun 2025 19:07:32 GMT  
		Size: 2.6 MB (2594680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47c84a28aa0c7fe24ea1fca62cdca5499ad5a2a00276eae1571a25d3dbee2952`  
		Last Modified: Wed, 25 Jun 2025 19:07:32 GMT  
		Size: 6.2 KB (6193 bytes)  
		MIME: application/vnd.in-toto+json

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
