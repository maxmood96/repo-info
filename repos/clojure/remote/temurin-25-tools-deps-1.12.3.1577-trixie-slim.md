## `clojure:temurin-25-tools-deps-1.12.3.1577-trixie-slim`

```console
$ docker pull clojure@sha256:a7d984daa64d8ffb4cdc38a3e85c4d5024c0af1747e9e1977fc4417bf59ef1ec
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

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6e75cb3ce67fa4ba16afdfc9c4ec8344e22d25cdde99568e1ff8f3ae07523e35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193810093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1368a7a3dfb06adc4907fb78338a1e44db4df7e1188e52e5db99fbd67a8996b6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
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
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9175bb4f570527e9833bfce887bdce852d20ab2021a964170241b04ee8f60a06`  
		Last Modified: Tue, 30 Sep 2025 00:57:40 GMT  
		Size: 92.0 MB (92036050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:465246928f9c331b9473d23f4c2b91bad0bed0c43c805080a317c8acf3e89d04`  
		Last Modified: Tue, 30 Sep 2025 00:57:36 GMT  
		Size: 72.0 MB (71995238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953ae00107f5fa94c7a2ba8c947151c6e7aee491d18ecc651899ccbdc9fcd2bd`  
		Last Modified: Tue, 30 Sep 2025 00:57:30 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0a77450cac614e259a286b3ba499552c5beb384caae4b5f49840de05016101`  
		Last Modified: Tue, 30 Sep 2025 00:57:30 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f4c298b623dec26f73eaa99f2ccce99202bd3dd655b1add24d7827c11e6f1ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5223987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abbe4ba3037605495a129f72f984ab50703e6fe8379c7486dfe89858725c1718`

```dockerfile
```

-	Layers:
	-	`sha256:546d83d81ccceaa9fd1f43a7079676dc9ed05369569e07b7fd354ed9ce66c045`  
		Last Modified: Wed, 01 Oct 2025 20:35:42 GMT  
		Size: 5.2 MB (5207451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e86a419a0987ded267c04dccb8588a969e2c3ee814e046b7b3c08bdeff1a1bc6`  
		Last Modified: Wed, 01 Oct 2025 20:35:43 GMT  
		Size: 16.5 KB (16536 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ee077a2855cf3e08c4d60262adb5b7543ced434f90da3e722bb1a2043a139808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (192995524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b82aba5acd58567f7e953ade1f399a3eb50cb8d9cbd272e86f7ef6daabc932b8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
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
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf0779e385630b3094c0e05803a7343ef5a20929efac0b24a8801d3070a2f81`  
		Last Modified: Tue, 30 Sep 2025 00:56:51 GMT  
		Size: 91.0 MB (91045230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4bbf6e4efef398b957ddee9bffce52dbdc581fd36894dbb4b4fba69cd83e3c6`  
		Last Modified: Tue, 30 Sep 2025 00:56:30 GMT  
		Size: 71.8 MB (71808414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881710ca5fc6029c733e46a1849fa423b6a93a8e9e4d2461481881bd01b0a682`  
		Last Modified: Tue, 30 Sep 2025 00:56:29 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b140599461cb51ef235fe4b5206b972100393df59f8e9c6dbe83de0b8aa0220c`  
		Last Modified: Tue, 30 Sep 2025 00:56:29 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:97011a4cdd54c5846347e0d737210167cd7266dff3eab5b2602e83a4434992b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b85cfdc93d129644c2516b24039fc9556877090fe12b98ebb2c84e4e2a7d5b`

```dockerfile
```

-	Layers:
	-	`sha256:7bebf25d3f4f29267d1f46fbdcf6a534c6b08e3365356193ca635a1be99bc73d`  
		Last Modified: Wed, 01 Oct 2025 21:46:06 GMT  
		Size: 5.2 MB (5213241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e466da30c1f26b00107f43366b2641391d1b0d4b8bca6fca1e167f3ad4a1f06`  
		Last Modified: Wed, 01 Oct 2025 21:46:07 GMT  
		Size: 16.7 KB (16677 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:4e112e134a3257b409753fec7179d11c6098615d6e95dc2eac16d59987c2ac02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.6 MB (202593820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c0cc7b6fd039532e8c6b7de231439bc2aa1c02ddbfec6729fe6a722248e9504`
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
	-	`sha256:f02aec982c14ce5979fd1cc3346d4a14cfe11350bfa7072f1c053674be3e6c39`  
		Last Modified: Tue, 30 Sep 2025 22:44:21 GMT  
		Size: 91.6 MB (91601754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9276019b6c4ac8b3419434459e3ae55e86d5b9544a3ee6b9414889f2af5ee36`  
		Last Modified: Tue, 30 Sep 2025 22:44:15 GMT  
		Size: 77.4 MB (77392571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7c0eba35bbc8505a8caebdbc185ca2d527718ae8ea4addf21b426b50693541`  
		Last Modified: Tue, 30 Sep 2025 22:44:11 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5f92e9b0e07a5f5df4970b8a19b1293885b2aa8939ce363523008a4c8fcbdb`  
		Last Modified: Tue, 30 Sep 2025 22:44:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c0d5728b81fe7dcb97cd9a94867b683fca651e74ee65d0b5daf95c9893e0e72d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db025c944535ad83790ae1588cd10c0c1eea82c7476dbb41d0c40519033eb4e6`

```dockerfile
```

-	Layers:
	-	`sha256:fa7ae7191b834dbfe049a243d76d4161f3729fe54b50fcac6985e6513b1e1c2a`  
		Last Modified: Wed, 01 Oct 2025 21:46:11 GMT  
		Size: 5.2 MB (5213132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa0935885c9c536f992dd092e8e4e79478373f5cb3f3a39258aac354d5ec2eb5`  
		Last Modified: Wed, 01 Oct 2025 21:46:12 GMT  
		Size: 16.6 KB (16596 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:c4431c5d1ecaf62ca2c596da3b44bd8f2f635be2fc531789c4959955f8089eff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.9 MB (189905612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d2e7687d038753430e7aaaf68bc42c7ccc9e7daf4d26f627459a88950c49ff`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
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
	-	`sha256:dd4e3fb8766f676c414c0c55be0f5d9f6e6359dc2628caa804016b0f2ba461f2`  
		Last Modified: Tue, 09 Sep 2025 01:07:45 GMT  
		Size: 28.3 MB (28271372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a8ad1b0ea1a654539a3a3cf5a691ced654fa53ee2076ba518ae9e7cde109a80`  
		Last Modified: Sat, 27 Sep 2025 01:07:11 GMT  
		Size: 90.8 MB (90752393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0529895632aa57c35c39e86983506c3e958268b49e4f372f1178485d0f3f1d`  
		Last Modified: Sat, 27 Sep 2025 01:31:04 GMT  
		Size: 70.9 MB (70880803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2f063fc815c53a4a935efb157632b6dd342e1562ada7f929ba69ebf75d8345`  
		Last Modified: Sat, 27 Sep 2025 01:30:57 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1a4b5d292782939ba821b9ebbffc8abdec67a431fd72535ab4084db941e582`  
		Last Modified: Sat, 27 Sep 2025 01:30:57 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e839708491d60b0afb6a6ce172bde7c16af4478d6ea3086b205924719f0c502c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5213520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4efe22d8b00f59db98078ebf175008469bc5bd06c269e62359f7d57c2e2b19`

```dockerfile
```

-	Layers:
	-	`sha256:86e06ca9b296337fb95c4bb572b7938d46503f5a7945df98dad2f8eda0d88783`  
		Last Modified: Sat, 27 Sep 2025 03:38:01 GMT  
		Size: 5.2 MB (5196924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46b465b7287bd3e8490a43a11c31b806725ac82a5d88c624e0f1e5b07c4fe712`  
		Last Modified: Sat, 27 Sep 2025 03:38:02 GMT  
		Size: 16.6 KB (16596 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:8c015ec70ccab65807a2c967d1afec4b8d700280385ece8ea6c15a4d73d0ce01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (190998421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8518ea48742ecc8349099c76010075ac4aef75068a78d796de9b8c2df53a6641`
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
	-	`sha256:42948e38dfef62917f0e859531aad0c12af86cbc4d41c161cc293ff4019a52f4`  
		Last Modified: Tue, 30 Sep 2025 13:41:20 GMT  
		Size: 88.2 MB (88206411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06b98ecfc528bbfe44cd8d7e556cae89348ab45163db3536faa5ddc02c72b62`  
		Last Modified: Tue, 30 Sep 2025 19:31:40 GMT  
		Size: 73.0 MB (72953740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599ca3bc2712ae3d8176b332787bc52c741f8ccf5654ac1ec71e9fbb27522ef2`  
		Last Modified: Tue, 30 Sep 2025 19:31:31 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d46c753cd594e5fdfa025ac55e82bf869cc572cd4ddb4e3bc4d38131189de3c`  
		Last Modified: Tue, 30 Sep 2025 19:31:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e1d12c0a5a9750ca73ec898866d1ae69a8fb00f3a47506df9e9a02778661408c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5222459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53d5a328e570131b8681f86c1abdeebae41905c9c92b9a199596a2ae494e2401`

```dockerfile
```

-	Layers:
	-	`sha256:b75a9500db93efca04b3fa77e657907a930b10fe95d079e2b6ad67239bfa7378`  
		Last Modified: Wed, 01 Oct 2025 21:46:20 GMT  
		Size: 5.2 MB (5205923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a90b200a96e50a446589acffde2852f202478d2dd027eb21777f743a8d7aa1f4`  
		Last Modified: Wed, 01 Oct 2025 21:46:21 GMT  
		Size: 16.5 KB (16536 bytes)  
		MIME: application/vnd.in-toto+json
