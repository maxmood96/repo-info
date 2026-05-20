## `clojure:temurin-17-tools-deps-trixie`

```console
$ docker pull clojure@sha256:2c041a3de631d2ff1134f2bc5ddf72795b00badbbecde61dac50c58866e1d97c
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

### `clojure:temurin-17-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:6fd302ecfefd537b841a91f5df96135ce205c633552b9c1ccade307c392cd040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280824604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e2a62bec10ccdfee9735227337067350819cea7631d9f9179d8bde463cd9ee`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:59:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:59:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:59:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:59:10 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Tue, 19 May 2026 23:59:10 GMT
WORKDIR /tmp
# Tue, 19 May 2026 23:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 19 May 2026 23:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 19 May 2026 23:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 19 May 2026 23:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 May 2026 23:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109fd49aa4bfacdaeae0f68b962a3a0ff088710278fb4d60c2c7616efd3c8484`  
		Last Modified: Tue, 19 May 2026 23:59:49 GMT  
		Size: 145.9 MB (145905476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d44c16ec3e658368dbcf9f0d080a08de9786763c8c53e6d7dc49af91ff77b6`  
		Last Modified: Tue, 19 May 2026 23:59:48 GMT  
		Size: 85.6 MB (85607463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f558a831ccabf9de81e3761a25a234da59177c7e20c6c2bb0563511a77b6338`  
		Last Modified: Tue, 19 May 2026 23:59:45 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bfde21397b7d08e48215cb6d74398ee6134a9142d4a14ce9613dadde6846aa3`  
		Last Modified: Tue, 19 May 2026 23:59:45 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:155618b9bcd6bfc522f7a71532a1fcaed9dbf572266de296d1068325b90b6e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7487404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5962cd15240d337905f17c70b3faf78ff7a7419dd73479500836dd5d0916d0`

```dockerfile
```

-	Layers:
	-	`sha256:ab6a578b498ae1b6c7b80e6a10bb659ce3517b2871c592099c2297007386eda4`  
		Last Modified: Tue, 19 May 2026 23:59:45 GMT  
		Size: 7.5 MB (7471496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a57e0e1c6ba66e8ad28cf4004b02fd553f0b50bdaba8c68c09cb3dc9597b15ed`  
		Last Modified: Tue, 19 May 2026 23:59:45 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:df14d1dd6e25996a3c2bd879a0a9822426976fa36dbcbfe2310dd6cc6896288f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279829634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98d38f6039edbfe057886aafbe5fc5318e6f86c26654f2b47e9a7b0ece501b6d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:06:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:06:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:06:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:06:15 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:06:15 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:06:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:06:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:06:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:06:32 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:06:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934929ff9f16f89563fafd9fac6adc194b6543d7e750222b702c18d8be093859`  
		Last Modified: Wed, 20 May 2026 00:06:50 GMT  
		Size: 144.7 MB (144724336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3727efaab637984e5eb7943aa519aa9a29d34eda4bdeda35777ab6d086d56f53`  
		Last Modified: Wed, 20 May 2026 00:06:56 GMT  
		Size: 85.4 MB (85432039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85f5cfb8dbd68d9c4d963127554ad70010557d66e784e83c13e17c2cb535b06`  
		Last Modified: Wed, 20 May 2026 00:06:51 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92fc21253dcf377c7fbcdb40ff627129b205a06a8dfe9a9a4ac6de1746e7ae9`  
		Last Modified: Wed, 20 May 2026 00:06:51 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6a0de984340463dff08fc2723b8165a8764f06560c3aa7e67ee79456e9e0b676
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e13edd7e533de8612a2b2d76fe02624a9ff76196cb636ad4af3f3a2dd73dbd52`

```dockerfile
```

-	Layers:
	-	`sha256:f535eaa8e6194c927c27685583e2247c9bc4d0ced2dd2e09113a434bd47edd57`  
		Last Modified: Wed, 20 May 2026 00:06:51 GMT  
		Size: 7.5 MB (7477889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5495be2dca635037eb245df204853c2026fa8de4ce6e74e4ac37ee2b205c9f93`  
		Last Modified: Wed, 20 May 2026 00:06:51 GMT  
		Size: 16.0 KB (16026 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:736a7a186c160a3e44ef1bf5fd9f922c48bb02331815bfb880b67bab6746aa45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289926581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c364805c617d89844571d8693b56d5854272cc69e9c756e55a3ceacc8bc86bb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 05:55:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 05:55:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 05:55:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 05:55:54 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 05:55:54 GMT
WORKDIR /tmp
# Wed, 20 May 2026 05:59:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 05:59:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 05:59:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 05:59:43 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 05:59:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:55497c62a793e62a2e78a3fd85fcedf060da73e331ad107733199ea991106b96`  
		Last Modified: Tue, 19 May 2026 22:37:59 GMT  
		Size: 53.1 MB (53132182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27b520fdf7e3554efa0af356645dd5dc149e4ce0f85e4af1780a538faa30f86`  
		Last Modified: Wed, 20 May 2026 05:57:20 GMT  
		Size: 145.8 MB (145766112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2adb210a7942e88667e43be4eb28fba6b4ab867efef34140d22fdcf4f3db68b`  
		Last Modified: Wed, 20 May 2026 06:00:26 GMT  
		Size: 91.0 MB (91027244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4628616af9c1c7f880a06cbd838bd1c5305e5f375a2ad075a17c774ec8ae0d`  
		Last Modified: Wed, 20 May 2026 06:00:23 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744eaebf0650708b3da8897636d321a9849296f3c3a9431f557a95eca52986c7`  
		Last Modified: Wed, 20 May 2026 06:00:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c2a2d1a441661748447c2ce2516f62c9f3848d9f121c0dc82a24c1a1222deb7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7491873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb5708d37a4f51623323e1786f346f89d5dec048115109f5be8628a9cae5cf93`

```dockerfile
```

-	Layers:
	-	`sha256:9c7bcc4618015b898fc936c822aac5849da1bc82e285bccfb6bc427ca25bfe84`  
		Last Modified: Wed, 20 May 2026 06:00:23 GMT  
		Size: 7.5 MB (7475917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b54aee443d248f837b07af1a2d37d4cdf5582a4599a693123eab9660a15e8fe`  
		Last Modified: Wed, 20 May 2026 06:00:23 GMT  
		Size: 16.0 KB (15956 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:4ac307590d8305424885d9122628de11f18cf8d1958d8ed3a0e196b7b387af49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271881787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78743fa5c6b482f4603f7af64a5aa997cf507e7d2e6010589c89ab45b437b54a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:43:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:43:42 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 01:43:42 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:44:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 01:44:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 01:44:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 01:44:57 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 01:44:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1540dbb0587ae9097c9d04c50809503aa74d42814940d640c6659645acc0bc6c`  
		Last Modified: Tue, 19 May 2026 22:37:00 GMT  
		Size: 49.4 MB (49379780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e6aeaf690365e231d191405438cab335606f7f662847488b61ec9fe50ce0af`  
		Last Modified: Wed, 20 May 2026 01:44:23 GMT  
		Size: 135.9 MB (135910432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e15eb3a53f1dad651c0d89ed341e1da21d7e793607a848f0e80a67b8e80ce3`  
		Last Modified: Wed, 20 May 2026 01:45:24 GMT  
		Size: 86.6 MB (86590535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adae7326f127151aae2b1e77bd2e9aa1b7ca62ccf185834a5fd65ee3c41c30a0`  
		Last Modified: Wed, 20 May 2026 01:45:22 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be613211315e837afac3e808945febf5049b912e0600a38398e86a7b0244a8ab`  
		Last Modified: Wed, 20 May 2026 01:45:22 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:58cf925ad565d480b49b2bcf18f5c15fede828d934a301cd48fc1c12f7bca8ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4f06eb43e854638a3337a14536cf3f13a4e0dde09dadb81778bbdd02fd3e0f`

```dockerfile
```

-	Layers:
	-	`sha256:4cf5e2d2108e5076ff0a97ffbab418012489140919cd2dc91179d356db1d19e8`  
		Last Modified: Wed, 20 May 2026 01:45:22 GMT  
		Size: 7.5 MB (7467418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11bca84af8215c14c4aa800fa3023e5231d480daa57a94568e109fd277469411`  
		Last Modified: Wed, 20 May 2026 01:45:22 GMT  
		Size: 15.0 KB (14953 bytes)  
		MIME: application/vnd.in-toto+json
