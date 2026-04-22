## `buildpack-deps:oldoldstable-scm`

```console
$ docker pull buildpack-deps@sha256:dbe4d009a5f603c365b58f1bff38d28aab9736a6b133cdf6cc22bcab2782a5df
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

### `buildpack-deps:oldoldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:6209278320d85cbe60b8a2364c6a7771265ff64e1604eef732f60f44bb56fb74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124314560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21108fc2295eba7dfdf9e3e81c96b2455f5b22ef18615e4b95b4e805664e398`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 05:00:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:12:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:54a03544060169d4b3f081ec8b02433016510da63c54baa3c2da97d8d0f1e9cc`  
		Last Modified: Wed, 22 Apr 2026 00:16:31 GMT  
		Size: 53.8 MB (53763152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1210b2030df8684a29d3d6bdd62a8d151c73a23016c72c44011c839c8d24c516`  
		Last Modified: Wed, 22 Apr 2026 05:01:06 GMT  
		Size: 15.8 MB (15790675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ff843d7c842f57820ba127a5b3e0c2594fa7af32413d9bed6b12e4f5d03214`  
		Last Modified: Wed, 22 Apr 2026 05:12:17 GMT  
		Size: 54.8 MB (54760733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:da4e72682116c4a5c93ac12733f9f8ef6cc103755e1df697698e65a4b1632364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7928693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c084de8a536c5cc7c25f175ae660f5c53e2b208627ff543519ba84ba4f4563d7`

```dockerfile
```

-	Layers:
	-	`sha256:7852a62ab78d7e75840ccf6e898660f768d36387186e51d9cf955a3a414d7f0b`  
		Last Modified: Wed, 22 Apr 2026 05:12:16 GMT  
		Size: 7.9 MB (7921377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9ac155457fe4186d8f780358ccf275744696e233104f8c9ec4d32ec4aaa4ca6`  
		Last Modified: Wed, 22 Apr 2026 05:12:15 GMT  
		Size: 7.3 KB (7316 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:77f96c05d00d37c99703008da18867920efbc940ad62e55c4ecd29a13233cab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114611699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb156061cbf691e6fcc997c9544dbe50597bfda35b412592e194741c04d986d4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 02:18:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 03:52:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:b7f7b3cfb222580c94a933dbaaabd959ea960847c9aff9c5d4daa21494eea44d`  
		Last Modified: Wed, 22 Apr 2026 00:16:47 GMT  
		Size: 49.1 MB (49055006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2698f04c927addec960608562122b5f1c50ad262b50810e813b3046303555106`  
		Last Modified: Wed, 22 Apr 2026 02:18:42 GMT  
		Size: 14.9 MB (14905103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a451edd267f2ece592819d45854d958b47c98b8c4b25b1c98edd54f76d1bcc`  
		Last Modified: Wed, 22 Apr 2026 03:52:30 GMT  
		Size: 50.7 MB (50651590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b8b482abf085d5381b6d31527efac2133fb56a4e16b2f5093e00744a6084d543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7930159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d981b2193cf35e04fe3cf64bfd65f0d529e02dca390a65744169ea7ea2d8b3a`

```dockerfile
```

-	Layers:
	-	`sha256:a4acab6a0172afe092027532d569dc09378b90eb9fc31ebd2f051c718eb35bfc`  
		Last Modified: Wed, 22 Apr 2026 03:52:29 GMT  
		Size: 7.9 MB (7922779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:093370ab030af171fef1d2ea52e3e535b06b706b607a7152f45788bfe4aafa58`  
		Last Modified: Wed, 22 Apr 2026 03:52:29 GMT  
		Size: 7.4 KB (7380 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b38a199192d351d19ff3fe4ad8413912701a5b18c2a33dcf1a750ec7dad72aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122914259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:029be32ec1ef525a4379ba5a323038e12768f9b428c8fec39c69f64682f901ef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:42:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:d66293db501a72163d605baf6b3e8451c38d0fe30b934c24cec53a4e66b6e46d`  
		Last Modified: Wed, 22 Apr 2026 00:16:07 GMT  
		Size: 52.3 MB (52253001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8876687e9899211f85cbf406fe17625833ba27c454fedd4275ac8a0a58206e1d`  
		Last Modified: Wed, 22 Apr 2026 01:43:08 GMT  
		Size: 15.8 MB (15774737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41762a69c06632f02d051591b8561619178cda30090272dff52f65c2d6157695`  
		Last Modified: Wed, 22 Apr 2026 02:32:20 GMT  
		Size: 54.9 MB (54886521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e07d88293648ee8191dfd86a45d6b716654ab6ef15a968d694294f08ce92a90b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7934507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6470c56c07a016f551652f456a25db9ac4cae1cb58ba1f9a848b19c2d25b8700`

```dockerfile
```

-	Layers:
	-	`sha256:57dee51a73309c0da7c1afe2cdb654bafebeacc012946a8888f194a1a4690016`  
		Last Modified: Wed, 22 Apr 2026 02:32:19 GMT  
		Size: 7.9 MB (7927111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87d45b069da789d2734dce3da78fe2fa8cda5a541c75334b8423879b3aa9cb9c`  
		Last Modified: Wed, 22 Apr 2026 02:32:19 GMT  
		Size: 7.4 KB (7396 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e3e050696034e3fb4bcc4deb855fb70f47451863fdf768818df9b026ee6010a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127061611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a209bffcd2cbf6afe2baeeee27942ebf7973aa510d59ca6bb077d7d32de902`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1776729600'
# Wed, 22 Apr 2026 01:42:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:02:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:737d996bc05c156425b11be5deec8366db5d7a009f49d85b480b1daec555cf4a`  
		Last Modified: Wed, 22 Apr 2026 00:16:40 GMT  
		Size: 54.7 MB (54705161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f313e1ea7e09266848088c3a09b07b715bfc6a8bb9980dc9b80da0fb20132694`  
		Last Modified: Wed, 22 Apr 2026 01:43:07 GMT  
		Size: 16.3 MB (16295616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae525ab0fbeb04dd4bb1d8468feefde68ce73f1bb5bc987c27f9283ecf43104`  
		Last Modified: Wed, 22 Apr 2026 05:02:53 GMT  
		Size: 56.1 MB (56060834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f6e8fcc11d79842cfb72f3847f55f09c581e6cb6c78766db0465ff4b48b8c217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7924241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89edbfb8fc274d599fe8f93dedce86b452bd7db36ec8000e310b223e185a5216`

```dockerfile
```

-	Layers:
	-	`sha256:6234661890a8a5ca56972dea09f37deebe12801b82a55889ba9e328936c7401b`  
		Last Modified: Wed, 22 Apr 2026 05:02:52 GMT  
		Size: 7.9 MB (7916947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9de5b62056006caf97edba534125d2e82485cab3dc3506a0d4f98c0c6fe6b447`  
		Last Modified: Wed, 22 Apr 2026 05:02:52 GMT  
		Size: 7.3 KB (7294 bytes)  
		MIME: application/vnd.in-toto+json
