## `clojure:tools-deps-1.12.5.1654-trixie`

```console
$ docker pull clojure@sha256:50288bd3bc9f1e1d2fda2d0d4df4d9afa7b3363a3c0d433b41e5aea08832149f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:tools-deps-1.12.5.1654-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:cb5c5d6649a6f36aab3144f1ef6760e6b5de5f327d349b0ddd41059d10d9e9f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.4 MB (224403692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3118f5c687d1e0e85783e213f796467e6ba9983707ff5d290ef4d23bc13d0a70`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:47:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:47:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:47:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:47:29 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:47:29 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:47:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:47:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:47:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:47:46 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:47:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:350fe9befa119b4116fe693fb88baf2ada42211da07b656c5961b19ee878ee9a`  
		Last Modified: Thu, 04 Jun 2026 17:48:06 GMT  
		Size: 92.6 MB (92574585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c99198b5210a1d06e6897089bfcd9505cc795a92e60bdb1d76088ba0e9a4f4b`  
		Last Modified: Thu, 04 Jun 2026 17:48:09 GMT  
		Size: 82.5 MB (82517442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc524d9db15c2c00bc9b299c9fb2a2bb6f66d13b6c751f417c0c864d8781619e`  
		Last Modified: Thu, 04 Jun 2026 17:48:06 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d836ba51438ae1f752b3dafd1ebcaca5c4a5631b8f85a3de34d2dfb49f8bec`  
		Last Modified: Thu, 04 Jun 2026 17:48:06 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.5.1654-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:02a7def82be3b323553bf4256c60863ae924d67f3f0b898b230792df48668931
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7453402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f650a926ee25a2c63a9a38c3ba8957083d84cc26bc5098efcce056996590ced5`

```dockerfile
```

-	Layers:
	-	`sha256:2bfa878bd608ff4601f9809f4be867f6b48b6c68412af323548c863dacdad5ea`  
		Last Modified: Thu, 04 Jun 2026 17:48:06 GMT  
		Size: 7.4 MB (7436833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a48f9b16f9486023b119a315f8edf2ee43833da982ce8447e9db6c1a38feffa`  
		Last Modified: Thu, 04 Jun 2026 17:48:06 GMT  
		Size: 16.6 KB (16569 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.5.1654-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2ceff24faa0cd0d7a0546f13fd36d28f8a20ade6b7b3b600623dc20e6c02d5c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.6 MB (223553875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae105079a8f8df5fba4c9fb1c3fc56bb9defe2ce5ddc4b1ddb02ae000f26d961`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:47:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:47:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:47:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:47:25 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:47:25 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:47:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:47:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:47:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:47:42 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:47:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8541aaf19d6003da3b96eaf8bb29fe8d984fb85cf9f473317a1422e264dde8b1`  
		Last Modified: Thu, 04 Jun 2026 17:48:06 GMT  
		Size: 91.5 MB (91542280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ff83af7903345c5bc74d0b6ec2cb73bfd975b6f6bee1f28e226286bec798fa2`  
		Last Modified: Thu, 04 Jun 2026 17:48:05 GMT  
		Size: 82.3 MB (82338333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac3932974732a8afe5eeb5f2d4a2e2d0b63e65b76e4e25b51b9d8b726197c94`  
		Last Modified: Thu, 04 Jun 2026 17:48:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6efcd6caf5e155cb2646f663332004e8002299355cd19093a7c01ba60422ab1c`  
		Last Modified: Thu, 04 Jun 2026 17:48:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.5.1654-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8bd7a9987c1ea93d72769fa5ad0cf3f95c9426f8683875a42195b4cbc1c686c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7459958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de10efc30b70c4a70293c57247041d81edfe033efd01275fedba4f54a9bbb16c`

```dockerfile
```

-	Layers:
	-	`sha256:13ff485b10904b7b459a68b78d0be91411231e2fb611fd2db5635a40f329d1a6`  
		Last Modified: Thu, 04 Jun 2026 17:48:02 GMT  
		Size: 7.4 MB (7443247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b904d2d96934b8588c471acb0e4b3d30550425c9085ef0978f4a39fc4bf62a0b`  
		Last Modified: Thu, 04 Jun 2026 17:48:01 GMT  
		Size: 16.7 KB (16711 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.5.1654-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:fbb5cac016cdec65476eca9c40f910852aa31908a3950698e53a0d2f05ade93e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232985237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0be6e4943940871cd107a2569f78bf3bf674bcc31903c4521fb410478f101c52`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 18:06:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 18:06:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 18:06:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 18:06:36 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 18:06:36 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 18:07:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 18:07:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 18:07:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 18:07:26 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 18:07:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:55497c62a793e62a2e78a3fd85fcedf060da73e331ad107733199ea991106b96`  
		Last Modified: Tue, 19 May 2026 22:37:59 GMT  
		Size: 53.1 MB (53132182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1525d5045df9660d1c5f453aabf32cfbeb82239dce10b64e81ec9ff422c41e`  
		Last Modified: Thu, 04 Jun 2026 18:08:14 GMT  
		Size: 91.9 MB (91914038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f380e52b3300e5add503f81d30cbd0d58c45f73c928f58499d6eb2e4ebc542d5`  
		Last Modified: Thu, 04 Jun 2026 18:08:13 GMT  
		Size: 87.9 MB (87937972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dd49354089fd1918b589b3ef775e15da1a3f8799e8c3cfda5014ef8d1c83ac`  
		Last Modified: Thu, 04 Jun 2026 18:08:09 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f39ffa7600ddfef43326fd93c7aa6e9b3a9da170291b1a879dfd889fb6a971`  
		Last Modified: Thu, 04 Jun 2026 18:08:10 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.5.1654-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1e90fac4d61957319bde84fb0b44c8de88df740310a1476f96b84ff20c4840f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7441207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:591051e6af2a42c1521e2eccd41da313d13bd2705ca7e8a507f64c158113d05b`

```dockerfile
```

-	Layers:
	-	`sha256:a2efd5386d91986778f7f533f54226aa1161d653d43702abc962367b4eff274c`  
		Last Modified: Thu, 04 Jun 2026 18:08:10 GMT  
		Size: 7.4 MB (7424578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1711428c4127436c0fc0d011f2abd4ba6dc6a08adc2181cba16d91e21fb29fa`  
		Last Modified: Thu, 04 Jun 2026 18:08:10 GMT  
		Size: 16.6 KB (16629 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.5.1654-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:79d287d82ffb07f4354cb336334b26a2b838bf51eae5e4baf6214d96cf5f7e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.3 MB (221303329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4a45ee98ec3bbebb3031c980c1a864d172204403f0387493551ceaec9ca98d3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:46:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:46:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:46:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:46:32 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:46:32 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:46:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:46:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:46:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:46:50 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:46:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1540dbb0587ae9097c9d04c50809503aa74d42814940d640c6659645acc0bc6c`  
		Last Modified: Tue, 19 May 2026 22:37:00 GMT  
		Size: 49.4 MB (49379780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef6169311977cc32a02b67f36955ec08c2a6656a54c75d96ff0469aace3def5`  
		Last Modified: Thu, 04 Jun 2026 17:47:21 GMT  
		Size: 88.4 MB (88420320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ed932c173a1b5fc086ae9952605b8a08ff1114161873a3bd83983724a77daf`  
		Last Modified: Thu, 04 Jun 2026 17:47:21 GMT  
		Size: 83.5 MB (83502182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf53f70439542721a5d0b829d39ac956b9f724a12b9bb1599a29b97f87ec39ba`  
		Last Modified: Thu, 04 Jun 2026 17:47:18 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f27ecbaade4e479fc64f38d7311356e11611ebb3f2207fcaa6a7860cb59ed30`  
		Last Modified: Thu, 04 Jun 2026 17:47:18 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.5.1654-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ca87c44db72fe8eea59e8f20440c91c9a4d136db8693cad43b32197b12cf915f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7433886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036e49e23c23b7e292f5fe118332cc62c2ce80e46ebc9a26822f58c6e7667be9`

```dockerfile
```

-	Layers:
	-	`sha256:2fac8ba44e5a94485e858b7de1adf58f1fd34b51b354f7034e66863b76c7d2a7`  
		Last Modified: Thu, 04 Jun 2026 17:47:19 GMT  
		Size: 7.4 MB (7417317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f62f243a605ed575317dce5e52c2d1a13ecd3bcac6eef73d0fd4ea4281ddad0`  
		Last Modified: Thu, 04 Jun 2026 17:47:18 GMT  
		Size: 16.6 KB (16569 bytes)  
		MIME: application/vnd.in-toto+json
