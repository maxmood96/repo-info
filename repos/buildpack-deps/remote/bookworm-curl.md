## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:441a4291a9c28dc580c98ba1c4f0145a6f5fafc2975a2dc70bda3bf106c86557
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

### `buildpack-deps:bookworm-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:3d2a48cc35c51e75eb583fb23e3d6af77c0775dad398295cd28a62cdc72c7128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72515352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103b158642900db6b962343d7882810e87418501109009f19bfac2b1a56fad17`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6401b7636bba3fe2d916b154ba44abe2081a737e117b2c736167ca6ea42334`  
		Last Modified: Tue, 12 Aug 2025 22:13:44 GMT  
		Size: 24.0 MB (24020841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:97cbada548dead5df809b791de14b78c51f0f6b8777ebfca238ded74643508eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4514386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d133586aa28744bd9f7ad057fc24231dbf0480ec5779629c0981a3149509c8bf`

```dockerfile
```

-	Layers:
	-	`sha256:af8138236f5b4a3433d40f90bcddd3ba103e2930b9d6fc1b614efba16a386ddf`  
		Last Modified: Wed, 13 Aug 2025 00:03:27 GMT  
		Size: 4.5 MB (4507222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c90b5aa1a35faa2d2245cd7312c3674609e4136b3647951093e526bb5c1539c`  
		Last Modified: Wed, 13 Aug 2025 00:03:26 GMT  
		Size: 7.2 KB (7164 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ec0f1121a688acd6ec8e8705fe43351b58a1f6c875fcec44b2892e425a758ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68723497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bed663084252dbf0208518a50ed63c7866fdabb7a69544cf3e9c90c5e29d97b6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ea0d25317149dd26fe3fc21f7a1766f8528af12760c2aee4e2fa23834000897f`  
		Last Modified: Tue, 12 Aug 2025 20:44:49 GMT  
		Size: 46.0 MB (46027235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d77dbe9c143107c5d6e98f6ee7910a0557899d9127736c302e12bf8899d1979`  
		Last Modified: Wed, 13 Aug 2025 00:00:04 GMT  
		Size: 22.7 MB (22696262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:748a6f1490b2260e2a8dddc956edb480b6b63288ae76dd0b35cdee46b9dc7ab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4517654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82532e391ac64096b7779fe6883e6470f5fdb7e7268d65ee16600204d4bc497d`

```dockerfile
```

-	Layers:
	-	`sha256:44cc195d3537bc69e0111f0da09f50eecef428ad2569bf540727a353cc25bf08`  
		Last Modified: Wed, 13 Aug 2025 01:20:12 GMT  
		Size: 4.5 MB (4510734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfc5f985b8d00dab03869168441c5858f19ba46b0b86b6c31d2a435a91f42a50`  
		Last Modified: Wed, 13 Aug 2025 01:20:13 GMT  
		Size: 6.9 KB (6920 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9b7a9e62c00d4b6b1f590bd089f40dfad39d7298e3fd7b5f1ff8d9d14eb8eec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66138409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e83d35b5f3752637df0cb1813c89a1990603ae7540a392f21b664d5d1fc54271`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a06e9cd35e09740ec78f63d1179c1e1528d9cfd9686a0094a4655ebe70922c99`  
		Last Modified: Tue, 12 Aug 2025 20:46:18 GMT  
		Size: 44.2 MB (44209044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4756b55428372e77ee6ab2b6c5a35bda8bf113537f0ebde9510c43737f4249c`  
		Last Modified: Wed, 13 Aug 2025 00:15:08 GMT  
		Size: 21.9 MB (21929365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f4387ed9565581e2e94f32b20d4c2d9ef411977d0ede16374e3c59bb827c649b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4516127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:182c8bfe80b12e97b8d0430a38f5242faa8d729a0221ea71176971c3d94ebdaa`

```dockerfile
```

-	Layers:
	-	`sha256:4e25d821e96344469739bfdb258b1b48c7a5fe6617c174eab7da9148e513483b`  
		Last Modified: Wed, 13 Aug 2025 01:20:18 GMT  
		Size: 4.5 MB (4509207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:469e757e83a8e69b77b66914f5b8b4d7f62cb10a75858923682856b07877e50f`  
		Last Modified: Wed, 13 Aug 2025 01:20:19 GMT  
		Size: 6.9 KB (6920 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e8e0a49f7915588c961b8d6204545d909d1fc8816089bb2d560311fda74df624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71912297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ee10ccee7deb327f6f16256a629cafb04aa9691490d5764975d04a82d3dc66`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cff9c97e1a1ee42786188e1d1b57f6a2035d65b648178ac0262d0eba0c5c86d`  
		Last Modified: Wed, 13 Aug 2025 07:22:32 GMT  
		Size: 23.6 MB (23569847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:6d4e460487f98b32f34fa76711beb725df7549c0d799755499cb96a7c8d45189
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4514119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0f1186a4719dca2665fc534aa604d5d1359a3c9d7e6552e1f06d2da1b14269`

```dockerfile
```

-	Layers:
	-	`sha256:449404a0d27388e218828408e6824340d0200f4ad948fd8479d177ecac4403b3`  
		Last Modified: Wed, 13 Aug 2025 07:19:56 GMT  
		Size: 4.5 MB (4507179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8c25cb6373b7ed84d96bc3b43ede1fbd77cd6b3c6f6156c3b3a05f720f94155`  
		Last Modified: Wed, 13 Aug 2025 07:19:57 GMT  
		Size: 6.9 KB (6940 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:876de160cbccbc028374df65147af52240a55c217c45a167adcc51bc30a4be53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74339240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c75b3a1a2ebabd53babd538190d11f2f7ff041d2b570495ac39049083b30ec`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:73488b414dce83adc963656678257daf6a25aaa9e6d76928aee03f81611c17ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 49.5 MB (49478115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874646e2459984b117c58d731a64ebcb9d23f76cf755c68e1ddb30317e57abc0`  
		Last Modified: Tue, 12 Aug 2025 22:13:36 GMT  
		Size: 24.9 MB (24861125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d03569d3ecb22dc15dc6f16e6e381023ed028c898de53380b9e9dfab9c8d043e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4511479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b5f76fd293b3f0687bcbb20e7e4313faf306a2ebed7ca82ad1793092778ec6`

```dockerfile
```

-	Layers:
	-	`sha256:932157bafec5af8c8bbf1ec423c383766c04b225a0ef4fa68b91cc3b221152d8`  
		Last Modified: Tue, 12 Aug 2025 22:20:22 GMT  
		Size: 4.5 MB (4504342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f5216df174f61c8338e515501b0bee20938272041a0b490fde447afce552a74`  
		Last Modified: Tue, 12 Aug 2025 22:20:23 GMT  
		Size: 7.1 KB (7137 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:3f71953104513ba7020effef5558f88afd9e6b539def3a111834ec69ab24bc38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72380316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6540f5b267d3f19d8dc76e6e004b720c52ffc345c6a441150ddb30434c4f6c20`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:39ab9a968f454fda0ebffae415d31434cb4c4b3f4bb9da0e89f360bd60fa3275`  
		Last Modified: Tue, 12 Aug 2025 21:09:50 GMT  
		Size: 48.8 MB (48776657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5bf976bc5466a2e4cdc6d87c28337bf663ea094da7d169694d61961d11248d`  
		Last Modified: Wed, 13 Aug 2025 06:38:46 GMT  
		Size: 23.6 MB (23603659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7bd274409d19a39b189167b12ce6049f520fee4634f92a98f9cdaafbd5edb8d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 KB (6693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5506fd53287b4162a1c26ba91bc94a4283685a306e817b14b0cf3edd76f5cf9a`

```dockerfile
```

-	Layers:
	-	`sha256:d1bf7c7978327e95b459be3fc7fd8058667b9fb34061afdc98b9d5d581f26c79`  
		Last Modified: Wed, 13 Aug 2025 07:20:04 GMT  
		Size: 6.7 KB (6693 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:6951ed9bb1e94b9fee3f62fb8a42f913e0843d5a4a84ff950d14d2502dd09198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.0 MB (78004116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63d4b341086961a1ddff5038d1b3a943735a81c1c96645f5a6b7320ad14cffc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:33bc01697f2fcceb00fe53fe1bf433b48dc127c82c1555f61eeddeda9d72ff40`  
		Last Modified: Tue, 12 Aug 2025 23:05:53 GMT  
		Size: 52.3 MB (52338077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f87ea767eb09118b3668a0dc44ddf5bf258db4f1bebc7989803cb1b75a66c9`  
		Last Modified: Wed, 13 Aug 2025 14:33:16 GMT  
		Size: 25.7 MB (25666039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:4a811509fbfb567ebae0de4b94798fd445730d48e731f0487564258e04f88e58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4518423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4024c9ffb56d23e45b3014fbba463b95af348d0ef10878112a92213db30f6fd`

```dockerfile
```

-	Layers:
	-	`sha256:c586a856b12a602176a8a5a0ec14c68f80338bdb78133fe91d8970ef42745ec3`  
		Last Modified: Wed, 13 Aug 2025 13:20:14 GMT  
		Size: 4.5 MB (4511532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9efc2b9829de6c347e7b75208474e579e0c1201fad567fa42b1b23a16c9d9ac1`  
		Last Modified: Wed, 13 Aug 2025 13:20:15 GMT  
		Size: 6.9 KB (6891 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0bf7db85aba6a375c40b16247bef64315fe77519e9e942b2235ffeb20cc6bed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71170038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ac7ca7fc7df28e2053fe4a931f1c45cc60535f5cd9462c669bf45f59e7b8eb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:635b31fd21bf059b6af0abf57b343066d0218ebb3e0b679927cc1752427a72da`  
		Last Modified: Tue, 12 Aug 2025 20:53:37 GMT  
		Size: 47.1 MB (47149866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af75c300f83884b3a2b4352096299334113ee00d6718ab116cdad0fd28ea4064`  
		Last Modified: Wed, 13 Aug 2025 03:14:49 GMT  
		Size: 24.0 MB (24020172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:bookworm-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7d85ccf8304f5269340b4ba5cb7b6b04a5dbc6af171e27d1a1b8a28e0cd5c9f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4510581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e64c776a54e14a307d6359cfe3384bfe6fa83a4657ce0f78efb0baff9fe06c78`

```dockerfile
```

-	Layers:
	-	`sha256:c37467bac136adfc616b2ab4f0ce4159be902706600fa54a6bd03fec004b8e3c`  
		Last Modified: Wed, 13 Aug 2025 04:20:00 GMT  
		Size: 4.5 MB (4503722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6766f1d57908a056bcfe4e42fc0fef311867019ec5dd5472af9169b78cc3de21`  
		Last Modified: Wed, 13 Aug 2025 04:20:01 GMT  
		Size: 6.9 KB (6859 bytes)  
		MIME: application/vnd.in-toto+json
