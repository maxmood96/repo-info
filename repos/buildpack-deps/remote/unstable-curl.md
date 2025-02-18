## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:106bb984732f54631b28535ddd98098a098e4aab41d359a31d70c1fca5bb8cf8
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

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f638ef05d64605d170c445f4dbc6194cb452a48dd22e37b7c512306d638fdcc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74514884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3caddad04e472fcf3574c79b97ef9b2c377554176ebd3c85ca858bcbb8bdda2d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9a66d07ec06276723a9d844f79110db2c04e99b6e7ca9f2467ee7789a25614bc`  
		Last Modified: Tue, 04 Feb 2025 07:09:27 GMT  
		Size: 48.5 MB (48478504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37249eb6f9b3505b2330ba5132b480155ccfe125c06c5def806fca9a9daeec74`  
		Last Modified: Tue, 04 Feb 2025 12:01:09 GMT  
		Size: 26.0 MB (26036380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a5a03516c213b8395285411f64ab7e53b1a86f5a65de46a7d95fafb667e0d8c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4043601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06af5378da6fdf718d35cb019e89f718b729a813ce8b83c506ee8a802ae4d389`

```dockerfile
```

-	Layers:
	-	`sha256:477cd3c19a37ed7a9ee13a81ff3da27cdcf9e27851258611a960eefd4f3e73ba`  
		Last Modified: Tue, 18 Feb 2025 07:04:08 GMT  
		Size: 4.0 MB (4036797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2f10ad7261a54ee4f8c56a579b66d638edab808a52504248debae6df278b9ac`  
		Last Modified: Tue, 18 Feb 2025 07:04:08 GMT  
		Size: 6.8 KB (6804 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:f45875ec73ce9b7c8aeb688b988e4dd79e4b6c842cd21b893b5f398a492c94ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.5 MB (71452663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b92a325e484088d0c8688eb6aea68ba80bc45eb8aafc520d1518ed29e7fe90`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armel' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:969faa28a060b3165779eb5369b5e31931290ad408fa4e8e60d177e2f80c2611`  
		Last Modified: Tue, 04 Feb 2025 21:20:32 GMT  
		Size: 46.7 MB (46706175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd2fe3d3c4202f31101bc1bc73cd3af8a62f52a1188e729c8a3228780cf83d0`  
		Last Modified: Tue, 04 Feb 2025 08:03:51 GMT  
		Size: 24.7 MB (24746488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8134fda17aa6d80f9759a5952f0ffeae4602704b27b326298b638578d10d443c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4051289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59fbe16f31e28338f95f054b58a4401aa744e22829c9917e4841dedd2e5ab5a2`

```dockerfile
```

-	Layers:
	-	`sha256:c4e2ff509be119eb73702d3d519a72531f576a70f9908862c43a7786492a6d96`  
		Last Modified: Tue, 18 Feb 2025 07:04:11 GMT  
		Size: 4.0 MB (4044425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe41ba8a61745b055d7c1ff4fcead3d482410c8dc06a548e6382e5c4c140e1aa`  
		Last Modified: Tue, 18 Feb 2025 07:04:12 GMT  
		Size: 6.9 KB (6864 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:feb9c2d61fb4c4c7b0252883717ff509c78811124a512a8ce3ecb9807979175d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68731225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ba6aec6b23b2b51d61ff1c09d4b883bd1ccf368730e25c946e90282a46f6033`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'armhf' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:eaba0613b673e68ada7f5f2b5e4971d3556823043148e63c2a6887ee2d5edef0`  
		Last Modified: Wed, 05 Feb 2025 06:15:39 GMT  
		Size: 44.8 MB (44838928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6395c61799d55a9640c01c9ef3b8549d20d61a975f9340e0353ec8e6422685f`  
		Last Modified: Wed, 05 Feb 2025 08:49:48 GMT  
		Size: 23.9 MB (23892297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fd556847f4ae2a75b56788585a6dbed042bd64bebdf265e9ad9a60375b4529d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4043885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb443e4c1924cb01c661174585062ed0e2396c690d9a227622c118244322b84`

```dockerfile
```

-	Layers:
	-	`sha256:7a16946bcda3770000ccad1fec8abad756c10a59958b8efbc69b478d0a12a6a3`  
		Last Modified: Tue, 18 Feb 2025 07:04:14 GMT  
		Size: 4.0 MB (4037021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbd45c6d9e9057c1679f44da49613d30cf0a4b169f2b71b52dbe6b2392d94da8`  
		Last Modified: Tue, 18 Feb 2025 07:04:15 GMT  
		Size: 6.9 KB (6864 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3cf31dfb3b9a512d37f417618dc8d2c709472b36c3d7493768dcaa9a394e0b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74377354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc13d99c12b3cd6acb985c585b0342c53dd123416f363f2d506091c48cb376ab`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f518c8f510cd10fda797c5ee77280d7c81b61ff1077c267de12ce9c337ddbe7b`  
		Last Modified: Tue, 04 Feb 2025 21:15:40 GMT  
		Size: 48.9 MB (48874714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b09bd24e474d679cb3c70ae42560294c37e17235d92a739791f20279494fa5e`  
		Last Modified: Wed, 05 Feb 2025 03:23:16 GMT  
		Size: 25.5 MB (25502640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b762f13089947f528337b22e97a2034d96f4970fb44b8514f374c981f492adb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4044577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2924e69ba8c13f46c71be66ca59a7404e757deedae5b1d977d6d35cfdfe739d0`

```dockerfile
```

-	Layers:
	-	`sha256:e50add4bfa70921343045e27ae494c4ba6b21657d3117a96e9e96c8f3143af4d`  
		Last Modified: Tue, 18 Feb 2025 07:04:17 GMT  
		Size: 4.0 MB (4037693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:accd7297c44bb051bb6828c0c99e27d5fcba3fe49d95e31fdc9ff6b84e6b2fdf`  
		Last Modified: Tue, 18 Feb 2025 07:04:18 GMT  
		Size: 6.9 KB (6884 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0f50343f2052ca365fd8378a57d6e415675836af02416da168be148c36f4b236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77069858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e0fb9d10924a5ef45ec45f9c72c8b720d45649556a48e0328c36eff1c0af02`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:51741382468681fc53992e03a5e8ce7f591198e39599d81f3b698e3652a63db4`  
		Last Modified: Wed, 05 Feb 2025 12:01:47 GMT  
		Size: 49.9 MB (49883916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4227754a1dcb648ed5c4c8f40f8d60f655bb96ef669b5da48ad50132dc9621`  
		Last Modified: Tue, 04 Feb 2025 04:23:42 GMT  
		Size: 27.2 MB (27185942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:69d9c63d976a1d2ec4df4b17cfbe241837c6d3fa77e82c0ae0239bc737f75989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4039334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dbff316c1752c79b0991fef1767dc049c843f8e4a6d26117434c6b95b5ec6b2`

```dockerfile
```

-	Layers:
	-	`sha256:80121ec0759de207705a8e6b0a5f2635b3c614ec56b2e4172a71cec99f8f701e`  
		Last Modified: Tue, 18 Feb 2025 07:04:21 GMT  
		Size: 4.0 MB (4032552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07ad54558e3d4158f6d4b0dc6bea4f73a317cde2c777f58a1128b0e6db038b16`  
		Last Modified: Tue, 18 Feb 2025 07:04:21 GMT  
		Size: 6.8 KB (6782 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:aa05dc86622d5acdae657a6e8d533c854b47c91390e4a8fd9461b0f2395b4425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74749601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:640bca2ee778df3ab3b2cb62893467ff967aea76ed7bebd6d55f83859c7988dd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'mips64el' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6ba41641f188bb1d74522008f197d258fe218bbf039fa1f236165286ebcda75a`  
		Last Modified: Tue, 18 Feb 2025 23:19:03 GMT  
		Size: 48.7 MB (48680970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1214950258d5885930b9bdcaedc26eedd6794e5ab349aac8800d95c05105fa89`  
		Last Modified: Tue, 04 Feb 2025 19:27:31 GMT  
		Size: 26.1 MB (26068631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f52175c9c93d64bc7cbee5a46e631add140778fdb42a7b920f358b8e12bb6cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 KB (6637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:accf8d55da0e331b61a0d7a392e7eefbb99473ccb2a8fe278877de6a783e5614`

```dockerfile
```

-	Layers:
	-	`sha256:99420b32f3fd16ebd660e100b21537b3aead41e288962036279524044dd08e70`  
		Last Modified: Tue, 18 Feb 2025 07:04:23 GMT  
		Size: 6.6 KB (6637 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b444e034fcd78a58112ed02d5089c9ed9523c0bcfeb72959d9d38b5e76918c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.9 MB (79881843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef59a3f5555ebb3a1ed91d3955dfa71dff4e43bc9f33b75541cb5c1d31ac0961`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:20ee406f6988f44113bcc71bae5adfb439e360c88b767260000751228a498e00`  
		Last Modified: Tue, 04 Feb 2025 22:22:01 GMT  
		Size: 52.3 MB (52287301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089b8eaf628cc7675b29225b3b455c5d86d2c6a1f5fa29d78dfb7f3bfa69b3ec`  
		Last Modified: Tue, 04 Feb 2025 07:25:22 GMT  
		Size: 27.6 MB (27594542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:104cc649b82b1e77cbd6184495b219156bcbf219aafc3ffa91c645b37c7397a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4052300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa49d461d527f74f3e9579c6ffbcd86bb78f64c91f1a79b6e24c087d80118384`

```dockerfile
```

-	Layers:
	-	`sha256:06ac9900b3736f9ef1743b06b377a584edf329ccb407da2e23a82060d06fbff4`  
		Last Modified: Tue, 18 Feb 2025 07:04:26 GMT  
		Size: 4.0 MB (4045465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb608baa041b04181310aae0975ae61d6de897858f601e0a076a01d775590fd5`  
		Last Modified: Tue, 18 Feb 2025 07:04:27 GMT  
		Size: 6.8 KB (6835 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:2734aa4dea895af92674c6244686355bcfa7c5f532af30ab2ccd9a106e755945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72452884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b17487fc2e48d4719f558a2b395daac4854c5cc8027f11e20fc0a057d484f87`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 'riscv64' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:41a19e48936e10f226b6bfe61097156b74f03101f788496e8860f0d4806f05ba`  
		Last Modified: Wed, 05 Feb 2025 12:01:49 GMT  
		Size: 47.0 MB (47040914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a706305f90a9f6f5a4662ef1063ca9b1d12e77b9f1482c3925294e4989eea2f`  
		Last Modified: Tue, 04 Feb 2025 04:38:37 GMT  
		Size: 25.4 MB (25411970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:44623c62d8dedafe11ab33444dff3d267c0b5a8cbf31207f2b7ea43d5854da5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4035021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d21dab2b6e78a3bd7ee008870193435baea98bbc4121d11d2482fec4e3e7e14`

```dockerfile
```

-	Layers:
	-	`sha256:dd80ddface841cec8633795f62cdd6ea9def4ba807b88f55db178fced191241e`  
		Last Modified: Tue, 18 Feb 2025 07:04:30 GMT  
		Size: 4.0 MB (4028186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:541368828ce448681a506ecc6bf3db770febf0bada8ea05ff3b963e42b1f3d0e`  
		Last Modified: Tue, 18 Feb 2025 07:04:31 GMT  
		Size: 6.8 KB (6835 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:171e8794c6153ede3b2dcd344446533bc1d8ea6b0b18282773719bc84686f7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.8 MB (75775246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63fe77152201f7c14106126b989c319db82ddb59047e1a6ed9a845747d8d6239`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Jan 2024 22:06:44 GMT
RUN # debian.sh --arch 's390x' out/ 'sid' '@1738540800'
# Fri, 12 Jan 2024 22:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1f48ea4a277664853f54eabe6340c7571241c845468906404bbb1efd60e69807`  
		Last Modified: Wed, 05 Feb 2025 12:01:49 GMT  
		Size: 48.6 MB (48560783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1f7d849459507f8a608795416d02b409e9f01c22159fa5acaf53ea0891b503`  
		Last Modified: Wed, 05 Feb 2025 08:49:47 GMT  
		Size: 27.2 MB (27214463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:unstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:87d777a50cfb26dc4d318ba34304296d2a7dfc51aff23790a64b8bf9d8c268a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4049932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68bcddd9e386b9d03f6814425470a8ea110334e24aa94511ea90bfc36742ec67`

```dockerfile
```

-	Layers:
	-	`sha256:9cba160456722d8e64ad7d4fc68cc65901918c0c5bca0dd5108b22cae6340e15`  
		Last Modified: Tue, 18 Feb 2025 07:04:33 GMT  
		Size: 4.0 MB (4043129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6b747fbcbe0026e5bbc6fd98c53854cdf3b2e96844372ef3cc2b6170266f168`  
		Last Modified: Tue, 18 Feb 2025 07:04:34 GMT  
		Size: 6.8 KB (6803 bytes)  
		MIME: application/vnd.in-toto+json
