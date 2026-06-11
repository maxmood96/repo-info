## `buildpack-deps:oldoldstable-scm`

```console
$ docker pull buildpack-deps@sha256:0ab1c29af91b6182985b2e27326674a0eae0e0d67d7601944755fd249c0c623a
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
$ docker pull buildpack-deps@sha256:956e1fcbab763fb83a0f004c81970e78307fe57260f63562a8ecdca373bd9a0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124305641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d664a4f20d3e02235f6d0a9499e2c5c8fc70699025e1095ebd3f04760695d81`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:42:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:af48a3e7696e07f88a02f9674e541901b65eadb5cf0f62e566b1d895099a1e9e`  
		Last Modified: Wed, 10 Jun 2026 23:40:09 GMT  
		Size: 53.8 MB (53771769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f53a3a71a19cca6d8312e9c60a5428b23742024a0057b1f0e46517df6ae4a9`  
		Last Modified: Thu, 11 Jun 2026 00:42:31 GMT  
		Size: 15.8 MB (15790824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3db6c46730caf21fd1b15e0e84732744cb5a66e6931cf2c3753965fc32257fc`  
		Last Modified: Thu, 11 Jun 2026 02:24:52 GMT  
		Size: 54.7 MB (54743048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d36ad13d3ec959c8f7f52dc61044b8e689633e25d4098678ccdba6e6416e7d76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7928697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dac7e6839d614bf3a8bd26b04d721fe1764e4eb72b4aa6177b5eb9000541d33`

```dockerfile
```

-	Layers:
	-	`sha256:26ad3364c9a04b258cab7858aded69a9ce376ea77cb2f24836923f78825fe93f`  
		Last Modified: Thu, 11 Jun 2026 02:24:50 GMT  
		Size: 7.9 MB (7921381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f72bfd24790a0b1e5805e158ada759c1459ad57c02ef61b847c59a1742c87602`  
		Last Modified: Thu, 11 Jun 2026 02:24:50 GMT  
		Size: 7.3 KB (7316 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f0b7a7cf6263809eefc74932203f50d1c1254f6df1398bc4377b5c9026a31a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.6 MB (114628397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81e6e0d80e73c5134f58a974d30ee9ca6c9bd0100bc9b540ceaa58d49e94200a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:24:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:43:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:057662c04791d47966179d44811cec5af4565f7f7a6a4690c7d8e834d0ba3bd2`  
		Last Modified: Wed, 10 Jun 2026 23:40:48 GMT  
		Size: 49.1 MB (49064004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa240a68c3059c2e50ee1949050052855111d59f6865103a70421028ec0d924`  
		Last Modified: Thu, 11 Jun 2026 01:24:38 GMT  
		Size: 14.9 MB (14905396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c8d826bdbb6b8ffba198124f6ff94c9cf241cbd4761c9ad97d0feb1a0f3333`  
		Last Modified: Thu, 11 Jun 2026 02:43:52 GMT  
		Size: 50.7 MB (50658997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ffae1509c4be21ffe4cf0c5186b33d03652af6c04d26754bbf0025493ac35677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7930163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:585f547e616db6b423fc6b75531204fa3b33c4f74943c4fefe900e05f77ad272`

```dockerfile
```

-	Layers:
	-	`sha256:8fd63b883a0a0070c39b5d2205ab52890a9b813953b483713f60b4a4a90343c1`  
		Last Modified: Thu, 11 Jun 2026 02:43:51 GMT  
		Size: 7.9 MB (7922783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39d509cd6e8d1c6d69020c20af4ff384540275f0cc843a1e542c5080260c78e5`  
		Last Modified: Thu, 11 Jun 2026 02:43:50 GMT  
		Size: 7.4 KB (7380 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:df88d3931b3071f7830a934cdadcd08741805b9438432887a47736809170fe7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122918502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa662ff54c0408e00f32642f3fc92717d0c72118dffea1e8f359cae6b0db8793`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:43:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:7c21e59e753cb91625909251110d6e4cc4a5411b4b7b37f74a62e56b927b7f1e`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 52.3 MB (52264114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8698eac281c2783fff44c0d5a2c381eeb273791e12f4dc8b407db26260bc3b85`  
		Last Modified: Thu, 11 Jun 2026 00:43:55 GMT  
		Size: 15.8 MB (15774833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd4791f1a451400cf59328cbd4f4f9bed438b89f7103b59dc50338fd2ac9293`  
		Last Modified: Thu, 11 Jun 2026 02:24:59 GMT  
		Size: 54.9 MB (54879555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e35b34fe971dbb8116d3f6198c8698dadbc964fe1eda7f009704773287536b87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7934511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:823c54b1cf8b30363420a28c3223b1918ef17deff5d80a43944b3a5a3be9fd83`

```dockerfile
```

-	Layers:
	-	`sha256:53143692f7de86c4e4d9b36bc5488fc1cf2f037f94230d1fe3c3d87078110003`  
		Last Modified: Thu, 11 Jun 2026 02:24:58 GMT  
		Size: 7.9 MB (7927115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e57eded9b41603853da4f4bf484fcf40c94ed402abdc49e74b220730876b2548`  
		Last Modified: Thu, 11 Jun 2026 02:24:58 GMT  
		Size: 7.4 KB (7396 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:oldoldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:8c4675ff4efb60a089327eef6a64bc78bfdf74ee4271988b0e0b2f5311c1db53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.1 MB (127056069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0779cadcc161d7ef7fd76b0b78505e4ff73bd690240c335141a9768bc736d4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 00:44:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fa94b3659141003eaf4c6c1ec8d2e2140d97afd4e23da5fb64936eff3ddbe795`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 54.7 MB (54712857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7baf1917f31dc6264a068963cb19f53c4fc1fb3df24b85fb7b1a7235134b9d`  
		Last Modified: Thu, 11 Jun 2026 00:45:01 GMT  
		Size: 16.3 MB (16295657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c66634bc3fa0a0bcd10bde2aef17a8a2d29d8cc303406e191342fab9599745`  
		Last Modified: Thu, 11 Jun 2026 02:24:53 GMT  
		Size: 56.0 MB (56047555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:oldoldstable-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8b778828141bd1dfb523e76327a9275ed19d1cba7809d7e9de5fbe5b1fc0b05f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7924245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dffc9b370bba35c2ce6debf15cde9ad548f9ca865d72a53a0b17614700d02685`

```dockerfile
```

-	Layers:
	-	`sha256:3b4539b2c1e7f2e80c197f3eaeceee7b28c777ea781c16b281e6434eb9d776a8`  
		Last Modified: Thu, 11 Jun 2026 02:24:51 GMT  
		Size: 7.9 MB (7916951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bd2c8b134233229b7240d346742d67a2073abe81bcaed463a8703661b9dc98a`  
		Last Modified: Thu, 11 Jun 2026 02:24:52 GMT  
		Size: 7.3 KB (7294 bytes)  
		MIME: application/vnd.in-toto+json
