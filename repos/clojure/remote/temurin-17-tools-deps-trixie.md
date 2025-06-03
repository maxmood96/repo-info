## `clojure:temurin-17-tools-deps-trixie`

```console
$ docker pull clojure@sha256:137d7275ec9b0439e102b5a04d338437e5e1e7e2e8e1ae4d027357e48bf14d1c
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

### `clojure:temurin-17-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:1773882ad9301ac53d69a7b1b31af9b6e0fe3888100562820efb170f53ca3fdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.1 MB (282105644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:373976815edcf213b74cdd81bad51ed6bfebf7de380eaed1ff813578deda80d2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b8364400c35b20e530ea76455b7a73bf615b17d9d6734e0c2539034d9fe0bed1`  
		Last Modified: Wed, 21 May 2025 22:28:00 GMT  
		Size: 49.2 MB (49246908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc907fb535af3165f8b650c675f4e5b7b6462c2bf7d93861b70d1221c70bda64`  
		Last Modified: Tue, 03 Jun 2025 05:16:26 GMT  
		Size: 144.6 MB (144635023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37d3ef9d3313194dfd2835bce7602d0dfd435c3a774294e0f6a6cd53a8b732a`  
		Last Modified: Tue, 03 Jun 2025 05:16:25 GMT  
		Size: 88.2 MB (88222674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2624f29708dcac1226a4ced217e826303c28e70d8b7a43c28f04f8143bcaef98`  
		Last Modified: Tue, 03 Jun 2025 05:16:24 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd02a0f90fbc5d35f33d2a87fafd60b6f7bdd1a5cdf0a43ba4de285e91c2622`  
		Last Modified: Tue, 03 Jun 2025 05:16:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:88f75e1cca0be89004c51d182305a4beebd0555a1a293bbdee01c875fc5750a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7334213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:496ae5d20bf503981801acfe93d8a29ccd542be695f96104b884324b031cb068`

```dockerfile
```

-	Layers:
	-	`sha256:2ae00da62ca0b10643b079608d53bac4d601bbdadd3836f00ddbf59551a9bef4`  
		Last Modified: Tue, 03 Jun 2025 05:16:24 GMT  
		Size: 7.3 MB (7318416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1c942e7b0e67d87b90ce2f9ee6233fbdef347da6a44e072ae3b778233fa27f5`  
		Last Modified: Tue, 03 Jun 2025 05:16:24 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c2552dd7b4cdc195481dbe29801dff908ca96eace802a33501ce15479e66a25a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.3 MB (278307428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7588c0bc1eecec0e478cf1674e537b78779a73067d57c2b6a73bbb91a73124b4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:397826b9fe635f12caff1a603eb12c37426a5b3dc563e0adff2debff0c68a6b0`  
		Last Modified: Wed, 21 May 2025 22:31:07 GMT  
		Size: 49.6 MB (49618294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c62834179478a30cc196384b5343ea2eea0a3a82d12d33dd77571aa1f847b4`  
		Last Modified: Thu, 22 May 2025 08:23:18 GMT  
		Size: 143.5 MB (143512648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766fd0a963396468c4f388bbe8b3668e86c8b7c96ea9c602ea3b334b04befe28`  
		Last Modified: Thu, 22 May 2025 08:27:53 GMT  
		Size: 85.2 MB (85175445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5ff6e7c5cf332d915afd34b508140ce4fda8d305f0e6b436a29d1a170018a5`  
		Last Modified: Thu, 22 May 2025 08:27:50 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9999c3185cb70774d4a6914f9df451cb1007051d537b4799c72aa4144abf3e7`  
		Last Modified: Thu, 22 May 2025 08:27:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4c74c7a5f530253ebbadbf4f5183fe36a6a037ccde7e9666777eede9da2a924d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7341361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d98e293703d0c3b78b145442bd3f2f8e43fcb7bf047987ceca9cccb975c581`

```dockerfile
```

-	Layers:
	-	`sha256:325a5d9562e02c493aee0ae689f40b7f40cd7d592271d26860a33ddd9d6fb4a4`  
		Last Modified: Thu, 22 May 2025 08:27:51 GMT  
		Size: 7.3 MB (7325446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2167b11b65af93629fba3d981ab0105d776d3f8fec9f9ccb6573ae21f52a3e42`  
		Last Modified: Thu, 22 May 2025 08:27:50 GMT  
		Size: 15.9 KB (15915 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:a2643cdad76584b26af86d3d230d4523f413cc69a479361de0d8039f27a49c1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.3 MB (291319071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ab23c40c6f5a63d8308bf6429d0906bb9a49ace7aa736194ab7f8e898232d6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:25dfffa4126a91eb76c700c90bfdc9a9e15f34c7438a81f16c8a6999bbde6e45`  
		Last Modified: Wed, 21 May 2025 22:32:01 GMT  
		Size: 53.1 MB (53080544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002fd7f4fc1007a30b1949050f0ba69932c1032b69ee73e8eb4d85a1f11db273`  
		Last Modified: Tue, 03 Jun 2025 08:51:10 GMT  
		Size: 144.3 MB (144280585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2528e498efe20d304b27bff2e11b4402d62ad16a5becd6e6b8982c1fb5cf8d`  
		Last Modified: Tue, 03 Jun 2025 09:00:47 GMT  
		Size: 94.0 MB (93956902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8db28c25f8097e424c056f91343ce4f09a7c40d3b29f1fcce1ebf78a47b98e7`  
		Last Modified: Tue, 03 Jun 2025 09:00:44 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da7a2c751071e8e7bdf6234429a7042c813456a75354cc34631f1e0a2c23f12`  
		Last Modified: Tue, 03 Jun 2025 09:00:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a8a88fe803d66a56893299100b146154df0d9341b610fab8801dc28be3674669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7338678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f4701a3e5f5ed8b227d9547ceeb701ecb5ab9594c73875ed65aa24916c1db0`

```dockerfile
```

-	Layers:
	-	`sha256:aa7f07208a7df728e602a9334d14cfc26ffd69184a00801d4d7ce6393802eab7`  
		Last Modified: Tue, 03 Jun 2025 09:00:45 GMT  
		Size: 7.3 MB (7322833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcbce80cc2af663ee4545be38acd06f531e525e402b44c09af96d5a49859aad0`  
		Last Modified: Tue, 03 Jun 2025 09:00:44 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:0d95118fe2158eb034a8c69c11cdbab01725b0a5e99cb86d9b38b8884fd9b9fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.4 MB (270445913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07e2c4248350553ab43151f1ef7d32d18e66ddd0ffd6027a392187bf94d8237`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c83c5fa20952cc8610d790073e97537e7832127593042fa9c620fa910fe6f6b9`  
		Last Modified: Wed, 21 May 2025 22:36:51 GMT  
		Size: 47.7 MB (47731411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa6d609f781d308e56eefcb1110f30e4afe9c0d5fb3da3186df488fb49f4424`  
		Last Modified: Wed, 21 May 2025 23:49:13 GMT  
		Size: 138.5 MB (138492686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1dc90a3edb914ebcf7e51b0b2213312fe85db336ba91f194c1390c44863489`  
		Last Modified: Wed, 21 May 2025 23:49:06 GMT  
		Size: 84.2 MB (84220778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8839e780573c0e2db9214f35caad4d5f66081b03f3db6cfc42dbaf709fee57d7`  
		Last Modified: Wed, 21 May 2025 23:48:54 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a164e59b725eaa0f553d2f8e581adba111f21f18b439cab3c9b8a003383b2be`  
		Last Modified: Wed, 21 May 2025 23:48:54 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e89cc61b8ac40a0969802f2c53c6448bf02adfbad89521238e7ddf47bbc10e1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7320253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b9180394b8562a4366bf52ee79bee165701577f17cac7a72048b3bf59ac5a1`

```dockerfile
```

-	Layers:
	-	`sha256:fde98592b179e3f9433af1e2c013e955d5fc1f5fe9b6fee2ad30ee51c5e1de68`  
		Last Modified: Wed, 21 May 2025 23:48:55 GMT  
		Size: 7.3 MB (7304408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9df34476e8d4efac22e7ba917337d14999bf37bc290c9de2bb7dc2bd334a73a`  
		Last Modified: Wed, 21 May 2025 23:48:53 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:c0de2896385e9bc7e49e143e7d89c7b9504ce6ecd17a2a678c1ffaab1a4fc688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.9 MB (272948094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:467a053d590a171ebf7f5a6c8a73ddf7d6de94f7b58c1aef823454fa48142bc1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:71c8524b25c34592c256fbae9045d0ade48f5e9889d37c5b2190092fa9017d48`  
		Last Modified: Wed, 21 May 2025 22:31:46 GMT  
		Size: 49.3 MB (49322227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d3774d10487b032eb1a2167ed2afb6c687158159ce2ed561584cd53595528c`  
		Last Modified: Tue, 03 Jun 2025 06:16:20 GMT  
		Size: 134.7 MB (134673548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fe3e20f9bd31af05d7ec4ab08077476755c736e5b993f4e7c6065ac70d2f14`  
		Last Modified: Tue, 03 Jun 2025 06:22:28 GMT  
		Size: 89.0 MB (88951279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5233ba87ba13b06c75fea97168014ec2774f6631b4b1964fdb816c69914f77bf`  
		Last Modified: Tue, 03 Jun 2025 06:22:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfcf22bdd296ae69338128d64dd5f3d75ba274cd6fb27cc30faf35c39c6132a`  
		Last Modified: Tue, 03 Jun 2025 06:22:27 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6bf712203db6918384a08fe1dbd6c73ef89caaff6002c2094f19b704f5653c19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7330134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e17cc25b083cc9a751e81fc597399e2c156729a4e34a1a2c138a184b5810e668`

```dockerfile
```

-	Layers:
	-	`sha256:b96d13b576ff5d09cb28e5eb913f349ad05626a65575a82fa45bb0c4be4fb8b4`  
		Last Modified: Tue, 03 Jun 2025 06:22:27 GMT  
		Size: 7.3 MB (7314338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f39ea298e9c7d6b3938bc029c8185d340d4f767edf0dbf815f9c3ce84cbb7912`  
		Last Modified: Tue, 03 Jun 2025 06:22:27 GMT  
		Size: 15.8 KB (15796 bytes)  
		MIME: application/vnd.in-toto+json
