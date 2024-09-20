<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `alt`

-	[`alt:latest`](#altlatest)
-	[`alt:p10`](#altp10)
-	[`alt:p11`](#altp11)
-	[`alt:sisyphus`](#altsisyphus)

## `alt:latest`

```console
$ docker pull alt@sha256:1a4f3803dee404126c6947ea9f791eb781e25b541477dc242ef188e4e7734bef
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
$ docker pull alt@sha256:3a4b938573c6678d2ef73a4b5bc80c68a174f6fe4e877930fb4704dc0c25fbba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45398580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b04e318148d10f6588f105c464679579ccaf32cdf15bfe524b456ce9d2e03e23`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 20 Sep 2024 08:14:24 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org]
# Fri, 20 Sep 2024 08:14:24 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3
# Fri, 20 Sep 2024 08:14:24 GMT
ADD alt-p10-x86_64.tar.xz / # buildkit
# Fri, 20 Sep 2024 08:14:24 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Fri, 20 Sep 2024 08:14:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8d0b964d5817071ac2105a52a322560585c8a20b4aab57b7f106b625ee6b79f9`  
		Last Modified: Fri, 20 Sep 2024 16:57:11 GMT  
		Size: 45.4 MB (45398389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529c2ffbf4d6aae339e7a247c073e9d4123d246e92fd02018ee699a2d2c943cb`  
		Last Modified: Fri, 20 Sep 2024 16:57:10 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:latest` - unknown; unknown

```console
$ docker pull alt@sha256:1822813339cbe50c62a3ea72905589d48ce57b6d5338d65ed8a61e2252440e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 KB (7806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea3f3332b97e289e019acd77703058a4f6d1b84991d100109b4db2a4d673f3e4`

```dockerfile
```

-	Layers:
	-	`sha256:e7eff4cdeb6e90f9427cf81491fa8a4786cf773cad984f35d53bff5e59b608b2`  
		Last Modified: Fri, 20 Sep 2024 16:57:10 GMT  
		Size: 1.6 KB (1621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bca069f05c81b9912559e7b8c2629cdac7b37bf74cec8ac1b319722f4ff52a9`  
		Last Modified: Fri, 20 Sep 2024 16:57:10 GMT  
		Size: 6.2 KB (6185 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:latest` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:aca57288062a96b666b3fae403917da7a0b5f161a765edf0d20c6c9f6bca1535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44628054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b368b68c5a05b3b55f1cd645d93b711bb45b93d6b4fdd5dd3118bc1e294fa1a4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 20 Sep 2024 08:14:24 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org]
# Fri, 20 Sep 2024 08:14:24 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3
# Fri, 20 Sep 2024 08:14:24 GMT
ADD alt-p10-aarch64.tar.xz / # buildkit
# Fri, 20 Sep 2024 08:14:24 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Fri, 20 Sep 2024 08:14:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c7058c4c7f261e7cc8a3e70eb2bba11e0750d2947411ef38a815a89c77dfe92d`  
		Last Modified: Fri, 20 Sep 2024 16:57:17 GMT  
		Size: 44.6 MB (44627863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8200f78e0142a374e7a3342a7cc55a7c4e3e8c055864fd2a49ae42bddfb504`  
		Last Modified: Fri, 20 Sep 2024 16:57:15 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:latest` - unknown; unknown

```console
$ docker pull alt@sha256:b434f60711c1a636a9e7be21715ceb7d806f6b17c35121daba9ff0f617ae2fbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2551055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0728c4c8fb9a2ab76011e406e0b0e9c199bff811921fbde0a588df70e89903b`

```dockerfile
```

-	Layers:
	-	`sha256:6a571c423469d35fdc631ac5567af8aafc6ac33da81d500054ae99f8d7d31586`  
		Last Modified: Fri, 20 Sep 2024 16:57:15 GMT  
		Size: 2.5 MB (2544826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0384a2c7991bc4b6835556ce25c0db5aa9c7eb9f888d53be99b03f765604889e`  
		Last Modified: Fri, 20 Sep 2024 16:57:15 GMT  
		Size: 6.2 KB (6229 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:latest` - linux; 386

```console
$ docker pull alt@sha256:096a3461d9265f6ee64703e3dd2ecf628a4958f8a5874c4b61413e689cd83702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46090110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b142e1686e691844aa4cf6a64432e8e7136d268c311fd2293bca87fd5fa3c0c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 20 Sep 2024 08:14:24 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org]
# Fri, 20 Sep 2024 08:14:24 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3
# Fri, 20 Sep 2024 08:14:24 GMT
ADD alt-p10-i586.tar.xz / # buildkit
# Fri, 20 Sep 2024 08:14:24 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Fri, 20 Sep 2024 08:14:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3a92cc9184d11c19946c52f84bc1c28cc99365ae4f405a5ae7840f91c426ddc2`  
		Last Modified: Fri, 20 Sep 2024 16:57:09 GMT  
		Size: 46.1 MB (46089919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e3f2b8ebc1ee5967d0676040ba3895327f2d57fa9e90b1a79a1bb11f142408`  
		Last Modified: Fri, 20 Sep 2024 16:57:08 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:latest` - unknown; unknown

```console
$ docker pull alt@sha256:3015e20e779390d42dcba97fe1d7a609920698193602b1920dc8ba12c1076c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 KB (7766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8667a7512e227bad0fda3b0884c0cdbd54b4f6e69ce5bde0ae0ef7e5cd7f29d3`

```dockerfile
```

-	Layers:
	-	`sha256:681ba2cc40b0ca2008090460fd68e61a8e5efac42c751b1df975ec6356ca1f68`  
		Last Modified: Fri, 20 Sep 2024 16:57:08 GMT  
		Size: 1.6 KB (1608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:349d0bd87f841b936e8a05987608e6029da2f20262d136d4c1adbfe70a8c4df0`  
		Last Modified: Fri, 20 Sep 2024 16:57:08 GMT  
		Size: 6.2 KB (6158 bytes)  
		MIME: application/vnd.in-toto+json

## `alt:p10`

```console
$ docker pull alt@sha256:1a4f3803dee404126c6947ea9f791eb781e25b541477dc242ef188e4e7734bef
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
$ docker pull alt@sha256:3a4b938573c6678d2ef73a4b5bc80c68a174f6fe4e877930fb4704dc0c25fbba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45398580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b04e318148d10f6588f105c464679579ccaf32cdf15bfe524b456ce9d2e03e23`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 20 Sep 2024 08:14:24 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org]
# Fri, 20 Sep 2024 08:14:24 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3
# Fri, 20 Sep 2024 08:14:24 GMT
ADD alt-p10-x86_64.tar.xz / # buildkit
# Fri, 20 Sep 2024 08:14:24 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Fri, 20 Sep 2024 08:14:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8d0b964d5817071ac2105a52a322560585c8a20b4aab57b7f106b625ee6b79f9`  
		Last Modified: Fri, 20 Sep 2024 16:57:11 GMT  
		Size: 45.4 MB (45398389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529c2ffbf4d6aae339e7a247c073e9d4123d246e92fd02018ee699a2d2c943cb`  
		Last Modified: Fri, 20 Sep 2024 16:57:10 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:p10` - unknown; unknown

```console
$ docker pull alt@sha256:1822813339cbe50c62a3ea72905589d48ce57b6d5338d65ed8a61e2252440e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 KB (7806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea3f3332b97e289e019acd77703058a4f6d1b84991d100109b4db2a4d673f3e4`

```dockerfile
```

-	Layers:
	-	`sha256:e7eff4cdeb6e90f9427cf81491fa8a4786cf773cad984f35d53bff5e59b608b2`  
		Last Modified: Fri, 20 Sep 2024 16:57:10 GMT  
		Size: 1.6 KB (1621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bca069f05c81b9912559e7b8c2629cdac7b37bf74cec8ac1b319722f4ff52a9`  
		Last Modified: Fri, 20 Sep 2024 16:57:10 GMT  
		Size: 6.2 KB (6185 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:p10` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:aca57288062a96b666b3fae403917da7a0b5f161a765edf0d20c6c9f6bca1535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44628054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b368b68c5a05b3b55f1cd645d93b711bb45b93d6b4fdd5dd3118bc1e294fa1a4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 20 Sep 2024 08:14:24 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org]
# Fri, 20 Sep 2024 08:14:24 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3
# Fri, 20 Sep 2024 08:14:24 GMT
ADD alt-p10-aarch64.tar.xz / # buildkit
# Fri, 20 Sep 2024 08:14:24 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Fri, 20 Sep 2024 08:14:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:c7058c4c7f261e7cc8a3e70eb2bba11e0750d2947411ef38a815a89c77dfe92d`  
		Last Modified: Fri, 20 Sep 2024 16:57:17 GMT  
		Size: 44.6 MB (44627863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8200f78e0142a374e7a3342a7cc55a7c4e3e8c055864fd2a49ae42bddfb504`  
		Last Modified: Fri, 20 Sep 2024 16:57:15 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:p10` - unknown; unknown

```console
$ docker pull alt@sha256:b434f60711c1a636a9e7be21715ceb7d806f6b17c35121daba9ff0f617ae2fbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2551055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0728c4c8fb9a2ab76011e406e0b0e9c199bff811921fbde0a588df70e89903b`

```dockerfile
```

-	Layers:
	-	`sha256:6a571c423469d35fdc631ac5567af8aafc6ac33da81d500054ae99f8d7d31586`  
		Last Modified: Fri, 20 Sep 2024 16:57:15 GMT  
		Size: 2.5 MB (2544826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0384a2c7991bc4b6835556ce25c0db5aa9c7eb9f888d53be99b03f765604889e`  
		Last Modified: Fri, 20 Sep 2024 16:57:15 GMT  
		Size: 6.2 KB (6229 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:p10` - linux; 386

```console
$ docker pull alt@sha256:096a3461d9265f6ee64703e3dd2ecf628a4958f8a5874c4b61413e689cd83702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46090110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b142e1686e691844aa4cf6a64432e8e7136d268c311fd2293bca87fd5fa3c0c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 20 Sep 2024 08:14:24 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org]
# Fri, 20 Sep 2024 08:14:24 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3
# Fri, 20 Sep 2024 08:14:24 GMT
ADD alt-p10-i586.tar.xz / # buildkit
# Fri, 20 Sep 2024 08:14:24 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Fri, 20 Sep 2024 08:14:24 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:3a92cc9184d11c19946c52f84bc1c28cc99365ae4f405a5ae7840f91c426ddc2`  
		Last Modified: Fri, 20 Sep 2024 16:57:09 GMT  
		Size: 46.1 MB (46089919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e3f2b8ebc1ee5967d0676040ba3895327f2d57fa9e90b1a79a1bb11f142408`  
		Last Modified: Fri, 20 Sep 2024 16:57:08 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:p10` - unknown; unknown

```console
$ docker pull alt@sha256:3015e20e779390d42dcba97fe1d7a609920698193602b1920dc8ba12c1076c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 KB (7766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8667a7512e227bad0fda3b0884c0cdbd54b4f6e69ce5bde0ae0ef7e5cd7f29d3`

```dockerfile
```

-	Layers:
	-	`sha256:681ba2cc40b0ca2008090460fd68e61a8e5efac42c751b1df975ec6356ca1f68`  
		Last Modified: Fri, 20 Sep 2024 16:57:08 GMT  
		Size: 1.6 KB (1608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:349d0bd87f841b936e8a05987608e6029da2f20262d136d4c1adbfe70a8c4df0`  
		Last Modified: Fri, 20 Sep 2024 16:57:08 GMT  
		Size: 6.2 KB (6158 bytes)  
		MIME: application/vnd.in-toto+json

## `alt:p11`

```console
$ docker pull alt@sha256:39f03d3bca1a92dc36835c28c2ba2f22ec15257e950b3930e0a3f034466e8dfb
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
$ docker pull alt@sha256:e48037f026a095882e30e0f9ee8f33c1fc7571c8c7466a55eacc08d95a48f3ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42241072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:542b3284d0344387e9e7eb6241e814082b958062272aff254ec555c7596a428a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 20 Sep 2024 08:14:31 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org]
# Fri, 20 Sep 2024 08:14:31 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3
# Fri, 20 Sep 2024 08:14:31 GMT
ADD alt-p11-x86_64.tar.xz / # buildkit
# Fri, 20 Sep 2024 08:14:31 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Fri, 20 Sep 2024 08:14:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8e347654994d5c48f07c62c053665e0aa454ce60881e73c1f12b61b2204fa2cb`  
		Last Modified: Fri, 20 Sep 2024 16:57:16 GMT  
		Size: 42.2 MB (42240880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa640bf354d10b9fb2ffc1af0fc07d4b7b52718ab7a799c3c7c338f8e56ef986`  
		Last Modified: Fri, 20 Sep 2024 16:57:15 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:p11` - unknown; unknown

```console
$ docker pull alt@sha256:7f28010e0f89fecfa3e4fdfb35e1f786affd27d102ea2c6e165da1050917503b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 KB (7223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844784fa39263cda654b35512defb959eaf9c8cbe128954b7d0ab4c4171a2b06`

```dockerfile
```

-	Layers:
	-	`sha256:ac5634e0d508a5aaa0d6af5b98c658188027b3f910f57deb4c1cdc5bc95a8cd7`  
		Last Modified: Fri, 20 Sep 2024 16:57:15 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f49a75d3e76d994fd88bdf1136642810fd37202d078865f97f4ab49d1f7c2a0d`  
		Last Modified: Fri, 20 Sep 2024 16:57:15 GMT  
		Size: 5.9 KB (5894 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:p11` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:9561b6f0108cdd823c723a2c55341aaf8183f32fb930d1ecbbb5670c07d4244f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41124926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e95366defcf0e248bbb8378487c417acd6d037f7f4d01332619d5a5dd9eb46ef`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 20 Sep 2024 08:14:31 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org]
# Fri, 20 Sep 2024 08:14:31 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3
# Fri, 20 Sep 2024 08:14:31 GMT
ADD alt-p11-aarch64.tar.xz / # buildkit
# Fri, 20 Sep 2024 08:14:31 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Fri, 20 Sep 2024 08:14:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:8917ec077017de19d2ddf1ad456796386fe634e85f6d05f5726def00084ff6e5`  
		Last Modified: Fri, 20 Sep 2024 16:58:23 GMT  
		Size: 41.1 MB (41124734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053f5603c2a576cd8edce29bdf1e7790720bd99d3348806cd29f31814d3caf0f`  
		Last Modified: Fri, 20 Sep 2024 16:58:21 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:p11` - unknown; unknown

```console
$ docker pull alt@sha256:5b26864334107aa00a9da100e44c95f08c1505ec379581436ebd8db602d8c26a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2480545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810c346d7dfceed551a3b1893cca5dcf4569e4508c5100f726765c979740a119`

```dockerfile
```

-	Layers:
	-	`sha256:6f8746c07cd666fab9907be90db1b35a415e7bbe4c125ce1ada296527cca5a78`  
		Last Modified: Fri, 20 Sep 2024 16:58:22 GMT  
		Size: 2.5 MB (2474620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:443c0aa860436929ff92831b1959d5e4885bbc25313eb88c019c52d3dce66ca9`  
		Last Modified: Fri, 20 Sep 2024 16:58:21 GMT  
		Size: 5.9 KB (5925 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:p11` - linux; 386

```console
$ docker pull alt@sha256:b9b472cbf2e83ac731455e8800e9b5f37da1a2a07b8af54fa87c736aa2e6ea36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42343403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e11d568ca81f59f563a38bb19d19ffa771569fb04f2f4f481fd96844ec14c583`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 20 Sep 2024 08:14:31 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org]
# Fri, 20 Sep 2024 08:14:31 GMT
LABEL org.opencontainers.image.licenses=ALT-Container or GPLv3
# Fri, 20 Sep 2024 08:14:31 GMT
ADD alt-p11-i586.tar.xz / # buildkit
# Fri, 20 Sep 2024 08:14:31 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Fri, 20 Sep 2024 08:14:31 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:4131ea1b9973f90a4131a5b439fd9f18c6e7740724d4b7af8e1816f1b10afdd5`  
		Last Modified: Fri, 20 Sep 2024 16:57:13 GMT  
		Size: 42.3 MB (42343211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33ff29aba0119779cc726fe73ede0fb3216217da56028ddf9bae2c8891c94e3`  
		Last Modified: Fri, 20 Sep 2024 16:57:12 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:p11` - unknown; unknown

```console
$ docker pull alt@sha256:3f1a4ba6932a6382042f5d3b6fb16d329c939ab327b937e044979a091f926bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 KB (7193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3565c0443483933c82a89797bec30ed6e5d54e1c9aa72b74bb7fa042af292610`

```dockerfile
```

-	Layers:
	-	`sha256:e257f2af928bff926425e0a09f752b453637e134989943a2a7002943cbc01491`  
		Last Modified: Fri, 20 Sep 2024 16:57:12 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e194889715aaf4f55f5866671d4f52e754ce2da1ae422bb64cacd1e34731ec14`  
		Last Modified: Fri, 20 Sep 2024 16:57:12 GMT  
		Size: 5.9 KB (5872 bytes)  
		MIME: application/vnd.in-toto+json

## `alt:sisyphus`

```console
$ docker pull alt@sha256:6efcccb2f790e40bf3ec235be6600c4dc847153d2fc84ef39aa448e5a59bc1f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `alt:sisyphus` - linux; amd64

```console
$ docker pull alt@sha256:6e009f3283650d5c8872b9025f0e7d9dba282fcb44e8591953b9110bee4162fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42268633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc276ed36c3fa674db3756e5e443e674c9b57a5e749b13707f6e2e14ccb39fd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 20 Sep 2024 08:14:17 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org]
# Fri, 20 Sep 2024 08:14:17 GMT
LABEL org.opencontainers.image.licenses=GPLv3
# Fri, 20 Sep 2024 08:14:17 GMT
ADD alt-sisyphus-x86_64.tar.xz / # buildkit
# Fri, 20 Sep 2024 08:14:17 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Fri, 20 Sep 2024 08:14:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6db279cbf7cba9af0e293a336c1306868b64f9d1b10cc3a3c95f337ba1e31fb0`  
		Last Modified: Fri, 20 Sep 2024 16:57:16 GMT  
		Size: 42.3 MB (42268439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebfb6680cf89730f591e04aee51341dd27d98e1774a45bdfdbed46b20a5c4f9`  
		Last Modified: Fri, 20 Sep 2024 16:57:15 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:sisyphus` - unknown; unknown

```console
$ docker pull alt@sha256:4d29f8ba44d77eaed7fe6984d92bedec76095b1cf847d3b9f594ebd194f57b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 KB (7232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76bff9f1e1d1fa7e54e42a7dec4659525a0d2ebe4b0d53069f95ac6efd6528bf`

```dockerfile
```

-	Layers:
	-	`sha256:3f132535ea4ed6cab15467a9cebfed3e98770929d5abdba288cc858bfefb4b83`  
		Last Modified: Fri, 20 Sep 2024 16:57:15 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53407185724f40903a1f2796094863063ef26e3bf1f8d09cb584c57a0740f938`  
		Last Modified: Fri, 20 Sep 2024 16:57:15 GMT  
		Size: 5.9 KB (5893 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:sisyphus` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:fdfd4269cc93da1508f92b24f3121650f76a29a73259075bd2d27f3ab7dd228e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41113441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6668e9c61c638acb7eb7fd42461b7e9023b443def70f8902bfe11a6d978f1136`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 20 Sep 2024 08:14:17 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org]
# Fri, 20 Sep 2024 08:14:17 GMT
LABEL org.opencontainers.image.licenses=GPLv3
# Fri, 20 Sep 2024 08:14:17 GMT
ADD alt-sisyphus-aarch64.tar.xz / # buildkit
# Fri, 20 Sep 2024 08:14:17 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Fri, 20 Sep 2024 08:14:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:d2acdfbd4d786df17102246c326f664e944056139822c16a810fda4b47442bae`  
		Last Modified: Fri, 20 Sep 2024 16:57:43 GMT  
		Size: 41.1 MB (41113249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d23e8fde7f4b3bd2c3597849cabaee242d001b349b43f22131b04fe4406a17`  
		Last Modified: Fri, 20 Sep 2024 16:57:41 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:sisyphus` - unknown; unknown

```console
$ docker pull alt@sha256:ab95e180a5b8ca07563a68b031ba8df61830799706cd5d292570dbb361de2cc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2468724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b8a95f75090efb1d60461ed28d46ef017afd74927a7e6252e81509544b704e`

```dockerfile
```

-	Layers:
	-	`sha256:b8179d803f4d1ab48588e1bc6a7155f7da96ec4117fa29a89fad296f0c87afa0`  
		Last Modified: Fri, 20 Sep 2024 16:57:42 GMT  
		Size: 2.5 MB (2462800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb4a58c12002b074b3d494331b8d9b5e08026cbc53b4a883d115b466ef77a540`  
		Last Modified: Fri, 20 Sep 2024 16:57:41 GMT  
		Size: 5.9 KB (5924 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:sisyphus` - linux; 386

```console
$ docker pull alt@sha256:fa9421f875b0faba85b0cb86866edc52efac0cd344cb737a4004b4890c9013cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42359155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a48ece6165d6fbf70fb3b4ea70f8f9b722c696480c4c00b9709acb7f7c6dccd0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 20 Sep 2024 08:14:17 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org]
# Fri, 20 Sep 2024 08:14:17 GMT
LABEL org.opencontainers.image.licenses=GPLv3
# Fri, 20 Sep 2024 08:14:17 GMT
ADD alt-sisyphus-i586.tar.xz / # buildkit
# Fri, 20 Sep 2024 08:14:17 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Fri, 20 Sep 2024 08:14:17 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:f022dbd4b326980c9d73b41f909e269966026d5ba5e36188bde0e138293b1031`  
		Last Modified: Fri, 20 Sep 2024 16:57:27 GMT  
		Size: 42.4 MB (42358962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba199c6a2d767982b29d4d63a9d58a7c2520fdad0aad2466968347bfd1cafd8`  
		Last Modified: Fri, 20 Sep 2024 16:57:25 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:sisyphus` - unknown; unknown

```console
$ docker pull alt@sha256:5b64f5d3e2d82fc03308682e2e2d6b033e71bbf0f03e7ef1e44bb1f35e9bbd76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 KB (7202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2890e4193dfade9ecdc30659da491fa89d88d0e4b1b4f110f21a642294270229`

```dockerfile
```

-	Layers:
	-	`sha256:ecae39ba4473a2b196c2871f5563c13e84a4d0dba2cfd6daef44d8d175f4552b`  
		Last Modified: Fri, 20 Sep 2024 16:57:25 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e35f5305396dd4c031b618555d29c86c0334e2cc549c6a0a15dd2dc92fbef36e`  
		Last Modified: Fri, 20 Sep 2024 16:57:25 GMT  
		Size: 5.9 KB (5871 bytes)  
		MIME: application/vnd.in-toto+json
