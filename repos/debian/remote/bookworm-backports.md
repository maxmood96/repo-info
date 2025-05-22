## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:1f690907b013fcef6a421683e75af52d184a17f101ab434629d360c4d156aba9
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
$ docker pull debian@sha256:c155b0a348ec4e38464229efd8d1ed42257a853de24830e47e36d5bf07af906e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48488470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fbba71c5bc6338332bc6d48a89a78e1d1fc73c4847fc06b2b16864e2f1279b9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Wed, 21 May 2025 22:27:42 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30915d07cef86368a0f2d38f67d262c57fa3b20203d1da795049afae6f39cee`  
		Last Modified: Wed, 21 May 2025 23:12:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:61bf190b38c3149af1570e47b7e26935419c768f431689ec6e74a0c4a9d0667a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a92a475cce19b9ee5fd12133d5b24b0235f046fba47f6e7712b88c105ab495d7`

```dockerfile
```

-	Layers:
	-	`sha256:02312358cf7282561af04ece241ccf877fa93c0452771a11562877ba2d29b54f`  
		Last Modified: Wed, 21 May 2025 23:12:02 GMT  
		Size: 3.6 MB (3635844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e67cd22e3673db60d5204b83e301d38e3cc84387edc89e13af61e25c5ae39136`  
		Last Modified: Wed, 21 May 2025 23:12:01 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:bb97b930b3f8bf3c429c9884321814858267b52831abe63d222d676c86e3aa82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46021707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59900f38dcb8e41cc54cfe97368a4d50846701ea4efb0db941c69adf1b828c85`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d34b66573dd99436757429c603646ae3e6d1948a3fa85413a39cf069620a7229`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 46.0 MB (46021484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40a3040ff3b0b978b49c5ee5bf1c2e86b7e2e1638ff5c1547ac4fa9343ef9e3`  
		Last Modified: Wed, 21 May 2025 23:11:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:74aca4d6e147ee4c544e73ec65432716b350b9ad8553a8777496c7e30f37fa76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b497ac2e89fddcb3b6af7c50a27f837b80aefce5f882f4c6c431bf9798c4896`

```dockerfile
```

-	Layers:
	-	`sha256:2d9bc4b9c3ca39ef4100462e7208717471b25fe78634e247f17873762b557878`  
		Last Modified: Wed, 21 May 2025 23:11:20 GMT  
		Size: 3.6 MB (3636045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d63618b2bf0df4e54d55a1fc9e38257a194baa681addf5b22395a76ab4b02bf`  
		Last Modified: Wed, 21 May 2025 23:11:19 GMT  
		Size: 5.9 KB (5898 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:b7a3567f26ec695f4cc888d8f38fffb311e88cbf229165aab3164bb062a0747e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44202994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8e1645cb4d3db2f804968671d9a37d1fb2c445b2cddf79b5dc1961bd4dd1d3e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3a781f536825e084b88c231841be4d1c7df016a4aa2ebdd27d7431b5f1ab3419`  
		Last Modified: Wed, 21 May 2025 22:27:37 GMT  
		Size: 44.2 MB (44202771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40a3040ff3b0b978b49c5ee5bf1c2e86b7e2e1638ff5c1547ac4fa9343ef9e3`  
		Last Modified: Wed, 21 May 2025 23:11:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e50a72d7b5c464a88ee3ffe80d7b22e3d53cf0fa1d7e835daa7859fb26e0b179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3643922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:644fa8e2a132154e096c2b26976e45a25ff6650db84df33c17a815e3ebfb7808`

```dockerfile
```

-	Layers:
	-	`sha256:8b10162136e009716da30c11edb17587c4fe0060fb4fa1a4989c3269569494b9`  
		Last Modified: Wed, 21 May 2025 23:11:21 GMT  
		Size: 3.6 MB (3638023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15083581849d16937d6cb19ab59800010ec1cdd25b7b27c7547351586d2419bd`  
		Last Modified: Wed, 21 May 2025 23:11:20 GMT  
		Size: 5.9 KB (5899 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:fe16f9d046b25ec8b34dacf7922abfa2ad84fe44a021328195797d97de31a3e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48327407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e1aeaacb4399023a716619751f744caa7ef9829dde17f7b45425af2fb59e3c7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:285699ba5d800ce9936d5a4ffbd14ed8772aacae497e82c5c635e723e353ebb3`  
		Last Modified: Wed, 21 May 2025 23:11:06 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6ae7ea03ab9a17bdf96abb14e732a351920046741d3aaf25da88e1ffa0cefc2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af1094560483f9c9a5aca622cbf319bb9a809d643b89cd50a229c94d1dabd588`

```dockerfile
```

-	Layers:
	-	`sha256:078501fdbb3984d573dee53910ab5050483ca87d8112e0d1e26c2b2cfa8be301`  
		Last Modified: Wed, 21 May 2025 23:11:06 GMT  
		Size: 3.6 MB (3636059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:006e2fdb4484d50aadcfb8c6290dc397a30fd7a4e191e609dac09a784cfc5d4c`  
		Last Modified: Wed, 21 May 2025 23:11:06 GMT  
		Size: 5.9 KB (5915 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:13f15d6d8593d1df504b8da95a1aaca46c391d06862660a47e11894114dce400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49471785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558cd25d360f11b9815bab11e9c7342e4c1062f10503405d10baf5706ece72ad`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7bdd0d6ce898fe017a461e5f67ccf41a15f147063ffe1c496fb7e5f75037adfb`  
		Last Modified: Wed, 21 May 2025 22:27:49 GMT  
		Size: 49.5 MB (49471562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a41a07b9150530d0fb6f79ae889d05ad0b1f3c6951945dcd0ccc82c8bb3bc8e`  
		Last Modified: Wed, 21 May 2025 23:11:39 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:986cb156089a9876adcb4b5dcbbe3743ab8c4b02da78181df47e63644192b6f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3638876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37e8d46af8a0e529af2b12e4c0599eb45893ab2a65327979541c16d890f36893`

```dockerfile
```

-	Layers:
	-	`sha256:60f7dee3de8879ae7cb51985e918ac04678bf9ae06ee41b07dc1e9f6a312dbfa`  
		Last Modified: Wed, 21 May 2025 23:11:40 GMT  
		Size: 3.6 MB (3633046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70d2516843a874e7e3bda2ac3c69cd42efa798798bf6c25bdd44f9996e3882ed`  
		Last Modified: Wed, 21 May 2025 23:11:39 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:e61218f0cd025546a98e183dd55fdb72c55e6026e313608660016ab8d4d7fbd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48769976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac4fc84635c2f6fa43b4acaf19c13ee2cbd00407c6034c36d9ba23f9661bc4c8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d480a40975e955224ed64be37e82f220f731f0379d20a7b8c36be0e47e31d8df`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 48.8 MB (48769753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0defe67986c874b0301cff3fda4b7e0de64a7964a1818c9f024de7f69f3c8152`  
		Last Modified: Wed, 21 May 2025 23:17:40 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:96684ae6024969d86865a25511fd54d679f6557e0f2003368846109e5f3282c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e473a8ed58709b12333bbbe8405c64df6a3410fe148f81e53b1a4ea955ed4a29`

```dockerfile
```

-	Layers:
	-	`sha256:7318792b06b42d28d659258ed45128e176f0f6870ab870c9206011c8dcea8adf`  
		Last Modified: Wed, 21 May 2025 23:17:40 GMT  
		Size: 5.7 KB (5670 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:fa25c171e569855bfe46f1a3bb540c0c834640d03c441d0809e9898696182210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52331844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de7fec44c05aae87075461494943f6951beae4b162628f48ba67595d12deedef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Wed, 21 May 2025 22:27:49 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f66c5a567d7e145017106fae87531136a75eef64df139a3e4cbc99193948360`  
		Last Modified: Wed, 21 May 2025 23:11:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a13efee9c10b99ac0c306321132a11f18590f6450dbcf092796f5e9d26c1485c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3646063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05fa07e61384c009263b6b73d1c662306dac4ae43564844c6303a4ee3bbd1b66`

```dockerfile
```

-	Layers:
	-	`sha256:e539b8e8c8851057ce5c20e32ff7b8e14c048a55eb68d5e1634e1cb6c226352e`  
		Last Modified: Wed, 21 May 2025 23:11:44 GMT  
		Size: 3.6 MB (3640190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:461ca96c93a1f80d389ebc6e49d489212b6dee12edc6cd96d8fd93102236a16e`  
		Last Modified: Wed, 21 May 2025 23:11:44 GMT  
		Size: 5.9 KB (5873 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:98f07d44741c9f466ac42e3d23213770fe20a32d3032293edd8579455f31a9a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.1 MB (47144067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:753d92563c2d03e7ea937a823f1d8ccc239c095e8db3f18ddd699c6df15cbb74`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 20 May 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Wed, 21 May 2025 22:28:14 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919802c3d1f52b611ae87eff4d538df19bda9ff597f0338ebcc5d27c997999c3`  
		Last Modified: Wed, 21 May 2025 23:11:35 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c7d6eaf3770af0c62fd5265a070a822b5c1f4b5bd97bc29c5d682d9a7702c76d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3641421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a16d9cc7c90725576e38e621837c5104a8423a27d8370ee18a080e75dc4eaa3`

```dockerfile
```

-	Layers:
	-	`sha256:982882c9f7da3e7a94c2b23d96bd7b72e1e039440e735fda4b338e3c8e4bda3a`  
		Last Modified: Wed, 21 May 2025 23:11:35 GMT  
		Size: 3.6 MB (3635574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:386e28241303b2e9c19d88e4ce183fbf6772475dbeda1fc16fced422ab7ffeed`  
		Last Modified: Wed, 21 May 2025 23:11:35 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json
