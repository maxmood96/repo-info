## `buildpack-deps:oldoldstable-curl`

```console
$ docker pull buildpack-deps@sha256:0a5d0e22da3ff7263ad385372692d7f7c52dab1a6ffb7f4a401d7c0a2a2361b3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `buildpack-deps:oldoldstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7b678d98fbb629cbe0ad9ac2e9c780df34568bf845aa90afd8eebfd5016d8890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69520166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128ec420be937307e6c0aa63242ff41266235a1983b0363ee2614be4de807446`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:10ffc47270cd106d2d04bc7ef4749d579620e45a84804ba3b18f0898fe5ecc64`  
		Last Modified: Mon, 29 Sep 2025 23:35:07 GMT  
		Size: 53.8 MB (53756064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840feb027ec25230e94a2f7f4414d50952ed3e6c6fc69a711b34ce7938a2dcdb`  
		Last Modified: Tue, 30 Sep 2025 00:10:31 GMT  
		Size: 15.8 MB (15764102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3e1022e3563a4b0c68bbcf1edc99eb5ef8bb8e634936eaddcb0ee027a148f67b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4635904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532daf395e899993a2f060e2487e18dd384d1930d68185aebc2915171e02e665`

```dockerfile
```

-	Layers:
	-	`sha256:cb59c3074a8629d4125ce5f2a3cd89bfaf9f69b47ad00a8e7e7f1bd3a679fc74`  
		Last Modified: Tue, 30 Sep 2025 01:19:39 GMT  
		Size: 4.6 MB (4629099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a4ba646b4bb6d6f19dc0a6b26320b9ffddfc7115e5a4a427ef1a7ca4cdceed2`  
		Last Modified: Tue, 30 Sep 2025 01:19:40 GMT  
		Size: 6.8 KB (6805 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:77c39dcef80f2805d988803c7c3d76fa47d8bd79143a7b3c1033e70b0a71a77c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63925071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be94c8cf012cf3a804ee22f87243b200b3449d91a722740bdba7a432a47f1f21`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1757289600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8274f5d2891e4b4a199e88ea54bf64be2b431cff01268ebaebfacd12519d655d`  
		Last Modified: Mon, 08 Sep 2025 21:14:50 GMT  
		Size: 49.0 MB (49044356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf7f7d1af869adfa648959578fb79545e78d3ad3763e029dfc7f93e144fcbcf1`  
		Last Modified: Tue, 09 Sep 2025 00:01:03 GMT  
		Size: 14.9 MB (14880715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bd19e63e5f27bb754bc71cf6983d4ab526d0eeda369273e9452bf07d86d26089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4637606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bab03517e3c9220f05865574d2130422d3895b42ef61c4935e7955b4524f8e5`

```dockerfile
```

-	Layers:
	-	`sha256:ac95d559ff3f76294841a7dcf23cf880de8cc5f9d9894464691ad61f49f51ede`  
		Last Modified: Mon, 08 Sep 2025 22:20:02 GMT  
		Size: 4.6 MB (4630735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cd3da0e00a3867abb305465cb206471fb4d2c757eca6e25e9f6454b454b1db7`  
		Last Modified: Mon, 08 Sep 2025 22:20:03 GMT  
		Size: 6.9 KB (6871 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ed491156ffbe60030a4beb69cf727e930675684facd11046f5ac904893b95515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68006717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86df154d4f2fd8129b30fbefa73378d9c08a7d7adab97324e8d13704274a31e1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1759104000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:9b16ae1bbd1ada84c12528379a10e280bd89e0d0332670c8487145eb77fe2fe1`  
		Last Modified: Mon, 29 Sep 2025 23:34:42 GMT  
		Size: 52.3 MB (52257414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed44f1c4305e990c6301b16db5ccb0849b5044d4eab021969a1274b1471f5cdc`  
		Last Modified: Tue, 30 Sep 2025 00:13:37 GMT  
		Size: 15.7 MB (15749303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:98ddff52d041619ece1056a79bfc06af4648a20e6150a07d7056fdbe05a9c4f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4635598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb184f97629d9b63ce524967e12cbf7ea5b59af2bdb0316b8bc34eeb322c0491`

```dockerfile
```

-	Layers:
	-	`sha256:901f13dbb6020a891d24e47b539f801015ca10597f59196033c98e8b2b1203f9`  
		Last Modified: Tue, 30 Sep 2025 11:46:49 GMT  
		Size: 4.6 MB (4628713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10f24236686d11e79ca1892ccffdf71280429301ecb4b265a4d2fb1098fae490`  
		Last Modified: Tue, 30 Sep 2025 11:46:49 GMT  
		Size: 6.9 KB (6885 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:aa3e40d6be03b4c4eaa260146044dbc519ba03f594e390e0298cf654aab08797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70967014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:903d1a8f87031b267cb967bd337467bf9676851d772f3c24f81077ceeffa5424`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1759104000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ceabdec1cb201cbc144cbbf99606ecccc3942e0acc3ede261d7cced4e3f632e8`  
		Last Modified: Mon, 29 Sep 2025 23:35:34 GMT  
		Size: 54.7 MB (54699245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f70b590df86e9bb29cea47ff5206076a14d6ec7a2d599a47314d5c807427f8`  
		Last Modified: Tue, 30 Sep 2025 00:20:26 GMT  
		Size: 16.3 MB (16267769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7b4f11cbf273df19afdbcef44e05851a0606c9309380241b197d8a335c0f1c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4632387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cc2a01cb2d1b3c527cfab0807b80f6d8b716c7e0e8034e952ecf1b27b1907ed`

```dockerfile
```

-	Layers:
	-	`sha256:ca73cab629d6b685d0081433ac546934be11d55c4e6266e34f028f637f710ee4`  
		Last Modified: Tue, 30 Sep 2025 16:36:26 GMT  
		Size: 4.6 MB (4625602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e6c90c0940171ca65bbff023e6a6c5d1846330d4b5b8c9003ccfd9a157622ba`  
		Last Modified: Tue, 30 Sep 2025 16:36:27 GMT  
		Size: 6.8 KB (6785 bytes)  
		MIME: application/vnd.in-toto+json
