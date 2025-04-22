## `golang:tip-bullseye`

```console
$ docker pull golang@sha256:e798adffa7a8fa456f4d91a135e8cb77bc778b12d17f96c9459e661fc1c2b973
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

### `golang:tip-bullseye` - linux; amd64

```console
$ docker pull golang@sha256:457095448a1de568ef4b795fe0b488e2b812bbf1c04ec09dfb9a937f1bdac6fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.1 MB (337125806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63a58db0c1731c2177ac24b277eb2cdf2892a4f8f848e47a7b7e04ffd09a29d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 21 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a7819131060d3c79e48555fb5b04fa584b86d2fb80e3ede0864c7e6bba7d87`  
		Last Modified: Tue, 08 Apr 2025 01:24:24 GMT  
		Size: 15.8 MB (15763510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0f843b455b9b7bececb5cfeb4ba5839d4aa47845ded1258734c375304df3d0`  
		Last Modified: Tue, 08 Apr 2025 02:13:52 GMT  
		Size: 54.8 MB (54755152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3acd0fadc520c25381b38db13210a94e1a429fc8f89e37113728d2dd07691000`  
		Last Modified: Mon, 21 Apr 2025 22:38:03 GMT  
		Size: 86.0 MB (86001134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25d4babeaf90344f4555f59166692dee6d066349b1a2f5cb41fc36591cc0aa6`  
		Last Modified: Mon, 21 Apr 2025 22:37:14 GMT  
		Size: 126.9 MB (126857323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c839217eaacae9a30587feb82384b220138593715059f532550a17e09e3e2bc8`  
		Last Modified: Mon, 21 Apr 2025 22:38:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:2481d0ca813f47cf7eabea5374fec8d4d17f75768ee85786b44769c736092dbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10293404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d823ff8ddc1d2b2b07699e3abe38a600c9e772519502b353dbde148b718a513`

```dockerfile
```

-	Layers:
	-	`sha256:3756dfe171f522fca789e89ee6f438e57c84e089304db34fbbdb1d5096e6cdfb`  
		Last Modified: Mon, 21 Apr 2025 22:38:01 GMT  
		Size: 10.3 MB (10266343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42873134dfa2e56760a446e9ba18b877c142ea2df39afd281239e0bc39a85db3`  
		Last Modified: Mon, 21 Apr 2025 22:38:01 GMT  
		Size: 27.1 KB (27061 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:3147665f408243bd30eb5ad48b0dd82bef894bfcae91b96d8ae4c893fda66481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301357239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:773fbace0d0a550c83f8d7e12ebc9e1bafae2b575e749a2ce01b3bcbeafff70a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 21 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8c2fc9e6d23f3debfa68416a2b96331b92d563b20272933315ecfbbada38e955`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 49.0 MB (49031449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525b68fed12d763a57f1b020aa1579673112de80a5b780b5ffaa045109c81f23`  
		Last Modified: Tue, 08 Apr 2025 07:38:26 GMT  
		Size: 14.9 MB (14878713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909681b45fdfcbd0bfebc28d96cd1bdab32fd85e3af6788b49d9cb80e8ff865a`  
		Last Modified: Tue, 08 Apr 2025 17:30:33 GMT  
		Size: 50.6 MB (50624452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cc995e80cedd9d30db7ba6d1ae52e5693d2c40c74ff9101649c68046e8319c`  
		Last Modified: Tue, 08 Apr 2025 20:43:27 GMT  
		Size: 64.9 MB (64922622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5cc54485761ae69a05b08a84359a87e39a46bace5d6d721b8ddc84655c07c3`  
		Last Modified: Mon, 21 Apr 2025 23:32:56 GMT  
		Size: 121.9 MB (121899846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233e989180a367579407e85c3a3da19268f517d58aaa43d65f5bd35513a93317`  
		Last Modified: Mon, 21 Apr 2025 23:36:10 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:36384555cc5adc748ad929ab813627f59a96949dae1fd58ffda80aa59962536d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10099852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df7af2c0fe1c6dfb59cbaef27f95adc40ca27076ec77d458ff6ceabf020b9ac`

```dockerfile
```

-	Layers:
	-	`sha256:4934dfc16f2be3d1d7bbb2fa6c31b7c1ff89eacfeed700f3795e2d1793e40d93`  
		Last Modified: Mon, 21 Apr 2025 23:36:11 GMT  
		Size: 10.1 MB (10072683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbc8f14683cbdbf63553015faf28d97f331baf0159e3f5bb87f47eedd812c665`  
		Last Modified: Mon, 21 Apr 2025 23:36:10 GMT  
		Size: 27.2 KB (27169 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:5b50481885fb16c1f41b5a534b001ef5d36cfb0189bd4118b14f6c7198edb976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.8 MB (323817032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69203b6c1e2de0a55e1ae2d2a0f229377b8933777caaafbae30913823b09ac7e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 21 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9322dad1d7c942b6794e486e4e0b838c10dfb06247f1794d20cc703ddfee969f`  
		Last Modified: Tue, 08 Apr 2025 06:03:40 GMT  
		Size: 15.7 MB (15749086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebaef8f9f6ff21c71a0e336a0e9a00fbb65d469480593ef8d1ef507941e6f6d`  
		Last Modified: Tue, 08 Apr 2025 12:18:43 GMT  
		Size: 54.9 MB (54850009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b066ec7b453f1f7a4cbf31adea4a73d091a7499693ce31c56205980d8778c9c9`  
		Last Modified: Mon, 14 Apr 2025 21:52:34 GMT  
		Size: 81.4 MB (81414208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49c3c4d9fc32722fbee95cae35a84bb5c2c18fa016fa934c1de17d28a4bfa33`  
		Last Modified: Mon, 21 Apr 2025 23:29:01 GMT  
		Size: 119.5 MB (119549349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d81830573bb259fd00c1d3e5eecfc9737c41f7e5af3f03ae24a437514969eb6`  
		Last Modified: Mon, 21 Apr 2025 23:31:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:805ddae870e0174179bb0372a5ebbf21099cd8ef14007c3961ea1fad253cd8b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10295112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fbee9a11b4f80e085a927364bccb2594dddcbd4c3a25ec359c1bd422bbe593f`

```dockerfile
```

-	Layers:
	-	`sha256:f50e123a0a7c6aac69bbab7452327cff4e8c06ddbf35465e7fc4fb93b1e8ddb4`  
		Last Modified: Mon, 21 Apr 2025 23:31:17 GMT  
		Size: 10.3 MB (10267915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:091068107add86705c145c063162214d5e9d89e5f29453d116098dbe19c357ef`  
		Last Modified: Mon, 21 Apr 2025 23:31:16 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; 386

```console
$ docker pull golang@sha256:d67b0ff8f6c3cb7d6e596c3a9ac3101058829d6e448e2a5e80b0f6ffade2523f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.5 MB (339468795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c218651a37050698111796b69100fcc423ff429ea73179855c6d27fb5b2d538c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 21 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 21 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 21 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 21 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0606c6e417e3f273e94fb33ac515dc5e3bacfec2558aa1e3ab7b9413dd31655c`  
		Last Modified: Tue, 08 Apr 2025 00:23:00 GMT  
		Size: 54.7 MB (54684465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ffef4e17cbc252fc170472ff3910647beec8b91ac9abe188d6595b2087a0dc`  
		Last Modified: Tue, 08 Apr 2025 01:24:12 GMT  
		Size: 16.3 MB (16267037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684d7ac3a47d27aefe42d135394e4d8b703fb530ab3bd2ad6ef78b8c9beaf885`  
		Last Modified: Tue, 08 Apr 2025 02:13:59 GMT  
		Size: 56.0 MB (56047217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed15810a6d8906e32b01ff8d087a97f7395fa9447ef7e6571fcf6e98974b75f`  
		Last Modified: Mon, 21 Apr 2025 22:37:53 GMT  
		Size: 87.4 MB (87426441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22385500e9d61ec2b239f5d3bd81241409c720a3ebb2a4cf2d458346f64bcc50`  
		Last Modified: Mon, 21 Apr 2025 22:37:44 GMT  
		Size: 125.0 MB (125043477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbc7117e27eac0e7bd61c0ae7b9a7f74e2200394f7ca8576be8ee5391852eef`  
		Last Modified: Mon, 21 Apr 2025 22:37:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:7a43c1962268fc33d91609acaeb3c43d683e47dbd19887585f20c7afd96c18dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10283161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73b8bb9031f9da7fdd0c3d15afe102c420e3a1c426fe294b611a4efa3985413c`

```dockerfile
```

-	Layers:
	-	`sha256:4c15039d3662781f32549e292338248a9735823b2c2164eebb651464b36d049f`  
		Last Modified: Mon, 21 Apr 2025 22:37:51 GMT  
		Size: 10.3 MB (10256134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ab3a264ac6de3e096ba83608f06e6b67f6e5de702cc7d98cddf03e5a98c1dab`  
		Last Modified: Mon, 21 Apr 2025 22:37:51 GMT  
		Size: 27.0 KB (27027 bytes)  
		MIME: application/vnd.in-toto+json
