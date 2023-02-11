## `notary:signer-0.7.0`

```console
$ docker pull notary@sha256:b3ba0e2985f1f882616ef90f5b54ab6cf05b3befd674f056c83ceac4070c9e3d
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
$ docker pull notary@sha256:f00c696380534b61fbf5e0c9137f0d2c475222c77b2a2b3090807c21dbf19480
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7565648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120b11cd1c150c6e4e3c823fc330779f4984867eac70bd007f2f2599f6d01152`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 06:38:02 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 12 Nov 2022 06:38:08 GMT
EXPOSE map[4444/tcp:{}]
# Sat, 12 Nov 2022 06:38:08 GMT
EXPOSE map[7899/tcp:{}]
# Sat, 12 Nov 2022 06:38:08 GMT
ENV INSTALLDIR=/notary/signer
# Sat, 12 Nov 2022 06:38:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Sat, 12 Nov 2022 06:38:08 GMT
WORKDIR /notary/signer
# Wed, 11 Jan 2023 00:28:27 GMT
COPY /notary-signer ./ # buildkit
# Wed, 11 Jan 2023 00:28:27 GMT
RUN ./notary-signer --version # buildkit
# Wed, 11 Jan 2023 00:28:28 GMT
COPY ./signer-config.json . # buildkit
# Wed, 11 Jan 2023 00:28:28 GMT
COPY ./entrypoint.sh . # buildkit
# Wed, 11 Jan 2023 00:28:28 GMT
USER notary
# Wed, 11 Jan 2023 00:28:28 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 11 Jan 2023 00:28:28 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab556644ad7457163fa974396862be0db6a3e9b2a288041b04e6009ae65f4ed`  
		Last Modified: Sat, 12 Nov 2022 06:38:20 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da59cda2c120691b5be31fdc1571f10856ae5c4527c577ae2f76cd70fcd4a05`  
		Last Modified: Sat, 12 Nov 2022 06:38:29 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18df28869ba84e36cb24d2a6ffa9c8c495aadfd4a580bbc2fd32241b8d3e53bf`  
		Last Modified: Wed, 11 Jan 2023 00:28:47 GMT  
		Size: 4.8 MB (4757208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d38f8b72abfe9ed90b46e58eec6c1c29e3956676d9859f7df8ba7c9ccd8fb6`  
		Last Modified: Wed, 11 Jan 2023 00:28:46 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf34f3a2e8b14a03d0f25158b458b3ca10e626f01f0abee722308141866bbc95`  
		Last Modified: Wed, 11 Jan 2023 00:28:46 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8fa916538b7fae7415495c17ce06d7c5066d3fd40a5c5b7da79a6233f391b9`  
		Last Modified: Wed, 11 Jan 2023 00:28:46 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; arm variant v6

```console
$ docker pull notary@sha256:bb634ca5536aa9b0f344d70a69b5bba91834f122d8b4b80b5d77f78a9cd9e115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7139247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b297fbb89517418584491cdfd9419367d1c4f28cb4691026d3f683e650942858`
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
# Sat, 11 Feb 2023 02:32:55 GMT
COPY /notary-signer ./ # buildkit
# Sat, 11 Feb 2023 02:32:56 GMT
RUN ./notary-signer --version # buildkit
# Sat, 11 Feb 2023 02:32:56 GMT
COPY ./signer-config.json . # buildkit
# Sat, 11 Feb 2023 02:32:56 GMT
COPY ./entrypoint.sh . # buildkit
# Sat, 11 Feb 2023 02:32:56 GMT
USER notary
# Sat, 11 Feb 2023 02:32:56 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 11 Feb 2023 02:32:56 GMT
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
	-	`sha256:eaa00b98a5acf034479f22ee64b7429d4a0aeaa856b44629b9756452041aa9e4`  
		Last Modified: Sat, 11 Feb 2023 02:33:27 GMT  
		Size: 4.5 MB (4520337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ffb805c9e2812b9294142e339972078f0d79a633a4ea690056cc04b6424e87`  
		Last Modified: Sat, 11 Feb 2023 02:33:26 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76d0cb4d34a8add21d4d92b2a4853079a584c6e0b04fe49ece561625ba35e4f`  
		Last Modified: Sat, 11 Feb 2023 02:33:27 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0ac6a2120d1e1319ad9168d959adcff931ac1e2a7c1c6d21a95efe4c5a712e`  
		Last Modified: Sat, 11 Feb 2023 02:33:27 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; arm64 variant v8

```console
$ docker pull notary@sha256:7cc9193896a1b251d5c57fd458cab668557003ab8e654e19235f798dbfc39463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7096247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b45990584b7c7b8d55319e5d6f006444953afe3ff1a8e91ba320205454af5af`
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
# Sat, 11 Feb 2023 02:01:58 GMT
COPY /notary-signer ./ # buildkit
# Sat, 11 Feb 2023 02:01:58 GMT
RUN ./notary-signer --version # buildkit
# Sat, 11 Feb 2023 02:01:58 GMT
COPY ./signer-config.json . # buildkit
# Sat, 11 Feb 2023 02:01:58 GMT
COPY ./entrypoint.sh . # buildkit
# Sat, 11 Feb 2023 02:01:58 GMT
USER notary
# Sat, 11 Feb 2023 02:01:58 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 11 Feb 2023 02:01:58 GMT
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
	-	`sha256:7b44e162f00aeb4f435e25060abfebcd6a3177de0014d4e29bbf5a153ceb48f5`  
		Last Modified: Sat, 11 Feb 2023 02:02:19 GMT  
		Size: 4.4 MB (4384594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8714777b7cf5843776b9082e6dd73159753d55218ae6f1732bdaff862c5ef93`  
		Last Modified: Sat, 11 Feb 2023 02:02:19 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84ed9f175dc798302fa2481354771d76f6e4f027aacb021b415e8dfb173dc4fb`  
		Last Modified: Sat, 11 Feb 2023 02:02:19 GMT  
		Size: 349.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b02ad41bc78686eaa6c286b9846236aeb22f1725692e5b5d7192923273d196c`  
		Last Modified: Sat, 11 Feb 2023 02:02:19 GMT  
		Size: 376.0 B  
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
$ docker pull notary@sha256:2b2cac51751dbe89a896622064b2b6daa113c9af5a44c68b092ffe41f1b2334f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7096889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f7d83174a997548fe80efaf19090e2ca8db1780da72697fd0e25fec0544cb5`
-	Entrypoint: `["entrypoint.sh"]`
-	Default Command: `["notary-signer","--version"]`

```dockerfile
# Sat, 12 Nov 2022 04:16:30 GMT
ADD file:6f7965319fe0caaea57086835c0c2212284c6850f33e3c4d522c758e43acbc98 in / 
# Sat, 12 Nov 2022 04:16:31 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 07:12:27 GMT
RUN adduser -D -H -g "" notary # buildkit
# Sat, 12 Nov 2022 07:12:40 GMT
EXPOSE map[4444/tcp:{}]
# Sat, 12 Nov 2022 07:12:40 GMT
EXPOSE map[7899/tcp:{}]
# Sat, 12 Nov 2022 07:12:40 GMT
ENV INSTALLDIR=/notary/signer
# Sat, 12 Nov 2022 07:12:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/notary/signer
# Sat, 12 Nov 2022 07:12:40 GMT
WORKDIR /notary/signer
# Wed, 11 Jan 2023 00:34:42 GMT
COPY /notary-signer ./ # buildkit
# Wed, 11 Jan 2023 00:34:43 GMT
RUN ./notary-signer --version # buildkit
# Wed, 11 Jan 2023 00:34:44 GMT
COPY ./signer-config.json . # buildkit
# Wed, 11 Jan 2023 00:34:44 GMT
COPY ./entrypoint.sh . # buildkit
# Wed, 11 Jan 2023 00:34:44 GMT
USER notary
# Wed, 11 Jan 2023 00:34:44 GMT
ENTRYPOINT ["entrypoint.sh"]
# Wed, 11 Jan 2023 00:34:44 GMT
CMD ["notary-signer" "--version"]
```

-	Layers:
	-	`sha256:5c3a6ece62351976dfb4b56dc417aebd2a7dbda14ebac2737edd2ab43883553f`  
		Last Modified: Sat, 12 Nov 2022 04:17:14 GMT  
		Size: 2.8 MB (2801551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15023fe5082ace3d77a3ca4c98a9b31b5bef60a4835bddce618606ee9f17cf6`  
		Last Modified: Sat, 12 Nov 2022 07:13:02 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca3c7abc8ed18b90618dae3d8ed39fa05a0357ae27fab896191fb471938ae78`  
		Last Modified: Sat, 12 Nov 2022 07:13:14 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deee061c403b3386800e6c7e6923b535156333ff7487eba4829685703f26b077`  
		Last Modified: Wed, 11 Jan 2023 00:35:16 GMT  
		Size: 4.3 MB (4293169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:105871502b0be8567633ecfebc62cb7b991169a9deab7511536215264306a237`  
		Last Modified: Wed, 11 Jan 2023 00:35:15 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43c93a3c85bd91aacf3c678ee7161a59f4e917b935af370e2610d5a427db3f94`  
		Last Modified: Wed, 11 Jan 2023 00:35:15 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152baf0ef7c80edfa82907d1e9ab9aa1a72dea74d9a533f9b7ed79414953cb57`  
		Last Modified: Wed, 11 Jan 2023 00:35:15 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `notary:signer-0.7.0` - linux; s390x

```console
$ docker pull notary@sha256:8820af22a3b00b473863d68fb40268dec9836bb55f3303db4333e876d085859c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7197247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f539e399ab2f3957c8fbad1bde72670b37493863b4da684a17e1812913a7f2`
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
# Sat, 11 Feb 2023 03:38:57 GMT
COPY /notary-signer ./ # buildkit
# Sat, 11 Feb 2023 03:38:58 GMT
RUN ./notary-signer --version # buildkit
# Sat, 11 Feb 2023 03:38:58 GMT
COPY ./signer-config.json . # buildkit
# Sat, 11 Feb 2023 03:38:58 GMT
COPY ./entrypoint.sh . # buildkit
# Sat, 11 Feb 2023 03:38:58 GMT
USER notary
# Sat, 11 Feb 2023 03:38:58 GMT
ENTRYPOINT ["entrypoint.sh"]
# Sat, 11 Feb 2023 03:38:58 GMT
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
	-	`sha256:ae7369c97070f6a3fbdc8ff9020486e48e76f68bea04cd630597a2b427124f61`  
		Last Modified: Sat, 11 Feb 2023 03:39:22 GMT  
		Size: 4.6 MB (4601507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e525f79d1d26921173c24db57698269bbb8a4052185fdf39494626b1315748a3`  
		Last Modified: Sat, 11 Feb 2023 03:39:21 GMT  
		Size: 92.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a82556109a5343cbc38e64d4587eca77872ead719d83b49d0f1973a2d51d2dc`  
		Last Modified: Sat, 11 Feb 2023 03:39:21 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4563f9e909600e7aaa50b03cd21fa864ab8cd2f3d51ecce02e3d966076d944eb`  
		Last Modified: Sat, 11 Feb 2023 03:39:21 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
