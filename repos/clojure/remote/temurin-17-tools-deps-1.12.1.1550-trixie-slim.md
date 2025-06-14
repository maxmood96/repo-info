## `clojure:temurin-17-tools-deps-1.12.1.1550-trixie-slim`

```console
$ docker pull clojure@sha256:1298f64245860cfa167813f35a6e8a137aa0395ab24bbc8a14c86cef8993fde3
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
$ docker pull clojure@sha256:5ef374f1e88e1f94ef6a1c2a797d7192a91bc43e0652e41579b8833c3439afd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 MB (245302177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1090a54bd765117c83433afd538df92cb629080812714d42bde9cab8bbd05ad`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1749513600'
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
	-	`sha256:c3306e90503bf56d5d575fca0323e4953fc66cffec788094159d11570a81151f`  
		Last Modified: Tue, 10 Jun 2025 22:53:04 GMT  
		Size: 30.1 MB (30121041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814f7774d0b60cf22bdadcce74d94c3fcb5808f2d71325882a1282b787e889c7`  
		Last Modified: Sat, 14 Jun 2025 08:36:52 GMT  
		Size: 143.5 MB (143512634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec49ec0f159ee10cdc4e8845826be88a1adbbe066d12316b06b9adc0ab124f2`  
		Last Modified: Wed, 11 Jun 2025 08:33:29 GMT  
		Size: 71.7 MB (71667461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6b8ace21f56127308cd172dd76bd401c100fa95cab2b6f47d63a940842bd85`  
		Last Modified: Wed, 11 Jun 2025 08:33:07 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7af028e413ea6ad80f373a2aa85f37f866f19ec729ab74e234b5b8a7840c18`  
		Last Modified: Wed, 11 Jun 2025 08:33:07 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1a18287e3c249ad31b73c056a18a8de54d3ce5a179732fa9a4e4226b6a23da7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5274540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:affb62169309bf446d8ab5ef0b5136a259ef73517ed7dbd712a1bcea6f68d8e5`

```dockerfile
```

-	Layers:
	-	`sha256:44abf4d30f025e7e734f4b08b9a5cf2af1e2afa00dac620b7119484044946e46`  
		Last Modified: Wed, 11 Jun 2025 09:38:52 GMT  
		Size: 5.3 MB (5258567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:065cef7d4912c6976223ad01fa83d18284dd2e6dbb87ad03d5d0c25f959b5c6e`  
		Last Modified: Wed, 11 Jun 2025 09:38:53 GMT  
		Size: 16.0 KB (15973 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1550-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:8e6de4fac7871564f6af2d438027f100bf5cac3d8f7d0dc02d310a0e3bfeb573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255098431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4e93620a6e273298d99b430d887e6ca5fb6a56546dec789aa2c28fcd1f6a99`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1749513600'
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
	-	`sha256:9851a8240d92395a99e35175026ad70b4eb50fb4e03132b209af1bf02a1fa307`  
		Last Modified: Wed, 11 Jun 2025 00:37:24 GMT  
		Size: 33.6 MB (33580925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c4960c62dfc754c594da175a4341eb4f68ab689ab613c30d1f7cc0ec35e4ae`  
		Last Modified: Wed, 11 Jun 2025 08:31:07 GMT  
		Size: 144.3 MB (144280582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0833af7a1b5ef971943bac5d50d3093efaabfc8abab7f158d8d80d9c18ccdb`  
		Last Modified: Wed, 11 Jun 2025 08:37:18 GMT  
		Size: 77.2 MB (77235878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0a68171c34188a3d7748febd6a2ee3cde3bf93a906d1b986064e5cd5c77ca9`  
		Last Modified: Fri, 13 Jun 2025 00:41:54 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:323d8f5727cd3cf04da26e1b3a8d0580cc2ba41825ba1d77989d3faa78358caa`  
		Last Modified: Fri, 13 Jun 2025 00:57:01 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c590f6837d731548ebef04eb46602ca023477bf58c165a3189336638842736cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5273072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f0a8c731f13bc66db706836041fef22feeab9a153020cb6f2deca9e6f24052`

```dockerfile
```

-	Layers:
	-	`sha256:efa4db6bcb0b7117007341af93e90cba59992c5a361ebb72ca4f8bf6b3085bad`  
		Last Modified: Wed, 11 Jun 2025 09:38:57 GMT  
		Size: 5.3 MB (5257169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a54e9338a6deba416675be238d0310cc674b507f77977eb25345dce0aa4c946`  
		Last Modified: Wed, 11 Jun 2025 09:38:58 GMT  
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
