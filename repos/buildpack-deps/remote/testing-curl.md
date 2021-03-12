## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:62fd55225d32a87156bc6445e06d657b0961186bce30343911d741386d0b6ed8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:testing-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:c6b95c52a994439111d0afa2cddbbbd303fbe3e5be2b97dcc477254f4370e3c5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70832808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f8ba2808da8d64523b144337a787ca964f02f15a6021842c85379907140977a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:04 GMT
ADD file:a858c472d72a55a1ed0b7b2fd2751bac78f77e3549a7533c508022aef7204233 in / 
# Fri, 12 Mar 2021 02:20:04 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:47:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:48:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:da21a291c553cde4f403910fa28fb69cad95f63ce1b378f341eb17738b45a6ac`  
		Last Modified: Fri, 12 Mar 2021 02:24:58 GMT  
		Size: 54.8 MB (54835833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f47dd55341835080544d848892987ce23838db35fe64a0d4338b1494ad6ed1c`  
		Last Modified: Fri, 12 Mar 2021 03:17:40 GMT  
		Size: 5.1 MB (5136253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb0644d825d57df2b92d247999a507695a22522c5fa2bd93de229b003ea515b`  
		Last Modified: Fri, 12 Mar 2021 03:17:40 GMT  
		Size: 10.9 MB (10860722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:4094803903fe643a53ef2a72ca89fb0d49568f0254a29ac602a4e13cc271d1a3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (67975440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99847c725764dc1f435c259fa75ccece571599bbe865cd866b9a96ce4dade87`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 01:50:53 GMT
ADD file:d9f9819ac30357029b6474afab9445de462a9c668b49ba4344b2dbaa06df05b2 in / 
# Fri, 12 Mar 2021 01:50:56 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 03:58:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 03:58:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:db47e66a99eee0f0e80fcffdc694f78f48d3211131714143c70983039b44d399`  
		Last Modified: Fri, 12 Mar 2021 02:00:49 GMT  
		Size: 52.4 MB (52366010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ac7c932658262e92ab79badf2b13a9b1cad33b3b58f4142dc86238a03e83da`  
		Last Modified: Fri, 12 Mar 2021 04:16:10 GMT  
		Size: 5.0 MB (5046243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ad2f690c9f36ebf3bd0ddfbb5d3f86e49179efda4e4860ba41f9c421155d95`  
		Last Modified: Fri, 12 Mar 2021 04:16:11 GMT  
		Size: 10.6 MB (10563187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6d5ff37aa0ff0ab7e709a89c34337232da7f1226945767c6eb79173b940b6a25
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65149659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:579955c47fa7c584af085cd39ceb604553c36e14b239312e9e733c069c5b52c4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 01:58:33 GMT
ADD file:af7fbd0fe0efe7b818f1484ffecc74c401c4d5b949e8e054570ea8cc7a7ed73b in / 
# Fri, 12 Mar 2021 01:58:40 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 03:27:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 03:28:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2e093244fe0614201f8731e47ce0387edd785d9fbbe8924f2c8e435a7afabe60`  
		Last Modified: Fri, 12 Mar 2021 02:09:18 GMT  
		Size: 50.0 MB (50033302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66de6d835f521bb9c85648b5a81b3279e777ef73195f17383766d6b48701c5f`  
		Last Modified: Fri, 12 Mar 2021 03:45:35 GMT  
		Size: 4.9 MB (4905657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e0b8fc9d72ae8c961878dc03047f7edad8e5025511797effcbca240ae292ee`  
		Last Modified: Fri, 12 Mar 2021 03:45:36 GMT  
		Size: 10.2 MB (10210700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:0545668137471868fb0c84a832e95bca9df08265eabeeff04ded48f46490925c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69507023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb18a84f643d415851e8619e56a55a2040dbf7c54e4c1a6c204b89fd652c3fb`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 01:52:22 GMT
ADD file:0b6f3c6d396337f2754d539814c02240e0a459436f4c0992dabf1736069b5a51 in / 
# Fri, 12 Mar 2021 01:52:29 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:26:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:6c214bbe001dfa953738440417693c3487f97b371a108bdd62425a704347faf8`  
		Last Modified: Fri, 12 Mar 2021 02:00:33 GMT  
		Size: 53.5 MB (53521132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1332f0d3a2e68785b75d30a2f0eeb7e0902ecf1068899b78d4a7e90f5201cf7f`  
		Last Modified: Fri, 12 Mar 2021 02:42:02 GMT  
		Size: 5.1 MB (5125702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70aaac2a7c6ebfc86100e530f2607998a0f8d84b4305495031bbfe789e6e1c2d`  
		Last Modified: Fri, 12 Mar 2021 02:42:03 GMT  
		Size: 10.9 MB (10860189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a8c053be7bbb884c13e2b3db745de4ae7bcddc0f89fa8ef34c7606818aad0585
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72353570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659d90036d8204d9a77c101873c69203cb786fd6bf51b5d3431414f0aefa30bd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 01:43:42 GMT
ADD file:bed5cd029b8a9960b76ca6cc40996e558168731aa38831163dfabe7bda8182fe in / 
# Fri, 12 Mar 2021 01:43:42 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:14:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:14:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:0a9f57a86f966b0edd22e1658988495d14ac0adce930bd6b34f3b6d87ff6e270`  
		Last Modified: Fri, 12 Mar 2021 01:50:43 GMT  
		Size: 55.8 MB (55847447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c33e90bcc52eaf7fb93fd28bda768ee89e08c8939b9086f76ba8159568845e3`  
		Last Modified: Fri, 12 Mar 2021 02:34:41 GMT  
		Size: 5.3 MB (5265242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e489d2f5630e3afaad47643cb9f061ff6441e8510705f706d05e12959d9d8e3a`  
		Last Modified: Fri, 12 Mar 2021 02:34:43 GMT  
		Size: 11.2 MB (11240881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:7f28618edb0542cb980d179efaa7245beab16aaf3547d1453a674efce9e679b4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69054344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f1c8b3c6b37a3f1237604d7a698873ecd1ccb44acc12f6dc791e4ee2ff206f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 02:08:41 GMT
ADD file:1d48f0f2d8c8cb792d2bbc40d674fcf7f9cd253be061964acd9899304360add2 in / 
# Fri, 12 Mar 2021 02:08:42 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 03:04:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 03:04:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:8a576eefe77178505a1242265c25ca38b94b29862aa56a6bf88c698de0ddc31d`  
		Last Modified: Fri, 12 Mar 2021 02:15:03 GMT  
		Size: 53.1 MB (53092083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed4895ee6979d25051187e6c8df7cfcd88bbb3c681b7ce775eb8d68b07962bb`  
		Last Modified: Fri, 12 Mar 2021 03:17:11 GMT  
		Size: 5.1 MB (5098054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6dd67088240632fdbd07e5c60a4b7a579388d081a123d8fb5f7522b43d632cc`  
		Last Modified: Fri, 12 Mar 2021 03:17:14 GMT  
		Size: 10.9 MB (10864207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:802e7bcc0b86cdbb1d8a0d52edc2f7fe5f44b557fe25e4b6681a7b3965bb743d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75746804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93c63a5200cc7a276a42935d24d64b28b96280430d98a70f3fa9832ea70dac2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 02:30:35 GMT
ADD file:73289d3f358472059064c70edf2135f994f4e4a8ab92fcc0434c1fd611d61e36 in / 
# Fri, 12 Mar 2021 02:30:47 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 10:37:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 10:38:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:eab69212baf77adfba26ada26d0c2b425ac1dd30c3a5bf296485f437993872a2`  
		Last Modified: Fri, 12 Mar 2021 02:40:30 GMT  
		Size: 58.7 MB (58746419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db317d5fedb325c195599b5ae894eac6653f54840383838d929f8320084888f9`  
		Last Modified: Fri, 12 Mar 2021 11:54:21 GMT  
		Size: 5.4 MB (5386575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363f493170adbe10fa914f328698104fa7a698cd4fb5fa4ffe9b3d2f8901354a`  
		Last Modified: Fri, 12 Mar 2021 11:54:28 GMT  
		Size: 11.6 MB (11613810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cf5bcb88198d0298f5183bf6b031ee5646d985003950dfd10bb9867cb528f183
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68984875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aab9fa52671f39df1a4f5169ea0c75bf1e079add23f4933604761bd95c6779b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 01:45:06 GMT
ADD file:cb5b3f6c2f66ddb51311634b097823751f759ee3270d06de8388ce763fe1087b in / 
# Fri, 12 Mar 2021 01:45:09 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 02:28:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 02:28:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:a4cdb5376551135d812bdd513cc33a080cf675d45fd21d8c58d993497afb1e87`  
		Last Modified: Fri, 12 Mar 2021 01:49:44 GMT  
		Size: 53.1 MB (53110995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2d00c7fd437d5508e95a96dd508b356303e256508643d5d6fee7c1e90b2aee`  
		Last Modified: Fri, 12 Mar 2021 02:38:37 GMT  
		Size: 5.1 MB (5121380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8325387d172e529e98282cbf5484e36eb26e81012e7894300cc43b35dee4780b`  
		Last Modified: Fri, 12 Mar 2021 02:38:37 GMT  
		Size: 10.8 MB (10752500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
