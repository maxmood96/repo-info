## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:77a1f911246e0beea782608b399047873bcc1df3388dfb8ce1a4260c0cc3d8f7
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
$ docker pull clojure@sha256:0939a8bd0e79df1f7a08097b94994834624a62e9cfb6f0392c5a14715a653960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242392288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abfd03ea8086655e9f1f23369f94819b668627a0de05445d60abba6409347cc0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a54ff32d6459dc3193c51ab3135d80f6e798c8978ea41a41306b54dfae54e38`  
		Last Modified: Tue, 03 Jun 2025 05:16:28 GMT  
		Size: 144.6 MB (144635071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e19432a4e065fc7ad27c7fd75c254834d6e05c354458c11f6df729ff05e3684`  
		Last Modified: Tue, 03 Jun 2025 05:16:26 GMT  
		Size: 69.5 MB (69530847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4344e5ea51f40e889992265ec18e6093661d503aa46ed44fd7b2fa7c90fbad`  
		Last Modified: Tue, 03 Jun 2025 05:16:24 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15acc508f87734031ecd6b69389e6da0fb9499d18f21f4f37cf7fb84b7bc6931`  
		Last Modified: Tue, 03 Jun 2025 05:16:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bf18c80d1cb7c9672df9d8bb2d921ee879db9453832d082bc7ac06bdb5dd608a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4977376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e490f3ececb01483511f8b153a7a74a76d2c78f04bee6effbf6b80029da65e6e`

```dockerfile
```

-	Layers:
	-	`sha256:84b8a1af06e5d4023969693dff5c8ba8907351e5a58816de30acb4da1139266d`  
		Last Modified: Tue, 03 Jun 2025 05:16:24 GMT  
		Size: 5.0 MB (4961498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42b40b80f1070c7ca2fad8f0859a37131e0de29622652b79316910a12fcd3993`  
		Last Modified: Tue, 03 Jun 2025 05:16:24 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2f2b4803da3131f5267aee9b19a37eca8d9efe929af9ce730486810536649f04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240965081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df0ed8c699d9cb05fe24e0fedc392441b66dd8447b4362a1468fb500a4e39ae4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b321836524b69ea3544c5efb3ffd84866c65bfdc9bc0020ff7d56a1633cff0d3`  
		Last Modified: Thu, 22 May 2025 08:20:52 GMT  
		Size: 143.5 MB (143512639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3a91216796ce999fae54dcb9b4dc51743e74220e782b62e9ab536dceef9c32`  
		Last Modified: Thu, 22 May 2025 08:25:49 GMT  
		Size: 69.4 MB (69386124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:793160d2a51ce79989475e916b3199c3b397272af153c2946008b73e76faebe3`  
		Last Modified: Thu, 22 May 2025 08:25:46 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ff0642eb278933713b27f4f7cf64a3ab4688d5477ab94cb63b68925c7b68f6`  
		Last Modified: Thu, 22 May 2025 08:25:46 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:99766b418fd681dcc8859b7e580a057027ec718d6822830b842fb8e80e10a959
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4983256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd26afe9120f644c2d0ceb2675de1db7a40d9868c3ac3b76cd8643f08c4ddd69`

```dockerfile
```

-	Layers:
	-	`sha256:e94b6e82cdba0cd4f4c6301fa1bf757fa40692006975a03e3dc017ff10f7e402`  
		Last Modified: Thu, 22 May 2025 08:25:47 GMT  
		Size: 5.0 MB (4967259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7578fe2d984bc6d128bb017ae1add68d1349bad71fff9d672b072723f77b1d4`  
		Last Modified: Thu, 22 May 2025 08:25:47 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:b54006d08db55018708ed9e2cee0c275a44a371abdb6c08e72a056a7078ae175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.7 MB (251695175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6a26748943de98152ed07c9b9aa6a973a926e9362363e1abebf5b2e70ead61a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
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
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Tue, 03 Jun 2025 13:39:02 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07686e6fdd26baa61178aa1b8e90f5239ab4c91006e539b5fbf39feb82e0a434`  
		Last Modified: Tue, 03 Jun 2025 08:46:31 GMT  
		Size: 144.3 MB (144280562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e63c1183bbe2ff415b44b8f41ff2f24c6091b87963d70df89143f86ac3a018`  
		Last Modified: Tue, 03 Jun 2025 08:56:08 GMT  
		Size: 75.3 MB (75346663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758bf3fe5a2f61a42ffef77236aa7a9251859db4b88c5b45ec0190506ef5b224`  
		Last Modified: Tue, 03 Jun 2025 08:56:05 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d85156a45a45ba1199d562b5a744cd3b3fcb573a14d14dfb1d01fd68d6ffbb6`  
		Last Modified: Tue, 03 Jun 2025 08:56:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d753f0e00ad328d6eadb1b746c18c7c59d97a212981b7c1e94b9d5ee291d8588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4982583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b5457801e9456a472ce1312aeb403cfcf381e0053a7e06737d71a7a3ae8659`

```dockerfile
```

-	Layers:
	-	`sha256:4cdcf679e1010c326096ee4491ee3476819c13ab9a87500d22ebca85d4a16493`  
		Last Modified: Tue, 03 Jun 2025 08:56:06 GMT  
		Size: 5.0 MB (4966656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3966697e5be14122e26dc4f6c6579954890c7fd3bacaa731dd1dfe27d34fcd6e`  
		Last Modified: Tue, 03 Jun 2025 08:56:05 GMT  
		Size: 15.9 KB (15927 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:9f44244ce6d76fa64464b1a28a56b932781288776b3a49ed813d5cfc2547bc58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229884482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ade5a099c18dacfc0bfd2db15db87839c4e80fb39a8235c5da8cfc3a1fd607`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
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
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Tue, 03 Jun 2025 13:31:54 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad34fa5b937772a939247553d5da11fa707ffc251f370c152ab8bf4d478cc3f`  
		Last Modified: Tue, 03 Jun 2025 06:13:21 GMT  
		Size: 134.7 MB (134673554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d506335fcd8116da059c3ad13347a2b63876bab33c1ab010c5cb442d7e654425`  
		Last Modified: Tue, 03 Jun 2025 06:19:13 GMT  
		Size: 68.3 MB (68327079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb8f84024aa9c146991addc1dec937c079ee5eda9145809894fe645258ccfdd`  
		Last Modified: Tue, 03 Jun 2025 06:19:11 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581ef0b5c6e07ab5276fe8bb62e9343e00b79e493435e1881cc70a23c67247d9`  
		Last Modified: Tue, 03 Jun 2025 06:19:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b8b3df654ec0ff7016e35e091bf3433c9655db1733a24f370a5b111119e06da3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4971590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744bc499393e82af68535f1e4b1ee1de9a62c742f5e4922c415fe750a6e9d418`

```dockerfile
```

-	Layers:
	-	`sha256:0c7b13f5f2697d8908b5483f721891a2c56efd6cd5489b792e0037933aa91a69`  
		Last Modified: Tue, 03 Jun 2025 06:19:12 GMT  
		Size: 5.0 MB (4955711 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb4e23b6a4c6b8e91ba397413e5e8a5eb539370aea11717be780afa203b994e5`  
		Last Modified: Tue, 03 Jun 2025 06:19:11 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json
