## `clojure:temurin-21-tools-deps-trixie`

```console
$ docker pull clojure@sha256:04168de1f5276272da6ec5c23d97e39c610a6e0c421380075a1ebf8baae62b36
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

### `clojure:temurin-21-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:e53e701c665af3ab6df2dee29a496c7b74860daeba532e0c0a8f371613549672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292662531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b2761fcfd1eaad10eb55f30243a0b7d1220c42cfa56847aa5d9f387ea58e5f7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:22:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:22:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:22:05 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:22:05 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:22:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:22:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:22:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:22:23 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:22:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f184b04661eb30804816a1f402aec6fdfdce123ce9bcc80ebf75c84c2f5bf3`  
		Last Modified: Tue, 03 Feb 2026 03:22:50 GMT  
		Size: 157.8 MB (157826000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d733b8fd63c4f045d3bcfa2f0924f527b5b19eddb8252a85911aa2e07a32edd`  
		Last Modified: Tue, 03 Feb 2026 03:22:50 GMT  
		Size: 85.5 MB (85542536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d82b1822740e6972da4bb63ed4b9f44e96b66bde4cd0b26dc59218c25ae438`  
		Last Modified: Tue, 03 Feb 2026 03:22:46 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c708b8ae63bff14364e9919f12ea780401803a1eb4788929c0ded73d462c9cf`  
		Last Modified: Tue, 03 Feb 2026 03:22:46 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b305876366aa4c122042bda33c1e6dd153d3cfcb155625e4d81071b6dc1ceb68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7486684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65bf9ceca861676a7f34afcd71c5aaf509dfc39c49b3e13f81969ae57bf83ceb`

```dockerfile
```

-	Layers:
	-	`sha256:60828d156e1473eb28fd82905747153ec14cbf4935941c0d6cacf2c102209e80`  
		Last Modified: Tue, 03 Feb 2026 03:22:46 GMT  
		Size: 7.5 MB (7470930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:950ba7e721b9d54860c8f52f99699db327589ef668cccf59eaf843dadf19c226`  
		Last Modified: Tue, 03 Feb 2026 03:22:46 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c94a47711229a407a05df8977d4ec90f1692dc315d028db3c25e2aa1f5916dfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 MB (291122185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5db1229c42c907ea49901e38896be839efc277d0cda5f128a362c72e44e6109`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 03:24:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:24:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:24:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:24:39 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:24:39 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:24:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:24:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:24:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:24:58 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:24:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b7bc9290d9582b559e900cb5895894bbde7f612b783b62074c45f6f3c30a77`  
		Last Modified: Tue, 03 Feb 2026 03:25:23 GMT  
		Size: 156.1 MB (156107579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ecd594bfa7d9a9ed39bfa5dbfcefc584d9a4b98d34d6f1c78c67842d33bd1e`  
		Last Modified: Tue, 03 Feb 2026 03:25:21 GMT  
		Size: 85.4 MB (85361544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26eb6670df4ce762076c68bf4855c33437193b44000108292557e67bfb468e07`  
		Last Modified: Tue, 03 Feb 2026 03:25:18 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40b391029a1f06c550adf155edc6cfdead5b2982930536bd12260d73ab2dada`  
		Last Modified: Tue, 03 Feb 2026 03:25:18 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e0f3479629668b4feeedfbbdce59277c7ed8df575dc2a4282d576c3a076ef5a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db944a94e74d558d09f4e2d1f8402c4a4ba74c0dbf9ad9936a5b748a8515d8fa`

```dockerfile
```

-	Layers:
	-	`sha256:667524a3c67a8ddf1c66fa964662e7824216f293f8e12c6882a50a3800ff3b2a`  
		Last Modified: Tue, 03 Feb 2026 03:25:19 GMT  
		Size: 7.5 MB (7477960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8089adb9b420306b1bb46e5d9a5ff65c6d953436c639f7a31c1c90f3030f9f4d`  
		Last Modified: Tue, 03 Feb 2026 03:25:18 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:f795a004c04c9b1a2e16742bcbe316cae465ab351a0393bd7b0beb7c273633ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (302003270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb013749e5105c7de49924822b192ab664764a603090fb77ea7fba2c78284d0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 09:47:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 09:47:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 09:47:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 09:47:48 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 09:47:48 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 09:52:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 09:52:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 09:52:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 09:52:10 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 09:52:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f073ee443853c23a0c81f2e493bac340b7fd10c67f60104022a9bece7ae4e7d7`  
		Last Modified: Tue, 03 Feb 2026 09:49:16 GMT  
		Size: 157.9 MB (157942921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4542a8eb81630cde1e2dc0f79234cb77fe5def4dd8dcf22f201340819b56e951`  
		Last Modified: Tue, 03 Feb 2026 09:52:51 GMT  
		Size: 90.9 MB (90947191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e24c36867b7abaadda6675d8be512e672ccaecd4047c7a20af60351124d570`  
		Last Modified: Tue, 03 Feb 2026 09:52:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0670d74543b5959b0cf3f68813e119f3b7cfd043887e82e8f10c8d703f4cf174`  
		Last Modified: Tue, 03 Feb 2026 09:52:49 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0aa37c23f818cd27850e52848bb9686924837eec41d7f9df735a695be56e9759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3364307829734e1b93173999be17ea0412bc644e6e76596998434d0988c2fab`

```dockerfile
```

-	Layers:
	-	`sha256:6d0541e7a19208a1314ff3b0bd7691f29794a0bd4c256506b9002394686d0635`  
		Last Modified: Tue, 03 Feb 2026 09:52:49 GMT  
		Size: 7.5 MB (7475351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78eabfc0304d91cf25f848a227a3af2fc4d1704ab9fad65a93afda95ffc7d884`  
		Last Modified: Tue, 03 Feb 2026 09:52:49 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:a3b1349369688d4a02babdeeac586ad906945e08f2f5924b021c3c0088557e6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289397267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3a9ab2375fc9260d0bf68c08c57ab9297280cca78546e193d2165385228be97`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 20:42:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 20:42:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 20:42:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 20:42:20 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 20:42:20 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 20:59:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 21:00:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 21:00:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 21:00:00 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 21:00:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:618efd37f74728f7dcba60c231fad7f2d777dc65e4da32d0adae5e032e1fd125`  
		Last Modified: Tue, 03 Feb 2026 07:13:10 GMT  
		Size: 47.8 MB (47776763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1cdbd3dbc058f023650ab2a7a190ceae0ea518397c9e3b43d69e110a89004f`  
		Last Modified: Thu, 05 Feb 2026 20:49:34 GMT  
		Size: 157.2 MB (157194298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe37afcdc3897f84755539a458de2d10bb7bce0ab1cc84dd101fbab8f707ffd`  
		Last Modified: Thu, 05 Feb 2026 21:04:36 GMT  
		Size: 84.4 MB (84425161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7843c43296650414f924034a9e09794547b11606f6dd4e10ee77ee4f7f2b37e0`  
		Last Modified: Thu, 05 Feb 2026 21:04:23 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca921e30660362564f1ebe2dd1012071925a132865625b5769849a2a79353754`  
		Last Modified: Thu, 05 Feb 2026 21:04:23 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d0e2b4bfccc5ee262f40aee607982f7f7e479b649aae786f04bddfb64e0e972d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7474647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abab08bac1a1ea5057b0b41fecbc3f383c3dff62697df67af74d277a143174ab`

```dockerfile
```

-	Layers:
	-	`sha256:c89d80b0824f03441ea567054ca1feb5432fc893a4d111127f91560cf21e71b8`  
		Last Modified: Thu, 05 Feb 2026 21:04:25 GMT  
		Size: 7.5 MB (7458845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:303d6cabfd44c2f7d2e33ce5fbeb2f779b7da8081cf7e2eba37b9a1e081583c7`  
		Last Modified: Thu, 05 Feb 2026 21:04:23 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:fe8ee9b51a8fba87ead65aed2a0b40bfbf9195a3e66c4d1d2e05dae5a6aca197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282936793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d1c0ece527451e41d47f2ba46f81c99396ad58e1ab95001b3f7952b14f40fa2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 05:04:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 05:04:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 05:04:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 05:04:00 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 05:04:00 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 05:05:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 05:05:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 05:05:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 05:05:16 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 05:05:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7110ef213ad849aef62022029533be2a09b2a6759b6635f693b2cbce0bee3834`  
		Last Modified: Tue, 03 Feb 2026 05:04:42 GMT  
		Size: 147.1 MB (147069858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b9a556dee36c513fff680a331219bd24ca58ae13d457f952f63b84400410d8e`  
		Last Modified: Tue, 03 Feb 2026 05:05:43 GMT  
		Size: 86.5 MB (86511515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67c8cc894350ef361ae138d6162af685bcd328fda94520d811546b0428e9161`  
		Last Modified: Tue, 03 Feb 2026 05:05:42 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8156331dd40d2df91e3630c0685968b6a25e66b56e71426bdee82f2f4b797eff`  
		Last Modified: Tue, 03 Feb 2026 05:05:42 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:660d1adc1bca0705c870ae5df9c183c99159fda6f3362b43b5f7e206ba4c26ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1b4da031ea53bdb9e6fd89d776ba76d17f9f6ca41303b65e4a06d3b57c2ed3d`

```dockerfile
```

-	Layers:
	-	`sha256:7c8beab1a95cd7165a7b4edb80543c2ae5c33acd3c3fe835bb392e99ff45b90a`  
		Last Modified: Tue, 03 Feb 2026 05:05:42 GMT  
		Size: 7.5 MB (7466852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a777756a512adf1b9aa0f6e696b2e858dd43993749851d7d89d0806dbc937bd3`  
		Last Modified: Tue, 03 Feb 2026 05:05:42 GMT  
		Size: 15.8 KB (15753 bytes)  
		MIME: application/vnd.in-toto+json
