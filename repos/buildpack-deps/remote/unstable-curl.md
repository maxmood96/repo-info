## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:a40dcccd83c82a06ebd430edd393e356b2124d74c0366106593fe889f70f0ad2
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

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7648d854cefa0a06121b94592ddf1ecdbd233af3b0afa94de4a77431c089d1fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76723157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faedd7c6ceadb7f60d3737fc6a3ba4f72178558e08b6dd625cfe75e8d1aaf6ba`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:42:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bdd122fd70d19475cad994fa0bd624dc1524d2143c57c7c1f3f9e23fe40ddb0a`  
		Last Modified: Wed, 10 Jun 2026 23:40:10 GMT  
		Size: 48.8 MB (48801212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250af42f2a097a32d106444385fc18ff806e3b5890910b0e364be8e50256f63d`  
		Last Modified: Thu, 11 Jun 2026 00:42:46 GMT  
		Size: 27.9 MB (27921945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6478f234a11e69c36298b52d66440e937aee15fe333feb54bd53fddf9dabd36d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4054117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5663f39d66f2bb196befad0f4da632b09ea2ab43b3ff944fed6ee65923838fa`

```dockerfile
```

-	Layers:
	-	`sha256:f7ea0b72556750a3bbb9ad1dfc5ebe3420d1950e15ab71c616a1bb872f2fa62e`  
		Last Modified: Thu, 11 Jun 2026 00:42:45 GMT  
		Size: 4.0 MB (4047356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57f980a6de489dd9ded326d7e7a4ffd0b2ae3365e6583e545de20249a49e9713`  
		Last Modified: Thu, 11 Jun 2026 00:42:45 GMT  
		Size: 6.8 KB (6761 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c4b14228be344f51ddd7391cdeb11eff878abf609eaec8517d2fd7d51f37ffdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71016085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0174e2bc4053d5e73c8544581ea07733be49aa2352cc93a378d561bd008dce69`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 01:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6dddbc4e0b590efd809489171b20c0c05ae23facbf49b0dac491dc8f542364ec`  
		Last Modified: Wed, 10 Jun 2026 23:42:26 GMT  
		Size: 45.7 MB (45703240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86724da0b6362c0867d62fcf26f2b64559186172953570f5baa9b4fad9928363`  
		Last Modified: Thu, 11 Jun 2026 01:26:19 GMT  
		Size: 25.3 MB (25312845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f36a530a4cc208ef803fe4cbcc2ee341b9b21fefa0188a6e4a7c7b9ac672c433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4055668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:836ebe1ec116d731ec2087643917a754443f5b4480989ffec61e845cd924fb6a`

```dockerfile
```

-	Layers:
	-	`sha256:49cd5abd5173f3421f1d3c0dad4755f2a2ba4b4a6ade260d54dfead97be4d9c6`  
		Last Modified: Thu, 11 Jun 2026 01:26:19 GMT  
		Size: 4.0 MB (4048843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37a12250227b8a8c118b88047764f968a2b7dfe816ae4d7128856590d0fa1f2e`  
		Last Modified: Thu, 11 Jun 2026 01:26:19 GMT  
		Size: 6.8 KB (6825 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f1c5684056780adf5938b84f6556d281f128686a9c6695a2b66981d97ccfd513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75942854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56acaf5d6f220fb2073b0159034f511208da04076b557b5f4f2fc49705ec39ea`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:44:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:015f4a5f6bd3bcaa5c5acf626b97030c3007c4b91e864c4cfabf1be5d52e7648`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 48.8 MB (48818557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bde100970346a8633eb293a95aaa718b901d789108bd4e63e4f66d9d3771ea`  
		Last Modified: Thu, 11 Jun 2026 00:44:23 GMT  
		Size: 27.1 MB (27124297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1cfe9d1ab18162089195db3a5ea4d33516cd02dccf20f5b9d4f3d07924b863ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4059556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:857334696a409c2ced6b95c74c88c2a9925eefd67a80b6f49f11dc35be52a897`

```dockerfile
```

-	Layers:
	-	`sha256:8028b1960efd439548990b1b7caae7dd88b7b61e5564fe3c0470091ea8f86876`  
		Last Modified: Thu, 11 Jun 2026 00:44:23 GMT  
		Size: 4.1 MB (4052715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b33d67b68faa91981241aec3565e668468013ef834f0f37ed7056a72369561d4`  
		Last Modified: Thu, 11 Jun 2026 00:44:23 GMT  
		Size: 6.8 KB (6841 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b359e1699ea65ed9bd940a9faa9e6f04e8c51442ab58edf37029a26827eaccba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79151644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3434f745ce4fb142c0674b07031813fe5c9aee5aa0b92093a3ca792fd9f47642`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 00:45:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a32252638de41825057387ef73b5d4de843fa9726fc243c76636da258263cc3f`  
		Last Modified: Wed, 10 Jun 2026 23:40:40 GMT  
		Size: 50.1 MB (50105399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6776bc9208fe6e23886fcebb117107385c0d62bb58b598a5be9aff86230bd6cf`  
		Last Modified: Thu, 11 Jun 2026 00:45:19 GMT  
		Size: 29.0 MB (29046245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1333a77d53b39edc9d0490165ad29153c611f1edb7c1e9bb18c70936eb5ee8ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea2635a454feee877540de8a7dcc82970e5af8198bfa2487c97919553bc3f1a9`

```dockerfile
```

-	Layers:
	-	`sha256:c5c77bc604523322f5e0394dc0c99cd6f7bab01cd22d3d29b10c154bc235392a`  
		Last Modified: Thu, 11 Jun 2026 00:45:18 GMT  
		Size: 4.0 MB (4044468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18de201c85c334db2da1b2f6316e93350c85e8e75aa7e77bcec716bc9102246f`  
		Last Modified: Thu, 11 Jun 2026 00:45:18 GMT  
		Size: 6.7 KB (6738 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ba81e0fec9f8274e0fe1e0cba3ac312b01310315746d5947a8cf1462bc70f65a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.2 MB (84249978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fac1ed55db14415426af6794337e3971830bbbd4aec2a87573aaa23ef98fb605`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 04:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1e0ce2460747d14df6cfd1da4b61c0c9b7caf034c9fddf19fabbcba65c2416ba`  
		Last Modified: Thu, 11 Jun 2026 00:23:09 GMT  
		Size: 54.1 MB (54132513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86f91ba1bf8c0d9e7dee82b12886a4f7ee70c339c3778c5cf99a230830c8d7b`  
		Last Modified: Thu, 11 Jun 2026 04:44:58 GMT  
		Size: 30.1 MB (30117465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8328cb04c7af92ad6fc1c5e67f25e03bec16f0cecdbff83cda3a23e9c6ada13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4057989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586969906a3affdb95524a749d845fbb8309cf7a158e1721b0644e94cf227b22`

```dockerfile
```

-	Layers:
	-	`sha256:50e793a8962f723b44811852d26b68bc208ff20c07961880c5ac787fd04e7075`  
		Last Modified: Thu, 11 Jun 2026 04:44:57 GMT  
		Size: 4.1 MB (4051196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80f22b18f19847b3549334fd9121f96c9585b972a5a5b9ef8b400d1ce650d16b`  
		Last Modified: Thu, 11 Jun 2026 04:44:57 GMT  
		Size: 6.8 KB (6793 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:309c0ee196768b7ad74b92a404ec9457ad533c16fe3b8544056be39d92e55800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74150092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae7524dbe175e949a5a9241441d0f7fda17c56c9fee50687b2b271fe9def1d9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1781049600'
# Sat, 13 Jun 2026 04:41:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e2efc7e0091930e45ea6218e0e9380e67d07fe2085c100b1d3d74190636f5938`  
		Last Modified: Thu, 11 Jun 2026 02:48:51 GMT  
		Size: 46.9 MB (46911636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b18596f8f629861877fe419ef9028caff67b10f2dba8a160480c551f8733fcc`  
		Last Modified: Sat, 13 Jun 2026 04:43:12 GMT  
		Size: 27.2 MB (27238456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c4b566387d40ddb2d6093cebbbcbe96075936b850d1852d03c63542eac3d4066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4045836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f45f138f1bce7a749fb0466803d6a178f4afb4084281f94f91a171e848ee7b4`

```dockerfile
```

-	Layers:
	-	`sha256:b2973dcf1701c2481ed36c8689014fa3a2125e2bf7da4bf3ae54f89191610f56`  
		Last Modified: Sat, 13 Jun 2026 04:43:08 GMT  
		Size: 4.0 MB (4039043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e241618679241926e6e5ca613f2152f522658553d8f03dd9b211b7100c14d47`  
		Last Modified: Sat, 13 Jun 2026 04:43:07 GMT  
		Size: 6.8 KB (6793 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6c74e8d473020f2aa0c4f1bc6d8d2c3a885d9e228fcc48e81c2516d7f0169851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76058311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e88bde7705c4edecc51853b8cfed539f609d21bdde936a79e289cc2043ca516`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1781049600'
# Thu, 11 Jun 2026 01:44:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fb23912042361f66d2c3fed63550770682f92117280cb0cf2a2611ef14ea13e4`  
		Last Modified: Wed, 10 Jun 2026 23:41:42 GMT  
		Size: 48.5 MB (48541819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdb3735386433a0b206e3395692138596ad8486bc9cf1339bdb4dc651cae241`  
		Last Modified: Thu, 11 Jun 2026 01:44:48 GMT  
		Size: 27.5 MB (27516492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7fa6ef257b6d81efac2c328b0aacbc5ff0a7c0679655f196aaf70faf6ae9725c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4055529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6967fb828fa5137d518ee6ed9bd2a9b014b015a559cb9cd3d8a110b0315ffcb7`

```dockerfile
```

-	Layers:
	-	`sha256:d7a247cf4159ca91a69df9f7bbdb0954d4da34df2c8704cdaad5451192fc5a99`  
		Last Modified: Thu, 11 Jun 2026 01:44:48 GMT  
		Size: 4.0 MB (4048768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e05643fd98b3843eb5c83e55df5e55cc89e73f5fe561c42948ee27662b7f9fd`  
		Last Modified: Thu, 11 Jun 2026 01:44:48 GMT  
		Size: 6.8 KB (6761 bytes)  
		MIME: application/vnd.in-toto+json
