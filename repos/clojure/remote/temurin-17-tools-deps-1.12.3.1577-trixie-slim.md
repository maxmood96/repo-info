## `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim`

```console
$ docker pull clojure@sha256:18413f3b241fd30df5628577ed8a40372ed84f442ddb6dc7d1549db2923e489d
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

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f5a2c8b0395f6285f80ba87c62f28e18b89542da846c80cd2a0665a79a415e15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246622358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c33c77d9862a69f224878320f101f3b39503eca09d6cce32198ac558569e54a3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 18:43:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:43:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:43:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:43:34 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:43:34 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:43:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:43:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:43:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:43:50 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:43:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6341a718b687b018545ac717f902c91bac847c51bfa12065815f91928273a782`  
		Last Modified: Sun, 09 Nov 2025 04:08:38 GMT  
		Size: 144.8 MB (144848044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03aacaf0d5b0aaad9f764513d8a753469385a2817bc6c9975072d9566a521d55`  
		Last Modified: Sat, 08 Nov 2025 20:20:59 GMT  
		Size: 72.0 MB (71995166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9edfc2e214574363b23790c8da890dca1084fe9cda90e55d5076221aa81bd5dc`  
		Last Modified: Sat, 08 Nov 2025 19:29:54 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89544baf39e3e1ef8f884855fb567b394f6a6c24c918a47e0769856a577e7a6`  
		Last Modified: Sat, 08 Nov 2025 19:29:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c188f69db4502651738a3eb40d61897c8a84a6f0e878b8d6fa20e1239d383e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be10f4c55c104fcc0269cf1fbd1b6ba320f6da9c02df303b0dbdc849865a16e`

```dockerfile
```

-	Layers:
	-	`sha256:041ab084e452ce3954dd39237f5f43df1e73bfd69af1f8ca57914552c1c5435b`  
		Last Modified: Sat, 08 Nov 2025 22:45:10 GMT  
		Size: 5.3 MB (5256169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6b0f8de332db54507f5c55e4d3ff52c2a7e02465b2ed7f00a74fc73731725a1`  
		Last Modified: Sat, 08 Nov 2025 22:45:10 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:653964e6e73d37cb6011775716c5c4abeab6e67dfccc1aaba559355ad9811ea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.6 MB (245631637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:724beca3f971854769f7428109340c684b999b116d6331b6ae9261632529d691`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:55:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:55:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:55:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:55:44 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:55:44 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:56:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:56:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:56:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:56:01 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:56:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539b83a6c4f463ecae61a13323375dc31fb7a84e5c857f6bec1bcbbb826cbcfc`  
		Last Modified: Fri, 14 Nov 2025 00:56:27 GMT  
		Size: 143.7 MB (143679912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ffef44bd0452f321ac9c0409cb1e626960f54036118315014b2d13f5f0612f`  
		Last Modified: Fri, 14 Nov 2025 00:56:37 GMT  
		Size: 71.8 MB (71808386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f9e2a0ef6f5adbea3be5b46952fb589baf9a3a70115c917777aef521d71bd1`  
		Last Modified: Fri, 14 Nov 2025 00:56:32 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d18c79fd8118976e21274fc6880f9ba0c3e84d05b89c304a56bf7abdbe26c62`  
		Last Modified: Fri, 14 Nov 2025 00:56:32 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bc6e56b193439a0d9bc41d46647610e71887e94f2a9981ad9d8fe76ce2566d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5826e0976d85aa8897593fb219fd600b03f2d9c75a3eb1af405d7810a9dba6b0`

```dockerfile
```

-	Layers:
	-	`sha256:4381896b3c1088c8629b289a452754074fcb9058d67b018415379feff31cb97c`  
		Last Modified: Fri, 14 Nov 2025 01:44:24 GMT  
		Size: 5.3 MB (5261938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c9f10bac0fc97c069cd9ffe3841b9ff1d3ee12bc76733472b11e3fda51db9f`  
		Last Modified: Fri, 14 Nov 2025 01:44:24 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:b3c6791b30abb2c1a14180a631ff31a7aa80edfa0a8f240cfb384bba693507c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255521579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acfca5044f81bf7604c5ff2f34bae6c81fcac056802811766ef7b184bbce4394`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 21:19:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 21:19:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 21:19:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 21:19:55 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 21:19:55 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 21:29:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 21:29:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 21:29:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 21:29:13 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 21:29:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb56603809314457cab77f3e6ee6113b545a14ddbb276ed775bd25c2e218484`  
		Last Modified: Mon, 10 Nov 2025 23:12:22 GMT  
		Size: 144.5 MB (144525174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e28ae93f90e7fd835148abdc27890eacbf9e003bb8c695276be5364ca92fef`  
		Last Modified: Sat, 08 Nov 2025 21:30:02 GMT  
		Size: 77.4 MB (77396716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e85eac4db7342e20b85648794d7eaf780717f4ad69acb15df9093bc19db6bec`  
		Last Modified: Sat, 08 Nov 2025 21:29:56 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c47a1ded9293d7822c387439521f3234921247eb0e0964b00ae89e9a7c8240`  
		Last Modified: Sat, 08 Nov 2025 21:29:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:22d9bb5875801c8c859b0a934238c6bc143e40fadd97ee9dc5d0d6d056e7deac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d43d63668f75f8924d51ef60298634aad7547cb2cb1f4d7b581c55badc23b35`

```dockerfile
```

-	Layers:
	-	`sha256:7f74734964fa616e92097901efeb15ed2fd30773b329da98c32d3ffa62cab221`  
		Last Modified: Sat, 08 Nov 2025 22:45:20 GMT  
		Size: 5.3 MB (5260540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23f75110b83273b5a08611da20f5dc8f920968af8c11cbbda80378153e135e09`  
		Last Modified: Sat, 08 Nov 2025 22:45:21 GMT  
		Size: 15.9 KB (15859 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:6a8cd779fe8b63d843803787c175214edd927c4f6096388f8414dfb7b9524312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (241047381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c63e1de4423d206f135a08a70fed651633bbc6cbcb006bb508939d85862b42`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Mon, 10 Nov 2025 03:21:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 10 Nov 2025 03:21:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 10 Nov 2025 03:21:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 03:21:44 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 10 Nov 2025 03:21:44 GMT
WORKDIR /tmp
# Mon, 10 Nov 2025 03:44:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 10 Nov 2025 03:44:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 10 Nov 2025 03:44:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 10 Nov 2025 03:44:20 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 10 Nov 2025 03:44:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b3bc662a464cc8c76c0909121505b0bd2314416266a8dac4aa9014c89143db2`  
		Last Modified: Mon, 10 Nov 2025 23:11:08 GMT  
		Size: 141.9 MB (141889561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2004d6f80e0cb3558c9fe02916a5962d3a89727eca01bb4240204ebcba51aada`  
		Last Modified: Mon, 10 Nov 2025 03:48:15 GMT  
		Size: 70.9 MB (70880988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45abd6ed0e27918ccf886f07a186d50795c0091bc946e0e116682ff5ba1f2209`  
		Last Modified: Mon, 10 Nov 2025 03:48:10 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597010538ae1ce1d95a84c3a94c025ce22dae15b3684b61c80fbe22028193791`  
		Last Modified: Mon, 10 Nov 2025 03:48:09 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:da876cb8710ad070389386920b3ed567bc92bdb89a6d644008c6bb6a029647d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99142899cef6789e3b14a431281056232dda95a9272e1ef738cdbc67e05d3e5f`

```dockerfile
```

-	Layers:
	-	`sha256:000d4b81eabf1af9665d95be0eec4d799a71aed2990eb150a3f00675d883766d`  
		Last Modified: Mon, 10 Nov 2025 04:36:18 GMT  
		Size: 5.2 MB (5243714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51542b49306001ac67a3bc4f29b8641dea8476993be64c0a9ea9e013cb5e62aa`  
		Last Modified: Mon, 10 Nov 2025 04:36:19 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:efdd0986d16ddc7ca3e772a6eda8f117bff8a6c6115df2b299849fd18a95501c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.7 MB (237651243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a3d9098edc5372bd821db7f3cfb8afe2e994625b548f0be699db3eb48dadaa1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:56:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:56:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:56:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:56:25 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:56:25 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:58:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:58:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:58:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:58:38 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:58:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f13d1771014468c2762b50fac444775ee212cfc03b2579f1c62f791ba963ecc`  
		Last Modified: Fri, 14 Nov 2025 00:57:03 GMT  
		Size: 134.9 MB (134859068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40cb8d02b5ed9fd549035c1498c79a680d1335501edfcceb47b9d9802a70e18c`  
		Last Modified: Fri, 14 Nov 2025 00:59:23 GMT  
		Size: 73.0 MB (72953742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f88e6cea5bb8efc2b154ab2d4c8d0f2bc6d8d10f0cf5e3aecab5112e44226e`  
		Last Modified: Fri, 14 Nov 2025 00:59:05 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ad8d135317a4e011469dc902d98aec42c43a78d2dc85995295351458115273`  
		Last Modified: Fri, 14 Nov 2025 00:59:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6dbc774821706073caaf001035fd727714b1abf5f35005d393c2067c59cf46a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5267905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b587d0837402a8beb4712580c74e5172c91afa35fa1cada59c14de5dc200c1`

```dockerfile
```

-	Layers:
	-	`sha256:a2a5e1226e5f5998a7b1a60261d9c0bedc7404362bd91be249009fba04d83ff9`  
		Last Modified: Fri, 14 Nov 2025 01:44:39 GMT  
		Size: 5.3 MB (5252093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35999569b2b4be780940e13fa346613d4281c624514a10bf2f55e7f78aa9a93c`  
		Last Modified: Fri, 14 Nov 2025 01:44:40 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
