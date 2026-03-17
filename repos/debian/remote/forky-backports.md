## `debian:forky-backports`

```console
$ docker pull debian@sha256:bda469fc76cf63c47be5026e225aab123c6376903deb00ba9b5b44979f85524e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:forky-backports` - linux; amd64

```console
$ docker pull debian@sha256:5a3a03cf16018f4c98ce4785932df7999e969ca2ffce1e516cbf3fb4a4a4288c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48625315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b454f79a44ae6c35f82516f8be7ea7ca53a60957bae2ee62d57bc754f522f3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:15:48 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e466ee06eaaf7587bf550c70a7fcd7231602b28fa903e3a172b66d9ef28299d4`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 48.6 MB (48625091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a34b73ccd9585219cf18b01e1c92f234c3ea62d3b1995cf6102c93d6f1088c`  
		Last Modified: Mon, 16 Mar 2026 22:15:55 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:cfd20e955679f631c75e9874ab3db4c9c78c9fb03b38b481e8acee1a5f8ca0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26106e6c63c1b8bda6a9d7a66ea603eef74d2a8876ccc3b68c6cd2b7cc9156b6`

```dockerfile
```

-	Layers:
	-	`sha256:4b980ab6a39d3651d1fcac838bd2beeaa3af565c560f768921b04015adcb3d33`  
		Last Modified: Mon, 16 Mar 2026 22:15:55 GMT  
		Size: 3.1 MB (3143332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec5f1ee21fee586723caae273f29c5d2e4f69c2446370f8a68e1a49962e2e54a`  
		Last Modified: Mon, 16 Mar 2026 22:15:55 GMT  
		Size: 5.8 KB (5778 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:2241c61b5e44967f3cd499b1fee841ad539650381d61f411a5c556b41fd717fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45555447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2c8f337adbc982f5e7da3fd8ab5be68212ce8ceca0928fa46b346010e36f89`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:15:42 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e808829cfe5315cd67981f1a90877f9ceed482400b0f64a9a61a5068bf2e2381`  
		Last Modified: Mon, 16 Mar 2026 21:53:22 GMT  
		Size: 45.6 MB (45555225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb135b2043f30e70657cdca4d7f0c0ca61de7cb4bdcc1562fc1118974cc0bd6`  
		Last Modified: Mon, 16 Mar 2026 22:15:51 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:0ea39da608c2b145d5510c707a08c2873e13f86c45fb3dc30add03b943f8651a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3150526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c52a5be68ef01bb6e6b8006ce84a26d45b1e8ad83e1911684bb79daafe4a56`

```dockerfile
```

-	Layers:
	-	`sha256:672e6079b8cc649f4ae3871fb7cd6ab5d46ee2b751671b97f3f88dd5bb6902b2`  
		Last Modified: Mon, 16 Mar 2026 22:15:52 GMT  
		Size: 3.1 MB (3144694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e27771a5e47f0e89116c89dce55cfcd365f0a05671176450de381d4f7006119`  
		Last Modified: Mon, 16 Mar 2026 22:15:51 GMT  
		Size: 5.8 KB (5832 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:7f36ab8cabc06c393963848de5b3ba642ef929975ab2eabede8b621ece986ab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48659283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d986c60f729e7852d6105d3b3f2baf2265e9da15af54ea86cd1934ea88fc030f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:15:45 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d2254738b23b1e05d3619d906c6e8a67a96280536a5a742eb7d517f2cb33ea0f`  
		Last Modified: Mon, 16 Mar 2026 21:52:20 GMT  
		Size: 48.7 MB (48659061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ef64d02fe3e3dc8c21e5fbe2de4dd3aa15cd3d7a9b1411526db0742c875fbe`  
		Last Modified: Mon, 16 Mar 2026 22:15:51 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:9db188ec5b5e604f18860e9cce7887663dff141c9b4c2defae40a58b5a668b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3155944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15c72fb059e3f00e97e8991d7d0419c9e57ff6514f79dfc564f119f84d76b0d1`

```dockerfile
```

-	Layers:
	-	`sha256:60271f1602e170f0d83de8260af312d7d3a18c998597e01962f6f80678eca678`  
		Last Modified: Mon, 16 Mar 2026 22:15:51 GMT  
		Size: 3.2 MB (3150098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0b87cd0d79d35f7acb51188e74890c17ba7b1b35a78f3582360a0eae7efced5`  
		Last Modified: Mon, 16 Mar 2026 22:15:51 GMT  
		Size: 5.8 KB (5846 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; 386

```console
$ docker pull debian@sha256:305b2d7212de395f18cf3edeebf887b67a544fc461450e4a49e73a96cbc321ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49920094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:699b4925642c253db71de7c6487d40a01e6a0a46d68a45357b01d83bd3bd6610`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:15:37 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:7e69024476cee0d949af8f266c3d1bb8032a19b46d27960e72964c7d5d99edae`  
		Last Modified: Mon, 16 Mar 2026 21:52:57 GMT  
		Size: 49.9 MB (49919871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad38168d39e0cefea49f223f42c69a312aa98da8c56fd24a98896a2a0c6a7fda`  
		Last Modified: Mon, 16 Mar 2026 22:15:43 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6bff0e91e68c1f831ea9451bcb3b9de89da9a44587f526d193f850b7446822d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3146296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70802981be50f87881f65e3a30561c4e40e15497b94d45f0bbfa12eddcf9ddeb`

```dockerfile
```

-	Layers:
	-	`sha256:1a65f4e75719e51be806fa40d9ad4e79836af3b00749318818a952fe497576b1`  
		Last Modified: Mon, 16 Mar 2026 22:15:43 GMT  
		Size: 3.1 MB (3140535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34247b716aff169ae140ef1426720e35cfae864b42687a355b88ea34800b653c`  
		Last Modified: Mon, 16 Mar 2026 22:15:43 GMT  
		Size: 5.8 KB (5761 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:a0d77c7f742431b9a1805bd2a03d61f11ce45326409d416d6db85d9a591a0202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53863537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde686871eaba9ce50ff1994787977f6d9f0897b8cc88c46c21eea141728770d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 23:33:35 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:75936ac254db13d0215c75f5fabecfedea28136e3ee0cacb89bd8884668a56af`  
		Last Modified: Mon, 16 Mar 2026 21:51:49 GMT  
		Size: 53.9 MB (53863314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa70303dcdc3d957782164ca01f21f9232558b9a24c3ac918b47ea1dc83bab3`  
		Last Modified: Mon, 16 Mar 2026 23:33:51 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2d06c613df23bff69937f977a321dda8ec370ff8e239a6ccfefe1326419bd188
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3152635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62b05a7c939940bb6d1d6f7bbe01537f3b8f857bedcd436e81a8a9e8ba14c6fe`

```dockerfile
```

-	Layers:
	-	`sha256:b163699623ffa7a2aabef8e197d7bf89f9953526d0ac0ad91c0f7f73ee399254`  
		Last Modified: Mon, 16 Mar 2026 23:33:51 GMT  
		Size: 3.1 MB (3146831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6fa1599c53b64ae9bc33b670a04fb6f66686304f2b3817b44e0028ec0df4939`  
		Last Modified: Mon, 16 Mar 2026 23:33:51 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; riscv64

```console
$ docker pull debian@sha256:75cbbf20aa02f4d6d432345cc21060c6d07b83f44b68e14c8b6f5491e017a4f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46721691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8afc79db9eec0cf2b4b8de9fab5f0ac91156beefba489d45782a73f11c635014`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:19:13 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c3fb5c15cbddc0ebbd7afd8ce992f6bfd6f0d5d4b1d5f4e672c5fc7451f1119d`  
		Last Modified: Mon, 16 Mar 2026 21:55:37 GMT  
		Size: 46.7 MB (46721467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b04b40a88a5449806c9f98fb7d9d726877cf2c4e0546e143fa0dce0725a92d`  
		Last Modified: Mon, 16 Mar 2026 22:20:05 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ec941d064bd89477d283adbad4c1521512a8914e17db5efbd608be7a810b5c09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3140637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de0eac5ff95c6f9f61b911908e00244d06fe13170e0cba12fce35b651d8e9ddc`

```dockerfile
```

-	Layers:
	-	`sha256:1821754f9a97227a02fe5e6602e7f3c5c569577249b04233ec84cd6d8023b8af`  
		Last Modified: Mon, 16 Mar 2026 22:20:06 GMT  
		Size: 3.1 MB (3134834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a94f91fadb62dcf248b56cf1f42c513810e610de63de4418c784d7d13a14ba6b`  
		Last Modified: Mon, 16 Mar 2026 22:20:05 GMT  
		Size: 5.8 KB (5803 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:forky-backports` - linux; s390x

```console
$ docker pull debian@sha256:b2df4eb923ca9fb401c0f711c7b875e8317e17a02f1cd10655aeb51095708295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48334845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a120dd198ff016085251f7b2f031b8090ba1497f111da9111d0b90cf7df6885`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1773619200'
# Mon, 16 Mar 2026 22:14:54 GMT
RUN echo 'deb http://deb.debian.org/debian forky-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f87b2d0069bddaedc5a87fced2f3e4651a654b1dbe947403a098a2d5a2045522`  
		Last Modified: Mon, 16 Mar 2026 21:51:42 GMT  
		Size: 48.3 MB (48334622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ddfe7391297e6901dd266547075fc88530b225c6ba941eb1f3956281572fd5`  
		Last Modified: Mon, 16 Mar 2026 22:15:06 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:forky-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6ff11ee32bfd94cb8e262e15e3ba088d3f4952c79f0a740cbc202a9dd22fd3d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3150561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afb16bb884001b0defa332418ca83817364c581a1402fc4e5ead620e6701b7f2`

```dockerfile
```

-	Layers:
	-	`sha256:d107b9080d98ee3cb3be0a59b43f88acad757aabde4ea4571f4b70797e817b66`  
		Last Modified: Mon, 16 Mar 2026 22:15:06 GMT  
		Size: 3.1 MB (3144783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8da9025bdd479fa84f445dc4facab7539f82fc40c76a701d43bd4bb4e312227b`  
		Last Modified: Mon, 16 Mar 2026 22:15:06 GMT  
		Size: 5.8 KB (5778 bytes)  
		MIME: application/vnd.in-toto+json
