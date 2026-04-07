## `debian:trixie-backports`

```console
$ docker pull debian@sha256:5e0a9a6b37a45e5183c77af0ccd051d78e07dd8d779eec30789c8cfb8acf0b9f
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:trixie-backports` - linux; amd64

```console
$ docker pull debian@sha256:428ab7962bbaa18c767ecb4996be65aec54df49aaf56162be65d77808fb685c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49298056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0099d3e547299d06c83e59cb7a59e5877f634f9635376606052e9ed6816ef33`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:17:04 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272e3aec75206fb33c1f3cf173b0806eb1235781ce30b7ecb74d57a792bfafdd`  
		Last Modified: Tue, 07 Apr 2026 01:17:11 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:71548aeb2292106dd57299e0e127cec92f15e29419f54be2b0650f0475b58812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3176697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22f0da840f349aee2d6e46b304b5713dc40fb9c23d4834156d1d1620b9c99410`

```dockerfile
```

-	Layers:
	-	`sha256:d18492cdfdd7d230f051341cfcdecf1827f1723f9db072036e463936e02770c2`  
		Last Modified: Tue, 07 Apr 2026 01:17:11 GMT  
		Size: 3.2 MB (3170913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9774fcbc73ff070e61033cf122476bef48e9a70d5de95ed7c00163d16a7b4b03`  
		Last Modified: Tue, 07 Apr 2026 01:17:11 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:41eab2d12e9ea8cdacdf2a686e9c0d7967cbf18400754a08c521167088bf9e4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47461116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9463bf32b170c24edbcb2b11b689c05ea91c744144c6b1240f2dd7b99cf4e019`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:33:01 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e2d99f94edc3d8dd6e6b758a4671793ae83d782d6d01f35ad2caf70b714b475b`  
		Last Modified: Tue, 07 Apr 2026 00:11:04 GMT  
		Size: 47.5 MB (47460892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df894928d7c0c3a7bd4a64d7629ca01d2ff6434a8d2cc0650c5ed3ae240db383`  
		Last Modified: Tue, 07 Apr 2026 01:33:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:5564ae0c0ed58de5d916b5e654fd6a9a0de724b98aaacbe3fb3f31247aab8e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08dd6830c177e810a11c4f18bb0f33100e3e02ecf6d11d25f232c512018b513e`

```dockerfile
```

-	Layers:
	-	`sha256:c5ac353d90f2f6ce4548ef025da962a32e32def5402a058f66f9271cec5472b9`  
		Last Modified: Tue, 07 Apr 2026 01:33:08 GMT  
		Size: 3.2 MB (3173850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:193582b803f6bc17cc729ee84c62b44884a8c24b657f875b14496a4977389a49`  
		Last Modified: Tue, 07 Apr 2026 01:33:08 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:dfa2be49c8a8f15f76267b7331f0547e8e367fee84bc001c503b414397dbd02f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45733221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441a350178f43824dac201c4e9c3eb7df3f2a17736b42c647659c5a55373d063`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:16:10 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:5b74af671a0d47dbd638dd4965926230c96ef85f87e920309332aae3ff83292c`  
		Last Modified: Tue, 07 Apr 2026 01:00:01 GMT  
		Size: 45.7 MB (45732997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae612c779dae71a306c06b433854f9828e6d09c8ee83cea11425c27a4b6467e`  
		Last Modified: Tue, 07 Apr 2026 01:16:16 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:3cee0ce5978e902069918a5fd33eedf5c4abc8f0f389c63c464c063413272a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0252e091e98547cc7217fd0059d3e9ce614db8fd7035ecb7ff151f4b6c2143ff`

```dockerfile
```

-	Layers:
	-	`sha256:0b0849a5e58af88040ecdaf4bb3f7be992677acdd0fa040e214ce0a5e32c8aa2`  
		Last Modified: Tue, 07 Apr 2026 01:16:16 GMT  
		Size: 3.2 MB (3172287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:860c548a3d0f9ce7169fe718c585412c7a4d2c9b4ad65ba451e78ac71406b21c`  
		Last Modified: Tue, 07 Apr 2026 01:16:16 GMT  
		Size: 5.8 KB (5840 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:bcd3f6b4c0a9cbf7e8265d5ee453483cf81585807789536e09f7fc0aa38f2790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49665478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46b9622267ffe85e1fe9bd2c4efbc9a4b8e902b8579d92c82743e38fd7d7396e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:15:47 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b62616227d898961f0e9baa1ed8e0fce18784dad348c636287642dfef3a136`  
		Last Modified: Tue, 07 Apr 2026 01:15:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c32a7a111f4572686e970e3cdb7c0b916cb7bfb5806c3b0a0fc05bf9480c8a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38c37d5aee60712ef3253ab30251ffbaae467e20567262877ddb0e42ad2a84d4`

```dockerfile
```

-	Layers:
	-	`sha256:83bd50e576bb63b27d7171bd720f39db01d1b10ecddfd79f9a36f4e2c2a501c8`  
		Last Modified: Tue, 07 Apr 2026 01:15:54 GMT  
		Size: 3.2 MB (3172394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b0308dff0130c36c19610176eca3dcffb2659a6b78da03d5a9f2887292057c6`  
		Last Modified: Tue, 07 Apr 2026 01:15:54 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:aa334e70fecdbdc8f6b69f6361324e6480f354e8b9b9da0df25a7929458cf9a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50819311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a8bd981786835ce4bddb7309613faba2817db34af777f8345187c877199d5e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:16:29 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:cdc6802f3021d1c2b9488d1de8ce2706686229997f4dcbab2461da2a3a1f115f`  
		Last Modified: Tue, 07 Apr 2026 00:11:26 GMT  
		Size: 50.8 MB (50819088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6c5856c72859cb0ab9165938b30882c355e036152449dffe4ab503b028908a`  
		Last Modified: Tue, 07 Apr 2026 01:16:35 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7ff3a81554921ead4e5bebf15a326aab3ae2da3e46fc67feaf1322fa148d6fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3173882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8bf4a634936bd7ad8a3494fa71390e2cc4fac45ca6f3b27ee03b0811ee1c754`

```dockerfile
```

-	Layers:
	-	`sha256:ca7307d95b16f9bac249008c2adaa110592be2b76b529b323cfc6d7096346b40`  
		Last Modified: Tue, 07 Apr 2026 01:16:35 GMT  
		Size: 3.2 MB (3168115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5af4096321283481a4f7cf183c8e6182cc5487519933788a15198acc8efa0579`  
		Last Modified: Tue, 07 Apr 2026 01:16:35 GMT  
		Size: 5.8 KB (5767 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:cc57dabc994b63d96df2d2491db476b2cec8ce2e1eaf400e55e3a6eba31b952e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53118893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8d949702e9606d34e5778262761021df51bfe8852b8cc6ac7b3a0fb4c4191de`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:17:06 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e381eb3f2c560dcec0fb42c3a64a8d68f2f9ac5d7b7b4628db77581829d4c233`  
		Last Modified: Tue, 07 Apr 2026 01:17:24 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:502a905a9078d8f9b4ac8bdc60cafee7cccb8894db96a3b51dedb31abe94cee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3180236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da54b9dada9d6482aa5b08f48b17479216cb208e08af1924100bbfab78f857dc`

```dockerfile
```

-	Layers:
	-	`sha256:5c9dfc71cd25f3587dde64ff53ec6b0c9fb2c70c8b7c659c4c5812574006d0e5`  
		Last Modified: Tue, 07 Apr 2026 01:17:24 GMT  
		Size: 3.2 MB (3174426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:009bb1176ad39fe2abdf7efff2b95844523d7d709d88b383ba68ac639c8de73f`  
		Last Modified: Tue, 07 Apr 2026 01:17:24 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; riscv64

```console
$ docker pull debian@sha256:537e959f54bffa4e18a697f4bd05bc3c4b9c0533c0449969a25d81886c5883a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47792849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9420fe2408faab33d084d01b398858ee5e36db54c4ea4bc749baf80f33b3e3ef`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:32:54 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3e61abfb88ee12dd42b3c32c20825f42c0eae3286fe2a9301e326413688c3d40`  
		Last Modified: Tue, 07 Apr 2026 01:54:08 GMT  
		Size: 47.8 MB (47792626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ab4796b2b5b187910f8971147259f70041e00951a1d00ecdf7c3e8e12f62d9`  
		Last Modified: Tue, 07 Apr 2026 02:33:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4e68fcfe48e766b326b80439740d5dfbd240a827d8fcc5d11bdd877c42cf4ddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3169047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6600701c0b616e571b685ec454751f04dc2643b5755aeedb2e842c331737b657`

```dockerfile
```

-	Layers:
	-	`sha256:1a3332d0ee32c289ae463dbee92978e913386fc115569c40323e04fb9854a8a4`  
		Last Modified: Tue, 07 Apr 2026 02:33:48 GMT  
		Size: 3.2 MB (3163238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81b036edb19dd7150ade2c9e1617ea2d323758d583da108ac42449d29c158557`  
		Last Modified: Tue, 07 Apr 2026 02:33:47 GMT  
		Size: 5.8 KB (5809 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:9ea4d093b42acc9d18047b469b8b63e07df80ea5d98ae66463aaadf276789a8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49365327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36195a51d521c39bd7aa10250095f3ea5478ba85e7a151fea4bcc2580993a308`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:17:04 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:99ccdb9e0b0ce79a36cbcc433fd972b049c1e4e84d217954de0e89224b1fb094`  
		Last Modified: Tue, 07 Apr 2026 00:13:49 GMT  
		Size: 49.4 MB (49365104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d988d07fa606f0d32a779639d1ecfe9cdeea3613b3eb27a58236acfdf582b6`  
		Last Modified: Tue, 07 Apr 2026 01:17:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c3910b032db62bc094e5b782881f4677e5949fbb5486b38e84f9f845227a5d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62064c380a52342bf5f6c3d3f6c515854a0c1d1c94ac7adbd224a062a83cd6a4`

```dockerfile
```

-	Layers:
	-	`sha256:9b00769e34c5f999c931fb6bcf30250c27d7b4189cef93e78c8dfd6f922c602a`  
		Last Modified: Tue, 07 Apr 2026 01:17:23 GMT  
		Size: 3.2 MB (3172360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b96456ee09bb313625ed07fe207af05e49ca0c42933eaab7f44991f82884aa24`  
		Last Modified: Tue, 07 Apr 2026 01:17:23 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json
