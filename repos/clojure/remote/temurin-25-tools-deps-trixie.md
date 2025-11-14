## `clojure:temurin-25-tools-deps-trixie`

```console
$ docker pull clojure@sha256:7c625d479c1fb37c0696a800ec85bbeff38adac0949582723cb2ae556c4c90cb
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

### `clojure:temurin-25-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:3ca07dc1c13a120482372e48f7edd6149e71daa32a1a3e600140ba35a5f51124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.9 MB (226872244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b2b0b681603d4810e1ce6bf3278a3e27fa1a1b46fc58ca377f842e7937ac7a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:56:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:56:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:56:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:56:24 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:56:24 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:56:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:56:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:56:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:56:40 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:56:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403eb0ab940aecc282775181915dd2a23a7e14bb534306d760712d5c278522a6`  
		Last Modified: Fri, 14 Nov 2025 00:57:20 GMT  
		Size: 92.0 MB (92045286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab70270d1b80999bf64cd25ff05470f9bd87851d41ac223a6f6a53f1ec1a5cbe`  
		Last Modified: Fri, 14 Nov 2025 00:57:16 GMT  
		Size: 85.5 MB (85540289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c460d92fcb75e46cc1e361e3430467f699cffb6f7fd7e3762d16d412f55eb8`  
		Last Modified: Fri, 14 Nov 2025 00:57:06 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7bd001c8b8b31051728f35ae090195b1fe1a16bf5589bd16c1848a20930a48`  
		Last Modified: Fri, 14 Nov 2025 00:57:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:04b4f65a72c845c3ba07ed62ca6da6406534ac5d83b60ae16e409a39e6b57a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7434646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d630e7b0ca6a540efa0c96a5bb4befac77f089606696b6c9418897d71aa4a61`

```dockerfile
```

-	Layers:
	-	`sha256:23b51afbe0e4450240ffbafc501b5b79c3a6baa28cc215955763301568e376f7`  
		Last Modified: Fri, 14 Nov 2025 01:48:28 GMT  
		Size: 7.4 MB (7418231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cd7c7dd375aeee0ef15fae85af080b6a034748ad61c22d96e7f66b7454892d4`  
		Last Modified: Fri, 14 Nov 2025 01:48:29 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9da7de9fb3c6d0740d5889aecd75aa467213a9c2183f848a35cef03c20303fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226067467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fcdd3c2d2fb644ee12b68ffcac5da32323f52940f3dc0b8e4d9184cebcd9f99`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:58:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:58:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:58:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:58:59 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:58:59 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:59:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:59:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:59:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:59:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:59:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2b5cad14c00ff3725ec593788264723530adb9ff6b1718c4f69ba7e81f88f0`  
		Last Modified: Fri, 14 Nov 2025 00:59:58 GMT  
		Size: 91.1 MB (91052531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0981f7fe4ba5d9fee5ccc2fdb8545f550f4477fc157bd46c47568aea8beefd8c`  
		Last Modified: Fri, 14 Nov 2025 00:59:55 GMT  
		Size: 85.4 MB (85363464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d64459861532b7f8029a5edb8f9ec0d9a8fc7595cfb0d48decda71984776b62`  
		Last Modified: Fri, 14 Nov 2025 00:59:47 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df76c40cc262c92bfdee4b2da8371071e9472b8c8225ea34d3ebfa1e8e53f849`  
		Last Modified: Fri, 14 Nov 2025 00:59:47 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:eb090cfe0c98fb060b5ba82a8a758ffa35e1bef7ea30c101aa9131f72c6df52b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7441837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37cf14bc8bfbc487b9870e1f1568bd3a39924b9fa095c8430740f4e585d72a18`

```dockerfile
```

-	Layers:
	-	`sha256:ae445458d93ff6dd75a5b04dba5849cdae4b83c78b512cd564f56f169d220197`  
		Last Modified: Fri, 14 Nov 2025 01:48:36 GMT  
		Size: 7.4 MB (7425282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9be0b07d603edf6fcabba3e1a5ac6282cdf4ec2942d66b96102347117b5a32f6`  
		Last Modified: Fri, 14 Nov 2025 01:48:36 GMT  
		Size: 16.6 KB (16555 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:6546def60c80d9adf8d79450c42594a8990cfc3ac20dabe02a80425732b4700e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235671984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:768a41ad1e0809b59b30cf0cc4f65d45dbda2dffddda208294c126282c847f02`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 21:49:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 21:49:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 21:49:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 21:49:21 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 21:49:22 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 21:57:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 21:57:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 21:57:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 21:57:54 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 21:57:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3c335bb15935da0eae5ce30111cfa6a289c813162bada9fd389d8ae5510d5d66`  
		Last Modified: Tue, 04 Nov 2025 00:20:22 GMT  
		Size: 53.1 MB (53110127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:446565adb94c3c0ddf2d551f99efb1cdfcd6ea440c7b05bac7b6b03d99ddeddd`  
		Last Modified: Sat, 08 Nov 2025 21:50:56 GMT  
		Size: 91.6 MB (91610756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471108546f957de3c053e48d3b48aedcdeda97cfce9d57cddd103c4f1e8e8490`  
		Last Modified: Sat, 08 Nov 2025 21:58:50 GMT  
		Size: 91.0 MB (90950058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85695fdb8df2b9bec2a5318896609179ac35898551c2600069ebaeb2b5996f3b`  
		Last Modified: Sat, 08 Nov 2025 21:58:45 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e8403c03940ed0ba5ef3812f2f00ba8dcac701bb0907bdc4dad0e539cc801`  
		Last Modified: Sat, 08 Nov 2025 21:58:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:23ee80680b8ba12ccac2d9c87327e7b7d9f7386797fa0cf0adf0c3e920667d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7440435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adf2e8e6a148d7dc6912a74cdc7efaa61e4a2da3ace8f249005aa48a1a05b1e0`

```dockerfile
```

-	Layers:
	-	`sha256:6508f6deda5c330c2397130d8bca27365b65d3e6a458bdf6eacda8eca5c79c74`  
		Last Modified: Sat, 08 Nov 2025 22:53:28 GMT  
		Size: 7.4 MB (7423960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a2d1e3e5155dbebbb1e267366e36863db4a74c68ec07c85eed9b2d5c9228541`  
		Last Modified: Sat, 08 Nov 2025 22:53:28 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:ff157b141966f98c8237a04d2c99097f4c5458280a8090665c3985c756c2ec64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (222951611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cc0d28a5c36e22d4f1da2d95713f4f69387199dd1bdc6899443a78e8359ebb4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Mon, 10 Nov 2025 04:31:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 10 Nov 2025 04:31:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 10 Nov 2025 04:31:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 04:31:34 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 10 Nov 2025 04:31:34 GMT
WORKDIR /tmp
# Mon, 10 Nov 2025 04:52:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 10 Nov 2025 04:52:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 10 Nov 2025 04:52:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 10 Nov 2025 04:52:16 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 10 Nov 2025 04:52:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:de6b66e2abcf55248485e438d6def9b92cf28773b7cd7896ee78f9409b6e7526`  
		Last Modified: Tue, 04 Nov 2025 00:27:48 GMT  
		Size: 47.8 MB (47770924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce920aff3ffeaa315b37b62cd44c0edec347fdf6332b121c2409c04bb3cf227`  
		Last Modified: Mon, 10 Nov 2025 04:37:22 GMT  
		Size: 90.8 MB (90752887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9c3728cfa212089d143533a0fa21dc32bfdfbfd6f464a5c0ab401abccabd28`  
		Last Modified: Mon, 10 Nov 2025 04:56:46 GMT  
		Size: 84.4 MB (84426755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e1e1ea7e27661ff0e5ae8f4a303182e008a76d7883e12f9e97c283159212c4`  
		Last Modified: Mon, 10 Nov 2025 04:56:38 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7463f69382d187ee06ae494fd7b0dfdd5f5acdae7f40187cd7374467ae2b1cb8`  
		Last Modified: Mon, 10 Nov 2025 04:56:38 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d0254dc340c8115d89bf7b60ee88c2c29bfdc3085fc154696bcf86b44fc8578a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7422628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6598325a0dfef71d2636c093f1c48953e58dd1c09991146f5c750a79b95b1a`

```dockerfile
```

-	Layers:
	-	`sha256:33b41c38317cc5426cb6aa05dd6f28ba482614cc5a08294733ca6f674464c909`  
		Last Modified: Mon, 10 Nov 2025 07:38:05 GMT  
		Size: 7.4 MB (7406153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be96c285c1edada14ea775bde9713df21b05cc644ddb80ed2377dbe2b21dfc13`  
		Last Modified: Mon, 10 Nov 2025 07:38:06 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:8c5dc763f9362b3df4db5aa65ecf6605722a4549cc5a88e4fb2ce60d131d9fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224072294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de9b2fc3785e8de6bda86a03586fa78abbea5ecf7cff204ac6973478aacb21d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 01:05:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 01:05:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 01:05:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:05:01 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 01:05:01 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 01:05:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 01:05:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 01:05:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 01:05:21 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 01:05:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:48bd359f940d437208e8579c571291503fa327e04a66a6c8d918cfe93cae2e1e`  
		Last Modified: Tue, 04 Nov 2025 00:19:45 GMT  
		Size: 49.4 MB (49352299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2a8a9fb8e930a57765ce42ae03395a4025a6a0a9e7231a907d0ce397171256`  
		Last Modified: Fri, 14 Nov 2025 01:06:11 GMT  
		Size: 88.2 MB (88210681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c76661e3348cf2d3849cfb8da7b8d0ea4f8b6b10ef62348adc4b9081ee9cb1`  
		Last Modified: Fri, 14 Nov 2025 01:06:12 GMT  
		Size: 86.5 MB (86508273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41635d7e530d7dcd21fbc02df90681995bce8f13d7f5af8b473b9b238552431a`  
		Last Modified: Fri, 14 Nov 2025 01:05:57 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f9ef295420f18fda5f94157b923d25ad06cc683a10416009c7587689eab7d0`  
		Last Modified: Fri, 14 Nov 2025 01:05:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7f2dc55fc47a5ab00717da173ee715bfa06100c100bc8dcf90b449a3d27b5704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7433116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a11e211b94213926e4f211c153eb0a64a7c74e6c77b74ce092954e999e00934`

```dockerfile
```

-	Layers:
	-	`sha256:4dd7669d9c33a2b4a873facdc4af1975c4352cb725d907dd643950607d5306eb`  
		Last Modified: Fri, 14 Nov 2025 01:48:55 GMT  
		Size: 7.4 MB (7416701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba7a13dc11feebb8331eccf53e4213849af69f4bf3a14d97608ad11310eb8b8f`  
		Last Modified: Fri, 14 Nov 2025 01:48:56 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json
