## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:f5d50ec5fd2cd558f6e154dadd1d4c713082577ea4503c23f573941dc7aa7a39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7639f726f153af7d3eb243326044567c4d91293c87f64efb7fd87403bf428964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234883966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9797429d1b159ee5530d8aab305297cd8c2b3efcc0035e56fc769ec5ddb1f114`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a333dbad3be2aeecd0c6a4a552c3e8d84fea1b4142a3ff171a6a8902ab425069`  
		Last Modified: Mon, 05 May 2025 17:08:14 GMT  
		Size: 145.6 MB (145635746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c197aeb92fb639b151e8eb45f60d10704d5669609d4cc34c46adda6b5559b1`  
		Last Modified: Mon, 05 May 2025 17:08:12 GMT  
		Size: 59.0 MB (58992971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4beba14f1694ddbdde32211f984649813342276e1012d0bc2234da1348e67f`  
		Last Modified: Mon, 05 May 2025 17:08:11 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:77c13bc997a3ee268efa9605d4080b95a17f3ffb41bcec38691f549892c7bc4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5153518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7298c7a64c8cb6675916f333b7799d1a5050ec7c8f3a81a7ecb6a7c5a2c6dfb3`

```dockerfile
```

-	Layers:
	-	`sha256:a0475a8eb311aed82c271163960c28d2f49ef9bc98a51c1ce17300937fcc5fd7`  
		Last Modified: Mon, 05 May 2025 17:08:11 GMT  
		Size: 5.1 MB (5139208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f79f56376212cabd7af8941d081f9419225f466fa5f7f9e3d617891c62b46ce3`  
		Last Modified: Mon, 05 May 2025 17:08:10 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c5189c8117fe049a57b9c8b8b460ca562243c4707d40d01eb7ef4c53d552e51f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230293588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe23693246ade0be2b8fe6f715dd3e19ec7c0e000d987061d1839ca5f77c4a3`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b561ac98db1022e14acafebccf18d2e70cfb7fd976f4944169fc6db0567635`  
		Last Modified: Mon, 05 May 2025 22:05:58 GMT  
		Size: 142.4 MB (142420730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43da759ade31cf93b18b1e9e39a99a6d12ed474db0d4c2cb283d4476e422dae`  
		Last Modified: Tue, 06 May 2025 00:30:08 GMT  
		Size: 59.1 MB (59127567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effec24006f3e6788a58180d2c977f5a4b7fd869939e42724e9a2ff8ba3b2b5c`  
		Last Modified: Tue, 06 May 2025 00:30:06 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b604da0a6380ddeddf74bb45855d8a660090d2a76dc7960d928f2f9a7713d8e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5159986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b7c0874aacfd3a675932ada4a9846e47bb0746e56c147deffda67bf10c69a1`

```dockerfile
```

-	Layers:
	-	`sha256:984c6e28be1e8f6bdbef83a545cb152ea9d8ea534925e22d219ad63e3b847c9b`  
		Last Modified: Tue, 06 May 2025 00:30:06 GMT  
		Size: 5.1 MB (5145558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be412bbab0d30fe9842e04e0410dce380bec269d66a90250142132204069ef6a`  
		Last Modified: Tue, 06 May 2025 00:30:06 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
