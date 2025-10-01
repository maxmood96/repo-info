## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:491f27f63f74d60ac6f73785d93b789b0bfc9a31a041e447f375ae3cdd97e814
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:467b21062e1e495c6f58c961b68250e90147e87b5f14b2424b7c2cc426f69b6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268974690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f915e5761d0e97c365bdfdc3120c438745ede6b7f35ac5b703b616827421fd`
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
	-	`sha256:1c95dccd09a097f11bc9c7cd183a6e0f3e04340d2c9132646610471084e2a1b7`  
		Last Modified: Tue, 30 Sep 2025 00:51:51 GMT  
		Size: 145.7 MB (145658240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ea1c3e827e88c65f798b9ebdcf53571382ecb2f62455d4bce858ac017f80b6`  
		Last Modified: Tue, 30 Sep 2025 00:53:14 GMT  
		Size: 69.6 MB (69559742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552f7c20a6af0c84570a402f1448e7ab0b5db24d02ead480281a4a835686a23a`  
		Last Modified: Tue, 30 Sep 2025 00:53:05 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:851d49d021c3e244d2703d972bb325e3d2cb19ed4167559df9c37fda48eed3be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7429259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:517ea4df42111331d39ce6f67b089f0e52f3e8da9cccca7a301d96e09e54e22f`

```dockerfile
```

-	Layers:
	-	`sha256:10607c3cad232527f8ad4d322a507bd10e7d63a7375afb5899663a7322509975`  
		Last Modified: Wed, 01 Oct 2025 15:35:26 GMT  
		Size: 7.4 MB (7415808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fc099a8a17135d1abb47e19a831eecfa3dc1192365cb4fc20c80fb1d0693d1f`  
		Last Modified: Wed, 01 Oct 2025 15:35:27 GMT  
		Size: 13.5 KB (13451 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:19e2684ced190699551d1bd0ebc8617a4855847ca451ac7107f644e71d8cd4de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.4 MB (264396617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97007ead774f4e0429015cf966872ab0a90fca875f858607e8b6a250a4a5cc89`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
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
	-	`sha256:7df02cb4a974a4e8a9eb65ffcff7274f9dca341d29aaa763294c42e49805ca19`  
		Last Modified: Mon, 08 Sep 2025 21:15:41 GMT  
		Size: 52.2 MB (52248370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580affed27e1ec9ceb2673227e72486936fae24a676826bb6ee2185c3d7e28ac`  
		Last Modified: Sat, 27 Sep 2025 03:03:57 GMT  
		Size: 142.5 MB (142458757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29006b926175b5e9115131d33bf9df33dc55b3e0d6711d8c58f48702c5f518c1`  
		Last Modified: Fri, 26 Sep 2025 17:54:28 GMT  
		Size: 69.7 MB (69688846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37231d8307574fd20fd6767a44d251cca0c30c922b9b3abaf99f9fc7204bfb05`  
		Last Modified: Fri, 26 Sep 2025 17:54:18 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:4b7ed8beb2e55e638989e5f1a0090afb276ee7e605f309017e95ac83b2c71179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7435895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e3ad79a4bf0246ded07eec8015b2db61fef39c27ac4f7dd7b2480d3c934bcf`

```dockerfile
```

-	Layers:
	-	`sha256:c7ef003dfadd389d0799f090aeb0188239324b2fba455d15c866a72d52a3032a`  
		Last Modified: Fri, 26 Sep 2025 18:36:27 GMT  
		Size: 7.4 MB (7421525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff03fe1168b53520659ceae0eb16e7c856921c4a3ff26e5cefcec9fe44278dec`  
		Last Modified: Fri, 26 Sep 2025 18:36:28 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
