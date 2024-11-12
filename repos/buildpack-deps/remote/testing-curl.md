## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:ab834ad536df5563da2eb202fbf667204c33c7c69f3e9d455af94182feef8593
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
$ docker pull buildpack-deps@sha256:2c9dda7b58f3cc1b6b5e844de7f661770af7817eeef0978bcb78f577596eca7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73824673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb86d3cefef9bea16dba2bada8facb004fefd5f8630d2c2e9ef621dc30fc334d`
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
	-	`sha256:723f7d6ce61509bbccf2af45aa75a4c5cd83b188d6e85822321cdc68268417bf`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 53.2 MB (53226763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1538514cb923497c68c854e6f9e45945ca05f4a0f5a179472e7f81b1ee0cfbb`  
		Last Modified: Tue, 12 Nov 2024 02:38:24 GMT  
		Size: 20.6 MB (20597910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:341e02af8da6e03d6cb6c843c920d1e11a358ba849e80427f814ea7d8167df0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4061376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f70136036ca06b148cdae061bc19b58ac4328268fb771f3a7d56712d4afa47`

```dockerfile
```

-	Layers:
	-	`sha256:cc3306c9a01b6e93fe278e11e07f05c659419817f5e82f4aac8bfeb2207d137a`  
		Last Modified: Tue, 12 Nov 2024 02:38:23 GMT  
		Size: 4.1 MB (4054555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04b7ee26ecf9dc640a238d3ae29c2b9614a6a82f979626b18d6f48299c4e2c3b`  
		Last Modified: Tue, 12 Nov 2024 02:38:23 GMT  
		Size: 6.8 KB (6821 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c09dcf78f1b0a06c8bd6f465a1adbebc5feb2fbe3f83cd9dfd2969b1f5feceb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.7 MB (69699297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a10d26a23af3144f1ea9c16aecef6411b34e0b5968162d389df222b05cad850a`
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
	-	`sha256:4ff391534f557bd19067799d6e6b7e386e43cbf7d061a795a182546eb2145e99`  
		Last Modified: Tue, 12 Nov 2024 00:58:57 GMT  
		Size: 50.1 MB (50091523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d129d70e5af0f50e5354ff02342f42eba97458b43a0df2209f72566f664a4a`  
		Last Modified: Tue, 12 Nov 2024 06:29:56 GMT  
		Size: 19.6 MB (19607774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:36013fb61628706615c5cf999a5952e22dc0dcfc8f985bb9b318ff8349ace822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4063658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5becb61b4809956e3da35a939f26fabba7ff7639d8c825ccb68d86ceb2f66025`

```dockerfile
```

-	Layers:
	-	`sha256:7a526bf7c983b9f3e240fb3a59d54f61c33f79916e8fcee7c9f0071815b438f7`  
		Last Modified: Tue, 12 Nov 2024 06:29:56 GMT  
		Size: 4.1 MB (4056777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f435a4ab56f4980a90c473c5c339e287f55acb946c26cc36ddbba38e0739a1fe`  
		Last Modified: Tue, 12 Nov 2024 06:29:55 GMT  
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
$ docker pull buildpack-deps@sha256:556e7e00b135aa369fc03c74579f79f4eae25c78e4bee00635729b6f12018df8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73922052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1be941a9867f832ef97ccf00bc779f0b68e380cb201a0a24c3026c9c509b135d`
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
	-	`sha256:4de57c6718ff0fb4c76cd3ff1a33db2bde24e482395a89d0d4f6c7e6b3c20f53`  
		Last Modified: Tue, 12 Nov 2024 01:03:14 GMT  
		Size: 53.7 MB (53669977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27cb33ae9e17116eb9be8382614725b619742aeedfb992b4bc26c5d5efa717e`  
		Last Modified: Tue, 12 Nov 2024 11:17:43 GMT  
		Size: 20.3 MB (20252075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d29c4fe931cedbe6dfa651e2107a03afd42cf2d8299d01445482c14cda8f0831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4066350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44cd0cad434906c6088ae004cae4327ef76d01dffa1a84cf157f7b78eb178589`

```dockerfile
```

-	Layers:
	-	`sha256:2a8bb80f2fa2059b19dee0dd06a01b5cc7aa7b85877be888124ee5bb76a4d3e4`  
		Last Modified: Tue, 12 Nov 2024 11:17:42 GMT  
		Size: 4.1 MB (4059450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9fd3ca1a9a3a8d76e8e4b087e685f0d1e2b32ab3bff8f0063a6c264d63c9949`  
		Last Modified: Tue, 12 Nov 2024 11:17:42 GMT  
		Size: 6.9 KB (6900 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:da816f8eb964403dca1d95dba259e31f140b9fc698f9815a96303413255f25fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75817617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad9ee0f4bec9c6fef7ee3aafc5b49c3ce72fe4c7009a22352f698636585b21cf`
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
	-	`sha256:a04f0591b5521dc9360454fa2fd6b21d9b7d989bb4c88327ad94f8282af3b267`  
		Last Modified: Tue, 12 Nov 2024 00:55:13 GMT  
		Size: 54.1 MB (54095157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914cc5c9bed5c786b85a6e40864cd3fb4af442dea3455ca88a01cfa26707d8df`  
		Last Modified: Tue, 12 Nov 2024 02:38:04 GMT  
		Size: 21.7 MB (21722460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9d0e6300c6451b2db0ff47a7b39d3b135872ec077ef50f473bddebefe68c2581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4057092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49fa3c56c66f4081ff0151f120b4b13784284fdcc2fe4a32b10b05bc9831a8d`

```dockerfile
```

-	Layers:
	-	`sha256:9b0f991f6eed552a6a904617d1e2af1fae7d23a97a5853ddb4b44b53b774fbba`  
		Last Modified: Tue, 12 Nov 2024 02:38:04 GMT  
		Size: 4.1 MB (4050293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa54182865e1c17ec6dd4311af29948d3270ee77ef5541ad3a9c3fd8fb0c8c68`  
		Last Modified: Tue, 12 Nov 2024 02:38:03 GMT  
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
$ docker pull buildpack-deps@sha256:b36ab86690611318dcc37e932f66352a6a608990639315d31b5db60822e3152e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79177514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8767495c53385436730670f594cf2570df7c4332029e877e7ccaa0497d0db1c6`
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
	-	`sha256:554b3bf5ec10b22cc962f7afc042e96c50635c0e2b0d817544a202afc2a52711`  
		Last Modified: Tue, 12 Nov 2024 01:05:47 GMT  
		Size: 57.2 MB (57193598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08187472bfe4fce6e3b2fc2951e231ce30c71f70be1dc829ad73735e312d479f`  
		Last Modified: Tue, 12 Nov 2024 08:31:04 GMT  
		Size: 22.0 MB (21983916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4163f50eacc16a9a74dacef16c13fe5b0e88708e96517b2d33282f53abb663bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4064697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea12c2369d549c15187a9e4de29519d195d5e11321f44ca7565e6f43ccd8c68`

```dockerfile
```

-	Layers:
	-	`sha256:8bc27c99b4b763ad4265fdae7572bf9de79c8c842950e22de9451dc57b21f89e`  
		Last Modified: Tue, 12 Nov 2024 08:31:03 GMT  
		Size: 4.1 MB (4057844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d89080bcc025993b77857d5b2cecb80f56da462e48216a66ae8586a554111e2`  
		Last Modified: Tue, 12 Nov 2024 08:31:02 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:24dcbbd0e2ee32d1dba9e2e5844af10d131703be2f58837fd22aa7f1f036bf17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.7 MB (71667113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4bd6b050755f4e2f11dc7120e640aa938167574228c3e901d4ae13e0d782f07`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:a39f1e594ed2d718a6cabab2e5ea2ce29b47a86f2d43588cafbf682ddc9af2ca in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5c18b80e18178230beda6e484fe9dcde3f9663fa4695718e63800e23f1c0399f`  
		Last Modified: Thu, 17 Oct 2024 01:17:23 GMT  
		Size: 51.5 MB (51529184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9afe98cafb187775506b46e655b83f4d919ff657d9c24036a88a37c7e186b3`  
		Last Modified: Sat, 19 Oct 2024 01:06:46 GMT  
		Size: 20.1 MB (20137929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2125c80eac7fb61dee0bf4629df8ac0785422e6e4c56f8f15ff090b697e76324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4031349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc49637a86d8c0ceaf270f6bc7ded55e1afba9aee8479567a486af0a1a9b906b`

```dockerfile
```

-	Layers:
	-	`sha256:a45cc8e562fd303037be29b476fa881a7ec77fd72466df42383dc6c612c2088f`  
		Last Modified: Sat, 19 Oct 2024 01:06:44 GMT  
		Size: 4.0 MB (4024707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c9bb89a3de98c2ea298a2ff66fa98c5e299403e1665068622932e7b890ab2b`  
		Last Modified: Sat, 19 Oct 2024 01:06:43 GMT  
		Size: 6.6 KB (6642 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:dae85776025d232213b996742b5a8627c1670b132b805534906e88e0ecfbd920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74594615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f467ac0e350dd644702d1948d2a30ebef2ae600aeccdc895d9a61a3afc0ed91e`
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
	-	`sha256:a54a131d29bb2d4a9258476cdcb51efa9314272b8894e2474e100e5d38d85679`  
		Last Modified: Tue, 12 Nov 2024 01:05:54 GMT  
		Size: 52.9 MB (52885488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a20f0f48b3016dae43f5b6fa4b9b89a2e08fbca4da340a0b01b79f3c8a37e0f`  
		Last Modified: Tue, 12 Nov 2024 09:03:50 GMT  
		Size: 21.7 MB (21709127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6bac11572437bb986cc2a3d91d185683c1877927cfeb576f23d4bd47c966ad22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4062302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c186f0d8a809a7d02f80d17bea3cd8be3931de9e10af463efc5ca9f15f6bfa`

```dockerfile
```

-	Layers:
	-	`sha256:0b946d20078a601263710f001ee104501a07e38f3ed5d718971c854aa87fe4f1`  
		Last Modified: Tue, 12 Nov 2024 09:03:50 GMT  
		Size: 4.1 MB (4055481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d2d0b1740b206909317d79e93207de19502facc9b8442347f2ab05b9e999748`  
		Last Modified: Tue, 12 Nov 2024 09:03:49 GMT  
		Size: 6.8 KB (6821 bytes)  
		MIME: application/vnd.in-toto+json
