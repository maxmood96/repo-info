## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:8ad99fd194945bbe4f96a36971f30347c8f3ba0d34bd5a2a5849e8980f7257e0
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

### `buildpack-deps:oldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:930fb10bb424dcd275a9a2f9a1b0f4a7122cf97d738a59da706b5c7b67579d3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136915402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d128f9193f1dc86007a71cbc963ee06ac7e81fd7b8d4617b8d90c604221a87`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:cffef7dc6f99e0837fd18f5ab2b363aff8d1c12ed377199f6d6478f80b458c05`  
		Last Modified: Tue, 12 Aug 2025 22:14:50 GMT  
		Size: 64.4 MB (64400050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:91fd21a8a59e9b8a0e85df7846cd3cae72d62a3fc78f57c6f6e2510ef8ebd1c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7966589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5834b9ad792184bae84ef33a707bdd030e8db58b44c6378787c47ab24caf4147`

```dockerfile
```

-	Layers:
	-	`sha256:0107c6cdb99dc081c7363a4834f0970d590391ae77ff2dfc86341146b4be18cc`  
		Last Modified: Wed, 13 Aug 2025 01:20:17 GMT  
		Size: 8.0 MB (7958934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc16533f2f33413a67738365d82982bfd09af7bd18334c53c0566b5d54a45eb8`  
		Last Modified: Wed, 13 Aug 2025 01:20:18 GMT  
		Size: 7.7 KB (7655 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:787b6668864deb0b7de322194c8db40365fe8cb6da38049cf679dfef1c401878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130721272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57d677b5ced510c3da2c0495e5075b6d1004cca054797746ed01f67abb141bec`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:15f842f3168ffd158b534ca355440e1a28a63cbae85f8b2422f379efca96dac9`  
		Last Modified: Wed, 13 Aug 2025 06:05:53 GMT  
		Size: 62.0 MB (61997775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1490742d51e7d7edcef10ce4df3847cbf652d2827ffd66356a762740356478cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7967903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5573ff514a955e1ebb8902b9eb3bb822fb13c00ec930eabfde0a9c801327f32b`

```dockerfile
```

-	Layers:
	-	`sha256:fba03133d630acb771c201b0403f14b812c89833ae4e8fd8a164b6e0f30ea1a7`  
		Last Modified: Wed, 13 Aug 2025 07:19:59 GMT  
		Size: 8.0 MB (7960490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6592fa15d05e85608398ca0b6ad1f809c0a0d9b176b190e978094ff54b0186b7`  
		Last Modified: Wed, 13 Aug 2025 07:20:00 GMT  
		Size: 7.4 KB (7413 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7734fc49a2ef7575d4301e19ad17cd6f1cc681022f19389c3b6cc404ab371a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125795150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c04b409363cbb47d81ee62b9e28da5ddbc762fefad5c22d57bc2d1e77c90860`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:897d6edccc28c5bb741d67021941e03742df0d455c33993ccd0aa632e1cd6d24`  
		Last Modified: Wed, 13 Aug 2025 06:46:44 GMT  
		Size: 59.7 MB (59656741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:fccd1a0899f4bdb5eb4358f9b7324760c367036608fc85809675d589cf9a3e31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7967321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54bc8946a395e170fa302dbb5b12ad7219db7f7ef89c8b2fb886525c1ab83e82`

```dockerfile
```

-	Layers:
	-	`sha256:0de620f26565e087d30a49103e2a93ea5b389a860b265a1d08511e6b01074cb8`  
		Last Modified: Wed, 13 Aug 2025 07:20:07 GMT  
		Size: 8.0 MB (7959909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dc223519275a2365cbc7c5d29839af84b58bef1619f0173dd4577732b82db52`  
		Last Modified: Wed, 13 Aug 2025 07:20:07 GMT  
		Size: 7.4 KB (7412 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a2697109243e032c4e2bba5886db3aed4fb00e14915368048eb5f6a18eae3acb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136279300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:904ad360cc9686ae4d137a98f12e4b8f6a2fbc9229b76658b492ad23736bc328`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:c4910ed05e8b3022bc1c6adfffae5e35b0d2b4c6d756ee21311b48b509147a1a`  
		Last Modified: Wed, 13 Aug 2025 16:31:39 GMT  
		Size: 64.4 MB (64367003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8dab604b40441db1d6a874005fe38244313ba2d93c2ce4d7077e9faa6dad44e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7972458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17738e4ee6ae047f8e90772e19ebbba3a0185c82d5f92f8c46ba21b71939767e`

```dockerfile
```

-	Layers:
	-	`sha256:f9a102acd23af4434c7f30ce090e8a1824beeb178650d59c7efe1a359fdd0620`  
		Last Modified: Wed, 13 Aug 2025 16:19:55 GMT  
		Size: 8.0 MB (7965025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86ba646f071e2739662d0eb748b1ca43a925c598f5fa5b9db0e859e3e7c0d74a`  
		Last Modified: Wed, 13 Aug 2025 16:19:56 GMT  
		Size: 7.4 KB (7433 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:003a7eb96e60a4a09ac69ed0a3275a597a10e60cc59cacdf8ea466359cfb0862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140565347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ea7a01957df789c63e3255c6545c26d49bfc661e51e83d8fd0ba2ec6a93794`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:7f2c25d261fc893dbf63d447e191cad0237f37f95f01960ee9b9026b75ab3a74`  
		Last Modified: Tue, 12 Aug 2025 22:14:47 GMT  
		Size: 66.2 MB (66226107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:47f29f58ce6c65fe69980420c8d6fffdf7a7653c09118cce783a57509f4bf814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7962720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b99e8f1026157b351cd210814780f68eae0362daeb7f276edb6aa221c9f7a118`

```dockerfile
```

-	Layers:
	-	`sha256:ff4c873b543e913329e18852da6a3bbdf2b44b1848fd096c2c16947723958639`  
		Last Modified: Wed, 13 Aug 2025 01:20:44 GMT  
		Size: 8.0 MB (7955093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53c7dcb2504fa5a48d3fe45b36d21d4f9344d7b2070596c7282967d59b83cf53`  
		Last Modified: Wed, 13 Aug 2025 01:20:46 GMT  
		Size: 7.6 KB (7627 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:0af539e8157ba279534e7ec40e53d946deb13bcc71bd18d618da8ebcf568ddfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.7 MB (135689031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86cbf13bd156ad443757ef41fa2e5723601c0acf3b00e39cf455cba7dcbedfa1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:1e53fb77ec58b351a832fef6343e52e81f478bfac5e6664210978fbb38a2cddf`  
		Last Modified: Wed, 13 Aug 2025 19:21:03 GMT  
		Size: 63.3 MB (63308715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ae767b3acea6b4e9df5e03f3262d18b389a0e72832b42a16f237ad22c502829b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 KB (7186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5b83a8b3a5666d11c8ce30aaf9f9b7fec343019b3bf6b7dff3ede90a810a94`

```dockerfile
```

-	Layers:
	-	`sha256:3841e43b5793ce163b6086997052c6380227d18a667a5557e1744f8e1c878c38`  
		Last Modified: Wed, 13 Aug 2025 19:20:05 GMT  
		Size: 7.2 KB (7186 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b72bba2182417f99a964bbf11d55bbb4b48f2cf2f918955c7a36a8947a363a67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.8 MB (147844082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e980f2e0e0ea9958a049fe4a14e100ffbfd14324231eeece6d7d59633ebc21ff`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:ddb09aa58684adf8f458ec24cfe46bcd658b8344a3c5c5ec70c88bbe9010b255`  
		Last Modified: Wed, 13 Aug 2025 22:43:40 GMT  
		Size: 69.8 MB (69839966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:201302114e7a81ebe245b77565e1f4799865a62503cd5b60683f7a310dfeda8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7973878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd3344f44cedea04699bf5575626cf58521d336b7a543eddfe2d113e1f69aa61`

```dockerfile
```

-	Layers:
	-	`sha256:57eb9b5adaa6a6a20a7ff447a9f921ccca850583aa272b3e3052696819624479`  
		Last Modified: Wed, 13 Aug 2025 22:20:07 GMT  
		Size: 8.0 MB (7966493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62d8a05a38fee0f63b96a5cdbb5ba559563c0dc675a394d9a9fffe7bdf65d8e2`  
		Last Modified: Wed, 13 Aug 2025 22:20:08 GMT  
		Size: 7.4 KB (7385 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:5e2c358e028db9088572818d06e8c4af5b4662cac3fe551ad5f0b89614350444
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134667807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8e846138286aa29e370eb2cf9935361974755ec4499a1053f68435bbfd98c2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:4afd6f1f2a58fa1289478b7c4157102354638b354f847958c5d7c5b4449c508e`  
		Last Modified: Wed, 13 Aug 2025 08:03:43 GMT  
		Size: 63.5 MB (63497769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b171f698ea0ba97e70a12cd9b93d1122c6a56b8f7377fe950d19c4b8a3ba8e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7962298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe7763692578eeea1a8fbc54e46d731c8b4579c84a738667d553e076c1d8c36b`

```dockerfile
```

-	Layers:
	-	`sha256:de1f742393f65cda74f04421cc90ff14e440c56fa1ba180fafa2f161bde896e9`  
		Last Modified: Wed, 13 Aug 2025 10:20:07 GMT  
		Size: 8.0 MB (7954945 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48937b347e90baef8fa42146cc2347b827e69d378d41c8f3580686ad378a85cd`  
		Last Modified: Wed, 13 Aug 2025 10:20:08 GMT  
		Size: 7.4 KB (7353 bytes)  
		MIME: application/vnd.in-toto+json
