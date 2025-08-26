## `clojure:temurin-24-trixie-slim`

```console
$ docker pull clojure@sha256:67ec745cdc9a3daec22a318cde0c17b6cc96e71f0b78d6d300be1ecc4f59f2f9
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

### `clojure:temurin-24-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a98382320e74e999b26e78235b4e7d132a39d2bc05c41002828bb7255b595341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 MB (191731874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875fd323993c9d8a075350fc53bf028b38d47c3aa60c65c61f1351375e87df2f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8416f29fca1026c5c7a3c8384a49ce4c6feefccc6be86dab25a49668aefcf36`  
		Last Modified: Tue, 26 Aug 2025 17:28:26 GMT  
		Size: 90.0 MB (89975231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca0b19c0abc80869a51987f99243690c29372c1f15a5ddfe013414c844ac57a`  
		Last Modified: Tue, 26 Aug 2025 17:27:40 GMT  
		Size: 72.0 MB (71982317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17045209dfea8885051d2086f1218a9bcc2b6c2eda6d8a8389b8e3fd899dfad8`  
		Last Modified: Tue, 26 Aug 2025 17:32:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b7fc08c00879e3915edbf78e7d9813b630a58de2bd0e4f6cd96e4535c6fb79`  
		Last Modified: Tue, 26 Aug 2025 17:32:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c5b0cdcd9047e8c2ce6f8227289fb6fa3804091022a6701d020de54de93b9b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5221733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06fc585ed345baf88b59889eea8852f1c8c91f8a0335d5d292b28b0ec5934f7a`

```dockerfile
```

-	Layers:
	-	`sha256:8ff5293c604f843de81052eaef13853d42df2c0d70adbe1bdb199983d41ec6ef`  
		Last Modified: Tue, 26 Aug 2025 18:43:05 GMT  
		Size: 5.2 MB (5205885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:238763448f0a2c268f846f38d663c74e8a5bdbeeece932b34f910110dad7f59c`  
		Last Modified: Tue, 26 Aug 2025 18:43:05 GMT  
		Size: 15.8 KB (15848 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:aafd0b580bbf84593e20f095854e71caa4e0c939d65c4788c500e44f7a2fad91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.0 MB (191033243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c853b4fc46f913fa3c8f5979040089f1dfab9831424a5f769dee3bab8e29c30d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe54333b06ad8dc6a1c19356b2654e06d357097398ccfe7bcc23b46b25aca1b`  
		Last Modified: Mon, 18 Aug 2025 17:25:14 GMT  
		Size: 89.1 MB (89092501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432e489d4777f64036ef55d59490f9cdca26a201ab682742854572244a16b1bc`  
		Last Modified: Tue, 26 Aug 2025 17:59:07 GMT  
		Size: 71.8 MB (71803654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c6f7ab409941e185c29ab3bd060e825a11db4cb6fb8efffefaccc9c5cb6fcf`  
		Last Modified: Tue, 26 Aug 2025 17:58:56 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e63a0f205a7516d2859b9e9459ed964dda9038a7cda1e233e603dff006e2519`  
		Last Modified: Tue, 26 Aug 2025 17:58:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:18c0a50e45cd73738202c7c7bf6a0113157e5ef7a592da2ae1ad49b977e48552
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5227617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb24945a92b9347949d8e66d9b7a0bbe70275237a844f3086153d69db8e2035c`

```dockerfile
```

-	Layers:
	-	`sha256:d1df14bd68222f5c79aaf51a403e88e6f324b8a790f53b9f03ebd0b2c2bbb719`  
		Last Modified: Tue, 26 Aug 2025 18:43:12 GMT  
		Size: 5.2 MB (5211651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe98071523545ab8248cf53257d917533ec297ddd1b68499a9af9d0c03a86a24`  
		Last Modified: Tue, 26 Aug 2025 18:43:13 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:07b2f06a70a42905c946cb6958a2df22f955d00af0a950c95f1cc32a020f07d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.8 MB (200803791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca3f625c8f4915b508cb9258d43e42b865df21b27cfe9d3775b103f2b12ad65`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344e68d3b82d646b17664e62a5168a46a359609aeb0118f6b14ccf55dbdbe212`  
		Last Modified: Tue, 19 Aug 2025 18:07:34 GMT  
		Size: 89.9 MB (89918237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959181a9738e1b91b1b2bcb37af75b497e68825affad2df3b3c37c81fc619a70`  
		Last Modified: Tue, 19 Aug 2025 18:07:51 GMT  
		Size: 77.3 MB (77290297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96e24da669fc2e3faa77a6fdbfd91843e863e0ee4af48d24b5a56e273aeb64f`  
		Last Modified: Mon, 18 Aug 2025 17:51:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d738df5078ad7d302705e1989ce9757b89b51f8913ad3422d3c855deeaf6dd98`  
		Last Modified: Mon, 18 Aug 2025 17:51:49 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6fbe1bfe9579bfda72dfba40cb8f96b2011f00072cd13192ca3a5208b6c36ec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5227450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db91518528770e4b976409d0a65e02ddd0a7555660e6b44f2192ae772bb58828`

```dockerfile
```

-	Layers:
	-	`sha256:9ef6e68ce4a8e4cd72e7a9f19d289049dff79653bef2dfe83b6f2d58fd4e1872`  
		Last Modified: Mon, 18 Aug 2025 18:44:11 GMT  
		Size: 5.2 MB (5211554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65734fd225161e6ddad6ff8746c5423431c51f52637b4b1a31db7571e030ec23`  
		Last Modified: Mon, 18 Aug 2025 18:44:11 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:e5ad9ae957dc4cf5bd57feac2d460aa99cdc9c67015797b3fbbe713ad7de465f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186723005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4683e4ee890057c549bb6ab4d444411b1e28b1623b44e6c8fbdd7c6baa417c67`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968e1c5a6cd6f5e83ac6331e97e27eeed78e5735d78cb563574656e787513c6d`  
		Last Modified: Fri, 22 Aug 2025 01:20:58 GMT  
		Size: 87.7 MB (87670405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67884805256a47d65d7ec9a2c746fa2d8f51cc16dcb468cfc469c67c7070a26a`  
		Last Modified: Fri, 22 Aug 2025 01:20:54 GMT  
		Size: 70.8 MB (70779933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e7c4d9afa1224e8ccb9753b885997c041bbe9cce4ca8ae071094441d4a973e`  
		Last Modified: Fri, 22 Aug 2025 01:20:45 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb3911c91090104d798588d784a03deb7cbfd17b7cb692ca95246af419f2259`  
		Last Modified: Fri, 22 Aug 2025 01:20:46 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dedb80b2367a5169792668da5f6f2d4bd6c5b99f6f6c4a54f08058329ed5aab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5211242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987cc135b59386ff29975e8906b8de75ee235e4444dc52d4505f4c1287d545ed`

```dockerfile
```

-	Layers:
	-	`sha256:3180eabdb9a894683e6dcc35322d19c67cfb0e3705b9473baebebd008d5df8b7`  
		Last Modified: Fri, 22 Aug 2025 03:37:47 GMT  
		Size: 5.2 MB (5195346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b8b7b5481bbc607af047fdacb7c9b5fac860ab7c71fc219916efbb44277587b`  
		Last Modified: Fri, 22 Aug 2025 03:37:48 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:473a81e5f15c0a473c1f38d155cb9866db203445c468d735301097f73cc9cb0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187911251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:902ddab8429102f485e68fe15d2b65c3c471ad5a24d6b3b33564cb255a25bc3a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec43252ef36a8b912f0b9161e21f8c05ad6c75f47c25da09877a4661719d555d`  
		Last Modified: Mon, 18 Aug 2025 18:26:18 GMT  
		Size: 85.2 MB (85226400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276d9ea90fb039a57d302e922d0eeedefbc6190a95927653e3c07861b7b04e3e`  
		Last Modified: Mon, 18 Aug 2025 18:26:14 GMT  
		Size: 72.9 MB (72850752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1289937791073124aa0362d7ab68ac616e08e046a8b1e36c5723b9799c496105`  
		Last Modified: Mon, 18 Aug 2025 18:26:05 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15040d2cd667056dde49804eb29b00b83bd3addfd6db2144f3ef9c931bfa49a6`  
		Last Modified: Mon, 18 Aug 2025 18:26:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9d29e07871ddc620c863c662462f92127054b8df9ebb9ffeb7ab231fe3701b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5220205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f6a3f3500b9c9d77a823dd38882020b92770b2c1d4994c6796407c9a6fa7a27`

```dockerfile
```

-	Layers:
	-	`sha256:9cc37780e0e229ae0ffc24502786b74100d9f4fd8cfa4cc12df90a884dc81a3e`  
		Last Modified: Mon, 18 Aug 2025 21:37:01 GMT  
		Size: 5.2 MB (5204357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e7fd77cc7b08c1f1c6639b3f39024b8bb7fe10e66f8304cf256c5d7c5145ef5`  
		Last Modified: Mon, 18 Aug 2025 21:37:03 GMT  
		Size: 15.8 KB (15848 bytes)  
		MIME: application/vnd.in-toto+json
