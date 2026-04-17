## `alt:sisyphus`

```console
$ docker pull alt@sha256:2eee0cd037611c8292dc0af2a83054007b32dec2210ad56a3df89a6f266fae0e
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
$ docker pull alt@sha256:cf999cd1d08e56e22566416b5853c9642ad0b416c2a469abffd99cf4bd08c41e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46671247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:624ee8b67d720963ba05cbba24772d35cc9b86ccc5199dcb6aa8d298eba91a38`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Apr 2026 23:15:21 GMT
LABEL org.opencontainers.image.authors=Alexey Shabalin <shaba@altlinux.org>,Nadezhda Fedorova <fedor@altlinux.org> org.opencontainers.image.licenses=GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Thu, 16 Apr 2026 23:15:21 GMT
ADD alt-sisyphus-x86_64.tar.xz / # buildkit
# Thu, 16 Apr 2026 23:15:21 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Thu, 16 Apr 2026 23:15:21 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:1b5644609165ad036ef37371f0beaa3e2b26d406aa789d201e731a9b6a4ea69a`  
		Last Modified: Thu, 16 Apr 2026 23:15:32 GMT  
		Size: 46.7 MB (46671056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ee7ac6a4ecb2de839ac0e451349f43f854a4e97ec08279447e86ab1052f7d5`  
		Last Modified: Thu, 16 Apr 2026 23:15:30 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:sisyphus` - unknown; unknown

```console
$ docker pull alt@sha256:c1cea715b465d08faab3a94d91c88607f851babdebb6a5e6c92bd326cb8bb458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2654788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:948740c242db5a3cc8a51c344e59c5af5b5014de2629bc4a3c10ab6f124951b6`

```dockerfile
```

-	Layers:
	-	`sha256:17779ed4a366593489e4978f9527d8847b9d20e69821ebfbf7a86e3d6ec412b7`  
		Last Modified: Thu, 16 Apr 2026 23:15:31 GMT  
		Size: 2.6 MB (2648688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c6607e2d27a71c3904f4ecbdc2d3be1fc19ea3aea4904ba38b2ee9294f81cb7`  
		Last Modified: Thu, 16 Apr 2026 23:15:30 GMT  
		Size: 6.1 KB (6100 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:sisyphus` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:69a25ec1cb0e2b8379862d550045f2461bc2ee8992524df93e8a0cba5a540081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45365617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741807c2699cc0c9815228243dadb07dc8768efd8d9d89d777a828b28e8ea9ec`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Apr 2026 23:16:00 GMT
LABEL org.opencontainers.image.authors=Alexey Shabalin <shaba@altlinux.org>,Nadezhda Fedorova <fedor@altlinux.org> org.opencontainers.image.licenses=GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Thu, 16 Apr 2026 23:16:00 GMT
ADD alt-sisyphus-aarch64.tar.xz / # buildkit
# Thu, 16 Apr 2026 23:16:00 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Thu, 16 Apr 2026 23:16:00 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:75777fc776b0beceb2660d76442c5c89295cc37363f8b4be681a6c0272ae7fcb`  
		Last Modified: Thu, 16 Apr 2026 23:16:12 GMT  
		Size: 45.4 MB (45365425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b216283123311e4dc4c72b7792baadfeaccd864e9faf8b7d2a20c74724bff6a7`  
		Last Modified: Thu, 16 Apr 2026 23:16:11 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:sisyphus` - unknown; unknown

```console
$ docker pull alt@sha256:ddf12fd15401c195e2babb4ab395657002d945384b2aa6180ad2224adab98c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2654251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a7a25515414628d4181fdadcb3bed211a01fe1a327207e808499f09f62a9c2c`

```dockerfile
```

-	Layers:
	-	`sha256:7103b817dce6f00e69a54890bc1158106f89162e132396c9268d8ec885f3459a`  
		Last Modified: Thu, 16 Apr 2026 23:16:11 GMT  
		Size: 2.6 MB (2648105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ecdbd8059e7bc75ad08339c56274b37ecc2086fbd7f98303d6ffd8071874111`  
		Last Modified: Thu, 16 Apr 2026 23:16:11 GMT  
		Size: 6.1 KB (6146 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:sisyphus` - linux; 386

```console
$ docker pull alt@sha256:635394496fbee2229113497614a91cdfcc739def5ba407b91300739986ae5bd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46671955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c291ed8cd8b982100e395e1d4445ea5dbaa66c8dccc315435798b8087b3fece9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Apr 2026 23:15:45 GMT
LABEL org.opencontainers.image.authors=Alexey Shabalin <shaba@altlinux.org>,Nadezhda Fedorova <fedor@altlinux.org> org.opencontainers.image.licenses=GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Thu, 16 Apr 2026 23:15:45 GMT
ADD alt-sisyphus-i586.tar.xz / # buildkit
# Thu, 16 Apr 2026 23:15:47 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Thu, 16 Apr 2026 23:15:47 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:84495811af3f80058c244a4853043768acd8765181997dcc7e6f1915e3e8ea4b`  
		Last Modified: Thu, 16 Apr 2026 23:16:00 GMT  
		Size: 46.7 MB (46671763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1213baf35137df0a0362dd1d94e01d9598ba2a3b4eabc5ced476e5727a078320`  
		Last Modified: Thu, 16 Apr 2026 23:15:58 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:sisyphus` - unknown; unknown

```console
$ docker pull alt@sha256:e4b893293b7016a9fb32da440bb282b96d7c5cb468cd9a8c74e64746488b0a2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2653490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9181f57b295060edbf62fd0d45409b56db52c188eadeb1f7b145d73168c7c688`

```dockerfile
```

-	Layers:
	-	`sha256:a49782ec2281344fa032001e26ee139cda38fbae34a79cfa929a5ba10bbe94aa`  
		Last Modified: Thu, 16 Apr 2026 23:15:58 GMT  
		Size: 2.6 MB (2647414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5641ee5446e9350957e06d620c8973287079026300f2c46a122d4041dc1b13a5`  
		Last Modified: Thu, 16 Apr 2026 23:15:58 GMT  
		Size: 6.1 KB (6076 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:sisyphus` - linux; riscv64

```console
$ docker pull alt@sha256:3cf5bc6acfc8273dc2052faea43de4db6ad0007cd0cd63af5081bcc90e81332b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 MB (44486087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41d2a588d57b588ae5273d2a515302542b60a3ceda71458c6a4f6c0e93075f90`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 22 Jan 2026 05:23:03 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Nadezhda Fedorova <fedor@altlinux.org>]
# Thu, 22 Jan 2026 05:23:03 GMT
LABEL org.opencontainers.image.licenses=GPLv3 org.opencontainers.image.title=alt org.opencontainers.image.description=Minimal image org.opencontainers.image.vendor=ALT Linux Team
# Thu, 22 Jan 2026 05:23:03 GMT
ADD alt-sisyphus-riscv64.tar.xz / # buildkit
# Thu, 22 Jan 2026 05:23:04 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Thu, 22 Jan 2026 05:23:04 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:ba25e668b40b2efaa9085cfdb237dd3fdac12bee44a47b6d0f8175d7c3eaa120`  
		Last Modified: Thu, 22 Jan 2026 05:24:49 GMT  
		Size: 44.5 MB (44485897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f644b3bca52aac38924d1e8d7515b0cb5ec91079fe48391b191fff649a9e5d`  
		Last Modified: Thu, 22 Jan 2026 05:24:42 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:sisyphus` - unknown; unknown

```console
$ docker pull alt@sha256:52c85bd8165d1b5da180d18ce920bf9ce8a74fa34e27d1b515834cf7883c8a6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2623698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18908b805353e0f803018b9e1dd6005bf5bd9b4b37efe28ddc7accfa6f6309bd`

```dockerfile
```

-	Layers:
	-	`sha256:7398354c4d28200d04aa4b30f5da872e5946e83d13d627671a9f01c40d73aa65`  
		Last Modified: Thu, 22 Jan 2026 05:24:42 GMT  
		Size: 2.6 MB (2617596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6598b1c5289c5c942753cee096d29bcbe5743711a88b57e9a06da50f3ed0ae98`  
		Last Modified: Thu, 22 Jan 2026 05:24:42 GMT  
		Size: 6.1 KB (6102 bytes)  
		MIME: application/vnd.in-toto+json
