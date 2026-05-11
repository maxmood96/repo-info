## `buildpack-deps:forky-curl`

```console
$ docker pull buildpack-deps@sha256:38ac087e654241e4a813f0b4243cca90d6d464f05a71c2f5d0bb4c7b27920192
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
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

### `buildpack-deps:forky-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:03d022d64dc88520274253ff5cbdbc93042745e76d4ba2e5b61045087b160172
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75553149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49305385bc7b08cfb7744bc9893a2099ad6feb1e54598ed5eed02d4d0c677fcd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:40:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0e929ba940bb6645aaebb3cf3e1b30d0ccaa2f7d53cb82e57d451efa023dead7`  
		Last Modified: Fri, 08 May 2026 18:23:00 GMT  
		Size: 48.6 MB (48622043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cfd9ff4ed5fe9d40159f9f23c065d56cc6738732b6aa6aa03dbabd14807df17`  
		Last Modified: Fri, 08 May 2026 19:40:58 GMT  
		Size: 26.9 MB (26931106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e8a19882e30ab3e4002c5c2f13c0bc0e26e4434b0b966c318c69dadb641588a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4082570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6600b59eea2dfec815d4d3de91dbbbc3f1768cd3f3bb7fce2efd9680a5d5fd70`

```dockerfile
```

-	Layers:
	-	`sha256:8e2b75c968482eef2dc1667411d1c28a05f4cbdc2a06d60ad1a49669cb552cf3`  
		Last Modified: Fri, 08 May 2026 19:40:57 GMT  
		Size: 4.1 MB (4075797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f34ded3715f72c30ffcfb9e262c444fa44d1d41603166b3c34f5dcc7906f61e0`  
		Last Modified: Fri, 08 May 2026 19:40:56 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3f3d2b13d08710ea9a747d9fccb82e0960f17f25ba56b6db8a1c38a651d63dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70187536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46a60deccdd338b483a5891c25726392d3d8ea093640fd53e140b7936b533852`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:44:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1d504d75b0bac1a71363cc538d085e2c22d8b451c5112cd1892dea705c788f73`  
		Last Modified: Fri, 08 May 2026 18:37:09 GMT  
		Size: 45.6 MB (45559652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa9e557f096b0076a9b942cb90588ca852b5e2621c1b8f7db68c5da56f1d563`  
		Last Modified: Fri, 08 May 2026 19:44:57 GMT  
		Size: 24.6 MB (24627884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d163080e69257dfb3e472825fc49028c676974d19c73665c66430bb9e384d5a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4084124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77121cd152d4ee50c4b234bf7bd3b2deab79da8fce4254cec18696a1271e751b`

```dockerfile
```

-	Layers:
	-	`sha256:b567e4927442f38b660a29449f7fa8c1c01af5b251266300979e50e0d9cb306a`  
		Last Modified: Fri, 08 May 2026 19:44:56 GMT  
		Size: 4.1 MB (4077287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d818569fa3a09a86ceb3923b5bf935b577c51f361a028ea499e9bcc2796a2c1`  
		Last Modified: Fri, 08 May 2026 19:44:56 GMT  
		Size: 6.8 KB (6837 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e058c22ce8cf26f7d2ecd2a316bbecbaab3dd2d8e83f933b9c89368e2b6eab70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74875718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c2e8d32669192f76833cb783825c0218c4e02f163183072c0af521f1649d5e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:42:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c3ba40fb7e0c033b95f4145478256aa8b70beaf3f8b8ad41dc909fdebc63a611`  
		Last Modified: Fri, 08 May 2026 18:25:22 GMT  
		Size: 48.7 MB (48659751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1cc0aceec664d055c261d350fe983921369e3615a68574b4c33a17a625489`  
		Last Modified: Fri, 08 May 2026 19:42:46 GMT  
		Size: 26.2 MB (26215967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:56e0462a20e3f13ae986445b0d8717d76d988b4ec9c7a3f02ec12c1b89e50ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4088653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d86c319eb5b12986d1e14d503be8da0d4b7e21c87897114857bfc6817a942c27`

```dockerfile
```

-	Layers:
	-	`sha256:217e4e82ffad45e0898aa2544c4e7ea322ad722c24c0ecb451ad5dfacfffb783`  
		Last Modified: Fri, 08 May 2026 19:42:45 GMT  
		Size: 4.1 MB (4081800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e31e4e5d7c57987bd97c87f4d92bed3d907d26e2d3856bd740b8ee0e50871c02`  
		Last Modified: Fri, 08 May 2026 19:42:44 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d9f46a714174216fcfe035095dea5f2a62f30f8712b7f5af3d8424cd6b09c867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78171556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96d1fa0dacf63a35bb66f34367078ec23d03b22f1085c248434a1440413d8c1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 19:43:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fe128ab7d9fa2ef88e1a5446e3be7ae6051e047d4c17dfb5871acbb83fbcb043`  
		Last Modified: Fri, 08 May 2026 18:31:14 GMT  
		Size: 49.9 MB (49924221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce975e5bc9e5b821fdbe31dcc55ec740aee98d254347a49a09e2157accffc9e`  
		Last Modified: Fri, 08 May 2026 19:44:04 GMT  
		Size: 28.2 MB (28247335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9d15cc3707fdbef2ee0a1b3c523fce7047086418299b393eb1c4a5b6a6c0bf8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4079648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cd5d62462cf456f8c244304332a86a3c014fc1a78f5048a8e0a45d065a78a15`

```dockerfile
```

-	Layers:
	-	`sha256:a29565d5e7e4d10013d78ffb45a4af269e78f3257522ee8f358ae24a9a70d4d3`  
		Last Modified: Fri, 08 May 2026 19:44:03 GMT  
		Size: 4.1 MB (4072898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:017ff43b39a6d26bf32b1a57f97dc98d5e0484c4ba75791a4e2a2f245a9ee802`  
		Last Modified: Fri, 08 May 2026 19:44:03 GMT  
		Size: 6.8 KB (6750 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:21adac4cc673459817beca6a53bd9804d6a136d31417ecf3698cecb262d0047b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83195951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722992e8040a69587e746a68a7d431104e6f955f385bcc22844f4f99934c69e6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 22:31:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b0beeba61b823ca3e14a339f1111ae37331fca42dd43aff18c04950bc3c9921a`  
		Last Modified: Fri, 08 May 2026 19:44:35 GMT  
		Size: 53.9 MB (53926974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143f3b32fb543eab144095fd22346cb5e6a9d20cf9a632717c0a11d280547f7a`  
		Last Modified: Fri, 08 May 2026 22:31:29 GMT  
		Size: 29.3 MB (29268977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bdaebdbfed0c7e09986cccecdbbc2dfea879b88a734ce8a1f6ed9ab2f8afcd0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4086469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68f01eb7c9e1f52f09a8eff04c1162d4f68e72f62385389ee820c3f0caac53e1`

```dockerfile
```

-	Layers:
	-	`sha256:a9ee8b9ab2062d5d50aa6f9be73866e93eebcab20354ffff92f64bf945d65469`  
		Last Modified: Fri, 08 May 2026 22:31:29 GMT  
		Size: 4.1 MB (4079664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:349697923af1c1d059000bbffe33728a6d9db72ea3cfb663255b51750c45e971`  
		Last Modified: Fri, 08 May 2026 22:31:28 GMT  
		Size: 6.8 KB (6805 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:d510b9eb3192dc6068d9a9002f77def7a533c5e1a591bf33ec00bc09fd8cbec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73265369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3632ea85d3e167d35118a0e8fe166f4b663f587a88867803a25b55d10906f6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1777939200'
# Mon, 11 May 2026 00:48:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f7ac0cf25d901b0f78c05ace03b84988d685b5007a5c2ecdb859ecb56d3b46f4`  
		Last Modified: Fri, 08 May 2026 20:22:22 GMT  
		Size: 46.8 MB (46773178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3f17a612f2a3435e0c1ae9abad061b774e7306b25478218d81e34d30f64a36`  
		Last Modified: Mon, 11 May 2026 00:50:05 GMT  
		Size: 26.5 MB (26492191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bd7d213d9b4ae1621184f5e395720630e2685f3e5f86bc3e20cb2c6333d9d0c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4074312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2343ddcc5af2d73916c580fc8b2a2d63f0518b51441916c663de56b9478447`

```dockerfile
```

-	Layers:
	-	`sha256:6b99e8e7867e2f82e67b1a517d17e69c78dc89b341bc5770bc7cd37be49016d7`  
		Last Modified: Mon, 11 May 2026 00:50:01 GMT  
		Size: 4.1 MB (4067507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:116b56ab32ad173cec8ea464a0c6ce321e0f337eef260add62b42b82c1cf1c85`  
		Last Modified: Mon, 11 May 2026 00:50:00 GMT  
		Size: 6.8 KB (6805 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:forky-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:771d25e411d3a9361499b85e7c2baa34b01bfe0d512d614829391cbb843c6870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75091159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce590c4fb083277271b9591aeed5f3402a4910ad1e9b3b899becda7dcc88d378`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1777939200'
# Fri, 08 May 2026 20:53:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ba3092798c7b7e427c9591ec4f0d9efaf8a9b59416038e46d07c57fb149b38ce`  
		Last Modified: Fri, 08 May 2026 18:27:50 GMT  
		Size: 48.4 MB (48373532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea40167dce774b75145b31dc946ba69ba4700a809db349b4a3bb2a9ef77497a1`  
		Last Modified: Fri, 08 May 2026 20:53:38 GMT  
		Size: 26.7 MB (26717627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:forky-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3868bffc5d49e40f45d19f3f63aa69ce9303d16e5e0bf9afcae39714132a12fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4083981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a2d97f85289ef42a434e3bba49557e6d8ea3a57cd6bdce55cc430228e545021`

```dockerfile
```

-	Layers:
	-	`sha256:358d466105b1ad81dfd1b3e93e269b5a0e902cd5b57855ee636d0274fc7f0510`  
		Last Modified: Fri, 08 May 2026 20:53:36 GMT  
		Size: 4.1 MB (4077208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bdf7ccc20669ade78ce6e704e763b719962a540ef82f6a9f79300641bbd8e64`  
		Last Modified: Fri, 08 May 2026 20:53:36 GMT  
		Size: 6.8 KB (6773 bytes)  
		MIME: application/vnd.in-toto+json
