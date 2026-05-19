## `debian:bookworm-backports`

```console
$ docker pull debian@sha256:6b0dfba1cbddd861da7395645117c58acc9d9b7574c0dbcfddddd13643d405e0
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:bookworm-backports` - linux; amd64

```console
$ docker pull debian@sha256:a457ccce24db436f72b295ebbc5bfdee852a8cd2f8d74e7fa1ce613a066d16bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48495657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a1723a9bc433878d17e64663d29f2b8f049ed9530301a227887abf54973234`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 22:57:37 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ad45b192ad7f19c44513b8712e318218086232c6957e8c51f4b7e626a418ad`  
		Last Modified: Tue, 19 May 2026 22:57:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c59eacc360135ab5224aa043818a8fe68042828a852d051b84c55aa9abe3e3ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c395e62f792c7872e2653204123aa5ababa11365a5a88473a96806f3499663`

```dockerfile
```

-	Layers:
	-	`sha256:b5ed20ba6a099e5b9fd4b7e4350b061da5ce7ebb83ffe22ea4670dc67445bdff`  
		Last Modified: Tue, 19 May 2026 22:57:44 GMT  
		Size: 3.7 MB (3734092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aac122618d9e8f1ef87534ba3f12d55beab88321ec74d001be717c808046bd51`  
		Last Modified: Tue, 19 May 2026 22:57:44 GMT  
		Size: 5.8 KB (5804 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:c5c6b8ff25254f271517a6a0fd5f70314b5a2f94b7910d2a7632a964917d3915
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46029730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a297662d8027b12288fe51b28770cf234b1e809cac33f9dc25a5203abc8646`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 22:56:32 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:5de6cd71f4d67443f5513239f3846f94cf483b810583f2d4d2ba8423f1ec7fc3`  
		Last Modified: Tue, 19 May 2026 22:36:01 GMT  
		Size: 46.0 MB (46029503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9560cc46ab91c4f61482857ba1fb77a47a96948571ed4ce62791c1b95d08211b`  
		Last Modified: Tue, 19 May 2026 22:56:39 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:3be93ccef12fb3567010032686009c16f29e57e713c9155131b865608ed9222d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8582bb292d8743c2da74188382573516e27071ad077a91ebf2a12c69666ed013`

```dockerfile
```

-	Layers:
	-	`sha256:70f23adecaa78f4c2a4dee7bebcb617ccd9d322949b1a6c5bb390efc998bbb48`  
		Last Modified: Tue, 19 May 2026 22:56:39 GMT  
		Size: 3.7 MB (3734293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8245e699d48b9633cd702f02ca01d101cac76e1c8728d05bf47a24dafbca161f`  
		Last Modified: Tue, 19 May 2026 22:56:39 GMT  
		Size: 5.9 KB (5859 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:9db47ef9684806b630b4c5c758d9dd2febd4945898b9e1d6000b86a8441d66e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44209379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ef7dc7032341e204f2d38ec9a9aca5cce911fd3bba45dd277ed18eaa9c9cfa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 22:56:39 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1af0b8b84389f4347663cc563bc1f6d59fe6d6f21081f428bafa1a09f6a276ce`  
		Last Modified: Tue, 19 May 2026 22:35:59 GMT  
		Size: 44.2 MB (44209154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb535b12ead0be8ece97ec030f1f920009c6a7663af0e7d38c104c2e0a2cef22`  
		Last Modified: Tue, 19 May 2026 22:56:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ce32bc0d2fe503bcc2aaa5d42031c4d150f054063e55737ed68b43d0e78c7aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3742130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba27dcce8a9e56faac4c332597631189c053f889173891867ce7c8ba2cc150c1`

```dockerfile
```

-	Layers:
	-	`sha256:69eac1c4144a6beb133b81d51f8c5123018ce18c58aed74368c05acdc486a70e`  
		Last Modified: Tue, 19 May 2026 22:56:46 GMT  
		Size: 3.7 MB (3736271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be0367a5bc256fdd5410f6acfe0c9538e956467271bc9719249ddd067b609310`  
		Last Modified: Tue, 19 May 2026 22:56:46 GMT  
		Size: 5.9 KB (5859 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:c71aad04fef46dfc445caaadb8d9d23f6ee6a3817513151da9f08e8a5ed8f4b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48379658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e04b45bff1f0929c56c1a67e710a565570db7f797aacb40dd3b7f2b7f9f3ee`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 22:55:33 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e6a83ae481c028f8d592cf991e230e52f5b5bbd822c515f090f975e19d3161`  
		Last Modified: Tue, 19 May 2026 22:55:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c717bf2e4b94a1f9bf92a4c11962f3dfe917b8419f77dbe5dd77825970145910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3740179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76bddb0d57c14e530521b5cd5c5b930966b1598131f4d5fb134eb476ef202530`

```dockerfile
```

-	Layers:
	-	`sha256:86bd2897241f0c19d5cb8e48a1cb3058782d266c03824829e38db70786cb7138`  
		Last Modified: Tue, 19 May 2026 22:55:40 GMT  
		Size: 3.7 MB (3734307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cb3728b7d12efab306eef6dab9becad8a7fe390d5e35cd73fa9737761d63fb7`  
		Last Modified: Tue, 19 May 2026 22:55:40 GMT  
		Size: 5.9 KB (5872 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; 386

```console
$ docker pull debian@sha256:f38fd621bb7aee6d7621cc52944949a781671c34be9e1252673963b62716370e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49483345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff3b9cd668d65a37bd720665c6c5bf5b70aca5ef3351ebaf2d00db23ac671cc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 22:56:53 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:8bf11fb6e89cfb8d682f511fb7d1b795e747af9c12a192f45f6e50ae7ca54f50`  
		Last Modified: Tue, 19 May 2026 22:36:20 GMT  
		Size: 49.5 MB (49483120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02274850cf801f44cda3a0fb8d787f81f6e1d0871ed63b694f81e293811d2e58`  
		Last Modified: Tue, 19 May 2026 22:57:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ba54076e2ff8f9a47d49597fbd7825cf63ea74252b55ec85f343b09343aef8e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3737075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d69eb9391a8fc010cea2e280e8f09b0b18511b02a8ec5704d93a20c27f6d4bfb`

```dockerfile
```

-	Layers:
	-	`sha256:0a3cb2f1a2ab1d23744b78d8b0df35ed3aa2f0919750cb3ae0eefac79695bb39`  
		Last Modified: Tue, 19 May 2026 22:57:00 GMT  
		Size: 3.7 MB (3731288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:883f27e6814d40af03d861461f131c600d71780f79e0e42460dea60e5a1e0b97`  
		Last Modified: Tue, 19 May 2026 22:57:00 GMT  
		Size: 5.8 KB (5787 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; mips64le

```console
$ docker pull debian@sha256:97481d9689e20820fd98def5aec3e61a39054db3d9a96f8631123abb0a5b9a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48786464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de534fa3cd569dbcf12fc4a77b025de6350e3cadaf5c5807a1f3dfdee0e8e3a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 22:56:24 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:813eaff938e8991b3dd16851af2c46dd2ffc5bb600e30ff866dd5a60502fbffa`  
		Last Modified: Tue, 19 May 2026 22:35:13 GMT  
		Size: 48.8 MB (48786239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d3e1d26b9c87d34f9aed080e27c029cd8a4be8c83bab1835e8d72bf439a86d`  
		Last Modified: Tue, 19 May 2026 22:56:41 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c1b7327dc4c1caac33daf7b514d9326b074f292ef5ba92fab02e26635433e755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 KB (5628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c59b4d9ffe75d61b8ef0f697d5235d10cafcdefabcd65d250b9739268cb06ae`

```dockerfile
```

-	Layers:
	-	`sha256:d1deff15dc7bde1e5a5647c97acabb96dfa0f0c1ca1402feef329dc51169ae00`  
		Last Modified: Tue, 19 May 2026 22:56:41 GMT  
		Size: 5.6 KB (5628 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:3919f22f02a732d94915823610a6ffbc306cbcc10b6e04424b86cbcf86fdcf52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52340425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b72c19c2e3a5704bbfe9db13f7c7a990fa74c2e55a237b2e989cbbc818971e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 22:55:32 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b3943e183051423c3dc79fa53ad6d50fff9621945bbfc636eec039b14ead2b66`  
		Last Modified: Tue, 19 May 2026 22:35:10 GMT  
		Size: 52.3 MB (52340199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e6a83ae481c028f8d592cf991e230e52f5b5bbd822c515f090f975e19d3161`  
		Last Modified: Tue, 19 May 2026 22:55:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:31b92c65dddee42ea61dec324df1f0113786c2982c43f198b3318d8dc61482e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3744280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704215ef4da14b1145340a570ae8ea12ce3b836b6d83cf445d4e106663bf8abe`

```dockerfile
```

-	Layers:
	-	`sha256:17cb67cee7e846f731384cbbf8e8c44cb3ed31884de354b2636c938e9bd05e16`  
		Last Modified: Tue, 19 May 2026 22:55:47 GMT  
		Size: 3.7 MB (3738450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c2b312dc2a4ee8be4b6f8c7b94d331c6478acceee82e664eb3a8d1dbd3086fd`  
		Last Modified: Tue, 19 May 2026 22:55:47 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bookworm-backports` - linux; s390x

```console
$ docker pull debian@sha256:8e7237e59347bcce09eea7dc1782328ccea7b906a24f17516ce464c71e358fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47155814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da32a606b346c4f1811726b58849a1d62763714c6ac410fe3ec65fbb5c7fcf34`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 22:56:05 GMT
RUN echo 'deb http://deb.debian.org/debian bookworm-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e0fc2c7a6bb12f7a9b333cc117b6ea5fa5cf251c5fa4dd298303beee01028f59`  
		Last Modified: Tue, 19 May 2026 22:35:39 GMT  
		Size: 47.2 MB (47155589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e001552467fced654d8938da8f5fee9ddd1eac67c701c99efee44798d0b73534`  
		Last Modified: Tue, 19 May 2026 22:56:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bookworm-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d15402d3fb70c324d04b210aae9f5f2f6b59e4c521ec6d099a3a78f5a2b68be3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3736733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a7e41e02d22c55e7c2c83bc7b52b981cf218cb4c6b8f2e599aa7fdfcc5d283`

```dockerfile
```

-	Layers:
	-	`sha256:7fc72f3f7c3144f79bf354086765fccaaf558a25bb04da71550a4369b3c6cf44`  
		Last Modified: Tue, 19 May 2026 22:56:16 GMT  
		Size: 3.7 MB (3730930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf5611f80e39fd776176c4f28c747a00de873e0a3ea8b800dab4fb7d9dc1128c`  
		Last Modified: Tue, 19 May 2026 22:56:15 GMT  
		Size: 5.8 KB (5803 bytes)  
		MIME: application/vnd.in-toto+json
