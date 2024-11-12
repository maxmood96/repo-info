## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:4a79eb60c1809dbfce94556c4046d94a674a697434e0821e6b42e7a530e760a2
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
$ docker pull buildpack-deps@sha256:d180725042f2a2ab49c7c1fc447b08346fb410e8ccd2b39bc09bb2659897fb6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.6 MB (66630851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aa632581817d68db4b843ad2aa9212467fb669c2e00b7a7d088070fda64f10`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:7b183110c42f24584c122a8e76db1e925d5fd8b3489ae273dbca0b0cc3bc0090 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a5589eaa1616610f1da5585cd04faf9e418fe913dd4e9ef827abdbe93f8caa5b`  
		Last Modified: Thu, 17 Oct 2024 03:10:29 GMT  
		Size: 47.7 MB (47659640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a052304c7554ffebe70b582d4e2eb7d1d61098f5f96c8c9603940278d081561`  
		Last Modified: Sat, 19 Oct 2024 00:58:30 GMT  
		Size: 19.0 MB (18971211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:0470a2043ec3f25f0ea4f3cb171bf6eb63e84dd5756b6bf5428f806acaf5dfed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4040383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97995b1fa73615aadd85b6c368ad28025d05668f1b7b57284489e441b06335b3`

```dockerfile
```

-	Layers:
	-	`sha256:79ed41688f0e95b7523b86415bef63aa4e0dc77c85bcfcea2c6526035fa5de6d`  
		Last Modified: Sat, 19 Oct 2024 00:58:29 GMT  
		Size: 4.0 MB (4033713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e2b4c6aeb777eb4ce5f93ac05e1d77537a7e8902cb2591c2a91b517434fc58f`  
		Last Modified: Sat, 19 Oct 2024 00:58:29 GMT  
		Size: 6.7 KB (6670 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a93ed2b7476c4b4c650d0a9e767323a8425d86600c581d1a5dac3a12efcbba72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73982198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46ea30739a536e3ca9caafac54fa4ed6021ae0b7de4d14ce468c8447f4be04d3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:5d91cfda460a83c91802e918bddf6951978599b67dbd5e3c0a492a53f20d6ad6 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6f4ac25c892a8a547634a70e67af9f356a5f2b1f34e7c78d52074f2a21999111`  
		Last Modified: Thu, 17 Oct 2024 01:17:18 GMT  
		Size: 53.6 MB (53599725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b74f65518d0117b47b1d80b0bf8981ebb7ddb04cdeeadd261af699b6e5d50`  
		Last Modified: Sat, 19 Oct 2024 01:12:15 GMT  
		Size: 20.4 MB (20382473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:75b88c801460857ce4f252829edc9b947a6cc73b60e70899f3fbc468903fd61c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4039158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfdff6d26f35602884a10eb106d1fcef888490b5112225c1d15f36474069cd61`

```dockerfile
```

-	Layers:
	-	`sha256:d5fd34ed984463d07df79cc91b1d1c74f4bf811aaa1fb60164a1db5677985fb2`  
		Last Modified: Sat, 19 Oct 2024 01:12:15 GMT  
		Size: 4.0 MB (4032468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1af92e790d6db773e23efea622300f00befcf371d8ec6f379548da7163789749`  
		Last Modified: Sat, 19 Oct 2024 01:12:15 GMT  
		Size: 6.7 KB (6690 bytes)  
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
$ docker pull buildpack-deps@sha256:f834ebfbe3e95dd0a105cb4a810aaf3adc6c6391bf2680fe4c29be7a23b9281b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73095108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1941ea8fe9aa74da25cc9b80d0ac7be9bc5f367fa62c06d53ffebbea28d5c6a8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:7540ed5b693bb419df5aaa69483f55c19bc0566d076c5e65757a0a6fe38375a3 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bd6795a0a311ac784071ff263d2b83d646956234334d40fe908b91a1dde11378`  
		Last Modified: Thu, 17 Oct 2024 01:22:22 GMT  
		Size: 52.1 MB (52128468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bde6977c24ffe15c007c6606184010ccb92606e6158cbd76d8e770997debfa`  
		Last Modified: Sat, 19 Oct 2024 01:01:31 GMT  
		Size: 21.0 MB (20966640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:677a0de1f4921cb9e1a2a4c4e4672acb0db8ad7c31cf75cda470c9510bde06e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 KB (6440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee53ebeafa5f6414326bb74bb26680e262cc9dfabad9e7bae6fd98d33e9435b8`

```dockerfile
```

-	Layers:
	-	`sha256:a067562384d90203b881d6bc281e38e7dc13db73587e1a6f680ee0df93128ad6`  
		Last Modified: Sat, 19 Oct 2024 01:01:29 GMT  
		Size: 6.4 KB (6440 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:333a3246926edcdafcdb086c05e26cd8f6e47ba0652964d2be4d30ad95d33fc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.4 MB (80441503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d2a144cb176366e52828f4fa686b8276615b96c81728dc782a985f769b315f1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:7d34de8e15cda6686099080e64714532070b3d06a451fa9d77a5716745974490 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:8299bac21377f71d4bbd00f3075290f241c45c39e6a9a76012dbff5b62d14e88`  
		Last Modified: Thu, 17 Oct 2024 01:23:55 GMT  
		Size: 57.1 MB (57126645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739c73c116650c722a140d5e98dc4d5b306e6daaa1f611e7f00699c828890445`  
		Last Modified: Sat, 19 Oct 2024 00:58:55 GMT  
		Size: 23.3 MB (23314858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e5667fe15aa72deb415d8548705d0d2c925ac903348d2c609e965984d9c47957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4042566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add606c2a2dd6eefd6489f1cfee162f25d6a04391121d4b25476fa52c230804e`

```dockerfile
```

-	Layers:
	-	`sha256:ddbfe5c9a08ff9950faed8f84c34aef3b9f0e80b32022611b962f3ddf2fd4334`  
		Last Modified: Sat, 19 Oct 2024 00:58:55 GMT  
		Size: 4.0 MB (4035924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f686912dedd73eebfe8b75f1e82f2e525ceeebc2915692f915949ee62c4642a`  
		Last Modified: Sat, 19 Oct 2024 00:58:54 GMT  
		Size: 6.6 KB (6642 bytes)  
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
$ docker pull buildpack-deps@sha256:75197af0953909f02c53f06d7e40d6a7e65c221dbb2c0a42fdc262c5b4a80e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74465032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097b15816e014bf9d61c00cb9093592a90a5369f9dd284b359d92e9dfc789413`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:fe7c88cb45fa7097d71f60ba00c0d6ad76dd030e8e34771e5ee3735b59a4d6e6 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:53440987c87b8deb9090e5298bf822ffc945f186eb4c81cecc0ebf58717ca549`  
		Last Modified: Thu, 17 Oct 2024 01:51:55 GMT  
		Size: 52.8 MB (52808844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3816f9124671541da45f7e11a0a925de47e719482f5bcd085247ecdcb8c613`  
		Last Modified: Sat, 19 Oct 2024 00:59:12 GMT  
		Size: 21.7 MB (21656188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cdcdb6c4c742b0560c3cd9217a2794dd3d3f6f343b591149399564df9735cdbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4040235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10cfec82e6efabe5ecf20d815273ee2628d6a0dd1e64df1c881f7e1748c51ea1`

```dockerfile
```

-	Layers:
	-	`sha256:3af77f9d57d4a2973c5d311064cd302187c63a5d2d2d4ca220a47d8a197bf8ac`  
		Last Modified: Sat, 19 Oct 2024 00:59:12 GMT  
		Size: 4.0 MB (4033619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e2450e5fbba047105865ee8ea4145e5355d4459c0397033c277fd63d2ae0336`  
		Last Modified: Sat, 19 Oct 2024 00:59:12 GMT  
		Size: 6.6 KB (6616 bytes)  
		MIME: application/vnd.in-toto+json
