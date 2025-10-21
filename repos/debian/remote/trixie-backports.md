## `debian:trixie-backports`

```console
$ docker pull debian@sha256:787108704e6f31ffdd780fecb7872f296c2baa4d4feab524cfbff2190c8c36a3
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
$ docker pull debian@sha256:4993ab80f563a183811f761c3157830871fce51241765c23e0d3c007d2778925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49284849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c23b2e953cc5a239759d596b654804fce77b354b81afab839935bfce761caa16`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8df953ebdf8853121f13a7280dec9c17bdcc60a630eb6e817e6a46a114801a`  
		Last Modified: Mon, 29 Sep 2025 23:48:05 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:67fa301cfc58da052735638fd675a036f345a7b6935188f3622b98b65ecae2e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c16c231a2bb335c52c33c3e12b309b862dd905bb444fca0bf17df689e3212c`

```dockerfile
```

-	Layers:
	-	`sha256:d158d982e36056bec596693c942d51581ff544a533f08bd55c10d41e52f78ae8`  
		Last Modified: Tue, 30 Sep 2025 00:31:54 GMT  
		Size: 3.2 MB (3169970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fb28dad81b929c6eeb6d4d6871e1e58bbb93fe5cbd33fc64111241724eaf280`  
		Last Modified: Tue, 30 Sep 2025 00:31:55 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:178230729bd5a0661e9387611565e7807c8463beb4965741367fb00bd7900b36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47448993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f965068a98e6760c9bca5f604ed144c7bcb1a8828a9fce4c80ad9802cd71d42`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:36e1dd9ce5730c29e323bfee77881b6b709a9ef3833ed3a509dabd626e23ef19`  
		Last Modified: Tue, 21 Oct 2025 00:20:35 GMT  
		Size: 47.4 MB (47448771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be1d42c9ba99d4e2bf224399b9871e5ccdfdbe5a8da90469ab3a242b2e31abe`  
		Last Modified: Tue, 21 Oct 2025 02:05:34 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:993e84693b5597510b707de9fcfa4168162d5b8a4bb349072cc431e1374e2f80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3b815ba092f3ea9657f473ff66dd2d7bf2afedfaec5e1b844c1d97aaffd9c7`

```dockerfile
```

-	Layers:
	-	`sha256:ca5b91a7d3b031368da7e15a307a0005486e2e9ceea0b764c74cc005c4f24733`  
		Last Modified: Tue, 21 Oct 2025 06:25:12 GMT  
		Size: 3.2 MB (3172961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2cb16feecf88f4cc85230af7f6e3bdc5fdd674aeb3046e008587877fd99a650`  
		Last Modified: Tue, 21 Oct 2025 06:25:13 GMT  
		Size: 5.9 KB (5883 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:87738b82d7823e6dad8d139976747090fa8024c1b856bd9cf02fdeddfeef2f6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45716362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e94557b35ed0ae126eca1ff54304677fde754006fee3fad17eed766106170f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2bfc3e00e130950b6362e6dfd7b2fb6422153e64a38bdcb425f69c089f79f4b2`  
		Last Modified: Mon, 29 Sep 2025 23:35:25 GMT  
		Size: 45.7 MB (45716141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6246b6e7c2763c08ad7946c950c4fdcb60d317783f878783d5d85a3a8e58a60`  
		Last Modified: Mon, 29 Sep 2025 23:53:29 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6a346d323f035f3084d492198c6ecc2c158bb70b876b6d644490ccd2a1898953
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f911a44e6ab82c6c185aac8e12ad8243d6acc0a70fdfed374f6af1ff33fc950a`

```dockerfile
```

-	Layers:
	-	`sha256:2659fc668a1dd253e57795033afe2d1f78fd2ccf7926220b2abd748419b90648`  
		Last Modified: Tue, 30 Sep 2025 00:32:04 GMT  
		Size: 3.2 MB (3171344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71676145055d57c18f45b537acf4bc218928d0ca94d30032b2be8e957c996110`  
		Last Modified: Tue, 30 Sep 2025 00:32:05 GMT  
		Size: 5.9 KB (5883 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:2288b18d33fe050793f9c19a92fff411c26b53c99f69d813c61b90aa67744d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49648917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9c0d6310794caa77d7447635da42301af04de4a223789ef10b6dae09e2dd7e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:28aec8b14b3eeacbf47ef38af72fab694b109fdcdf31581722750599baf1a932`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.6 MB (49648695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d069da7215dcb47be91541b7e759b92a60ffbcf5e0cc4b5e6876e221c8942aa5`  
		Last Modified: Mon, 29 Sep 2025 23:48:19 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ceaaa8c6c7e8203c8d5cfb6c6fcce15b1792697b88988aa1a00338e7d5e932c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe55804cb44b23daa3eb7871a50910321838951064966f456c6b52ef5f6f1e0`

```dockerfile
```

-	Layers:
	-	`sha256:cb9622d927066b96b66eee03621bc3df1740071220495b1be9a2bb5e46bd282c`  
		Last Modified: Tue, 30 Sep 2025 00:32:09 GMT  
		Size: 3.2 MB (3171451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13ad098599ecb3dbe710f5dc520da5628901ad52648b1725a29923a8f2d6b28c`  
		Last Modified: Tue, 30 Sep 2025 00:32:10 GMT  
		Size: 5.9 KB (5895 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:d04a7f33ebea6c0d974dfb38d6564e7502f815b84619700f54e61103ff06c67d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50800451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3333fa8a702400e8ac9c7566e06084c85d7203062cef5f3ea66f354cfb2d2c7c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f1c1f592b5569b5e2093c3107a48f2929b609f05af6d24c06d41a7ec1ae5e0e1`  
		Last Modified: Mon, 29 Sep 2025 23:35:36 GMT  
		Size: 50.8 MB (50800229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d069da7215dcb47be91541b7e759b92a60ffbcf5e0cc4b5e6876e221c8942aa5`  
		Last Modified: Mon, 29 Sep 2025 23:48:19 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:3c5d2712d301f1df580c284bf47b94c143bb16f7c5cd3b4112590f8080c1c0ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3172983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17cc7eb7e029464e8123e39bf5e01b56b3360af854f561071fa626a6955c42f5`

```dockerfile
```

-	Layers:
	-	`sha256:392c14c6226a8d9d0e0ff150d1e27677f7b93aeb279065f64d063b22dacd5953`  
		Last Modified: Tue, 30 Sep 2025 00:32:14 GMT  
		Size: 3.2 MB (3167173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ce4f3146d558bc1e75b96046dda3dd37fef99c205167698b23108711f0873b3`  
		Last Modified: Tue, 30 Sep 2025 00:32:15 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:f0749b9f09767fe9962e65248a300b291e18a85bece06816328bb92a1854946c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53109698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb77df218c9a280a27d0ddd89bdec90039b51e262a19bb26f413f430b8ff9b7c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:047d1b265d8a7d20ef8b3ccb9f133c3c5f1e4f9c92089889756590b7f20452b5`  
		Last Modified: Tue, 21 Oct 2025 00:26:24 GMT  
		Size: 53.1 MB (53109476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a97a59d13c31064f55f9380726bb3a16a87007ea2fe0993370dad2f3ae0ab9`  
		Last Modified: Tue, 21 Oct 2025 01:21:16 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:7e5be3ed000229503f8846d66ba09187f973db619b9baa216a213b2ad7683455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f384a4979e92f5cca2f7818f6ee5fd33a2fea710089bd5d02863000f424b0e7f`

```dockerfile
```

-	Layers:
	-	`sha256:59b4902670d95a480ce3ac63437c00e3d61fb10afabfaaf264a0cb0c16f87978`  
		Last Modified: Tue, 21 Oct 2025 03:30:58 GMT  
		Size: 3.2 MB (3173535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:060e198a91ec29ca1dd5d57eeb13dd2b4aee7b0b7ff4c27172223f34598faf63`  
		Last Modified: Tue, 21 Oct 2025 03:30:59 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; riscv64

```console
$ docker pull debian@sha256:2b2e7ac79b321ec799a59de333db3e76e6d7ba14b50e2629159731e8b98f8a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47770529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32caeaa65eb10971bc53f69def6d8ecdfdf19c42cb093dabb8cc9a91a06c70f0`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:f99bc11a75f6f7a676f3f49bda98f8ef1b59f2c8ba74759e5fa155fda025bf88`  
		Last Modified: Tue, 21 Oct 2025 00:35:52 GMT  
		Size: 47.8 MB (47770306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3622645b89c381e5e3f4534ab6b1da9e6315cd9f125dbec5a92d5ae36efdf797`  
		Last Modified: Tue, 21 Oct 2025 01:22:52 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:fc0947d354bf61a68bd11f11e9472cbab31ee6250f5ac3b4cfbd47183ab788f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3168199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff5f40fa9992b085fb2cb15afbcfa09809b7adeb2bba46f1c4a5b96cd599d9b`

```dockerfile
```

-	Layers:
	-	`sha256:695fe4e75552e7a37d9e9047f567475dac811a4815408f5f22c2402c0097a01f`  
		Last Modified: Tue, 21 Oct 2025 03:31:03 GMT  
		Size: 3.2 MB (3162347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6063e95803761db13b93fa64b05823fe69b36f9c93d7ab29a91a5f1c17a4db8f`  
		Last Modified: Tue, 21 Oct 2025 03:31:03 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:8f12f2bf4552c81969b7b9683b34d4cd08cded335ec473b8eb3e338fcef5bcdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49351921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5e6f09e6aa520c0657d3abff62092c3c11b979622f97c096425f9319f5b0557`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 20 Oct 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Mon, 20 Oct 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:be7c8533c3f8dfcf5ab5c0fd76b47a568dc971c853834a20808defd1e88a5ffe`  
		Last Modified: Tue, 21 Oct 2025 00:27:58 GMT  
		Size: 49.4 MB (49351699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a7d49607018ddffbdba473375a205197327a8f9b34ee9200e14e47e212f41f`  
		Last Modified: Tue, 21 Oct 2025 01:21:29 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:5a0d3ba22aae96ca737a8db90879881c158cb151a896d03a0a1f2dc897704f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bdcd099a9f63bcc44066d543d920574bb0609696649e8b7a17beb4b2cede444`

```dockerfile
```

-	Layers:
	-	`sha256:733aba472fa9c21d2695cf417119f4cc057f53a9066074d7e6dda41989f47105`  
		Last Modified: Tue, 21 Oct 2025 06:25:33 GMT  
		Size: 3.2 MB (3171471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7c7b54a453761cc54b032b4af920e02ff6ae1113831c7049efda6425e3e8d31`  
		Last Modified: Tue, 21 Oct 2025 06:25:34 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json
