## `clojure:temurin-17-tools-deps-1.12.1.1550-trixie-slim`

```console
$ docker pull clojure@sha256:6e0cdfb03f39e17dde90c46f53e3bb38aaac2a1143530409d07f84d1ba3472af
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

### `clojure:temurin-17-tools-deps-1.12.1.1550-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3e8c9600190b6a1cc7fd13f0690b66fa45c5c8849415ee2e5d3128ff7393be33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 MB (246114531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9ef70707166f7450505f91ef669bb40d7a0c6f490a7179f816b5b07bd495fb2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6f052c0ff895d860a8f6983dcf5207c5e8ff5949529101bf68c1e92e9c8baf36`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 29.8 MB (29756816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97cbbf0a376a24830e9f4192d5a132a9d369153545803dfaa99d4e9b778b302`  
		Last Modified: Wed, 11 Jun 2025 03:55:22 GMT  
		Size: 144.6 MB (144635030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215ae7b4bad1c9c3825b75931763ffe6bae0fc0fbe745040a46065665bd5c395`  
		Last Modified: Tue, 10 Jun 2025 23:52:27 GMT  
		Size: 71.7 MB (71721643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3edeca0aff23423c7ec93856000729f38cfac393708b57a934b306c1e3af60`  
		Last Modified: Tue, 10 Jun 2025 23:52:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab217204deeeef0146b4aeaea4ed819cde29843a894cb7f13234dc40972910d1`  
		Last Modified: Tue, 10 Jun 2025 23:52:24 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f267e641cb5c457c18ab5597e76a1d3c5afe7caf2cc287dcd042c25e7a7ce0d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5268653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e283308ffa69d7c8ff8431241c5e3ab6ca4985c6e0b32e34c27211e33917246c`

```dockerfile
```

-	Layers:
	-	`sha256:5114c2d9dc7d8a8a0a0a598a3971d073e09f62ece68622ba49d0a28054c0d04f`  
		Last Modified: Wed, 11 Jun 2025 03:37:56 GMT  
		Size: 5.3 MB (5252798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de88d3ff4705bdf8969c832480ed021eb23f06dd0c0beeeb0e6e410f916acf96`  
		Last Modified: Wed, 11 Jun 2025 03:37:57 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1550-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f5c3f221300b8947166df14f7f9f77e0b7926322cea00fdb0b114e3362637e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.6 MB (248600499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46fddd64770ea0339c0e8a7cc01d5546b012e213ad1a3c01892dbeb2e3f9f27`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6098c2c9fa277c00ab580ce12bf64a9e1edf9e9139ba18ad85f3cc3063834aa6`  
		Last Modified: Tue, 03 Jun 2025 13:33:56 GMT  
		Size: 30.1 MB (30119455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92aa191031ed8a3c8712cc547eedf7bf4ab856214d4cc0076e445d91663c3142`  
		Last Modified: Fri, 06 Jun 2025 12:48:45 GMT  
		Size: 143.5 MB (143512648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf80e244821e65be1a09cbab69a3d8ee8fd7628ecc71f4003b6a027eb36f64b`  
		Last Modified: Mon, 09 Jun 2025 17:51:08 GMT  
		Size: 75.0 MB (74967355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f174435e639a44b467303a817621f43b33a79533e5b3a6b2c0c8798badad92b`  
		Last Modified: Mon, 09 Jun 2025 17:50:51 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e513901d64c8d6cc29da831fda489b66ef74c7e13697b10062a492765c4d2c`  
		Last Modified: Mon, 09 Jun 2025 17:50:53 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:aec8bc8f04abf58644c77992d7091c5efba9794302b3a5f48906545fbdb6c282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5274026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6613c3f44e23621d6f85e8686d0c1c1df8c7d8210dac732bb7b6d4dc4e0c677e`

```dockerfile
```

-	Layers:
	-	`sha256:a5473e5db78878ad87357d0b25cdb6913b8c807c4a463b56df10cc702de78979`  
		Last Modified: Mon, 09 Jun 2025 18:38:30 GMT  
		Size: 5.3 MB (5258053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:262b489a058cc74d315f9109daefd3613896f9b19033964ccc3799347eb2aca6`  
		Last Modified: Mon, 09 Jun 2025 18:38:31 GMT  
		Size: 16.0 KB (15973 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1550-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:b689ef94da55779c3df1459c3cedf57aac3a0448774ae9e33ac37625235911e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.3 MB (258264084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5182042bdff8f1d59d03fe62d8f0fd77e94685abb703597be9919556c0f3d25c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:62eecea9deba6eaccef3e829ddec51f2c540dbbb668a68816c8ce3c4b8023d93`  
		Last Modified: Tue, 03 Jun 2025 14:07:09 GMT  
		Size: 33.6 MB (33580565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe2f8a21171dd5775e8651cab944241a8c5250daaaecb5a5a99444957bad86b`  
		Last Modified: Tue, 10 Jun 2025 11:53:47 GMT  
		Size: 144.3 MB (144280520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91cdb469457f476e2bca82ad101cf74d16177ac5ede8679f17d72471c44913f5`  
		Last Modified: Mon, 09 Jun 2025 18:10:02 GMT  
		Size: 80.4 MB (80401959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830c01d4e01fcb4c5e7560215412608e17b6d1008e276319067382caa8ef61f9`  
		Last Modified: Mon, 09 Jun 2025 18:09:52 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3cc4f94d0a9b6b72c7667ea568f03f3961cd51ce361dc73add4362bde571e90`  
		Last Modified: Mon, 09 Jun 2025 18:09:51 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a3ba03768c3d1742ae87e8c9266cbf633d016c0b4bf7c559e3ed17af6291a724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23194c74eba3f15fcc0d07c5a4cf73f468dd7e968539a1cdca46cec1aa6e2e96`

```dockerfile
```

-	Layers:
	-	`sha256:957b11672d992e79a256a996d5eac2366d58acce3abb4640632a50e3c3b31386`  
		Last Modified: Mon, 09 Jun 2025 21:37:00 GMT  
		Size: 5.3 MB (5256655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40dd4de0d23feb699f0b10c9b2acd73243136f1391372b50c7fca8c4a2d7aa5b`  
		Last Modified: Mon, 09 Jun 2025 21:37:01 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1550-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:cd3e05ebe49171231970324080e13af568d100ecb6bc37fdcd8587e826b97878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237454499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af08a119ce66ce31527905a2d140c0e1916eab1aec8bbc045cd292fb2c944b4e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3a4ce3b49438d6e971d6a25501e5ee98899a309dea36cc03fae31602fe4551a7`  
		Last Modified: Tue, 10 Jun 2025 22:57:56 GMT  
		Size: 28.2 MB (28247070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801fb376cc7c8e7bfbbb65eff86597a614bb479a16bf71ae95e26d76287b1f10`  
		Last Modified: Tue, 10 Jun 2025 23:52:38 GMT  
		Size: 138.5 MB (138492460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e0d0195e6404a47994931fae896160f77b3b2689b92ec29cdeed59195de120`  
		Last Modified: Wed, 11 Jun 2025 00:07:24 GMT  
		Size: 70.7 MB (70713921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a0f3b5aadfdd8ebf42dc3248f2033341d64f4dfd1a355e216a1bee464701a2`  
		Last Modified: Wed, 11 Jun 2025 00:07:17 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47717d01bbad82f7185dc6edb9109a089297f466fc0b4a45a4faf392d0b3db0b`  
		Last Modified: Wed, 11 Jun 2025 00:07:18 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:27123053579ed01929cd055a6ba9b25e4114f2958b602ab3035a567c161c55a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5256246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b73bca59704300bd25b95c7108231391398ed7e88b5c5da9c8b65db033b0dc2`

```dockerfile
```

-	Layers:
	-	`sha256:67c6d9ab50afd5b6e41ab00636fadd4fd899916ee9796d16ab30835b9df50c35`  
		Last Modified: Wed, 11 Jun 2025 03:38:09 GMT  
		Size: 5.2 MB (5240343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87b1f23facfae214d4abc369f57ce6caa2c7df1e6c8f247216adbd1481f44348`  
		Last Modified: Wed, 11 Jun 2025 03:38:10 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1550-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:426466105f143f7d62745269c7b731901d0d9a0f6dd0ddd9b781a49cca11be63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.3 MB (237326312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f6c98972bec09c5b96c13a83527430973f8d6dfebe80c5f14d7bbc6c2d6c22`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c274825e96bcfbbdcdc116bb72e2d5d06d51048380b2fb22f400e6f9627616b6`  
		Last Modified: Wed, 11 Jun 2025 00:37:39 GMT  
		Size: 29.8 MB (29831871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c489b6c8f248781a7b1d9c7eab0f9ecfd3f9f22de710e987c15317b99f6993`  
		Last Modified: Wed, 11 Jun 2025 05:44:56 GMT  
		Size: 134.7 MB (134673559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52bd7d9b619dae466e3e9066a907104e6878744868bb93612e84e18b699fe79`  
		Last Modified: Wed, 11 Jun 2025 05:48:48 GMT  
		Size: 72.8 MB (72819844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a44e21122da289257b5924e037188120f79e2f3b9b05fa02c2e523b78ca96a2`  
		Last Modified: Wed, 11 Jun 2025 05:54:21 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d9ee86593465361b3d79fe3ccaa3a41d96f0ece7713aa2d73207a75ac845e3`  
		Last Modified: Wed, 11 Jun 2025 05:54:26 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d6afc92842421eb380147001ad3a947be633828c9839c63dec09ca59eab73310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5264576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a1b838385bdbad1f2157162f274c3befdd142e563e0feecd0ddbd3c4708c15`

```dockerfile
```

-	Layers:
	-	`sha256:df84384d81a7c289527dc10979db9fe3267bc0d35c6d3ae7b44c774d299d9581`  
		Last Modified: Wed, 11 Jun 2025 06:37:24 GMT  
		Size: 5.2 MB (5248722 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24dad06318cabb82e69ce2a1ab0ea992281eed25145da0a621c9e6d302294481`  
		Last Modified: Wed, 11 Jun 2025 06:37:25 GMT  
		Size: 15.9 KB (15854 bytes)  
		MIME: application/vnd.in-toto+json
