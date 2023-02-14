## `notary:signer-0.7.0`

```console
$ docker pull notary@sha256:5373d1dc7a4bb1a0d5845dc8e980033e152c4abba83935f92af8e362ed4be593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `notary:signer-0.7.0` - linux; amd64

```console
$ docker pull notary@sha256:a32ca4b08f0ccdc45b43475d7b7353af6833d8037bad57f4efcb0d9537912f22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7570971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fbfefc7359c8393ee6b8c724964f95dbd722babc1cc61b7f054b1c8e80eb5ee`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 10:15:51 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 11 Feb 2023 10:16:14 GMT
EXPOSE map[4444/tcp:{}]
# Sat, 11 Feb 2023 10:16:14 GMT
EXPOSE map[7899/tcp:{}]
# Sat, 11 Feb 2023 10:16:14 GMT
ENV INSTALLDIR=/notary/signer
# Sat, 11 Feb 2023 10:16:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Sat, 11 Feb 2023 10:16:14 GMT
WORKDIR /notary/signer
# Tue, 14 Feb 2023 19:48:25 GMT
COPY /notary-signer ./ # buildkit
# Tue, 14 Feb 2023 19:48:26 GMT
RUN ./notary-signer --version # buildkit
# Tue, 14 Feb 2023 19:48:26 GMT
COPY ./signer-config.json . # buildkit
# Tue, 14 Feb 2023 19:48:26 GMT
COPY ./entrypoint.sh . # buildkit
# Tue, 14 Feb 2023 19:48:26 GMT
USER notary
# Tue, 14 Feb 2023 19:48:26 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 14 Feb 2023 19:48:26 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a8bf9348133d1e770b90e9991d3f65c555075470962fb5e1321cf7201947a6`  
		Last Modified: Sat, 11 Feb 2023 10:16:25 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0208e6d213823747dbf355ecd6e4879b414b1413e219476f0ffa3791d92aade7`  
		Last Modified: Sat, 11 Feb 2023 10:16:33 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ea3b132bb393557035251ac3ad556a8f57d1374a7cfb3f2ecd7f97dc9814d0`  
		Last Modified: Tue, 14 Feb 2023 19:48:45 GMT  
		Size: 4.8 MB (4761040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a8c0509c8246e238f50e7d252bcc55458fd125efdd76eeb075d4315aeaad5b2`  
		Last Modified: Tue, 14 Feb 2023 19:48:44 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2b6c690c3444e66f6d6827e165fb13d288db85b531f46685aae419e0e54bca`  
		Last Modified: Tue, 14 Feb 2023 19:48:44 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331e19bd6af30dd478fa5b6d49f371ca240f50e9dbd28fce6a5a3092896215da`  
		Last Modified: Tue, 14 Feb 2023 19:48:44 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; arm variant v6

```console
$ docker pull notary@sha256:150152b98fa58322e04938a5daac7e3f0404a60e0fcbe3810e2540f87269b9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7143381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb2d50f5f9c16b2c84f3c7c7e9ef3773365d8816b0731a7a30e34d304996af2`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:32 GMT
ADD file:be37ec4af7b6db1fa6f84ab2c33fc04aaba5914eb2ac433a417e619fed27c5b4 in / 
# Fri, 10 Feb 2023 20:49:32 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 02:32:16 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 11 Feb 2023 02:32:55 GMT
EXPOSE map[4444/tcp:{}]
# Sat, 11 Feb 2023 02:32:55 GMT
EXPOSE map[7899/tcp:{}]
# Sat, 11 Feb 2023 02:32:55 GMT
ENV INSTALLDIR=/notary/signer
# Sat, 11 Feb 2023 02:32:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Sat, 11 Feb 2023 02:32:55 GMT
WORKDIR /notary/signer
# Tue, 14 Feb 2023 21:25:08 GMT
COPY /notary-signer ./ # buildkit
# Tue, 14 Feb 2023 21:25:08 GMT
RUN ./notary-signer --version # buildkit
# Tue, 14 Feb 2023 21:25:08 GMT
COPY ./signer-config.json . # buildkit
# Tue, 14 Feb 2023 21:25:08 GMT
COPY ./entrypoint.sh . # buildkit
# Tue, 14 Feb 2023 21:25:08 GMT
USER notary
# Tue, 14 Feb 2023 21:25:08 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 14 Feb 2023 21:25:08 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:c35ac6bda1fd9456dc61d44052491ecd935dcde4eb6088d66765ca8c6b57cb7d`  
		Last Modified: Fri, 10 Feb 2023 20:50:40 GMT  
		Size: 2.6 MB (2616778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85e652d0821d7b3cb171424201f4c94165c61ecc2b9f1b6d059c6b18994ffd08`  
		Last Modified: Sat, 11 Feb 2023 02:33:16 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c6ce0c76930b11592424a93e59b53baba39c156698eec54ee9e678cdede4a7`  
		Last Modified: Sat, 11 Feb 2023 02:33:27 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c46f8dfcf85e61f69f1c568d9a8b16fff27f3e15c7f38fec5b345776f7346502`  
		Last Modified: Tue, 14 Feb 2023 21:25:41 GMT  
		Size: 4.5 MB (4524467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b1087aad7cd54f74e3d9aa81a08b456bb66658da54640e1e480a9930f36c97`  
		Last Modified: Tue, 14 Feb 2023 21:25:40 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0449f608b673cfd349c4147c1cfb626385132c2d0676b4c5477527343f1500b1`  
		Last Modified: Tue, 14 Feb 2023 21:25:40 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8757f95d6ad6e47175082a9acaf16bd92632acea77e82ce04e942b71b6a837d4`  
		Last Modified: Tue, 14 Feb 2023 21:25:40 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:b996fa59113db0724190ede3d6fb80277220d6454f266b6b215b78bc6b5adea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7100912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69097e69e033542a4684aca4d0901a72052b402c5fb14366c2a4aaff7d70c54`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 02:01:39 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 11 Feb 2023 02:01:58 GMT
EXPOSE map[4444/tcp:{}]
# Sat, 11 Feb 2023 02:01:58 GMT
EXPOSE map[7899/tcp:{}]
# Sat, 11 Feb 2023 02:01:58 GMT
ENV INSTALLDIR=/notary/signer
# Sat, 11 Feb 2023 02:01:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Sat, 11 Feb 2023 02:01:58 GMT
WORKDIR /notary/signer
# Tue, 14 Feb 2023 20:05:11 GMT
COPY /notary-signer ./ # buildkit
# Tue, 14 Feb 2023 20:05:11 GMT
RUN ./notary-signer --version # buildkit
# Tue, 14 Feb 2023 20:05:11 GMT
COPY ./signer-config.json . # buildkit
# Tue, 14 Feb 2023 20:05:11 GMT
COPY ./entrypoint.sh . # buildkit
# Tue, 14 Feb 2023 20:05:11 GMT
USER notary
# Tue, 14 Feb 2023 20:05:11 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 14 Feb 2023 20:05:11 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76b9e3dceb52b5f1909f74e5761d8b0968630630d4c5d37134133ff1529d57ca`  
		Last Modified: Sat, 11 Feb 2023 02:02:10 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9044747e4fd585aae1a06ddae8513379f85e397343798bc36f0e5504eaa9863f`  
		Last Modified: Sat, 11 Feb 2023 02:02:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a81d4b78187ac1efd333e945e651dc6b6198daae9c082d94d7119fe25f3ebca`  
		Last Modified: Tue, 14 Feb 2023 20:05:31 GMT  
		Size: 4.4 MB (4389245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f56fe643adcf25bb51de8f06906ff1b64c14b9056ad59ff37dad70382951afe0`  
		Last Modified: Tue, 14 Feb 2023 20:05:30 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd8fe7e0c1c1e22804d7ef7823bb82d60d4bef8002a1dec3da88a96b3f88986d`  
		Last Modified: Tue, 14 Feb 2023 20:05:30 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd487ee96c34fbc41727344a83b1ab76255216752122ec7a7cba14f964998f22`  
		Last Modified: Tue, 14 Feb 2023 20:05:30 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; 386

```console
$ docker pull notary@sha256:79b4c323f58cb5f6ea257c2af5204098abeea66bb6d3c60b46f4693e04741701
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7381566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ddf368d5d9c9179b534f7d9a67b82e27281f60554a17dc0820eabc3abfca32c`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Sat, 12 Nov 2022 03:38:23 GMT
ADD file:561637cbdd23fdd69f555dbc938902d79be2b123eb244d2cfd35b337878b63df in / 
# Sat, 12 Nov 2022 03:38:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:57:54 GMT
RUN adduser -D -H -g "" notary
# Sat, 12 Nov 2022 04:58:12 GMT
EXPOSE 4444
# Sat, 12 Nov 2022 04:58:12 GMT
EXPOSE 7899
# Sat, 12 Nov 2022 04:58:13 GMT
ENV INSTALLDIR=/notary/signer
# Sat, 12 Nov 2022 04:58:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Sat, 12 Nov 2022 04:58:15 GMT
WORKDIR /notary/signer
# Wed, 16 Nov 2022 20:11:26 GMT
COPY file:044b2b6099382d2e11ff09d47c7a63f7cf3796f05317a8a2bbfed5d98c843503 in ./ 
# Wed, 16 Nov 2022 20:11:26 GMT
RUN ./notary-signer --version
# Wed, 16 Nov 2022 20:11:28 GMT
COPY file:180643db1fd4154262e619c42c1255057d49a4c6cd56be3f475942fd0a35a236 in . 
# Wed, 16 Nov 2022 20:11:29 GMT
COPY file:849eab43398bc401ed08e75cbad3ea52969452506337a4135a0ef8144dff93ad in . 
# Wed, 16 Nov 2022 20:11:29 GMT
USER notary
# Wed, 16 Nov 2022 20:11:30 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 16 Nov 2022 20:11:31 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:0c10ccf9426f4a034c81b9e1a0fa81fc5cd957d8a4e0ea545ee33f4cd59f227b`  
		Last Modified: Sat, 12 Nov 2022 03:39:07 GMT  
		Size: 2.8 MB (2808348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e2a37344f15c9c47f28fb76d0bbfae6f9adb65b4d686216a9a5881505ed0ec`  
		Last Modified: Sat, 12 Nov 2022 04:58:40 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26472dc994c1e659b114a40b8becb18e4595de57079b3495843fe3ee077329d`  
		Last Modified: Sat, 12 Nov 2022 04:58:51 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77cc9f8b030709827b83734498c26e9c13fdcad73c1751041bf38760164b7c8`  
		Last Modified: Wed, 16 Nov 2022 20:11:58 GMT  
		Size: 4.6 MB (4571177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d739be5aa3edcc7ba9f282a037921fc7c54d03aa47497444165ee21ada1487a6`  
		Last Modified: Wed, 16 Nov 2022 20:11:57 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f6cc98121c6d6e23c455cc4891ee75f1d872207a89e3ff24c67d8eedf86dac`  
		Last Modified: Wed, 16 Nov 2022 20:11:58 GMT  
		Size: 383.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; ppc64le

```console
$ docker pull notary@sha256:4250c10583a47db0acb27996c14af9bb0a527a6e60de127345afa805a8db6bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7102631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f0fa719a72f6ccfe9ba74a86650c468ccb8e88a02522baeee242d920c6e939`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:44 GMT
ADD file:d9267e5b7618ca1c5ac918cde29e6967fae2132ab0672112ee2c6604e96a0b66 in / 
# Fri, 10 Feb 2023 21:20:45 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 09:31:58 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 11 Feb 2023 09:32:48 GMT
EXPOSE map[4444/tcp:{}]
# Sat, 11 Feb 2023 09:32:48 GMT
EXPOSE map[7899/tcp:{}]
# Sat, 11 Feb 2023 09:32:48 GMT
ENV INSTALLDIR=/notary/signer
# Sat, 11 Feb 2023 09:32:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Sat, 11 Feb 2023 09:32:48 GMT
WORKDIR /notary/signer
# Tue, 14 Feb 2023 20:15:00 GMT
COPY /notary-signer ./ # buildkit
# Tue, 14 Feb 2023 20:15:01 GMT
RUN ./notary-signer --version # buildkit
# Tue, 14 Feb 2023 20:15:01 GMT
COPY ./signer-config.json . # buildkit
# Tue, 14 Feb 2023 20:15:02 GMT
COPY ./entrypoint.sh . # buildkit
# Tue, 14 Feb 2023 20:15:02 GMT
USER notary
# Tue, 14 Feb 2023 20:15:02 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 14 Feb 2023 20:15:02 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:e3b9153081a195877a8587137034c9b223749c582ea32371419055f7d77c97ba`  
		Last Modified: Fri, 10 Feb 2023 21:21:53 GMT  
		Size: 2.8 MB (2804628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674d271c42b70a8c82b552b2772787a6cac62d60cdc88c599bd983e06b4b1199`  
		Last Modified: Sat, 11 Feb 2023 09:33:10 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11d0b9967527e3e2fe9a387dd1b08ba83b7816d9e3863fb0f3e9c0a13f0225d`  
		Last Modified: Sat, 11 Feb 2023 09:33:20 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cf6298bbc72ecb7b1d6fcd1cfe5577e70428f82def85e4e5e723220a95877f`  
		Last Modified: Tue, 14 Feb 2023 20:15:33 GMT  
		Size: 4.3 MB (4295841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b5e5b3b288b9ceb09e32d8c70945bf38bd6d50ba8cde6f293935823018d3f9`  
		Last Modified: Tue, 14 Feb 2023 20:15:31 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2d02094f2fbb29e29edc0b0c6c7fa436245b124690c0a9f3b6bcef89877c0a`  
		Last Modified: Tue, 14 Feb 2023 20:15:31 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0408e382b4f148c24f633c13bd5b869bdeb1c2672be269c87c8a5c837d411509`  
		Last Modified: Tue, 14 Feb 2023 20:15:31 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; s390x

```console
$ docker pull notary@sha256:4fdcbeca622ba6241ed58226dad1b57bd1184a196391ab3ddca31d2f69a2fa67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7200770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f58a1450acc82b0abe0ca7be52a0c6236da591895ecd1c85835b138a9d94f5`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:31 GMT
ADD file:17af250b49631cf2acf655c85df90977eddab4c9afd67bda3c577db5200364f1 in / 
# Fri, 10 Feb 2023 21:41:32 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 03:38:26 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 11 Feb 2023 03:38:57 GMT
EXPOSE map[4444/tcp:{}]
# Sat, 11 Feb 2023 03:38:57 GMT
EXPOSE map[7899/tcp:{}]
# Sat, 11 Feb 2023 03:38:57 GMT
ENV INSTALLDIR=/notary/signer
# Sat, 11 Feb 2023 03:38:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Sat, 11 Feb 2023 03:38:57 GMT
WORKDIR /notary/signer
# Tue, 14 Feb 2023 20:11:23 GMT
COPY /notary-signer ./ # buildkit
# Tue, 14 Feb 2023 20:11:23 GMT
RUN ./notary-signer --version # buildkit
# Tue, 14 Feb 2023 20:11:23 GMT
COPY ./signer-config.json . # buildkit
# Tue, 14 Feb 2023 20:11:23 GMT
COPY ./entrypoint.sh . # buildkit
# Tue, 14 Feb 2023 20:11:23 GMT
USER notary
# Tue, 14 Feb 2023 20:11:23 GMT
ENTRYPOINT ["entrypoint.sh"]
# Tue, 14 Feb 2023 20:11:23 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:667d93a24f321610e24486f3148545191f113ab9ab2444804087dd65ebbda9ed`  
		Last Modified: Fri, 10 Feb 2023 21:42:26 GMT  
		Size: 2.6 MB (2593581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf825008c0747d1db1e6a08e31a5fa2a33c8e0f8a5fe8b2f86af75110c97e790`  
		Last Modified: Sat, 11 Feb 2023 03:39:15 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47b3001bbc3d992bc8bd18f0274d2c096ab38122bfe91ebb713a068610faf80`  
		Last Modified: Sat, 11 Feb 2023 03:39:21 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cac66e854f11abab43d7b30fe65513a601cb405b6f9b518fd84ebd661e02965`  
		Last Modified: Tue, 14 Feb 2023 20:11:51 GMT  
		Size: 4.6 MB (4605020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d38e12dd4eebba9a3bd638a4411e7efbf56c1458ca16f05c0e39ae163d2f494`  
		Last Modified: Tue, 14 Feb 2023 20:11:51 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03d24e11ffcd1a03ece4219982fd2013790c86ecb653bcecbe2dba9ea8f5fe1`  
		Last Modified: Tue, 14 Feb 2023 20:11:51 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562f4be7070599e2988be138ee08882440aa7b6211ec1a8f16d50e118603b38f`  
		Last Modified: Tue, 14 Feb 2023 20:11:51 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
