## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:325c5886ec65099e4fad441d8cfd8e90e5f45b780944db03eb31ad62d9d0fe73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4e7dd0ea2d225e1e9c0bd89207bd7b709a8d175f0b3ee6a2246631d1d4df09d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.4 MB (234377563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4f15f853927d11391459e9eba06695ac145122412aed8c1ceb3cbed06f75c53`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Sat, 08 Nov 2025 18:41:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:41:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:41:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:41:45 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:41:45 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:41:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:41:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:41:59 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6063e94ec9b46cd47efed243fe699115ab5d9e4ec6e454442879845577df3fcd`  
		Last Modified: Sun, 09 Nov 2025 03:15:59 GMT  
		Size: 145.0 MB (144966479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ca8c585d28d47ca5cd3a865fe341e8b49d23b7619f6d187791dacdd6b2c647`  
		Last Modified: Sat, 08 Nov 2025 18:43:02 GMT  
		Size: 59.2 MB (59151841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009fe3ebb7f7a22cdeb64d1dbd0e297db05b42c66af6f692b52dd1cf521aedf3`  
		Last Modified: Sat, 08 Nov 2025 18:42:36 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2f647746234fb76e4017af9b157f9a9b76f8d295ee2b093168123b23acd8c9f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5342475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:250dc4a16093ad48171b99e1f6f03630dd5d1720d33dd82999b40557c271e3f0`

```dockerfile
```

-	Layers:
	-	`sha256:acf6479b8139de334a84d099adaca00eeea59e8b8741ad7ae63a96280e2b23e8`  
		Last Modified: Sat, 08 Nov 2025 22:36:45 GMT  
		Size: 5.3 MB (5328208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:188e7d7373638555c21dafe3217a2d313830e6f1390d91148bb9ad4b1f761f4e`  
		Last Modified: Sat, 08 Nov 2025 22:36:46 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9361d097dc59ba302b771e6db99add38b1d3b4b7c8f50d689cd337b89a341b51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229768487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9becc58a780b55b04c0471b361ceacef0350bf6bcc65d4992ce962694c0bc63a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Sat, 08 Nov 2025 18:40:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:40:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:40:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:40:27 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:40:27 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:41:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:41:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:41:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80bb9194f6674674431ea98448ec2a03f513d26407580c44d18fda721496869a`  
		Last Modified: Sun, 09 Nov 2025 08:55:33 GMT  
		Size: 141.7 MB (141731669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb5c7b61a54568c004ac11169d3f99190f1f15c3f7a87a375f9eaa5156c714f`  
		Last Modified: Sat, 08 Nov 2025 18:41:59 GMT  
		Size: 59.3 MB (59287621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4e2fa03e65f2ea5ba34a70e91d382f2214dfd69c7348ea7d1cc2af871ccd9c`  
		Last Modified: Sat, 08 Nov 2025 18:41:56 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4a7f2b26de817efa6d97a7a064d253f6a392cfc5a83829ef4837bc4f004398d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5348142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f93c8c791bbdfa39c9355d0d66d422d2911cf0467a773f8e1c46b8a7f356033a`

```dockerfile
```

-	Layers:
	-	`sha256:eba9ea0db231725516295a26aae62b0902797a1250d42b9dae404d387dce7316`  
		Last Modified: Sat, 08 Nov 2025 22:36:51 GMT  
		Size: 5.3 MB (5334558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82bf19bdc40a001ef60cf051e2baf099ac730614422ef7b90fd9c1565a4abfb4`  
		Last Modified: Sat, 08 Nov 2025 22:36:51 GMT  
		Size: 13.6 KB (13584 bytes)  
		MIME: application/vnd.in-toto+json
