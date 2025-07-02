## `clojure:temurin-21-bookworm-slim`

```console
$ docker pull clojure@sha256:de67e767e73dc7ce73b1b21bfc5c31565077007f9989cd4fa45470e451b0a6a0
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

### `clojure:temurin-21-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7f08591c2f94aab1ba821fa23f1ff608931215e15c3a3e4a44de1c02d8455d90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255399000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e18faea2167e3f1dfae30e41469075df8eb41add4a96af9aa78bc2cd2e0eac`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8620846a0622ca2e69fb27c9f932acf94b387307a9129dd630a0db956227d0`  
		Last Modified: Wed, 02 Jul 2025 06:44:38 GMT  
		Size: 157.6 MB (157634442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434bb917f7f33c93d254b54fc8481122459b3e4778e07a732719522a79b639fe`  
		Last Modified: Wed, 02 Jul 2025 04:17:17 GMT  
		Size: 69.5 MB (69533378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b69e61d07f0d80c49f3c70e36738d597af17ea933c8d8a04025f601bcdfc652`  
		Last Modified: Wed, 02 Jul 2025 04:17:05 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41aa0075be15059d5ebfea3302231c9c4125aa23dd733175f464e036fded302`  
		Last Modified: Wed, 02 Jul 2025 04:17:05 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9e7b7a4fd390d0737201278bd4de47109b63c6d103fa00d8ca14bbe6d834dab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5131617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35287ae6e2c13ff3e5d8c5ce2c35391abb57ba64d93e1cb4fc9c7edbd41689c6`

```dockerfile
```

-	Layers:
	-	`sha256:5a835f2771e5b16d1d49189804d7137156364a350cea13cc30c02480de08ee27`  
		Last Modified: Wed, 02 Jul 2025 06:39:15 GMT  
		Size: 5.1 MB (5115042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9145c0505e2f6fa251b16edfffa107475c8374699017900c946d013f76e6eed7`  
		Last Modified: Wed, 02 Jul 2025 06:39:16 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9ffea213d5a690efc509949d3520536631c6ac0a9897b1e9e3eceaef0f6280aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253396091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94c41199c40e1bb3bcae78d4ed1d77a619958334a52e47fa61dca29cc3d8494`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
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
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3acac392c98990c320593217a0d8bd8d0ffd8c866d1992689a7186665231aa3`  
		Last Modified: Wed, 02 Jul 2025 05:06:57 GMT  
		Size: 155.9 MB (155928844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512eeb512f8d9187eade339476e6eb962073ed849ce329671e26f94d6a63ac40`  
		Last Modified: Tue, 01 Jul 2025 12:54:14 GMT  
		Size: 69.4 MB (69388531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9633a1f6118614cad10fed69aaf785a4f38a0275871a8f5042abe173c777241f`  
		Last Modified: Tue, 01 Jul 2025 12:54:10 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4213bd6c11bbc7ebcfe32aac52ad03ed005350b6596eae8f9f74a4a538bfe1c7`  
		Last Modified: Tue, 01 Jul 2025 12:54:10 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d5f10fb32254207d0f993ed058c9330c23b932fa23e99496873b257e424c1dac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8a8fa66cb6a01e7796cbe27536206635153186fb4ea3298b00f35b5171a140`

```dockerfile
```

-	Layers:
	-	`sha256:51e7398d81ab4235ef22441022b7799f7998a261686e9834b4aedd43f3e79d79`  
		Last Modified: Tue, 01 Jul 2025 15:38:25 GMT  
		Size: 5.1 MB (5120827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3b1f54bd50dd974cd7bfd6931cf2d728edac2ff0205c71ca758fc40199daa46`  
		Last Modified: Tue, 01 Jul 2025 15:38:26 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:7d0aed9253dfbf4c2b25b226a500e4fd7d2b985ac4380f892e3ae7e7977d2a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.2 MB (265236679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3cac1387a40fd30760f6cf1b6b40aae71814bb77109f5580adb069555914980`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
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
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38654763bb3a63922902695f120b682d664a012fcc0d772bf4d0ef943e45880`  
		Last Modified: Tue, 01 Jul 2025 13:21:46 GMT  
		Size: 157.8 MB (157804904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a3329b1d5937bb0df91c6682f89b503048a1aedee95912689cb64395563015`  
		Last Modified: Tue, 01 Jul 2025 09:04:34 GMT  
		Size: 75.4 MB (75357918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884ee21b0b1f417255b4f140560b0bfb768585c9b40ab70b5292a5b5c9c94caa`  
		Last Modified: Tue, 01 Jul 2025 09:04:26 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34daaa86378fd8a52da12d1a74acbff73a2bb25937d753b588f45ca684513ecd`  
		Last Modified: Tue, 01 Jul 2025 09:04:26 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2c7ebf6843ddb5eafb691cb27ad8d753211a297ba3102ba6b0dc1c4aa6d6e5b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5136847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b54a6ada4fbdd31aee7b1d43a7c939cc8510c5c88254ba259837ac148a5c69`

```dockerfile
```

-	Layers:
	-	`sha256:e2736071e86ee6b659db03193346708ce9aa3b8137b2edda29142ce96cb36e1c`  
		Last Modified: Tue, 01 Jul 2025 09:39:50 GMT  
		Size: 5.1 MB (5120212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29d6fe63aa161555b1b0175286e679e3cb1f6f9f304c105ddff583b6d35f1710`  
		Last Modified: Tue, 01 Jul 2025 09:39:51 GMT  
		Size: 16.6 KB (16635 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:7120ecf6f988de2f024c33cf27405d23dca0f9a78b83ce4b2a550cbbac1ac5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.1 MB (242138735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:813ba970c185aeeb64c11cb8e55fc1882a03f4d3c27579d28ddc3d5a08e3ed21`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
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
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b8573fa47c2bc5409f11e03c513f5b48e958af3b508908c4d9437b6726eb8b`  
		Last Modified: Wed, 02 Jul 2025 06:45:33 GMT  
		Size: 146.9 MB (146910935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b04eb3acbff8fdb293c2623ddaa80d1a747983e79c8c5d8677c4e95feb949e`  
		Last Modified: Wed, 02 Jul 2025 06:51:22 GMT  
		Size: 68.3 MB (68338948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53525d4a166c4345aa43b64336710f53ab536e49c0f42ad42b922cee2f844d5a`  
		Last Modified: Wed, 02 Jul 2025 06:51:17 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089fabfd3b631238af3300a5f3753bc4c39eee13b9b3fc522de5b25b83b6498d`  
		Last Modified: Wed, 02 Jul 2025 06:51:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:295345c371feef83fb0eacb490634e620d9455bb52711b32499446915aeb59cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5122938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fdea127db53c84be5ca017cce2e3bf4b9a2e9c451bbe1d667a8154145f918d9`

```dockerfile
```

-	Layers:
	-	`sha256:450ac29819b6736d32c122d8ce7aa16970652c249e958804f101006c890a9f8f`  
		Last Modified: Wed, 02 Jul 2025 09:38:57 GMT  
		Size: 5.1 MB (5106363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d4a66d245dd9bb9fe2df76dc108f90ffecb8581dddc131853e42f29d6aaa439`  
		Last Modified: Wed, 02 Jul 2025 09:38:58 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json
