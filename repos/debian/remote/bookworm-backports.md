## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:19f1211e87007eddb741622b6cb505fab14c389be078b6ca15c58d6431a6db3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:5516aa153e98c06518ed1222c3b86b40b7eaa77ddefea52bc8f3bfc4add71ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48489047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ad053d77fe2c5a98cc2c7eac07ab39c319153e04ce36d3998ad0ec8c39e0ed`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:16:12 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56504771fc6aca8e8579deed286d80d59e162bdc3c8f7736fa9cf2753d0a5577`  
		Last Modified: Tue, 07 Apr 2026 01:16:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:54fe68ae58d5ddebaeaf6b0ffc4536a9423c33b4d9bcfd20f5ac52fb1accd4cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a850ef8dbfd1311949b30a20fdfa13a3dece5acc76b0b727bd840c55ec61c86b`

```dockerfile
```

-	Layers:
	-	`sha256:933be5d1c06ae7dbd415d58ff0a1219abf4e7556166a5795caaf5dec0ef82f77`  
		Last Modified: Tue, 07 Apr 2026 01:16:18 GMT  
		Size: 3.7 MB (3734074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ede7927b46b0daa9d524e4894abbdf499db2508b2821b28dbdd87dc5bcb37032`  
		Last Modified: Tue, 07 Apr 2026 01:16:18 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:59efb53adfb2a296750714858eb2e554f51dbbe16f72c57c4e26c6baec59eada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46021892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525d6c0209c6c3e0e91faf2861f424dcea8bf973b3908477f6c18b17185b02f2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:31:55 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c4564d3f444801f4c4ab3e01fd62e7dd3bd91054769ac22888b9bef61823a830`  
		Last Modified: Tue, 07 Apr 2026 00:10:20 GMT  
		Size: 46.0 MB (46021666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a90a216d1031db6d29303b33d55963a8cceef8f1b9ed71480501428b334783f`  
		Last Modified: Tue, 07 Apr 2026 01:32:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:0de792e8c430dab2edc6ecee7fd56e823e43a55e11c8e7a28bab42cac15e4a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4031aa4d7430ecc6d94442595fe2e697cb944ae2c52770c0bbad50d78525200`

```dockerfile
```

-	Layers:
	-	`sha256:27dfe2774b44de12c989a16f2e5885e8bc18cfe0109eee5f0f11059897054187`  
		Last Modified: Tue, 07 Apr 2026 01:32:01 GMT  
		Size: 3.7 MB (3734275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1422265204b9896932260e73a90cc80425689d38db0fae263eab224c2913ea93`  
		Last Modified: Tue, 07 Apr 2026 01:32:01 GMT  
		Size: 5.9 KB (5860 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:10d105be31efbfb831a15691cc7361a72a89142ae0249218e707635e7329b4de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44208042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfae90791f611e444de5c3ee96c373c873017327546cd921df3d37b1ed276b75`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:15:15 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a99a9abe3964725d9016ffc8402d9cffc28e94f404db8e764ca9583f2090145e`  
		Last Modified: Tue, 07 Apr 2026 00:58:42 GMT  
		Size: 44.2 MB (44207817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858e5cc4d843cd5bcafce73daada3047a79a17d21759a21b6f90770c4ebc2632`  
		Last Modified: Tue, 07 Apr 2026 01:15:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1fc79754a4da4238a096f0184ef051ce354714e9f4bdf2a107477503e2797682
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3742113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ccb5a0506e99fd0dc1fdc5dbc715fb4602c48b7e894c4de45a9d807b515a8d`

```dockerfile
```

-	Layers:
	-	`sha256:fc7e155ba98bb6a6655b258e5a220933a59c92d3e1e0f42aac61a24bb0c4f746`  
		Last Modified: Tue, 07 Apr 2026 01:15:22 GMT  
		Size: 3.7 MB (3736253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1d5e8cb7303b67384fd0639de035568d6ca5f825eda73a9a7a01beb07d75a9b`  
		Last Modified: Tue, 07 Apr 2026 01:15:21 GMT  
		Size: 5.9 KB (5860 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:4b6f1171b703f8f59b03181cad79625ab14d11feb835445324de92592ac933e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48373487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72c5760e5d576ff6d98e19810b265f6bb3c7d3e606dde8691db790a862c24156`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:15:13 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac15f2a787b24c385b08102cd4486b45982768bb0a36dc58741d19be7b130a02`  
		Last Modified: Tue, 07 Apr 2026 01:15:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c6858f34f8626e31ce433c8a8d742f04b8ac73357e7b3c0507e005cafe408438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993da0ef0f35426e892e5da54f9d61cd78f63e3e0aeeb304d814664ae58f14ba`

```dockerfile
```

-	Layers:
	-	`sha256:957e7cc5e960736e99950103285fd387a227a664019c9f822af44ebff1c33d08`  
		Last Modified: Tue, 07 Apr 2026 01:15:20 GMT  
		Size: 3.7 MB (3734289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ef68a1b705d92a72aeda009fd435a472026a4ea64d240c90b19263f6b9d1a74`  
		Last Modified: Tue, 07 Apr 2026 01:15:20 GMT  
		Size: 5.9 KB (5872 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:75d097f309cb8bd63d0fd88d3dee4e862b29b8425416ffcd8cd24f3da8b53129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49478138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b44cca8449fa4c5e18e23fdcef2c966d3f491232e50d95b90043cf39484aec19`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:15:24 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6b838e591408b61fcf923bcc567649c4053d737a0dcf488cb215bcd633b7d70f`  
		Last Modified: Tue, 07 Apr 2026 00:10:40 GMT  
		Size: 49.5 MB (49477915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b09c7b20dc45df2879aeb4e61a350bc4444bc4bb69f1046c9609227ad7a852`  
		Last Modified: Tue, 07 Apr 2026 01:15:31 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:0c594aaf93adc89abfb12c42bde7d30b49dd89ef348ec4e6adeec8271d6bad21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563af9ce58e61087ae6dd8083bc4200bf0e6fdca47e3529d22cdb96039913072`

```dockerfile
```

-	Layers:
	-	`sha256:a1f81dc846478326b845a167a9a72bf7c7d08b384eba156901923e0490b4cfe7`  
		Last Modified: Tue, 07 Apr 2026 01:15:31 GMT  
		Size: 3.7 MB (3731270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:027d259444e83e44264075f5eaa4ba854be8b8be6eff56b4bea02a5e9de24e98`  
		Last Modified: Tue, 07 Apr 2026 01:15:31 GMT  
		Size: 5.8 KB (5787 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:a87169fb4713485071a74e52941aba3675a395c01f89ea4aef5fcb87485cdc8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48782817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99908fd8b2f56be4c3d8506eb96f70448d04e64709ea777b2b3b880c39ddb090`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:16:33 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7a9b4a7963b008240d9a254ca4fd1193c938bed0a9c6fe9c04630f13b1a17a44`  
		Last Modified: Tue, 07 Apr 2026 00:09:37 GMT  
		Size: 48.8 MB (48782593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0df48940354ba6eab3525f68ed13f7d56d4c44cfc533b7a7b0abdf8614e42e0`  
		Last Modified: Tue, 07 Apr 2026 01:16:51 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e8e4cba4aa9fb70318285ccd8c84222d92349388563b69cd7016dafee3ded110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 KB (5628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bde046e9c07b4b551728e046abfb0f64ed35ccff50a56bb78a84ff79f7fc836`

```dockerfile
```

-	Layers:
	-	`sha256:10a5942bae8a3adf44a94ea50b144d3e46b843cb793fb3e255cfebf22ab7c52b`  
		Last Modified: Tue, 07 Apr 2026 01:16:51 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:a1acda4117a8e54b991d4ccc10f53c3de21e4d1878fa1ac3c9313c95005f5cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52337163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82fb0426ba4ba75e408046ad5a2b7b10cda6799ff0d3d15b5e81312104bc8da7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:15:32 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6b775f7ad22043f8bb75d535d8a1279e43453a08a4a9e6a0b48c020c9b387079`  
		Last Modified: Tue, 07 Apr 2026 00:09:43 GMT  
		Size: 52.3 MB (52336938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6758f39ca54389f9a277f38a7bb3476c7bf14ee0a9d3bf6cec18b29dde4c5969`  
		Last Modified: Tue, 07 Apr 2026 01:15:47 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:aeec6c6f77dc850a7cf0afcd963e502505fd4ad53c063bea92d046a6e965060d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3744261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9c83f6446c3d9bebc58c9ba82756ca6e3265a9558ff346f6a8f6aff73b4115e`

```dockerfile
```

-	Layers:
	-	`sha256:c16507a720c6c621c7ea54c83a4b3a50f9bd1b104cf38539f50340fba58ef12f`  
		Last Modified: Tue, 07 Apr 2026 01:15:48 GMT  
		Size: 3.7 MB (3738432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:733ac97c92aa74cb56ba8cf98263f64c8b77617b30a466e049b2bde060498ff7`  
		Last Modified: Tue, 07 Apr 2026 01:15:47 GMT  
		Size: 5.8 KB (5829 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:46e13d00f32d1db20431360f03484d06891832b3f3d508357258d210161ea392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47148310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:166256586be026246e69ae887cf136ad4aef397babc47cfeeebd4d8b87a32f18`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:15:58 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:40ecbf1d4e17f6b072e6cef463823baec601d9f21c9dc33d98bd258448a986f6`  
		Last Modified: Tue, 07 Apr 2026 00:10:32 GMT  
		Size: 47.1 MB (47148084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac437eb773e463ebd8a2b5779f0142ad1d9a10901e6781261d6baf85a84dd230`  
		Last Modified: Tue, 07 Apr 2026 01:16:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8001fb5ee685a38a651579bcc2f5d7110a1f9a6f71443630ffad7b5d56a3e171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:751e04d61ca6c1f5e01d71a54d214d916ede98c8bb958068b86ca186d3554dd1`

```dockerfile
```

-	Layers:
	-	`sha256:a6da6b98ab25aec1e1a4695768495192109a2377b69dbf2088d59a29f80ba1b0`  
		Last Modified: Tue, 07 Apr 2026 01:16:17 GMT  
		Size: 3.7 MB (3730912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f7f0d2242a5a9769ecc9c905fc9ed4f72f40d776935f3243ad19366fb150965`  
		Last Modified: Tue, 07 Apr 2026 01:16:17 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json
