## `clojure:temurin-17-trixie-slim`

```console
$ docker pull clojure@sha256:d39206ced846c5e21e6c09abd88cdee003a48cf1942bc31e6d287cb1b08c167e
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

### `clojure:temurin-17-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:533192d1fd882272a925a27a91bf95c9305f11bd573c9f152bfc87fede414300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.5 MB (246466914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:239dd1f61592a6ca851b7a1610edb5ce60c82f20bd70377c3167c832ca091203`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a789709f2dd5fc1d2372b3620e4f1b0148dcf8e8521e7611478cd79636fdd5a4`  
		Last Modified: Tue, 21 Oct 2025 12:51:25 GMT  
		Size: 144.7 MB (144693294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8d40d302a33fa3d52f93daf9a43713b87bacee4ffc02363fbe0c5223ba63b4`  
		Last Modified: Tue, 21 Oct 2025 02:22:35 GMT  
		Size: 72.0 MB (71994655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcef85c10f1a2d40eb64b439f8085f997f2ccda27f64c9ed24a8ac92b6ebf4c`  
		Last Modified: Tue, 21 Oct 2025 02:22:32 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e494813e21b99c7670d2a9311d3900ab2d678284dc81f64e5a67c398c3fabc`  
		Last Modified: Tue, 21 Oct 2025 02:22:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b548bd86c0d48200487f8adb8692c1b6a60b898b9f1855ff16669da22da7bb0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659bb00577dd26ef9122abff669c2a682c011716ec13106a04a48b2302a0f0e0`

```dockerfile
```

-	Layers:
	-	`sha256:010fddcee7c4a641151c6e877b845fbbe1f3169cea894865097a89606da74543`  
		Last Modified: Tue, 21 Oct 2025 09:40:30 GMT  
		Size: 5.3 MB (5256167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7428974dbfcdaac43ee06e43f0a0f82d7637f175312e76bf00548344ae588c1c`  
		Last Modified: Tue, 21 Oct 2025 09:40:31 GMT  
		Size: 15.9 KB (15855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:20f4a42dada708b24f1c668165295da62837f935703a22a2bdc689b3c1ead9b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.5 MB (245493572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d20d2016bc50ecb57259211cda54492af73c291dadd9b2fcc61c24c463f44f5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28b98c886e64e9b25db06613bc67008841efc163ff091149cdad51d95001052`  
		Last Modified: Tue, 21 Oct 2025 02:28:09 GMT  
		Size: 143.5 MB (143542159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4c2f2e9ab5527bd70ee14cbd8a64db9d3669c5f5bfeaf9ddbd2540795737ab`  
		Last Modified: Tue, 21 Oct 2025 02:28:36 GMT  
		Size: 71.8 MB (71808246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:353586e0f54867057fbbb92746af277b5571ffab49df7e3fa9afefb40e75e2d4`  
		Last Modified: Tue, 21 Oct 2025 02:28:25 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71fd30fd14af59e108502379d2734fd4244949b6fd70f18bd089596145efb649`  
		Last Modified: Tue, 21 Oct 2025 02:28:25 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0bdafd9e127bd4de3c6be967ef44855a863a5215a1a73e638a2dbefd51bbc288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44b8d9055366f3961e068ecb65190ac825c2416af682c24c25725f77fd5d82c8`

```dockerfile
```

-	Layers:
	-	`sha256:9b0877977fa62140e1f3b34ca3d411e798c85fc8440f0b823af2774f0d14e166`  
		Last Modified: Tue, 21 Oct 2025 09:40:36 GMT  
		Size: 5.3 MB (5261936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30ce4fe6d546eae10304c170f08e13c34fd7c748cd11dfd1dbb5ac4da2fee588`  
		Last Modified: Tue, 21 Oct 2025 09:40:37 GMT  
		Size: 16.0 KB (15973 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:aa51895e0d108421ad429a36a63f45fcaaadcf348723dceb73473ef18c358bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.6 MB (258560510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e41e38105e37758ba16adc98e596bfa46ab4a217795bd64b111c2646c0f40a34`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cba05d3e1f82aa7350de29683542014410151ba5da078d43d5651f61d1cd89b`  
		Last Modified: Fri, 10 Oct 2025 05:22:47 GMT  
		Size: 144.4 MB (144372884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d79e0cfd3f1315366f3b18972071aa9ddf9ceae8c87942e4cf9b2e17de70d34`  
		Last Modified: Fri, 10 Oct 2025 05:32:17 GMT  
		Size: 80.6 MB (80588126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e7ee4e8abf28393b3e8454fa43fb505bfd58058714f1e77aee29391ba8279a`  
		Last Modified: Fri, 10 Oct 2025 05:32:13 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b83f727539bf46f3d2c2da2b79ce1414efb8e383e32d3d386c8d1a5d6d0e562`  
		Last Modified: Fri, 10 Oct 2025 05:32:13 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3a4a3e55334929c53f3503e528b464615f34e29ddd1ac94cb6f72340b04b88ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d972a9c72b78f6941755d567dfb82367e96905b624782ae9e1178a445150dc5b`

```dockerfile
```

-	Layers:
	-	`sha256:157b19a86a63b869ca3101a48018012a29ec6a8b9a0233e41cff59127a0cb251`  
		Last Modified: Fri, 10 Oct 2025 06:42:57 GMT  
		Size: 5.3 MB (5260538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ab9dbf6c6fac2adf12662208b0c502224547af96d45cc8d45756b21d40d5251`  
		Last Modified: Fri, 10 Oct 2025 06:42:58 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:5d586e0f15efe6d249ae33a1cec12daf361126569874798a3f0696d87dea59b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240340644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05e79462d18df539d5fb271f8823e33cb94fc041d2c718a8dbe489deeec393de`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ecc6f9aec21fb94a493c2875c244e720a2f7c6c034063ce87b2f5b6b46962ec9`  
		Last Modified: Tue, 30 Sep 2025 01:05:14 GMT  
		Size: 28.3 MB (28275502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dfb1dd1350f7a95ce53ab9177ca67c179a1680059cb360645b0c6008226957`  
		Last Modified: Thu, 16 Oct 2025 07:40:42 GMT  
		Size: 138.6 MB (138575657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33aeeedb75ee546155058752c86a5550795879cbd57e6b310ac287eb8b5b0cd0`  
		Last Modified: Thu, 16 Oct 2025 08:02:18 GMT  
		Size: 73.5 MB (73488440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12002bebce79841f50ec01bb0cea316e21472883a359c85b72fee6af75bff6fd`  
		Last Modified: Thu, 16 Oct 2025 08:02:12 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ef9066e1f7355aec2a990f44d13357a986a73a76c5febdd78bf10111fb6834`  
		Last Modified: Thu, 16 Oct 2025 08:02:12 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0c46d29956ac61b7b70fb267e3a4da2d93ccefed419c948a0c038d7b09d6d1f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e165947d87b3a7eb669c69836056a7a3b551d7dbc43e17355e428ac0c1b1b85`

```dockerfile
```

-	Layers:
	-	`sha256:f60bd8d4ddd3ff29156cf2fee7417a1e2463b437a0a8fcdaacfd625e61389fbf`  
		Last Modified: Thu, 16 Oct 2025 09:37:10 GMT  
		Size: 5.2 MB (5243712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:162f1207d57af72c6ffa30b4164d766446f493871195a320df73e514582ed65e`  
		Last Modified: Thu, 16 Oct 2025 09:37:10 GMT  
		Size: 15.9 KB (15903 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:982f88aa6acc082b1be9dc086d2c18ef9c910ca823295a3665b7f5da201d142d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.1 MB (240125194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c76604a448df7ddd685f0824ada6c8b49e7cd87acdf09c5ba76119d13be04c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a273f5c9c3ebb0cfa0ce46495a97571c2fbd1b6027c2ffebbdf7f10520a2e627`  
		Last Modified: Thu, 09 Oct 2025 23:12:50 GMT  
		Size: 134.7 MB (134723655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca5571cf2da1e2cd85e19fd0282c541c2aaa0e817e8da19fdf5ef046dbcd67a`  
		Last Modified: Thu, 09 Oct 2025 23:18:23 GMT  
		Size: 75.6 MB (75563267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91caffb0c2132c82952a916c04629d25476369f18e286487eb6994e236227292`  
		Last Modified: Thu, 09 Oct 2025 23:18:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1469c4c0a2904700448d77e0bc75eac2817f02c0696f823605563fb3540a1d36`  
		Last Modified: Thu, 09 Oct 2025 23:18:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:03372e5050df5efc8849be00b28cdd9fe253425518b9bd94c21dfaeab00f008a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5267945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:720c93b044129d35d108cdbc30fe98ae13ae93f19dde685248fc179ce4a18e89`

```dockerfile
```

-	Layers:
	-	`sha256:33007678471fe0f0932637f02b33546f6448fc73daae4ae56a94ef3fdf67f14f`  
		Last Modified: Fri, 10 Oct 2025 00:38:57 GMT  
		Size: 5.3 MB (5252091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4d2adb4e6ded1a99c482b9022addd7d3caecc715284e68d028e26187920bad8`  
		Last Modified: Fri, 10 Oct 2025 00:38:59 GMT  
		Size: 15.9 KB (15854 bytes)  
		MIME: application/vnd.in-toto+json
