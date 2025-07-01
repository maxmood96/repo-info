## `clojure:temurin-17-trixie`

```console
$ docker pull clojure@sha256:61e5b8e35db1d741bdd704b11a4afcf4226ba6d1f4e605623a09ade7423d3254
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
$ docker pull clojure@sha256:8b3fe201d5f51b98cd275e0afda8dad2e0fb16fbaa125061286752e10cd14972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279254969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93203e1df717351b334c5245baa623c38e31cf447a243073bda0a67be9e87a2c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
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
	-	`sha256:b72fed6e2775feec9291a4bd4b416f996dfc503eda11eaa00def55711302b4ce`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 49.3 MB (49263877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59cd987919b1bf79f4e3145d8025322e2fdd6ed7070bde405da79e788e7c5115`  
		Last Modified: Tue, 01 Jul 2025 02:39:40 GMT  
		Size: 144.6 MB (144634963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1195f06c1e64b92221e74d8b1dfdb87210fd343a7650a59b9aa682e6b1f1d5c`  
		Last Modified: Tue, 01 Jul 2025 02:39:39 GMT  
		Size: 85.4 MB (85355089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c75a28a648920d15325276a98b065e462e62f749afeb610e3b1faa7d5be4ec`  
		Last Modified: Tue, 01 Jul 2025 02:40:02 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd5e3f8c3eef5979d58fe34e19a2de5c73cbfd8d6bc37881cfe8734185219fa`  
		Last Modified: Tue, 01 Jul 2025 02:39:56 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ef3fd17e6fea9748ebe32611e78b74b6a556faf90050cba7ddd8e520a3fcdd9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7474950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2881dfec5ecb67b31864a0aa4578de586b74527a1c8debf162676fd1c2b12dc`

```dockerfile
```

-	Layers:
	-	`sha256:c79fed19fe6df5d437e5c6b5050c71f44c51ad5afa67870a0922449490e9eb3c`  
		Last Modified: Tue, 01 Jul 2025 06:38:13 GMT  
		Size: 7.5 MB (7459153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd7c70e8d7be5359ccec165e3e5920224f488cefd81db5470b23dad712e0c611`  
		Last Modified: Tue, 01 Jul 2025 06:38:14 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6f6c098079693474a0c8f1ca3f1344afca06cddafa5134e74ab690d9993d6997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.3 MB (278331739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5db5e644c6eadc86abe70315820f2b22203bf6e0f26a4846ad41e03e5c7720`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1749513600'
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
	-	`sha256:546a427a0109bbde3a869c6a4ff1ed90ec74768e7fd82dd00441608d83416632`  
		Last Modified: Tue, 10 Jun 2025 22:52:49 GMT  
		Size: 49.6 MB (49621528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6a72e475a5b55de2eb90497671caedc20f1da6c7e5ca00aab0d3c77b204c6b`  
		Last Modified: Sat, 14 Jun 2025 08:38:05 GMT  
		Size: 143.5 MB (143512615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10a429b9ffd932e4ee40499cd0468f6cf59e332542cb5043cda50e18a1e90a4`  
		Last Modified: Wed, 11 Jun 2025 08:32:50 GMT  
		Size: 85.2 MB (85196554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db7fdda14d7dca50d9da52df66b022c6fc71f04ca5589479fe099636b533462`  
		Last Modified: Wed, 11 Jun 2025 08:32:36 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46962a463fa93df701a440a16396cd8017302d1395350eb0413b23f622feb9a3`  
		Last Modified: Wed, 11 Jun 2025 08:32:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ac41783164b51e6bed71eb7c736b0d518da9426ba43786f6ba29fc6f1be12aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69cd48084c66a2a0acb459127d9849080ec433b5b16b9214b1dffc72e07e1423`

```dockerfile
```

-	Layers:
	-	`sha256:622d8fb9dd698c1cbeffabdcdbe8f783740e673d2c8c0e773464752777750de6`  
		Last Modified: Wed, 11 Jun 2025 09:38:47 GMT  
		Size: 7.5 MB (7466179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f355180a8034cf738201d8c01eec7ae1ef16ca83dfc848f0ea5d76e0f9b43fe`  
		Last Modified: Wed, 11 Jun 2025 09:38:48 GMT  
		Size: 15.9 KB (15914 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:93e1583c11086ca77a20d77c926704247b63a51bf222175c2e29b6d26bb0994a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.1 MB (288148271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771cade0c320efa51bcdb426b565fec620c8cce95ea88a893eca8b80792fc6cf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
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
	-	`sha256:5c6a246a80c20351fe842a314b6b3f8561a5ceaea736decf36fe380b29e53224`  
		Last Modified: Tue, 01 Jul 2025 01:18:57 GMT  
		Size: 53.1 MB (53097236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0584037f9e2e942ab798efa93b8fd502cab7aa17a73e78e986f82b3b700b3380`  
		Last Modified: Tue, 01 Jul 2025 08:46:03 GMT  
		Size: 144.3 MB (144280582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaede1bfe2e32ffbc526cbdf924b2502c82c8cb59d870ba8a001e976f7c08309`  
		Last Modified: Tue, 01 Jul 2025 08:53:03 GMT  
		Size: 90.8 MB (90769413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e56d0b2542b9f41cc93f382cac156a78db2fad88bfb87d2d53b6b8300cd28dc`  
		Last Modified: Tue, 01 Jul 2025 08:52:56 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6b31fc82229162a92f998e0ec7d473e8b41d1cb6995544bca522d782bf2c62`  
		Last Modified: Tue, 01 Jul 2025 08:52:56 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9994b0322d1e63b2602d3a7446572ea55c41e129e66278a50d64a5eaf6ba2bee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7479415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128a7f06295afafddbab9832ea62e771bf3c0421c7009899b199c9d75bf6e8b3`

```dockerfile
```

-	Layers:
	-	`sha256:fd1e3c037e7e9afa15b9c80484de506c0bce2ac889e5c2107bf24ff0e0230208`  
		Last Modified: Tue, 01 Jul 2025 09:38:35 GMT  
		Size: 7.5 MB (7463570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0829e974bef2f4f683ce6b86cfb2d7b0ef7379faaf9a447928d6ee0bf480a3c4`  
		Last Modified: Tue, 01 Jul 2025 09:38:36 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:90f64b81769801bbb660b1116f144927357767630eaf5149089b076eef2a0989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.5 MB (270481911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e409f4b4ed849fff5b74f5efe3d1884d9853b808592401b59ac62840ebf7679d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1751241600'
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
	-	`sha256:a19cda6d0aca0ae93b23898ddaa4518ab5077c7011f945c7a7e4a2cacb08ca5f`  
		Last Modified: Tue, 01 Jul 2025 01:23:18 GMT  
		Size: 47.8 MB (47750158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d3e53d716a4eca82bc7ec1d014b1e63164f7a508de7049dd71a1355386dbfc`  
		Last Modified: Tue, 01 Jul 2025 02:33:31 GMT  
		Size: 138.5 MB (138492488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c63f0c5a295ac31376dfa16adc9e52085a21d933a7ee3057a9cf5207e485c1f`  
		Last Modified: Tue, 01 Jul 2025 02:48:27 GMT  
		Size: 84.2 MB (84238222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cce080ac0586c0d8a8d288fedf5b576c87ec98c60f5bd04c60cd2620f5a362`  
		Last Modified: Tue, 01 Jul 2025 02:48:04 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655234db54803e4e863eb472cfdfc42ca1f87448c021a84fdee2b89d2653dec4`  
		Last Modified: Tue, 01 Jul 2025 02:48:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:59f6cce5e6ca680eda03598ddf0d278c229cd8c3bef054c7c878febed1d6e190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7460990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ea15d53f500595cda1dfeae68d8e3e9b7abc842928f94d7b459173dc4debda`

```dockerfile
```

-	Layers:
	-	`sha256:dc9efc3133f6ad6d915cd22aae5e1c9e63380fd79e7143adb9adeced1785089c`  
		Last Modified: Tue, 01 Jul 2025 03:36:19 GMT  
		Size: 7.4 MB (7445145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f305567feb76fcbe18d6a5c5b50db788bc755ad1c1141caa36665ca262deeaf`  
		Last Modified: Tue, 01 Jul 2025 03:36:20 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:1bfdb505006ed832fce8f840848bf5fa466bc6b7ce1432756182aef499bcd9e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.4 MB (270352330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3cf72d148228a5acf67eb8cdfd17ea910dac2cf193409b22b51a79d16c8b23d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1751241600'
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
	-	`sha256:48de1d8f52c0a2a00375babc11bf69628b8225862d3b6ebbb2205e4ae2f3e96a`  
		Last Modified: Tue, 01 Jul 2025 01:19:00 GMT  
		Size: 49.3 MB (49343660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968c8d7f32961543a7f872e2e66912ec4216d7c221769ba446e70bd47f4dafa6`  
		Last Modified: Tue, 01 Jul 2025 08:11:44 GMT  
		Size: 134.7 MB (134673550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272e96b0a5da4720e4a4eab688bd5f2c390b8c0fe3e81cb777de890417c430c6`  
		Last Modified: Tue, 01 Jul 2025 08:15:47 GMT  
		Size: 86.3 MB (86334079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52f27eb0cb63d5e1cad76aa3c817b108906a0701e14854a6cbf6e0fd5e5a962`  
		Last Modified: Tue, 01 Jul 2025 08:15:36 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d369a35c5419fb0642d1838ee7de46fa81497a1c7b211ff9aa337c2220e2445`  
		Last Modified: Tue, 01 Jul 2025 08:15:35 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8886d32859bbd2168131f844474dc8f3e323746860b2874d71702ad1eedae0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7470872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93407c8dffa6aa471182dd65310b6160b53f350934f1711c38414fbcffb0782e`

```dockerfile
```

-	Layers:
	-	`sha256:d0132535b7576064446940a2d0cc22c13484dedf47e18ef1824db8a508a1f60a`  
		Last Modified: Tue, 01 Jul 2025 09:38:45 GMT  
		Size: 7.5 MB (7455075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fed693e5b069282a9f548760cdb00ac1cad3139bb0b4f5450526a2e27842caa`  
		Last Modified: Tue, 01 Jul 2025 09:38:46 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json
