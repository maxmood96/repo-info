## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:01fd645731a49208d996d3f595aa1388e13813e7f5fb1cdf6bf46ce6264981a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:7196899d74fdba60daa27694d3dec48e9c8a7a074b850cccc2874694b79c915a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268974728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62dc9c3fcfa3de283cfb7ec5b9127708435ef1482e9a393b6e1d8c552f3db0a8`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
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
	-	`sha256:10ffc47270cd106d2d04bc7ef4749d579620e45a84804ba3b18f0898fe5ecc64`  
		Last Modified: Mon, 29 Sep 2025 23:35:07 GMT  
		Size: 53.8 MB (53756064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ca78b09a734640db748edcc48cc08672d56d45c4787f8433eadc0840ba5653`  
		Last Modified: Thu, 02 Oct 2025 13:15:08 GMT  
		Size: 145.7 MB (145658171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c27dc874015cdc92f052672cf988b958b6cc27c20c920779a37458859df9fc2`  
		Last Modified: Thu, 02 Oct 2025 13:15:06 GMT  
		Size: 69.6 MB (69559850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ed18321adcc5bfaab795df07cb4501d43fb1a1c04d79386b190d4a3116d92e`  
		Last Modified: Thu, 02 Oct 2025 13:14:54 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:52870dad2fbc248fbb4d2ee3f0b4e55d8d68c089bf48e1bdf989ed8f3c2706b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7430059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46eadd40f334e1fa40fd41daeb68a3f679f8236146578a2a7bfe26e3faf227ab`

```dockerfile
```

-	Layers:
	-	`sha256:97cb4d6d5c087cf0a693f336c23a5f3ffcde46f6ec95b69304982c7f9d13ec8a`  
		Last Modified: Thu, 02 Oct 2025 12:35:43 GMT  
		Size: 7.4 MB (7415808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7264faf120ebba0d53e73e7e68321eeaadff1438bd27c4f4c04a58380cf19e32`  
		Last Modified: Thu, 02 Oct 2025 12:35:44 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ae81df26061ca5e4ae29a8d2acc2546911002451e355e1648970009d8bcc7d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.4 MB (264403400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d731363aed5d9f48d3b8d69d40fa3e6f6cee8fb5b047567784a30f86e3da31a0`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1759104000'
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
	-	`sha256:9b16ae1bbd1ada84c12528379a10e280bd89e0d0332670c8487145eb77fe2fe1`  
		Last Modified: Mon, 29 Sep 2025 23:34:42 GMT  
		Size: 52.3 MB (52257414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041aa23cd45898d78616e7dd61fc8d86d6d516f40034a113caa0c0961fe7f8c0`  
		Last Modified: Thu, 02 Oct 2025 02:42:13 GMT  
		Size: 142.5 MB (142458701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e72c8838e8dfabfa74bc1f6310ca01983a4475f2f022b6a6712e9dfac1b8a0d`  
		Last Modified: Thu, 02 Oct 2025 02:42:26 GMT  
		Size: 69.7 MB (69686641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8493a659356194abd17565729cf37548e26b1b6fe40cd42fa4f50b86a106b4d3`  
		Last Modified: Thu, 02 Oct 2025 02:42:17 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d212b70450ba36c5c74aafe51953e376cb99aa646f688b078739f6d2a3483770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd8ed02e25ee49ac9c1a296c4bfd873d30867a7a144b9be3155a54e1b59e5dec`

```dockerfile
```

-	Layers:
	-	`sha256:12f0a7cbce6615b971cb38904c270a8f0d375573c9800836f969fc37d6a25a35`  
		Last Modified: Thu, 02 Oct 2025 06:35:58 GMT  
		Size: 7.4 MB (7421525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc275f37325d3e4b2420e299adab4869d4b39d8255170fe513808a1d0e27555a`  
		Last Modified: Thu, 02 Oct 2025 06:35:59 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
