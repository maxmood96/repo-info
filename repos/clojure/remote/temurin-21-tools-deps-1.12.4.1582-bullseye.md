## `clojure:temurin-21-tools-deps-1.12.4.1582-bullseye`

```console
$ docker pull clojure@sha256:897ff296ad0da58c00a867b1e133c6440036e2eb96ea2f5efd01ae58ef111903
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.4.1582-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:f6a7451e0a15b93ccbdc56c83a1874dd62fc2e91da171be07214e544034b0d9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281140346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:184d8b6afaa3ed52931a0499bed561ac10c44e7b87f1926ab280f9992fd1a3bd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 01:02:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:02:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:02:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:02:06 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:02:07 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:04:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:04:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:04:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:04:19 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:04:19 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:81c5fe73ee38995b42041f20ff8af640cf790ab264e1dc7316c4c1de7eceb4f1`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 53.8 MB (53756440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4d22356725fdab0f82b1b5561ff42b014f41f21ea3cf9bdb01c5e3f9d960df`  
		Last Modified: Tue, 30 Dec 2025 01:03:15 GMT  
		Size: 157.8 MB (157826031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf00b7879bb5c8a131e01bcb970539271908baa102f90014ee9b497e8066906f`  
		Last Modified: Tue, 30 Dec 2025 01:04:48 GMT  
		Size: 69.6 MB (69556833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f60482d01dbbd11bea402235430ce63461ff3e8bfbd6f0d4b918624d4cfcb2b`  
		Last Modified: Tue, 30 Dec 2025 01:04:42 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a58f19031c289d619eddb36be75fed0b8ac98b0433b9e4bd81e9378e3f419e5`  
		Last Modified: Tue, 30 Dec 2025 01:04:42 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1582-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:68755ad83b0eebd7948dc29d2bbb0afc3a280b259eafd06bf6a2ac7d53473818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7413747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40733d61f14d00d34e37b3aaf2d87389f6420c17c256fb6e1804d6ca483fa260`

```dockerfile
```

-	Layers:
	-	`sha256:436bf124b948fef96a784160ebce2c6868ba5f8b4254a60d770546896f5c0f61`  
		Last Modified: Tue, 30 Dec 2025 04:43:14 GMT  
		Size: 7.4 MB (7398771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e18fc6bd861677ca5fba5ed0f3c4feb2bc67b101dc27da5322ab8b3fd1fff7a4`  
		Last Modified: Tue, 30 Dec 2025 04:43:15 GMT  
		Size: 15.0 KB (14976 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1582-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c78f060cebf66e3003df474e54249c854a5737c5074c243e2a8737d2293a0ba4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278053337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2942ef24dfec8e7f05aba379eb3867932125dfbb0be49fb4ac8f959c31b7fabd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Tue, 30 Dec 2025 01:05:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:05:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:05:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:05:43 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:05:43 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:05:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:05:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:05:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:05:58 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:05:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9cc7bc8e086c95eb3e992d2c623bd505740ab0a6afcbc89656d0bb477878489f`  
		Last Modified: Mon, 29 Dec 2025 22:27:00 GMT  
		Size: 52.3 MB (52257770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125192ad649368a3af3fe443e1b64b2166dbcc0b4d8792218bb440622fe22a40`  
		Last Modified: Tue, 30 Dec 2025 01:06:58 GMT  
		Size: 156.1 MB (156107580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1290cf781e464252e893bfeec44750636997dd3e974c23a2322d760e3a3e40ff`  
		Last Modified: Tue, 30 Dec 2025 01:06:35 GMT  
		Size: 69.7 MB (69686951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9246e8ef3410f1e5e196027daf3a7674f0f3df06c5411fc9db78874bec250e42`  
		Last Modified: Tue, 30 Dec 2025 01:06:29 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ea1381b1e0d04002b72f7f03c3e81d526db2c51f04eda77ae6fa9b4e1b0de5`  
		Last Modified: Tue, 30 Dec 2025 01:06:29 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1582-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f7583fd150455f1a266a1e6218be0f9a5831c4a91157b0e0613418806a0c46d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7419766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2267a58e97ec4b2b4a0d89903c13c35284cbbcac75a2234c36b4cfc3a3ce9b3b`

```dockerfile
```

-	Layers:
	-	`sha256:724c25f705be68ab7f796f964eb6b03a1a98c03f32b851ccefefb1d331cd3933`  
		Last Modified: Tue, 30 Dec 2025 04:43:20 GMT  
		Size: 7.4 MB (7403870 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d90ed7804c3ba10bca9929d310a1c83abdc7b9450ffa33e1e48a8496df08a7a3`  
		Last Modified: Tue, 30 Dec 2025 04:43:21 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json
