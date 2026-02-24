## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:fd0913d933794f22500d1952f89c7f1df7a6ba242ba7c2e84df3f83d93a8aeb4
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
$ docker pull debian@sha256:6edbbebbd742c2975d90e175edd034781d6cee6a4e9bf30facecc12a84a74aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48489002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede2879dc63b5ca221cc3d5b50948ff052df68d3f2161978bb42c5e458591b4d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 18:51:43 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6e58fae281912a2268ff8b1f6ccc119ed0c411b436dce5c07d2b70ea9a41e0`  
		Last Modified: Tue, 24 Feb 2026 18:51:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:f4ba9163b525c8351b1a822ca85c7176f3f79ac8c7994efa972ecf3de7fc2237
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe006458bde59b6bc9184744cb6a5d86e4a23b3cc9072ba9cca987ee3bd17b15`

```dockerfile
```

-	Layers:
	-	`sha256:ac2488fc388177dd95af830b0955173914ab3462ea604762251a2a733c1e0cb2`  
		Last Modified: Tue, 24 Feb 2026 18:51:49 GMT  
		Size: 3.7 MB (3734074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5b22b84f876d9b82c10373540a7ecc9d49bb51135be1b8006f484126a1b120c`  
		Last Modified: Tue, 24 Feb 2026 18:51:50 GMT  
		Size: 5.8 KB (5803 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:c81a2fb525a673b8ace78ee16c2ad596615e2fb53234840303d2f9e6d14567ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46021885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77913cddcdba8d207daa9415d16a7c701a70f4810f067ca0d46a6c0bbfc1602c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 18:52:39 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e6dff74bad3c0a4d20c6ddf48bb9ccf82f570d23f324336b4a4e2168c71b093e`  
		Last Modified: Tue, 24 Feb 2026 18:41:45 GMT  
		Size: 46.0 MB (46021660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac1d7ff52fcba5a3a4221149ee6bbfa1916f9fa194e854c44466d8789c1881b`  
		Last Modified: Tue, 24 Feb 2026 18:52:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:727e889ac8f3b572a6a86dfbc728fe3decfe5a1d15b8119079d6a81b3747d6a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96014921246c32f8d7fb798dac1dd36e29f83648802276c4501de55a8d262dbc`

```dockerfile
```

-	Layers:
	-	`sha256:f1a262fc4966bcfe765d6a3caca8a9e25f1a0b8e8e86c6f878e23e42b484730c`  
		Last Modified: Tue, 24 Feb 2026 18:52:46 GMT  
		Size: 3.7 MB (3734275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dffcd1a0f7358787a91759ea11eaaf0d64d21e029b52c6b1a1a0d13da21467c4`  
		Last Modified: Tue, 24 Feb 2026 18:52:45 GMT  
		Size: 5.9 KB (5860 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:1f66662d217faccd56db24b0c4046ecd37de7fe54607f3cc5541077f0524dbbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44208042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e38a68e4d65bb2bdc7d78d0e8d7a8a465cbb75bdf0cb41cea46f09c633428c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 18:53:33 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:510542cb38bcb0c99cf41f8715bc80ae2e63df19b8399efbb11254ee0ddd4299`  
		Last Modified: Tue, 24 Feb 2026 18:41:53 GMT  
		Size: 44.2 MB (44207818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92560b62c62bac03834299a1b824487b7528a5f6785d4ea9be3fcadc5d06341`  
		Last Modified: Tue, 24 Feb 2026 18:53:39 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:96fd803205b39f0a8e3875eb3722ae3027c50adcd6f889a83b4cb7e5b7585029
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3742113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d22cefd75ac02477f62908a6e35d454543af32859ecfe6a6d6320fbfd7b006cd`

```dockerfile
```

-	Layers:
	-	`sha256:d474fd18d02ca1f90c655db021431de2e466fecbed35ea9290c4c46f7640a3d8`  
		Last Modified: Tue, 24 Feb 2026 18:53:39 GMT  
		Size: 3.7 MB (3736253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f496d46acd12b89302f233d81670d550e2765625b211cceb756dbe089407e25`  
		Last Modified: Tue, 24 Feb 2026 18:53:39 GMT  
		Size: 5.9 KB (5860 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:554e114ad4900bd881bdcc1f058d9b49256c1217c0b551396f9df21565be0d4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48373435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b839319de2e55400bac2132c02b99c70b19f85b907a80695270a023d73217b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 18:55:53 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffcdf732d815cbba3816a809f9db0dd3030abd029442a38ec6a8e92e3999ea9`  
		Last Modified: Tue, 24 Feb 2026 18:56:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2acc4bb0b04cd26add9dba770fa4a6cf5028d531a7504b19b329a3111575266c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb5f192affa6b567d6c4e7912e9066897a6c0f276d0b557fcc3085bc6e0f58aa`

```dockerfile
```

-	Layers:
	-	`sha256:a6f855126e14c7ec32e939dde5fe6f38d56671d66d3d7213338b1218a9f92753`  
		Last Modified: Tue, 24 Feb 2026 18:56:00 GMT  
		Size: 3.7 MB (3734289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a5fb07f5b5022149a506f3f952a2c47e56c53fdad8b16aeb8834ef0fb48cbed`  
		Last Modified: Tue, 24 Feb 2026 18:56:00 GMT  
		Size: 5.9 KB (5871 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:d0b9acbaa4fbd227bbf74fe848b41adb681d2dbe32088fce2c4381d9d15915f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49478076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89eca1b1777a901811a023b64c8689771d23f7f40e2c862f14a52671a2b3c196`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 18:52:49 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:443394a7d911f581670ce4df7959c82f7e8f0be02b5a7ba3c71bc5958012963d`  
		Last Modified: Tue, 24 Feb 2026 18:41:48 GMT  
		Size: 49.5 MB (49477853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4ff4de0f03083b1d1dcad4bd131cfb67ea6fe8375fd8e3066f566148efa474`  
		Last Modified: Tue, 24 Feb 2026 18:52:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b96a7b899c4726a0142f525cf9105dcf3ac0c0bd8000964d40ea7c862691248f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bfbe68bae4d11dc417b5b86a0283b7117ea01d002cfbd196ca67f47322c216`

```dockerfile
```

-	Layers:
	-	`sha256:a91a993c4f6bf85c411d5524fa888ec1bc22691ad237020a94d6543e313e1151`  
		Last Modified: Tue, 24 Feb 2026 18:52:55 GMT  
		Size: 3.7 MB (3731270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75bff7ea91aae2ccbb2f1a6880da7c940e64b92d9550194df8f2685bc168437a`  
		Last Modified: Tue, 24 Feb 2026 18:52:55 GMT  
		Size: 5.8 KB (5787 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:45dffb667c30a7be2a420465eba23e8dee5aa53c91bff081fbf9f9eaa4637479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48782734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:779021cee22475fada97808fec0859f7a895d59c5a19a4380164843c53672804`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 18:52:46 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:6ec71ee94fb878725e70f6a21c20349985b89066361ee1f753b3854cfa2c839a`  
		Last Modified: Tue, 24 Feb 2026 18:41:37 GMT  
		Size: 48.8 MB (48782510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a559a729ef87516aa016f61cddcb048d2a6ec9a84ed807a4c75d68de5bf70b4`  
		Last Modified: Tue, 24 Feb 2026 18:53:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ef19fb7c4361ec4796da000f8ba65478b7961027f6f92cac672c27b302de6f62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 KB (5628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0d29c45087361d6bdf85e794de836f50b265525d9b4c4e27f747b784bc9037`

```dockerfile
```

-	Layers:
	-	`sha256:c3e2dba3b2e3076145469ee57a9a6e6b0c29b0759cc45feb13ccaea4545067b9`  
		Last Modified: Tue, 24 Feb 2026 18:53:04 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:e9bf4a7a19aeae4f32ad49ed9e9706b58256fedb3212cbdbc4935535c8e1f9ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52337022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01506142057fff59173c4299780321a9c38765a780d1b0f5e198d3aded581911`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 18:52:36 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec527f8241df651142f282000ae219d11e73b99abb76fd4c1cccc5d886796d0`  
		Last Modified: Tue, 24 Feb 2026 18:52:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:45465f7bff5d16ea397b0d91bad143504a00d9eb983049a83f45bea9c6a95cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3744262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073cb3dfe3797cac687c7a755fdf4264bf0f7d2743172f4deaef9810197f77a7`

```dockerfile
```

-	Layers:
	-	`sha256:59ba012263f8c4a3f532154b9bb5503d088f5f4a8f4c4255d44a4a6d0fdc123e`  
		Last Modified: Tue, 24 Feb 2026 18:52:59 GMT  
		Size: 3.7 MB (3738432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc459f2df80b10b7deb438e9e0bb22d13af09842a812f54704a13143bebf8fb3`  
		Last Modified: Tue, 24 Feb 2026 18:52:58 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:a5243b5496c6e840d638182b461c8d594b97fefa0a019474e5356b42f0e82012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47148312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785fc925428df56e4b54b21e67f30b26d7f017dc86f7c529dbd62b24d74ccba4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 18:52:38 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:00b1871f38dea81b1982e306480bd9f97cedf7b0cb3342e4bc84925e6082ade8`  
		Last Modified: Tue, 24 Feb 2026 18:41:26 GMT  
		Size: 47.1 MB (47148087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac1d7ff52fcba5a3a4221149ee6bbfa1916f9fa194e854c44466d8789c1881b`  
		Last Modified: Tue, 24 Feb 2026 18:52:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a2c63e81a0d92085aff7ebc8733d7318e4cd6c14b2b9af738d82003a1bdcc34c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebea8f95c45b633b06d22e804fd49df78cd0c6ae910a9aa99041bf7eb8eb9a74`

```dockerfile
```

-	Layers:
	-	`sha256:dd70d036b41c707a8eac05405ec7e4d151bdd8c6691586dfbe80a08b2ac85e09`  
		Last Modified: Tue, 24 Feb 2026 18:53:00 GMT  
		Size: 3.7 MB (3730912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f652d001d0555e2b4cecddc0b28953023340a0083a80699130a5bb5a312c5c0`  
		Last Modified: Tue, 24 Feb 2026 18:53:00 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json
