## `clojure:temurin-8-tools-deps-1.12.1.1550-trixie-slim`

```console
$ docker pull clojure@sha256:8fc00bd0dd6f7214ee52615d012fe0b2da3e49cc48fab6c80fda0bb712169877
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.1.1550-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:86d59784a6e9475546fd0088ce10b0106a5c9a0e4fc4b6eddc99889ddb9896e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.3 MB (156345670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:849ea9349d24a96e63d6915df8beba4553fbe93f3e2b97699a121d7161bd1049`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a020bfe07782e8496e55df2accd3671feec820402e5150fa2c46cd21eb03da`  
		Last Modified: Tue, 12 Aug 2025 21:34:52 GMT  
		Size: 54.7 MB (54731354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dca6c5d4310db5360fe6eceed3d8027d1cbaf3b335a6f0b1f501640a81d5637`  
		Last Modified: Tue, 12 Aug 2025 21:34:53 GMT  
		Size: 71.8 MB (71840389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4392cb4f8f42488611df0fc29b970d367d47820d3c6660a4854a58e8d5d6bb63`  
		Last Modified: Tue, 12 Aug 2025 21:34:50 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:429017d3313a0b8f2261f272c68f37c331f10a3faf8d8087dbbe0e94c2576d5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5391086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd5d856155e50e7935aa270ab85a6122e0f2135ea9658aacc75f0652a190004`

```dockerfile
```

-	Layers:
	-	`sha256:4fa6d16f6019366aa005b7a972de4d7e9d118f5272ac90a61a298eb37b7d53b8`  
		Last Modified: Wed, 13 Aug 2025 00:42:38 GMT  
		Size: 5.4 MB (5376818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c08a47ad727440302b34dbfe50aa116670ad66ebc77883716e9234b937a8ee68`  
		Last Modified: Wed, 13 Aug 2025 00:42:39 GMT  
		Size: 14.3 KB (14268 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.1.1550-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ad12e7e079e6b972867803e26e03e51e1e96f8653b775e47e58f23f2870dc0a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.6 MB (155635808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f44b333ac897cb5b8d90cbb866e7632375eecfc18853130954b14770135f8e`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b020be334f1de1bd4d9582643e5d90be19d9eaca83ff137a0359573efe5c59c`  
		Last Modified: Wed, 13 Aug 2025 16:15:29 GMT  
		Size: 53.8 MB (53835607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4932e73cf437c07d668acaf20c1a3f753c38a26b020948a752cb8bdc472b049`  
		Last Modified: Wed, 13 Aug 2025 14:10:24 GMT  
		Size: 71.7 MB (71663513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552d88870e9b7c31064a57f8c314d3fbaca0569a1e4f2746fa6ecab5567485ef`  
		Last Modified: Wed, 13 Aug 2025 14:10:07 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7e3e644647d4dc255cf879346c3bffbe496e39364beabffdd68dfcaee2870a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5397674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29319c000831d3286a01e00c42218f9d366264d42221811372350bde0fcb8eb5`

```dockerfile
```

-	Layers:
	-	`sha256:820e96771d0c5ff9b787e8213fe49c99161e8ca588d1801d4ecdd8ee9b5fb617`  
		Last Modified: Wed, 13 Aug 2025 15:43:26 GMT  
		Size: 5.4 MB (5383285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:711da63b4e5302e74174232370be16e9fd627d113d0cd325fa6a40d73b36b134`  
		Last Modified: Wed, 13 Aug 2025 15:43:27 GMT  
		Size: 14.4 KB (14389 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.1.1550-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:60bdf174d3cb38fb20f28db0d8a02b0ea689596acb7246fe6d01341f6274e81b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (163006881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af5b94a2d92a97af2df09ed60ad056a5278e32dd49f1970831098eadd904ac0b`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f15fa0d26e779ea32b956f9c74aa95362d3f7e4b0e8d04a1c875819f54a0130a`  
		Last Modified: Wed, 13 Aug 2025 21:10:24 GMT  
		Size: 52.2 MB (52165400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b1796ca837227abde40f3158401259c1453f084d29479790ec0bb8263d61df`  
		Last Modified: Wed, 13 Aug 2025 19:30:25 GMT  
		Size: 77.2 MB (77246623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c139fdd6733a906a2bcb3a570d1f5b359314e30cdc5fa581a8a88583145da63a`  
		Last Modified: Wed, 13 Aug 2025 19:30:09 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:527c7698b111220696a7f74ac69d1a1e80303d70a0084f6fe17ba291de88fae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5396101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875dd6d5004b31f2665b1f06f7aeff0701444faf407aa83d0099320858666d21`

```dockerfile
```

-	Layers:
	-	`sha256:d22df3692c27ac498297a4b9cb9939a65ab25ad77d73517a538d967b9bb8c691`  
		Last Modified: Wed, 13 Aug 2025 21:41:18 GMT  
		Size: 5.4 MB (5381782 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2750d1442d0e596348e70c4aba55bcaec6a69b7494f209e3b9d3569f58d279db`  
		Last Modified: Wed, 13 Aug 2025 21:41:19 GMT  
		Size: 14.3 KB (14319 bytes)  
		MIME: application/vnd.in-toto+json
