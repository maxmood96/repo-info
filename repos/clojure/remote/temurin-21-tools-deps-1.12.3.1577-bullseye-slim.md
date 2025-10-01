## `clojure:temurin-21-tools-deps-1.12.3.1577-bullseye-slim`

```console
$ docker pull clojure@sha256:3947617c5b824b73117df10844d3266e12ca2c464431c225db5491d50f42fe9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.3.1577-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:277fb7b7ddea09eb10d0eed7b486e9153309dc47d52f7f27d08cbd6ad82c0ff9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247214931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ced6e3f392db801c761bee89e28d916a53c11b36750b25e76e7494d31f3fb5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4eb1dd59a73886acc6a3cc9d4c8f8e66d1fd6ba6d6195b05ce21c22b0658aab8`  
		Last Modified: Mon, 29 Sep 2025 23:35:18 GMT  
		Size: 30.3 MB (30258363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:594877e74181dc366fddc9be3868ce080fc7dfe5049c5cf03e2ebbe0a2980d1a`  
		Last Modified: Wed, 01 Oct 2025 16:59:01 GMT  
		Size: 157.8 MB (157804763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff62f99c83644eda04a70d505e11f035e34ca16d33926a83dc2715abf358639`  
		Last Modified: Wed, 01 Oct 2025 16:58:59 GMT  
		Size: 59.2 MB (59150770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05f9fca922d3ee501e822f417f995dca568eb1a3f4c76c2c96b438034e385db`  
		Last Modified: Tue, 30 Sep 2025 01:41:46 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ea9a2dcf76f06b7fa63b6b17c6674869024ae850a8969223f94f0d251ea66a`  
		Last Modified: Tue, 30 Sep 2025 01:41:45 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bba886b5e6a167372b61571f9adda9d608f59b2d7a27d92b2f61eca1aa0230d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5327048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab605b96c1033d7aaffbb428c526320bd531dac614fef78416fe36cefe795b17`

```dockerfile
```

-	Layers:
	-	`sha256:35dfff4b4a50e2cce4c464cd8fa8ed961a3f990697be941c5ca0d5ac178b91ca`  
		Last Modified: Wed, 01 Oct 2025 15:39:39 GMT  
		Size: 5.3 MB (5311169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a855bbc5eb82e4f8448b7f4c78be66556a279ebc00b4187ce4512e70f0747ae`  
		Last Modified: Wed, 01 Oct 2025 15:39:40 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.3.1577-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:795ddd58ba094c7c9a12f3d20851251b657351a1c4c22484d268b85098f57e5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.1 MB (244115361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780cba5dd333a1acb04e4bb8cfd3267422516679963b1ad246e9fc8e537eefd5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:93b0b88e50eb7468103e583a7be2e8ee3fe5f86e6c74df4baca40a3685b5eee1`  
		Last Modified: Mon, 29 Sep 2025 23:34:34 GMT  
		Size: 28.7 MB (28748427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a401a4a426795e96f4ac52cdc52e7eb6b52eadd2682320f33d72feff47a9acd3`  
		Last Modified: Tue, 30 Sep 2025 00:54:08 GMT  
		Size: 156.1 MB (156081218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3e62bbaf1d51d88f526d2617f24fc76ba77550ea59910f3c1878cd3521f463`  
		Last Modified: Tue, 30 Sep 2025 00:54:23 GMT  
		Size: 59.3 MB (59284677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6fc4cae030d92db95ecbc7173aaa77192ef96548f420f820b9803f5a4e6e158`  
		Last Modified: Tue, 30 Sep 2025 00:54:19 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae0ee49d7d7a2ec780608027e40770ec4d59906db84484b4b86e7fa33c156f9`  
		Last Modified: Tue, 30 Sep 2025 00:54:19 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.3.1577-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e3a3a554756be776d656f3bb61ec1294f86b54aa2c6cd36d5425022f7d0670e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5332898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a4953e88949bc8c2f3acb6e838d035ac9a5cff679d9b977fad5382d8f530be`

```dockerfile
```

-	Layers:
	-	`sha256:c9f0f5fbed6af98fec00b6d30e4bca2488f10b4acb4a18ddf34e20a1c041f9b4`  
		Last Modified: Wed, 01 Oct 2025 12:35:55 GMT  
		Size: 5.3 MB (5316901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dd2300482f385d829175d307f660d840cf897aeb40e0f08445d7c014c977cc5`  
		Last Modified: Wed, 01 Oct 2025 12:35:56 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
