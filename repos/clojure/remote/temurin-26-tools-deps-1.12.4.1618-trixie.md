## `clojure:temurin-26-tools-deps-1.12.4.1618-trixie`

```console
$ docker pull clojure@sha256:2007bbb63933bc0663d5d18fb744076ae24007f63ce32bb331ca180a7f497bff
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

### `clojure:temurin-26-tools-deps-1.12.4.1618-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:82ed4ab79cf7bd72d4e5365eb2484c7b39ca7d226768e33c343c926cf6f66435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232834907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808d32138837c5db1a2c1cae7c3e410497c1a5ebea3b38b899298c354a4816be`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:08:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:08:03 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:08:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:08:03 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:08:03 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:08:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:08:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:08:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:08:21 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:08:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fdeb2304bfd7c482d3d846cc816963e6cd1d4d3c36a3154908b6a9683b1695`  
		Last Modified: Wed, 15 Apr 2026 22:08:42 GMT  
		Size: 94.5 MB (94455682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc63994900d8d509a2733b97382871f11515842ac1d955e0512ebb5eb712c0d`  
		Last Modified: Wed, 15 Apr 2026 22:08:42 GMT  
		Size: 89.1 MB (89080349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d35ef2be94b3245479df0f600ffa67b53230134ff34a9b91ea1358f1813037`  
		Last Modified: Wed, 15 Apr 2026 22:08:39 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763d0656cb823b1c8336923515441f4cfb0378936f2e11f04bdca9080933e1e9`  
		Last Modified: Wed, 15 Apr 2026 22:08:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:abdbdf15210917d035242d7436b544ff8ccc6b69d9e220dbe6e9cd6f750d10df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7451918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e263134c8c80c97e2f84b1d15c62f32e9854dbc0d34e9ea0b75297cc86e2765d`

```dockerfile
```

-	Layers:
	-	`sha256:ea7160d505d10296fa129ffaa0d5835e1145d632d765281e6426bcba5544e72e`  
		Last Modified: Wed, 15 Apr 2026 22:08:39 GMT  
		Size: 7.4 MB (7436171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f084969fd6029ccb2c75959ba4fb87810b1e0bd3afaa494594db087bd82236d`  
		Last Modified: Wed, 15 Apr 2026 22:08:38 GMT  
		Size: 15.7 KB (15747 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.4.1618-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7559415be0a583bddc3e8fdf4a77af7279d4a52090bcc05b0dd2baf47e6a7e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232314827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13256818fca6a262e0dda71ac9937123bc052d53eb7fe9fef0ff7252126d5c6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:19:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:19:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:19:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:19:54 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:19:54 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:20:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:20:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:20:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:20:13 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:20:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4bd3db078e0bbd80656f9905eee205171bcd7b7e5d26abcc3f50c749c6ad23`  
		Last Modified: Wed, 15 Apr 2026 22:20:37 GMT  
		Size: 93.4 MB (93395224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28eba6f40c8a25985c859d25923615c1ca510e3c4f9263b8c0835eb50e21257`  
		Last Modified: Wed, 15 Apr 2026 22:20:37 GMT  
		Size: 89.3 MB (89253307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46294e17b9d9e152992e01f1d3903dfd131dd6075a24fedf1391b7dc7c94791`  
		Last Modified: Wed, 15 Apr 2026 22:20:33 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d0f9e7454c593b9fb9f02515d2fe5f2303d0f82488bc49997d9c451962b0bc`  
		Last Modified: Wed, 15 Apr 2026 22:20:33 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:57d8e8ace7eaec2f79a8dce5804be3d8a0e03876590b6dba7fb52fae2b7ad0d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7459063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69774b4ecc5ccabb1c52d5907e6e6271a61bc227079dcc191bd949e2ab43eb25`

```dockerfile
```

-	Layers:
	-	`sha256:f32ea3436bc58d44e3cee114d626603eff9e5f59786a5cbe86f1dd45cc91de08`  
		Last Modified: Wed, 15 Apr 2026 22:20:33 GMT  
		Size: 7.4 MB (7443198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb6b44a487d206073e61e4b99c25bbeb304c61f0db937669aa73b9b69eb329d9`  
		Last Modified: Wed, 15 Apr 2026 22:20:33 GMT  
		Size: 15.9 KB (15865 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.4.1618-trixie` - linux; ppc64le

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

### `clojure:temurin-26-tools-deps-1.12.4.1618-trixie` - unknown; unknown

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

### `clojure:temurin-26-tools-deps-1.12.4.1618-trixie` - linux; riscv64

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

### `clojure:temurin-26-tools-deps-1.12.4.1618-trixie` - unknown; unknown

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

### `clojure:temurin-26-tools-deps-1.12.4.1618-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:8751d9a65266fc354f029d9df9789263ffc437ad8841d2f7340cda6fc8099c43
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

### `clojure:temurin-26-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2007cc8eb169170e8bb6db55bc581bfa803ec834bf8d886f9ec09063ef24b3cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7433026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acdc43df4efec94cd4b78d40a9c6fcfb44f3a35b5d7f9ebb583560ed3aeef17e`

```dockerfile
```

-	Layers:
	-	`sha256:5b1227ab20a2a0687fec6d0e1eb6d10fb8861d355d6ebccb6a83c7d227884e67`  
		Last Modified: Thu, 16 Apr 2026 00:47:44 GMT  
		Size: 7.4 MB (7417279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:992f5ae2e075b5e38587320d3d375635b5595adcf1efe340c38d7af0a1b97c5d`  
		Last Modified: Thu, 16 Apr 2026 00:47:44 GMT  
		Size: 15.7 KB (15747 bytes)  
		MIME: application/vnd.in-toto+json
