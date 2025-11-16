## `clojure:temurin-25-tools-deps-trixie`

```console
$ docker pull clojure@sha256:0b27a9d60158961fd80b8c0e1abc6f1fe75fede9bb88a60c7565cdcb62ce5071
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

### `clojure:temurin-25-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:3ca07dc1c13a120482372e48f7edd6149e71daa32a1a3e600140ba35a5f51124
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.9 MB (226872244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89b2b0b681603d4810e1ce6bf3278a3e27fa1a1b46fc58ca377f842e7937ac7a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:56:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:56:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:56:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:56:24 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:56:24 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:56:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:56:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:56:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:56:40 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:56:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403eb0ab940aecc282775181915dd2a23a7e14bb534306d760712d5c278522a6`  
		Last Modified: Fri, 14 Nov 2025 00:57:20 GMT  
		Size: 92.0 MB (92045286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab70270d1b80999bf64cd25ff05470f9bd87851d41ac223a6f6a53f1ec1a5cbe`  
		Last Modified: Fri, 14 Nov 2025 00:57:16 GMT  
		Size: 85.5 MB (85540289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c460d92fcb75e46cc1e361e3430467f699cffb6f7fd7e3762d16d412f55eb8`  
		Last Modified: Fri, 14 Nov 2025 00:57:06 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7bd001c8b8b31051728f35ae090195b1fe1a16bf5589bd16c1848a20930a48`  
		Last Modified: Fri, 14 Nov 2025 00:57:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:04b4f65a72c845c3ba07ed62ca6da6406534ac5d83b60ae16e409a39e6b57a56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7434646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d630e7b0ca6a540efa0c96a5bb4befac77f089606696b6c9418897d71aa4a61`

```dockerfile
```

-	Layers:
	-	`sha256:23b51afbe0e4450240ffbafc501b5b79c3a6baa28cc215955763301568e376f7`  
		Last Modified: Fri, 14 Nov 2025 01:48:28 GMT  
		Size: 7.4 MB (7418231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cd7c7dd375aeee0ef15fae85af080b6a034748ad61c22d96e7f66b7454892d4`  
		Last Modified: Fri, 14 Nov 2025 01:48:29 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9da7de9fb3c6d0740d5889aecd75aa467213a9c2183f848a35cef03c20303fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226067467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fcdd3c2d2fb644ee12b68ffcac5da32323f52940f3dc0b8e4d9184cebcd9f99`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 00:58:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 00:58:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 00:58:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 00:58:59 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 00:58:59 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 00:59:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 00:59:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 00:59:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 00:59:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 00:59:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2b5cad14c00ff3725ec593788264723530adb9ff6b1718c4f69ba7e81f88f0`  
		Last Modified: Fri, 14 Nov 2025 00:59:58 GMT  
		Size: 91.1 MB (91052531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0981f7fe4ba5d9fee5ccc2fdb8545f550f4477fc157bd46c47568aea8beefd8c`  
		Last Modified: Fri, 14 Nov 2025 00:59:55 GMT  
		Size: 85.4 MB (85363464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d64459861532b7f8029a5edb8f9ec0d9a8fc7595cfb0d48decda71984776b62`  
		Last Modified: Fri, 14 Nov 2025 00:59:47 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df76c40cc262c92bfdee4b2da8371071e9472b8c8225ea34d3ebfa1e8e53f849`  
		Last Modified: Fri, 14 Nov 2025 00:59:47 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:eb090cfe0c98fb060b5ba82a8a758ffa35e1bef7ea30c101aa9131f72c6df52b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7441837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37cf14bc8bfbc487b9870e1f1568bd3a39924b9fa095c8430740f4e585d72a18`

```dockerfile
```

-	Layers:
	-	`sha256:ae445458d93ff6dd75a5b04dba5849cdae4b83c78b512cd564f56f169d220197`  
		Last Modified: Fri, 14 Nov 2025 01:48:36 GMT  
		Size: 7.4 MB (7425282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9be0b07d603edf6fcabba3e1a5ac6282cdf4ec2942d66b96102347117b5a32f6`  
		Last Modified: Fri, 14 Nov 2025 01:48:36 GMT  
		Size: 16.6 KB (16555 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:fb259c0f08fa27be1592040be0c3e46342766e73949819a87e79624c12032b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235671478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deae522f90333030f74786b43043bc57663e44bb5942fe4334e1ed1034b1e3bc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 07:37:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 07:37:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 07:37:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 07:37:21 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 07:37:21 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 07:45:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 07:45:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 07:45:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 07:45:39 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 07:45:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3c335bb15935da0eae5ce30111cfa6a289c813162bada9fd389d8ae5510d5d66`  
		Last Modified: Tue, 04 Nov 2025 00:20:22 GMT  
		Size: 53.1 MB (53110127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fca0d27d8996ef66dcabcb59cfb3c0eebdf10bc7ec89045b01223b384d9ee00`  
		Last Modified: Fri, 14 Nov 2025 07:38:48 GMT  
		Size: 91.6 MB (91610768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c5c5adda99b958d253b9c637235a27af62b48b5e4f2ec764890026e8f84019`  
		Last Modified: Fri, 14 Nov 2025 07:46:36 GMT  
		Size: 90.9 MB (90949538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4dd86a101c319bffc0f2aa5d292f04d07610f0250b1c459d9b9f85ed09bd20`  
		Last Modified: Fri, 14 Nov 2025 07:46:29 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb168fa31676cbe767d73530aaec9e4d26c135776380d80c7d84f9c25f4aa38`  
		Last Modified: Fri, 14 Nov 2025 07:46:29 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7182cf218ea2dde44167fb14e8e72148aaf8c8764aa85259e7bac06d79d1d526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7440434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd96326ec4f10e78bbca0d1165c6a8cef3d133ce144157204e95cd384d5af68d`

```dockerfile
```

-	Layers:
	-	`sha256:e0ac0bc9385d85be37c32b467b16043b708aff5deb5b785e5dca108fa02b291e`  
		Last Modified: Fri, 14 Nov 2025 10:40:40 GMT  
		Size: 7.4 MB (7423960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fc40e577a5b3339bda9bf9db7187133d79b006fe32eda2e696f9790e5dbbdc7`  
		Last Modified: Fri, 14 Nov 2025 10:40:41 GMT  
		Size: 16.5 KB (16474 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:2174818d877424ab8ec0ca43dc6a07e44704b00373becce62c68918f38973f47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226109637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b08a94508a1470edd87db7df92c2a2bc7f4401caf4d10b0b19b6c3673b371ebd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Sat, 15 Nov 2025 22:18:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 15 Nov 2025 22:18:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 15 Nov 2025 22:18:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 15 Nov 2025 22:18:32 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 15 Nov 2025 22:18:32 GMT
WORKDIR /tmp
# Sat, 15 Nov 2025 22:39:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 15 Nov 2025 22:39:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 15 Nov 2025 22:39:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 15 Nov 2025 22:39:53 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 15 Nov 2025 22:39:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:de6b66e2abcf55248485e438d6def9b92cf28773b7cd7896ee78f9409b6e7526`  
		Last Modified: Tue, 04 Nov 2025 00:27:48 GMT  
		Size: 47.8 MB (47770924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a46ebd6f56fdb6d1c0e17f14db200e703d8de3e8f2d436ad48d3420edcd35b6`  
		Last Modified: Sat, 15 Nov 2025 22:24:32 GMT  
		Size: 90.8 MB (90752842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c692c2db63f826e49e4a8b9c01397f2d292210c8f1b4ca58a6d2feecf2d8287`  
		Last Modified: Sat, 15 Nov 2025 22:44:31 GMT  
		Size: 87.6 MB (87584831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e11d8ac7eb45806acfa0b09d21d64afdacea6638111f9efceebec5015c5e5c5`  
		Last Modified: Sat, 15 Nov 2025 22:44:25 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7df507f8ec72920728163aa7d08d885139d294a384bc3759b06320aff863e1`  
		Last Modified: Sat, 15 Nov 2025 22:44:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:dbffd57719bc63ab8296e93dfe4c1e19997f7cbf24784b84ccc3cefe5fb23fed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7422658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8026ff7c4c9d243c02529d582029f1bb6259d64e76166df072b1e2f1d439a31`

```dockerfile
```

-	Layers:
	-	`sha256:93c43ecf85a8f17ed1ab8ba7ea33c58e83171b8bb8c36ddcbfaa0905b6a65310`  
		Last Modified: Sun, 16 Nov 2025 01:37:19 GMT  
		Size: 7.4 MB (7406183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14395d09a15f8c158ca89e670da06ece0466555dc4c8d9dbfc6c2ee1bd39bd1b`  
		Last Modified: Sun, 16 Nov 2025 01:37:20 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:8c5dc763f9362b3df4db5aa65ecf6605722a4549cc5a88e4fb2ce60d131d9fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224072294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de9b2fc3785e8de6bda86a03586fa78abbea5ecf7cff204ac6973478aacb21d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Fri, 14 Nov 2025 01:05:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 14 Nov 2025 01:05:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 14 Nov 2025 01:05:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 14 Nov 2025 01:05:01 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 14 Nov 2025 01:05:01 GMT
WORKDIR /tmp
# Fri, 14 Nov 2025 01:05:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 14 Nov 2025 01:05:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 14 Nov 2025 01:05:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 14 Nov 2025 01:05:21 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 14 Nov 2025 01:05:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:48bd359f940d437208e8579c571291503fa327e04a66a6c8d918cfe93cae2e1e`  
		Last Modified: Tue, 04 Nov 2025 00:19:45 GMT  
		Size: 49.4 MB (49352299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2a8a9fb8e930a57765ce42ae03395a4025a6a0a9e7231a907d0ce397171256`  
		Last Modified: Fri, 14 Nov 2025 01:06:11 GMT  
		Size: 88.2 MB (88210681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c76661e3348cf2d3849cfb8da7b8d0ea4f8b6b10ef62348adc4b9081ee9cb1`  
		Last Modified: Fri, 14 Nov 2025 01:06:12 GMT  
		Size: 86.5 MB (86508273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41635d7e530d7dcd21fbc02df90681995bce8f13d7f5af8b473b9b238552431a`  
		Last Modified: Fri, 14 Nov 2025 01:05:57 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f9ef295420f18fda5f94157b923d25ad06cc683a10416009c7587689eab7d0`  
		Last Modified: Fri, 14 Nov 2025 01:05:57 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:7f2dc55fc47a5ab00717da173ee715bfa06100c100bc8dcf90b449a3d27b5704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7433116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a11e211b94213926e4f211c153eb0a64a7c74e6c77b74ce092954e999e00934`

```dockerfile
```

-	Layers:
	-	`sha256:4dd7669d9c33a2b4a873facdc4af1975c4352cb725d907dd643950607d5306eb`  
		Last Modified: Fri, 14 Nov 2025 01:48:55 GMT  
		Size: 7.4 MB (7416701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba7a13dc11feebb8331eccf53e4213849af69f4bf3a14d97608ad11310eb8b8f`  
		Last Modified: Fri, 14 Nov 2025 01:48:56 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json
