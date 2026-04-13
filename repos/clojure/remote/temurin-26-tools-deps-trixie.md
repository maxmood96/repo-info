## `clojure:temurin-26-tools-deps-trixie`

```console
$ docker pull clojure@sha256:873bea92bd6493eacc66a28ed7e2fc07e8a56084a9dc79e0dae8660ebf84af4b
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

### `clojure:temurin-26-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:19d8e0e1e170d386e4e1527520824cdddc274e4542626067cadb17d477d39be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232836443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ee330759683a4ec6cad813594b3b9738b29520a330316e0940679e71b79507`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Thu, 09 Apr 2026 23:37:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Apr 2026 23:37:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 09 Apr 2026 23:37:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Apr 2026 23:37:28 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 09 Apr 2026 23:37:28 GMT
WORKDIR /tmp
# Thu, 09 Apr 2026 23:37:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 09 Apr 2026 23:37:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 09 Apr 2026 23:37:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 09 Apr 2026 23:37:45 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 09 Apr 2026 23:37:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ee3f2cd1841f34a437c48ed04b58e918164909f475add21bac50c8c8768e28`  
		Last Modified: Thu, 09 Apr 2026 23:38:02 GMT  
		Size: 94.5 MB (94455682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910aa2f21734b4e8e5371acec40166a642b969a2eccb3ae984fb329cb951387a`  
		Last Modified: Thu, 09 Apr 2026 23:38:07 GMT  
		Size: 89.1 MB (89081885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b221d347d87e94524ea7b9fdd909637516d5e639a95fcb2a769b279f1c8ff00b`  
		Last Modified: Thu, 09 Apr 2026 23:38:04 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f18c3dc8d838aac6ecfa05e570bfc7acc59c290f262a7ea35afa038574cb23`  
		Last Modified: Thu, 09 Apr 2026 23:38:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d2398d1ef21ecad59eeb930e33cf1b485e9079fe822d58b56cb5ff9f18f8212f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7451918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b45ffc3e8b2438cec619341aa54679344208078311c9be6f6f98cf369daa201`

```dockerfile
```

-	Layers:
	-	`sha256:3aa904421814b476aa9010b86f0b9d71da96b199c7da79490e5d3c4492353960`  
		Last Modified: Thu, 09 Apr 2026 23:38:04 GMT  
		Size: 7.4 MB (7436171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdd6a93c4e8b31cb802f5905682f0e5cc68c5d73846e1d9eac3f51fa110dc21e`  
		Last Modified: Thu, 09 Apr 2026 23:38:04 GMT  
		Size: 15.7 KB (15747 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8baa0c1fe14cee5f5d076c1c9f043aff75a2ae66a6a90a195fcfc83633f96b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232315163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e27e9e0e5219203094dc6f79918885efd9b48ace0eb0c1017ab748ab99f14804`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Thu, 09 Apr 2026 23:37:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Apr 2026 23:37:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 09 Apr 2026 23:37:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Apr 2026 23:37:14 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 09 Apr 2026 23:37:14 GMT
WORKDIR /tmp
# Thu, 09 Apr 2026 23:37:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 09 Apr 2026 23:37:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 09 Apr 2026 23:37:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 09 Apr 2026 23:37:32 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 09 Apr 2026 23:37:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adefceacc28c17596cd2b04f72192fe4ed709420c925e155e2f2a3bc5256df5c`  
		Last Modified: Thu, 09 Apr 2026 23:37:54 GMT  
		Size: 93.4 MB (93395164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:900de000b0f05d74300b23ec34c707a505cbae8708e530353e902cc7f3379ca7`  
		Last Modified: Thu, 09 Apr 2026 23:37:54 GMT  
		Size: 89.3 MB (89253699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296007c959227ef5bcc07a4f379069ddc62f8a0f03211ff8f373a7ed064d35f3`  
		Last Modified: Thu, 09 Apr 2026 23:37:51 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3adbac1d4c65889256716ace24fcad2dc300ad6f7d49d49dc38df9052cbc0ac3`  
		Last Modified: Thu, 09 Apr 2026 23:37:51 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:908c7c9581894a1521c2d74324acaf3745a503ee742a0960d2adc32fdefc2656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7459063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50331d404c25300ceb7d5aeb298d77e7ceff1a23b0badc001492967b982e27f0`

```dockerfile
```

-	Layers:
	-	`sha256:a2d7945b7fe5030ae1ac2555a516e6f4deb9a58aafade5f55602647a856d28b6`  
		Last Modified: Thu, 09 Apr 2026 23:37:51 GMT  
		Size: 7.4 MB (7443198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:689a0d11d5bd98ed29f256af456112f214c3c295257b545d9581b00cffc2c8c3`  
		Last Modified: Thu, 09 Apr 2026 23:37:51 GMT  
		Size: 15.9 KB (15865 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:0907464c8df3cd5cf629fe52315c8612646d235ea3aa026899240b2c29474dd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.6 MB (241623565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8afe13a4362078a7cf0d98f867d74559f3874f85779b6698e125b9af7f02d13e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Fri, 10 Apr 2026 00:52:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 10 Apr 2026 00:52:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 10 Apr 2026 00:52:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Apr 2026 00:52:59 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 10 Apr 2026 00:53:00 GMT
WORKDIR /tmp
# Fri, 10 Apr 2026 00:57:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 10 Apr 2026 00:57:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 10 Apr 2026 00:57:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 10 Apr 2026 00:57:23 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 10 Apr 2026 00:57:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dfcead13693a6857ab51b621e372876765c71adf46e88c3448e530a15832886`  
		Last Modified: Fri, 10 Apr 2026 00:54:22 GMT  
		Size: 93.8 MB (93781469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22186d8ac29b0b2af7f835c8bb05c3caeed1a6b7e2cb5e1edcc000e6be99b8e`  
		Last Modified: Fri, 10 Apr 2026 00:58:05 GMT  
		Size: 94.7 MB (94722382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cc08ab0b0863771c35799cb1d43a29ba96c4144d1f7011fd03fe61546e2cf7`  
		Last Modified: Fri, 10 Apr 2026 00:58:02 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19986828ab8b1f3264659aeed9cd5d1d8a035591c55dffab66c7416e31b7bf1b`  
		Last Modified: Fri, 10 Apr 2026 00:58:02 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8bc2df7cde2e00a820dd5cda26f7beecee979b864cfda7faeaf8136d18af73ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7440322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c918b29226bab2f4fa96c06465f16e13e69e0de931c8f1a708a2a7cf7f47dca5`

```dockerfile
```

-	Layers:
	-	`sha256:3f1bfd5ed3f25c109c6f73a498e4826b718ffdd3563da69b072a515152fdad4c`  
		Last Modified: Fri, 10 Apr 2026 00:58:03 GMT  
		Size: 7.4 MB (7424528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c94c955673c7b8bcbfbb31736309d98226d4179d3250dfaa93d6b06fdbd36c33`  
		Last Modified: Fri, 10 Apr 2026 00:58:02 GMT  
		Size: 15.8 KB (15794 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:2422eb8796137e505969917bb8de7cedec20a84860e11258a05e7999976b4ddc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228433085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d954564f23d1be70e9d7ab78236d23df66de9d25ec0e92150c442398d91e4af`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sun, 12 Apr 2026 18:49:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 12 Apr 2026 18:49:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sun, 12 Apr 2026 18:49:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 12 Apr 2026 18:49:16 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sun, 12 Apr 2026 18:49:16 GMT
WORKDIR /tmp
# Sun, 12 Apr 2026 19:11:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sun, 12 Apr 2026 19:11:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sun, 12 Apr 2026 19:11:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sun, 12 Apr 2026 19:11:09 GMT
ENTRYPOINT ["entrypoint"]
# Sun, 12 Apr 2026 19:11:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3e61abfb88ee12dd42b3c32c20825f42c0eae3286fe2a9301e326413688c3d40`  
		Last Modified: Tue, 07 Apr 2026 01:54:08 GMT  
		Size: 47.8 MB (47792626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90d8e4f2f94de58856173d1d55466c632c6602bdea8fc895ac0398eaddfdb2e`  
		Last Modified: Sun, 12 Apr 2026 18:55:02 GMT  
		Size: 93.0 MB (93008107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d013d6c9d666bc6e390fdb5a870bc359543c4cc0e4c2da351e27a1652e887f`  
		Last Modified: Sun, 12 Apr 2026 19:15:30 GMT  
		Size: 87.6 MB (87631307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1428db3a608fec01678edd50662e1b6cbea33b268877893078bd6d9c50e0fdc0`  
		Last Modified: Sun, 12 Apr 2026 19:15:16 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f899273360954c29f37f65df4ac45f50a5e8240bd892757116f1486b6c310fe`  
		Last Modified: Sun, 12 Apr 2026 19:15:16 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:db12d8b89d0b3958bec692fc70093a5b36b05d03c8a84245f0fc931ac4b95bb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7422516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f532555c74b18b4d306796a811f2a6702cbdbfcbba73259504fa1d9f86d83389`

```dockerfile
```

-	Layers:
	-	`sha256:3675add79a67d1c6a6e86a3392136b481368dad30846d18cd4e3332d3a8f5b31`  
		Last Modified: Sun, 12 Apr 2026 19:15:18 GMT  
		Size: 7.4 MB (7406721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7ea183f41df025f0f789c1024400575d6d59a37d121fb8ba4141f9e949c41f2`  
		Last Modified: Sun, 12 Apr 2026 19:15:15 GMT  
		Size: 15.8 KB (15795 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:a77d8711278307b00ccb29a84d0222832894725c64952a9a87a1d8a71c4ee432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.6 MB (229624354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667aebb0f1196fad4a8fe1943914efb21aff62e7bc7c36e048f0d3193f3d8f41`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Thu, 09 Apr 2026 23:45:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Apr 2026 23:45:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 09 Apr 2026 23:45:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Apr 2026 23:45:23 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 09 Apr 2026 23:45:23 GMT
WORKDIR /tmp
# Thu, 09 Apr 2026 23:45:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 09 Apr 2026 23:45:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 09 Apr 2026 23:45:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 09 Apr 2026 23:45:45 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 09 Apr 2026 23:45:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:99ccdb9e0b0ce79a36cbcc433fd972b049c1e4e84d217954de0e89224b1fb094`  
		Last Modified: Tue, 07 Apr 2026 00:13:49 GMT  
		Size: 49.4 MB (49365104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ccc9384a3516894cda80cf7c376f24672d63213432c362fcc78f0d0126929f8`  
		Last Modified: Thu, 09 Apr 2026 23:46:16 GMT  
		Size: 90.5 MB (90547699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7efddfb50bac93e7e6398a131df7c6a722ef89526e149dedd8dd4aa59af6f4e`  
		Last Modified: Thu, 09 Apr 2026 23:46:17 GMT  
		Size: 89.7 MB (89710509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ed73bf9785d56cb42d8741f7d1f08071d9a552e54ac3078e1c825b8cce01a1e`  
		Last Modified: Thu, 09 Apr 2026 23:46:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195786e757d7b839159bf0e7cf64c9e873276967ffcdccba80431212915ea3c5`  
		Last Modified: Thu, 09 Apr 2026 23:46:14 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:753530b1716f0a61a289fb7b7490c9dae63707bfc3282a2f99fb934e64b27dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7433026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e37d218f689598d8bbd0163bf2d9bf5ca874a2086849a34d082b1e2f0bfce8e`

```dockerfile
```

-	Layers:
	-	`sha256:bebf64d7985d1132a0b2f7a379638d453478a3d5fbf61d0e349e2f6db7669f48`  
		Last Modified: Thu, 09 Apr 2026 23:46:14 GMT  
		Size: 7.4 MB (7417279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ae242669a9ec4ededed4f62470fabde50440392e61c8c248b0c47ae7a76f424`  
		Last Modified: Thu, 09 Apr 2026 23:46:14 GMT  
		Size: 15.7 KB (15747 bytes)  
		MIME: application/vnd.in-toto+json
