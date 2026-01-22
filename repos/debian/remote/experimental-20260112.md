## `debian:experimental-20260112`

```console
$ docker pull debian@sha256:aa405b2966e5fba23067fce587b0e91ce81178de89711c07627f14ba37e7fc94
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

### `debian:experimental-20260112` - linux; amd64

```console
$ docker pull debian@sha256:9f85725d74c7a6f2b2542249201b8cb613ec5d0761997bdd5d14869e0a9a41c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48842180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423e50f81ca4698e9c9b27e9e8c4192247be35aa84bd3718b3ff175a1b6e018f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'unstable' '@1768176000'
# Tue, 13 Jan 2026 01:17:26 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:8e36c1fbb8f949ba76f5152f240c90e27935c79571b76123d0af79c9a578156b`  
		Last Modified: Tue, 13 Jan 2026 00:42:32 GMT  
		Size: 48.8 MB (48841957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd9e53fbca78634a0be35375125fcf8dca0cef46fe0f1b2a99a5284260dc208`  
		Last Modified: Tue, 13 Jan 2026 01:17:32 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20260112` - unknown; unknown

```console
$ docker pull debian@sha256:1f39ff7c2d0baf0a086530f393d26047d521b57f6fae4db8355a1222f25beb4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3149249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca88c6cc4c5ad3cdd034b90bc3255e3cd3aa17110d0effeb0f10d9f0897b7070`

```dockerfile
```

-	Layers:
	-	`sha256:855c29b913b709948f2ac49ecb8ff0c14e4424df2f7322eec6d98a8e137a8c39`  
		Last Modified: Tue, 13 Jan 2026 04:25:02 GMT  
		Size: 3.1 MB (3143148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed09918da676f78412c7e68d59c84905e894e42076143f9fe43419ff710b8483`  
		Last Modified: Tue, 13 Jan 2026 01:17:32 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20260112` - linux; arm variant v7

```console
$ docker pull debian@sha256:d7ce67bca5069c3235ef05bdef238f7f40439654045a3fc589f45b1e94627160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45125182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf7c1e91e01c55ff0cb62216c6e013fa208b18b19293ecfb97fb61319dc1c74`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'unstable' '@1768176000'
# Tue, 13 Jan 2026 01:15:16 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:25f8b8c05c313e5aa19fd75cd8eb0e8d59bbccfd54f23a1dba8c45ff7717b9da`  
		Last Modified: Tue, 13 Jan 2026 00:42:37 GMT  
		Size: 45.1 MB (45124962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d46489b7b9480bab773164ead408e88749c641d2c2f48563e2cc98523d0f68c`  
		Last Modified: Tue, 13 Jan 2026 01:15:23 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20260112` - unknown; unknown

```console
$ docker pull debian@sha256:a8550cbe2021f8c8c0a42bc255bbaa408b354d01accc6fa98a9b8fad8cb1889f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3150687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2cafff2b05732f8f4f0bad8c7666dc6bbf480240608ed64f515013de33592a2`

```dockerfile
```

-	Layers:
	-	`sha256:a3c9e1b362f78612a1d1455fc313987dcafecc0f9e0c8a0874546c1ebadac1bb`  
		Last Modified: Tue, 13 Jan 2026 04:25:07 GMT  
		Size: 3.1 MB (3144524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:868ef0cc8adee3959827bf05644cd38415d278975373f176d5d6367211c0cc41`  
		Last Modified: Tue, 13 Jan 2026 04:25:08 GMT  
		Size: 6.2 KB (6163 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20260112` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:bf57d4ae1e91aaa1e567bb396b53606ad1a1107b847e39d2a31b0503ca674135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48824944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c85fa1ef8ee149aae7f702198d3ad6c682c4f2cb67c47ab1d49bba92acebbf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'unstable' '@1768176000'
# Tue, 13 Jan 2026 01:17:12 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:a36821f44fb17f424807a0a0283bb021936ee48bb00ed8bd7e54ed7400a38cb7`  
		Last Modified: Tue, 13 Jan 2026 00:42:57 GMT  
		Size: 48.8 MB (48824725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023e919e23758c8fdd2a64336c9b5b9028eac766f47858e3a7a203a759b21c39`  
		Last Modified: Tue, 13 Jan 2026 01:17:23 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20260112` - unknown; unknown

```console
$ docker pull debian@sha256:e1f155afec88c0824eb5666f70cc43ef93e0496f01c9e2232e22dc6ea3e1e150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3150182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1a139a9b29feb83ccb56416f3a1d53b4f7999e9e931bbfcf2c9a2d7c9d0c3c`

```dockerfile
```

-	Layers:
	-	`sha256:6b2c1621cce08d319d201eabeff311dcb9dfc3571f237649ddece0d4f22e09e0`  
		Last Modified: Tue, 13 Jan 2026 01:17:19 GMT  
		Size: 3.1 MB (3144001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:699be2f0e5a18a5cd6e8d1071825340829cef0d0252a3be77c23fa13ec87c483`  
		Last Modified: Tue, 13 Jan 2026 01:17:19 GMT  
		Size: 6.2 KB (6181 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20260112` - linux; 386

```console
$ docker pull debian@sha256:7bdbb9411497bfd029317f36cfd4bfc4c466b5b982c79e040ccfec316fc41b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49944042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e1d87ab4ab7700f641ce5ba281ff9adeaf13170772b835d5b95776c35eb4e47`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'unstable' '@1768176000'
# Tue, 13 Jan 2026 01:18:04 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:6cc523c1353e2f7e3d9076701063b4820e209e699c3f43420df2e5422da80a8b`  
		Last Modified: Tue, 13 Jan 2026 00:43:07 GMT  
		Size: 49.9 MB (49943823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70295a80ece57a62edef8c29aeb93d9a58943f87dcd790ca673ef68b26b4b1bd`  
		Last Modified: Tue, 13 Jan 2026 01:18:15 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20260112` - unknown; unknown

```console
$ docker pull debian@sha256:701baf865f26404ef88eb9b0b33c6426d6c8926b8fb7cad6fb90875d9501e7e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3146426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e1865bb59c2f963df1057c82df53b8d9331c08d4c740776fac1ba386c24900d`

```dockerfile
```

-	Layers:
	-	`sha256:eda1cf4db6393a3abf9649eb5e37fb80cbb592fe2057b9560ce3113f3b4c05e7`  
		Last Modified: Tue, 13 Jan 2026 04:25:17 GMT  
		Size: 3.1 MB (3140347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84817cef0c4347ef2b9e0c2439dd286a382f4306d1a8964b6cefe5ccb61b0df4`  
		Last Modified: Tue, 13 Jan 2026 04:25:18 GMT  
		Size: 6.1 KB (6079 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20260112` - linux; ppc64le

```console
$ docker pull debian@sha256:200425bb43c4efefccebfc1aa1f487c1ec61f1b9d0aa6a77ac72846a8debdd5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53525662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104c761579de501633934ef3f4ffa54ef3f6dc08780eda5497cdaa5f447e3242`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'unstable' '@1768176000'
# Tue, 13 Jan 2026 01:16:13 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:75d23fcd6952d9dccf14223316ecdb2a099a0fde7cf0e9f290132381f047bb05`  
		Last Modified: Tue, 13 Jan 2026 00:43:10 GMT  
		Size: 53.5 MB (53525441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351b9094da20bd5aee3638582dcfffe182db4ef8140f66dccabb9dd81c21ced1`  
		Last Modified: Tue, 13 Jan 2026 01:16:30 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20260112` - unknown; unknown

```console
$ docker pull debian@sha256:1638c48442b9f9df3cee1d3ef63b52bcf47deebf48bcf7c872285d55f6d4a93e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3152790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce68c943a3b295dc06cbe8a3b1b7a3e845c85cb4afb77557d118202dde6601e6`

```dockerfile
```

-	Layers:
	-	`sha256:978c9382d9643c4c7b845628dca62ec92af2803d541cbe38793a99f9cd83677c`  
		Last Modified: Tue, 13 Jan 2026 04:25:22 GMT  
		Size: 3.1 MB (3146657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10bb7e0528ef6581e8eb7ae92b10bafc989b7e5c3fe2299e1a60c235de132ac1`  
		Last Modified: Tue, 13 Jan 2026 01:16:28 GMT  
		Size: 6.1 KB (6133 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20260112` - linux; riscv64

```console
$ docker pull debian@sha256:834b6ab231089fb32193ee62e5410df70198c5b5bb9270db63c0ec578d06578e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46856980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f10ff523d275d8eeea43cee931e7bca82158b5f747c951394555619be67087e3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'unstable' '@1768176000'
# Wed, 14 Jan 2026 04:11:17 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:247c00c4e36f0aa85cff57992c0ca22b2bfb8e9809a678d7c62987521aaf3c49`  
		Last Modified: Tue, 13 Jan 2026 01:10:02 GMT  
		Size: 46.9 MB (46856760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1fcce0b2b45e441c3fc65fa5e4d8042fda66161b227f2170ae5d4c5d52a334`  
		Last Modified: Wed, 14 Jan 2026 04:12:21 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20260112` - unknown; unknown

```console
$ docker pull debian@sha256:9be8014c0529734e71d76a1c265bdf90887fd4dce05ed9184ae9068453b9f9c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3140784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:940498cd748275dec0720f9cae93238ef2504278611934b1818606e4160b57e1`

```dockerfile
```

-	Layers:
	-	`sha256:5eea785cd6c7f700e22ebe5b7172997c6d5a0300fc931914fa4af21481935086`  
		Last Modified: Wed, 14 Jan 2026 04:12:12 GMT  
		Size: 3.1 MB (3134652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6c441d4ec7b63f0d40906541f59f5b4211f54e73710ea28b690b1d38854d625`  
		Last Modified: Wed, 14 Jan 2026 04:12:12 GMT  
		Size: 6.1 KB (6132 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:experimental-20260112` - linux; s390x

```console
$ docker pull debian@sha256:a158b1f9fda3789898aced244c74ecf3716b23607898848c223da8a7c8270926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48388857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5689a032801e079c8eab08cae2ca98ad6e94f75fcd4977b0b44aec84eb78363`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'unstable' '@1768176000'
# Tue, 13 Jan 2026 01:15:19 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list # buildkit
```

-	Layers:
	-	`sha256:39395b66c096ad42be248a0276d7b50f9a0f73b66489c5cef6ddd51219942493`  
		Last Modified: Tue, 13 Jan 2026 00:42:21 GMT  
		Size: 48.4 MB (48388638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5b2c722d0e46d4782a7535e84813c438147cd3c40baf20c47471cd5cefaac2`  
		Last Modified: Tue, 13 Jan 2026 01:15:29 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:experimental-20260112` - unknown; unknown

```console
$ docker pull debian@sha256:9902dc060ab033bfe75df644470c36c926cbea93610cb354a380759b0fcb9fcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3150698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374cf88cc0c39d19493036b8148b34f2de6a615ada7cf2a7389d8f14bb945c1f`

```dockerfile
```

-	Layers:
	-	`sha256:3b7d8c7947c2d5ff28ef740e35495208d65088ea5da6a24c82a5be72c10055de`  
		Last Modified: Tue, 13 Jan 2026 04:25:29 GMT  
		Size: 3.1 MB (3144597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68ce0a90c424ff34534269c425d9d4ad1a00b0f8353d368a7d533725d2a2d2c8`  
		Last Modified: Tue, 13 Jan 2026 01:15:30 GMT  
		Size: 6.1 KB (6101 bytes)  
		MIME: application/vnd.in-toto+json
