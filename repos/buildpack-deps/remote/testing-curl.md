## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:63dd57b6666d934a947d98f96fa01e4e89c2eb53aa2a34c8cf6d28b2a6be3678
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:09347ab21dbe40771d99a15cab37312df2d79b84b20f00024dd9d2aa86c134c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72712575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff8729e7826c86f479423ac5f4b4021c14f66333d084863578bd0fb752e50b1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e4743b5a77e386ff2c8b73b5f4786349b4c3b4a5bba77f60a49c3b94a3b29584`  
		Last Modified: Tue, 03 Dec 2024 01:27:30 GMT  
		Size: 52.1 MB (52113554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4547041a33b6c57d94bf3840b901ad1987b2672b67b1e68ff564d9703716a01`  
		Last Modified: Tue, 03 Dec 2024 02:29:17 GMT  
		Size: 20.6 MB (20599021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:92cb7df0e0568b7fc8be80e75c42503f0f546decb5c3004df7a857015f9c975a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4057349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a0c85f012d61a9fc7143b1a644830e03f38003f09652809b711fab14b97fd6`

```dockerfile
```

-	Layers:
	-	`sha256:5569ed63877a3b72ccc15acbc764971d91622137a10c5bbd4fc02fc9be1de3e7`  
		Last Modified: Tue, 03 Dec 2024 02:29:16 GMT  
		Size: 4.1 MB (4050528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:627d4a6c9c39fbb055fdb6079287f7c327c52f47c42cb61d4a295b5c69546de9`  
		Last Modified: Tue, 03 Dec 2024 02:29:16 GMT  
		Size: 6.8 KB (6821 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d8ea82934f2fc0340bc3dd165bd2631df066fb4b99ee2604429d93d1063b2fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68276182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18abdcf7f029537135a3bf80ff6fca091e446b667218bc2bb526050acab29df1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5bc3ae687a9226ba4c006ebae837bdf4fc9ce21a92c2280c2fe34aaa801bc170`  
		Last Modified: Tue, 03 Dec 2024 01:29:30 GMT  
		Size: 48.7 MB (48667592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f104f4b59037c21344a76456c37d0109c126d6df42220396b04d3aaad3cdf4`  
		Last Modified: Tue, 03 Dec 2024 05:25:08 GMT  
		Size: 19.6 MB (19608590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1eb34888c6bcf558d750c7870dda70fdf0f677466a2bbbcc3f6c637b22487b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4058816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9c7af33842f88d04619f7cc12b57fd5b403c23cd2614ee934cdf3ae837c5d2`

```dockerfile
```

-	Layers:
	-	`sha256:2cf1cf74dc8eeed6c1bb5790c8f26feba27f7b6d1c40fe71aac84b9b41a01e49`  
		Last Modified: Tue, 03 Dec 2024 05:25:07 GMT  
		Size: 4.1 MB (4051935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7fe5c7ac56fdbff4e2873392d02ec8b314fa10e354a7ba07fc4635a599cf911`  
		Last Modified: Tue, 03 Dec 2024 05:25:07 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3244cb4ae15e09963fb818758a3171b84d208a914cecf7b8948bab3070d8268f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.6 MB (66626866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c40d70011a851a088c8939609eb972337202cf9ca4e44713222d2060b3b8f0f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:da23906b82d0da338b0e507d1bef5cf2747e130d745e77708e8f5279af9a4764`  
		Last Modified: Tue, 12 Nov 2024 01:02:46 GMT  
		Size: 47.7 MB (47681766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9b00d9d0a43af35aa09caad4b98ca01f5b7a33e4efde2bc19aa6be0499f216`  
		Last Modified: Tue, 12 Nov 2024 16:02:34 GMT  
		Size: 18.9 MB (18945100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:939536ff2e2f735538e7914b008724ca3b0776bbd3785d5342bf15bd5ba7f06a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4062456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab45a4af1054cc4670e39ae2a067e67945abecaf95ad1fb893d51e1e6600893a`

```dockerfile
```

-	Layers:
	-	`sha256:a928037a0af31f797489ef0af5dcac5f8acfe6e04948025ea1d72dd175d5bacd`  
		Last Modified: Tue, 12 Nov 2024 16:02:33 GMT  
		Size: 4.1 MB (4055575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed54083f197d3df360b288c743be5a16f3d315e19c0cbc3a73ca735da45a5e4c`  
		Last Modified: Tue, 12 Nov 2024 16:02:33 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:62ca8e183f695e07fd77d42de9eb952a9ce0f2bd81914352258fd5df3fabc163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72592723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dd542b1b36710b3cbdcdd7517cffaa02e85e218a11eefe72c00236aaf47c454`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9eb21918436f171705acc6e3469286cf27466cc89ea0d17c1699761c888e169c`  
		Last Modified: Tue, 03 Dec 2024 01:32:46 GMT  
		Size: 52.3 MB (52340851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937167b9612f87af0bddfb5d6d68eeee5ceeb8c8e8837f1f9918d7f613aa06c4`  
		Last Modified: Tue, 03 Dec 2024 05:40:08 GMT  
		Size: 20.3 MB (20251872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a94476264c1e7242d723c3365da1c45377d31fd1a12b6a62e469be2e43827db3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4060870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a37982247246a3d113bc6f1432d81fa74d3f8414b545b61a9fd23ecc2dba41`

```dockerfile
```

-	Layers:
	-	`sha256:eace2bf523f290287e5780c39e5c7eec9eff8cad96e1b70253ed0df332f690ea`  
		Last Modified: Tue, 03 Dec 2024 05:40:07 GMT  
		Size: 4.1 MB (4053969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4099db3e98b8a583ea5f7762fa8bd19aef21d9cef7e7a12da3fc6ad75000894`  
		Last Modified: Tue, 03 Dec 2024 05:40:07 GMT  
		Size: 6.9 KB (6901 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a6ebcd0c7cea790946057fda68727834fcb1f1ab8c2a2cbecc0cd00b7689a8f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74683082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86fbea63eca11a42df3be73da5082f4836dbbea12db110a6cd99fde0a9151cfd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1a5aa91e83fa5cc5d15dce96bbfdc6d2483a659fdee76a341522b60ff87dc849`  
		Last Modified: Tue, 03 Dec 2024 01:27:32 GMT  
		Size: 53.0 MB (52956284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79565d36fc8ccc76d07975f07b5cf916b84627952cb6785e10e8d0301cc2acdd`  
		Last Modified: Tue, 03 Dec 2024 02:14:48 GMT  
		Size: 21.7 MB (21726798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5ba1442a97ff789f6bb2cb0d3049639905dc572d7bf741c036f717f65d149fd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4053067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:015381732709d1c297b791898e04c69ae4c5205990adce22b4655b7e46a671c7`

```dockerfile
```

-	Layers:
	-	`sha256:176cb187e2706652c4ca5818dd406d955898e774f7115bc3bb60b1a2d168736f`  
		Last Modified: Tue, 03 Dec 2024 02:14:47 GMT  
		Size: 4.0 MB (4046268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f486e67dad6e670961faa1e0fcb8fc2739fd1e62af0f0638302edce42641d7c`  
		Last Modified: Tue, 03 Dec 2024 02:14:47 GMT  
		Size: 6.8 KB (6799 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:81c589f2e660a5b752bfae2db7fa09038bd3ba6ee6a790235d41ca922ea2f163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73152229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8f3b3755b9c9a37637278ae88121f4293b8b3478b630d2a334fbc0f53bc7795`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e85824c3ce994136e0b1f6545ca38052c56e3faf7dc4ab5102ef2c2e357cee02`  
		Last Modified: Tue, 12 Nov 2024 01:08:01 GMT  
		Size: 52.2 MB (52200415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40c4cfa8a0eedb22460a31984d56495095c0e6d072ab4be3aa70aec30584cf7`  
		Last Modified: Tue, 12 Nov 2024 18:05:03 GMT  
		Size: 21.0 MB (20951814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:22b45c3877321b46a20730e3995b95b27059501e1bcc9cf8fde2e2a9fadbc978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 KB (6654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d30710b7ecf8b19351e2cf995144203be23417de25869ea2d576f55f685ce89`

```dockerfile
```

-	Layers:
	-	`sha256:1674988eace870937b148290b435d75c369a1f4ef2f39991693861bc4aeaeff7`  
		Last Modified: Tue, 12 Nov 2024 18:05:00 GMT  
		Size: 6.7 KB (6654 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b24a6f3bfb5d90eae9a5f1291087f4524ece57b6baaf6d55faaee5f3ec3be691
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77946483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05f2ca9d89910187afd4b082d53679045965e64a48835dec4c14980dee2f82b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5e74ce1d603959ee7e791ff530dd1c46ce3dbdbf2d00f3d3917cd370d2c2ca56`  
		Last Modified: Tue, 03 Dec 2024 01:31:51 GMT  
		Size: 56.0 MB (55955673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e3c1d8feca2b36465cdfb5b57d9969f0fb66fe43bf079a81607bc309440b99`  
		Last Modified: Tue, 03 Dec 2024 04:38:34 GMT  
		Size: 22.0 MB (21990810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6129433d73c80b125b33b97afa7b275525f8e7db7fa264888e3dcbee986ea82c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4059849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb0dfe20db3e1186849044f17a622ccbcf2b0502819273cefab07e313414925`

```dockerfile
```

-	Layers:
	-	`sha256:fe3644c932e0d3d66e82b55f78268ecaa3c0f2e959e1d2a65cb58ae92b6780a0`  
		Last Modified: Tue, 03 Dec 2024 04:38:33 GMT  
		Size: 4.1 MB (4052996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d4161de8029270d73443c8adfd4374ea3a2773bd54db17c0c25b5bd34a74bdb`  
		Last Modified: Tue, 03 Dec 2024 04:38:33 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8c9562888bee88d31280e1a6f71a3eecacaf01e807555ec7050bdc331b4149cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70690922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59cd5d12ab06814d0d844853a51b3cdcdfea7b42f07dd7cde645329f035b04b0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:758bf82feb19a3477451e92c0cc7de2b281e4c03b2e4688fc172a592db81eb9b`  
		Last Modified: Tue, 03 Dec 2024 01:35:35 GMT  
		Size: 50.6 MB (50615063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfb15a1cc625368226ad4eb800a5fd3d4d9ac31fa481466aeee4edfc63619ab`  
		Last Modified: Tue, 03 Dec 2024 02:54:06 GMT  
		Size: 20.1 MB (20075859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:59b85afd46f933fd6f5ff6f4a36a63102c7d09a2efb622556244f4adbfefd1a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4049448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:021bdc3fd08f8b7d753a98ac09f988951399486c003e94f0afb7c53b12481988`

```dockerfile
```

-	Layers:
	-	`sha256:5e778ee90e5fbcd40a0e66c2a7740a616bb73e77471081714c36d6ae613ffa18`  
		Last Modified: Tue, 03 Dec 2024 02:54:04 GMT  
		Size: 4.0 MB (4042595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52b2fb840650ee03d4b7ddaf411e70923f4705cda031f920aacd2b11d68c809d`  
		Last Modified: Tue, 03 Dec 2024 02:54:03 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3492864c7bec0307681feb0e9e57419d8f196d4dc4c8802f2082355b7ead6126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73779519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79ac88e31d068c210c3337af30b80a35b12b5e36c13a10634fad46c9a179246f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:33a597a4ae2eff9c605f460e3e4517cc31e0999c816baef2a6ee6ab3da5c61ec`  
		Last Modified: Tue, 03 Dec 2024 01:31:39 GMT  
		Size: 52.1 MB (52069406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3f8d29d82faa501360f9fefd446cacd0bf557a29588aa4fc37c50e750000a3`  
		Last Modified: Tue, 03 Dec 2024 04:09:18 GMT  
		Size: 21.7 MB (21710113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b7b0bf870b7e705d773a392381394d425ef8eabd790acf1ca29817d904cf1bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4057460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39894dbbed8a03548b063995700454cdbae478d087f58f6db396c8545c0b3274`

```dockerfile
```

-	Layers:
	-	`sha256:bf623140f2dc9c2b694480e2869281e5d59e053b494e21260276ab187ffe8245`  
		Last Modified: Tue, 03 Dec 2024 04:09:17 GMT  
		Size: 4.1 MB (4050639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb1b7101e22a03ccec00af26972c90c63723d98e0d5310dbd1ac6e0ae345ad7a`  
		Last Modified: Tue, 03 Dec 2024 04:09:16 GMT  
		Size: 6.8 KB (6821 bytes)  
		MIME: application/vnd.in-toto+json
