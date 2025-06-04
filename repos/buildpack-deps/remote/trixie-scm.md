## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:c97e4a56dba8d92c86903f6f6f6f68ad0fe0e6bec55b057dcddd89297da06466
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:trixie-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:670a28b8329310e9fd829dab5223994c40e13f804b443f730f6c37f47d789c74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142468232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d88fd5d5b7024179fd9f747d7c12f444305ae9f8790bb51ddd920ff09609fe54`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b8364400c35b20e530ea76455b7a73bf615b17d9d6734e0c2539034d9fe0bed1`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 49.2 MB (49246908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073c3e094f775042a2296ed99ca159904c7ae19127cddd6dc0e02dfeff3ac66b`  
		Last Modified: Tue, 03 Jun 2025 13:35:19 GMT  
		Size: 25.6 MB (25583751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796d3fae0f8d1c689d461da616de1a85e5ade1f7c61c5496c0c3b6b1bf6e722d`  
		Last Modified: Tue, 03 Jun 2025 14:37:41 GMT  
		Size: 67.6 MB (67637573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ce214589e4104395181191462ac402a858d4e55b14b9d817bdb804f776b37110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7594204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1db18e1c4a4d5f9ae2f8a3c97aaacd9934b6d1b7d1b4bccd928d032e8cf9eeb`

```dockerfile
```

-	Layers:
	-	`sha256:f3216e58376bb04d7525e8e72d81fb486c2feae50c32228bb430a2d336bbef84`  
		Last Modified: Wed, 21 May 2025 23:38:02 GMT  
		Size: 7.6 MB (7586890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f25ff982fd40201daa5df5eab85594ffb798c910d383e5bbee522a229b5d0394`  
		Last Modified: Wed, 21 May 2025 23:38:01 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ed84fabefed004107ba272c0eb97384651c4050c9e0ce968cd3fb01bb97b01df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137120533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63edf384d86f178198d312ae1a903bd2d8da7351396d93bc2d541e5334a792d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1747699200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9616f5c2624aa57711d4d3a917ef21ea33c33b9e29ed21732abc6456aa133801`  
		Last Modified: Tue, 03 Jun 2025 21:52:52 GMT  
		Size: 47.4 MB (47438143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fced245b3861daa32a8eb96fca42f40c6b8763a3cff659d7638f85cead39fe0`  
		Last Modified: Thu, 22 May 2025 01:15:18 GMT  
		Size: 24.3 MB (24327560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bbae712d6151507af038108c551389130a66d8e4e0824e97fb8a78ba564685d`  
		Last Modified: Thu, 22 May 2025 04:46:33 GMT  
		Size: 65.4 MB (65354830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:68ef67ae0e34bbe6e43646dc71db40edb2c9781b163200c79bbc40060dfeffea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7601666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893a61a92038230444fd0011d60617821b4658775e31134ca3132feaa23a0eb2`

```dockerfile
```

-	Layers:
	-	`sha256:2b9f0516d1906950bb5d8325ddffb8f17f7e57936a946b62fefb2689bae6a4c6`  
		Last Modified: Thu, 22 May 2025 04:46:31 GMT  
		Size: 7.6 MB (7594292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47d153f558a774e4a187b5125b076d95d732549c1c30e51d5eafc3d8e7c700c8`  
		Last Modified: Thu, 22 May 2025 04:46:30 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6b3f3e837fb124193924f0574f802504ead35757d2b360a2bf227c4a67de693d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132045775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce73a1119fe69f4863e0025f2b3fa6493d972774362864b0a5b643e19547bcc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1747699200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d82ad715078dca1bd38ac71d3c9c872661d1bdfae377c84300033db7bf3581fc`  
		Last Modified: Wed, 04 Jun 2025 00:32:15 GMT  
		Size: 45.7 MB (45690818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e80b8be2756aeb2756ee1709c45d1af8640bfca2b89a56244b22bcddaa053da`  
		Last Modified: Thu, 22 May 2025 02:30:07 GMT  
		Size: 23.6 MB (23592590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef402b2ae65b191fb52b33f040b2eef1a8184aee8984cf58e6acc607be371f5`  
		Last Modified: Thu, 22 May 2025 12:14:20 GMT  
		Size: 62.8 MB (62762367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5269d54d7e76d71b950b27e83bb8d519ff63e3bdcf2532f02de803bb72140d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7594762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e61b3143fb0210dc9642803dcbf58aa46dc325f4eafacf3a7c8494d218ed573f`

```dockerfile
```

-	Layers:
	-	`sha256:cf472439cba1e8378208727f0a358242a8ddf34544df2999268b7da5ebc17762`  
		Last Modified: Thu, 22 May 2025 12:14:18 GMT  
		Size: 7.6 MB (7587389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5918f227f505d8d1c3e0323451ae3c845ac6ff45bd3ccc0b4d4dcc0de63def8f`  
		Last Modified: Thu, 22 May 2025 12:14:18 GMT  
		Size: 7.4 KB (7373 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8dd1024cc47eef54ac579868c259f3518685ec01ab1e317226f232c50e6104ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142205347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03d6e7714e16bd3c20d657422f994bf4e3fed8b8ec97fe983b2256b6d2ccdeae`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:397826b9fe635f12caff1a603eb12c37426a5b3dc563e0adff2debff0c68a6b0`  
		Last Modified: Tue, 03 Jun 2025 13:47:15 GMT  
		Size: 49.6 MB (49618294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b925a0b1aba64c2f9934b5b752199fa927f08300fc82c456fa922c4303a06f43`  
		Last Modified: Thu, 22 May 2025 02:48:53 GMT  
		Size: 25.0 MB (24981840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:546584c670303be4513862213cb042edd5a8f7eec9db9d6e8c5844665b49b26c`  
		Last Modified: Thu, 22 May 2025 09:20:02 GMT  
		Size: 67.6 MB (67605213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3f223d162ebb94f86f5848b0fe365e0cafa62dfcc3a5e71ab2739dd9b62826fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7601947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5842487f069198920e41af681bf71c422040e5a222c47e842a45ce7d920bf36b`

```dockerfile
```

-	Layers:
	-	`sha256:9e9128aa631899ce2b9f9480548c02ed22fd3dbe9863b0db9d0ea89be4c65e76`  
		Last Modified: Thu, 22 May 2025 09:20:01 GMT  
		Size: 7.6 MB (7594553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83e8ba31965af0a63045d7b26c75726057bad6ec1fb9ac52dd17673091c2a48d`  
		Last Modified: Thu, 22 May 2025 09:20:00 GMT  
		Size: 7.4 KB (7394 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:16b1dbfbf6c19fd740e70f0ea7535a207aec0321f5446324212cb04e5d125dcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.2 MB (147162908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e83ebf2260c33cf24108549f959103aa24ac4e6dddfdc7a78271459d13a1a728`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1747699200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7e1acd19dab9f7ab62b7570b85e71035e78cd9d9b9bff975df4b0a635578c7be`  
		Last Modified: Tue, 03 Jun 2025 14:04:15 GMT  
		Size: 50.8 MB (50761280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24ada90c6b3f67e8ac11f8d9700e1fbeb5f64ed848c2ef5d89e89c3d1161d7e`  
		Last Modified: Wed, 21 May 2025 23:19:58 GMT  
		Size: 26.7 MB (26745816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53475a03e00d0d9a396cb70f6edb89c6daaba7c95e28d935ced8a0100b7b7bc9`  
		Last Modified: Wed, 21 May 2025 23:38:03 GMT  
		Size: 69.7 MB (69655812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:76844c192aa756d088a0cd28f75f2d23ade712e7d3b55328bc3131eb02ca6c7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7590328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc7c36ac2ca91fe322dcb854ffd3bb88aff53fe7a214160b0f1ff95293d4729`

```dockerfile
```

-	Layers:
	-	`sha256:4c597acadfbdb2dfe8551ef142270217aeb0e7b6d98007f7887f04b716a73466`  
		Last Modified: Wed, 21 May 2025 23:38:01 GMT  
		Size: 7.6 MB (7583036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66a4a31c6d01a15764486d38d9951059a091be429e5e4e420beb11aa0f7b715f`  
		Last Modified: Wed, 21 May 2025 23:38:00 GMT  
		Size: 7.3 KB (7292 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f21e454c4869aae765909116507b11de1d26e3af9324b63c30287f80051a1a8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153091394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596f1904bd5a50f5c6231597287165266a9dda4d5220710c35a45d71c19aa4b9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:25dfffa4126a91eb76c700c90bfdc9a9e15f34c7438a81f16c8a6999bbde6e45`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 53.1 MB (53080544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e139263efe3c22e2cdab37e8ebc2c1a1759b3b3d0c9c98b6becc0fbbd0bcf2`  
		Last Modified: Thu, 22 May 2025 07:33:02 GMT  
		Size: 27.0 MB (26965977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bb27d293c54626589e1325f716f65d323eba25d860b81956ce153386de17da`  
		Last Modified: Thu, 22 May 2025 12:42:41 GMT  
		Size: 73.0 MB (73044873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:53248fb118091869c6fefa98a638a86e2d2df26fc74c387600fe9517aa11b688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7607713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a77e9665f2bad023a0d2076fe010491986544c5f4230bbc39ce90008e2c65337`

```dockerfile
```

-	Layers:
	-	`sha256:3c6837f8706b85b19ec9cd8cf507c16a52b2d2eabd00167d4639089b765de78c`  
		Last Modified: Thu, 22 May 2025 12:42:39 GMT  
		Size: 7.6 MB (7600367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5ec6b3fadab1bf7780f7d83bd88a6413a56011c06dedcaeb41aaafbc6e387be`  
		Last Modified: Thu, 22 May 2025 12:42:39 GMT  
		Size: 7.3 KB (7346 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:54ba23fa8a5ffcb880b7753b6c1d7ec174d532a6e501bcb1772fc7c88d77af7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.3 MB (139252299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bca75d8af1799275f25d0e3c784397cc27370ca737823e538edc5b8f9e71c4ff`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1747699200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c83c5fa20952cc8610d790073e97537e7832127593042fa9c620fa910fe6f6b9`  
		Last Modified: Tue, 03 Jun 2025 15:26:09 GMT  
		Size: 47.7 MB (47731411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bd8670e232ca11355ffc7ddcb280e00c712f98c6d6ef1c601d041012816cfa`  
		Last Modified: Wed, 21 May 2025 23:26:24 GMT  
		Size: 24.9 MB (24917594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eab19773c2912f0a6e7295e8a9ea585980b042ba4f201575fb17ac1763bdae3`  
		Last Modified: Thu, 22 May 2025 01:15:24 GMT  
		Size: 66.6 MB (66603294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ee1c7757c6ed3dd2a6b693495f2fab7160131ce3c05646e915edb74279a9be7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7584054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfee7396a41fdd371b836ddd8a76222594ddae42f6f5820cd3dd7826b152e069`

```dockerfile
```

-	Layers:
	-	`sha256:90546302bb34affa8b1705430c3f7ee5ecb61eef8167d46ee935d988d7d17a5b`  
		Last Modified: Thu, 22 May 2025 01:15:16 GMT  
		Size: 7.6 MB (7576708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddf209c649f27166d4bbc5c5e0d3ceba15670abd3a620960fac1f9eb2f04bd9a`  
		Last Modified: Thu, 22 May 2025 01:15:14 GMT  
		Size: 7.3 KB (7346 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8e1a4c5838977966cca4ea11c795b958fb5245a8f566d0928f86703314179ba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144733717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae65eeedfc206519c2b9760013617a2c6a20feab2c38b96cfec287e256bc5e5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:71c8524b25c34592c256fbae9045d0ade48f5e9889d37c5b2190092fa9017d48`  
		Last Modified: Tue, 03 Jun 2025 15:34:07 GMT  
		Size: 49.3 MB (49322227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8645228c4b06e89bef4ee7caae64a6417dc0f102985c8d7902876a160465531e`  
		Last Modified: Thu, 22 May 2025 01:03:11 GMT  
		Size: 26.8 MB (26757774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925cb7f6baca00c5ff3348d92eef6b2e3dd349323f30f9ed50efa944600d250f`  
		Last Modified: Thu, 22 May 2025 04:39:04 GMT  
		Size: 68.7 MB (68653716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7ef2b356702c816f257042da89ffd94838eaead425bd7624474ad67396d5d967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7601489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d2c669188f6cc18613fabdc7566ad28eb8c33e7a257d6bce9fdd72d96d70dd6`

```dockerfile
```

-	Layers:
	-	`sha256:f11a269a6b5fd2d82ed40550b59ec274b79c64e92a5a38682c2e53629c2de5c6`  
		Last Modified: Thu, 22 May 2025 04:39:03 GMT  
		Size: 7.6 MB (7594175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4358fd0e3b3165d6d47a8e030d3798876bbd339920a917b9607933f7d14bf7ce`  
		Last Modified: Thu, 22 May 2025 04:39:02 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json
