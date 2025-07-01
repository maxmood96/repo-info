## `clojure:temurin-8-bullseye`

```console
$ docker pull clojure@sha256:7651615179b674f0b6e8dac88369914ee7f30c0d084f6538d9337fd3a35ef623
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:c546d4272928c12d81b01da54218596abe5e84c51ebbe3254751b9d3b38f2425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177881738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e15e963334a5d0e133601e541b9bac0c1bea5cbb96e86dff48f02ef62dcc718f`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
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
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba5f63d5a372a59a6922700fcd57a6ac1e9959cff2df7bace48e34435adc69c`  
		Last Modified: Tue, 01 Jul 2025 13:00:39 GMT  
		Size: 54.7 MB (54716181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6477c2cc52ab3f95753d30c214ff82b66dbe72072953333090a21567ec2027fc`  
		Last Modified: Tue, 01 Jul 2025 13:00:44 GMT  
		Size: 69.4 MB (69410090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b784bf9126c711e4f7f0c3abb271781ea46379b3005fa23a330ede4264fdd457`  
		Last Modified: Tue, 01 Jul 2025 02:37:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:52516b81a0d05f7efa95c76bf49fca2c9a33626e18de6b9c7de2e931d7dca885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7531483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a318448816c759eb25800dc957724399540f73d0079b91e8d06780d9d6af79f4`

```dockerfile
```

-	Layers:
	-	`sha256:d3c2b6f2baff6d3fbc40497e5e6b61814d3ff0d5226e4f157db56e6cc797b9cb`  
		Last Modified: Tue, 01 Jul 2025 06:42:20 GMT  
		Size: 7.5 MB (7517248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56306a1f3af65c769762fe4766f3035e0457f6a825945cc6b9f8e8c90690c089`  
		Last Modified: Tue, 01 Jul 2025 06:42:21 GMT  
		Size: 14.2 KB (14235 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:983de7e3b5117170276b59dd28eb7c037455e3ba91c0e131e795d081d7a277a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.6 MB (175620893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44702d5904e78d42c73d9ffbae775f095bc834502b16f326dcfb87ec1e3f5394`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1751241600'
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
	-	`sha256:df45b4853b6fce6b81d1ac6218d861c6d7c8c14da4be409d42ee4bfdf0737e71`  
		Last Modified: Tue, 01 Jul 2025 01:15:18 GMT  
		Size: 52.3 MB (52252254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2173dace57cd95f6b961f519b1831f8dc02594b745e5fa3f8192bc4de9f28be3`  
		Last Modified: Tue, 01 Jul 2025 11:57:44 GMT  
		Size: 53.8 MB (53830497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4b041a3f8343ff45f280c19af39f36ebba4cf3131ece43b5d5861ed9fb277d`  
		Last Modified: Tue, 01 Jul 2025 12:02:30 GMT  
		Size: 69.5 MB (69537500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd0743695a959fd4d850d6708ea93f9d00ace096f77607c3e81460dc8f64389`  
		Last Modified: Tue, 01 Jul 2025 12:02:27 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e8f1fe5a7d2076d4dd1f89af0ecf6132430cfae81cbc37736971a40b23334154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7537400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e884fadd88dd099b5bcf3b89e9ffc5770e530b87ccefb40f0f57ed573f1c926`

```dockerfile
```

-	Layers:
	-	`sha256:c20f0594c6a838e0ef7869ab20b5dd4cf5a76ed0ac7a55eb722f2efee85eb869`  
		Last Modified: Tue, 01 Jul 2025 12:38:50 GMT  
		Size: 7.5 MB (7523045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a154584ddeaf9f6096c8a6084e31369650d87e1da8cfa87d9cef2392f384135`  
		Last Modified: Tue, 01 Jul 2025 12:38:51 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json
