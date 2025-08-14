## `clojure:temurin-21-bookworm-slim`

```console
$ docker pull clojure@sha256:44e2e52e3ecb377837a9be8fadbb1980fa5135b6b7fdb4a4a07c5e398e1b8534
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

### `clojure:temurin-21-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:864451f09b5a05bfb89cf9707f388433dc3989980e575f466998470584a570b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.6 MB (255570414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0050f20176e092ab9bf3a398ae30aa7e56a708368327f35c35734092445662d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c251c9b5f3818b6daa2cb9183d757b8ef0b7ffb4f49fc044775bd62812b7b4e8`  
		Last Modified: Wed, 13 Aug 2025 01:28:05 GMT  
		Size: 157.8 MB (157804771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c951b4824c4cf245f1537e70f1b96e463a930720f1ddcecb43d6b6aac8acafac`  
		Last Modified: Tue, 12 Aug 2025 21:37:22 GMT  
		Size: 69.5 MB (69534350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915a4824f77ee8aed6e1fa1f8585b7b964263e38db6012ad72aed49d920debc9`  
		Last Modified: Tue, 12 Aug 2025 21:37:15 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f13a7c87f406049621ea7ef21e56ce011a6fb4ba9f6d317772608125d63681`  
		Last Modified: Tue, 12 Aug 2025 21:37:15 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7a49c8b34486fd494cc84ed87423ff2b80a39de79a8e4d91043201473cc7e493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5131616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d40b83559276a2d0317f612d9300d9a386bcfb530631d22d5dd9b057213e733`

```dockerfile
```

-	Layers:
	-	`sha256:547933cd5032a4136551149cf8b34be977602bf2b75c8089ed549e7df50bacb1`  
		Last Modified: Wed, 13 Aug 2025 00:38:28 GMT  
		Size: 5.1 MB (5115042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8573e83330c6670983387448bd1112518586b8e4d70da1fb08c72916f5353d88`  
		Last Modified: Wed, 13 Aug 2025 00:38:28 GMT  
		Size: 16.6 KB (16574 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b16dd9020891a6713d20ce8f201894a865d5845fd59297bae90224e607877fe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 MB (253569595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6338fdec04b49664ae25aa5ae398a7a731c43d889217d5f4932d811947144f2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
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
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da1750076401d158050dbd1c87521fd0cd8b51f7155b8af4b73fd53bc16d3ec`  
		Last Modified: Wed, 13 Aug 2025 16:11:33 GMT  
		Size: 156.1 MB (156081253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae0a6b48213fef145c57888d1c37d156ab81f8cc53360083062bf746cbd4046`  
		Last Modified: Wed, 13 Aug 2025 16:11:32 GMT  
		Size: 69.4 MB (69405301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c0363bdbe6e37b7cc26909ac4d1d1a9e5e846234e475975b975ac602907e0d`  
		Last Modified: Wed, 13 Aug 2025 16:11:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:080e1542233233f41167934d463f8574ea89ccc341f7e60d1699b9e196081050`  
		Last Modified: Wed, 13 Aug 2025 16:11:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7fad953ed7e62a1d46371ab72fe3da64875fa1dad59335cc9301b54f4fec49c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6142deb529ff0f29662a1eaf747870278398ff84bfb0b73ca889bb60765e95e3`

```dockerfile
```

-	Layers:
	-	`sha256:e61ca9dd2b3d1a31c8aafd06a59412e6f765204496b23fe897741ce5c2d2d89d`  
		Last Modified: Wed, 13 Aug 2025 15:38:48 GMT  
		Size: 5.1 MB (5120827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0757533a134a4c8c5bcf0bb3e8827c51ff7503c6325157497950c2f4f45b3e54`  
		Last Modified: Wed, 13 Aug 2025 15:38:49 GMT  
		Size: 16.7 KB (16716 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:b66f57bb0d6701395d410dd21b238bb5059a1ebed071e732abb124ae0ef2c8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.4 MB (265398094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7d9a28b621edca499f6b787082f5084938a3fa4fe956408d339ace0b15d69b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
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
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d2d3f5cb4fef7386c9bc669b3b453c95aee8f0d5997610af0050686337c8bd0`  
		Last Modified: Thu, 14 Aug 2025 17:44:39 GMT  
		Size: 158.0 MB (157963461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec45a40ae74c4670e912760316f308ed776af59b2f21818a722e5d24ebbe2f92`  
		Last Modified: Wed, 13 Aug 2025 20:12:40 GMT  
		Size: 75.4 MB (75360169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99339453e34ec8ede7463263f8f549d62bc94dc2487710ab847f066123abf39`  
		Last Modified: Wed, 13 Aug 2025 20:12:30 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566e6882f15eac3b70b0b5dd5a26232786e4a447c68be6afdb5cea2b12b1c35d`  
		Last Modified: Wed, 13 Aug 2025 20:12:30 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ec31299658d61da067fa31347e5ae22bda6c6d3480590890438fa5b5ae8f0f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5136847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b772a20421f636b45f0bc34c0006e4105a3c01a2df92f43e14fb9e54e17a38e5`

```dockerfile
```

-	Layers:
	-	`sha256:6dfaa7c65c324d1ddb52463ab5643248052231cee9cbfb32e3161138821936fe`  
		Last Modified: Wed, 13 Aug 2025 21:37:53 GMT  
		Size: 5.1 MB (5120212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a318179afbedfc1bc09a7ab29bdaaa105186d956f587ed52a978e273ff1e7c04`  
		Last Modified: Wed, 13 Aug 2025 21:37:54 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:f2fa41ebd8e5aab6d997ab31579a94735a72a46f32c2605c10579e78a5b0ef08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242257920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4796effc412bf3b3fe9f4b4bdc8176e81c8b86388b4a22c13782c126daad764c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
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
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdfdfb3dd202a92cb87969f023e320f3b096af8feb39c444ae1248a5be5ae92`  
		Last Modified: Wed, 13 Aug 2025 19:37:52 GMT  
		Size: 147.0 MB (147026960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecdfe191f4c02f07a3fa52be63641e35038aeef1c70ef477aee641d3d8f1d9e9`  
		Last Modified: Wed, 13 Aug 2025 18:12:46 GMT  
		Size: 68.3 MB (68342082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5629ca1c2f6a565ae125d5cb091974d3c78c641ae3f045f8c3975070c1b7e3`  
		Last Modified: Wed, 13 Aug 2025 18:12:42 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7791ceed28de0415dc2331717af8bcf689acc1bdfbd9be9a96f8c2a854d215`  
		Last Modified: Wed, 13 Aug 2025 18:12:44 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c934d8863937c01bbeaa294431b00e5ab09286b51e22b39cc8e646998fedd28b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5122938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:685317798909a0dc98361cf0ca9a61c91b8d3c0f45a9ffe3ef40a220a5c40105`

```dockerfile
```

-	Layers:
	-	`sha256:96f11030964f8b571ee7376815bd4fbcc428d7286064e94ac8d8980c13fba324`  
		Last Modified: Wed, 13 Aug 2025 18:36:26 GMT  
		Size: 5.1 MB (5106363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:faf90d5d29bd0587575da12ae7ed196fd29056bad3c0a1301b07d6db3bb3a975`  
		Last Modified: Wed, 13 Aug 2025 18:36:27 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json
