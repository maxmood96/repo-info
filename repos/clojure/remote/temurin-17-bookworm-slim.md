## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:7addda06c20bfaa4687c4cac97a3d5ee7d5d3f3d67c4bd96c0694f7a84ab3468
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

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:344d4ef286233d816bddc36ea0a61e8aee9af8abdc72206b7d0adc73eef38056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.5 MB (243535943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78107ae2ead49958767021afba39d6c29f77e045be28b816d9360f1bee18b215`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:43:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:43:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:43:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:43:12 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:43:12 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:43:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:43:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:43:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:43:27 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:43:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60786c4bafcbee56275d983ed5109a507171352690cce450af5da945904d4e10`  
		Last Modified: Tue, 17 Feb 2026 21:43:48 GMT  
		Size: 145.6 MB (145628794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:308523ea4ba886e002eea3d503dd52f90e6228acb9ff1850481ef41601c8577f`  
		Last Modified: Tue, 17 Feb 2026 21:43:46 GMT  
		Size: 69.7 MB (69677621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30eba6bbe0d32eff3c65a4484967934b31f0e375b291088cfd317b0123b07e3`  
		Last Modified: Tue, 17 Feb 2026 21:43:43 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a9485b182ae5ba4ead6f5fb585988a17d16a3eb27b49c4cc995c98533dbf7c`  
		Last Modified: Tue, 17 Feb 2026 21:43:43 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:23acfa0f08006a5aceebe4e96eea6e326c643b13da926805a709b14a819cfc06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5130490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7bfbf6f6673a0da9a6259bb9972fb0e6d6bfb84978e52cfbbebf9735bb78f8`

```dockerfile
```

-	Layers:
	-	`sha256:7483f5149dd5b27d42c2cc31af6b71b5fc962a590ac891f8cf9f95f5ea7c50f5`  
		Last Modified: Tue, 17 Feb 2026 21:43:43 GMT  
		Size: 5.1 MB (5114654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f98ec6cf641fd95ca64aed6ce0f8f40990f75d0d6603983ff2b6c98cac3efa22`  
		Last Modified: Tue, 17 Feb 2026 21:43:43 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:27ba2474f127cd0a0f5e999c3520a4e4573dc185b295524e078628b0e6a1d0c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.2 MB (242217662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a791ed4839186b4c7f8f7e3dcf92cfc4d5920301066fa0c101cc3604dcdc59e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:42:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:42:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:42:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:42:24 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:42:24 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:43:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:43:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:43:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:43:23 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:43:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f339462ebb73c47e790b7ae79d512da87bf812efd3933e67089d72b9a7c05288`  
		Last Modified: Tue, 17 Feb 2026 21:43:01 GMT  
		Size: 144.4 MB (144436250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482fab2c8fc6612c5c0af5a39ff06b007d0b7ba18dd8fd9fbd990afff89c5dbc`  
		Last Modified: Tue, 17 Feb 2026 21:43:40 GMT  
		Size: 69.7 MB (69672546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae531978889a8db3f416d0110a6b42db63d6cfeb7b29407d4ced652e84e09be`  
		Last Modified: Tue, 17 Feb 2026 21:43:38 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22d07701cbf82f05ad6c0001b1acec49133499e5cbf31bea98e6dd1f200cd39`  
		Last Modified: Tue, 17 Feb 2026 21:43:38 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:00f458c72295a00da8f315e90a4bc3b9924a00de84b215587cc0dc0cf077cdf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5136369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd50bda207d42db4c875afd689fe374a2037a4dceb1e74a3a3daeb328a4fda8e`

```dockerfile
```

-	Layers:
	-	`sha256:3b88366b394217790abd1279a71987816d2b4a869874cda732faf0e1d5666d05`  
		Last Modified: Tue, 17 Feb 2026 21:43:38 GMT  
		Size: 5.1 MB (5120415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:135f376c35b7856dc419018d780000e021fa6052b65c063817e7202f1899b3c7`  
		Last Modified: Tue, 17 Feb 2026 21:43:38 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:030fd79bc9cd4f2603f4634559fb864d223b2e0ba08547911525920850f7279d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (253022171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f9aba1095b8d610e20cb59a335d9b2f90881a9ae1ec0c0b7cf8479fcc7e62d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Fri, 06 Feb 2026 00:22:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:22:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:22:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:22:02 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Fri, 06 Feb 2026 00:22:04 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:28:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:29:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:29:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:29:02 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:29:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7910825c7ec7b68916beacd9af906d34dec10e730af19f67c87aa4e2ee440381`  
		Last Modified: Tue, 03 Feb 2026 01:12:56 GMT  
		Size: 32.1 MB (32068712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56445963f10f9073db32d8e55af4130cabe6e777336d5f50276061d989325f1a`  
		Last Modified: Fri, 06 Feb 2026 00:23:46 GMT  
		Size: 145.4 MB (145438231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7aa19b54159e662764c554974ee7bcf22a2cbb38eaa8dc57a0b6172871f8d8e`  
		Last Modified: Fri, 06 Feb 2026 00:29:49 GMT  
		Size: 75.5 MB (75514185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977176e520a8d8e543e6f990a43ed054ab1ec4aa4c6d7b388021533b72907c7b`  
		Last Modified: Fri, 06 Feb 2026 00:29:47 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e75b55894808d63b4dcbbf02aece8bb1c7b172eb9eea15eca37751dcc63acf3`  
		Last Modified: Fri, 06 Feb 2026 00:29:47 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:da81d45d3890cd7ba63622867d49b666f50cad03ef76f60648c8c3eaa1fb247f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5135696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afb1da38fa077c33377a5bc379a51b802fd4c931358b6bbd76630eb71144111`

```dockerfile
```

-	Layers:
	-	`sha256:1b93d76c5080df3c51aa6680be864b27493658238675a670a4d25daac14379d1`  
		Last Modified: Fri, 06 Feb 2026 00:29:47 GMT  
		Size: 5.1 MB (5119812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ccc7c11c3b5d358facd6651e4bbc85c491f4222f6e1b885efc7509fc4162d91`  
		Last Modified: Fri, 06 Feb 2026 00:29:47 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:361041745ddd36964333165b144a5b5a9444c9662fe1e8daffee0e956063af2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231002455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d427e13ae11333482f8819920fda4843c28e6cbebd27672ad1547e7b62822479`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:01:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:01:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:01:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:01:57 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:01:57 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:04:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:04:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:04:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:04:15 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:04:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1af58cc4761e637c6263de1747b7d56f05c86d8d94c69c1d5359a66432b8c048`  
		Last Modified: Thu, 05 Feb 2026 23:02:41 GMT  
		Size: 135.6 MB (135627055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01411b9f0319e393c520ce01bb7255e61cefae14cc7bcee315f7a3adf75e0978`  
		Last Modified: Thu, 05 Feb 2026 23:04:40 GMT  
		Size: 68.5 MB (68489975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda0c92a77fd0f1c53cebaeeb46cd16288f1e2a319679eb71f3d889f2fd2a089`  
		Last Modified: Thu, 05 Feb 2026 23:04:39 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad60b7a2d5779fb735da4db70c62e66ba3eb468f5fba80695e6c232456417fc`  
		Last Modified: Thu, 05 Feb 2026 23:04:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:af5aafd5aad8f873d2c5fad890bf12e13ebe8f64d6b5211cb2981032ff8f7df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5121811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a3ab09aaabb90d21c221760aad3c3ec9699809aafbe35ae7b9eff5a8f71365`

```dockerfile
```

-	Layers:
	-	`sha256:16ad59152bc66ad18d705a157bb314ccf5e89bd7f7b53092f2e7bdc165713afa`  
		Last Modified: Thu, 05 Feb 2026 23:04:39 GMT  
		Size: 5.1 MB (5105975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7acc46b8fe265a3cf14509f8cfcd96c3135ef2f51004444dae32c3ffb05b5b66`  
		Last Modified: Thu, 05 Feb 2026 23:04:39 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json
