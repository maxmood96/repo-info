## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:d96cb626af0d9b49c921e5f6a635dc4f1d81bf0783f0d49f9224bab613d6814b
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
$ docker pull debian@sha256:0013df62e817a8e65e7f63f9aa2c2a910275d4c10711968e1f8a041dc813fdc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48491424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b713f09598f350d71eaa4c73ffeacaa7615a87359e4af6fc7823d5510596008`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fd47fde392af6507415e0c446a139c716c628b90115cf260959529821163b09`  
		Last Modified: Thu, 08 May 2025 17:59:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8b93fbe5fb0a70c70b1fefbfef99f03338b1de348f71d5eab83c7916fca46347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a8a1446b0e182cbd458a6340a8f840632a64f860d9e15981ef2abf095f66757`

```dockerfile
```

-	Layers:
	-	`sha256:fd2560e42e81b0b326f3dd8c34c2806f6841583633adfd6cae0911a43ea10f68`  
		Last Modified: Mon, 28 Apr 2025 21:41:49 GMT  
		Size: 3.6 MB (3620572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ce75ef98f34c7ddd5dfec561b6a6abf786c064322444986702f563477cd7fa4`  
		Last Modified: Mon, 28 Apr 2025 21:41:49 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:1ecde97b945d52dcdbe5c8d945e322070c85210184e28732a0ee587fae3cf5bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46027021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2476a9cdbaa2ae0e762ab570a23fd420251f35927785bb5134fbee873bd8d8f0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:41b62f0ff831a6d9573670f580122f67e27137902fa02ca0a3faf11fda42603f`  
		Last Modified: Thu, 08 May 2025 17:16:08 GMT  
		Size: 46.0 MB (46026796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99ce66224ef6dd865a76f8fca66497307701ca6a5957a48cb239807675fb6cc`  
		Last Modified: Mon, 28 Apr 2025 21:41:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:291d0e4573241db92d1c2ab058e9560dccffb546ce1898fe63d14a6cd76fe9c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bbb83fc6df10e688570391d098cae475a27a7e083a8cddf38f1a586c7db2c8b`

```dockerfile
```

-	Layers:
	-	`sha256:98210a4481e7a29122de8e52831eacaabf9e01779d2ace583fe2d65a262e2f01`  
		Last Modified: Mon, 28 Apr 2025 21:41:21 GMT  
		Size: 3.6 MB (3620773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06e8a3b779345cf9fe5ccc685a4eef19123f7e34e9710798977c38637db84fdc`  
		Last Modified: Mon, 28 Apr 2025 21:41:21 GMT  
		Size: 5.9 KB (5899 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:8165b2e261f8a55e9acd0ff0d17ff365a72f723f030e90990cd2e7419e70ef11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44197303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:511847bf3f5cc30ab75252c391d6b538ff0c6d4fdd4fde4a5a35510fa1ad290a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a735d4b4a53e8e11448d15bc50ce4670d54dff52e426cf0510c9b713d3a7ad09`  
		Last Modified: Thu, 08 May 2025 17:04:48 GMT  
		Size: 44.2 MB (44197079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9e7b26ede0282a0478fd27fe08983dc5a22c4e1c9f1dd2914128949f50f4c3`  
		Last Modified: Mon, 28 Apr 2025 21:41:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8b862bab9b1bdfa171b31de6d3a6a1846e2b78750d4610d628993251d5c49052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de26dde8716083ea994f97b456c5f85cce8c197c2f9f5f9649fcc9b67e25ef2`

```dockerfile
```

-	Layers:
	-	`sha256:9307f90747ff5e402a99a8cfd5c83c178a8bab45467510c8326932a1a7c5562b`  
		Last Modified: Mon, 28 Apr 2025 21:41:33 GMT  
		Size: 3.6 MB (3622751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87ad4c78296ec8a4354d755aac7fa063e9dfac31d27571f96c1dbc0a363694db`  
		Last Modified: Mon, 28 Apr 2025 21:41:33 GMT  
		Size: 5.9 KB (5899 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:a78e8ad6970ed5de0112eaed484b24ce7bbab2d087f87b55ebe07919a23635d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48327866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c423ea3a42814ea4216ad30bafc234367913c7b2390741022a4d3e3810a27bdb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd61a3a950538c0f69bcc80253aec98a77ebcb94165039d5ae7b6ce4925aff87`  
		Last Modified: Mon, 28 Apr 2025 21:41:10 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c53e28143b3c101d18a66be435b6084ed955e2ee667a977fa21a2a9d69e6a713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e31498460a024d18446effa0d0d754e3704ac7777579ee89acc5cad8711e4e4`

```dockerfile
```

-	Layers:
	-	`sha256:b64b5953814b6fbfb335ed232bc12a5fe434f228c5c5c90232c964c4e750da80`  
		Last Modified: Mon, 28 Apr 2025 21:41:11 GMT  
		Size: 3.6 MB (3620787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4042e18a022e425f60b8f526c8f6b60d0e1c2da840a5bdee20c4e02390d2852`  
		Last Modified: Mon, 28 Apr 2025 21:41:10 GMT  
		Size: 5.9 KB (5915 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:55610e7f16b9366709f0cb5db8d477b04c18d63a2077011f74fdb185f8ec503b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49478797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e8163cf574e9164fd0dcbd327efebea440531d8b64e9a200813cd703580f8e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d6426ff7fee55f1c5da8050672c1463528bb15df73bf93e3ac0a5200042f6c3f`  
		Last Modified: Thu, 08 May 2025 17:05:10 GMT  
		Size: 49.5 MB (49478572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ceda9ceb9a04502fe4fcdff00e596199a1d0bdb799aef588be4a386ef936e9b`  
		Last Modified: Mon, 28 Apr 2025 21:41:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d5ed769331bbb8ce20446d91bc657367580e31df858c9e4fcdcc8191454b864d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3623563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e77ce089274c8033bf101fbf6f28cd157c268d8689e108866f8eb566db51bc7`

```dockerfile
```

-	Layers:
	-	`sha256:3af441ee2d3ffd64d3c1fa485c05336d3d03a2a00dd9e5ee05175eb95e498dfd`  
		Last Modified: Mon, 28 Apr 2025 21:41:48 GMT  
		Size: 3.6 MB (3617733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:694e664803ce608a7bde643999c0ad4601b2e88facd5a5150ffcbca8398d2a31`  
		Last Modified: Mon, 28 Apr 2025 21:41:48 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:660d7594360c9639724da7a1002ede685668c0d624a978d812403dda978e6a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48775664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb14885c39cd18ddaa56cccbddf9ba84951f2b477f0449f321c6050f5adeab4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:fa5acbf36757d3126014bc0e0a159fb5593a1d68ddba5992ef7ac9aa3e7db8dc`  
		Last Modified: Thu, 08 May 2025 19:59:58 GMT  
		Size: 48.8 MB (48775438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543f77bf0a3897b80b381e96b7e6f50308de9c78ded2e992f8b7688ba017f4cc`  
		Last Modified: Mon, 28 Apr 2025 21:42:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b9641c673e04e04c40b15dbcf9851a759a4c2942cf088545a03328b0ad6abe76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 KB (5671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a721d2f8c1d0afc40595df6feee31cb56b2b792d4f5db058b26e9dd2f4579b39`

```dockerfile
```

-	Layers:
	-	`sha256:359e35cf8141308e5fe6fba29cbc8307c52a9431e7483db730419be29021bdce`  
		Last Modified: Mon, 28 Apr 2025 21:42:34 GMT  
		Size: 5.7 KB (5671 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:e61e69be9a95af804d59c55c27ab0755ba93059c6493b33da11ca9cbf6c19424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52332354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:383b4e58b1548928003b78e00e2289aa017cac5652d48d5421e634dfe539691b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:33862e890d6c23fba01df0303b503e727dad5c72574fdf8af76d76dc3140d561`  
		Last Modified: Thu, 08 May 2025 17:13:17 GMT  
		Size: 52.3 MB (52332129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ad4b65116f2eed87890f49695e6644280e9ce6b6958245f906c92a6dc3c636`  
		Last Modified: Mon, 28 Apr 2025 21:42:59 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1382281b2e59d94480f9049f41138598335b1387dc94758daff9515cb948559c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ef9b0d3b1729335b8f577dc3d3b9fc3d75181885f2550156d88c7a633bff817`

```dockerfile
```

-	Layers:
	-	`sha256:b69332fd6532e5548c88c82841682636843dbd68bfc136a02f8441e13453cc83`  
		Last Modified: Mon, 28 Apr 2025 21:42:59 GMT  
		Size: 3.6 MB (3624832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d936bbc66b8b302522bf59abf0df4429e8cb471fd54c13d30d6bdf554bff96b1`  
		Last Modified: Mon, 28 Apr 2025 21:42:59 GMT  
		Size: 5.9 KB (5873 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:68e6a59e1c79a7d0c18f71fe978f4c52010c8527c1567bb317adabda5eb66731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47151556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0607e2a70bdc9bff0a1f44d2164cdf29987beb086a52bb32fcc0bb1a61999a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a5e7ec27bb28a531688c62bada8c4b448d8e280327ecabb8be798bc43be30c38`  
		Last Modified: Thu, 08 May 2025 17:04:50 GMT  
		Size: 47.2 MB (47151332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce885327ba629fb59685b1d950269760bfdcc965efaef247f577836a48fa2a65`  
		Last Modified: Mon, 28 Apr 2025 21:41:37 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:0621dbdc257f532c51c5a271c4c86ca48eb9e8bea765409b8f35e39b0d8840b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d98d915d98990c869d34b3c933cfd1581ce1c2f1c259518fff7f2959c5a85c3e`

```dockerfile
```

-	Layers:
	-	`sha256:b12c788f861bb36777e717bf91001bbbb08e74833cc10afed59d6b7ff2c0d792`  
		Last Modified: Mon, 28 Apr 2025 21:41:37 GMT  
		Size: 3.6 MB (3620302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:041b8511f80346587ce5f65615e30fe74619d4cd5669ac9ac5700c76907b3802`  
		Last Modified: Mon, 28 Apr 2025 21:41:37 GMT  
		Size: 5.8 KB (5847 bytes)  
		MIME: application/vnd.in-toto+json
