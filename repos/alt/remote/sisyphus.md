## `alt:sisyphus`

```console
$ docker pull alt@sha256:452819527c36dd7177edde46d0e2a69dc7319244e71582cd8f4924b2ae699a1e
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
$ docker pull alt@sha256:027ddf9216e3b85d1969434574f2b73323edcd9707dfc4047df8d271e77a38d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42196208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3841439d2581d36d88a101575c24c119ba864302b16523261639ce8e68133c1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 May 2024 15:35:25 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Fri, 03 May 2024 15:35:25 GMT
ADD alt-sisyphus-x86_64.tar.xz / # buildkit
# Fri, 03 May 2024 15:35:25 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Fri, 03 May 2024 15:35:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:6a74e13e52ed9606c81302565eae934f0556dc9e25c4fd35e7c80a8a66875d49`  
		Last Modified: Mon, 08 Jul 2024 18:58:56 GMT  
		Size: 42.2 MB (42196016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869c2e05b825c9285857494015b85e76d835df03adb6c4dc09baae74c7a7dd07`  
		Last Modified: Mon, 08 Jul 2024 18:58:56 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:sisyphus` - unknown; unknown

```console
$ docker pull alt@sha256:b58983270a8ac3b09060cb4cae347a2a2dd58dd14728f831b204f701bebf86f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2445919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf059aa24a306d770a2875caf737bb1438d0c7323e4f4655033d49cb7a005a3`

```dockerfile
```

-	Layers:
	-	`sha256:2128b8d5d704b565cfde0af72ef6a67ed6b7a48dfaedc1e6497e5c6ded7f1a53`  
		Last Modified: Mon, 08 Jul 2024 18:58:56 GMT  
		Size: 2.4 MB (2440092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95cf2ab995b9d243358ae563f26d90558cd5f09d92da5c0c704d28ec25556545`  
		Last Modified: Mon, 08 Jul 2024 18:58:56 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:sisyphus` - linux; arm64 variant v8

```console
$ docker pull alt@sha256:0ae2e69b0eedbfdadea2afc7e594f69de841bbd2ad20b9cdc3f58b92ae9699fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.0 MB (41048669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba44bcd99cc8fc2b264153d177479fe187dffaa8f352101b05f24610801df53`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 May 2024 15:35:25 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Fri, 03 May 2024 15:35:25 GMT
ADD alt-sisyphus-aarch64.tar.xz / # buildkit
# Fri, 03 May 2024 15:35:25 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Fri, 03 May 2024 15:35:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:565414905a8793b56848e8581b74760359d1d3e69c27fe8a2e641f32008b84b5`  
		Last Modified: Mon, 08 Jul 2024 19:09:25 GMT  
		Size: 41.0 MB (41048476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0edca5e61bee33cc540272dad77fff6757bdf29c39463b04b6fa5cf64e50d2`  
		Last Modified: Mon, 08 Jul 2024 19:09:23 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:sisyphus` - unknown; unknown

```console
$ docker pull alt@sha256:3eecfd4aeb28e3dc2fd10303f3e63aeaaab6dc6fd38cf6f390c235a2dd9dbb17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2445369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4502ee4fc8f13037bb3793baeb85c287197adcde6d78e9508a3d11c4bf151de8`

```dockerfile
```

-	Layers:
	-	`sha256:53b263831f30bbb3632237a05b1dec6bcf265500fdb26996c3b3be24f783e093`  
		Last Modified: Mon, 08 Jul 2024 19:09:24 GMT  
		Size: 2.4 MB (2439508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70dfc29dbb70ef0956f36828b30c675f22671c4d6b6f0367398d73f254ddbec4`  
		Last Modified: Mon, 08 Jul 2024 19:09:23 GMT  
		Size: 5.9 KB (5861 bytes)  
		MIME: application/vnd.in-toto+json

### `alt:sisyphus` - linux; 386

```console
$ docker pull alt@sha256:9bb2ca2666bf7f1e3c4d02830957c2c12c21b61ca5e637c96d34cde2c2a1bc12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42297762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd7ad88dd95418ec708905a3b5ebd68ff044f0944ccd6d6dccab010bb95a7bd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 May 2024 15:35:25 GMT
MAINTAINER [Alexey Shabalin <shaba@altlinux.org>] [Mikhail Gordeev <obirvalger@altlinux.org]
# Fri, 03 May 2024 15:35:25 GMT
ADD alt-sisyphus-i586.tar.xz / # buildkit
# Fri, 03 May 2024 15:35:25 GMT
RUN true > /etc/security/limits.d/50-defaults.conf # buildkit
# Fri, 03 May 2024 15:35:25 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:07ccd7cdd088eda5e5deaae96b55e7a07c461bf0505499bb6a995ace28b84f94`  
		Last Modified: Mon, 08 Jul 2024 18:58:49 GMT  
		Size: 42.3 MB (42297571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3c5ed0a3c9c8c97b22295b56e905054e5d56bcfba677cbb474c23aa4e6c3b8`  
		Last Modified: Mon, 08 Jul 2024 18:58:47 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `alt:sisyphus` - unknown; unknown

```console
$ docker pull alt@sha256:c3b35036e4e71ee8f15fa4135c29a4f2cb2013d560ed5c0f6b3c158d6c66f197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2444643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42098d60e0b55e59df382c754ccee01d89fd8158eb091eb2b8fade3a7d8b97e5`

```dockerfile
```

-	Layers:
	-	`sha256:72edd77435039d6ee0f25d216c86c191fe36595426613e55973daf7cd65dd542`  
		Last Modified: Mon, 08 Jul 2024 18:58:46 GMT  
		Size: 2.4 MB (2438835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3548ed7bd86bd8e33a57fc11c51c05a94e1f4a2e4fb8fe64fbd3517f6a1fed1b`  
		Last Modified: Mon, 08 Jul 2024 18:58:47 GMT  
		Size: 5.8 KB (5808 bytes)  
		MIME: application/vnd.in-toto+json
