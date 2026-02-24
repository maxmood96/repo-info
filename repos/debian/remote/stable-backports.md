## `debian:stable-backports`

```console
$ docker pull debian@sha256:5a5d27fb0c919a6fd5c25be66d9216f1ecdec1f1637d1af5cedd525e7799fc76
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

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:8f738af9c8ae5ab5932da97c96824000600f63dce931311e5b400b1e784ec181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49293349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e86c42dd168814fc870d278cf53be72a0c2b77a3d3db27c42d820f39c1ff6b5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'stable' '@1771804800'
# Tue, 24 Feb 2026 18:51:56 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:55b5edb073789256f86cc8b68165387fa3968337d5aef7aa90ff1e73365a4a08`  
		Last Modified: Tue, 24 Feb 2026 18:43:48 GMT  
		Size: 49.3 MB (49293127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34208df6707a0a915fedf026d8874593cc28512e196c10fef7dabc407bf6374`  
		Last Modified: Tue, 24 Feb 2026 18:52:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c74e5c28a16b32fd91532946e2bcb652f9a1f4ea13844037a4121af697ba4626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3176661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0b8f88c5f97b4ce3c4b9f646b08748d62087a74101b984e5e7b1c4c938780e`

```dockerfile
```

-	Layers:
	-	`sha256:ba5e3b4e49fa2e3ed902e7b56dd6e28ec25a26345ad47981bf277bec3d0b69da`  
		Last Modified: Tue, 24 Feb 2026 18:52:02 GMT  
		Size: 3.2 MB (3170877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7ff591ad4498fad763f28c8fc1cd32295a668be5837df0caf6e6b59cd196e8e`  
		Last Modified: Tue, 24 Feb 2026 18:52:02 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:13b0728de00f41192b2590844c035cb9c48c9d4e5bc2c6fe4643473aef081101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47454385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f433ea4f8239b01fd90f0f6ff3e328fff3fa59e0f6332745ff63f43ee0fb534`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'stable' '@1771804800'
# Tue, 24 Feb 2026 18:52:58 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:eea45aab68bdd71d8ec25b84b03ee447a50e05a855dcc104cdb8ec6caa3259da`  
		Last Modified: Tue, 24 Feb 2026 18:42:01 GMT  
		Size: 47.5 MB (47454161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e147290282f345745a4661fa8ec9bc7b5e07a68ed5454f084b8aed1626ce0541`  
		Last Modified: Tue, 24 Feb 2026 18:53:04 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:339723a43aa20489fda4b5ccab0582c0b82c966b0e127ce870f4a6314fdd3765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3179653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6cf5db44bbee3a70d145d2980091c2692930700ca8363845d3f68042e3f7b5`

```dockerfile
```

-	Layers:
	-	`sha256:383ff6e50f0723bb17405a13d0fa63735e88c2b8f9e1736c167908c1a443bfc3`  
		Last Modified: Tue, 24 Feb 2026 18:53:04 GMT  
		Size: 3.2 MB (3173814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adf50e3f17bc380b2f51160c7881b8d084ad4f96fcc3f55ef4a4ee84a2d0eb32`  
		Last Modified: Tue, 24 Feb 2026 18:53:04 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:30750d1559e745d858c7c6a6c7bfee2247d83ba8b1349d4194400e26a20f0fc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45725310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8500c980b1b1ea4e60936a0e32424e7170aec45ce4eab770871bb9aee343d92d`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'stable' '@1771804800'
# Tue, 24 Feb 2026 18:56:19 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:2c4b73f8c7c4a53e1f4c0d100290b9072b2df05a80fff99fa9f7cb0a703353fa`  
		Last Modified: Tue, 24 Feb 2026 18:42:39 GMT  
		Size: 45.7 MB (45725089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1700f540aa1572d6c2f55fc8df1a29cd8f86742edb6c36cb28f2c1390d11ead`  
		Last Modified: Tue, 24 Feb 2026 18:56:25 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:0d58ea70303c6ea29474b585b4fcc2aaca8410e9c9c60345e31b042c4c94ada8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8e8c3669db9d1bec75f02f61e6f255c1f00de46e6d362681d47399f11bf049`

```dockerfile
```

-	Layers:
	-	`sha256:30ef41be29378f54a5a08b51a6d2bca75a1cd021b9d34232c3267577cdc5c245`  
		Last Modified: Tue, 24 Feb 2026 18:56:26 GMT  
		Size: 3.2 MB (3172251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:834d92e86c364b9f446117b9dbe34b7b2bf39c6d89475ab60f8c5090b0be6eb8`  
		Last Modified: Tue, 24 Feb 2026 18:56:25 GMT  
		Size: 5.8 KB (5839 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:c66f60b498bb8a93766524c10c06775d4d0d190ce3ccf862ec3ddc5e47650057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49652388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f752d5175d573e8e223a6e8ea2aebf88cfcc974142e88538584450013ca633bf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'stable' '@1771804800'
# Tue, 24 Feb 2026 18:56:47 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:690dd49186701d2d36710210df09381e56b05ab75bb42a890d5d53249d197a00`  
		Last Modified: Tue, 24 Feb 2026 18:43:23 GMT  
		Size: 49.7 MB (49652166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a5fa3f9709fd55a9b1e6f8872e6c2f65e91e5732377dc891d396d97ae50731`  
		Last Modified: Tue, 24 Feb 2026 18:56:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d8a7e463be72ac156fe1ed99faffd21c79207cb68fcca31dc08add4bb8a4c44d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fadd33a31ffd92494c2758edac19894e91e5450eb2f163f2cc836752c70c5ffd`

```dockerfile
```

-	Layers:
	-	`sha256:f21a412577089c0bf18a3095bd492cbaeef4760e284510e5b5ab22cc3cdba127`  
		Last Modified: Tue, 24 Feb 2026 18:56:54 GMT  
		Size: 3.2 MB (3172358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48d31856469a83ddb74722a4b7dbbcc967bcf65629357af4e6d352053c92bc34`  
		Last Modified: Tue, 24 Feb 2026 18:56:54 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:bb612fbbf7597e59de26b305f314fa73dd32b303b638c8bda18a4dab22d99a5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50805497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7367d0617b9f818e5f5a1c828e6b0395b34f440718ec49e8d7fd21b817d5ca`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'stable' '@1771804800'
# Tue, 24 Feb 2026 18:53:40 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:49d42225e8df939dc7ccbf8368db234227c89bc5f2921477a3396161a9f47f24`  
		Last Modified: Tue, 24 Feb 2026 18:42:31 GMT  
		Size: 50.8 MB (50805274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a85c5cecc185e7a6196dc5815e23582f9ac4bb92ca0a80b48b7604edc55fc83`  
		Last Modified: Tue, 24 Feb 2026 18:53:46 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a4cfc88da603af7e72587e96db6cf493f0b15f651b11a733ff2949dad1882da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3173846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b48295315a099ca0d0d7ba6a0ed7d28f86dd192a1963d20d771fd39137a7ea3`

```dockerfile
```

-	Layers:
	-	`sha256:34563aff585b194a5f5c66102f239fd11ff5be90f250dcbc2ec489ddca18d570`  
		Last Modified: Tue, 24 Feb 2026 18:53:46 GMT  
		Size: 3.2 MB (3168079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09b58ed7a41ce7d8331421b6b8752529d9937e9254f434dd0c87737e435cfd8e`  
		Last Modified: Tue, 24 Feb 2026 18:53:46 GMT  
		Size: 5.8 KB (5767 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:647d783ad671ddfa87512462ce6d5ddee52df5b2a0f1182f9e9554aca310938b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53112485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd91f0c54a95a5c28194aad8b7a5fb8c579e69e95424cadbdafbfa4301d26ed`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'stable' '@1771804800'
# Tue, 24 Feb 2026 18:54:02 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3bde950ce93c7536badd86576e1b614d13001c4e8b0acc9190a6a7c6bc64894e`  
		Last Modified: Tue, 24 Feb 2026 18:44:08 GMT  
		Size: 53.1 MB (53112262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce64370d038f44de3e4b91eed4111d3885a31e7a3daba2033f3aa42e3d6b68b`  
		Last Modified: Tue, 24 Feb 2026 18:54:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:134ce461f03ce09f39a4d499fb96b86e92202e8f07abc496e8f16ac81fd73aae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3180200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3846a5501ceded704969d8ae0a0ecb43d655a3c5a9004162578bc443dcc27b`

```dockerfile
```

-	Layers:
	-	`sha256:143a9d8772cb736afd9bc3c01f2842968361df89db310879f85494644660f386`  
		Last Modified: Tue, 24 Feb 2026 18:54:21 GMT  
		Size: 3.2 MB (3174390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:666a7af75411f2b9a8d758ffd307a5de3dc929e8b28f2f09729767a918854191`  
		Last Modified: Tue, 24 Feb 2026 18:54:20 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; riscv64

```console
$ docker pull debian@sha256:4457c006ee02351e072acf53ecb6f11822061bdbfa3c6529548cde824247cd83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47777160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52de397c367287e69b3386c95d7af42a64dce5efbf9e55e7855e4ad5074b4b73`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'stable' '@1771804800'
# Tue, 24 Feb 2026 20:46:22 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8103641ffd5f60299ef92032a9ca0b462c596961c754c8414e56e3ce03a6ce85`  
		Last Modified: Tue, 24 Feb 2026 18:50:25 GMT  
		Size: 47.8 MB (47776936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0494b2cc2a3b834b6d852c1b2b98fc4b28c21ee2282b53546ada7c5cabd55b87`  
		Last Modified: Tue, 24 Feb 2026 20:47:17 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:57ab76e675c4add4ef6284f250265f042755e8d69c3f958cd7e730d1ca24bb72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3169012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed07e983746872f35b0c4dfbc4fcb586f2039cf0e8dd9646f472357c342a1a04`

```dockerfile
```

-	Layers:
	-	`sha256:ca19f1be6c0b8e4f8f42647c6827394e9ff5ce11d9216ba4914dbbfc5c52679e`  
		Last Modified: Tue, 24 Feb 2026 20:47:18 GMT  
		Size: 3.2 MB (3163202 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ded3df6738f918a33fd55aa1f781d4f70f39447bbf1ab72ec2619e2d4c48a7c`  
		Last Modified: Tue, 24 Feb 2026 20:47:17 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:e5edd7765cd26a2ce7592f55d94990262a8da7ddd91097a481cf3b00453cfd1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49354758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e935ca312d4111ee977e73b202ba5b429a3c83a731481d31def54f553ac321ba`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'stable' '@1771804800'
# Tue, 24 Feb 2026 18:52:39 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:eafcc3ce5dc390886e8284a2b2366d6027a55d987f0669ef66690a9fa1b120a3`  
		Last Modified: Tue, 24 Feb 2026 18:43:03 GMT  
		Size: 49.4 MB (49354535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c4995df7dee2f45d10c604c5428470302570616911ebc3b3500eab7d72e9aa`  
		Last Modified: Tue, 24 Feb 2026 18:53:00 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:stable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:2024055e11cb48b41a518336b49da42ab0f046afb75dbfe191c3c77a78cdec58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3178108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdca9593b7d1284bb1e47b67a61d797f6669af0143e7afc0976050672e708c7`

```dockerfile
```

-	Layers:
	-	`sha256:afeb97a599bb1519ba07e91173e398ca28a4f46936f7a27cb06fff7e9964ccfd`  
		Last Modified: Tue, 24 Feb 2026 18:53:01 GMT  
		Size: 3.2 MB (3172324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0ad2d3be908041305b3a623e1f1b4f4f92cae79ea36b050d75aa3daddee8e4d`  
		Last Modified: Tue, 24 Feb 2026 18:53:00 GMT  
		Size: 5.8 KB (5784 bytes)  
		MIME: application/vnd.in-toto+json
