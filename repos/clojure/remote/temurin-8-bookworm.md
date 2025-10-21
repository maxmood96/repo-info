## `clojure:temurin-8-bookworm`

```console
$ docker pull clojure@sha256:0cd6e5dfc26ccc3bdf0646afdc84ff03bf37f78bc1e154ff3d7a5c4c8f7f067c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:1c5d010aadec7be214834c7a001de419b411ee346787c862a6916e117eb26176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184360255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16fa434f2888562e2117727f2698e787791c97dc0f09994e513b76fe8e7c54cc`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:cd01849e3cbdfc6993640303768edbb56372cf9f1ae101d516334c8d462341af`  
		Last Modified: Tue, 21 Oct 2025 00:19:25 GMT  
		Size: 48.5 MB (48480563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e06ed8be785b05a6a772c6ef87b12f7b35386d2c6ed1c108823225eeaf20e2`  
		Last Modified: Tue, 21 Oct 2025 02:19:27 GMT  
		Size: 54.7 MB (54731346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d92b8a8e377d8dca77e786d738e92f3c81ac59e086f58c407570f1dd014dbf`  
		Last Modified: Tue, 21 Oct 2025 02:19:29 GMT  
		Size: 81.1 MB (81147702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9523bb75122d89cb92e46f8ffe09a855e6eb9dd2a7731be1c950f94ab4fe54`  
		Last Modified: Tue, 21 Oct 2025 02:19:20 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5c3f80f0605271519a86a9cbdfa022de8ef95314654a89a33a04275e184c453f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7510737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5866759aaf0a07e71d8f83b179be8d6d861a5330b4c30e0a0012d7cb05e4e249`

```dockerfile
```

-	Layers:
	-	`sha256:bbd716661890b01e234eb744d5348dcf7c9252da7d5a23badfd20b9490c8fa23`  
		Last Modified: Tue, 21 Oct 2025 09:46:05 GMT  
		Size: 7.5 MB (7496500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1339bcc6ac74e5d733bb56ea55a97c065967732faedd5aa2a3fd30a29e50d444`  
		Last Modified: Tue, 21 Oct 2025 09:46:06 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cca30f533eb4861d3fcc551ec5c69064004443fbf0521e66538cacfe0fc77ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.2 MB (183223574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04db7082b02b979b7789000df0f3bfa704ce977bf0dc7cbd7c5b3da2f263facf`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:394d8e61f78f890cc5a49345ac4d4eb6176cdcf6b4b6af62502ae74b1662e421`  
		Last Modified: Tue, 21 Oct 2025 00:18:41 GMT  
		Size: 48.4 MB (48358996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a41a4082368fca66d66e5744f605939e7f45de7c6bc628da1f2eb10041bb67`  
		Last Modified: Tue, 21 Oct 2025 02:25:19 GMT  
		Size: 53.8 MB (53835606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd3a68cc128817927bcd61feb14adddfb30edcff38fc0b2494c59bec14f2d07`  
		Last Modified: Tue, 21 Oct 2025 02:25:20 GMT  
		Size: 81.0 MB (81028328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a58d00cb15469e05d447c6fdd529352427396b9b337a089a744220e51c681cc`  
		Last Modified: Tue, 21 Oct 2025 02:25:14 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:6d243fbb413967be61fe0b0a513233744a776501d82c1b803c0dcb43d50127c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7517316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:569d01455482107835b2bf9be53caa3dca5a40384317da6060a42a78d6a2a2e5`

```dockerfile
```

-	Layers:
	-	`sha256:9caa605cc8a09290442638415044e2cd09f3875ecc25265e0cf304cda6854898`  
		Last Modified: Tue, 21 Oct 2025 09:46:12 GMT  
		Size: 7.5 MB (7502961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6051d9c76980abbb6faba219c0ba4e65cdebf4ef45ed80031ef0bff4669431e`  
		Last Modified: Tue, 21 Oct 2025 09:46:13 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:7e8c4b593c9e1ad5cc15ca9a83d21bbfc63c2efe33e5a10dfb203f893a03c3b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191478684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b659d3490ceee2c5ade423e8fd63a8cad871dea9d50660ff6578098d31b918`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:812b25f785969d275d8c3962568c03f83ccc4df31b95f01c0646d79d6d5069f3`  
		Last Modified: Mon, 29 Sep 2025 23:33:30 GMT  
		Size: 52.3 MB (52326764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401ddd0af0f7ebbdbb14517b608732ced7b77f026bd12e988950f03c5eea95a4`  
		Last Modified: Fri, 10 Oct 2025 04:42:10 GMT  
		Size: 52.2 MB (52165400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b61e1614548b02ae50c714b219cda14d31bc55cc5fdb07679882917faf0d65`  
		Last Modified: Fri, 10 Oct 2025 04:49:13 GMT  
		Size: 87.0 MB (86985873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a6121c513a27b7934f556e6a28ea5aa57b12c61b7664d75a20ef8c80097732`  
		Last Modified: Fri, 10 Oct 2025 04:49:00 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9e438e9086ef28235ec33eb32a6b6b37fadd5d0cd9f80a721bf56d8e360bbc7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7516592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feed68d1cc62b08068989874a45be5d3b51724e9de325f2a4a03bcbce204fa8d`

```dockerfile
```

-	Layers:
	-	`sha256:d2ec13124939e3da7f545922a79e6ecaa341fa56ed434d3ef3b4cc8dc3494f83`  
		Last Modified: Fri, 10 Oct 2025 06:50:11 GMT  
		Size: 7.5 MB (7502307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8b7c12a15c9a658baebbc9ffed8f6b48be747b34f6cb750e22792804c2f5cf4`  
		Last Modified: Fri, 10 Oct 2025 06:50:12 GMT  
		Size: 14.3 KB (14285 bytes)  
		MIME: application/vnd.in-toto+json
