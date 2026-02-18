## `clojure:temurin-17-trixie`

```console
$ docker pull clojure@sha256:1ba86646eef3a8442c1da47d377e8be93d21a295c82fdd04faac9161c368af80
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

### `clojure:temurin-17-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:ef02952aa574dbb67604138a854124b6f6219570695bb1beba0ee5afea11bb9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280464748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ee849b3d943e761a64db042073b2c9b53e043fa1f87960ba5f831869773616`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 21:43:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:43:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:43:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:43:36 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:43:36 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:43:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:43:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:43:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:43:55 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:43:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7cb6cb56ec583689fbf4ac75eb06a08ed40616eed6c8b368f86f8d1e233cf7`  
		Last Modified: Tue, 17 Feb 2026 21:44:18 GMT  
		Size: 145.6 MB (145628776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8e7ed05483de808aabe0b5136dab7491b50204b0b82957f60d031862356f4a`  
		Last Modified: Tue, 17 Feb 2026 21:44:17 GMT  
		Size: 85.5 MB (85541977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e71bf1841666ea7c0a20815de85730b25bc644791229a670e316db4a95872a`  
		Last Modified: Tue, 17 Feb 2026 21:44:13 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098949a8a2056b9f5362d3820128bde593e6e25335b97262410973241e65e5df`  
		Last Modified: Tue, 17 Feb 2026 21:44:13 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ae2b4aa8db2fbc8def922cecbe823081aca6a6ec19559a6446692234fb77d63b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7484834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa64bb85655751b7eaa5123638de06496115b8a568bd726e784b5037351bb832`

```dockerfile
```

-	Layers:
	-	`sha256:c04a707506b0bdc2b4d2e17c49bbecd2e0858bd5605cf0f8a836504c0d8798ec`  
		Last Modified: Tue, 17 Feb 2026 21:44:14 GMT  
		Size: 7.5 MB (7469080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16b0e10b53d5a930b28e33d13b58477e0079dc1bc4f6ef07634315be688a6c3a`  
		Last Modified: Tue, 17 Feb 2026 21:44:13 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:17b82dd7c25090001383a0a13443e9f1ecfffd1a56c3a25af95632e5fa5aa9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 MB (279450489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c75c9ca153f34e350e078fe4ad54f4616e0e92e4a7a2973850ce88d50ff29e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 21:43:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:43:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:43:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:43:24 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:43:24 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:43:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:43:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:43:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:43:42 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:43:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59ae201edf9d494bdc50f255b67f7ad528b4257f82c47605f2df2fe3a7471f4`  
		Last Modified: Tue, 17 Feb 2026 21:44:05 GMT  
		Size: 144.4 MB (144436209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c637e2effdf7ce6a2cade75ba6e1748ef36c5e5073e1b65408f6aef543c675`  
		Last Modified: Tue, 17 Feb 2026 21:44:04 GMT  
		Size: 85.4 MB (85361220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3a7865beac7d261b3302135029b7611c6458ce9935e4fee34b79abd4dbfc25`  
		Last Modified: Tue, 17 Feb 2026 21:44:01 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13551db3bfa83b87c9e51a22d4d3beb79d3d17ff619f498274f3da318657b419`  
		Last Modified: Tue, 17 Feb 2026 21:44:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:367e82b12b64cad8d8d248e42e50fabac765ca6c24211b952e95888814fe9316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bbd00b0a639dac3fe5ad74ded55155a2f329503c6e0e9e602bc9fac5a816af5`

```dockerfile
```

-	Layers:
	-	`sha256:a95ff5859e0335bcdbe65e1cc480b7537529a8bd00787493809c387872a44374`  
		Last Modified: Tue, 17 Feb 2026 21:44:01 GMT  
		Size: 7.5 MB (7476110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cf8198a8cfadb350284b233aa752349af216dba7e16e550a0ff05ab193eb2a6`  
		Last Modified: Tue, 17 Feb 2026 21:44:01 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:b5438792a8d435a780d893963adcdadb5a3a08b43b1b3a88a9ef0b55a4d45e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.5 MB (289498954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0b860d9e527d8ddf6e7652649c72ca8b09b9742bff7bd49aa9d7ce6f8deb508`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 23:48:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 23:48:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 23:48:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:48:37 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 23:48:38 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 23:55:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 23:55:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 23:55:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 23:55:50 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 23:55:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b4cabddd66d71e97ccb04d7861e4511a418edbd43a9f1a73ba473b7207138b`  
		Last Modified: Tue, 17 Feb 2026 23:50:19 GMT  
		Size: 145.4 MB (145438194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4cf53b8db1c2aed6f5237c04438f7b130c4dda8feda192480f8e952fe511787`  
		Last Modified: Tue, 17 Feb 2026 23:56:39 GMT  
		Size: 90.9 MB (90947599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60027f35b226184dc9ffa079a19a29ab0a18cd7c13c9e6e5d85519246f1a5f28`  
		Last Modified: Tue, 17 Feb 2026 23:56:33 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae140fcd67828b0c5d3cabd2abe5e0b320de4095266766959b5dae19a838e093`  
		Last Modified: Tue, 17 Feb 2026 23:56:33 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e9eff2c4b59fbba3c2c5d3ce873b44e3a47e673733a801a286d5cd638f6fc3ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:700040a1660645770df84e15712e4d31915df837c3ddab07eca25ac94cd546bc`

```dockerfile
```

-	Layers:
	-	`sha256:cc1b6d1712627bf09ff80f018ea42d06955144bdf8e7cc42148e260bf28e0ba5`  
		Last Modified: Tue, 17 Feb 2026 23:56:36 GMT  
		Size: 7.5 MB (7473501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd0d8535891b875eea1698a8814c539832fbd8f0d628984d9ebd28128aaea8ee`  
		Last Modified: Tue, 17 Feb 2026 23:56:36 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:3cc8eb7d909f3fd8fbdea2f8c4cde1cfb37b6c2713bdbe55b705674478b050b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.9 MB (274865926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a852778dfc7b206b8ba9ac1a3b76df16bc1c7b18bbb0278a8df374e23c15e3b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 11:35:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Feb 2026 11:35:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Feb 2026 11:35:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 11:35:34 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Mon, 09 Feb 2026 11:35:34 GMT
WORKDIR /tmp
# Mon, 09 Feb 2026 11:57:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Feb 2026 11:57:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Feb 2026 11:57:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Feb 2026 11:57:45 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Feb 2026 11:57:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:618efd37f74728f7dcba60c231fad7f2d777dc65e4da32d0adae5e032e1fd125`  
		Last Modified: Tue, 03 Feb 2026 07:13:10 GMT  
		Size: 47.8 MB (47776763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6961c6293dfaf6b0d10e3586db69d555fc30986d768195e9ca2432d9b671a1be`  
		Last Modified: Mon, 09 Feb 2026 11:41:33 GMT  
		Size: 142.7 MB (142663040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb710d27286fd213dbfe569370f8f16cc74a1915d38daf494ce19713edf3418`  
		Last Modified: Mon, 09 Feb 2026 12:02:09 GMT  
		Size: 84.4 MB (84425076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c2adf8d261dfe1969d486744a7cfc94d58b2cfc91e259fa0e70354aa39fe26`  
		Last Modified: Mon, 09 Feb 2026 12:01:56 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6cfcd37a2fe1a2b7dbb60afb00378063d303854344d22b09bdd100bba4e54e3`  
		Last Modified: Mon, 09 Feb 2026 12:01:56 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:55908f9831a0450d577e1892619a52dbcec025aa60ad111c6d24f23b5a4cf5d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7470877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2000aca8ea591f98a519904933c6f8be4c07b5d972951fcdb080f4a6623626ff`

```dockerfile
```

-	Layers:
	-	`sha256:6d696293170741485cfdb0f2ca737b449ae73114677362edef1f05d420eebc83`  
		Last Modified: Mon, 09 Feb 2026 12:01:58 GMT  
		Size: 7.5 MB (7455076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:406392feaed449537d07182d8332279cdf271ff0ab73094b7e976246f0d1df8b`  
		Last Modified: Mon, 09 Feb 2026 12:01:56 GMT  
		Size: 15.8 KB (15801 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:91d8db1552ea7e9dba89408ad579955acaa364136d35e03bbb6f5913eb2a3f6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271494624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370ec6c6ff55fe65a7b00b988bd330c3b3ff7551a8d8a8b211fa97ab415f4cf9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 22:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 22:09:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 22:09:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 22:09:56 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 22:09:57 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 22:10:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 22:10:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 22:10:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 22:10:49 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 22:10:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868d422d07fcb06624c9f60a8bf6f9f34a34f93817bcffd68a63a327f55e0e11`  
		Last Modified: Tue, 17 Feb 2026 22:11:27 GMT  
		Size: 135.6 MB (135627116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66802d351feaa5515da5f4ae69601b137c86309431790646c50f76060421df60`  
		Last Modified: Tue, 17 Feb 2026 22:11:32 GMT  
		Size: 86.5 MB (86512084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859ff4808a6eab1368c73eda3eaead105a2a7f0204b63f9f725c553907a3c891`  
		Last Modified: Tue, 17 Feb 2026 22:11:30 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db7df25eda8372c5e32ee023fa7e2a583d88454dccfd0184b3307944d61778b5`  
		Last Modified: Tue, 17 Feb 2026 22:11:30 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:56d0683410df60aed64775f04d5fada316c6efb50bdecc936c1a799deec6629f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7480756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e70965b8c714be35a71697d6670c90bb0ec48dcb18e00de0050efba32984bb57`

```dockerfile
```

-	Layers:
	-	`sha256:6130f2e2e7cc591118dd6b55417f9fdbf27fd6f0c085033366a9c2ea46efce67`  
		Last Modified: Tue, 17 Feb 2026 22:11:31 GMT  
		Size: 7.5 MB (7465002 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:188b8f8ed4ffee522339ad4d1545b85c47c8f3e9a48a5ae9a52366497c147a1e`  
		Last Modified: Tue, 17 Feb 2026 22:11:30 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
