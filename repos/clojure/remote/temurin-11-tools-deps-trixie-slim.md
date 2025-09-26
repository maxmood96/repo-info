## `clojure:temurin-11-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:51e697b1e3349ba7fdfcc6ed4d1be517e9c751e488fbc0ffdeed3cc7ecf68aae
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

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:19bb1cf1c8e32d011cfb6f09785da705bc7450379ae1d5c7b97a5b503f80071c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 MB (247427282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0cb2452960e94df01cff7d278dfbbafe8b886fda5e1f9535c9b37de7aa71515`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc86ecd6b77c70fd81e3f3a422b0fefb7fd30d947154fb08135aa4af782137d`  
		Last Modified: Fri, 26 Sep 2025 17:55:25 GMT  
		Size: 145.7 MB (145658246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d655990d0e76380be1aca008bc772acb51bb6d33c303d0fb2c272557dfa08849`  
		Last Modified: Fri, 26 Sep 2025 17:56:07 GMT  
		Size: 72.0 MB (71994895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4480b9524cb037aeee62e27017af39a0bfcd20ee50ccd02eb0dbcc10e17eddca`  
		Last Modified: Fri, 26 Sep 2025 17:55:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2a12cbbdb6b25d6c049c7fc2b18930d71cb742477123b2353d30d13be64d5a0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5290540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b10d08de82380426d7d8679f3dd698ccd6c4da854ea8a652f2bd4c4c0636963a`

```dockerfile
```

-	Layers:
	-	`sha256:6b3398a5bb156a3e46b5989d78b8956543458b7e34d0ee886d66ae3a6fba8a13`  
		Last Modified: Fri, 26 Sep 2025 18:37:42 GMT  
		Size: 5.3 MB (5276254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e53ee7ada1905e30191aaa5c5cd9c960ecba035b01997aa727118dc2571e172b`  
		Last Modified: Fri, 26 Sep 2025 18:37:43 GMT  
		Size: 14.3 KB (14286 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9ffbb61b9edef3aa3b533a95ba08a88a33106f6953f042afa35b854cb906246e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.4 MB (244404411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:596fc2af36f4671460f1afbdb124255ba5571c44aaf7f8e13f6349b3684162fe`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e768f5bc5962050dc7cd7e82c8232f517b2f49b575cc96de5fcd6372840c3aa`  
		Last Modified: Fri, 26 Sep 2025 17:54:17 GMT  
		Size: 142.5 MB (142458757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a59d70bf72f1d2eff877d8793b876d8d19cafccbe655d08761db0f507273dc9`  
		Last Modified: Fri, 26 Sep 2025 17:54:49 GMT  
		Size: 71.8 MB (71808376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518ed59f9ca0a6eee9d045c57549a5f0f54002175fa8753ab3f3a24863c504fa`  
		Last Modified: Fri, 26 Sep 2025 17:54:28 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9b534c622977ba4367d2349d503af45353bff02f7ac1fb745a11c4025c5b2ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13e602b877dfa83d48cb2066ca6aa97906eebfbea7c1cb7490e41471f1338153`

```dockerfile
```

-	Layers:
	-	`sha256:e2b5cd66bc9e228c4d77dfbd973428eed866ad56afd69463542d73881bb3cfb2`  
		Last Modified: Fri, 26 Sep 2025 18:37:48 GMT  
		Size: 5.3 MB (5282641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42da2ca321710bc4b8ba1db64cb2d176ca3a592a816bdb084b76d4ca18c1d4ea`  
		Last Modified: Fri, 26 Sep 2025 18:37:49 GMT  
		Size: 14.4 KB (14403 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:881530c6e2e0aced2f4317eb1d19f7431c7dfa7552359394f40c5e79cec097bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243842500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf88555015bf967c9e9e5aba93d1c28dc429c43f89607f40fe638dedfe4fcfc`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
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
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd24a6000d0db05f3f61ca99b8bc75ccdd9e7e0398a4a8341532dc9e4de8562`  
		Last Modified: Fri, 26 Sep 2025 18:11:41 GMT  
		Size: 132.9 MB (132852806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8976f10d229e0b651f73661b528c9f6871ff08e60f10d0c1cee80eec07331108`  
		Last Modified: Fri, 26 Sep 2025 18:12:11 GMT  
		Size: 77.4 MB (77394698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd605aeb433f4b0c5e5a08dcf69844efa6fe832d6fd357c23fb84c3e36fd578`  
		Last Modified: Fri, 26 Sep 2025 18:12:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ae3e35359c163f17cbfe90be2cff00c7fe62b4aefa9829d98cdd1025ce1bf466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5294344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76dd277b145763d1985797f917c4f05784ce7831f4368fc506d7b21615b50b4e`

```dockerfile
```

-	Layers:
	-	`sha256:ef0905254ee1182bd0e829db764996e0c6ff4300f4837ff7d63f3ba0b08d0788`  
		Last Modified: Fri, 26 Sep 2025 21:36:36 GMT  
		Size: 5.3 MB (5280010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:113b91f19498a4afece6622177cb6b90fd41297d19c47657c858c5aec6854cfe`  
		Last Modified: Fri, 26 Sep 2025 21:36:37 GMT  
		Size: 14.3 KB (14334 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:3d762c2adf0ed817fa3385dc8e7d90ff9bdd0e184664e06de1c31c85c803d3e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228409575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f1aac4f77e5c821a74fa3da7699947e20e0e332e08d093d170f1b165199713`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
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
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75f5e71f328a32bd3c21f6959d2f275a0ac453b096e2b0d11b59fa89df37c1c`  
		Last Modified: Fri, 26 Sep 2025 18:58:22 GMT  
		Size: 125.6 MB (125622240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5890c85a9542fa9084b50af475839ee7ccc6c5da1ef9653e664444a921afeba9`  
		Last Modified: Fri, 26 Sep 2025 18:58:33 GMT  
		Size: 73.0 MB (72953784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84cda37a2b11d3a840aa8cd22cd7b301ac6bfd54336003b988d86ed0db1278e8`  
		Last Modified: Fri, 26 Sep 2025 18:58:28 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:40571b32f45e29ca9e63c6c7b9a0f96926481c2eb22fc196266a0944969fdd2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5286467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ff63c1049520963eee2ddf7d972adeafe6f7679b4cec5760d7ce36e3b0bf5e`

```dockerfile
```

-	Layers:
	-	`sha256:f046d62bd5ddc2b96d0132e5f7188cbc613ca50cb0df4b01010366d105a76ae6`  
		Last Modified: Fri, 26 Sep 2025 21:36:42 GMT  
		Size: 5.3 MB (5272182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aebb268046f39e07bb6896e63b4378e1aab10e67e9877fbf340e79e5513d6f3f`  
		Last Modified: Fri, 26 Sep 2025 21:36:43 GMT  
		Size: 14.3 KB (14285 bytes)  
		MIME: application/vnd.in-toto+json
