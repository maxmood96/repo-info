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
		Last Modified: Mon, 08 Dec 2025 01:11:03 GMT  
		Size: 46.5 MB (46469180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b7edb8fa05c9eab302cf5e23d72da00078a158045945c7cd91e4e7416291b7`  
		Last Modified: Mon, 08 Dec 2025 01:10:52 GMT  
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
		Last Modified: Sat, 13 Dec 2025 12:47:17 GMT  
		Size: 2.6 MB (2602569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb8505a978441d22f7e3629438d4a154af8b3bf1be2280558f7438eb60a1eac6`  
		Last Modified: Sat, 13 Dec 2025 12:47:17 GMT  
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
		Last Modified: Tue, 09 Dec 2025 08:15:51 GMT  
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
		Last Modified: Wed, 08 Oct 2025 17:49:36 GMT  
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
		Last Modified: Wed, 08 Oct 2025 17:50:43 GMT  
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
		Last Modified: Wed, 08 Oct 2025 17:50:36 GMT  
		Size: 2.6 MB (2601237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1442934513b0dff1f98ab9a1e4883d3be0c1bae1934aa7307f92006ea710eb3c`  
		Last Modified: Wed, 08 Oct 2025 17:50:35 GMT  
		Size: 6.1 KB (6145 bytes)  
		MIME: application/vnd.in-toto+json
