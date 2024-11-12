## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:0be6372a343c9f9b40176541facf85943cc28560749d6cb3cd655f4ef3728ed3
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
$ docker pull debian@sha256:ad68e32ee12d419f462690fe80ebe88caaf4cfd3693aaf59985ee137c7e59c42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55109005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a47b0b254062a881bb40cfb19cc6d891eff61bba66d481f5ad36652fc2796ee`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2361a354fdf69fd99c824e0da06e6b4a8439e06e1a4c531114b68212f9e52d5b`  
		Last Modified: Tue, 12 Nov 2024 02:01:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:53d88db803b5d324887119a2f93dfe21bfeee1fabd8dddb76bfa5e417f8f970d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3929731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:021fbac5c52900a0fa6a43a0353b8e74dcdfd0a3f40990f6474e75432a1d8738`

```dockerfile
```

-	Layers:
	-	`sha256:6acc0a4b4984f17825f2dc240161027aa68806b99c80f25bcb0079009a2ec747`  
		Last Modified: Tue, 12 Nov 2024 02:01:49 GMT  
		Size: 3.9 MB (3923884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e334b90535967ba74fa717400cb8df89e887dc8c6ae42271d85d0589688d5d2f`  
		Last Modified: Tue, 12 Nov 2024 02:01:49 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:15de717de0a157da1914e3c6299d61d37d0c293d5fe0acb0a6f0dbb476b7b6d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50272565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30edc6fb888f95664f210938acab5f9783a1a38573e6878e2b4ace0566a774ac`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c18c6ef253e2b87a07739846b10eb333531241b80c23e3aec0643adc1b449e1a`  
		Last Modified: Tue, 12 Nov 2024 00:57:22 GMT  
		Size: 50.3 MB (50272340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b064d2b4cb61edcec878b32242fd589abf57c88da41ceb6153b035f580d2d35`  
		Last Modified: Tue, 12 Nov 2024 02:20:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:456c7a65fdfe9fbe8502717f23968dbecaffa61bdde35e76ecd67af652f5d00d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3931342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10783caa161b85db4995ef10f921e4d196ea4d435257f9207d9af35f73c8f82d`

```dockerfile
```

-	Layers:
	-	`sha256:a0cd7f55bf9cc8596bb216b119f1a0b4863b1fd5332732aa9006013731574ea1`  
		Last Modified: Tue, 12 Nov 2024 02:20:18 GMT  
		Size: 3.9 MB (3925444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1abd0dd636890991ff195b84e7322cf6691ec6e2f6271216f7e8acb85fded9a`  
		Last Modified: Tue, 12 Nov 2024 02:20:18 GMT  
		Size: 5.9 KB (5898 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:41bb591422bfde39d35fc2525bf86263547edb835c14c8f616a4c086abde8bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53757297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb4e65d513fd1616a7a2a6b7333f15f66ac30233cce83d5210694396b9ec4b2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a839664fe62f615da74af799f94ccbc890a15d0f78470aac54302c2fd5475615`  
		Last Modified: Tue, 12 Nov 2024 00:57:41 GMT  
		Size: 53.8 MB (53757072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76aa55ac52f2277851d46572b8a5767c71668df15c6634e16d7c507b3895035d`  
		Last Modified: Tue, 12 Nov 2024 02:22:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ada0219d8145624213cc958ecdf27e876c37aed10963395661271c40fe898287
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3929377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19cd0236cda16e6fb8fb86dead05d3c5e3ce3d9bf142585456af75f8feb869c`

```dockerfile
```

-	Layers:
	-	`sha256:7c0cc88469415dd7ac44f4c490d1f408908112dd32ef6825a6887dfe7b15f857`  
		Last Modified: Tue, 12 Nov 2024 02:22:11 GMT  
		Size: 3.9 MB (3923462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:028570c9b8193376b7900334657b3e004de898d84e186088e5376dc222a6204a`  
		Last Modified: Tue, 12 Nov 2024 02:22:10 GMT  
		Size: 5.9 KB (5915 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:4e183723f2df7e38f3804ab53c9c977d17253cf9de5dabb48e4e9a9ee17fcc57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56093908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:327e9a68178d996842496a8cc87f677e40bdf902c9cdf4d1132370cb3e0d9995`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Mon, 11 Nov 2024 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:401daab178046178ea38abc84ce80fe4a7e7530a75e6b198a161344b358750f7`  
		Last Modified: Tue, 12 Nov 2024 00:54:54 GMT  
		Size: 56.1 MB (56093682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fae5c9d87cf89c44a1d23e8a51a88c4d84b6bd167a8b80bab1b3fb3e41d834c`  
		Last Modified: Tue, 12 Nov 2024 02:01:59 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:793022b658257993e55fd6182a383f5260bab25fc554c83d83b6b3fdc7f00127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3926219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe7e24f11f8b65aabcf3709779584900a94ff82ae050ee45c2299bd236c2079`

```dockerfile
```

-	Layers:
	-	`sha256:021a2a45b2b87d34200a76937bd9b6a8cde88fc6ab3db02555a07dc301414612`  
		Last Modified: Tue, 12 Nov 2024 02:02:00 GMT  
		Size: 3.9 MB (3920389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce165645f12802ffd62b62371603f1138171a6e0194abd03e24f968decdb0988`  
		Last Modified: Tue, 12 Nov 2024 02:02:00 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.in-toto+json
