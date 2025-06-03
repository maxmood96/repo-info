## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:1abef06d632c31d5953f21f410095914abc9be2a49b88f7bf6bca68f9c6f50ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `debian:bullseye-backports` - linux; amd64

```console
$ docker pull debian@sha256:e008a568786bd234bbf2475c8bb6acde853f9db45a69d99d4c295feddff9ae3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53750420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88afe97d55f05c03c64ded94c0aff809419de1832d65d18d32db7834ea1fdf3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a67e96280abcd1421c477e084e8ce3d3c7624417508550603760bd09a7c4785`  
		Last Modified: Tue, 03 Jun 2025 13:36:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1044badcc373e0c815b31ca9ac1be3b132cc07542cde9904962959f63a57a117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3944571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56db4c507cf3e2e4b20bfb36d41fea002f12187ef6583b0e75a1921eef44b516`

```dockerfile
```

-	Layers:
	-	`sha256:dbd62f129dc09bc47d299d3b3c6ed10abc547bf2452dd260252464f31fe817b3`  
		Last Modified: Tue, 03 Jun 2025 21:26:35 GMT  
		Size: 3.9 MB (3938724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9589472b0a55fb0910d46323048144b8a95710dff945e36be872c03ed13acbf6`  
		Last Modified: Tue, 03 Jun 2025 21:26:36 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:68e3161ce946f8c556c0420abc060d8dfcbb10e7bd3d02a0dae712032e0532bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49042214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036097a649b5a4b4de1c18d1f65f6aa8976ee3189196d64f83869357b1c3ef7e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2bf062f1f44f96722293994387f4b88016e2f0a9f49c7f09b2ceffefc7717199`  
		Last Modified: Tue, 03 Jun 2025 13:43:06 GMT  
		Size: 49.0 MB (49041988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f745bdd4ba55e0f04125ae65785a00e65b718adedb58c519719fadd30a58da`  
		Last Modified: Wed, 21 May 2025 23:12:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8638a0d99d0b07bea5e4e7145e787c26d737504cac1aa63d104bb0936b804056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b32e6095edd7b0d3a96c9e633cd3411710c0352fc892cc6583bfcb0abcd50424`

```dockerfile
```

-	Layers:
	-	`sha256:d630b1d26291511955d74a8de414e220e4196fb92e320b6a657f58de09b692b3`  
		Last Modified: Wed, 21 May 2025 23:12:21 GMT  
		Size: 3.9 MB (3940286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a89aa6602d54b8332fe1e3ae2ebba492a50ac66ae57451795d86f5fe6e4efd5`  
		Last Modified: Wed, 21 May 2025 23:12:20 GMT  
		Size: 5.9 KB (5899 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:715217eb20cac2ca9c84c93d337f91fd842457a86e0d48a9d70f4e7b7e892e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52247981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6516fe9c8a248a600851757214d8e31ea45d7b333afbbc8f45658039f54b21`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd28ac5b9647a0a0d81cce49bc39189e7902a1d50f14e065f3545e01f1bd9be`  
		Last Modified: Tue, 03 Jun 2025 20:03:23 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:50675200edd276d7a583c1c8bba5e093b1115735b35d034ebe8bf96bdede5756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3944218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ac61a224f64be3bc5cf824ba41b5e4d669b70eb3086eaf3ed9a079e8b80b96`

```dockerfile
```

-	Layers:
	-	`sha256:91c85835991279507e8e0d76a14b65f62caa11774c1d754ba8473167e9e5054a`  
		Last Modified: Wed, 21 May 2025 23:11:49 GMT  
		Size: 3.9 MB (3938304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36d33e949aae90ca365a0592bfcf231b26794146a449a1e306b772e1ec992d4c`  
		Last Modified: Wed, 21 May 2025 23:11:49 GMT  
		Size: 5.9 KB (5914 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:e08ce94c94c386eb40b3bc2f9b251f07d9faaf2161e8115525624161a4f2ecad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54686007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c02adbd61950fbcb2887c8bad85a7bec968d72b14ebfa414b2bbc0d1ac10ecfe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6c1a0525f904d970c0719d0ae307af1606eed8214108a47c9374eaffab5c71ae`  
		Last Modified: Tue, 03 Jun 2025 13:41:46 GMT  
		Size: 54.7 MB (54685782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b344893d29abd05554f275606b19645b290d79cbeb327be56e1dbfd959362dc5`  
		Last Modified: Wed, 21 May 2025 23:11:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:466ddd838d43ab770ea4ee2f72abbb2f00d62034c8bb0d04c9987872d3f89f9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3941108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:761a6d662e74f6feaf71f88293ad5693bc4c166ff1c81f00504f70f503853792`

```dockerfile
```

-	Layers:
	-	`sha256:56d5189ed96f60930bb9affdc3c4129393a2ecb656f129864eed9909ce47442c`  
		Last Modified: Wed, 21 May 2025 23:11:44 GMT  
		Size: 3.9 MB (3935278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0686c70e1d22db932c2eb40d5027d0a04d980510ecdae2095ba3e91a5ef66636`  
		Last Modified: Wed, 21 May 2025 23:11:44 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.in-toto+json
