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
