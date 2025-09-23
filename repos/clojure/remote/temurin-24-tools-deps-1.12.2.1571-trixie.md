## `clojure:temurin-24-tools-deps-1.12.2.1571-trixie`

```console
$ docker pull clojure@sha256:d67dfbb5fa710368b5ae4bb80d3bb4768f71e0e31f7207e86191dc7eef37eb10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-1.12.2.1571-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:514de9d2a9605b7492b94e8f112475d115abc1ba26c8ef4fdd92617a43f44f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224788255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ce81686a22f0cf526c8d794986fc6e553baeb30bc2dced90793009e24530f3b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:15b1d8a5ff03aeb0f14c8d39a60a73ef22f656550bfa1bb90d1850f25a0ac0fa`  
		Last Modified: Mon, 08 Sep 2025 21:12:52 GMT  
		Size: 49.3 MB (49279531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda7b96e53d3336d914001e0800014788858c916bcb66c417653b7c34f247d17`  
		Last Modified: Mon, 22 Sep 2025 23:47:24 GMT  
		Size: 90.0 MB (89975197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3b68d5814949801a365a0bedc942282ed8860b4b4be54cb4308fe351a9637d`  
		Last Modified: Mon, 22 Sep 2025 23:47:24 GMT  
		Size: 85.5 MB (85532484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a12b542aba2fc9dd40af1205c4e6e6ac21be57301b7b0a3d8a3df2593c7bce`  
		Last Modified: Mon, 22 Sep 2025 23:47:16 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f73bd2ea5533fcad21f9ba4dfbefebbc560d3c7387f1136d9fe07ff40513d8`  
		Last Modified: Mon, 22 Sep 2025 23:47:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1571-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:206004e93a026e47f31f1469aee214108b07c27e3b211b44d388bcd5043fb799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7433283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f5857377a6e848696f6d61c0fa0e7637727b0ca64a2fe593eed64833bd6fea`

```dockerfile
```

-	Layers:
	-	`sha256:f67c585cab1a791ae31cd7de4d803db5d40ac6c9665fb98cb762b5f1169a128b`  
		Last Modified: Tue, 23 Sep 2025 00:45:26 GMT  
		Size: 7.4 MB (7417493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e71b8f401fbf2d32e0b30a8d5cea92407ebba9d888ff678f30126b4a46433f7c`  
		Last Modified: Tue, 23 Sep 2025 00:45:27 GMT  
		Size: 15.8 KB (15790 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.2.1571-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f17304da11d1039faef75ab268bd776e3ecdf43945ccdf5009baa8e331527341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224096308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43cc7a3f5f7387acd7257e22eecea08f4e9c11d7578273ba5d03901238dc5b6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:37b49b813d9cadbc816aea22a15ef76898c66b4db015fea88b8f15bf213d5004`  
		Last Modified: Mon, 08 Sep 2025 21:13:28 GMT  
		Size: 49.6 MB (49643746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef88509a56402482ab6fffd0ffc7ba4732f49617f9364b25186feb8f8a44aa07`  
		Last Modified: Tue, 23 Sep 2025 02:09:18 GMT  
		Size: 89.1 MB (89092491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93993442cc6899707bf9724fb1996bc0963e10a70d20df714355f73c9700bad7`  
		Last Modified: Mon, 22 Sep 2025 22:22:05 GMT  
		Size: 85.4 MB (85359028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d248490b025d24e8383c4360a0ff57481099b4c0fa90ef64c4923ecd0bf5382e`  
		Last Modified: Mon, 22 Sep 2025 22:21:55 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84f120435eb8beddcc659c3f163874812c14077adba8c06b361fc3459fe5e1f`  
		Last Modified: Mon, 22 Sep 2025 22:21:55 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1571-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4e39e9679db219c80e5c14708e81432fa42451de1ec5ad759394af03bd5570f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7440428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b166e2d8bd465f8c8dd511d20aadf6bc5305be0dcc5975f3658fb5bd4c48612`

```dockerfile
```

-	Layers:
	-	`sha256:bafc3826ab5e481fb4df3144dc019af086e770a4b5da3016704b384ba99f474a`  
		Last Modified: Tue, 23 Sep 2025 00:45:33 GMT  
		Size: 7.4 MB (7424520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eddc1574f99956762b95b6042183ee31061dc7f57fdedca7a78794ebc9be8afe`  
		Last Modified: Tue, 23 Sep 2025 00:45:34 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.2.1571-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:9cbbc8ab7aac6c7ac9b34dd9c89d766d5dd7d770570cd09a488028e5d6c5b08c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (233977956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc6ff7c8694020771b231b76abe6e8e02ba148cddf5d7f0633901eb879fac8a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4cb8224e7ffc22512c71f1cfc1042cb22342df02312e61cb1ab0c492c3369711`  
		Last Modified: Mon, 08 Sep 2025 21:18:07 GMT  
		Size: 53.1 MB (53104433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5b739094a78d48c0bbc7fb63510f63ad98a27b361a087db2310996e81c516f`  
		Last Modified: Sat, 13 Sep 2025 03:54:37 GMT  
		Size: 89.9 MB (89918174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d9bef45b2eff87727965fce7d3abe6c3942b61ff241911a80b713106b2491e`  
		Last Modified: Mon, 22 Sep 2025 23:29:07 GMT  
		Size: 91.0 MB (90954305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fcb36985c555f69363605bb3fd3a24c901324d3da659c8f60e4a2d33fbb408`  
		Last Modified: Mon, 22 Sep 2025 23:29:00 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177909dba246acee4a418b1b01e97414ea5db69db9f1c43a0f6419f2d2b4588a`  
		Last Modified: Mon, 22 Sep 2025 23:29:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1571-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:40f516cc37023f3b47334ba9a2c319f3091cf0a4e6ce00aa7e0b5761623fd09e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7439048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0125991f96dde1f0b2e4fde4dd71184c1e2aefaae18b49de4d12308c0ba7625c`

```dockerfile
```

-	Layers:
	-	`sha256:34b0ee8628a39b93ebedd4408f69eb58dee5507530a3cb7d7017da4f6c2ea87a`  
		Last Modified: Tue, 23 Sep 2025 00:45:42 GMT  
		Size: 7.4 MB (7423210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02352909235a6b5d2d5797fe81ce65eeee1d718722e18297da30eb46c90b639b`  
		Last Modified: Tue, 23 Sep 2025 00:45:43 GMT  
		Size: 15.8 KB (15838 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.2.1571-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:9e930344150c3c4064c822f11b2fc260fab5185a21c74d9240bfedefb2b5af6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.9 MB (219864760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32caba49554e234041a951fe3f65f9af371f98f242c1b09966bb681a6fbd347f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8f913be5ecadf79e3ee9792194aaab366421c7e066487d572f285b293ff78a7a`  
		Last Modified: Tue, 09 Sep 2025 00:25:27 GMT  
		Size: 47.8 MB (47765447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7d189ceacdc7f5da0211b697db9d729111f59e6d463a6da7206d9f465b3934`  
		Last Modified: Sun, 14 Sep 2025 00:31:09 GMT  
		Size: 87.7 MB (87670426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae33bb161f31fbd74eec8b6a9a783d76bbac5cbfeb27f418ae404d338b0ca4ef`  
		Last Modified: Tue, 23 Sep 2025 01:16:31 GMT  
		Size: 84.4 MB (84427841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421bc820f8c385c0061c0ca2d55fc0bc47e444b473a1164b1411fb623011bab0`  
		Last Modified: Tue, 23 Sep 2025 01:16:15 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d00ca1e16c03f126977b9df2f887899b987fa5dd29e24c5333be63c7850e05`  
		Last Modified: Tue, 23 Sep 2025 01:16:15 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1571-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c1a713ff3d2e7d67e970a138d505b28343cb2bf0043e7be4824c36ded2698a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7421241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b7d07766899e4683a00b4406a3028e7fe1bdc1254884bc0cba03a2a75b08f9c`

```dockerfile
```

-	Layers:
	-	`sha256:a7f3d1979f027a3f0abdfd7befa8ff8ecdb39389d79b9632acb257b89be22a41`  
		Last Modified: Tue, 23 Sep 2025 03:37:57 GMT  
		Size: 7.4 MB (7405403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:947d2d4ee864d552c4c3aef08d01c291497d5de8cb131c892c54ed4c7c9f6b1a`  
		Last Modified: Tue, 23 Sep 2025 03:37:58 GMT  
		Size: 15.8 KB (15838 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.2.1571-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:cba60a2bc78cf09e51551595d07d127fcdf688a42559bd27ae0bf4d7b05cb932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221082470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f5ba68153567aebec957e69bb2618a138ca223981ce464a25b607be948bf728`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:28eee642962fd09c10ecf87da2d4b65d208f3d5c1bf3fcca21c105c0213f558a`  
		Last Modified: Mon, 08 Sep 2025 21:32:18 GMT  
		Size: 49.3 MB (49346327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e09349677796a376b1cf6d7ed472d5ab8acf54c67c758a17004a2a4e5cc7fb8e`  
		Last Modified: Sat, 13 Sep 2025 03:20:43 GMT  
		Size: 85.2 MB (85226397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a113c13d997437d27875408cddbdd29c67651bbb320d6a922d19864daefa341`  
		Last Modified: Mon, 22 Sep 2025 23:23:00 GMT  
		Size: 86.5 MB (86508704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4351f48b674be20d0a3093e907946d32deec0b26b1ade977f5604184c685d8b`  
		Last Modified: Mon, 22 Sep 2025 23:22:54 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9c358abcde450cd0a421da488eef4e36b916e16b0907cb4ea6b729a9c170ab`  
		Last Modified: Mon, 22 Sep 2025 23:22:54 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.2.1571-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1808c0aa13246419308d189100d39ca680ec24b2ed030d5e11c6973e3650a24e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7431752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9782734a7271ccdba2c54aa9ac66506ad32f72414290713906b0bdcfaeb30780`

```dockerfile
```

-	Layers:
	-	`sha256:0f74e7e07e7b9980e2ca0337e0380d03766bb986b5ac6e192953dad68320a30b`  
		Last Modified: Tue, 23 Sep 2025 00:45:49 GMT  
		Size: 7.4 MB (7415963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49c6e3f9eb6f79cf6c1910f1cc0ea12facc586efc05fe8cb75eb979beb72b96a`  
		Last Modified: Tue, 23 Sep 2025 00:45:50 GMT  
		Size: 15.8 KB (15789 bytes)  
		MIME: application/vnd.in-toto+json
