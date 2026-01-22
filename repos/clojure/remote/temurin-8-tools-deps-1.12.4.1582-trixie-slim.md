## `clojure:temurin-8-tools-deps-1.12.4.1582-trixie-slim`

```console
$ docker pull clojure@sha256:fd413127adc843000d3cf60938a1af94ccc80f405bb79c6c7df1850966c45948
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1582-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:81191fc912510813d635420976d0296ef122d6a0942beaa2ea6033fad6093895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156500997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be8100ade01302022b87c5eda7454ff132dac89b4f33600bc7a1a2f47a3fe28a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 01:45:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:45:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:45:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:45:23 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:45:23 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:45:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 01:45:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 01:45:40 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7cde224f5b269e54a311d0a5b8b2aca6ff0e5cace927db6cf558e609e0e6e5`  
		Last Modified: Fri, 16 Jan 2026 01:45:58 GMT  
		Size: 54.7 MB (54733366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84af28c2d91c7e5cfefb8787cef527bd83ddc6ec4ec09554f9e2ba7dd4238d2`  
		Last Modified: Fri, 16 Jan 2026 01:45:58 GMT  
		Size: 72.0 MB (71993301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32fe0b4ff62ea3555df18a591d93e9fe9f967bdcfdee260cd4d6ee8c8d2f3543`  
		Last Modified: Fri, 16 Jan 2026 01:46:08 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1582-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:43464b97074160d3fc476c5d19da9f50394e66e06af0c91c62627a7a905a2c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5392133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fab6cf4ba362575fda52b04f3e3705ba683949a50c5182fc0c004c1289e5b91`

```dockerfile
```

-	Layers:
	-	`sha256:f3a7672475ff19d5870f156cc28db36419d7755ea9bcc3e68695dc050b29845c`  
		Last Modified: Fri, 16 Jan 2026 01:45:57 GMT  
		Size: 5.4 MB (5377905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:225dd1a633ecd19c4fef4bef411cefef8b4a838ea64bd5b8c90733b21b48db22`  
		Last Modified: Fri, 16 Jan 2026 04:55:21 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1582-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:33674f3b1f2dae23b3a4208e7c6e96a34843cd19c8ca083081259ddd6d486076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.8 MB (155755897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c652f621f350cdc8c5ebae2f207560a14d0f6defa61d3be02c3f224c2e4db2`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 01:49:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:49:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:49:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:49:10 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:49:10 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:49:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 01:49:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 01:49:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a273c659470b446bfee3cefd5cf10225955df1ecad224fcfb03b052a7c3aeb`  
		Last Modified: Fri, 16 Jan 2026 01:49:47 GMT  
		Size: 53.8 MB (53815013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0b443b0ca0e6c00a5ab005329c37f8a6a8f090a6893cdbd0c24593d910f036`  
		Last Modified: Fri, 16 Jan 2026 01:49:47 GMT  
		Size: 71.8 MB (71806199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e70c7296b8ef01677514e26535a2a09f008acf3e2ca1d991742a8da31e6a5b`  
		Last Modified: Fri, 16 Jan 2026 01:49:53 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1582-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c348f219fae01a5c1af3d6d67e1b16d0b6623e523afccf24ba498d7fe4ef63ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66bb9e667461877024c0130384b54e607b470059a30b29dededdf6a3ab7fc7e3`

```dockerfile
```

-	Layers:
	-	`sha256:2bdba20fa794b490e5bc2d266a8eb3ff06b89f42a7279cb3c78257b6b911d121`  
		Last Modified: Fri, 16 Jan 2026 01:49:44 GMT  
		Size: 5.4 MB (5384372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19ff0592330ac323e9804a584a358289dcda8b47c70f741daff7c6ba99ee7e9f`  
		Last Modified: Fri, 16 Jan 2026 01:49:44 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1582-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:d060e905dc35d6a6cc7859c970d20e54dbb55d9795461591e81b59974ae6de62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.2 MB (163161517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55bdcc8129f974c8e2b151d324a704a81204b5322d6d11e3c002bed08c46a68b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 02:49:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 02:49:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 02:49:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 02:49:44 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 02:49:45 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 02:56:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 02:56:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 02:56:19 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b120fe6bca491b5d43488fbe9708b684a36bfbedc4a0256ac7fca0cabd7b42ee`  
		Last Modified: Fri, 16 Jan 2026 02:51:23 GMT  
		Size: 52.2 MB (52175136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2cf299eb8414e8cd98a6d2f5ee40c872642fc28b858ca56d813da88e18e5f0`  
		Last Modified: Fri, 16 Jan 2026 02:56:57 GMT  
		Size: 77.4 MB (77390135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83433a6cad21d5ca6bbdde0ad554d7ab6214ffdc14d748596b0c7ae498693cb8`  
		Last Modified: Fri, 16 Jan 2026 02:56:55 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1582-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2d283911558b46e94473f704593f2910c83736d1638a89acf71d08b1b59fe4af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ec63141a4cb5ee20da651b8f7762fa8ea1770c4313720fae36f33ee0dbb0c01`

```dockerfile
```

-	Layers:
	-	`sha256:b7d8ea8490f07d8cb68a2b32d7485b9a8a7a56060020797293983213cb1d280d`  
		Last Modified: Fri, 16 Jan 2026 02:56:55 GMT  
		Size: 5.4 MB (5382869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a71fa7f7dfcb7a1af793269df443fe34aee7da10c258b39fae2804dd01a7545f`  
		Last Modified: Fri, 16 Jan 2026 04:55:32 GMT  
		Size: 14.3 KB (14275 bytes)  
		MIME: application/vnd.in-toto+json
