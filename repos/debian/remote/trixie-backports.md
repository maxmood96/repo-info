## `debian:trixie-backports`

```console
$ docker pull debian@sha256:c50bb58e13478d004620df7e5c0a2951b64e0e412b73fcd08e62dca825fcb96d
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
$ docker pull debian@sha256:b20b72e681f3b13e1ec3163a744ea8500ac2ac0808369028447e6b4eb26ff24e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47448701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:826db6fc540122cbddde77f516835416d5faa2e0ff833a83caf73d26abce937b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1759104000'
# Mon, 29 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:0096434708f67385cef0fbdd93979f2d8849a82842e1217f692977f3e6600333`  
		Last Modified: Mon, 29 Sep 2025 23:34:22 GMT  
		Size: 47.4 MB (47448480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1edfb676e8f0266ffaae61aa410ef07643b746c5535a59ab794957814cb30b06`  
		Last Modified: Mon, 29 Sep 2025 23:52:37 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c69280ada0528e35879a40e7a0d9c5168e5af2373abc73a1a15673a5b8e5b830
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b30830cef800e156fb189ec9bb6f429e21a6a444d02e69533dc3a33872bc84`

```dockerfile
```

-	Layers:
	-	`sha256:9b827e8ad9bd3f2b22419b375d45c8973aa5546f79fa303934fc5c5ba593565d`  
		Last Modified: Tue, 30 Sep 2025 00:31:59 GMT  
		Size: 3.2 MB (3172907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e289e1bf68c579ca1fac1e7f219aa31b5022b46a0fc111926d46bf2a8f35606`  
		Last Modified: Tue, 30 Sep 2025 00:32:00 GMT  
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
$ docker pull debian@sha256:4a00ba346e9808dae90bde530e8e8d35a20532e436a58c13c28e6e3cdbaec31c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53104656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f4ddac24910530253979e1deb0437e203ef6b01b180a6d528a5292b2b29c266`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4cb8224e7ffc22512c71f1cfc1042cb22342df02312e61cb1ab0c492c3369711`  
		Last Modified: Mon, 08 Sep 2025 21:18:07 GMT  
		Size: 53.1 MB (53104433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c66d95f8d42c7a234997f80ccbad8dfbf679b3ed63e0a6be2c1fad00a2a53a2`  
		Last Modified: Mon, 08 Sep 2025 21:59:18 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b9d518ab49e2cf0468476c8bdb1f94dfb6c9fb111303b9bc2d68276ff4d699e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075c2b4e964d9415cdc5db9ccc51a6eeb6d2c650a221b3463a28c59f6cbccb6e`

```dockerfile
```

-	Layers:
	-	`sha256:f533912d0de0b42fbc55ac5365b1c18eb1139ac2c384806d2f63d62a053dbaea`  
		Last Modified: Mon, 08 Sep 2025 21:31:30 GMT  
		Size: 3.2 MB (3173481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:056c9061ea207c5777c0e0425318bbdad8016eedca6cc8619e772995533f530c`  
		Last Modified: Mon, 08 Sep 2025 21:31:31 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; riscv64

```console
$ docker pull debian@sha256:6e2dd89d2f95f9761d824b13dbbea5720a21ff19cd25f4558f7dd16405b8c2f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47765671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73396a1ad814b833022cd0efc11454ef71f6a14214a542d1de9fd0ecb49f37cc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8f913be5ecadf79e3ee9792194aaab366421c7e066487d572f285b293ff78a7a`  
		Last Modified: Tue, 09 Sep 2025 00:25:27 GMT  
		Size: 47.8 MB (47765447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6161aeaefb07f8e55ef05510ab0b089e5956caf7f11a7164c32b9f5beeb9a6`  
		Last Modified: Tue, 09 Sep 2025 15:22:35 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:22c0e54f2783a427dde1d1e4d9ea61852dad788533d864160e44c1a8ccdb40ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3168146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32ea4debbbe2d9b0876bdc0e44a266af0145e560fd3170b8e73f1d6ab475d9f8`

```dockerfile
```

-	Layers:
	-	`sha256:34f1878942f23862af1b52d8f4388283955bc37f2cbc6e3e84dfa3aed460f07b`  
		Last Modified: Tue, 09 Sep 2025 18:24:56 GMT  
		Size: 3.2 MB (3162293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a186b59060f948dae921a213fa0ad422cf6e7719941e4089ee9a10edf4055c6`  
		Last Modified: Tue, 09 Sep 2025 18:24:57 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:2780edb2449e8710d4e204f2dc7e14efb0a248770a3a5e13f3bb51e31adac656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49346549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3e33861d8362606fa752228670f4c8c166e49a92a7aaed04a3a086c8553843e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Mon, 08 Sep 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:28eee642962fd09c10ecf87da2d4b65d208f3d5c1bf3fcca21c105c0213f558a`  
		Last Modified: Mon, 08 Sep 2025 21:32:18 GMT  
		Size: 49.3 MB (49346327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622809380b98b7e4407f3dd4bc1c6e0f78f242a5a1501c89fb7c17ce2e5d9893`  
		Last Modified: Mon, 08 Sep 2025 21:56:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:86e900e650c2ecb259bd2bbf996df62d0b562fb97667aab0fe17b0dc270f23bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a194ceed5e93718ffdf9d7b5e60dd5d2908117484b9a641aaf40eaa72d33b2fb`

```dockerfile
```

-	Layers:
	-	`sha256:821ef3955a1ce71b2129b3083d528725d132a12d72c3aaa718f12abb4a35a4e8`  
		Last Modified: Mon, 08 Sep 2025 21:31:40 GMT  
		Size: 3.2 MB (3171417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84d61a65f5ca39894d128101317cd9fd79bd44d7a0a59904be1896c2be38251c`  
		Last Modified: Mon, 08 Sep 2025 21:31:41 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json
